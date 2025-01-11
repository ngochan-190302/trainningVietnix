# HOSTING
 
## Hosting 
Hosting cung cấp không gian lưu trữ dữ liệu, nó giúp đăng data, Website và app lên Internet giúp chúng hoạt động 24/7. Chia server thành nhiều không gian lưu trữ dữ liệu. 
## Web 
Web chứa các dữ liệu, hình ảnh, video nằm trên cùng một domain, được lưu trữ trên Webserver.

Web tồn tại dưới dang tập tin html hoặc xhtml có thể truy cập bằng giao thức http hoặc https. Người dùng có thể truy cập thông qua Edge Microsoft, Google Chrome, ... 

Để Web hoạt động được thì cần có Source Code Website, Web hosting và Domain. 
### Một số port thông dụng
HTTP: 80

DNS: 53

HTTPS:443

SMTP: 25

POP3: 110

IMAP: 143

## Các thông số cần thiết của Web hosting 
CPU là khả năng xử lý của hosting, CPU càng cao thì càng mạnh.

Core: xử lý tất cả các tác vụ của hệ thống. các core có  thể chạy các chương trình khác nhau cùng lúc. 

Threads CPU là khả năng CPU có thể thực hiện bao nhiêu tác vụ đồng thời.

Xung nhịp để so sánh hiệu suất của CPU.

RAM lưu trữ dữ liệu và các chương trình đang được sử dụng bởi máy chủ. 

Domain là tên miền của website. Tên miền là địa chỉ của website trên Internet, giúp người dùng có thể dễ dàng tìm kiếm và truy cập website. 

Băng thông là thông số dung lượng tối đa mà lượt truy cập người dùng có thể vào website. 

Data transfer là quá trình truyền tải dữ liệu từ máy chủ đến với các thiết bị khác và truyền đi dưới dạng bit hay byte. 

MySQL quản lý dữ liệu thông qua các cơ sở dữ liệu và mỗi cơ sở dữ liệu có nhiều bảng quan hệ chứa dữ liệu. 

FTP account: cho phép bạn truy cập vào máy chủ Hosting của mình thông qua giao thức FTP. 

Entry processes: là số lượng tác vụ đang xử lý tại một thời điểm trên tổng số các tác vụ mà Hosting có thể xử lý cùng lúc. 

LiteSpeed Webserver: là một dịch vụ web server chạy trên nền tảng Linux và có thể được sử dụng để lưu trữ các trang web và ứng dụng web, và nó có hiệu suất hoạt động cao. 

CloudLinux cung cấp hệ điều hành có các tính năng cho phép admin hệ thống kiểm soát chi tiết việc sử dụng tài nguyên của server. 

Imunify360 bảo vệ chống lại bất kỳ loại tấn công độc hại hoặc hành vi bất thường. 

Jetbackup là một giải pháp sao lưu và khôi phục toàn diện cho máy chủ web Linux. 

## DNS

DNS là hệ thống phân giải tên miền. Phân giải Domain thành IP. 

DNS tiếp nhận yêu cầu tên miền hoặc bất kỳ mạng nào sau đó phản hồi bằng cách cho họ biết nơi tìm chúng. 

### Các thành phần của domain:

![Domain_components](https://github.com/user-attachments/assets/ec503bdc-08a7-4676-87bd-da40231ad148)
 
Protocol: là giao thức để các máy trao đổi thông tin liên lạc, dữ liệu qua các kênh truyền thông. 

Sub-domain: cho phép quản lý các phần khác nhau của trang web dưới cùng một tên domain chính. Mỗi subdomain có thể trỏ đến một trang web hoặc phần cụ thể của trang. 

Second-Level Domain: là phần mà người dùng xác định trang Web.

Top Level Domain (TLD): phần cuối của tên miền, thường được quốc gia quản lý. 

### Cách DNS xử lý request:  

Nếu đó là domain đã từng được tìm kiếm ở máy chủ DNS trước đó thì sẽ lấy IP từ trong bộ nhớ ra để trả về kết quả.

Nếu máy chủ DNS không có IP nó sẽ hỏi DNS gốc. DNS gốc sẽ trả về IP của máy chủ cấp cao nhất cho website. 

Cuối cùng máy chủ DNS cấp cao nhất sẽ trả về IP theo  từng cấp ngược lại. 
### Các loại DNS Server
Root Name Server là một dịch vụ phân giải tên miền gốc. Nó sẽ quản lý tất cả các Top-level Domain.

TLD Nămserver: Tra cứu tên miền và hướng đến máy chủ có thẩm quyền miền đó.

Authoriatative nameserver: Nơi tìm địa chỉ IP muốn truy cập đến.

Web server: đích đến

=>Truy xuất theo thứ tự: Root nameserver > TLD nameserver > Authoriatative nameserver > Web server.

### Các loại bản ghi DNS thường dùng

A Record: Dùng để trỏ tên miền website tới một địa chỉ IP cụ thể, nó ánh xạ tên miền với địa chỉ ipv4.

CNAME: hướng dẫn chuyển sang tên khác (ví dụ tab ẩn danh).

NS: dùng để chỉ định root nameserver chịu trách nhiệm quan lý tên miền hoặc một miền con.

MX: xác định một máy chủ nhận mail cho một tên miền
### Các loại truy vấn trong DNS
Recursive query: DNS client yêu cầu máy chủ DNS => sẽ trả về client 1 record hoặc thông báo lỗi nếu không tìm thấy record yêu cầu.
Iterative query: DNS client sẽ cho phép máy chủ DNS trả về câu trả lời tốt nhất => Nếu không truy ra được kết quả trùng khớp sẽ trả về một giới thiệu đến máy chủ có thẩm quyền thấp hơn, sau đó client sé tiếp tục truy vấn đến địa chỉ đã giới thiệu.
Non-recursive query: Xảy ra khi DNS resolver client truy vấn máy chủ DNS một record mà server có quyền truy cập hoặc bản ghi tồn tại bên trong bộ đệm của server.





