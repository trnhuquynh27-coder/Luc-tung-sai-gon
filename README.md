# Lục Tung Sài Gòn – Tour tự thiết kế

Website cho bài tập nhóm môn Marketing du lịch (CASE 1 – Lữ Hành Sài Gòn).
Trang chính thức: https://luctungsaigon.win/
Kênh YouTube: https://youtube.com/@luctungsaigon

## Cấu trúc
- `index.html`: toàn bộ trang (HTML, CSS, JavaScript và tất cả ảnh, mã QR, favicon được nhúng sẵn dạng base64), chỉ cần một file này là chạy
- `README.md`: tài liệu này
- Riêng ảnh xem trước khi chia sẻ (`og-image.jpg`) dùng đường dẫn tuyệt đối `https://luctungsaigon.win/og-image.jpg`, cần đăng file này lên website nếu muốn hiện ảnh khi chia sẻ link

## Đăng web
Kéo thả file `index.html` (hoặc file zip) vào Netlify Drop. Giữ tên file là `index.html`.

## Ưu đãi (đang áp dụng trong phần Tạm tính)
- Thành viên mới: giảm 10% đơn đầu tiên khi đăng ký tài khoản
- Đi nhóm: 4–5 người giảm 5%, 6–9 người giảm 8%, từ 10 người giảm 10%
- Khách quen: giảm 8% từ chuyến thứ 3 (khách tự tick, nhóm đối chiếu)
- Không cộng dồn, áp dụng mức cao nhất. Sửa mức giảm trong hàm `promoFor` và nội dung mục `#uu-dai`.

## Chỉnh sửa nhanh (trong khối script cuối `index.html`)
- Điểm dừng và giá tham khảo từng điểm: mảng `C`
- Tour mẫu (tên, ảnh, điểm dừng): mảng `TOURS`. Giá tour tự tính bằng tổng giá các điểm dừng.
- Thông tin nhận tiền: khối `var PAY=`
- Câu trả lời của trợ lý ảo: mảng `KB`

## Mạng xã hội
Facebook, TikTok, Instagram, Threads, YouTube. Liên kết nằm ở mục Liên hệ, chân trang, dữ liệu `sameAs` (JSON-LD) và câu trả lời trợ lý ảo (`KB`). Muốn đổi thì sửa các chỗ này trong `index.html`.

## Lưu ý
- Giá hiển thị là giá tham khảo.
- Đăng nhập là bản demo: tài khoản và lịch trình đã lưu chỉ nằm trong trình duyệt của người dùng.
- Form "Gửi yêu cầu" và xác nhận thanh toán dùng Netlify Forms. Bật thông báo email trong Netlify (Forms) để nhận yêu cầu.
