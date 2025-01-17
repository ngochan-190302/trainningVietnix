# Setup Reserver Proxy
## Tổng quan
### Khái niệm
Reserver Proxy là máy chủ trung gian nằ giữa client và Origin Server.

Khi người dùng truy cập thì yêu cầu chuyển đến Reserver Proxy tahy vì trực tiếp chuyển đến máy chủ.

Nó có các tính năng giống như một firewall

### Công dụng
Load Balencer: Phân phối lưu lượng truy cập, tránh dồn lưu lượng về một máy chủ gây quá tải => Cái thiện hiệu năng và khả năng chịu lỗi

Security: Ẩn địa chỉ IP của máy chủ => Giảm nguy cơ bị tấn công , ngăn chặn các nguy cơ độc hại trước khi đến máy chủ.

Cache: Lưu trữ tài nguyên tĩnh để giảm tải cho máy chủ => Giảm thời gian phản hồi cho người dùng

Xử lý mã hóa/ Giải mã SSL/ TLS => giảm quy trình xử lý của máy chủ.

Nén dữ liệu giứp giảm băng thông và tăng tốc độ tải

Chuyển hướng request theo yêu cầu đến server.
## Các bước cấu hình Reserver Proxy 
### 1. Cấu hình Backed Server
#### Backend server 1
- Tạo file index.html với nội dung
```bash
<h1> Web1 <h1>
```
- Tạo ra một con Webserver chạy port 8000
```bash
python -m SimpleHTTPServer
```
- Kiểm tra

![2025-01-17_09-49](https://github.com/user-attachments/assets/6ad5f3aa-cfa5-4225-b386-52d61857ed35)

#### Backend server 2
- Tạo file index.html với nội dung
```bash
<h1> Web2 <h1>
```
- Tạo ra một con Webserver chạy port 8000
```bash
python -m SimpleHTTPServer
```
- Kiểm tra

![2025-01-17_09-53](https://github.com/user-attachments/assets/5824dd4f-d623-4930-8f77-547cd478944f)

### 2. Cấu hình Reserver Proxy Server
- Cày đặt Nginx
```bash
sudo apt install nginx -y
```
- Mở file cấu hình để chỉnh sửa
```bash
sudo nano /etc/nginx/sites-available/default
```
- Thêm cấu hình Reverse Proxy:
```bash
server {
    listen 80;
    server_name ltnhan.site;
    root/var/www/web2;
    index index.php index.html;
    location / {
        proxy_pass http://192.168.181.133:8000; 
    }
}
```
- Khởi động lại Nginx:
```bash
sudo systemctl restart nginx
```

=> Lúc này, những request vào nghan.name.vn (là địa chỉ của Reverse Proxy Server) sẽ được chuyển đến 192.168.181.133 (Backend server 1)

![2025-01-17_10-28](https://github.com/user-attachments/assets/771d06ff-b53f-46d4-9d10-4595cf68d146)

- Cài đặt SSL sử dụng Let's Encrypt
Cài Certbot
```bash
sudo apt install certbot python3-certbot-nginx -y
```
Cấp chứng chỉ SSL
```bash
sudo certbot --nginx -d example.com
```
### Kiểm tra hoạt động
Log Nginx:
```bash
sudo tail -f /var/log/nginx/access.log
sudo tail -f /var/log/nginx/error.log
```
