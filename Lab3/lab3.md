# Lab: File path traversal, traversal sequences stripped non-recursively

> Phòng thí nghiệm này chứa lỗ hổng path traversal trong việc hiển thị hình ảnh sản phẩm. Ứng dụng tách các trình tự duyệt đường dẫn khỏi tên tệp do người dùng cung cấp trước khi sử dụng nó. Để giải quyết phòng thí nghiệm, hãy truy xuất nội dung của tệp / etc / passwd.

Chọn 1 bức ảnh may mắn để lấy đường dẫn hiển thị hình ảnh sản phẩm.

Dễ thấy được path dẫn ảnh ở đây là `/image?filename=1.jpg`. Thử với phương pháp của lab trước nhưng không truy cập được. Trang web đã loại bỏ các cụm ký tự `../` nhằm chặn việc quay lại thư mục cha trên server. Mình có thể bypass bằng cách sử dụng `....//`, lúc này cụm `../` đã bị loại bỏ và phần còn lại là `../` vẫn đảm bảo mình có thể quay lại thư mục cha

Payload: `....//....//....//etc/passwd`