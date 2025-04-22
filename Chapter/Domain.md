# Domain 
## Domain
Domain là địa chỉ trang web hoạt động trên Internet, nó được thể hiện bằng chữ cái thay thế cho địa chỉ IP.

Địa chỉ IP là địa chỉ mà để các thiết bị giao tiếp với nhau trên mạng.

Đối tưởng sử dụng là các doanh nghiệp, tổ chức, cá nhận hoạc các nhà phát triển Web.

Nếu không có tên miền, sẽ phải sử dụng địa chỉ IP của máy chủ để truy cập trang web.

Domain hoạt động như một địa chỉ định danh trên Internet. Nó được dùng để xác định và truy cập các tài nguyên trên mạng.

Mỗi domain có một phần tên chính và một phần mở rộng.
### Cách thức hoạt động của domain

Đầu tiên cần chọn tên miền phù hợp thông qua nhà đăng ký tên miền được uy quyền

Các máy chủ thực hiện quá tình phân giải tên miền khi người dùng nhập tên miền và ấn Enter, máy tính sẽ không thể hiện rõ địa chỉ IP của
máy chủ mà tên miền đó trỏ đến. Thay vào đó, máy tính sử dụng DNS để tìm kiếm địa chỉ IP tương ứng với tên miền.

Khi địa chỉ IP được xác định, trình duyệt sẽ kết nối đến máy chủ đó. Máy chủ đó sẽ chứa các tài nguyên.

