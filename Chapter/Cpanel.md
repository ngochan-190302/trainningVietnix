# cPanel

## I. cPanel Interface

### Search bar
cPanel có rất nhiều tính năng, để có thể tìm kiếm đến một tính năng nhanh nhất.

### General Information
Chứa các thông tin cơ bản của gói Hosting và server cPanel.

### Statistics
Thống kê Ram, CPU, Processes, AddonDomain, Email account, Bandwidth đang sử dụng.

### Features
Toàn bộ tính năng của cPanel mà admin cho phép người dùng sử dụng.

## II. Chi tiết từng tính năng

### 1. Email

#### Email Accounts:
Chức năng chính: Tạo email, xóa email, kiểm tra email, quản lý email, cấu hình email cho mail client.

#### Forwarders:
Dùng để forward Email đến 1 email khác.
#### Email Routing
Luôn luôn là Local Mail Exchanger. Chỉnh sang bất kì giá trị nào khác đều sẽ không gửi mail được.

#### Autoresponder
Cấu hình trả lời Email tự động.

#### Default Address:
Nơi cấu hình Catch-all Email. 

Thay vì khi nhận Hosting nhận được một email đến 1 địa chỉ không tồn tại trên hosting thì nó sẽ trả về cho người gửi thông báo "No Such User Here", thì khi cấu hình Default Address Hosting sẽ gửi các email đó đến email default này.

#### Mailling Lists
Tạo một group tên "tech@vietnix.vn". Sau đó add nhiều email vào đây như tech1@vietnix.vn, tech2@vietnix.vn. 
Chức năng của Mailling List là khi có một email gửi tới tech@vietnix.vn thì sẽ được gửi đồng thời đến tất cả email trong group đó.

#### Track Delivery
Theo dõi trạng thái của email gửi ra.

#### Global Email Filters
Filter email với toàn bộ email account trên Hosting

#### Email Filters
Filter email với từng email account trên Hosting

#### Email Deliverablity
Kiểm tra, lấy cấu hình DKIM, SPF, PTR đối với domain email trên Hosting

#### Address Importer
Import danh sách email account lên Hosting. Có thể tạo nhanh 1 list email trên hosting bằng cách tạo 1 file .csv và Import vào cPanel:


#### Spam Filters
Cho phép cấu hình cài đặt lọc thư rác (được cung cấp bởi Apache SpamAssassin™) cho tài khoản email. Bộ lọc thư rác xác định và sắp xếp hoặc xóa email không mong muốn. Cấu hình cài đặt danh Whitelist, blacklist.
→ email hosting không sử dụng spam filters này.

#### BoxTrapper
- Xác thực người gửi: Khi ai đó gửi email đến địa chỉ email của bạn, BoxTrapper yêu cầu họ xác minh rằng họ là người thật bằng cách thực hiện một thao tác xác minh.
- Blacklist & Whitelist: Người dùng có thể xác định danh sách whitelist và blacklist cho phép hoặc chặn các người gửi cụ thể.
- Xử lý thư rác: BoxTrapper kiểm tra email đến và tự động loại bỏ thư rác hoặc chuyển nó vào thư mục rác tạm thời để bạn kiểm tra sau.
- Quản lý danh sách liên hệ: BoxTrapper có khả năng tự động cập nhật danh sách liên hệ dựa trên những người gửi đã được xác minh.
→ BoxTrapper không có trên email hosting

#### Email Disk Usage
Thống kê disk của từng email.

#### ASSP Antispam
##### Spam Scoring
Điều chỉnh giá trị spam score, từ lowest → highest. Hoặc bật tắt tính năng này cho từng domain email.

##### Delaying filter
Khi nhận được 1 email thì email hosting sẽ lưu lại 3 thông tin là email address, domain, ip. Sau đó email hosting sẽ trả lại 1 thông báo cho người gửi mail với mã lỗi 451 error (spf soft failure). Khi sever của người gửi nhận được mã này thì nó sẽ retry lại email ban đầu 1 lần nữa. Lúc này email này sẽ bị whitelist. Việt làm này tương tự cơ chế Syn Proxy. Mặc định tính năng này bị tắt trên mail hosting.

##### No local addresses filter
Chỉ cho phép nhận các email mà người nhận có tồn tại trên hosting (email account có tạo). Khi bật tính năng này thì tính năng catch all email của cpanel sẽ không sử dụng được.

##### Virus Protection
Quét email và filter các email có virus.
### 2. File

