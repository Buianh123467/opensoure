 Cài đặt Ubuntu + Docker

 sau khi cài xong chạy thử với lệnh 

 ls -l Liệt kê các file trong thư mục
 <img width="1070" height="174" alt="Image" src="https://github.com/user-attachments/assets/393f025b-a72e-45a6-bac3-809b9adc0260" />

Xem ip của máy ubuntu: ip -4 addr

<img width="867" height="188" alt="Image" src="https://github.com/user-attachments/assets/488d366d-dc2b-46a0-8648-0a1c5a80fcbf" />

Cài đặt docker cho Ubuntu

sau khi cài kiểm tra xem docker có hoạt động chưa 

<img width="1096" height="378" alt="Image" src="https://github.com/user-attachments/assets/76bb91b9-d422-49de-a31d-eb0dfb1a7e05" />

Tìm hiểu tập lệnh của docker và docker compose:

 Các tập lệnh thường dùng trong docker:


Tải một image từ Docker Hub: docker pull nginx

Chạy một container mới từ image (chạy ngầm, mở cổng 80): docker run -d -p 80:80 --name web-server nginx

Liệt kê các container đang chạy: docker ps

Liệt kê tất cả container (cả đang chạy và đã dừng): docker ps -a

Dừng một container: docker stop web-server

Xóa một container: docker rm web-server

Xem danh sách các image đang có trên máy: docker images


Tập lệnh docker conpose:


Khởi chạy các dịch vụ được định nghĩa trong file docker-compose.yml (chạy ngầm): docker compose up -d

Dừng và xóa các container trong file compose: docker compose down

Xem log hoạt động của các container: docker compose logs -f

Khởi động lại các dịch vụ: docker compose restart


Cấu hình tường lửa( UFW):


Cho phép kết nối SSH (Cực kỳ quan trọng để không bị mất kết nối): sudo ufw allow 22/tcp

Cho phép cổng 80 (Web): sudo ufw allow 80/tcp

Cho phép cổng 1880 (Node-RED): sudo ufw allow 1880/tcp

Cho phép cổng 9630: sudo ufw allow 9630/tcp

Kích hoạt tường lửa (Chọn 'y' khi được hỏi): sudo ufw enable

Kiểm tra trạng thái các cổng đã mở: sudo ufw status


