# Nhật ký thay đổi do AI thực hiện

Tệp này ghi lại các thay đổi đáng kể do AI thực hiện trong dự án để tiện theo dõi và tra cứu. Không ghi các thao tác nhỏ như sửa lỗi chính tả đơn lẻ hoặc định dạng không làm thay đổi nội dung.

## Quy ước ghi log

Khi có thay đổi lớn, thêm một mục mới lên đầu phần **Lịch sử thay đổi**, theo mẫu:

```text
### YYYY-MM-DD - Tên thay đổi
- **Phạm vi:** Các chức năng hoặc tệp bị ảnh hưởng.
- **Nội dung:** Tóm tắt thay đổi và lý do.
- **Kiểm tra:** Cách xác minh kết quả; ghi rõ nếu chưa chạy kiểm tra.
```

Thay đổi lớn có thể bao gồm: bổ sung hoặc thay đổi chức năng, thay đổi cấu trúc/giao diện đáng kể, sửa lỗi ảnh hưởng đến hành vi, cập nhật cấu hình/triển khai, hoặc cập nhật tài liệu phát hành. Giữ mô tả ngắn gọn, chính xác; không ghi thông tin bí mật.

## Lịch sử thay đổi

### 2026-11-06 - Đổi màu nền ảnh 1 sang dải màu sáng quang phổ lăng kính (Prismatic Spectrum)
- **Phạm vi:** `assets/css/styles.css`.
- **Nội dung:** Thay thế dải đèn LED dạng hạt rời rạc bằng hiệu ứng màu sáng phổ quang (prismatic optical spectrum glow) mượt mà, bao gồm đầy đủ các dải bước sóng quang phổ ánh sáng nhìn thấy (Đỏ Ruby, Cam hổ phách, Vàng chanh, Lục bảo, Cyan neon, Lam điện, Tím huyền bí, Hồng cánh sen); bổ sung nền đệm kính tối hòa sắc quang phổ (`radial-gradient`), viền kính trắng mờ tinh tế và hiệu ứng tỏa hào quang đa tầng rực rỡ, sang trọng.
- **Kiểm tra:** Kiểm tra cú pháp bằng `git diff --check`, đối chiếu hiển thị không dùng JavaScript và kiểm tra chế độ `prefers-reduced-motion`.

### 2026-11-06 - Nâng cấp đèn LED chạy quanh ảnh đầu tiên và bổ sung đom đóm sáng mờ dưới nền
- **Phạm vi:** `assets/css/styles.css`, `index.html`.
- **Nội dung:** Nâng cấp hiệu ứng viền ảnh đầu tiên (`.hero-avatar`) thành chuỗi dải đèn LED RGB đa sắc (Ruby `#ff1744`, Cyan `#00e5ff`, Vàng `#ffea00`, Xanh lá `#00e676`, Cam `#ff9100`, Tím `#d500f9`) chạy xoay tròn liên tục kiểu chaser lights; bổ sung lớp đom đóm sáng mờ (`.firefly-dim`) trôi bồng bềnh dưới nền sâu kết hợp với đom đóm sáng rõ (`.firefly-bright`) tạo chiều sâu không gian đa tầng; duy trì toàn bộ tiêu chuẩn nút bấm 4 tiêu chí (`text-decoration: none`, `display: inline-block`, `padding`, `background-color`, `color`, `border-radius`, `transition` kết hợp `:hover` phóng to `transform: scale(1.05)`).
- **Kiểm tra:** Kiểm tra cú pháp bằng `git diff --check`, đối chiếu hiển thị không dùng JavaScript và kiểm tra chế độ `prefers-reduced-motion`.

### 2026-11-06 - Thêm hiệu ứng đom đóm chuyển động và chuẩn hóa nút bấm từ thẻ <a>
- **Phạm vi:** `assets/css/styles.css`, `index.html`.
- **Nội dung:** Bổ sung hiệu ứng đom đóm chuyển động lập lòe (animated fireflies) bay lượn ngẫu nhiên trên bầu trời đêm Navy Blue bằng 15 hạt đom đóm phát sáng vàng xanh; chuẩn hóa toàn bộ các thẻ liên kết `<a>` (`.btn`, `.card-link`, `.contact-list a`, `.to-top`) thành các chiếc nút (button) đẹp mắt theo đúng 4 tiêu chí: `text-decoration: none`, `display: inline-block`, `padding`, `background-color`, `color`, `border-radius` và `transition` kết hợp `:hover` phóng to nhẹ (`transform: scale(1.05)`).
- **Kiểm tra:** Kiểm tra cú pháp bằng `git diff --check`, xác minh tính tương thích và kiểm tra chế độ `prefers-reduced-motion`.

