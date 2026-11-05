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