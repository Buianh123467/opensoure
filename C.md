tạo dự án 

Tạo cấu trúc thư mục cho dự án: mkdir -p ~/myapp/myweb ~/myapp/nginx ~/myapp/nodered

cd vào thư mục vừa tạo: cd ~/myapp
<img width="1094" height="60" alt="Image" src="https://github.com/user-attachments/assets/84690298-ff5b-41fc-bea3-9d394e444af3" />

sử dụng lệnh nano để tạo 1 file index.html và code trực tiếp bằng cmd,

sau khi code xong bấm Ctrl O -> Enter -> Ctrl X để lưu và thoát: nano ~/myapp/myweb/index.html

<img width="1076" height="599" alt="Image" src="https://github.com/user-attachments/assets/7bcefff1-8af9-4672-875c-f35c28692d50" />

tạo file cấu hình để Nginx biết cách trỏ tên miền và Proxy sang Node-RED: nano ~/myapp/nginx/nginx.conf

<img width="1096" height="598" alt="Image" src="https://github.com/user-attachments/assets/095e3e17-5f03-4bf3-ad7e-770ffdbac9a5" />

Tạo file docker-compose.yml ( file cốt lõi để khởi chạy được cả 2 dịch vụ trên):nano ~/myapp/docker-compose.yml

<img width="1082" height="585" alt="Image" src="https://github.com/user-attachments/assets/749540b1-3f0d-4da9-8163-3e3abd6df63a" />

Khởi chạy docer-compose trước để NodeRed sinh ra file cấu hình: docker compose up -d

<img width="1098" height="330" alt="Image" src="https://github.com/user-attachments/assets/d6b7350b-214e-406b-8693-df7b8a1f8f28" />

Kiểm tra dự án

<img width="1310" height="179" alt="Image" src="https://github.com/user-attachments/assets/672c306c-27e9-4828-8430-d65860138595" />

Proxy qua nginx:

<img width="1361" height="618" alt="Image" src="https://github.com/user-attachments/assets/ec1eb3a6-5630-4895-af4f-3ad4b399445e" />

 Kiểm tra location /api dùng proxy_pass trỏ tới 1 (hoặc nhiều) node http_in của nodered:
 
Cấu hình nodered
<img width="1360" height="614" alt="Image" src="https://github.com/user-attachments/assets/d4a0ab74-307b-473c-a14a-d9d75c8521f8" />

Kiểm tra truy cập proxy

<img width="1328" height="710" alt="Image" src="https://github.com/user-attachments/assets/619667dc-9dab-4cd9-a75b-fac4c78ac26e" />

