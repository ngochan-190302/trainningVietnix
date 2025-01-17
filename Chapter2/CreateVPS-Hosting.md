# Cài đặt cấu hình Hosting/VPS
## Cài đặt cấu hình VPS
### Chuẩn bị 
- Chọn nhà cung cấp VPS, và chọn cấu hình phù hợp (RAM, CPU, ổ cứng SSD, băng thông...).
  
- Chọn hệ điều hành
  
- Nhận thông tin đăng nhập từ nhà cung cấp gồm IP, Tài khoản quản trị (thường là root) và mật khẩu mặc định hoặc SSH key.
### Kết nối VPS
- Vào terminal để ssh đến VPS
```bash
  ssh root@<IP-của-VPS>
```
### Cập nhật hệ thống
```bash
apt update && apt upgrade -y
```
### Tải và cài đặt cPanel/WHM
```bash
cd /home && curl -o latest -L https://securedownloads.cpanel.net/latest && sh latest
```
### Cài đặt môi trường
- Apache

```bash
apt install apache2 -y     
yum install httpd -y
```
Khởi động service
```bash
systemctl start apache2    
systemctl start httpd
```
- Ngnix
```bash
apt install nginx -y       
yum install nginx -y
```
Khởi động service
```bash
systemctl start nginx
```
### Cài đặt database
- MySQL
```bash
apt install mysql-server -y       
yum install mysql-server -y
```
Cài đặt bảo mật
```bash
mysql_secure_installation
```
### Truy cập vào WHM
```bash
https://[IP-VPS]:2087
```
=> Chuyển vào giao diện đăng nhập của WHM

Username: root

Password: Mật khẩu VPS
- Giao diện WHM của VPS
![Screenshot from 2025-01-16 14-52-50](https://github.com/user-attachments/assets/6222501d-eb22-4428-9316-bc0086a9bfcc)



