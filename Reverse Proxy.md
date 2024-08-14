Xây dựng mô hình reverse proxy kết hợp giữa 2 webserver là nginx và apache, php 8.1, mysql và phpmyadmin 

Thao tác xây dựng 2 web với 2 domain - sử dụng vhost (domain các bạn chủ động trỏ về IP VPS)
+ 1 Website chạy wordpress
+ 1 Website chạy laravel

Bất kỳ domain nào khác khi trỏ về IP VPS hoặc truy cập qua IP phải cần qua 1 default vhost.
  + mysql (bật remote mysql từ xa)
  + cho phép truy cập port 80, 443, 3306, 22

------		

### Cài đặt apache

	sudo apt install apache2 -y

Kiểm tra trạng thái

	sudo systemctl status apache2

### Cài đặt php8.1
**Thêm repository để cài đặt PHP 8.1:**

	sudo add-apt-repository ppa:ondrej/php
	sudo apt update

**Cài đặt PHP 8.1 và các module cần thiết:**

	sudo apt install php8.1 php8.1-cli php8.1-common php8.1-mysql php8.1-xml php8.1-curl php8.1-mbstring php8.1-zip -y


**Kiểm tra phiên bản PHP đã cài:**

	php -v

### Cài đặt mysql

**Cài đặt MySQL Server:**

	sudo apt install mysql-server -y

**Bảo mật MySQL:**

	sudo mysql_secure_installation

**Tạo cơ sở dữ liệu cho WordPress và Laravel:**
Đăng nhập vào MySQL:

	sudo mysql -u root -p

Tạo cơ sở dữ liệu:

	CREATE DATABASE wordpress_db;
	CREATE DATABASE laravel_db;
Tạo người dùng và cấp quyền:
	
	CREATE USER 'wp_user'@'localhost' IDENTIFIED BY 'password';
	CREATE USER 'laravel_user'@'localhost' IDENTIFIED BY 'password';

	GRANT ALL PRIVILEGES ON wordpress_db.* TO 'wp_user'@'localhost';
	GRANT ALL PRIVILEGES ON laravel_db.* TO 'laravel_user'@'localhost';

	FLUSH PRIVILEGES;
	EXIT;

**Cài đặt phpMyAdmin**

	sudo apt install phpmyadmin -y

### Thiết lập Virtual Hosts cho hai website
**Đổi port cho Apache từ 80 sang 8080** 

	nano /etc/apache2/ports.conf 
	
	Listen 8080

	<IfModule ssl_module>
	        Listen 8443
	</IfModule>

	<IfModule mod_gnutls.c>
	        Listen 8443
	</IfModule>

**Tạo file cấu hình cho `khoa.vietnix.xyz` (WordPress):**

	sudo nano /etc/apache2/sites-available/khoa.vietnix.xyz.conf
	
	<VirtualHost *:8080>
	    ServerName khoa.vietnix.xyz
	    DocumentRoot /var/www/khoa.vietnix.xyz

	    <Directory /var/www/khoa.vietnix.xyz>
	        AllowOverride All
	        Require all granted
	    </Directory>

	    ErrorLog ${APACHE_LOG_DIR}/khoa_error.log
	    CustomLog ${APACHE_LOG_DIR}/khoa_access.log combined
	</VirtualHost>

**Tạo file cấu hình cho `koa.vietnix.xyz` (Laravel):**

	sudo nano /etc/apache2/sites-available/koa.vietnix.xyz.conf

	<VirtualHost *:8080>
	    ServerName koa.vietnix.xyz
	    DocumentRoot /var/www/koa.vietnix.xyz

	    <Directory /var/www/koa.vietnix.xyz>
	        AllowOverride All
	        Require all granted
	    </Directory>

	    ErrorLog ${APACHE_LOG_DIR}/koa_error.log
	    CustomLog ${APACHE_LOG_DIR}/koa_access.log combined
	</VirtualHost>
	