### 2026-11-06 - Đổi giao diện nền Navy Blue chuyển động và thêm viền ánh sáng cho 3 ảnh dự án
- **Phạm vi:** `assets/css/styles.css`, `index.html`.
- **Nội dung:** Chuyển đổi toàn diện chủ đề sang Navy Blue đậm chất công nghệ với nền gradient chuyển động tuần hoàn giữa các tông Midnight Ocean, Navy và Deep Sapphire; tối ưu giao diện kính mờ tối (dark glassmorphism) với chữ trắng bạc sáng rõ; bổ sung khung viền ánh sáng neon cyan/sapphire phát sáng lung linh kèm nhịp thở ánh sáng (`glowPulse`) cho 3 ảnh phần dự án tiêu biểu.
- **Kiểm tra:** Kiểm tra cú pháp bằng `git diff --check`, đối chiếu độ tương phản văn bản đạt chuẩn và xác nhận tính tương thích giảm chuyển động `prefers-reduced-motion`.

### 2026-11-06 - Bổ sung hiệu ứng tia sáng chạy quanh ảnh đại diện và trạng thái màu nổi lên cho ô chữ
- **Phạm vi:** `assets/css/styles.css`.
- **Nội dung:** Bổ sung animation tia sáng neon xoay 360 độ liên tục chạy quanh viền ảnh đại diện đầu tiên (`hero-avatar`); bổ sung trạng thái tương tác màu nổi lên (elevated pop-up state, 3D lift, viền sáng và đổ bóng màu gradient phát sáng) cho các phần ô chữ (chip kỹ năng, thẻ dự án, nhãn tag, ô liên hệ, nút bấm và liên kết điều hướng).
- **Kiểm tra:** Kiểm tra cú pháp bằng `git diff --check`, đối chiếu tính tương thích responsive trên mobile/tablet/desktop và đảm bảo tôn trọng `prefers-reduced-motion`.

### 2026-11-06 - Nâng cấp hiệu ứng nền màu chuyển động đa sắc và kính mờ
- **Phạm vi:** `assets/css/styles.css`.
- **Nội dung:** Bổ sung nền màu chuyển động đa sắc (animated moving gradient) chuyển động 360 độ liên tục, tối ưu phần cứng qua `position: fixed` và `will-change`; kết hợp lớp khuếch tán ánh sáng aurora và phong cách kính mờ (glassmorphism) cho thẻ dự án, header, chip kỹ năng và footer; đảm bảo độ tương phản chữ rõ nét và tôn trọng tùy chọn `prefers-reduced-motion`.
- **Kiểm tra:** Kiểm tra định dạng bằng `git diff --check`, đối chiếu các breakpoint responsive và khả năng tiếp cận.

### 2026-11-05 - Soạn báo cáo kiểm thử trước bàn giao
- **Phạm vi:** `docs/test_report.md`.
- **Nội dung:** Soạn báo cáo QA theo sáu nhóm tiêu chí; chụp ảnh responsive ở viewport mobile/tablet/desktop và lưu trong `docs/screenshots/`.
- **Kiểm tra:** Kiểm tra ảnh responsive ở kích thước 390×844, 768×1024, 1440×900; đo chiều rộng tài liệu để xác nhận không tràn ngang tại các viewport đã thử; kiểm tra định dạng bằng `git diff --check`.

### 2026-11-05 - Khởi tạo nhật ký AI
- **Phạm vi:** `docs/AI_LOG.md`.
- **Nội dung:** Tạo quy ước ghi nhận các thay đổi lớn do AI thực hiện và khởi tạo lịch sử thay đổi.
- **Kiểm tra:** Đọc lại nội dung và xác nhận `git diff --check` không phát hiện lỗi định dạng.

### 2026-11-05 - Bổ sung ghi chú phát hành v1.0
- **Phạm vi:** `docs/RELEASENOTE.md`.
- **Nội dung:** Ghi phiên bản v1.0, ngày phát hành, chức năng mới, lỗi đã sửa và các hạn chế còn tồn tại của portfolio.
- **Kiểm tra:** Đối chiếu mô tả với mã nguồn hiện tại và xác nhận `git diff --check` không phát hiện lỗi định dạng.

### 2026-11-05 - Viết tài liệu hướng dẫn dự án
- **Phạm vi:** `README.md` tại thư mục gốc.
- **Nội dung:** Bổ sung hướng dẫn tiếng Việt về dự án, yêu cầu môi trường, cấu hình và chạy website trên Windows, macOS, Linux, cùng Docker.
- **Kiểm tra:** Xác nhận nội dung UTF-8 và các mục bắt buộc; `git diff --check` không phát hiện lỗi định dạng.