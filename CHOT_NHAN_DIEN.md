# Quyết định đã chốt – App Script – 11/10/2026

Thông tin nhận diện dùng thống nhất trong dự án:
- Họ và tên: Lê Thanh Tùng.
- SĐT: 0916106016.
- Zalo: 0888158584.
- Không dùng số cũ 0816106016; không dùng Quốc Trung/0919.52.42.79 cho nhận diện dự án này.

Cụm nhận diện mặc định trên QR:
- Bên trái: biểu tượng VNPT nền trong suốt.
- Dưới biểu tượng: VNPT Ninh Kiều.
- Bên phải: Lê Thanh Tùng; Zalo: 0888158584.
- Trên QR dùng tên và Zalo, không dùng số điện thoại ở cụm giữa.
- Ở giữa hai bên: nét dọc mảnh, nhẹ.
- Logo là phần chính; chữ tên và Zalo nhỏ, kín đáo, rõ và chuyên nghiệp.
- Các ô QR thật ở mép lấn nhẹ vào logo/padding, cho cảm giác logo ở phía sau QR. Giữ vùng chữ dễ đọc.
- Không vẽ ô QR giả để trang trí. Chỉ khôi phục các ô tối vốn có trong ma trận QR.
- Vùng nhận diện nhỏ hơn các ảnh concept để ưu tiên khả năng quét.
- QR tĩnh, không có link trung gian, không giới hạn thời gian hay lượt quét của app. Link/file đích vẫn phải tồn tại.

Luồng được giữ:
- Hai phần tách riêng: Tạo mã QR và Thiết kế bảng QR.
- QR có thể tải riêng hoặc chuyển sang thiết kế nền.
- Có tải logo tùy chọn, nhập chữ, ảnh nền riêng, bốn mẫu nền xanh theo phong cách VNPT, chỉnh/kéo thả chữ/logo/QR, hoàn tác/làm lại, lưu/mở JSON.
- Giao diện đồng nhất với trang chủ v2.1; không thay đổi đăng nhập của trang chủ.

Kiểm tra:
- QR thật dùng mức sửa lỗi H, vùng trắng tối thiểu 4 module, ô QR đặt theo lưới pixel nguyên.
- Mẫu phải qua giải mã độc lập ở ảnh gốc và mô phỏng JPEG chất lượng 75% tại 1024/512 px trước khi cho tải.
- Không bảo đảm mọi bản nén của Zalo hoặc mọi thiết bị sẽ quét được. Cần thử trên Zalo thật trước khi in/gửi rộng rãi.
