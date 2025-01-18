# Setup Windows Server
## Allow/Block port, ip trên Windows Server
- Sau khi cày Windows Server. Vào Service Manager > Chọn Local Server > Microsoft Defender Firewall : Private: Off

![2025-01-18_10-45](https://github.com/user-attachments/assets/92166586-4c94-448e-a48e-7c0abf450cf0)

- Tiếp theo bật Private Network và Public Network

![2025-01-18_10-51](https://github.com/user-attachments/assets/e78054ef-4f20-4c65-af91-6cd8558d7f9d)

- Vào Windows Defender Firewall > Advanced Security > Inbound Rules > Chọn New Rules

![2025-01-18_10-58](https://github.com/user-attachments/assets/1b0ed802-71f3-4d08-9478-b30ab9b25ee2)

- Chọn Port

![2025-01-18_11-00](https://github.com/user-attachments/assets/1b93b74b-ba3c-41f9-8acb-1610380807e1)

- Chọn giao thức sử dụng và port number

![2025-01-18_11-03](https://github.com/user-attachments/assets/800e5261-caed-41fa-badc-b4f4eb3e8dd2)

- Chọn Allow connection/Block Connection

![2025-01-18_11-08](https://github.com/user-attachments/assets/7f055411-6be5-4042-9096-eb1646cb3db1)

- Sau đó giữ mặc định chọn Next > Next > Nhập Tên Rules > Finish

![2025-01-18_11-10](https://github.com/user-attachments/assets/bc66cb55-9a97-4376-8f10-0b3f09eb3aa6)

## Giới hạn Port/Ip trên Windows Firewall, chỉ cho phép ip chỉ định truy cập

- Vào Windows Defender Firewall > Advanced Security > Inbound Rules > Chọn New Rules > Custom

![2025-01-18_21-56](https://github.com/user-attachments/assets/f1ce4fa3-15e6-4a6e-8742-166e2181dbcf)

- Chọn All Program > Next
  
![2025-01-18_21-59](https://github.com/user-attachments/assets/a4fcd9d9-1265-4451-9e7e-e495dc8f39d7)

- Chọn loại protocal và remote

![2025-01-18_22-04](https://github.com/user-attachments/assets/786f47bb-57cb-44a8-8466-d1a18c445cbf)

- Nhập Địa chỉ IP từ xa mà bạn muốn kết nối cổng của mình. Nhấp vào Nút Add, nhập Địa chỉ IP, rồi nhấp vào Ok và Next.
  
![2025-01-18_22-08](https://github.com/user-attachments/assets/d93a2640-7730-416e-9243-d02b1f83853a)

![2025-01-18_22-13](https://github.com/user-attachments/assets/5389eac9-9a7f-43ca-b5e0-2355e9a24f81)

- Chọn  Allow the connection và nhấp vào Next

- Ở Profile Page > Chọn Domain, Private and Public.

![2025-01-18_22-17](https://github.com/user-attachments/assets/a0c3a94e-a1c9-4fb4-8445-1fbf335802db)

- Nhập tên Rules > Finish

## Cài đặt IIS trên Webserver
- Vào Server Manager > Add Roles and Feature

![2025-01-18_22-28](https://github.com/user-attachments/assets/1b95c534-c7d1-4ddf-ad87-f1873b3a226f)

- Ở Befor you Begin > Next
- Intallation Type > Next
- Server Selection > Next
- Server Roles > Bật Web Server (IIS)
  
![2025-01-18_22-33](https://github.com/user-attachments/assets/f3521352-8dec-4fbf-bc7d-9cb47a2b44de)

![2025-01-18_22-35](https://github.com/user-attachments/assets/d4b19a29-ac1c-4e38-8875-c879f1853606)

- Tiếp tục chọn Next đến Install

![2025-01-18_22-37](https://github.com/user-attachments/assets/75a020a6-c4ad-4be9-b0ed-0a013557577f)


