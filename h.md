 1.Tại sao phải dùng Nginx làm Reverse Proxy mà không trỏ thẳng Tunnel vào Node-RED?
Nginx đứng giữa để điều hướng request
Có thể:
        bảo mật tốt hơn
        xử lý nhiều service
        thêm SSL, cache

Nếu trỏ thẳng:

        khó quản lý
      kém bảo mật
2. Mount file vs Mount thư mục trong Docker
Mount file:

chỉ map 1 file cụ thể
dùng cho config (vd: nginx.conf)

👉Mount thư mục:

map cả folder
dùng cho code / dữ liệu

3.Sửa index.html thì web có đổi ngay không?

 (thường là có)

 Vì:

Docker đang mount trực tiếp file từ máy host
nên sửa là container thấy ngay

4.restart: always / unless-stopped để làm gì?

dùng để tự động restart container

always: luôn restart (kể cả reboot máy)
unless-stopped: restart trừ khi bạn stop thủ công

5.Dùng chung 1 network trong Docker
Lợi ích:
container giao tiếp với nhau bằng tên
không cần IP
dễ quản lý

6.Đưa Cloudflare Token vào .env + .gitignore
Vì sao quan trọng?

Tránh lộ:

        API key
         token

 Nếu lộ → người khác có thể:

      chiếm quyền
       phá hệ thống

7.Tại sao thêm :ro khi mount Nginx config?

:ro = read-only

nghĩa là:

container chỉ đọc,không sửa được

 giúp tránh lỗi,tăng bảo mật