**Tạo file .htaccess để trỏ vào thư mục Public trong Lavarel** 

	nano /var/www/koa.vietnix.xyz/.htaccess 
	
	<IfModule mod_rewrite.c>
	RewriteEngine On

	RewriteCond %{REQUEST_URI} !/public
	RewriteRule ^(.*)$ public/$1 [L]

	</IfModule>

**Kích hoạt các Virtual Hosts:**

	sudo a2ensite khoa.vietnix.xyz.conf
	sudo a2ensite koa.vietnix.xyz.conf
	sudo systemctl reload apache2

### Cài đặt WordPress và Laravel

**Cài đặt WordPress:**
-   Tải về và cài đặt WordPress tại `/var/www/khoa.vietnix.xyz`.
-   Điều chỉnh quyền sở hữu thư mục:

		sudo chown -R www-data:www-data /var/www/khoa.vietnix.xyz

**Cài đặt Laravel:**
-   Tạo dự án Laravel tại `/var/www/koa.vietnix.xyz`.
-   Điều chỉnh quyền sở hữu thư mục:

		sudo chown -R www-data:www-data /var/www/koa.vietnix.xyz

**Tải về và giải nén WordPress:**

	cd /var/www/
	sudo wget https://wordpress.org/latest.tar.gz
	sudo tar -xvzf latest.tar.gz
	sudo mv wordpress khoa.vietnix.xyz

**Điều chỉnh quyền sở hữu thư mục:**

	sudo chown -R www-data:www-data /var/www/khoa.vietnix.xyz

**Cấu hình WordPress:**
Sao chép file cấu hình mẫu:

	cd /var/www/khoa.vietnix.xyz
	sudo cp wp-config-sample.php wp-config.php

Mở và chỉnh sửa file `wp-config.php`:

	sudo nano wp-config.php

Tìm và cập nhật các giá trị sau:
	
	define('DB_NAME', 'wordpress_db');
	define('DB_USER', 'wp_user');
	define('DB_PASSWORD', 'password');
	define('DB_HOST', 'localhost');

Lưu và thoát.

### Cài đặt Laravel
**Cài đặt Composer (nếu chưa cài đặt):**

	sudo apt install curl php-cli php-mbstring git unzip -y
	cd ~
	curl -sS https://getcomposer.org/installer -o composer-setup.php
	sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
Tạo dự án Laravel:
	
	cd /var/www/
	sudo composer create-project --prefer-dist laravel/laravel koa.vietnix.xyz

**Điều chỉnh quyền sở hữu thư mục:**

	sudo chown -R www-data:www-data /var/www/koa.vietnix.xyz
	sudo chmod -R 755 /var/www/koa.vietnix.xyz

**Cấu hình kết nối database cho Laravel:**

Mở file `.env` trong thư mục Laravel:
	
	cd /var/www/koa.vietnix.xyz
	sudo nano .env

Cập nhật các giá trị sau:

	APP_URL=http://koa.vietnix.xyz

	DB_CONNECTION=mysql
	DB_HOST=127.0.0.1
	DB_PORT=3306
	DB_DATABASE=laravel_db
	DB_USERNAME=laravel_user
	DB_PASSWORD=password

**Chạy migrations để tạo bảng trong database:**
	
	cd /var/www/koa.vietnix.xyz
	php artisan migrate

**Cài đặt Nginx**

	sudo apt install nginx -y

**Khởi động và kích hoạt Nginx:**

	sudo systemctl start nginx
	sudo systemctl enable nginx

**Cấu hình Nginx làm Reverse Proxy**
Tạo file cấu hình cho `khoa.vietnix.xyz` (WordPress):
	
	sudo nano /etc/nginx/sites-available/khoa.vietnix.xyz
	
	server {
	    listen 80;
	    server_name khoa.vietnix.xyz;

	    location / {
	        proxy_pass http://127.0.0.1:8080;
	        proxy_set_header Host $host;
	        proxy_set_header X-Real-IP $remote_addr;
	        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
	        proxy_set_header X-Forwarded-Proto $scheme;
	    }
	}

