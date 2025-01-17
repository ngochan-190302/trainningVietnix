# Cài đặt cấu hình Hosting/VPS
## Cài đặt hosting 
### Chuẩn bị
- Chọn nhà cung cấp domain, mua và đăng ký tên miền. Sau đó đăng nhập vào tài khoản
  
B1: Đăng nhập vào tài khoản tên miền của bạn với nhà cung cấp tên miền

B2: Chọn tên miền muốn cấu hình, vào Maanage > DNS Management 

![2025-01-17_14-00](https://github.com/user-attachments/assets/565db961-8d0b-482c-9c29-c49744a3b680)

B3: Thêm Rerord A: Chọn Add Record > Nhập Domain > chọn Record A > Conten là địa chỉ nơi muốn trỏ Domain về > Add.

![2025-01-17_14-21](https://github.com/user-attachments/assets/589da20f-63a8-426e-bc5e-cdae67f45d1a)

B4: Thêm 2 Record NS: 

- NS1: Chọn Add Record > Nhập Domain > Chọn Record NS > Content trỏ về NS1 của nơi muốn trỏ về > Add
  
![2025-01-17_14-25](https://github.com/user-attachments/assets/1c60b1ee-cf46-4d6b-89a9-fa4e862f705a)

- NS2: Chọn Add Record > Nhập Domain > Chọn Record NS > Content trỏ về NS2 của nơi muốn trỏ về > Add

![2025-01-17_14-34](https://github.com/user-attachments/assets/96c2fc7c-b9aa-4295-87d1-75eda9df13e8)

- Kết quả:
  
![2025-01-17_14-40](https://github.com/user-attachments/assets/acd7e23c-5a79-46a5-bb5d-0b2fdee10817)

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




