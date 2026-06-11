Phần gỡ lỗi

khởi chạy

docker compose ps

<img width="1094" height="149" alt="Image" src="https://github.com/user-attachments/assets/fe3f7f94-8c0b-4018-b798-ed17442ba176" />

Thêm healthcheck cho myapi trong file docker-compose.yml
healthcheck:
  test: ["CMD", "curl", "-f", "http://localhost:9630"]
giới hạn resource cho một service: (tránh việc 1 service chiếm quá nhiều ram)
deploy:
  resources:
    limits:
      memory: 512M

<img width="1078" height="620" alt="Image" src="https://github.com/user-attachments/assets/a05a6d9a-c539-4aa5-bcc9-f45814772066" />

sử dụng lệnh: docker compose stats để quan sát lượng ram sử dụng bởi mỗi service

<img width="1323" height="557" alt="Image" src="https://github.com/user-attachments/assets/b0bd63cd-6607-480a-a8c9-222b27f556a2" />




