# Lab: File path traversal, traversal sequences stripped with superfluous URL-decode

> Phòng thí nghiệm này chứa lỗ hổng path traversal trong việc hiển thị hình ảnh sản phẩm. Ứng dụng truyền đường dẫn tệp đầy đủ thông qua tham số yêu cầu và xác nhận rằng đường dẫn được cung cấp bắt đầu với thư mục mong đợi. Để giải quyết phòng thí nghiệm, hãy truy xuất nội dung của tệp / etc / passwd.

Chọn 1 bức ảnh may mắn để lấy đường dẫn hiển thị hình ảnh sản phẩm.

Dễ thấy được path dẫn ảnh ở đây là `/image?filename=1.jpg`. Thử với phương pháp của lab trước nhưng không truy cập được. Trang web yêu cầu đường dẫn tệp đầy đủ thông và phải bắt đầu từ thư mục cha `var/www/images`.

Payload: `/var/www/images/../../../etc/passwd`