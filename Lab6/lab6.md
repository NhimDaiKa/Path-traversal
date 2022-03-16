# Lab: File path traversal, validation of file extension with null byte bypass

> Phòng thí nghiệm này chứa lỗ hổng path traversal trong việc hiển thị hình ảnh sản phẩm. Ứng dụng xác nhận rằng tên tệp được cung cấp kết thúc bằng phần mở rộng tệp dự kiến. Để giải quyết phòng thí nghiệm, hãy truy xuất nội dung của tệp / etc / passwd.

Chọn 1 bức ảnh may mắn để lấy đường dẫn hiển thị hình ảnh sản phẩm.

Dễ thấy được path dẫn ảnh ở đây là `/image?filename=1.jpg`. Thử với phương pháp của lab trước nhưng không truy cập được. Trang web yêu cầu tệp tải lên phải là phần mở rộng được cho phép.

Nếu ứng dụng yêu cầu tên tệp do người dùng cung cấp phải kết thúc bằng phần mở rộng tệp dự kiến, chẳng hạn như .png, thì có thể sử dụng byte null để kết thúc hiệu quả đường dẫn tệp trước phần mở rộng được yêu cầu.

Payload: `../../../etc/passwd%00.png`