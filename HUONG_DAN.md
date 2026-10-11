# QR Studio GitHub v2.1

## Cập nhật từ v2.0
Nhận diện đã chốt được đặt làm mặc định: biểu tượng VNPT trong suốt bên trái, dòng VNPT Ninh Kiều phía dưới; nét dọc ngăn với Lê Thanh Tùng / Zalo: 0888158584 bên phải. Các ô QR thật lấn nhẹ mép logo để tạo cảm giác logo ở lớp sau. Mặc định QR ô vuông, xanh đậm, PNG 2048 × 2048.
Thông tin đầy đủ và quyết định thiết kế được ghi trong CHOT_NHAN_DIEN.md.

## Đưa lên GitHub
1. Giải nén và upload **nội dung bên trong** QR_Studio_GitHub_v2_1 vào gốc repository QR-Generator hiện tại, ghi đè các file app. Giữ đủ thư mục assets và vendor.
2. Nếu config.js hiện tại đã có link trang chủ, giữ giá trị đó hoặc điền lại vào config.js mới:
   window.QR_CONFIG = { homeUrl: 'https://LINK-TRANG-CHU-CUA-ANH' };
3. Settings → Pages → Deploy from a branch → main → /(root) → Save nếu chưa bật Pages.
4. Link dự kiến với tài khoản quoctrungkg: https://quoctrungkg.github.io/QR-Generator/ . ZIP chưa tự được triển khai lên GitHub.
5. Link app con đã dán ở trang chủ giữ nguyên. Chọn Nhúng trong trang chủ hoặc Mở tab mới theo nhu cầu.

## Tạo QR và gửi qua Zalo
- Chọn link / link ảnh-video-PDF / văn bản; nhập nội dung.
- Nhận diện VNPT Ninh Kiều bật mặc định. Có thể tắt để tạo QR thường; có thể chọn ảnh logo riêng để thay biểu tượng.
- Bấm Tạo mã QR. Chờ kiểm tra giải mã trước khi tải. App không tự dùng AI để vẽ ma trận QR.
- Tải PNG (mặc định 2048 px). Chia sẻ ảnh gốc qua Zalo; nếu chất lượng bị giảm, gửi dưới dạng File để giữ nguyên PNG. Không chụp màn hình, không cắt sát viền trắng.
- Bộ kiểm tra mô phỏng thu nhỏ và nén JPEG tại 1024/512 px trước khi bật tải; mã quá dày/kém đọc sẽ bị từ chối. Hãy dùng nội dung/link ngắn hơn hoặc chọn ô vuông khi gặp thông báo này.
- Đây là kiểm tra kỹ thuật bằng jsQR, chưa thử với bộ nhận diện riêng của Zalo. Anh cần thử gửi và quét bằng Zalo trên thiết bị thật trước khi dùng rộng rãi.
- Logo nhỏ và mức che đã giới hạn để ưu tiên quét; diện tích không giống hoàn toàn các ảnh concept lớn đã minh họa.
- QR tĩnh không hết hạn theo app, không giới hạn số mã/lượt quét; link/file đích cần tồn tại và có quyền xem. QR tĩnh không sửa nội dung sau khi in.
- Ảnh/video/PDF cần link chia sẻ. App không upload file lên Drive.
- Chữ dưới QR tùy chọn được xuất cùng QR riêng. Khi chuyển sang bảng nền, dùng các khối chữ độc lập.
- PNG là định dạng ưu tiên. SVG có nhúng PNG để giữ logo và chữ, không phải toàn bộ đường nét vector.

## Thiết kế bảng QR
- Tạo QR → Chèn vào bảng QR, hoặc mở tab Thiết kế bảng QR để thiết kế nền riêng.
- Bốn nền: Sóng xanh, Công nghệ, Thanh lịch, Bảng đơn vị; có upload nền riêng.
- Khổ: Dọc 900×1200, A4 900×1273, Vuông 1000×1000, Ngang 1200×900.
- Chọn thành phần trực tiếp trên bảng hoặc danh sách; sửa chữ, font, màu, cỡ chữ, đậm/nghiêng, canh chữ và chiều rộng.
- Kéo thả bằng chuột/ngón tay; chỉnh X/Y hoặc dùng phím mũi tên. Shift + mũi tên: bước 10 px.
- + Văn bản, + QR đã tạo, tải logo/ảnh riêng. QR vẽ trên cùng để không bị các khối khác che mất.
- Hoàn tác/Làm lại; lịch sử được giới hạn để tránh tăng bộ nhớ trên điện thoại.
- Tải bảng PNG 1×/2×; kiểm tra QR trên bảng trước khi xuất. In/Lưu PDF dùng hộp thoại in tùy trình duyệt.
- Lưu thiết kế tải JSON; Mở thiết kế để chỉnh tiếp. JSON có chứa ảnh và QR của bản đã lưu. Không tự lưu vào Drive.
- QR trên bảng là bản chụp khi chèn. Nếu sửa nguồn QR, hãy tạo lại và Chèn vào bảng QR lần nữa để cập nhật.
- Dự án JSON v2.0 vẫn được hỗ trợ; các nội dung đã lưu không tự thay đổi nhận diện. Chèn QR mới để áp dụng nhận diện mặc định v2.1.

## Quay về trang chủ
Điền homeUrl trong config.js. Khi nhúng, ưu tiên nút ngoài trên thanh công cụ của trang chủ để giữ nguyên phiên. Nếu không cấu hình, nút trong app thử đóng tab do trang chủ mở, rồi hiện ô nhập URL khi không đóng được.
Không có đăng nhập riêng ở app QR; link Pages công khai vẫn truy cập trực tiếp được.

## Kiểm tra và giới hạn
PASS cú pháp; tạo/đọc QR vuông/bo góc/chấm tròn; nhận diện mặc định; Unicode và logo tùy chọn; JPEG 1024/512 px với link website, link Google Form và URL có tham số; từ chối mã dài thất bại sau nén; bốn mẫu nền; chỉnh chữ/hoàn tác/làm lại; lưu/mở JSON; đổi khổ; từ chối URL sai.
Kiểm tra render bằng @napi-rs/canvas và jsQR. Chưa chạy E2E trình duyệt/điện thoại hoặc gửi-quét trên Zalo thật vì môi trường không tải được Chromium. Việc đạt kiểm tra mô phỏng không phải cam kết mọi thiết bị hay chất lượng nén đều đọc được.

## Thư viện và logo
qrcode-generator 1.4.4: MIT (Kazuhiko Arase). jsQR 1.4.0: Apache-2.0 (Cosmo Wolfe), xem vendor/jsQR-LICENSE.txt.
assets/vnpt-emblem.png: bản tách nền bằng ImageGen từ logo tham khảo anh đã cung cấp; không phải file vector gốc chính thức. Có thể thay bằng PNG trong suốt chuẩn của đơn vị, giữ tên file này để áp dụng toàn app.
Giao diện và footer giữ nhận diện của trang chủ: Lê Thanh Tùng, SĐT 0916106016, Zalo 0888158584.
