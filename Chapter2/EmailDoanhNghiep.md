## Email Doanh Nghiệp

### Email hosting

Email Hosting là dịch vụ cho phép doanh nghiệp sử dụng địa chỉ email với tên miền riêng, hoạt động trên một nền tảng Hosting độc lập, mang lại mức độ bảo mật cao hơn các dạng email thông thường.

Email hosting lưu trữ và quản lý email chuyên nghiệp dành cho doanh nghiệp, cho phép tạo và duy trì các địa chỉ email với tên miền riêng
#### Lợi ích của email doanh nghiệp
 - Dễ dàng tùy chỉnh và quản lý số lượng tài khoản email theo nhu cầu

 - Cho phép doanh nghiệp dễ dàng cấu hình và quản lý số lượng tài khoản email

 - Mã hóa dữ liệu, đảm bảo an toàn thông tin người dùng.

 - Cung cấp không gian lưu trữ lớn, giúp doanh nghiệp dễ dàng quản lý và lưu trữ thông tin quan trọng mà không lo hết dung lượng.
### So sánh giữa Domain Hosting, Web Hosting và Email Hosting

![Screenshot from 2025-01-15 16-34-37](https://github.com/user-attachments/assets/f8534a23-77f4-4188-8fb4-795a380902c3)

### Email Relay
Email relay còn gọi là SMTP relay, là dịch vụ cho phép người dùng sử dụng chương trình email client kết nối với máy chủ email của bạn để gửi email

Email Relay sẽ nhận email từ máy chủ thư này, sau đó thông qua một bên thứ ba để chuyển tiếp email sang cho một máy chủ thư khác. 

Email relay là quá trình chuyển tiếp email từ máy chủ email của một tổ chức hoặc người dùng đến máy chủ email của một địa chỉ đích khác.
#### Các thành phần chính trong Email Relay
- Mail Relay Server: Một máy chủ email có thể được cấu hình để chuyển tiếp email đến một máy chủ email khác
- 
- Smart Host: là một máy chủ email đóng vai trò là điểm trung gian cho việc chuyển tiếp email từ máy chủ nguồn đến máy chủ đích.
#### Cách thức hoạt động của Email Relay
- Người gửi gửi email: Người gửi viết và gửi một email thông qua ứng dụng email hoặc máy chủ email của họ.

- Máy chủ email của người gửi kiểm tra tên miền của địa chỉ đích bằng cách thực hiện một truy vấn DNS để xác định máy chủ MX cho miền đó

- Máy chủ email của người gửi tiếp xúc với máy chủ MX được xác định và cố gắng gửi email đến địa chỉ đích.

- Máy chủ email của người gửi xác định máy chủ email relay phù hợp để gửi thông điệp.

- Máy chủ email relay nhận thông điệp từ máy chủ email của người gửi và tiếp tục chuyển tiếp email đến máy chủ email của người nhận thông qua việc tìm máy chủ MX của đích qua các truy vấn DNS.

- Máy chủ email của người nhận nhận được email và lưu trữ nó trong hộp thư của người nhận.

- Người nhận mở ứng dụng email hoặc truy cập vào máy chủ email của họ để đọc email mới nhận được.
### DKIM record và SPF record
DKIM là một tiêu chuẩn xác thực email giúp xác định tính hợp lệ của email và nguồn gốc của nó bằng cách sử dụng chữ ký số được gắn vào email
DKIM giúp xác nhận Email thông qua chữ ký số giúp tránh email giả mạo.

SPF được sử dụng để bảo vệ và xác minh tính xác thực của email. SPF được sử dụng để ngăn chặn email giả mạo và gian lận.
## Các bước cấu hình Email doanh nghiệp
B1: Cần đăng ký Domain và Tạo tài khoản cPanel. Sau đó vào Email Account tạo tài khoản email

![email](https://github.com/user-attachments/assets/dd93f5c2-c74a-466c-8fee-9c9b912608c9)

B2: Cấu hình DNS

Vào tài khoản DNS nơi mà đã đăng ký domain để quản lý tên miền

Sau đó tiến hành trỏ các loại record lần lượt là A, MX, DKIM, SPF

- Record A: để trỏ tài khoản mail về hosting
  
- Record MX: để trỏ doamain về địa chỉ email để có thể nhận mail, đảm bảo bản ghi MX trỏ về cPanel
  
- Record DKIM:  xác thực email bằng chữ ký số.
  
- SPF giúp bảo vệ email của bạn khỏi bị giả mạo.

![2025-01-16_10-16](https://github.com/user-attachments/assets/f37785f9-e4de-418a-950d-f69e34494234)


