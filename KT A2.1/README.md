# Portfolio CV - Nguyễn Trần Quang Kiệt

Website CV cá nhân giới thiệu thông tin, kỹ năng, một số dự án và các kênh liên hệ của **Nguyễn Trần Quang Kiệt**, định hướng Frontend Developer.

## Chức năng

- Giới thiệu bản thân và định hướng nghề nghiệp.
- Hiển thị các kỹ năng: HTML5, CSS3, Flexbox, Grid, JavaScript, responsive design, Git/GitHub và Figma.
- Trình bày các dự án tiêu biểu bằng thẻ nội dung có hình ảnh.
- Điều hướng đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp liên kết đến TikTok, Instagram và Facebook.
- Bố cục responsive cho điện thoại, máy tính bảng và máy tính.

> Đây là website tĩnh. Các liên kết “Xem chi tiết” trong thẻ dự án hiện là liên kết mẫu (`#`).

## Công nghệ

- **HTML5**: cấu trúc nội dung và ngữ nghĩa trang.
- **CSS3**: giao diện, Flexbox, CSS Grid, biến CSS và responsive design.
- **Nginx** (tùy chọn): phục vụ website khi chạy bằng Docker.

Trang web không cần framework, thư viện JavaScript, trình biên dịch hay quy trình build.

## Yêu cầu môi trường

Để xem trang:

- Trình duyệt hiện đại như Chrome, Edge, Firefox hoặc Safari.
- Có thể mở `index.html` trực tiếp; nếu muốn chạy máy chủ cục bộ, cài Python 3.

Để chạy bằng Docker:

- Docker Engine trên Linux hoặc Docker Desktop trên Windows/macOS.
- Có kết nối Internet lần đầu để tải image `nginx:alpine`.

## Cài đặt

### Windows (PowerShell)

```powershell
git clone https://github.com/kietpok/My-CV.git
cd "My-CV\KT A2.1"
```

### macOS và Linux

```bash
git clone https://github.com/kietpok/My-CV.git
cd "My-CV/KT A2.1"
```

Nếu đã có mã nguồn, mở thư mục `KT A2.1` trong trình soạn thảo hoặc terminal. Đây là thư mục chứa `index.html`.

## Cấu hình và tùy chỉnh

Dự án không có file cấu hình riêng, file `.env` hay thông số cần thiết lập trước khi chạy.

- Sửa nội dung, thông tin liên hệ và liên kết trong `index.html`.
- Thay đổi màu sắc, bố cục và kiểu chữ trong `assets/css/styles.css`.
- Thay ảnh trong `assets/img/`; nếu đổi tên ảnh, cập nhật đường dẫn tương ứng trong `index.html`.
- Không cần cài đặt package hoặc chạy lệnh build sau khi chỉnh sửa.

## Chạy thử

### Mở trực tiếp

Mở file `index.html` trong trình duyệt:

- **Windows:** trong File Explorer, nhấp đúp `index.html` hoặc chọn mở bằng trình duyệt.
- **macOS:** nhấp đúp `index.html` hoặc mở bằng Safari/Chrome.
- **Linux:** nhấp đúp `index.html` hoặc mở bằng trình duyệt đã cài đặt.

### Chạy máy chủ cục bộ

Mở terminal tại thư mục `KT A2.1`, sau đó chạy lệnh phù hợp. Python 3 cần được cài đặt và có trong `PATH`.

**Windows (PowerShell):**

```powershell
py -3 -m http.server 8000
```

**macOS/Linux:**

```bash
python3 -m http.server 8000
```

Mở [http://localhost:8000](http://localhost:8000) trên trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

## Chạy bằng Docker

Chạy các lệnh sau tại thư mục chứa `index.html`. Docker sẽ phục vụ các file tĩnh bằng Nginx trên cổng `8080`.

**Windows (PowerShell, Docker Desktop):**

```powershell
docker run --rm --name my-cv -d -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS/Linux:**

```bash
docker run --rm --name my-cv -d -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080). Dừng container bằng:

```bash
docker stop my-cv
```

Trên Windows PowerShell, lệnh `docker stop my-cv` cũng dùng như trên.

## Cấu trúc thư mục

```text
KT A2.1/
├── index.html
├── README.md
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