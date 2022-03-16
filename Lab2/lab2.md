# Lab: File path traversal, traversal sequences blocked with absolute path bypass

> Phòng thí nghiệm này chứa lỗ hổng path traversal trong việc hiển thị hình ảnh sản phẩm. Tên tệp được cung cấp có liên quan đến thư mục làm việc mặc định. Để giải quyết phòng thí nghiệm, hãy truy xuất nội dung của tệp / etc / passwd.

Chọn 1 bức ảnh may mắn để lấy đường dẫn hiển thị hình ảnh sản phẩm.

Dễ thấy được path dẫn ảnh ở đây là `/image?filename=1.jpg`. Thử với phương pháp của lab trước nhưng không truy cập được. Tệp có liên quan đến thư mục mặc định, tức là không cần sử dụng `../../` để quay về mà nó sẽ xuất phát từ chính thư mục cha đó. 

`https://ac031f5a1eabcd7fc0c0632c00a500a3.web-security-academy.net/image?filename=/etc/passwd`
