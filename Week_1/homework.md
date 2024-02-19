# Bài tập lý thuyết

## Docker, docker-compose là gì?
# Docker
`Docker` là một nền tảng phần mềm cho phép developer tạo, triển khai và quản lý các ứng dụng. Docker đóng gói phần mềm vào các đơn vị tiêu chuẩn hóa được gọi là `container` có mọi thứ mà phần mềm cần để chạy một cách nhất quán trên bất kỳ môi trường nào (ví dụ: thư viện, tệp hệ thống, code, biến môi trường, thời gian chạy). Docker sử dụng CRIU (Checkpoint/Restore in Userspace), namespaces, và cgroups của Linux để cô lập và quản lý các container.
# docker-compose
`Docker Compose` là một tool cho phép định nghĩa và quản lý các ứng dụng bao gồm nhiều container khác nhau. Ta cần sử dụng một tệp YAML (như là `docker-compose.yml`) để cấu hình service của mình, mô tả cả các dịch vụ, mạng, và thiết lập môi trường. Sau đó sử dụng các lệnh của docker-compose để quản lý và triển khai toàn bộ ứng dụng.

## Linux vs Unix vs BSD hay *nix? macOs thuộc loại nào?
# Unix
Unix là hệ điều hành đầu tiên trong nhóm, được phát triển vào những năm 1969 tại Phòng thí nghiệm Bell của AT&T. Nó là một hệ điều hành đa nhiệm và đa người dùng, được thiết kế với mục tiêu về sự đơn giản, tái sử dụng mã, và khả năng di động. Unix có nhiều biến thể và dẫn xuất, bao gồm cả System V và BSD, mỗi biến thể phát triển thêm các tính năng và công cụ riêng.

# BSD
BSD (Berkeley Software Distribution) là một dẫn xuất của Unix được phát triển tại Đại học California, Berkeley. Ban đầu, nó chỉ là một bộ sưu tập các bản vá cho Unix, nhưng sau đó phát triển thành một hệ điều hành độc lập với nhiều tính năng mới và cải tiến. Có nhiều phiên bản BSD hiện nay, bao gồm FreeBSD, NetBSD, và OpenBSD, mỗi phiên bản tập trung vào các mục tiêu cụ thể như bảo mật, khả năng tương thích phần cứng, và ổn định.

# Linux
Linux, khác biệt với Unix và BSD, là một hệ điều hành được phát triển từ đầu bởi Linus Torvalds vào năm 1991. Mặc dù Linux tương tự như Unix về mặt kiến trúc và giao diện lập trình ứng dụng (API), nó được phát triển và phân phối dưới dạng phần mềm tự do và mã nguồn mở theo Giấy phép Công cộng GNU (GPL). Linux không phải là Unix theo nghĩa pháp lý, nhưng nó tuân thủ các tiêu chuẩn POSIX, giúp đảm bảo tương thích với các ứng dụng Unix.

# *nix
*nix là để chỉ các hệ điều hành thuộc Unix-Like, tức là có cách thức hoạt động tương tự với hệ điều hành Unix nhưng không kế thừa trực tiếp từ Unix.

# macOs
macOS, trước đây được biết đến với tên gọi OS X, là hệ điều hành của Apple cho máy Mac. macOS dựa trên Darwin, một hệ điều hành mã nguồn mở có cốt lõi là XNU (X is Not Unix), kết hợp các yếu tố từ BSD và Mach. Do có cơ sở là Darwin, macOS thừa hưởng nhiều đặc điểm của Unix và được chứng nhận là tuân thủ POSIX.

## Alpine với Ubuntu
# Alpine
Alpine Linux là một bản phân phối Linux rất nhỏ gọn, bảo mật, và hiệu quả về tài nguyên. Được xây dụng trên musl libc và BusyBox, Alpine Linux nổi tiếng với kích thước cài đặt rất nhỏ, hiệu suất cao và một hệ thống quản lý gói đặc biệt được gọi là apk (Alpine Package Keeper) và các tập lệnh openRC của riêng mình.
# Ubuntu
Ubuntu là một bản phân phối Linux thông dụng, dựa trên Debian GNU/Linux. Giống như Debian, Ubuntu sử dụng trình quản lý gói DEB, có kích thước lớn hơn so với Alpine.

## VNC
VNC hay còn gọi là "Virtual Network Computing," là một công nghệ cho phép người dùng điều khiển và truy cập một máy tính từ xa thông qua mạng, thường là Internet. VNC cung cấp một giao diện đồ họa (GUI) cho phép người dùng sử dụng chuột, bàn phím và các thiết bị khác để tương tác với máy tính từ xa.
VNC hoạt động dựa trên mô hình client/server. Máy tính cần được cài đặt thành một máy chủ VNC, trong khi máy tính khác muốn điều khiển từ xa cần cài đặt một trình xem VNC, hoặc còn gọi là client. Khi hai thành phần này được kết nối, máy chủ VNC sẽ chuyển gửi hình ảnh màn hình từ xa đến trình xem VNC.