Khi kết nối thành công đến máy chủ, thì tài nguyên liên quan đến tên miền sẽ được tải xuống và hiển thị trên trình duyệt của bạn.
### Những thành phần của domain
Gồm 3 thành phần chính: Subdomain, Domain Name, và Top-Level Domain
![Screenshot from 2025-01-11 09-40-53](https://github.com/user-attachments/assets/50ed6249-922a-4c54-9579-2f539cd14318)

Protocol: tập hợp các quy tắc chuẩn cho phép thiết bị trong cùng một hệ thống để trao đổi thông tin liên lạc, dữ liệu.

Subdomain: là một phần tùy chọn và nằm phía trước tên miền chính. Nó giúp chia nhỏ và tổ chức trang web.

Domain Name: là phần chính của tên miền

Second Level Domain: giúp phân biệt các tên miền, giúp người dùng hiểu rõ hơn về nội dung hoặc lĩnh vực hoạt động của trang web

Top-Level Domain: là phần cuối cùng của tên miền và thường là các phần mở rộng như .com, .net, .org, .edu, .vn... Miền cấp cao giúp xác định loại hình trang web.

### Những tên miền phổ biến nhất hiện nay

![Screenshot from 2025-01-11 09-45-26](https://github.com/user-attachments/assets/df500de0-1c7f-4c7d-a67c-1fc618b81f9f)

### Một số khái niệm liên quan
#### NameServer
NameServer: có chức năng điều phối quá trình hoạt động của tên miền website, chuyển đổi từ tên miền sang địa chỉ IP.
#### Addon Domain
Addon Domain: là một tên miền có thể được sử dụng cùng với tên miền chính để lưu trữ nhiều trang web khác nhau trên cùng một tài khoản web hosting. Nó hoạt động giống tên miền chính. thường được sử dụng bởi các doanh nghiệp hoặc cá nhân sở hữu nhiều trang web có liên quan đến nhau. 
#### Parked Domain
Parked Domain là tên miền được đăng ký nhưng không được sử dụng. Thay vào đó, tên miền được trỏ đến một trang web "parked".

Parked Domain thường được sử dụng bởi các nhà đầu tư tên miền.
#### Alias Domain
Alias Domain là tên miền phụ, là một tên miền có thể được trỏ đến cùng một tài nguyên như một tên miền khác. Alias Domain thường được sử dụng để tạo các tên miền ngắn gọn hơn hoặc dễ nhớ

Nó hoạt động giống một tên miền chính, nhưng không có địa chỉ IP riêng

Thường được sử dụng bởi các doanh nghiệp hoặc cá nhân sở hữu nhiều trang web hoặc tài nguyên.
### Phân loại tên miền
#### Tên miền cấp 1
Tên miền cấp 1 hay còn được gọi là tên miền quốc tế, được sử dụng chung cho nhiều quốc gia khác nhau. Mỗi tên miền cấp 1 sẽ đại diện cho một ngành nghề, một lĩnh vực hoặc một khu vực địa lý. Đặc điểm của loại tên miền này là chỉ có một dấu chấm “.”.

#### Tên miền cấp 2
Tên miền cấp 2 hay tên miền quốc gia, là tên miền cao nhất trực thuộc quốc gia đó.

Mỗi quốc gia sẽ có Tổ chức quản lý mạng riêng để định nghĩa tên miền cấp 2.

Tên miền cấp 2 thường chỉ có 2 ký tự phía sau dấu chấm “.” để dễ dàng phân biệt giữa các quốc gia với nhau.
#### Tên miền cấp 3
Tên miền cấp 3 là kết hợp giữa tên miền cấp 1 và tên miền cấp 2, thường có 2 dấu chấm “.”
### Các trạng thái của domain
#### Trạng thái bình thường 

| **Trạng thái** | **Mô tả** |
|----------------|-----------|
| **OK** | Trạng thái bình thường, không bị khóa. Tên miền hoạt động đầy đủ. |
| **clientTransferProhibited** | Tên miền bị khóa chuyển nhượng theo yêu cầu của chủ sở hữu. Không thể chuyển sang nhà đăng ký khác. |
| **clientUpdateProhibited** | Tên miền bị khóa cập nhật thông tin (như DNS, thông tin chủ sở hữu) theo yêu cầu của chủ sở hữu. |

#### Trang thái cấm hoặc bị hạn chế

| **Trạng thái** | **Mô tả** |
|----------------|-----------|
| **OK** | Trạng thái bình thường, không bị khóa. Tên miền hoạt động đầy đủ. |
| **clientTransferProhibited** | Tên miền bị khóa chuyển nhượng theo yêu cầu của chủ sở hữu. Không thể chuyển sang nhà đăng ký khác. |
| **clientUpdateProhibited** | Tên miền bị khóa cập nhật thông tin (như DNS, thông tin chủ sở hữu) theo yêu cầu của chủ sở hữu. |
| **clientDeleteProhibited** | Tên miền bị khóa xóa theo yêu cầu của chủ sở hữu. |
| **serverHold** | Registry (nhà đăng ký cấp cao) giữ lại tên miền, DNS sẽ không hoạt động. |
| **serverTransferProhibited** | Registry cấm chuyển tên miền sang nơi khác. |
| **serverUpdateProhibited** | Registry cấm cập nhật thông tin tên miền. |
| **serverDeleteProhibited** | Registry không cho phép xóa tên miền. |
| **clientHold** | Bị tạm ngưng do lý do vi phạm hoặc chưa xác minh thông tin chủ sở hữu |

#### Trạng thái tạm thời

| **Trạng thái** | **Mô tả** |
|----------------|-----------|
| **pendingTransfer** | Tên miền đang trong quá trình chuyển nhượng sang nhà đăng ký khác. |
| **pendingDelete** | Tên miền đang chờ xóa khỏi hệ thống. Sau giai đoạn này, tên miền sẽ trở thành tự do để đăng ký lại. |
| **pendingRenew** | Tên miền đang trong quá trình chờ được gia hạn. |

# DNS
## DNS là gì? 
DNS (Domain Name System) là hệ thống phân giải tên miền thành địa chỉ IP tương ứng
## Các loại bản ghi DNS

| **Loại bản ghi** | **Mô tả** |
|------------------|-----------|
| **A (Address)** | Trỏ tên miền đến địa chỉ IPv4 |
| **AAAA** | Trỏ tên miền đến địa chỉ IPv6 |
| **CNAME (Canonical Name)** | Alias – trỏ tên miền này đến tên miền khác |
| **MX (Mail Exchange)** | Cấu hình email, trỏ đến máy chủ mail |
| **NS (Name Server)** | Chỉ định máy chủ DNS chịu trách nhiệm cho domain |
| **TXT** | Bản ghi chứa văn bản, thường dùng để xác minh domain (Google, Microsoft...) hoặc cấu hình SPF/DKIM |
| **SRV** | Xác định dịch vụ cụ thể trên domain (như VoIP, IM) |
| **PTR** | Bản ghi ngược – phân giải địa chỉ IP thành tên miền |
## Nguyên tắc làm việc của DNS

Hệ thống DNS hoạt động theo nguyên tắc **phân giải tên miền thành địa chỉ IP** để giúp máy tính tìm được đúng máy chủ lưu trữ website.

## Quá trình phân giải DNS (DNS Resolution)

1. **Người dùng nhập tên miền** (ví dụ: `www.example.com`) vào trình duyệt.
2. **Trình duyệt kiểm tra bộ nhớ đệm (cache)**:
   - Nếu tên miền đã được phân giải trước đó → sử dụng lại kết quả.
   - Nếu không có → chuyển sang bước tiếp theo.
3. **Truy vấn được gửi đến DNS Resolver** (do ISP hoặc người dùng cấu hình, ví dụ: 8.8.8.8 của Google).
4. **DNS Resolver thực hiện truy vấn theo từng cấp bậc**:
   - **Root DNS Server** → cung cấp thông tin cho máy chủ quản lý miền cấp cao (TLD).
   - **TLD DNS Server** (ví dụ `.com`) → cung cấp thông tin Name Server chính thức của domain.
   - **Authoritative DNS Server** → chứa bản ghi thực tế (A, CNAME, MX...) và trả về địa chỉ IP tương ứng.
5. **DNS Resolver trả kết quả IP về cho trình duyệt**.
6. **Trình duyệt dùng IP này để kết nối đến máy chủ lưu trữ trang web**.