Tạo file cấu hình cho `koa.vietnix.xyz` (Laravel):

	sudo nano /etc/nginx/sites-available/koa.vietnix.xyz

	server {
	    listen 80;
	    server_name koa.vietnix.xyz;

	    location / {
	        proxy_pass http://127.0.0.1:8080;
	        proxy_set_header Host $host;
	        proxy_set_header X-Real-IP $remote_addr;
	        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
	        proxy_set_header X-Forwarded-Proto $scheme;
	    }
	}

**Kích hoạt các cấu hình Nginx:**

Tạo liên kết symbol từ thư mục `sites-available` đến `sites-enabled`:

	sudo ln -s /etc/nginx/sites-available/khoa.vietnix.xyz /etc/nginx/sites-enabled/
	sudo ln -s /etc/nginx/sites-available/koa.vietnix.xyz /etc/nginx/sites-enabled/
**Kiểm tra cấu hình Nginx:**

	sudo nginx -t

**Khởi động lại Nginx:**

	sudo systemctl restart nginx

### Cấu hình SSL cho các domain
Cài đặt Certbot (nếu chưa cài đặt):

	sudo apt install certbot python3-certbot-nginx -y

Cài đặt SSL cho `khoa.vietnix.xyz`:

	sudo certbot --nginx -d khoa.vietnix.xyz

Cài đặt SSL cho `koa.vietnix.xyz`:

	sudo certbot --nginx -d koa.vietnix.xyz

### Kiểm tra lại các file cấu hình trong Aache và Nginx
**Nginx**

 /etc/nginx/sites-enabled/khoa.vietnix.xyz  

	server {
	    server_name khoa.vietnix.xyz;

	  listen 443 ssl; # managed by Certbot
	    ssl_certificate /etc/letsencrypt/live/khoa.vietnix.xyz/fullchain.pem; # managed by Certbot
	    ssl_certificate_key /etc/letsencrypt/live/khoa.vietnix.xyz/privkey.pem; # managed by Certbot
	    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
	    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot

	        location ~* \.(gif|jpg|jpeg|png|ico|wmv|3gp|avi|mpg|mpeg|mp4|flv|mp3|mid|js|css|html|htm|wml)$ {
	        root /var/www/khoa.vietnix.xyz/wordpress;
	        expires 30d;
	    }
	    location / {
	        proxy_pass https://localhost:8443;
	        proxy_set_header Host $host;
	        proxy_set_header X-Real-IP $remote_addr;
	        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
	        proxy_set_header X-Forwarded-Proto $scheme;
	    }
	}
	server {
	    if ($host = khoa.vietnix.xyz) {
	        return 301 https://$host$request_uri;
	    } # managed by Certbot
	    
	    listen 80;
	    server_name khoa.vietnix.xyz;
	    return 404; # managed by Certbot
	}



/etc/nginx/sites-enabled/koa.vietnix.xyz 
	
	server {
	    server_name koa.vietnix.xyz;

	        location ~* \.(gif|jpg|jpeg|png|ico|wmv|3gp|avi|mpg|mpeg|mp4|flv|mp3|mid|js|css|html|htm|wml)$ {
	        root /var/www/koa.vietnix.xyz;
	        expires 30d;
	    }
	    location / {
	        proxy_pass https://localhost:8443;
	        proxy_set_header Host $host;
	        proxy_set_header X-Real-IP $remote_addr;
	        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
	        proxy_set_header X-Forwarded-Proto $scheme;
	    }
	    listen 443 ssl; # managed by Certbot
	    ssl_certificate /etc/letsencrypt/live/koa.vietnix.xyz/fullchain.pem; # managed by Certbot
	    ssl_certificate_key /etc/letsencrypt/live/koa.vietnix.xyz/privkey.pem; # managed by Certbot
	    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
	    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot
	}
	server {
	    if ($host = koa.vietnix.xyz) {
	        return 301 https://$host$request_uri;
	    } # managed by Certbot

	    listen 80;
	    server_name koa.vietnix.xyz;
	    return 404; # managed by Certbot
	}

