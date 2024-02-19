Trong bài thực hành này, em sẽ tạo một docker image sử dụng docker-compose, cài đặt VNC server và DE (Desktop Environment) trong đó.
## Bước 1 : Tạo tệp Dockerfile
Sử dụng lệnh `touch Dockerfile` để tạo một tệp Dockerfile mới
Thêm nội dung vào `Dockerfile` như sau:

Ở trong Dockerfile, em đã có câu lệnh :
```
RUN apt-get update && \
    apt-get install -y \
    tightvncserver \
    xfce4
```
Câu lệnh này được sử dụng để cài đặt TightVNC Server và Desktop Environment (DE) Xfce4 trong một Docker image
## Bước 2 : Tạo docker-compose.yml
Tạo một file docker-compose.yml trong thư mục chứa Dockerfile với nội dung sau:

## Bước 3 : Build và Chạy Container
Mở Command Prompt hoặc PowerShell và di chuyển đến thư mục chứa Dockerfile và docker-compose.yml.

Thực hiện lệnh sau để build và chạy container:
```
docker build -t test_vnc
docker run -p 5901:5901 test_vnc
```

## Bước 4
Sử dụng một trình VNC Viewer trên máy tính cá nhân và kết nối đến localhost:5901.
Nhập mật khẩu là "nam2003" (mật khẩu đã đặt trong Dockerfile).
Ta sẽ thấy môi trường desktop XFCE trên trình VNC Viewer.