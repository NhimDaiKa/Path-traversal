# Lab: File path traversal, traversal sequences stripped with superfluous URL-decode

> Phòng thí nghiệm này chứa lỗ hổng path traversal trong việc hiển thị hình ảnh sản phẩm. Ứng dụng chặn đầu vào chứa trình tự duyệt đường dẫn. Sau đó, nó thực hiện giải mã URL của đầu vào trước khi sử dụng. Để giải quyết phòng thí nghiệm, hãy truy xuất nội dung của tệp / etc / passwd.

Chọn 1 bức ảnh may mắn để lấy đường dẫn hiển thị hình ảnh sản phẩm.

Dễ thấy được path dẫn ảnh ở đây là `/image?filename=1.jpg`. Thử với phương pháp của lab trước nhưng không truy cập được. Trang web thực hiện giải mã URL đầu vào trước khi thực hiện nó vì vậy mình cần mã hóa đầu vào để trang web có thể giải mã.

Payload: `..%252f..%252f..%252fetc/passwd`