**Apache**

/etc/apache2/sites-available/khoa.vietnix.xyz.conf 
	
	<VirtualHost *:8080>
	    ServerAdmin admin@khoa.vietnix.xyz
	    ServerName khoa.vietnix.xyz
	    DocumentRoot /var/www/khoa.vietnix.xyz/wordpress

	    <Directory /var/www/khoa.vietnix.xyz>
	        Options Indexes FollowSymLinks
	        AllowOverride All
	        Require all granted
	    </Directory>

	    ErrorLog ${APACHE_LOG_DIR}/khoa.vietnix.xyz_error.log
	    CustomLog ${APACHE_LOG_DIR}/khoa.vietnix.xyz_access.log combined

	</VirtualHost>

	 <IfModule mod_ssl.c>
	<VirtualHost *:8443>
	    ServerName khoa.vietnix.xyz
	   DocumentRoot /var/www/khoa.vietnix.xyz/wordpress

	        <Directory /var/www/khoa.vietnix.xyz/wordpress>
	            Options Indexes FollowSymLinks
	            AllowOverride All
	            Require all granted
	        </Directory>
	    SSLEngine on
	    SSLCertificateFile /etc/letsencrypt/live/khoa.vietnix.xyz/fullchain.pem
	    SSLCertificateKeyFile /etc/letsencrypt/live/khoa.vietnix.xyz/privkey.pem
	    # Các chỉ thị SSL khác
	    SSLOptions +StrictRequire
	    SSLProtocol all -SSLv2 -SSLv3
	    SSLCipherSuite HIGH:!aNULL:!MD5
	    SSLHonorCipherOrder on

	    # Thêm các cấu hình khác nếu cần
	         ErrorLog ${APACHE_LOG_DIR}/khoa.vietnix.xyz_ssl_error.log
	    CustomLog ${APACHE_LOG_DIR}/khoa.vietnix.xyz_ssl_access.log combined

	</VirtualHost>
	</IfModule>

  /etc/apache2/sites-available/koa.vietnix.xyz.conf    

	<VirtualHost *:8080>
	    ServerAdmin admin@koa.vietnix.xyz
	    ServerName koa.vietnix.xyz
	    DocumentRoot /var/www/koa.vietnix.xyz

	    <Directory /var/www/koa.vietnix.xyz>
	        Options Indexes FollowSymLinks
	        AllowOverride All
	        Require all granted
	    </Directory>

	    ErrorLog ${APACHE_LOG_DIR}/koa.vietnix.xyz_error.log
	    CustomLog ${APACHE_LOG_DIR}/koa.vietnix.xyz_access.log combined
	</VirtualHost>

	 <IfModule mod_ssl.c>
	<VirtualHost *:8443>
	    ServerName koa.vietnix.xyz
	   DocumentRoot /var/www/koa.vietnix.xyz

	        <Directory /var/www/koa.vietnix.xyz>
	            Options Indexes FollowSymLinks
	            AllowOverride All
	            Require all granted
	        </Directory>


	    SSLEngine on
	    SSLCertificateFile /etc/letsencrypt/live/koa.vietnix.xyz/fullchain.pem
	    SSLCertificateKeyFile /etc/letsencrypt/live/koa.vietnix.xyz/privkey.pem

	    # Các chỉ thị SSL khác
	    SSLOptions +StrictRequire
	    SSLProtocol all -SSLv2 -SSLv3
	    SSLCipherSuite HIGH:!aNULL:!MD5
	    SSLHonorCipherOrder on

	    # Thêm các cấu hình khác nếu cần
	         ErrorLog ${APACHE_LOG_DIR}/koa.vietnix.xyz_ssl_error.log
	    CustomLog ${APACHE_LOG_DIR}/koa.vietnix.xyz_ssl_access.log combined

	</VirtualHost>
	</IfModule>

















































































































