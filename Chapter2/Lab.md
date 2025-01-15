# Setup Reserver Proxy
## Khái niệm
Reserver Proxy là máy chủ trung gian nằ giữa client và Origin Server.

Khi người dùng truy cập thì yêu cầu chuyển đến Reserver Proxy tahy vì trực tiếp chuyển đến máy chủ.

Nó có các tính năng giống như một firewall

## Công dụng
Load Balencer: Phân phối lưu lượng truy cập, tránh dồn lưu lượng về một máy chủ gây quá tải => Cái thiện hiệu năng và khả năng chịu lỗi

Security: Ẩn địa chỉ IP của máy chủ => Giảm nguy cơ bị tấn công , ngăn chặn các nguy cơ độc hại trước khi đến máy chủ.

Cache: Lưu trữ tài nguyên tĩnh để giảm tải cho máy chủ => Giảm thời gian phản hồi cho người dùng

Xử lý mã hóa/ Giải mã SSL/ TLS => giảm quy trình xử lý của máy chủ.

Nén dữ liệu giứp giảm băng thông và tăng tốc độ tải

Chuyển hướng request theo yêu cầu đến server.
## Các bước cấu hình Ngnix Reserver Proxy trên cPanel
### Các cấu hình yêu cầu
Chạy EasyApache 4

Có quyên truy cập của người dùng root vào máy chủ
### Các bước cấu cài đặt
Bước 1: Đăng nhập vào WHM với tư cách Root user.

Bước 2: Truy cập vào giao diện NGINX Manager tại WHM >> Home >> Software >> NGINX Manager.

Bước 3: Chọn Install để Bắt đầu cày đặt 

![Setup Reserver Proxy](https://github.com/user-attachments/assets/9d000772-726f-45a4-9d82-7b7fcda19870)

Ngoài ra, còn có thể sử dụng giao diện EasyApache 4 hoặc chạy lệnh sau với tư cách là người dùng root:

![Screenshot from 2025-01-15 14-34-51](https://github.com/user-attachments/assets/651b642b-aba5-4c22-bfa0-969a1b4c17fa)


