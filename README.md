![Chụp màn hình từ 2024-08-05 08-55-32](https://github.com/user-attachments/assets/39a1e305-6080-41fd-b26c-598bb37fb5e7)
## Hosting
Hosting hay web hosting là không gian lưu trữ dữ liệu được chia nhỏ từ các máy chủ (server), giúp đăng tải dữ liệu và xuất bản website, app trên Internet. Khi đăng ký dịch vụ hosting, nghĩa là đang thuê một chỗ đặt chứa tất cả các file và dữ liệu cần thiết lên trên server để website có thể hoạt động được 24/7.
Tất cả các website của nhiều khách hàng đều dùng chung tài nguyên của máy chủ như CPU ​​và RAM.

### Cơ bản thì hosting hoạt động từ 3 phía: người dùng, nhà cung cấp dịch vụ và người thuê hosting.
1. Đối với khách hàng truy cập website

Sau khi hoàn thành quá trình mua hosting và tải lên dữ liệu lên trang web, thì website của bạn về cơ bản sống trên một máy chủ. Người dùng có thể truy cập trang web đó bằng cách nhập địa chỉ trang web (tên miền) tương ứng vào trình duyệt web. Khi nhận được truy vấn, máy tính của họ sẽ kết nối với máy chủ mà trang web được lưu trữ.

Sau đó, đến lượt máy chủ gửi các tệp đã lưu trữ trên bộ nhớ để hiển thị cho khách truy cập web. Giả sử khách truy cập muốn xem blog, máy chủ sẽ gửi blog đến màn hình trình duyệt của họ. Sau khi đã chọn một bài đăng trên blog cụ thể, máy chủ sẽ hiển thị bài đăng đó trên màn hình của khách hàng. 

2. Đối với nhà cung cấp dịch vụ hosting

Ở phía nhà cung cấp dịch vụ hosting, sẽ có trách nhiệm chuẩn bị hệ thống server lưu trữ cho người thuê hosting. Thường thì các gói hosting tại thị trường Việt Nam sẽ được tạo ra bằng cách chia sẻ tài nguyên của server đích thành các không gian lưu trữ nhỏ hơn gọi là Shared Hosting.

Nhà cung cấp sẽ tiến hành cấu hình và chia nhỏ dịch vụ hosting của họ ra nhiều gói khác nhau theo cấp bậc tăng dần. Mỗi loại gói sẽ đi kèm với khoản chi phí hosting tương ứng với cấu hình. Trong quá trình sử dụng web hosting, nếu người thuê có nhu cầu nâng cấp để đáp ứng nhu cầu phát triển thì nhà cung cấp sẽ tiến hành điều chỉnh cho phù hợp.

3. Đối với người thuê hosting

Về phía người sử dụng hosting, họ chỉ cần tiến hành upload các file và dữ liệu liên quan lên không gian lưu trữ của mình sau đó cấu hình hoạt động cho phù hợp. Thông thường, web hosting sẽ được thuê để lưu trữ các trang web. Trong trường hợp này, người thuê sẽ tiến hành xây dựng trang web và điều chỉnh để website phù hợp với mục đích ban đầu, có thể là kinh doanh, blog, tin tức,…

## Virtual Hosts

Virtual Host là một dạng lưu trữ mà bạn lưu được nhiều domain khác nhau trên cùng một máy chủ serer. Hiện nay Virtual host được xem là một giải pháp tiết chi phí vì nó cho phép bặn nhúng nhiều domain trên một địa chỉ IP trong một Server. Server sẽ tự động hiểu tên miền nào đang vận hành bên trong vị trí lưu trữ Server tuỳ theo cách cài đặt của bạn.

Virtual Hosts được xem là một giải pháp tối ưu vừa tiết kiệm chi phí vừa được trải nghiệm tốt khi sử dụng nhiều tên miền chỉ trên một địa chỉ IP của Server. Bên cạnh đó, Virtual Hosting còn mang đến khá nhiều lợi ích trong quá trình sử dụng như:

- Bạn có thể dễ dàng thao tác vào một thư mục lưu trữ Code nào và không phải copy Code vào htdocs trong giao diện XAMPP.
- Trong quá trình thiết lập ban đầu, nếu bạn phân vùng lưu trữ Code ở một Folder Code nhất định, thì bạn sẽ không tốn thời gian sao lưu lại dữ liệu trong Folder Code khi cài đặt lại hệ điều hành Window.

### Cách thức vận hành của Virtual Host

Có nhiều cách khác nhau để xác định cấu hình của một Virtual Host, nhưng cách được sử dụng thông dụng ngày nay là:

- IP Based.
- Port – Based.
- Name Based.

#### IP Based

IP-Based Virtual Hosts (xác định website dựa theo IP): Đây là phương pháp đơn giản nhất trong 3 phương pháp, Một IP sử dụng cho 1 Website. Máy chủ web sẽ chịu trách nhiệm ánh xạ IP được yêu cầu có đế đến đúng website mong muốn hay không. Vì thế, mỗi trang web sẽ được định nghĩa bởi 1 IP duy nhất nhằm tránh những vấn đề không đáng có cho trang web liên quan đến địa chỉ IP. Tuy nhiên IP-Based (dùng trên 1 máy chủ) cần thiết lập Virtual Interface trên 1 máy chủ để có thể sử dụng được nhiều IP.

#### Port Based

Port Based tương đương với IP-Based, nhưng sự khác biệt ở phương thức này là có thể quản lý nhiều trang web dựa theo số Port được định nghĩa cùng với IP hoặc tên miền. Ngoài ra, Port sử dụng tránh lặp lại với Port được mặc định của ứng dụng khác khi đang hoạt động.

#### Name Based

Name Based (xác định website dựa theo tên – Domain Name): Nhiều website sử dụng chung 1 IP. Server sẽ đối chiếu http header từ client yêu cầu để ánh xạ đến đúng website được chỉ định theo Domain. Cho nên, Name-Based rất được ưa thích trong việc quản lý nhiều trang web trên cùng 1 máy chủ và trước tình trạng thế giới đang dần cạn kiệt IP Public, đồng thời sử dụng tối đa tài nguyên hiện có. Hạn chế lớn nhất khi bạn dùng IP chung, nếu gặp vấn đề thì tất cả các trang web của bạn đều sẽ bị ảnh hưởng theo.

    
## SEO Hositng 

SEO Hosting là giải pháp hosting được tạo rả giúp cho các website cần tối ưu SEO

Mỗi tài khoản hosting sẽ có nhiều địa chỉ IP giúp chạy nhiều website trên cùng một tài khoản và các website sẽ có range IP khác nhau, không bị Google footprint.

## Email hositng

Email hosting là một dịch vụ trong đó nhà cung cấp dịch vụ hosting thuê các email server cho người dùng của mình.

Doanh nghiệp lớn thường chạy các dịch vụ email hosting theo tên miền của họ để tăng độ uy tín và chuyên nghiệp.


## VPS
VPS (Virtual Private Server) hay máy chủ ảo riêng, là một loại dịch vụ lưu trữ web phân vùng máy chủ vật lý thành nhiều máy ảo, mỗi máy có tài nguyên chuyên dụng riêng, bao gồm CPU, RAM, bộ lưu trữ và hệ điều hành. Công nghệ ảo hóa này cho phép mỗi VPS có thể hoạt động độc lập, cung cấp cho người dùng những lợi ích to lớn như khả năng kiểm soát và tính linh hoạt cao hơn so với dịch vụ Shared hosting.

### Cách hoạt động của VPS
1. Ảo hoá: Công nghệ ảo hoá đóng vai trò quan trọng trong việc tạo ra các VPS. Ban đầu, công ty cung cấp VPS sẽ cài đặt phần mềm ảo hoá trên hệ điều hành (OS) của máy chủ vật lý để chia server thành nhiều máy ảo VPS riêng biệt. Và mỗi VPS sẽ được mô phỏng như một máy tính hoàn chỉnh với CPU, RAM, ổ cứng và hệ điều hành riêng. Các phần mềm ảo hoá cho VPS phổ biến trên thị trường như: VMWare, Hyper – V, KVM.

2. Phân bổ tài nguyên: Khi thuê một VPS, bạn sẽ được cung cấp một lượng tài nguyên nhất định, bao gồm CPU, RAM, dung lượng ổ cứng và băng thông (Bandwidth). Tài nguyên này đã được phân bổ riêng biệt cho từng gói VPS bạn thuê nên sẽ không chia sẻ tài nguyên này với bất kỳ VPS nào đang hoạt động trên cùng một máy chủ.
  
3. Hệ điều hành và phần mềm: Về hệ điều hành, bạn có thể cài đặt hệ điều mình và phần mềm mong muốn trên VPS của mình. Mặc định ban đầu các gói VPS sẽ có sẵn hệ điều hành Windows và Linux.
   
4. Quản lý VPS: Khi quản lý VPS, bạn có quyền truy cập root/admin vào VPS của mình, cho phép bạn kiểm soát hoàn toàn cấu hình và quản trị hệ thống thông qua giao diện web hoặc dòng lệnh. Hiện tại khi thuê VPS Vietnix bạn sẽ được sử dụng Control Panel để quản lý VPS của mình đó là DirectAdmin giúp bạn quản lý dễ dàng và được tích hợp nhiều tính năng hỗ trợ.

### Lợi ích sử dụng VPS
* Kiểm soát nâng cao và tính linh hoạt: Dịch vụ VPS cấp cho người dùng quyền truy cập root vào máy ảo của họ, cho phép họ tùy chỉnh môi trường máy chủ, cài đặt phần mềm cụ thể và định cấu hình cài đặt nếu cần. Tính năng kiểm soát chi tiết này không thể thực hiện được với dịch vụ lưu trữ chia sẻ.
* Cải thiện hiệu suất và khả năng mở rộng: Người dùng VPS có các tài nguyên chuyên dụng, bao gồm CPU, RAM và bộ nhớ, đảm bảo hiệu suất ổn định và loại bỏ tắc nghẽn tài nguyên thường gặp trong môi trường Shared Hosting. Ngoài ra, dịch vụ lưu trữ VPS có thể dễ dàng tăng hoặc giảm quy mô để đáp ứng nhu cầu luôn biến động.
* Tăng cường bảo mật và độ tin cậy: Người dùng VPS có các tài nguyên chuyên cung cấp một môi trường biệt lập và an toàn hơn so với Shared Hosting. Mỗi máy ảo sẽ hoạt động độc lập, giảm nguy cơ vi phạm bảo mật và các vấn đề về hiệu suất do người dùng khác trên máy chủ gây ra.
  
### Ứng dụng của VPS
* Đối với máy chủ game
* Tạo ra môi trường ảo cho quy trình lập trình, phân tích, nghiên cứu sản phẩm
* Lưu trữ website đa dịch vụ
* Làm nơi lưu trữ các dữ liệu: Tài liệu, video, hình ảnh, data riêng
* Phát triển Platform
* Sử dụng cho hệ thống email doanh nghiệp
* Các chương trình truyền thông online

### Các thông số cần biết khi thuê máy chủ ảo VPS
  * CPU
  * RAM
  * SWAP
  * Ổ cứng
  * Băng thông
  * IP
  * Thời gian uptime của máy ảo
  * Hệ điều hành
  * Sao lưu dữ liệu (backup)

## Máy chủ (Server)
Server còn được gọi là máy chủ là một máy tính (phần cứng và phần mềm) được kết nối mạng máy tính hoặc Internet. Trên máy chủ cài đặt thêm các phần mềm hệ thống hay một máy tính chuyên dụng. Hoặc nhiều máy tính nối mạng có khả năng lưu trữ để phục vụ và cung cấp các dịch vụ và tài nguyên cho các máy tính khác truy cập.

### Hệ thống server gồm
**Mainboard server (Bo mạch chủ)**
* Kết nối và truyền dẫn giữa các thiết bị trong máy.
* Có khe socket cho các bo mạch phụ, kênh truyền dữ liệu, bộ xử lý, khe chứa bộ nhớ, giao diện cho các thiết bị ngoại vi.
* Có thể tích hợp các mạch điều khiển cho modem, âm thanh, card màn hình.
* Kết nối và truyền dẫn giữa các thiết bị trong máy.
* Có khe socket cho các bo mạch phụ, kênh truyền dữ liệu, bộ xử lý, khe chứa bộ nhớ, giao diện cho các thiết bị ngoại vi.
* Có thể tích hợp các mạch điều khiển cho modem, âm thanh, card màn hình.

**RAM (Bộ nhớ truy cập ngẫu nhiên)**
* Quyết định khả năng xử lý của máy chủ tại một thời điểm.
* Có 2 loại chính là SDR và DDR, với DDR có tốc độ truyền dữ liệu nhanh hơn.
* RAM server thường có chức năng ECC để kiểm tra và sửa lỗi.

**Chassis server**
* Bảo vệ các thiết bị phần cứng bên trong máy.
* Có các loại như Rack Mount, Tower server, Blade server tùy thuộc vào kích thước và mục đích sử dụng.

**HDD server (Ổ cứng máy chủ)**
* Lưu trữ dữ liệu, hệ điều hành, phần mềm ứng dụng và dữ liệu người dùng.
* Có thể gắn nhiều HDD để tăng dung lượng lưu trữ.
* Sử dụng chuẩn giao tiếp cao như SCSI để tăng tốc độ và đảm bảo kết nối trong hệ thống mạng LAN.

**Card RAID**
* Kết hợp các ổ cứng thành một hệ thống nhất với cơ chế sao lưu và chống lỗi.
* Bảo vệ dữ liệu khi có sự cố vật lý xảy ra.

Tất cả các thành phần này là những yếu tố quan trọng để xây dựng và duy trì một hệ thống server ổn định và hiệu quả.

### Vai trò của máy chủ 
Vai trò chính của máy chủ (server) là lưu trữ, cung cấp và xử lý dữ liệu rồi chuyển đến các máy trạm liên tục 24/7 cho người dùng hay một tổ chức thông qua mạng LAN hoặc Internet. Máy chủ được thiết kế để có thể chạy liên tục trong thời gian dài và chỉ tắt khi có sự cố gì đó cần bảo trì.

Máy chủ là bộ phận quan trọng đối với công ty/doanh nghiệp trong việc lưu trữ cơ sở dữ liệu, thông tin, quản lý và vận hành những phần mềm của doanh nghiệp. Chỉ cần tối ưu phần cứng cho hệ thống máy chủ mà không cần phải đầu tư chi phí nhiều các máy trạm khác.

### Mô hình hoạt động của hệ thống máy chủ
Các máy chủ thường hoạt động trong mô hình Client – Server (máy khách – máy chủ). Máy khách kết nối với máy chủ thông qua hạ tầng mạng sử dụng giao thức IP (Internet Protocol), một máy chủ hoạt động như một socket listener. 

![ảnh](https://github.com/user-attachments/assets/643364e7-bd88-4dc9-a186-aab498355257)

Thông qua mạng hoặc internet các máy chủ cung cấp dịch vụ thiết yếu cho người dùng hoặc cá nhân trong tổ chức. Khi cần, một mô hình thay thế là mạng peer-to-peer cho phép các máy tính hoạt động như một trong hai Server hoặc Client.

### Phân loại máy chủ
Hiện nay, có nhiều loại máy chủ khác nhau, để dựa vào phương pháp tạo thành hệ thống máy chủ thì máy chủ được chia thành 3 loại chung như sau:

**Máy chủ vật lý (Dedicated Server)**
Là máy chủ chạy trên phần cứng như RAM, HDD, CPU, Card mạng,… Tất cả đều phụ thuộc vào phần cứng, khi hư hỏng hay thay đổi cấu hình máy chủ và nâng cấp đều phải thay đổi phần cứng của máy chủ.

**Máy chủ ảo (VPS – Virtual Private Server)**
Máy chủ ảo VPS, được chia thành nhiều server khác từ máy chủ vật lý. Và nó có tính năng như máy chủ vật lý ban đầu. Việc nâng cấp dễ dàng thông qua phần mềm quản lý hệ thống.

**Máy chủ đám mây (Cloud Server)**
Là máy chủ được xây dựng trên nền tảng điện toán đám mây nên dễ dàng nâng cấp từng phần mà không gián đoạn quá trình sử dụng. Và được kết hợp từ nhiều máy chủ vật lý khác nhau với cùng hệ thống lưu trữ SAN (Storage Area Network) với tốc độ truy xuất vượt trội giúp máy chủ hoạt động ổn định.

Dựa vào chức năng server, chia làm các loại máy chủ sau: 
* Máy chủ ứng dụng (Application Server): Thuật ngữ gọi chung cho các máy chủ chạy ứng dụng (application). 
* Máy chủ Audio / Video Server: Cung cấp đa phương tiện cho website phát cho người dùng phát nội dung đa phương tiện.
* Máy chủ web (Web Server): Là máy chủ mang website đến với người dùng và kết nối với nhau thông qua giao thức HTTP, nội dung được hiển thị chủ yếu dưới dạng HTML.
* Máy chủ FTP (FTP server): Cung cấp khả năng truyền file an toàn, bảo mật và kiểm soát đường truyền giữa các máy tính.
* Máy chủ DNS (DNS Server): Là máy chủ phân giải tên miền. Để thuận tiện cho việc sử dụng và dễ nhớ ta dùng tên (domain name) để xác định thiết bị đó. Hệ thống tên miền DNS (Domain Name System) được sử dụng để ánh xạ tên miền thành địa chỉ IP.
* Máy chủ DHCP (DHCP server): Là máy chủ có cài đặt DHCP có chức năng quản lý sự cấp phát địa chỉ IP động và các dữ liệu cấu hình TCP/IP.
* Máy chủ Database (Database Server): là máy chủ cài đặt phần mềm hệ quản trị cơ sở dữ liệu: MySQL, SQL server,…

## Địa chỉ IP
Địa chỉ IP là viết tắt của Internet Protocol – giao thức Internet. Đây là một địa chỉ đơn nhất mà những thiết bị điện tử hiện nay đang sử dụng để nhận diện và liên lạc với nhau trên mạng máy tính bằng cách sử dụng giao thức Internet. Về bản chất, địa chỉ IP là mã định danh cho phép gửi thông tin giữa các thiết bị trên mạng: IP chứa thông tin vị trí và giúp các thiết bị điện tử có thể truy cập được để liên lạc.

Internet cần một cách để phân biệt giữa các máy tính, bộ định tuyến (router) và trang web khác nhau. Địa chỉ IP cung cấp một cách thức hoạt động và tạo thành một phần thiết yếu của cách thức hoạt động của Internet. Địa chỉ IP là một chuỗi số được phân tách bằng dấu chấm. Địa chỉ IP được biểu thị dưới dạng một tập hợp bốn số – một địa chỉ ví dụ có thể là 192.158.1.38. Thông thường, mỗi số có trong tập hợp này sẽ ngẫu nhiên từ 0 – 255.  Vì vậy, phạm vi địa chỉ IP đầy đủ là từ 0.0.0.0 đến 255.255.255.255.

### Địa chỉ IP được dùng để
Địa chỉ IP cung cấp danh tính của các thiết bị được kết nối mạng có thể giúp nhận dạng thiết bị và phục vụ cho việc trao đổi thông tin. Giao thức Internet hoạt động giống như các ngôn ngữ khác, giao tiếp bằng cách sử dụng các nguyên tắc đã thiết lập để truyền thông tin.

Giao thức Internet được dùng để thiết bị này có thể tìm, gửi và trao đổi dữ liệu / thông tin với thiết bị khác. Bằng cách nói cùng một ngôn ngữ, bất kỳ máy tính nào ở bất kỳ vị trí nào cũng có thể kết nối với nhau.Ví dụ: Để gửi hàng cho một người, bạn cần phải biết địa chỉ chính xác để gửi hành. Cần phải ghi địa chỉ cụ thể bằng cách tra cứu trong danh sách địa chỉ mà bạn có. Đối với địa chỉ IP cũng vậy, thay vì tìm địa chỉ thì máy tính sử dụng các máy chủ DNS để tìm kiếm địa chỉ IP của máy đó.

### Cấu tạo của địa chỉ IP
Các bit đầu tiên trong địa chỉ IP được gọi theo thuật ngữ chuyên dùng là các bit mạng. Chúng xác định một mạng cụ thể. Các bit còn lại được gọi là các bit chủ và xác định một thiết bị (hoặc máy chủ) trong mạng đó. Giá trị đầu tiên của địa chỉ IP cho biết địa chỉ được chia thành các bit mạng và các bit máy chủ. Có ba lớp địa chỉ được xác định bởi giá trị ban đầu này:

* Lớp A:  8 bit mạng và 24 bit host
* Lớp B:  16 bit mạng và 16 bit host
* Lớp C:  24 bit mạng và 8 bit host

![ảnh](https://github.com/user-attachments/assets/533d8a3b-df72-412b-bc64-47d3c3a96659)

### IPv6
IPv6 (Internet Protocol version 6) là một phiên bản của giao thức Internet Protocol (IP), được thiết kế để thay thế và mở rộng IPv4 (Internet Protocol version 4), phiên bản IP trước đó. IPv6 được phát triển để giải quyết vấn đề cạn kiệt địa chỉ IP duy nhất của IPv4 do sự mở rộng nhanh chóng của Internet và sự gia tăng số lượng thiết bị kết nối.

Một số đặc điểm chính của IPv6 bao gồm:
* Kích thước địa chỉ:IPv6 sử dụng địa chỉ IP dạng 128 bit, so với IPv4 chỉ có 32 bit. Điều này tăng khả năng cung cấp số lượng địa chỉ IP hỗ trợ cho sự mở rộng toàn cầu của Internet.
* Khả năng mở rộng: Với kích thước địa chỉ lớn hơn, IPv6 cung cấp một không gian địa chỉ IP đủ lớn để chứa số lượng lớn hơn các địa chỉ IP.
* Hỗ trợ an ninh: IPv6 tích hợp nhiều tính năng bảo mật hơn so với IPv4, bao gồm cơ chế xác thực và mã hóa dữ liệu.
* Tích hợp quản lý dịch vụ: IPv6 hỗ trợ tích hợp các dịch vụ quản lý mạng, giúp quản trị server dễ dàng hơn.

IPv6 là một phần quan trọng của nỗ lực chuyển đổi để đảm bảo Internet có đủ địa chỉ IP và đáp ứng được với sự mở rộng ngày càng tăng. Tuy IPv4 vẫn còn phổ biến, nhưng việc triển khai IPv6 đang được khuyến khích để đảm bảo sự liên thông và bền vững của Internet trong tương lai.

### IPv4 
Pv4 (Internet Protocol version 4) là một phiên bản của giao thức Internet Protocol (IP), được thiết kế để xác định và gửi dữ liệu giữa các thiết bị trên Internet. IPv4 là phiên bản chính thức đầu tiên của IP và là nền tảng cơ bản cho việc kết nối mạng trên toàn cầu.

Dưới đây là một số đặc điểm chính của IPv4:
* Kích thước địa chỉ: IPv4 sử dụng địa chỉ IP dạng 32 bit, tạo ra khoảng 4,3 tỷ (2^32) địa chỉ duy nhất. Địa chỉ IP thường được biểu diễn dưới dạng bốn nhóm số thập phân, ví dụ: 192.168.0.1.
* Sự cạn kiệt địa chỉ: Vì số lượng địa chỉ IPv4 có hạn, và Internet ngày càng mở rộng nhanh chóng, cạn kiệt địa chỉ IPv4 trở thành vấn đề lớn. Điều này đã thúc đẩy sự phát triển và triển khai của IPv6.
* Không gian địa chỉ: IPv4 định nghĩa ba loại địa chỉ IP chính: địa chỉ dành cho mạng (network address), địa chỉ dành cho thiết bị (host address), và địa chỉ dành cho địa chỉ đặc biệt (broadcast address).
* Phương thức truyền tải dữ liệu: IPv4 sử dụng giao thức truyền tải dữ liệu có tên là Transmission Control Protocol (TCP) hoặc User Datagram Protocol (UDP) để chuyển giao thông mạng.

### Các loại địa chỉ IP
#### IP Public – Địa chỉ IP công cộng

Địa chỉ IP công cộng (IP Public) là loại địa chỉ mà nhà cung cấp Internet dùng để truyền tải những yêu cầu về hệ thống mạng đến một tổ chức hoặc hộ gia đình cụ thể. Có thể nói, đây cũng là địa chỉ mà hệ thống mạng tổ chức, gia đình dùng để kết nối/liên lạc với nhiều thiết bị đã cài đặt Internet khác. Điều này cho phép người dùng kiểm soát được các thiết bị có trong danh mục được phép truy cập hệ thống mạng này.

#### IP Private – Địa chỉ IP cá nhân

Địa chỉ IP cá nhân (hay còn gọi là IP Private) là địa chỉ riêng sử dụng trong nội bộ mạng LAN như mạng gia đình, nhà trường, công ty. Địa chỉ IP Private khác với IP Public ở chỗ chỉ có các thiết bị trong cùng một mạng mới có thể thực hiện chức năng giao tiếp với nhau bằng bộ định tuyến router, ngoài ra các thiết bị khác không thể thực hiện kết nối mạng Internet với cùng địa chỉ IP này. Người dùng có thể tự thiết lập địa chỉ IP cá nhân bằng phương pháp thủ công, hoặc cho phép bộ định tuyến cài đặt tự động.

#### IP Static – Địa chỉ IP tĩnh

Địa chỉ IP tĩnh (IP Static) được hiểu là một loại IP được thiết kế riêng biệt và cố định cho một hoặc một nhóm người sử dụng, với điều kiện mọi thiết bị kết nối đến Internet của họ đều được đặt cùng một địa chỉ IP. Thông thường IP tĩnh được cấp cho một máy chủ với một mục đích riêng như web server, email,… để nhiều người có thể truy cập mà không làm gián đoạn các quá trình đó.

#### IP Dynamic – Địa chỉ IP động

Trong trường hợp doanh nghiệp không muốn dùng IP tĩnh cho khách hàng, họ chỉ được hệ thống ISP gán cho mỗi lần kết nối là một địa chỉ IP khác nhau. Sau đó, khi một phiên kết nối hoàn tất, địa chỉ IP này sẽ tự động thay đổi. Hiện nay, nguồn địa chỉ IP đang trở nên cạn kiệt, và phương pháp hữu dụng để khắc chế tình trạng này là việc ISP cung cấp IP động. Điều này được hiểu rằng, khi một thiết bị không được truy cập vào mạng Internet, thì nhà cung cấp sẽ tận dụng IP này để cấp cho một người dùng khác.

### Ứng dụng của địa chỉ IP 
Hacker trên mạng có thể sử dụng nhiều kỹ thuật khác nhau để lấy địa chỉ IP của bạn. Hai trong số những cách phổ biến nhất là dùng social engineering và online stalking.
* Online stalking
* Tải xuống nội dung bất hợp pháp bằng địa chỉ IP của bạn
* Theo dõi vị trí
* Trực tiếp tấn công mạng
* Tấn công vào thiết bị

### Hướng dẫn cách ẩn địa chỉ IP
Ẩn địa chỉ IP là một cách để bảo vệ thông tin cá nhân và danh tính trực tuyến của bạn. Hai cách chính để ẩn địa chỉ IP của bạn là:

* Sử dụng proxy server
* Sử dụng mạng riêng ảo (VPN)

## Domain
Domain (hay tên miền) là địa chỉ độc nhất của một website trên Internet, hoạt động giống như một “ngôi nhà ảo” chứa đựng toàn bộ nội dung và thông tin của trang web. Thay vì phải ghi nhớ dãy số phức tạp của địa chỉ IP, người dùng có thể dễ dàng truy cập website bằng cách nhập tên miền vào trình duyệt.

Tên miền được cấu thành từ các ký tự và chữ số trong bảng chữ cái, kết hợp với TLD (Top-Level Domain) như .com, .net, .org, .vn,… Bên cạnh domain chính (main domain), bạn có thể tạo thêm subdomain để tổ chức website một cách hiệu quả.

### Thành phần của Domain

https://    host247.      vietnix                .vn                  /webmail
protocol    sub-domain    second level domain    top level domain     page-path

#### Protocol 
là một tập hợp các quy tắc chuẩn cho phép hai hoặc các thực thể trong cùng một hệ thống để trao đổi thông tin liên lạc dữ liệu qua các kênh truyền thông.

Các Protocol phổ biến: http, https, ftp,...

#### Sub-domain
cho phép bạn tổ chức và quản lý các phần khác nhau của trang web hoặc ứng dụng web dưới cùng một tên miền chính.

Nếu bạn có tên miền chính là vietnix.vn bạn có thể tạo các sub-domain như blod.vietnix.vn, hoặc support.vietnix.vn.

Mỗi sub-domain có thể trỏ đến một trang web hoặc phần cụ thể của trang.

#### Second level domain (SLD)
là phần tiếp theo của tên miền và thường là phần mà người dùng tuỳ chỉnh để xác định trang web hoặc dịch vụ của họ.

Ví dụ:

- google trong google.com
- vietnix trong vietnix.com

#### Top level domain (TLD) 
là phần cuối cùng của tên miền và thường được quốc gia hoặc quản lý toàn cầu.

Ví dụ:

- .com cho tên miền thương mại.
- .org cho tên miền tổ chức phi lợi nhuận.
- .net cho tên miền mạng lưới.
- .vn cho tên miền quốc gia của Việt Nam.

#### Pgae-Path 
là đường dẫn trang cho viết cách di chuyển trong cấu trúc trang web. Mỗi phần của đường dẫn trang thường thể hiện một thư mục hoặc một trang cụ thể trên trang web.

Ví dụ:

/webmail có thể đại diện cho một thư mục hoặc chủ đề cụ thể trên trang web


Đây là ví dụ minh họa cho sự khác nhau giữa địa chỉ URL (Uniform Resource Locator) và một tên miền:

URL: https://vietnix.vn/domain-la-gi/
Tên miền: vietnix.vn

### Cách hoạt động của tên miền, domain 
Để website của bạn hiện thị trên Internet, trình duyệt cần biết cách tìm đến đúng máy chủ lưu trữ (Hosting). Quá trình này được thực hiện thông qua hệ thống phân giải tên miền (DNS).

Bạn nhập tên miền (domain name) vào trình duyệt, thiết bị của bạn sẽ gửi một yêu cầu (request) đến DNS Resolver- thường được cung cấp bởi nhà cung cấp dịch vụ Internet (ISP),DNS Resolever sẽ tra cứu thông tin trong DNS Zone tương ứng với tên miền bạn nhập.

DNS Zone chứa các bản ghi (DNS Record), bao gồm địa chỉ IP của máy chủ định danh cho tên miền đó. Nameserver này, thường được quản lý bởi nhà cung cấp dịch vụ hosting, sẽ trả về địa chỉ IP của máy chủ web chứa website của bạn.

Máy chủ web (Web Server), được cài đặt phần mềm máy chủ web phổ biến như Apache hay Nginx, sẽ xử lý yêu cầu từ trình duyệt, tìm nạp nội dung website và gửi dữ liệu trở lại cho trình duyệt.

Hiểu rõ cách thức hoạt động của tên miền giúp bạn tối ưu hóa hiệu suất và bảo mật cho website. Tốc độ phân giải DNS ảnh hưởng trực tiếp đến thời gian tải trang, góp phần mang lại trải nghiệm người dùng tốt hơn. Bên cạnh đó, bạn có thể cấu hình DNS để nâng cao bảo mật cho website, chống lại các cuộc tấn công mạng.

### Vai trò của domain 
Domain đóng vai trò then chốt trong sự thành công của bất kỳ doanh nghiệp nào hoạt động trực tuyến. Nó không chỉ là địa chỉ duy nhất của trang web trên Internet mà còn là nền tảng để xây dựng thương hiệu, thu hút khách hàng và gia tăng doanh thu.

* Xây dựng thương hiệu: Tên miền (domain name) là đại diện cho thương hiệu của bạn trên môi trường Internet. Một tên miền dễ nhớ, phù hợp với lĩnh vực hoạt động giúp khách hàng dễ dàng nhận diện và ghi nhớ thương hiệu, từ đó tăng cường uy tín và niềm tin đối với doanh nghiệp. Ví dụ, tên miền “tiki.vn” ngắn gọn, dễ nhớ và thể hiện rõ lĩnh vực hoạt động của Tiki là thương mại điện tử.
* Tối ưu hóa SEO: Domain có tác động trực tiếp đến thứ hạng tìm kiếm trên Google. Tên miền chứa từ khóa liên quan đến nội dung website giúp Google hiểu rõ lĩnh vực hoạt động của bạn, từ đó nâng cao thứ hạng trong kết quả tìm kiếm. Bên cạnh tên miền, URL cũng cần được tối ưu hóa để thu hút thêm traffic từ các công cụ tìm kiếm.
* Tăng cường lòng tin và uy tín: Sở hữu một tên miền riêng, đặc biệt là với TLD uy tín (.com, .net, .vn), thể hiện sự chuyên nghiệp và đáng tin cậy của doanh nghiệp. Điều này tạo lòng tin cho khách hàng tiềm năng, thúc đẩy họ tương tác với website và sử dụng dịch vụ.
* Khả năng mở rộng: Khi doanh nghiệp phát triển, bạn có thể dễ dàng mở rộng website bằng cách tạo subdomain cho các mảng kinh doanh khác nhau. Điều này giúp bạn tổ chức nội dung hiệu quả, đồng thời nâng cao trải nghiệm người dùng.
* Bảo vệ thương hiệu: Đăng ký tên miền giúp bảo vệ thương hiệu của bạn khỏi những đối tượng xấu muốn sử dụng tên miền tương tự với mục đích lừa đảo hoặc gây tổn hại đến uy tín doanh nghiệp.
* Dễ dàng quản lý: Sở hữu tên miền riêng cho phép bạn toàn quyền kiểm soát nội dung và thiết kế website, tự do lựa chọn nhà cung cấp hosting phù hợp với nhu cầu.

## WHOIS
Whois là công cụ tra cứu thông tin đăng ký tên miền, hé mở cánh cửa bí ẩn về chủ sở hữu, ngày đăng ký, ngày hết hạn, máy chủ lưu trữ và nhiều thông tin quan trọng khác.
- Minh bạch: Tiết lộ thông tin chủ sở hữu, giúp bạn đưa ra quyết định sáng suốt khi giao dịch tên miền.
- Bảo mật: Nâng cao khả năng bảo vệ website khỏi các hành vi lừa đảo, giả mạo.
- Hỗ trợ: Cung cấp thông tin liên hệ chính xác của nhà cung cấp dịch vụ, giúp bạn dễ dàng tiếp cận hỗ trợ khi cần thiết.
- Hiệu suất: Giúp bạn đánh giá hiệu quả hoạt động của website thông qua thông tin máy chủ lưu trữ.

Lợi ích của khi kiểm tra whois tên miền
- Kiểm tra tình trạng tên miền
- Tìm kiếm chủ sở hữu tên miền
- Kiểm tra ngày hết hạn tên miền
- Xem vòng đời tên miền

## DNS
DNS viết tắt của Domain Name System có nghĩa là hệ thống phân giải tên miền. DNS là hệ thống cho phép thiết lập tương ứng giữa địa chỉ IP và tên miền trên Internet.
    
DNS được phát minh vào năm 1984 cho Internet và đây là một trong số các chuẩn công nghiệp của các cổng bao gồm cả TCP/IP. Hệ thống phân giải tên miền chính là chìa khóa chủ chốt của nhiều dịch vụ mạng hiện nay như Internet, Mail server, Web server…

### Chức năng của DNS
DNS đóng vai trò như một “biên dịch viên” giữa tên miền và địa chỉ IP. Tên miền là chuỗi ký tự dễ nhớ, trong khi địa chỉ IP là chuỗi số khó nhớ. DNS giúp chuyển đổi tên miền thành địa chỉ IP, từ đó giúp máy tính có thể truy cập vào các trang web trên internet.

Mỗi máy tính khi kết nối vào Internet sẽ được gán cho 1 địa chỉ IP (Ví dụ: 1414.1158.62462) riêng biệt và không trùng lẫn với bất kỳ máy tính nào khác trên thế giới. Cũng giống như vậy đối với website cũng có địa chỉ IP riêng biệt của website đó.

### Cách thức hoạt động của DNS

- Khi người dùng truy cập một website, máy tính sẽ gửi yêu cầu đến máy chủ DNS cục bộ để tìm địa chỉ IP của website đó. Máy chủ DNS cục bộ sẽ kiểm tra cơ sở dữ liệu của mình xem có chứa địa chỉ IP của website hay không. Nếu có, sẽ trả về địa chỉ IP cho máy tính của người dùng.
- Quá trình phân giải DNS bao gồm chuyển đổi tên máy chủ (chẳng hạn như www.example.com) thành địa chỉ IP thân thiện với máy tính (chẳng hạn như 192.168.1.1). Một địa chỉ IP được cung cấp cho mỗi thiết bị trên Internet và địa chỉ đó là cần thiết để tìm thiết bị Internet phù hợp. Giống như một địa chỉ đường phố được sử dụng để tìm một ngôi nhà cụ thể.
- Khi người dùng muốn tải một trang web, một bản dịch phải xảy ra giữa những gì người dùng nhập vào trình duyệt web của họ (example.com) và địa chỉ thân thiện với máy cần thiết để định vị trang web example.com.
- Nếu máy chủ DNS cục bộ không có địa chỉ IP của website, nó sẽ hỏi máy chủ DNS gốc. Máy chủ DNS gốc sẽ trả về địa chỉ IP của máy chủ DNS cấp cao nhất cho website.
- Máy chủ DNS cấp cao nhất sẽ trả về địa chỉ IP của máy chủ DNS quản lý website. Máy chủ DNS quản lý sẽ trả về địa chỉ IP của trang web cho máy chủ DNS cục bộ.
- Cuối cùng, máy chủ DNS cục bộ sẽ trả về địa chỉ IP của trang web cho máy tính của người dùng. Máy tính của người dùng sẽ sử dụng địa chỉ IP này để kết nối với website.

### Các loại DNS bản ghi DNS thường sử dụng

Hiện nay, DNS có bảy loại bản ghi, bao gồm:

- CNAME Record: Là một bản ghi tên quy chuẩn (Canonical Name Record). Đây là một dạng bản ghi tài nguyên trong hệ thống tên miền.
- A Record: Dùng để trỏ tên miền website tới một địa chỉ IP cụ thể. Đây được xem là bản ghi DNS đơn giản nhất.
- MX Record: Bản ghi này bạn có thể sử dụng để trỏ tên miền đến mail server. MX Record chỉ định server nào quản lý các dịch vụ Email của tên miền đó.
- AAAA Record: Dùng để trỏ tên miền đến địa chỉ IPv6 và cho phép thêm host mới, TTL và IPv6.
- TXT Record: Ngoài ra, có thể thêm giá trị TXT, Host mới, TTL và Point To để chứa các thông tin định dạng văn bản domain.
- SRV Record: Đây là bản ghi DNS đặc biệt, dùng để xác định chính xác dịch vụ nào đang chạy Port nào. Và thông qua bản ghi này bạn có thể thêm Priority, Port, Weight, TTL, Point to Point.
- NS Record: Bản ghi này có thể chỉ định Name Server cho từng tên miền phụ và bên cạnh đó có thể tạo tên Name Server, TTL hay host mới.

### Các loại DNS Server

Root Name Server là một dịch vụ phân giải tên miền gốc và trên thế giới có khoảng 12 DNS root Server.

DNS root Server quản lý tất cả các tên miền Top-level. Khi có yêu cầu phân giải một Domain Name thành một địa chỉ IP, client sẽ gửi yêu cầu đến DNS gần nhất (DNS ISP). DNS ISP sẽ kết nối tới DNS root Server để hỏi địa chỉ của Domain Name.

DNS root Server sẽ căn cứ và dựa vào các Top Level của tên miền và từ đó có những tài liệu hướng dẫn phù hợp để chuyển hướng cho khách hàng đến đúng địa chỉ cần truy vấn.

Local Name Server

DNS Server này dùng để chứa thông tin để truy xuất và tìm kiếm máy chủ tên miền. Và thường được duy trì và phát triển bởi các doanh nghiệp hay các nhà cung cấp dịch vụ Internet.

DNS Recursor

DNS Recursor là một máy chủ có nhiệm vụ chuyển đổi tên miền thành địa chỉ IP. Được hoạt động như một thư viện, lưu trữ thông tin về địa chỉ IP của các trang web và ứng dụng. Khi người dùng nhập một tên miền, DNS Recursor sẽ tìm kiếm thông tin đó trong cơ sở dữ liệu của mình. Nếu không tìm thấy, nó sẽ liên hệ với các DNS Recursor khác để tìm kiếm. DNS Recursor cũng sử dụng bộ nhớ đệm để lưu trữ thông tin về các tên miền mà nó đã từng truy cập. Điều này giúp tăng tốc độ phản hồi cho các truy vấn trong tương lai.

TLD Name Server
TLD Name Server là máy chủ tên miền cấp cao nhất, chịu trách nhiệm lưu trữ thông tin về các tên miền có phần mở rộng chung (gTLD), chẳng hạn như .com, .org, .net. Trong quá trình tìm kiếm địa chỉ IP, máy chủ định danh sẽ liên hệ với TLD Name Server để lấy thông tin về tên miền.

Authoritative Name Server
Authoritative Name Server lưu trữ thông tin về tên miền và địa chỉ IP tương ứng. Là điểm cuối của quá trình truy vấn và phân giải địa chỉ IP cần thiết cho DNS Recursor.

### Nguyên tác vận hành của DNS

Về vận hành của DNS là gì sẽ có cơ chế hoạt động tương tự với hệ thống khách, nó cũng sẽ có những nguyên tắc hoạt động nhất định và muốn sử dụng được bạn bắt buộc phải hiểu được nguyên lý hoạt động.

Nội dung bên dưới sẽ đề cập khái quát về nguyên tắc làm việc DNS Server cụ thể như sau: 

- Mỗi nhà cung cấp dịch vụ sẽ có hệ thống DNS riêng để phân giải tên miền của mình trên Internet và đảm bảo cho người dùng có thể truy cập vào các trang web của doanh nghiệp nhanh chóng nhất.
- Khi người dùng truy cập vào một trang web, DNS server sẽ phân giải tên miền của website đó tại chính tổ chức quản lý website, không phải ở các tổ chức hay nhà cung cấp dịch vụ khác.

- INTERNIC là tổ chức được thành lập với mục đích đăng ký tên miền của internet và theo dõi các DNS server tương ứng. Tuy nhiên, INTERNIC không thực hiện phân giải tên miền mà chỉ quản lý tất cả các DNS trên server. DNS có khả năng truy vấn các DNS Server khác để có được tên miền đã được phân giải, và nó có hai chức năng chính là phân giải tên miền và trả lời các yêu cầu của các DNS server khác.

- Mỗi DNS server sẽ quản lý và chịu trách nhiệm phân giải tên miền từ các máy bên trong tên miền đến các địa chỉ internet mà nó quản lý. Ngoài ra, nó còn có trách nhiệm trả lời các yêu cầu từ các DNS server khác bên ngoài đang cố gắng phân giải tên miền mà nó quản lý. Tất cả các nhà cung cấp dịch vụ đều có hệ thống DNS riêng để đảm bảo an toàn và hiệu quả cho người dùng, và INTERNIC là tổ chức quản lý các tên miền và DNS server trên toàn thế giới.

### Cách phần giải địa chỉ DNS

Để hiểu được cơ chế hoạt động của DNS là gì bạn cần hiểu quy trình của một máy tính cá nhân khi muốn truy cập vào địa chỉ Vietnix.vn, cụ thể theo từng bước như sau: 

Bước 1: Khi bạn sẽ truy cập vào website của Vietnix.vn bằng máy tính cá nhân, lúc này máy client sẽ gửi đến yêu cầu tìm địa chỉ IP của tên miền  Vietnix.vn đến máy chủ tên miền cục bộ. 

Bước 2: Tiếp tục, máy chủ miền cục bộ sẽ thực hiện rà soát các cơ sở dữ liệu để xem có những thông tin vào khác có tương ứng IP  tên miền “Vietnix.vn” nữa không? Nếu không thì sẽ nhanh chóng trả IP của Vietnix.vn cho máy Client. 

Trường hợp, nếu sau khi rà soát và không phát hiện cơ sở dữ liệu có liên quan đến miền Vietnix.vn máy chủ miền cục bộ sẽ tiếp tục gửi yêu cầu đến ROOT Name Server. 

Bước 3: Tuy nhiên, Root Name Server không chứa thông tin về địa chỉ IP của Vietnix.vn, mà chỉ chứa thông tin về máy chủ quản lý tên miền của Việt Nam (.vn).

Khi đó Root Name Server sẽ gửi thông tin về địa chỉ máy chủ quản lý tên miền .vn cho máy chủ tên miền cục bộ.

Bước 4: Lúc này, máy chủ tên miền cục bộ sau đó sẽ gửi yêu cầu tìm kiếm đến máy chủ quản lý tên miền .vn để tìm địa chỉ IP của Vietnix.vn.

Máy chủ quản lý tên miền .vn có cơ sở dữ liệu chứa thông tin về tất cả các tên miền .vn, bao gồm cả Vietnix.vn. Vì vậy, máy chủ quản lý tên miền .vn sẽ trả lại địa chỉ IP của Vietnix.vn cho máy chủ tên miền cục bộ.

Bước 5: Bởi vì máy chủ quản lý tên miền VN có chứa cơ sở dữ liệu của tất cả các website có đuôi .vn (Tức là miền .vn) nên sẽ trả lại địa chỉ IP tên miền Vietnix cho máy chủ tên miền cục bộ. 

Bước 6: Cuối cùng máy chủ tên miền cục bộ sẽ gửi thông tin về tên miền Vietnix đến máy Client, sau đó client sẽ tiếp tục sử dụng ip vừa được cấp để truy cập tới máy  Server Vietnix.vn. 

## DKIM
DKIM là viết tắt của DomainKeys Indentified Mail - một phương thức giúp xác nhận Email thông qua chữ ký số giúp tránh email giả mạo. Một kỹ thuật thươngf được sử dụng trong lừa đảo và spapm email.

DKIM cho phép người nhận kiểm tra xem email được xác nhận từ một tên miền cụ thể có thực sự được chủ sở hữu uy quyền hay không? Nó sẽ gắn chữ ký điện tử, được liên kết với tên miền vào mỗi email gửi đi. Hệ thống người nhận có thể xác minh điều này bằng cách tra cứu mã khóa công khai (Public-key cryptography) của người gửi được xuất bản trong DNS.

Bên cạnh đó, DKIM còn cso khả năng chặn các email giả mạo, đây là chức năng được sử dụng nhiều hiện nay. Đối với các thư với mục đích giả mạo, lừa đảo, email spam chứa các mã độc….

- Khóa công khai thường được công bố trên DNS với dưới dạng TXT record.
- Khi gửi email, chữ ký sẽ được chèn lên đầu với trường DKIM-Signature.

## SPF 
SPF (Sender Policy Framework) là một cơ chế xác thực email được thiết kế để chống lại giả mạo địa chỉ email (email spoofing). SPF cho phép chủ sở hữu tên miền xác định các máy chủ email được phép gửi email cho tên miền của họ. Điều này giúp giảm thiểu khả năng email giả mạo và cải thiện bảo mật email.

### Nguyên Tắc Hoạt Động của SPF

1. Bản Ghi SPF:
- SPF sử dụng một bản ghi TXT trong hệ thống DNS của tên miền để chỉ định các máy chủ hoặc địa chỉ IP hợp lệ có quyền gửi email cho tên miền đó. Ví dụ, bản ghi SPF có thể cho phép các máy chủ từ địa chỉ IP cụ thể hoặc các máy chủ DNS khác gửi email thay mặt cho tên miền.

2. Kiểm Tra SPF:
- Khi một máy chủ email nhận một email, nó sẽ kiểm tra bản ghi SPF của tên miền người gửi (domain sender) để xác định liệu địa chỉ IP của máy chủ gửi email có được phép gửi email cho tên miền đó hay không.

3. Kết Quả SPF:
- Pass: Địa chỉ IP của máy chủ gửi email nằm trong danh sách được phép, và email được gửi từ một nguồn hợp lệ.
- Fail: Địa chỉ IP của máy chủ gửi email không nằm trong danh sách được phép, và email có thể bị xem là giả mạo.
- Softfail: Địa chỉ IP không nằm trong danh sách, nhưng không hoàn toàn từ chối email. Email có thể được đánh dấu là nghi ngờ.
- Neutral: Không có thông tin đầy đủ để xác định tính hợp lệ của địa chỉ IP.
- None: Không có bản ghi SPF được cấu hình cho tên miền.

### Cấu Trúc Bản Ghi SPF

Bản ghi SPF là một bản ghi TXT trong DNS và có cấu trúc cơ bản như sau:

v=spf1 [mechanisms] [modifiers]

- v=spf1: Phiên bản của SPF.
- Mechanisms: Các điều kiện để xác định địa chỉ IP hợp lệ. Ví dụ:

    - ip4:<IP_ADDRESS>: Cho phép một địa chỉ IP cụ thể.
    - ip6:<IP_ADDRESS>: Cho phép một địa chỉ IP IPv6 cụ thể.
    - a: Cho phép bất kỳ địa chỉ IP nào liên kết với tên miền của bản ghi A.
    - mx: Cho phép bất kỳ địa chỉ IP nào liên kết với bản ghi MX của tên miền.
    - include:<DOMAIN>: Bao gồm các quy tắc SPF từ tên miền khác.
    - all: Xác định cách xử lý tất cả các địa chỉ IP không được liệt kê rõ ràng.

SPF giúp bảo vệ chống lại email giả mạo bằng cách cho phép chủ sở hữu tên miền xác định các máy chủ email hợp lệ. Khi kết hợp với các cơ chế xác thực email khác như DKIM (DomainKeys Identified Mail) và DMARC (Domain-based Message Authentication, Reporting, and Conformance), SPF tạo ra một lớp bảo mật mạnh mẽ cho hệ thống email.

## PTR
PTR (Pointer Record) là một loại bản ghi DNS được sử dụng chủ yếu trong các hệ thống DNS ngược (reverse DNS lookup). PTR record giúp ánh xạ địa chỉ IP trở lại tên miền của nó, điều này thường được sử dụng để xác minh tính hợp lệ của địa chỉ IP trong các quy trình như kiểm tra email và bảo mật mạng.

### Nguyên Tắc Hoạt Động của PTR Record

1. Chuyển Đổi Địa Chỉ IP Thành Tên Miền:
- PTR record cho phép bạn thực hiện chuyển đổi ngược từ địa chỉ IP về tên miền. Điều này ngược lại với bản ghi A (hoặc AAAA) thường dùng để ánh xạ tên miền đến địa chỉ IP.
2. DNS Ngược (Reverse DNS Lookup):
- Trong DNS ngược, thay vì tra cứu địa chỉ IP từ tên miền, bạn tra cứu tên miền từ địa chỉ IP. Điều này thường được sử dụng để kiểm tra tính hợp lệ của các địa chỉ IP khi máy chủ email gửi thư đến hoặc trong các quá trình bảo mật mạng.

### Cấu Trúc Bản Ghi PTR

Bản ghi PTR trong DNS có cấu trúc cơ bản như sau:

<reversed IP>.in-addr.arpa. IN PTR <hostname>.

- <reversed IP>: Địa chỉ IP được đảo ngược. Ví dụ, địa chỉ IP 192.168.1.1 sẽ được viết ngược thành 1.1.168.192.
- in-addr.arpa: Tên miền cơ sở cho tra cứu DNS ngược.
- PTR: Loại bản ghi.
- <hostname>: Tên miền mà địa chỉ IP ánh xạ tới.

### Vai Trò và Tầm Quan Trọng

1. Xác Thực Email:
- PTR records giúp xác minh rằng địa chỉ IP gửi email thực sự thuộc về tên miền mà nó tuyên bố. Điều này giúp chống lại các cuộc tấn công giả mạo và spam.

2. Bảo Mật Mạng:
- PTR records có thể được sử dụng trong các hệ thống bảo mật để đảm bảo rằng các địa chỉ IP và tên miền tương ứng là hợp lệ và đáng tin cậy.

PTR records đóng vai trò quan trọng trong việc xác minh tính hợp lệ của địa chỉ IP và tên miền trong các hệ thống DNS ngược. Chúng thường được sử dụng trong các quy trình bảo mật mạng và kiểm tra email để đảm bảo tính chính xác và độ tin cậy của các kết nối mạng.
        
## Datacenteratacenter
Datacenter (hay còn gọi là trung tâm dữ liệu) là nơi chứa hệ thống máy tính hoặc máy chủ và các tài nguyên công nghệ với mật độ cao, chẳng hạn như hệ thống lưu trữ (storage systems) và truyền thông mạng (network communications).

Datacenter thường bao gồm nguồn cung cấp điện dự phòng, kết nối truyền thông dữ liệu dự phòng, kiểm soát môi trường, chẳng hạn như điều hòa không khí, ngăn chặn hỏa hoạn và các thiết bị an ninh khác nhau. Các cụm server nối mạng được sử dụng để xử lý, lưu trữ và phân phối lượng lớn dữ liệu. Đối với hầu hết mọi loại giao dịch kinh doanh, trao đổi dữ liệu điện tử là bắt buộc. Khi nhu cầu về dữ liệu tăng lên, datacenter ra đời để có thể xử lý các yêu cầu đó.

### Colocation Datacenter
Colocation là dịch vụ cung cấp không gian để đặt máy chủ. Khi sử dụng colocation bạn sẽ không cần lo các vấn đề về thiết bị vật lý, bởi colocation đã có nhà cung cấp quản lý. Chi phí quản lý và duy trì trung tâm dữ liệu nội bộ ngày càng tăng, kết hợp với sự gia tăng của công nghệ đám mây, đang biến các colocation operators thành một lựa chọn hấp dẫn cho nhiều tổ chức.
 
Các nhà khai thác vị trí (colocation operator) cung cấp cho các tổ chức cơ sở trung tâm dữ liệu để chứa và vận hành máy chủ của họ. Colos thường cung cấp các vị trí vật lý cũng như các dịch vụ cấp nguồn, làm mát, mạng và bảo mật cho máy chủ của khách hàng.

### Ưu điểm của Datacenter
Nói đến ưu điểm của trung tâm dữ liệu, không thể bỏ qua tính bảo mật thông tin của chúng. Khi doanh nghiệp sử dụng dịch vụ cung cấp chỗ đặt máy chủ, họ sẽ có không gian lưu trữ dữ liệu chuyên nghiệp và an toàn.

Việc dùng đường truyền như xDSL hoặc PSTN/ISD là có thể sử dụng. Điều quan trọng là quy trình cài đặt không phức tạp và rất tiết kiệm thời gian. Với Datacenter, doanh nghiệp có thể giảm chi phí lưu trữ và quản lý dữ liệu một cách đáng kể. Đồng thời, hoạt động kinh doanh của công ty vẫn diễn ra một cách hiệu quả và thuận lợi.

### Cách hoạt động của trung tâm dữ liệu
Datacenter thường được coi là bộ não của công ty. Đây là nơi tất cả các quy trình quan trọng của một doanh nghiệp được chạy trên các máy chủ. Những dữ liệu quan trọng được xử lý, lưu trữ và tổ chức thành các packet để truyền. Đây là nơi các bộ định tuyến (router) xác định con đường tốt nhất để dữ liệu di chuyển. Bản thân datacenter được xây dựng với nhiều thiết bị được tích hợp khả năng phục hồi.

### Các thành phần của Datacenter

Một số thành phần bên trong các trung tâm dữ liệu như sau:

- Cơ sở vật chất: Thành phần đầu tiên cần được đề cập khi nói về các Datacenter là không gian để đặt server. Tiêu chí quan trọng của không gian trong trung tâm dữ liệu là phải đảm bảo sạch sẽ và an toàn.
- Thiết bị duy trì và vận hành bộ phận trong trung tâm dữ liệu: Nguồn điện cần được cung cấp liên tục, đi kèm với máy điều hòa, hệ thống thông gió, phòng cháy chữa cháy, hệ thống làm ấm và ống xả,…
- Công cụ và thiết bị IT hỗ trợ cho hoạt động lưu trữ dữ liệu và các công việc liên quan đến công nghệ thông tin khác cho doanh nghiệp.
- Nhân viên điều hành, quản lý và giám sát mọi hoạt động của thiết bị và cơ sở hạ tầng trong trung tâm dữ liệu. Các Datacenter cần có nhân viên quan sát để đảm bảo rằng mọi thứ được vận hành đúng và liên tục.

### Vai trò của Datacenter
Datacenter có vai trò tạo ra môi trường cho người dùng thuê không gian và các dịch vụ hỗ trợ khác mà không cần cài đặt phức tạp. Người dùng chỉ cần kết nối đến trung tâm cung cấp dữ liệu thông qua PSTN/ISD, xDSL,… Có thể thấy datacenter liên quan chặt chẽ đến tính bảo mật của hệ thống network. Vì vậy vấn đề bảo mật, an toàn và độ tin cậy của datacenter là một trong những ưu tiên hàng đầu của các đơn vị cung cấp.

Nhu cầu về không gian lưu trữ, khả năng xử lý thông tin đang tăng lên theo cấp số nhân và các công ty cần phải có khả năng theo kịp để có thể cung cấp, đáp ứng nhu cầu của khách hàng. Trong nhiều trường hợp, các mô hình kinh doanh công ty hiện đại được xây dựng dựa trên trung tâm dữ liệu làm nền tảng hoặc “manufacturing plant” cho các dịch vụ mà công ty cung cấp.

Chẳng hạn, các công ty như Facebook, Apple, eBay, Amazon và LinkedIn đều phụ thuộc vào các trung tâm dữ liệu để cung cấp các dịch vụ và sản phẩm cốt lõi cho khách hàng của họ. Nếu không có trung tâm dữ liệu, các doanh nghiệp không thể tồn tại hoặc tự đặt mình vào nguy cơ mất doanh thu và tác động tiêu cực đến sự hài lòng của khách hàng.

### Phân loại Datacenter
- Data Center doanh nghiệp (tại chỗ)
- Data Center đám mây công cộng
- Data Center nơi cho thuê chỗ đặt máy chủ

## CPU
CPU được viết tắt từ Central Processing Unit – bộ xử lý trung tâm đóng vai trò cốt lõi giúp hệ thống máy tính thực thi các câu lệnh qua việc thực hiện và phân tích phép toán, so sánh, logic. Bên cạnh đó, CPU còn có tác dụng xử lý các yêu cầu nhập hoặc xuất dữ liệu cơ bản của người dùng.

CPU còn được biết đến với những tên gọi khác như: Processor, Microprocessor, Central processor. Nhìn chung, CPU dùng để điều khiển tất cả hoạt động và được xem như đầu não của toàn hệ thống máy tính hoặc laptop. CPU sẽ xử lý các dữ kiện từ phần mềm hệ thống, phần mềm ứng dụng cho đến phần cứng đang hoạt động bình thường trên máy tính.

### Chức năng của CPU

CPU chủ yếu đảm nhận nhiệm vụ xử lý tất cả các chương trình trên máy tính. CPU không chỉ xử lý dữ liệu đầu vào mà còn thực hiện mọi lệnh được gửi đến thông qua phần mềm hoặc phần cứng đang hoạt động trên máy tính. Nói dễ hiểu hơn, CPU có nhiệm vụ chính là nhận thông tin từ các thiết bị ngoại vi hoặc chương trình máy tính, sau đó phân tích và thực hiện các tác vụ cần thiết, bao gồm hiển thị thông tin lên màn hình và thực hiện các yêu cầu của các thiết bị ngoại vi.

### CPU của hosting
CPU của hosting là thông số của CPU, là % CPU đang sử dụng của gói hosting. Thông thường gói CPU của hosting dao động từ 75% – 3000%. Thông số này càng cao thì khả năng xử lý của hosting càng mạnh.

### Cách CPU làm việc
CPU là gì đã được giải thích đơn giản như trên, vậy cách mà bộ xử lý trung tâm hoạt động là như thế nào? Một CPU sẽ có nhiệm vụ chính là điều khiển toàn bộ cơ chế làm việc của máy tính theo thuật toán và thao tác người dùng.

CPU sẽ nhận thông tin từ những thiết bị ngoại vi bao gồm: Chuột, máy in, bàn phím,… đồng thời kết hợp với chương trình đã lập trình trên máy tính và xử lý thông qua các phân tích phép tính, logic, so sánh để xuất kết quả ra màn hình. Ngoài ra, những yêu cầu từ thiết bị ngoại vi cũng được xử lý nhanh chóng.

### Cấu tạo của CPU gồm 
Về cơ bản CPU có nghĩa là bộ xử lý trung tâm, thế nên nó sẽ là sự kết hợp của nhiều chi tiết với công dụng khác nhau. Dưới đây là 5 bộ phận cấu tạo hoàn chỉnh của mỗi chiếc CPU mà Vietnix đã tổng hợp.

- Khối điều khiển (CU – Control Unit)

Khối điều khiển còn được gọi là CU – Control Unit, chức năng chính của bộ phận gồm:

- CU đảm nhiệm việc dịch các lệnh đang xuất hiện trên chương trình máy tính.
- CU có tác dụng điều khiển việc xử lý các lệnh.

Đây là một phần quan trọng hàng đầu trong bộ xử lý trung tâm được cấu tạo bởi những mạch logic so sánh cùng những chi tiết bán dẫn transistor. Ngoài ra, xung nhịp đồng hồ sẽ là yếu tố điều tiết chính xác hoạt động của CU.

- Khối tính toán (ALU – Arithmetic Logic Unit)

Đây là một bộ phận được gọi là Arithmetic Logic Unit (ALU) đảm nhiệm chức năng thực hiện giải các phép toán gồm: Số học, logic, so sánh. Sau khi hoàn thành quá trình này, ALU sẽ đưa ra kết quả và trả về bộ nhớ hoặc thanh ghi.

- Các thanh ghi (Registers)

Thanh ghi (Registers) là những bộ nhớ với dung lượng thấp tuy nhiên lại có đặc tính về tốc độ truy cập vô cùng cao. Bộ phận này sẽ có nhiệm vụ cơ bản là lưu trữ dữ liệu hoặc kết quả tạm thời có thể kể đến như: Kết quả thực hiện tính toán, dữ kiện các ô nhớ, toán hạng, thông tin điều khiển. CPU sẽ có nhiều thanh ghi nhưng quan trọng nhất là PC – Program Counter (bộ đếm chương trình) đề ra lệnh sẽ được thực hiện kế tiếp.

- Opcode

Opcode trong CPU là bộ phận lưu trữ mã máy của bộ xử lý trung tâm được thực hiện các lệnh trong tệp được cho phép.

- Phần điều khiển

Nhiệm vụ của phần điều khiển trong CPU là gì? Đối với bộ phận này sẽ có 2 nhiệm vụ chính, gồm chức năng điều khiển toàn bộ các khối được trang bị tại CPU và kiểm soát tần số xung nhịp của hệ thống.

## RAM
RAM viết tắt của từ Random Access Memory, là bộ nhớ tạm thời của thiết bị giúp lưu trữ các dữ liệu trong thời gian nhất định hỗ trợ CPU trong hoạt động truy xuất và thực thi. Đây là bộ phận quan trọng hàng đầu đứng cạnh vi xử lý.

RAM đóng vai trò tất yếu ở hầu hết thiết bị điện tử có thể nói đến như laptop, PC, máy tính bảng, điện thoại thông minh, máy in,… Ngoài ra, nó còn có đặc tính như tên gọi bộ nhớ tạm thời, nghĩa là khi thiết bị tắt (ngắt nguồn điện), mọi dữ liệu hoàn toàn biến mất. 

ROM là viết tắt của Read Only Memory, có nghĩa là bộ nhớ chỉ đọc. Đây là loại bộ nhớ không khả biến được sử dụng trong các thiết bị tính và hệ thống điều khiển, nơi mà dữ liệu chỉ có thể được đọc mà không thể ghi. Bộ nhớ ROM chứa các chương trình quan trọng giúp khởi động máy tính và nếu thiếu thành phần này, máy tính sẽ không hoạt động được.

### Cấu tạo của RAM

Với chức năng vô cùng quan trọng trong thiết bị, RAM sẽ được cấu tạo từ nhiều bộ phận khác nhau để tạo ra hiệu năng tối ưu. Trong đó, 5 bộ phận gồm bo mạch, chip SPD, vi xử lý, bộ đếm, ngân hàng bộ nhớ. Chi tiết các bộ phận như sau:

1. Bo mạch

Bo mạch hay còn được hiểu đơn giản là bảng mạch chứa toàn bộ các thành phần cấu tạo nên RAM. Bên cạnh đó, mạch bán dẫn silicon có vai trò kết nối các bộ phận của bộ nhớ vào máy tính.

2. Chip SPD

Chip SPD có tên chuẩn là serial presence detect được tích hợp ngay trên bo mạch và giúp lưu giữ những dữ liệu như: Tốc độ, kích thước, thời gian truy cập và loại bộ nhớ. Với bộ phận này, nó cho phép người dùng truy cập các thông tin nhất định ngay khi mở thiết bị. 

3. Vi xử lý

Đối với DRAM, các hoạt động của bộ nhớ hoàn toàn không được đồng bộ. Ngược lại, SDRAM sẽ hỗ trợ động bộ hóa tất tần tật dữ liệu bằng vi xử lý. Việc này mang đến người dùng trải nghiệm điều khiển tốt hơn và cắt giảm gần như tuyệt đối các tín hiệu không phù hợp. 

4. Bộ đếm

Với mục đích nâng cao tốc độ truy cập cụm, các bộ đếm trên RAM hỗ trợ theo dõi những địa chỉ cột để tối ưu việc này. Bộ đếm sẽ dùng đến 2 loại cụm bao gồm xen kẽ và tuần tự.

5. Ngân hàng bộ nhớ 

Một thành phần không thể thiếu của RAM là ngân hàng bộ nhớ. Bộ phận này bao hàm những mô đun lưu trữ thông tin. SDRAM sẽ có tối thiểu 2 ngân hàng bộ nhớ hoặc nhiều hơn thế nữa, đồng thời còn cấp quyền cho một đối tượng bất kỳ truy cập vào các ngân hàng khác.

### Cơ chế hoạt động của RAM

RAM hoạt động như một trung gian luân chuyển dữ liệu giữa ổ cứng và CPU. Cơ chế hoạt động cụ thể của RAM như sau:

- Khi bạn mở một ứng dụng hoặc trò chơi, thiết bị sẽ tải dữ liệu mà CPU cần xử lý lên RAM.
- CPU sẽ truy xuất dữ liệu từ RAM để thực hiện các tác vụ cần thiết cho ứng dụng.
- Nếu người dùng ngắt nguồn điện của thiết bị hoặc tắt ứng dụng, các thông tin trong RAM sẽ được trả về ổ đĩa. 

Hiểu đơn giản, chức năng của RAM trong máy tính hay điện thoại nhằm phối hợp với bộ nhớ máy tính giúp bạn truy cập, điều khiển và dùng dữ liệu. Bạn có thể coi RAM giống như trí nhớ ngắn hạn của con người, nơi để lưu trữ dữ liệu tạm thời cho các hoạt động sắp diễn ra như như danh sách mua sắm siêu thị, số điện thoại cần gọi,… Nếu bị mất trí nhớ ngắn hạn, bạn sẽ không thể nhớ được bất cứ điều gì quá một vài giây.

Ngược lại nếu trí nhớ ngắn hạn tốt thì bạn có thể nhớ được nhiều thông tin hơn để phục vụ cho các hoạt động trong ngày. Tương tự, RAM giúp lưu trữ dữ liệu tạm thời cho hệ điều hành và các ứng dụng đang chạy. RAM càng nhiều thì máy tính, điện thoại của bạn sẽ càng có thể chạy nhiều ứng dụng cùng lúc và hoạt động mượt mà hơn.

### Các loại RAM phổ biến

RAM được phân chia thành hai loại, đó là SRAM và DRAM. SRAM, hay còn được biết đến là RAM tĩnh – không mất dữ liệu sau khi máy tính được khởi động và thường được sử dụng để lưu trữ thông tin khởi động. Ngược lại là DRAM – RAM động, được sử dụng để tạm thời lưu trữ dữ liệu khi ứng dụng đang chạy và có thể bị giải phóng vùng nhớ khi ứng dụng đóng, máy tính tắt hoặc điện thoại tắt.

![ảnh](https://github.com/user-attachments/assets/4dcdb8ae-e4e1-4b40-9d0d-91eb3b07b5aa)

Có 6 loại RAM động:

1. SDRAM: Đây là bộ nhớ tạm thời đồng bộ có tên chuẩn là Synchronous Dynamic RAM.
2. DDR (Double Data Rate SDRAM): Đây là phiên bản nâng cấp của SDR được ra mắt khá lâu trước đây và hiện tại còn rất ít thiết bị sử dụng loại này. 
3. DDR2: Có thể nói, phiên bản này được cải tiến khá mạnh so với DDR vào thời điểm được ra mắt. Thế nhưng, hiện nay chỉ có các thiết bị đời cũ sử dụng.
4. DDR3: Có thể nói, dòng DDR3 đã và đang được người dùng sử dụng nhiều nhất với hiệu năng ổn định được tối ưu.
5. RDRAM: Với loại bộ nhớ này đã được các kỹ sư thiết kế theo tiêu chuẩn tiên tiến hoàn toàn so với những phiên bản trước đó. Ngoài ra, nó còn được gọi là Ram bus (Rambus Dynamic RAM).
6. DDR4: Là bản thay thế cho DDR3, xuất hiện lần đầu ở năm 2014, nó được nâng cấp về tốc độ (khoảng 2133 – 4266 MHz khi truyền tải), sử dụng điện áp thấp (chỉ cần 1.2V). Vì thế, DDR4 sẽ có mức giá nhỉnh hơn thế hệ tiền nhiệm. 


## SSL

SSL (Secure Sockets Layer) là một giao thức bảo mật được thiết kế để mã hóa dữ liệu giữa trình duyệt web và máy chủ web. SSL giúp bảo vệ dữ liệu nhạy cảm (như thông tin đăng nhập, dữ liệu thẻ tín dụng) khỏi bị nghe lén hoặc can thiệp trong quá trình truyền tải. SSL đã được thay thế bởi TLS (Transport Layer Security), nhưng thuật ngữ SSL vẫn thường được sử dụng để chỉ các chứng chỉ bảo mật và giao thức hiện tại.

### Có ba phương pháp chính để chứng thực SSL:

1. Chứng thực với Chứng chỉ (Certificate-based Authentication):
- Đây là phương pháp phổ biến nhất, trong đó máy chủ sử dụng chứng chỉ SSL để mã hóa dữ liệu và xác thực danh tính của nó. Khi trình duyệt kết nối đến máy chủ, máy chủ sẽ gửi chứng chỉ SSL và trình duyệt sẽ kiểm tra chứng chỉ đó.

2. Chứng thực với Tên miền (Domain-based Authentication):
- Phương pháp này xác thực rằng người yêu cầu chứng chỉ là chủ sở hữu của tên miền. Quy trình này thường bao gồm việc kiểm tra thông tin tên miền và có thể yêu cầu xác nhận qua email hoặc các phương pháp khác.

3. Chứng thực với Doanh nghiệp (Organization-based Authentication):
- Phương pháp này cung cấp mức độ bảo mật cao hơn bằng cách xác minh không chỉ tên miền mà còn thông tin về tổ chức hoặc doanh nghiệp yêu cầu chứng chỉ. Các chứng chỉ này thường được gọi là Extended Validation (EV) SSL Certificates.

### CSR (Certificate Signing Request) 
là một tệp được tạo ra bởi máy chủ yêu cầu chứng chỉ SSL. Tệp CSR chứa các thông tin quan trọng cần thiết để cấp chứng chỉ SSL, bao gồm:

- Tên miền hoặc tên tổ chức.
- Tên tổ chức (nếu có).
- Địa chỉ email liên hệ.
- Thông tin địa lý (thành phố, quốc gia).
- Khóa công khai (public key) để mã hóa thông tin.

Quá trình tạo chứng chỉ SSL thường bao gồm việc tạo CSR, sau đó gửi CSR đến CA (Certificate Authority) để yêu cầu cấp chứng chỉ SSL. CA sử dụng thông tin trong CSR để tạo chứng chỉ SSL hợp lệ.

### Sử dụng OpenSSL để gen file CSR sau đó request SSL cho domain tech.training.vietnix.tech

#Tạo private key
openssl genpkey -algorithm RSA -out tech.training.vietnix.tech.key -aes256

#Tạo CSR
openssl req -new -key tech.training.vietnix.tech.key -out tech.training.vietnix.tech.csr

Quá trình tạo CSR sẽ yêu cầu bạn nhập thông tin liên quan đến chứng chỉ. Tệp tech.training.vietnix.tech.csr sau đó có thể được gửi đến CA để yêu cầu chứng chỉ SSL.

### PEM (Privacy-Enhanced Mail) 
là định dạng tệp thường được sử dụng để lưu trữ chứng chỉ SSL, khóa riêng (private key), và các dữ liệu bảo mật khác. Tệp PEM thường có đuôi .pem, .crt, .cer, hoặc .key và chứa dữ liệu được mã hóa bằng Base64 giữa các đoạn tiêu đề như -----BEGIN CERTIFICATE----- và -----END CERTIFICATE-----.

### Private Key (Khóa Riêng) 
là một phần của cặp khóa được sử dụng trong mã hóa SSL/TLS. Khóa riêng được giữ bí mật và không được chia sẻ với bất kỳ ai ngoài tổ chức yêu cầu chứng chỉ. Nó được sử dụng để giải mã dữ liệu mà khóa công khai (public key) đã mã hóa và để ký các yêu cầu chứng chỉ (CSR). Việc bảo mật khóa riêng là rất quan trọng để đảm bảo an toàn cho kết nối SSL.

### PFX (Personal Information Exchange)
là định dạng tệp chứa chứng chỉ SSL, khóa riêng (private key), và các chứng chỉ trung gian (intermediate certificates) trong một tệp duy nhất. PFX, thường có đuôi .pfx hoặc .p12, cho phép bạn xuất và nhập các chứng chỉ SSL cùng với khóa riêng.

### Cách chuyển từ file crt file sang PFX file.

Để chuyển từ file .crt (hoặc .pem) và khóa riêng (.key) sang tệp PFX, bạn có thể sử dụng lệnh OpenSSL sau:

openssl pkcs12 -export -out tech.training.vietnix.tech.pfx -inkey tech.training.vietnix.tech.key -in tech.training.vietnix.tech.crt -certfile intermediate.crt

Trong lệnh trên:

- export: Chỉ định rằng bạn đang tạo một tệp PFX.
- out tech.training.vietnix.tech.pfx: Tên tệp PFX đầu ra.
- inkey tech.training.vietnix.tech.key: Tệp khóa riêng.
- in tech.training.vietnix.tech.crt: Tệp chứng chỉ chính.
- certfile intermediate.crt: (Tùy chọn) Tệp chứng chỉ trung gian, nếu có.

Lệnh này sẽ yêu cầu bạn nhập mật khẩu để bảo vệ tệp PFX, và sau đó tạo ra tệp .pfx chứa tất cả các thông tin cần thiết.

## ping/hping3 
### ping 
ping là một công cụ cơ bản để kiểm tra kết nối mạng bằng cách gửi gói tin ICMP Echo Request đến một địa chỉ IP hoặc tên miền và nhận lại gói tin ICMP Echo Reply.
### hping3 
hping3 là một công cụ mạnh mẽ hơn, cho phép bạn gửi nhiều loại gói tin và tùy chỉnh các thông số.
### ping đến domain vietnix.vn 

![ảnh](https://github.com/user-attachments/assets/4851f889-252a-40d3-817a-67f6d7db4bdb)

- TTL: Cho biết số lượng router (hops) mà gói tin đã đi qua hoặc khả năng sống sót của gói tin trong mạng.
- Time: Cho biết thời gian mà gói tin mất để đi từ nguồn đến đích và trở lại, đo bằng miligiây.

## ssh command
Lệnh ssh (Secure Shell) được sử dụng để kết nối đến một máy chủ từ xa một cách an toàn qua mạng. Dưới đây là hướng dẫn về cách sử dụng lệnh ssh trong các tình huống khác nhau

### Dùng password
ssh username@hostname_or_ip

- username là tên người dùng trên máy chủ từ xa.
- hostname_or_ip là tên miền hoặc địa chỉ IP của máy chủ từ xa.

Khi bạn chạy lệnh này, bạn sẽ được yêu cầu nhập mật khẩu của người dùng trên máy chủ từ xa.
### Dùng key

#### Tạo cặp khóa SSH
Trước tiên, bạn cần tạo một cặp khóa SSH gồm một khóa công khai (public key) và một khóa riêng (private key). Để làm điều này, bạn sử dụng lệnh ssh-keygen.

ssh-keygen -t rsa

Sau khi chạy lệnh, bạn sẽ được yêu cầu chọn vị trí lưu khóa và cung cấp mật khẩu (passphrase) để bảo vệ khóa riêng. Mặc định, khóa được lưu tại ~/.ssh/id_rsa và khóa công khai tại ~/.ssh/id_rsa.pub.

#### Cài đặt khóa công khai trên máy chủ từ xa
Để sử dụng khóa SSH, bạn cần phải cài đặt khóa công khai của bạn vào tệp authorized_keys trên máy chủ từ xa. Bạn có thể sử dụng lệnh ssh-copy-id để thực hiện điều này dễ dàng.

ssh-copy-id -i ~/.ssh/id_rsa.pub username@hostname_or_ip

-i ~/.ssh/id_rsa.pub: Chỉ định tệp khóa công khai bạn muốn cài đặt.
username@hostname_or_ip: Thay thế bằng tên người dùng và địa chỉ IP hoặc tên miền của máy chủ từ xa.

Lệnh này sẽ thêm khóa công khai của bạn vào tệp ~/.ssh/authorized_keys trên máy chủ từ xa.

#### Kết nối bằng khóa SSH

Sau khi khóa công khai đã được cài đặt trên máy chủ từ xa, bạn có thể kết nối mà không cần nhập mật khẩu, chỉ cần khóa riêng của bạn.

ssh -i ~/.ssh/id_rsa username@hostname_or_ip

-i ~/.ssh/id_rsa: Chỉ định tệp khóa riêng của bạn.
username@hostname_or_ip: Tên người dùng và địa chỉ IP hoặc tên miền của máy chủ từ xa.

#### Cấu hình SSH Client (Tùy chọn)
Bạn có thể cấu hình SSH client để sử dụng khóa mặc định mà không cần chỉ định mỗi lần bằng cách chỉnh sửa tệp cấu hình ~/.ssh/config. Ví dụ:

Host example
    HostName hostname_or_ip
    User username
    IdentityFile ~/.ssh/id_rsa
    Port 22

Host example: Tên gọi tắt cho máy chủ từ xa.
HostName hostname_or_ip: Địa chỉ IP hoặc tên miền của máy chủ từ xa.
User username: Tên người dùng trên máy chủ từ xa.
IdentityFile ~/.ssh/id_rsa: Đường dẫn đến tệp khóa riêng của bạn.
Port 22: Cổng SSH (thay đổi nếu sử dụng cổng khác).

Khi cấu hình tệp này, bạn có thể kết nối bằng cách đơn giản:

ssh example
#### Bảo mật khóa riêng
Khóa riêng (private key) phải được bảo vệ cẩn thận. Nếu khóa riêng của bạn bị lộ, bất kỳ ai có khóa công khai tương ứng có thể truy cập vào hệ thống của bạn.

Lưu ý bảo mật:

- Sử dụng passphrase: Khi tạo khóa, sử dụng một passphrase để bảo vệ khóa riêng của bạn.
-Phân quyền đúng: Đảm bảo tệp khóa riêng có quyền truy cập chỉ dành cho bạn. Bạn có thể thiết lập quyền bằng lệnh:

chmod 600 ~/.ssh/id_rsa

Không chia sẻ khóa riêng: Chỉ chia sẻ khóa công khai.

### Dùng port custom
Nếu máy chủ từ xa đang chạy SSH trên một cổng khác ngoài cổng mặc định (22), bạn có thể chỉ định cổng tùy chỉnh bằng tùy chọn -p. Cú pháp là:

ssh -p port_number username@hostname_or_ip

- port_number là số cổng tùy chỉnh mà máy chủ từ xa đang lắng nghe.
- username là tên người dùng trên máy chủ từ xa.
- hostname_or_ip là tên miền hoặc địa chỉ IP của máy chủ từ xa.

## scp command
Lệnh scp (secure copy) được sử dụng để sao chép tập tin và thư mục giữa máy tính của bạn và một máy chủ từ xa hoặc giữa hai máy chủ từ xa thông qua SSH

### scp 1 file
#### Từ máy tính của bạn đến máy chủ từ xa:

scp /path/to/local/file username@remote_host:/path/to/remote/directory/

- /path/to/local/file: Đường dẫn đến tập tin trên máy tính của bạn.
- username@remote_host: Tên người dùng và địa chỉ IP hoặc tên miền của máy chủ từ xa.
- /path/to/remote/directory/: Thư mục đích trên máy chủ từ xa.

#### Từ máy chủ từ xa về máy tính của bạn:

scp username@remote_host:/path/to/remote/file /path/to/local/directory/

- username@remote_host: Tên người dùng và địa chỉ IP hoặc tên miền của máy chủ từ xa.
- /path/to/remote/file: Đường dẫn đến tập tin trên máy chủ từ xa.
- /path/to/local/directory/: Thư mục đích trên máy tính của bạn.

### scp 1 folder
Để sao chép toàn bộ thư mục, bạn cần sử dụng tùy chọn -r (recursive) để sao chép tất cả các tập tin và thư mục con.

#### Từ máy tính của bạn đến máy chủ từ xa:

scp -r /path/to/local/folder username@remote_host:/path/to/remote/directory/

- /path/to/local/folder: Đường dẫn đến thư mục bạn muốn sao chép trên máy tính của bạn.
- username@remote_host: Tên người dùng và địa chỉ IP hoặc tên miền của máy chủ từ xa.
- /path/to/remote/directory/: Thư mục đích trên máy chủ từ xa.

#### Từ máy chủ từ xa về máy tính của bạn:

scp -r username@remote_host:/path/to/remote/folder /path/to/local/directory/

- username@remote_host: Tên người dùng và địa chỉ IP hoặc tên miền của máy chủ từ xa.
- /path/to/remote/folder: Đường dẫn đến thư mục trên máy chủ từ xa.
- /path/to/local/directory/: Thư mục đích trên máy tính của bạn.

## rsync command
Rsync (Remote Sync) là một công cụ hữu hiệu để sao lưu và đồng bộ dữ liệu trên Linux. Với câu lệnh rsync bạn có thể sao lưu và đồng bộ dữ liệu remote từ các máy sử dụng hệ điều hành Linux một cách dễ dàng và thuận tiện. 

Cú pháp cơ bản

rsync options source destination

Các tuỳ chọn trong rsync

-v : verbose

-r : sao chép dữ liệu theo cách đệ quy ( không bảo tồn mốc thời gian và permission trong quá trình truyền dữ liệu)

-a :chế độ lưu trữ cho phép sao chép các tệp đệ quy và giữ các liên kết, quyền sở hữu, nhóm và mốc thời gian

-z : nén dữ liệu

-h : định dạng số

### rsync file
rsync -av /source/path/file.txt /destination/path/

### rsync folder
rsync -av /source/path/folder/ /destination/path/

### rsync increamental
rsync -av --delete /source/path/ /destination/path/

## cat command
Cat command trong Linux là một lệnh thường dùng nhất và bạn cần học. Nó là chữ viết tắt của từ concatenate. Nó giúp bạn tạo, nhập, print file tới màn hình chuẩn hay tới một file khác, và còn nhiều tính năng khác nữa.

Cú pháp Cat Command

cat [OPTION] [FILE]


### cat nội dung 1 file
Để hiển thị nội dung của một tệp, bạn sử dụng lệnh:

cat filename.txt

### cat dòng thứ <n> trong file
cat không trực tiếp hỗ trợ việc hiển thị dòng cụ thể, nhưng bạn có thể kết hợp với sed để làm điều này:

sed -n '<n>p' filename.txt

Trong đó, <n> là số dòng mà bạn muốn hiển thị. Ví dụ, để hiển thị dòng thứ 3, bạn dùng:

sed -n '3p' filename.txt

### cat nhiều dòng vào 1 file bằng EOF
Bạn có thể sử dụng cú pháp here document với EOF để thêm nhiều dòng vào một tệp. Ví dụ:

cat <<EOF > filename.txt
Line 1
Line 2
Line 3
EOF

Lệnh này sẽ ghi nội dung từ Line 1 đến Line 3 vào filename.txt. Bạn cũng có thể dùng >> thay vì > nếu muốn thêm các dòng này vào cuối tệp mà không ghi đè nội dung hiện có.

## echo command
Lệnh echo trong Unix/Linux được sử dụng để hiển thị thông điệp hoặc nội dung chuỗi lên màn hình hoặc chuyển hướng vào tệp

### Dùng echo để chèn thêm 1 dòng vào cuối file
Bạn có thể sử dụng >> để thêm nội dung vào cuối tệp mà không ghi đè nội dung hiện có. Ví dụ:

echo "This is a new line" >> filename.txt

Lệnh này sẽ chèn dòng "This is a new line" vào cuối filename.txt.

### Dùng echo để overwirte nội dung của file
Để ghi đè toàn bộ nội dung của tệp bằng lệnh echo, bạn sử dụng > thay vì >>. Ví dụ:

echo "This is the new content" > filename.txt

Lệnh này sẽ thay thế toàn bộ nội dung hiện có của filename.txt bằng dòng "This is the new content".

## tail/head command
### Head
Lệnh head được dùng để in ra các phần đầu tiên của tệp. Nó đọc các tập tin từ đầu. Nếu bạn có một tệp có hơn một nghìn dòng, sẽ rất khó mở và đọc nó. Bạn có thể dễ dàng in ra một vài dòng trên cùng bằng lệnh head.

Cú pháp cơ bản của lệnh là:

head [option] [file]

Lệnh head được sử dụng để hiển thị các dòng đầu tiên của tệp. Theo mặc định, head hiển thị 10 dòng đầu tiên.

Hiển thị 10 dòng đầu tiên của tệp:

head filename.txt

Hiển thị n dòng đầu tiên của tệp:

head -n 20 filename.txt


### Tail 
Lệnh này in các dòng cuối cùng của tệp. Nó đọc các tệp từ cuối và xuất ra các dòng cuối. 

Cú pháp cơ bản của lệnh là:

tail [option] [file]

Lệnh tail được sử dụng để hiển thị các dòng cuối cùng của tệp. Theo mặc định, tail hiển thị 10 dòng cuối cùng.

Hiển thị 10 dòng cuối cùng của tệp:

tail filename.txt

Hiển thị n dòng cuối cùng của tệp:

tail -n 20 filename.txt

#### tail và tailf
##### Lệnh tail với tùy chọn -f

tail với tùy chọn -f được sử dụng để theo dõi một tệp trong thời gian thực, tức là hiển thị nội dung mới được thêm vào cuối tệp khi tệp đó được ghi thêm. Đây là tính năng phổ biến nhất khi theo dõi các tệp nhật ký.

tail -f filename.txt

Tùy chọn -f của tail có các tính năng hiện đại như khả năng xử lý tốt khi tệp được ghi đè hoặc di chuyển.

##### Lệnh tailf

tailf là một lệnh cũ và gần giống với tail -f, nhưng có một số khác biệt nhỏ:

- Hiệu năng: tailf được tối ưu hóa hơn cho việc theo dõi các tệp không thường xuyên cập nhật. Nó không kiểm tra thay đổi tệp liên tục như tail -f mà chỉ kiểm tra khi có hoạt động đọc mới, giúp giảm tải hệ thống khi theo dõi các tệp lớn ít thay đổi.

- Giới hạn: tailf không hỗ trợ tùy chọn mở rộng hoặc theo dõi các tệp đã được di chuyển hoặc ghi đè. Nó sẽ ngừng theo dõi khi tệp bị di chuyển hoặc thay thế, điều này đã làm cho tailf trở nên ít phổ biến hơn và không còn được khuyến nghị sử dụng.

tailf filename.txt

## sed command
sed (Stream Editor) là một công cụ mạnh mẽ trong Unix/Linux để xử lý và biến đổi văn bản. Một trong những tính năng phổ biến nhất của sed là tìm kiếm và thay thế chuỗi.

### Dùng sed để find and replace một string trong file

sed 's/old_string/new_string/g' filename.txt

s: Là lệnh thay thế (substitute).
old_string: Chuỗi bạn muốn tìm kiếm.
new_string: Chuỗi bạn muốn thay thế.
g: Tùy chọn toàn cục (global), thay thế tất cả các lần xuất hiện của old_string trong dòng. Nếu bỏ qua tùy chọn này, sed sẽ chỉ thay thế lần xuất hiện đầu tiên trên mỗi dòng.
filename.txt: Tệp mà bạn muốn thay đổi.
## traceroute/tracert command
Traceroute (hay tracert trên Windows) là một công cụ chẩn đoán mạng máy tính để hiển thị các tuyến đường (đường dẫn) và đo lường sự chậm trễ quá cảnh của các gói dữ liệu trên một giao thức Internet (IP) mạng.

traceroute sử dụng bản tin time to live expired của lệnh ping để biết được từng chặng mà gói tin sẽ phải đi qua trước khi đến đích.

Sau khi traceroute xong giải thích chi tiết kết quả trả về

![ảnh](https://github.com/user-attachments/assets/a0d1b8af-ba02-4265-90fb-99c4660a1fc3)

## netstat command
netstat là một công cụ dòng lệnh được sử dụng để theo dõi số liệu thống kê về mạng. Nó cho phép bạn xem dữ liệu mạng như các cổng đang sử dụng, các kết nối đang hoạt động, các gói đã được chuyển, v.v.

### hiển thị các socket đang listen

![ảnh](https://github.com/user-attachments/assets/5611c06a-c882-42a2-9909-816e661502f1)

### don't resolve hostname
Không giải quyết hostname: -n

![Chụp màn hình từ 2024-08-05 08-55-32](https://github.com/user-attachments/assets/a63ac3b5-586d-4753-ae5e-63c2d6440a61)

### don't resolve portname
Không giải quyết portname: -n (đồng thời không giải quyết cả hostname và portname)

![Chụp màn hình từ 2024-08-05 08-55-32](https://github.com/user-attachments/assets/e08e148b-9bce-4bb8-8248-64093af511f9)

### display process name/PID
Hiển thị tên tiến trình và PID: -p

![Chụp màn hình từ 2024-08-05 08-56-42](https://github.com/user-attachments/assets/62b55fb3-b0b0-41c6-a634-bcef0e725bef)

### only show tcp socket
Chỉ hiển thị socket TCP: -t

![ảnh](https://github.com/user-attachments/assets/4716d5ab-5d20-448a-b0a5-9f625b5827ab)

### only show udp socket
Chỉ hiển thị socket UDP: -u

![ảnh](https://github.com/user-attachments/assets/02454160-5195-4d10-a0cb-57772f059181)

## sort command
Lệnh sort trong Unix/Linux được sử dụng để sắp xếp dữ liệu. Dưới đây là cách sử dụng sort để sắp xếp theo thứ tự tăng dần, giảm dần và theo cột cụ thể:

### sort theo thứ tự tăng dần
![ảnh](https://github.com/user-attachments/assets/103b5550-f13f-48b6-8047-409624205566)

### sort theo thứ tự giảm dần

![Uploading Chụp màn hình từ 2024-08-05 09-42-21.png…]()

### sort theo column
![ảnh](https://github.com/user-attachments/assets/00f06b5a-37f1-49f6-9bbe-6f03f7118eb5)


## uniq command
Lệnh uniq trong Linux được sử dụng để hiển thị các dòng giống hệt nhau trong tệp văn bản
### lọc ra các dòng lặp lại trong một file
uniq -d file.txt 
### lọc ra các dòng lặp lại trong file và đếm số lượng các dòng lặp lại
uniq -d -c file.txt 

## wc command
Lệnh wc (word count) có thể được sử dụng để đếm số dòng, số từ, và số ký tự trong một file. Dưới đây là cách sử dụng wc cho các yêu cầu của bạn:

### Đếm số dòng trong file
wc -l file.txt 
### Đếm số kí tự trong file
wc -m file.txt 

## chmod, chown, chattr command
Các lệnh chmod, chown và chattr là những công cụ cơ bản và quan trọng trong hệ thống Linux/Unix để quản lý quyền truy cập vào các tập tin và thư mục. Chúng cho phép người dùng điều chỉnh quyền sở hữu, quyền đọc, ghi và thực thi đối với các đối tượng trên hệ thống.

Lệnh chmod: Thay đổi quyền truy cập

Lệnh chown: Thay đổi chủ sở hữu và nhóm

Lệnh chattr: Thay đổi các thuộc tính mở rộng

### Phân quyền bằng số, phân quyền bằng chữ
chmod - Phân quyền bằng số và bằng chữ

#### Phân quyền bằng số:
Mỗi quyền được biểu diễn bằng một con số từ 0 đến 7:
- 0: không có quyền nào
- 1: quyền thực thi (x)
- 2: quyền ghi (w)
- 3: quyền thực thi + ghi (wx)
- 4: quyền đọc (r)
- 5: quyền đọc + thực thi (rx)
- 6: quyền đọc + ghi (rw)
- 7: quyền đọc + ghi + thực thi (rwx)

Ví dụ: chmod 755 file.txt sẽ cấp quyền rwxr-xr-x cho tệp tin file.txt.

 #### Phân quyền bằng chữ:
        u: user (chủ sở hữu)
        g: group (nhóm)
        o: other (người khác)
        a: all (tất cả)
        Ví dụ: chmod u=rwx,g=rx,o=r file.txt sẽ cấp quyền rwxr-xr-- cho tệp tin file.txt.

### Đổi owner user/group
chown dùng để thay đổi chủ sở hữu (user) và nhóm (group) của một tệp tin hoặc thư mục.

Ví dụ:

    chown user1 file.txt: Thay đổi chủ sở hữu của file.txt thành user1.
    chown user1:group1 file.txt: Thay đổi chủ sở hữu và nhóm của file.txt thành user1:group1.

### Set Immutable Attribute
chattr dùng để thay đổi các thuộc tính đặc biệt của một tệp tin hoặc thư mục.

Một trong những thuộc tính quan trọng là immutable, nó ngăn không cho tệp tin được xóa, sửa đổi hay ghi đè.

Ví dụ:

    chattr +i file.txt: Đặt thuộc tính immutable cho file.txt.
    chattr -i file.txt: Bỏ thuộc tính immutable khỏi file.txt.

## find command
Lệnh find là một công cụ hữu ích để tìm kiếm các tệp tin trong hệ thống Linux. Nó cho phép người dùng tìm kiếm theo nhiều tiêu chí khác nhau và thực hiện các hành động trên các tệp tin được tìm thấy

### find các file có đuôi .log
find / -type f -name "*.log"

    find /: Tìm kiếm trên toàn bộ hệ thống (/ là thư mục gốc).
    -type f: Chỉ tìm kiếm các tệp tin (file), không tìm thư mục.
    -name "*.log": Tìm kiếm các tệp tin có tên kết thúc bằng .log.

### find các folder có tên abc
find / -type d -name "abc"

    -type d: Chỉ tìm kiếm các thư mục.
    -name "abc": Tìm các thư mục có tên chính xác là abc.

### find các file có tên abc
find / -type f -name "abc"

    -type f: Chỉ tìm kiếm các tệp tin.
    -name "abc": Tìm các tệp tin có tên chính xác là abc.

### find các file có tên abc và thực hiện phần quyền read only cho file
find / -type f -name "abc" -exec chmod 444 {} \;

    -exec chmod 444 {} \;: Sau khi tìm thấy các tệp tin, thực hiện lệnh chmod 444 {} trên chúng. Trong đó {} được thay thế bằng đường dẫn của từng tệp tin được tìm thấy.
    chmod 444: Cấp quyền read-only (r--r--r--) cho các tệp tin.

## cp command
Lệnh cp trong Linux/Unix được sử dụng để sao chép các tệp tin và thư mục

### cp file
cp file.txt file_copy.txt

Câu lệnh này sẽ tạo một bản sao của tệp tin file.txt với tên file_copy.txt trong cùng thư mục.
### cp folder
cp -r documents/ documents_backup/

Câu lệnh này sẽ sao chép toàn bộ nội dung của thư mục documents/ sang thư mục mới documents_backup/. Tùy chọn -r (recursive) cho phép sao chép cả các thư mục con. 

## mv command
Lệnh mv trong Linux/Unix được sử dụng để di chuyển hoặc đổi tên các tệp tin và thư mục.

### mv file, folder
#### Di chuyển tệp tin: 
mv file.txt documents/

Câu lệnh này sẽ di chuyển tệp tin file.txt vào thư mục documents/. 
#### Đổi tên tệp tin: 
mv file.txt new_file.txt

Câu lệnh này sẽ đổi tên tệp tin file.txt thành new_file.txt. 

#### Di chuyển thư mục: 
mv documents/ documents_backup/

Câu lệnh này sẽ di chuyển thư mục documents/ vào thư mục documents_backup/. 

#### Đổi tên thư mục: 
mv documents/ new_folder/

Câu lệnh này sẽ đổi tên thư mục documents/ thành new_folder/. 
## cut command
Lệnh cut trong Linux/Unix được sử dụng để trích xuất một phần của một chuỗi ký tự

### cut kí tự thứ <n> trong string
echo "Hello, World!" | cut -c 7

![ảnh](https://github.com/user-attachments/assets/c1c2508b-f526-4654-a829-d69a43a75a22)

### cut từ kí tự thứ <n> trở về sau
echo "Hello, World!" | cut -c 7-

![ảnh](https://github.com/user-attachments/assets/fffcdb7d-86b9-475f-a47b-bf86e0050f05)

Kết quả: World!
Lệnh này sẽ trích xuất các ký tự từ vị trí thứ 7 trở về sau trong chuỗi "Hello, World!".
### cut từ kí tự thứ <n> trở về trước
echo "Hello, World!" | cut -c -6

![Uploading ảnh.png…]()

Kết quả: Hello,
Lệnh này sẽ trích xuất các ký tự từ đầu chuỗi đến ký tự thứ 6 trong chuỗi "Hello, World!".
# dig command
Lệnh dig (Domain Information Groper) là một công cụ mạnh mẽ để kiểm tra thông tin về các bản ghi DNS (Domain Name System) khác nhau

### Dùng Dig command để kiểm tra resolv record A, MX, NS
#### resolv record A
dig vietnix.vn A

#### resolv record MX
dig vietnix.vn MX

#### resolv record NS
dig vietnix.vn NS

### Dùng Dig command để kiểm tra resolv record A, MX, NS với custom DNS
#### resolv record A
dig @8.8.8.8 vietnix.vn A

#### resolv record MX
dig @8.8.8.8 vietnix.vn MX

#### resolv record NS
dig @8.8.8.8 vietnix.vn NS

## tar/zip/unzip command
Trong Linux và các hệ điều hành tương tự, các lệnh tar, zip và unzip được sử dụng để nén và giải nén các tệp và thư mục.

### Nén/Giải nén file tar.gz
#### Nén file/thư mục: 
 tar -czf output.tar.gz input_file_or_directory
 
    -c: Tạo một kho lưu trữ mới
    -z: Sử dụng nén gzip
    -f: Chỉ định tên tệp kho lưu trữ
#### Giải nén file tar.gz: 
tar -xzf input.tar.gz

    -x: Giải nén
    -z: Sử dụng nén gzip
    -f: Chỉ định tên tệp kho lưu trữ

### Nén/Giải nén file .zip
#### Nén file/thư mục: 
zip -r output.zip input_file_or_directory

    -r: Nén đệ quy (để nén thư mục)

#### Giải nén file .zip: 
unzip input.zip

## mount/umount command

### Add thêm một ổ cứng sdb ~ 5gb
Giả sử ổ cứng mới đã được gắn vào hệ thống với thiết bị tên là /dev/sdb, 

Tạo phân vùng trên ổ cứng mới:

sudo fdisk /dev/sdb

Tạo hệ thống tệp (filesystem):

Để tạo hệ thống tệp ext4 trên phân vùng mới tạo, sử dụng lệnh sau:

sudo mkfs.ext4 /dev/sdb1

Thay /dev/sdb1 bằng tên phân vùng cụ thể.
### Kiểm tra được có bao nhiêu ổ cứng trên máy chủ
Lệnh lsblk: Hiển thị danh sách các thiết bị lưu trữ và phân vùng của chúng.

lsblk

Lệnh fdisk -l: Liệt kê tất cả các phân vùng và ổ đĩa.

fdisk -l

Lệnh df -h: Hiển thị thông tin về không gian đĩa đã sử dụng và còn trống.

df -h
### Mount ổ cứng vào /mnt/test
 Tạo thư mục mount point
 
mkdir /mnt/test

 Mount ổ cứng vào thư mục /mnt/test
 
mount /dev/sdb1 /mnt/test

### Umount /mnt/test

umount /mnt/test


## Symbolic Links, Hard Links command

### Định nghĩ Sym Link

Symbolic Link (hay còn gọi là symlink hoặc soft link) là một loại file đặc biệt chứa đường dẫn đến một file hoặc thư mục khác. Khi bạn truy cập một symlink, hệ thống sẽ tự động chuyển hướng đến file hoặc thư mục gốc mà nó tham chiếu. Symlink không chứa dữ liệu thực sự của file mà chỉ chứa đường dẫn đến nó.
### Ví dụ về Sym Link
Giả sử bạn có file gốc là /home/user/file.txt và bạn muốn tạo một symlink có tên là /home/user/symlink.txt:

ln -s /home/user/file.txt /home/user/symlink.txt

Bây giờ, khi bạn truy cập symlink.txt, nó sẽ chuyển hướng bạn đến nội dung của file.txt.
### Định nghĩa Hard Link
Hard Link là một tham chiếu trực tiếp đến dữ liệu trên ổ đĩa, được lưu trữ trong cùng một hệ thống file. Khi tạo một hard link, nó sẽ trỏ đến cùng dữ liệu vật lý mà file gốc sử dụng, có nghĩa là cả hai link (file gốc và hard link) sẽ chia sẻ cùng một inode.

### Ví dụ về Hard Link
Giả sử bạn có file gốc là /home/user/file.txt và bạn muốn tạo một hard link có tên là /home/user/hardlink.txt:

ln /home/user/file.txt /home/user/hardlink.txt

Cả file.txt và hardlink.txt đều trỏ đến cùng một dữ liệu. Nếu bạn xóa file.txt, dữ liệu vẫn sẽ có sẵn qua hardlink.txt.
## ls command
Lệnh ls trong hệ điều hành Linux được sử dụng để liệt kê các file và thư mục trong một thư mục

### Liệt kê danh sách file/thư mục
Để liệt kê các file và thư mục trong thư mục hiện tại, bạn chỉ cần sử dụng lệnh ls:

ls
### Liệt kê danh sách file/thư mục và thuộc tính
Để liệt kê file và thư mục cùng với các thuộc tính của chúng (như quyền, số lượng liên kết, chủ sở hữu, nhóm, kích thước, thời gian sửa đổi cuối cùng), bạn sử dụng tùy chọn -l:

ls -l
### Show file ẩn
File ẩn trong Linux thường bắt đầu bằng dấu chấm (.). Để hiển thị cả file ẩn, bạn sử dụng tùy chọn -a:

ls -a

Kết hợp hiển thị file ẩn và thuộc tính

ls -la

ls -al

## ps command
Lệnh ps trong Linux được sử dụng để hiển thị thông tin về các tiến trình đang chạy trên hệ thống. Kết hợp với lệnh kill, bạn có thể dừng các tiến trình cụ thể

### show tiến trình
Lệnh ps đơn giản sẽ hiển thị các tiến trình hiện tại do người dùng đang sử dụng chạy trong cùng một terminal.

Sử dụng tùy chọn -e hoặc -A để liệt kê tất cả các tiến trình trên hệ thống:

ps -e

hoặc

ps -A

Sử dụng tùy chọn -f hoặc -l để hiển thị thông tin chi tiết (full-format listing) về các tiến trình, bao gồm PID (Process ID), TTY, TIME, CMD, v.v.:

ps -ef

hoặc

ps -el

Sử dụng tùy chọn --forest để hiển thị các tiến trình trong dạng cây, giúp bạn thấy các tiến trình cha-con dễ dàng hơn:

ps -ef --forest

### kill tiến trình
Sử dụng lệnh kill với PID của tiến trình bạn muốn dừng:

kill PID

Dừng tiến trình một cách mạnh mẽ (force kill)
Nếu tiến trình không dừng lại khi sử dụng lệnh kill thông thường, bạn có thể sử dụng tín hiệu -9 để ép buộc dừng:

kill -9 PID

Lưu ý rằng việc sử dụng kill -9 có thể không an toàn vì nó không cho tiến trình cơ hội để dọn dẹp và lưu trạng thái trước khi bị dừng.
## top command
Lệnh top trong Linux là một công cụ giám sát hệ thống mạnh mẽ, cung cấp thông tin chi tiết về các tiến trình đang chạy, tài nguyên hệ thống như CPU, bộ nhớ, và nhiều thông số khác. 

### Kiểm tra tài nguyên cpu đang sử dụng của một vài process đang chạy
Khi bạn chạy lệnh top, nó sẽ hiển thị một danh sách các tiến trình đang chạy, cùng với các thông tin chi tiết về tài nguyên mà mỗi tiến trình đang sử dụng. Để xem thông tin về việc sử dụng CPU của các tiến trình, bạn có thể quan sát cột %CPU.

top

### Giải thích về Load average, us, sy, ni, id, wa, hi, si, st, zombie process, sleeping process
#### Load Average
Load Average là một chỉ số cho biết số lượng tiến trình đang chạy hoặc sẵn sàng chạy trong hàng đợi CPU. Nó thường được hiển thị dưới dạng ba số tương ứng với trung bình tải trong 1, 5, và 15 phút qua.

    Giá trị dưới 1 cho thấy CPU không quá tải.
    Giá trị trên 1 có nghĩa là hệ thống có nhiều yêu cầu hơn so với khả năng xử lý của CPU.
    
#### CPU States
Các trạng thái CPU được hiển thị trong top bao gồm:

    us (user): Phần trăm CPU sử dụng cho các tiến trình của người dùng.
    sy (system): Phần trăm CPU sử dụng cho các tiến trình hệ thống (kernel).
    ni (nice): Phần trăm CPU sử dụng cho các tiến trình với mức độ ưu tiên đã được thay đổi.
    id (idle): Phần trăm CPU không làm việc, thể hiện thời gian CPU rảnh rỗi.
    wa (wait): Phần trăm thời gian CPU đang chờ I/O (ví dụ: đọc/ghi ổ đĩa).
    hi (hardware interrupts): Phần trăm thời gian CPU xử lý các ngắt phần cứng.
    si (software interrupts): Phần trăm thời gian CPU xử lý các ngắt phần mềm.
    st (steal time): Phần trăm thời gian CPU bị "ăn cắp" từ một máy ảo khác (trong trường hợp sử dụng ảo hóa).  
    
#### Process States
    Zombie Process: Tiến trình đã kết thúc nhưng vẫn còn tồn tại trong bảng tiến trình bởi vì tiến trình cha chưa đọc trạng thái thoát của nó. Zombie tiến trình không sử dụng tài nguyên hệ thống (ngoại trừ một mục nhỏ trong bảng tiến trình).

    Sleeping Process: Tiến trình đang đợi một sự kiện xảy ra (như I/O hoặc tín hiệu). Nó có thể là:
        Interruptible sleep: Tiến trình có thể bị đánh thức bởi các tín hiệu (được chỉ định bởi chữ S trong cột STAT).
        Uninterruptible sleep: Tiến trình không thể bị đánh thức bởi tín hiệu (được chỉ định bởi chữ D trong cột STAT), thường là khi đang chờ I/O từ đĩa hoặc mạng.    
    
## free command
Lệnh free trong Linux cung cấp thông tin về việc sử dụng bộ nhớ trong hệ thống, bao gồm RAM và swap. Khi bạn chạy lệnh free, bạn sẽ thấy một bảng liệt kê chi tiết về việc sử dụng bộ nhớ, với các cột như used, free, shared, buff/cache, và available

### Giải thích ram used, free, shared, buff/cache, free
### used
- RAM đã sử dụng: Đây là tổng dung lượng RAM đang được sử dụng bởi hệ thống, bao gồm cả bộ nhớ đã được hệ thống và các ứng dụng chiếm dụng.
- Giá trị này bao gồm cả bộ nhớ dành cho các bộ đệm (buffers) và bộ nhớ đệm (cache), mà có thể được giải phóng nếu cần thiết cho các tiến trình khác.
### free
- RAM còn trống: Đây là lượng RAM hoàn toàn chưa được sử dụng và có sẵn để sử dụng ngay lập tức mà không cần giải phóng bất kỳ tài nguyên nào.
### shared
- Bộ nhớ chia sẻ: Đây là lượng bộ nhớ được sử dụng cho các phân vùng bộ nhớ chia sẻ (shared memory segments), thường được sử dụng bởi các tiến trình để trao đổi dữ liệu với nhau. Đây là một phần của bộ nhớ used.
### buff/cache
- Bộ nhớ đệm (buffers): Đây là bộ nhớ tạm thời được sử dụng bởi kernel để lưu trữ dữ liệu trong quá trình di chuyển từ hoặc đến các thiết bị I/O, như ổ đĩa.
- Bộ nhớ đệm (cache): Đây là bộ nhớ được kernel sử dụng để lưu trữ các trang bộ nhớ đã đọc từ đĩa để tăng tốc độ truy cập trong tương lai.
- Bộ nhớ trong buff/cache có thể được giải phóng và sử dụng lại khi hệ thống cần thêm bộ nhớ.
### available
- Bộ nhớ khả dụng: Đây là ước tính lượng bộ nhớ có sẵn cho các ứng dụng mới mà không cần trao đổi bộ nhớ đã tồn tại. Khác với free, available bao gồm cả bộ nhớ hiện đang được sử dụng bởi các bộ đệm và bộ nhớ đệm, mà có thể được giải phóng khi cần.

## df command
Lệnh df trong Linux được sử dụng để hiển thị thông tin về việc sử dụng không gian đĩa của các hệ thống file.

### Xem dung lượng disk
Hiển thị thông tin cơ bản:
df

Hiển thị thông tin với đơn vị dễ đọc hơn:
df -h
### Phân vùng 
Trong Linux, phân vùng / (hay còn gọi là root partition) là phân vùng chính chứa hệ thống file gốc của hệ điều hành. Đây là nơi chứa tất cả các thư mục và file cần thiết cho hệ thống để khởi động và vận hành. Khi một hệ thống Linux khởi động, nó sẽ gắn kết phân vùng / trước tiên, và tất cả các thư mục khác đều là các nhánh con của phân vùng này.

#### Một số thư mục quan trọng trong phân vùng / bao gồm:

    /bin: Chứa các chương trình nhị phân thiết yếu.
    /boot: Chứa các file cần thiết cho quá trình khởi động, bao gồm kernel.
    /dev: Chứa các file thiết bị (device files).
    /etc: Chứa các file cấu hình hệ thống.
    /home: Chứa thư mục home của các người dùng.
    /lib: Chứa các thư viện chia sẻ cần thiết cho các chương trình hệ thống.
    /mnt: Điểm mount tạm thời cho các hệ thống file.
    /opt: Thường chứa các phần mềm tùy chọn (optional software).
    /proc: Hệ thống file giả lập chứa thông tin về các tiến trình.
    /root: Thư mục home của người dùng root.
    /sbin: Chứa các chương trình hệ thống thiết yếu.
    /usr: Chứa các chương trình và thư viện của người dùng.
    /var: Chứa các file dữ liệu thay đổi (như log và dữ liệu của ứng dụng).

Phân vùng / rất quan trọng vì nó chứa toàn bộ cấu trúc thư mục của hệ thống và đảm bảo rằng tất cả các thư mục và file cần thiết đều có thể truy cập được.