#### File Manager
Upload file, xóa, sửa file, nén, giải nén. Ngoài ra để hiển thị file ẩn (.htaccess, .env...).

#### Directory Privacy
Cài đặt user/pass cho các thư mục trên cPanel → Tương tự htpasswd

#### Disk Usage
Thống kê disk đang sử dụng

#### Web Disk
Quản lý dữ liệu trên web, tương tự như google drive, onedrive. Web disk hỗ trợ giao thức webdav để truyền tải.

#### FTP Accounts
Tạo tài khoản ftp account, hỗ trợ phân quyền tài khoản cho thư mục.

#### Backup & Backup Wizard
Backup của cPanel → Không sử dụng

#### Git Version Control
Làm việc với github, tự động pull code khi có update code mới trên repo

#### JetBackup 5
Ba lựa chọn quan trọng:
- Sao lưu toàn bộ: Đây là các bản backup full, khi restore lại sẽ restore toàn bộ hosting, bao gồm database, source, ssl,...
- Thư mục Home: Đây là backup file, có thể lựa chọn riêng từng file để restore
- Cơ sở dữ liệu: Restore database

### 3. Quản lý cơ sở dữ liệu

#### phpMyAdmin
Đăng nhập phpMyAdmin, tài khoản login là tài khoản MySQL

#### MySQL Databases
- Tạo database
- Tạo User
- Add user vào database
- Grant quyền user

#### MySQL Database Wizard
Hỗ trợ tạo Database step-by-step. Giúp người tạo không bị quên các bước như tạo user, add user vào database, grant quyền.

#### Remote MySQL
Bật remote MySQL đối với database.

### 4. Công cụ WordPress

#### WP Toolkit
- Cài wordpress
- Cài themes
- Cài plugin

#### Site Publisher
Tạo nhanh 1 website bằng template có sẵn của cPanel

### 5. Domain

#### Domain
Thêm, xóa domain

#### Redirect
Redirect domain

#### Zone Editor
Sau khi trỏ NS về Hosting thì có thể điều chỉnh các record ở đây. NS của hosting có dạng, ví dụ host212.vietnix.vn:
ns1.host212.vietnix.vn
ns2.host212.vietnix.vn


#### Dynamic DNS
Sau khi tạo cPanel sẽ cấp cho mình 1 Url. Khi muốn cập nhật NS cho subdomain này thì chỉ cần curl đến URL này.

#### IP Manager (chỉ có trên Hosting SEO)
Dùng để đổi IP cho các domain.

### 6. Bảo mật

#### SSH Access
SSH lên hosting, có thể cho phép add ssh key

#### IP Blocker
Block ip không cho truy cập vào website của bạn

#### SSL/TLS
Quản lý SSL Server
- Private Keys (KEY): Tạo Private key
- Certificate Signing Requests (CSR): Tạo CSR
- Certificates (CRT): Thêm, xóa, sửa SSL của Domain
- Install and Manage SSL for your Site (HTTPS): Quản lý SSL của Domain

#### Imunify360
Quét virus, quá trình quét virus là tự động

### 7. Software

#### MultiPHP Manager (hỗ trợ bởi cPanel)
Có thể tùy chọn các phiên bản PHP khác nhau cho từng website.

#### MultiPHP INI Editor (hỗ trợ bởi cPanel)
Bật tắt các biến môi trường php ở đây.

#### Softaculous Apps Installer
Cài đặt app bằng 1 click. Ví dụ: Wordpress, Laravel, Moodle, NextCloud,...

#### Setup Node.js APP
Cài đặt nodeJS App

#### Select PHP Version (hỗ trợ bởi cloudlinux)
Nếu khách có dùng LSCache plugin thì mình có thể hỗ trợ khách flush cache từ giao diện cPanel.

### 8. Advanced

#### Terminal
Được dùng để chạy các lệnh terminal.

#### Cron Job
Các nhiệm vụ lặp đi lặp lại được tự động hóa vào thời gian đã lên lịch. Ví dụ: tạo hóa đơn vào 12:00 hàng ngày.

#### Track DNS
Truy tìm tuyến đường từ PC đến máy chủ nhằm kiểm tra cài đặt DNS.

#### Error Pages
Giúp định cấu hình cách của các trang lỗi xuất hiện cho khách khi truy cập.

#### Apache Handlers
Đây là các lựa chọn xử lý của Apache.

#### MIME Types
Dùng để hướng dẫn để xử lý với các phần mở rộng tệp khác nhau, chẳng hạn như: .html, .htm.

