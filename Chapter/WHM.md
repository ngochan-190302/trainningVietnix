# WHM

## Đổi Primary Domain

1. Modify an Account → Tìm kiếm User → Modify
2. Tại giao diện Modify → đổi Primary Domain → bấm Save

Có 2 trường hợp xảy ra:
- Save thành công
- WHM báo đã có domain này tồn tại trên hệ thống → Check domain này khách hàng có add trước đó là add-on domain hay không, nếu đã add thì báo khách chủ động remove ra.

## Migrate và Transfer

1. Từ server cần migrate đến, vào Transfer Tool → Điền IP của server cũ vào ô Remote Server Address.
2. Chọn Authentication Method là SSH Public Key và chọn key "transfer"
3. Scan Remote Server và tìm user cần transfer, thực hiện copy.

Sau khi transfer hosting ở bên cũ sẽ tự suspend, nhưng tech cần kiểm tra lại một lần nữa để đảm bảo.

## Terminal

### a. Reload Hosting

```bash
cagefs -m <user>
```

### b. Check domlogs
File log của domain nằm tại:
```bash
Domain không có SSL: /var/log/apache2/domlogs/<domain>
Domain có SSL: /var/log/apache2/domlogs/<domain>-ssl_log
```
### c. Check process đang chạy của một user
```bash
ps aux | grep <user>
```

## Kiểm tra hosting đang kết nối mail relay server bằng port nào

Ctrl + F để tìm từ khóa POSTMAILCOUNT

## Tìm một add-on domain đang thuộc user nào

### Dùng terminal
```bash
cat /etc/userdatadomains | grep "conheo.com"
abc.conheo.com:
```

### Dùng giao diện
```
khanhtest==root==sub==khanhtest.com==/home/khanhtest/abc.conheo.com==103.200.23.68:80==103.200.23.68:443====0==
conheo.com.khanhtest.com:
khanhtest==root==sub==khanhtest.com==/home/khanhtest/conheo.com==103.200.23.68:80==103.200.23.68:443====0==
conheo.com:
khanhtest==root==addon==conheo.com.khanhtest.com==/home/khanhtest/conheo.com==103.200.23.68:80==103.200.23.68:443====0==
```

## PHP X-Ray

php x-ray dùng để trace cụ thể thời gian thực thi các function php, giúp phát hiện các func nào gây chậm website khách hàng

Chọn vào đây để xem kết quả:

1. Vào plugin Cloudlinux Manager → X-ray → Start Tracing
2. URL: điền URL cần tracing, url này là trang chủ hoặc url khách báo vào bị chậm
3. Client's IP: Điền IP máy của tech vào, hoặc để * thì mọi ip request đến url này đều được trace
4. Record for: Có thể chọn Time Period để trace trong 1 khoảng thời gian hoặc Request để trace dựa theo số lần request.
5. Sau khi thiết lập các thông số xong, tech tiến hành request vào đường link trên 1 vài lần để x-ray phân tích

