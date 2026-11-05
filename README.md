# Portfolio CV - Nguyễn Trần Quang Kiệt

Website CV cá nhân giới thiệu thông tin, kỹ năng, các dự án tiêu biểu và kênh liên hệ của **Nguyễn Trần Quang Kiệt**, định hướng Frontend Developer.

## Chức năng

- Giới thiệu bản thân và định hướng nghề nghiệp.
- Trình bày các kỹ năng và công nghệ quan tâm.
- Hiển thị các dự án tiêu biểu kèm hình ảnh và mô tả.
- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp liên kết đến TikTok, Instagram và Facebook.
- Giao diện responsive, phù hợp với điện thoại, máy tính bảng và máy tính.

> Đây là website tĩnh. Các liên kết “Xem chi tiết” trong thẻ dự án hiện là liên kết mẫu (`#`).

## Công nghệ

- **HTML5**: cấu trúc nội dung và ngữ nghĩa trang.
- **CSS3**: giao diện, Flexbox, CSS Grid, biến CSS và responsive design.
- **Nginx** (tùy chọn): phục vụ website qua Docker.

Website không sử dụng framework, thư viện JavaScript, trình biên dịch hay quy trình build.

## Yêu cầu môi trường

Để xem website:

- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Có thể mở trực tiếp `KT A2.1/index.html`. Để chạy máy chủ cục bộ, cài **Python 3** và bảo đảm lệnh Python có trong `PATH`.

Để chạy bằng Docker:

- **Windows/macOS:** Docker Desktop.
- **Linux:** Docker Engine.
- Kết nối Internet trong lần chạy đầu để tải image `nginx:alpine`.

## Cài đặt

Nếu chưa có mã nguồn, mở PowerShell hoặc terminal và clone repository:

### Windows (PowerShell)

```powershell
git clone https://github.com/kietpok/My-CV.git
cd "My-CV\KT A2.1"
```

### macOS

```bash
git clone https://github.com/kietpok/My-CV.git
cd "My-CV/KT A2.1"
```

### Linux

```bash
git clone https://github.com/kietpok/My-CV.git
cd "My-CV/KT A2.1"
```

Sau khi cài đặt, các lệnh chạy thử trong tài liệu này cần được thực hiện tại thư mục `KT A2.1` — thư mục chứa `index.html`.

## Cấu hình và tùy chỉnh

Dự án không có file cấu hình riêng, file `.env` hay thông số cần thiết lập trước khi chạy.

- Chỉnh nội dung, thông tin cá nhân và liên kết trong `KT A2.1/index.html`.
- Chỉnh màu sắc, bố cục và kiểu chữ trong `KT A2.1/assets/css/styles.css`.
- Thay ảnh trong `KT A2.1/assets/img/`. Nếu đổi tên ảnh, cập nhật đường dẫn tương ứng trong `index.html`.
- Không cần cài package hay chạy lệnh build sau khi chỉnh sửa.

## Chạy thử

### Mở trực tiếp trong trình duyệt

Mở file `index.html` trong thư mục `KT A2.1` bằng trình duyệt:

- **Windows:** nhấp đúp file trong File Explorer hoặc chọn mở bằng trình duyệt.
- **macOS:** nhấp đúp file hoặc mở bằng Safari/Chrome.
- **Linux:** nhấp đúp file hoặc mở bằng trình duyệt đã cài đặt.

### Chạy máy chủ cục bộ

Mở PowerShell hoặc terminal tại thư mục `KT A2.1`, sau đó chạy lệnh tương ứng. Python 3 cần được cài đặt và có trong `PATH`.

**Windows (PowerShell):**

```powershell
py -3 -m http.server 8000
```

**macOS:**

```bash
python3 -m http.server 8000
```

**Linux:**

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

## Chạy bằng Docker

Chạy lệnh tại thư mục `KT A2.1` (thư mục chứa `index.html`). Docker sẽ phục vụ các file tĩnh bằng Nginx ở cổng `8080` trên máy của bạn.

**Windows (PowerShell, Docker Desktop):**

```powershell
docker run --rm --name my-cv -d -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS:**

```bash
docker run --rm --name my-cv -d -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

**Linux:**

```bash
docker run --rm --name my-cv -d -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080) để xem website. Dừng container bằng:

```bash
docker stop my-cv
```

## Cấu trúc thư mục

```text
.
├── README.md
└── KT A2.1/
    ├── index.html
    ├── BAOCAO-A2.1.docx
    └── assets/
        ├── css/
        │   └── styles.css
        └── img/
            ├── 3.jpg
            ├── 4.jpg
            ├── 5.jpg
            ├── 6.jpg
            └── 7.jpg
```

## Thông tin liên hệ

- **TikTok:** [@quangkiet.08](https://www.tiktok.com/@quangkiet.08)
- **Instagram:** [@_quangkiettrann_](https://www.instagram.com/_quangkiettrann_)
- **Facebook:** [Quang Kiệt](https://www.facebook.com/share/1GuVTFMvD9/)

## Tác giả

**Nguyễn Trần Quang Kiệt** — Frontend Developer  
© 2026 Nguyễn Trần Quang Kiệt.