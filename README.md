# Lục Tung Sài Gòn – Tour tự thiết kế

Website cho bài tập nhóm môn Marketing du lịch (CASE 1 – Lữ Hành Sài Gòn).
Trang chính thức: https://luctungsaigon.win/
Kênh YouTube: https://youtube.com/@luctungsaigon

## Cấu trúc
- `index.html`: toàn bộ trang (HTML, CSS, JavaScript và tất cả ảnh, mã QR, favicon được nhúng sẵn dạng base64), chỉ cần một file này là chạy
- `README.md`: tài liệu này
- `og-image.jpg`: ảnh xem trước khi chia sẻ link (1200x630). Dùng đường dẫn tuyệt đối `https://luctungsaigon.win/og-image.jpg`, nên phải đăng file này cùng `index.html`

## Đăng web
Giải nén zip, kéo thả cả thư mục (có `index.html` và `og-image.jpg`) vào Netlify Drop. Giữ tên file `index.html`.

## Ưu đãi (đang áp dụng trong phần Tạm tính)
- Thành viên mới: giảm 10% đơn đầu tiên khi đăng ký tài khoản
- Đi nhóm: 4–5 người giảm 5%, 6–9 người giảm 8%, từ 10 người giảm 10%
- Khách quen: giảm 8% từ chuyến thứ 3 (khách tự tick, nhóm đối chiếu)
- Không cộng dồn, áp dụng mức cao nhất. Sửa mức giảm trong hàm `promoFor` và nội dung mục `#uu-dai`.

## Giới thiệu bạn bè (mục `#gioi-thieu`)
- Người dùng đăng nhập sẽ có mã giới thiệu riêng dạng `LT-XXXXXX` (tạo từ email, hàm `refRender`), kèm nút chép mã, chép đường dẫn `?ref=MÃ` và chia sẻ.
- Bạn bè nhập mã vào ô "Mã giới thiệu" trong form Gửi yêu cầu (hoặc mở đường dẫn, mã tự điền). Mã được gửi lên Netlify Forms ở trường `ma-gioi-thieu` và ghi trong phần lịch trình.
- Người giới thiệu nhận voucher giảm 10% tại https://hihorse.win. Nhóm gửi voucher thủ công sau khi đối chiếu mã trong Netlify Forms (chưa có máy chủ để tự cấp).
- Mã chặn dùng chính mã của mình và chặn sai định dạng. Muốn đổi điều kiện thì sửa đoạn chữ trong mục `#gioi-thieu`, FAQ và mảng `KB`.

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
