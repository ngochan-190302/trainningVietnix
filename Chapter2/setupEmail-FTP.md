# Setup Email Account và FTP Account thủ công
## Setup Email Account
### Sử dụng Postfix 
#### Cài đặt Postfix 
- Cập nhật bộ nhớ đệm
```bash
$ sudo apt update
```
- Cài postfix
  
Cần truyền biên môi trường vào DEBIAN_PRIORITY
```bash
$ sudo DEBIAN_PRIORITY=low apt install postfix
```
Tiếp tục điền các thông số theo yêu cầu
```bash
General type of mail configuration?: Internet Site
System mail name: example.com 
Root and postmaster mail recipient: Tên người dùng tài khoản Linux 
Other destinations to accept mail for: Thêm vào các miền
Force synchronous updates on mail queue?: No
Local networks: 127.0.0.0/8 [::ffff:127.0.0.0]/104 [::1]/128
Mailbox size limit: 0
Local address extension character: +
Internet protocols to use: All
```
Khởi động lại tiến trình Postfix để đảm bảo rằng tất cả các thay đổi trên đều đã được áp dụng:
```bash
sudo systemctl restart postfix
```
#### Cài đặt Client và khởi tạo cấu trúc Maildir
- Đặt nó trong tệp /etc/bash.bashrc và thêm biến đó vào một tệp trong /etc/profile.d để bảo đảm biến này được thiết lập mặc định cho tất cả user.
```bash
  echo 'export MAIL=~/Maildir' | sudo tee -a /etc/bash.bashrc | sudo tee -a /etc/profile.d/mail.sh
```
- Đọc biến vào phiên hiện tại
```bash
 source /etc/profile.d/mail.sh
```
- Cài đặt trình email client s-nail với APT:
```bash
  sudo apt install s-nail
```
- Trước khi chạy client, cần thay đổi một số thiết lập. Mở tệp /etc/s-nail.rc trong trình soạn thảo văn bản:
```bash
$ sudo nano /etc/s-nail.rc
```
- Thêm đoạn sau ở cuối tệp
```bash
. . .
set emptystart
set folder=Maildir
set record=+sent
```
-Gửi email bằng cách nối một chuỗi vào lệnh s-nail. Điều chỉnh lại câu lệnh để đánh dấu user Linux của bạn là người nhận:
```bash
$ echo 'init' | s-nail -s 'init' -Snorecord sammy
```
- Kiểm tra để đảm bảo rằng thư mục đã được tạo thành công
```bash
$ ls -R ~/Maildir
```
-Đầu ra tin nhắn sẽ như này
```bash
Output
/home/sammy/Maildir/:
cur new tmp

/home/sammy/Maildir/cur:

/home/sammy/Maildir/new:
1463177269.Vfd01I40e4dM691221.mail.example.com

/home/sammy/Maildir/tmp:
```
