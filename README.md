# 🧩 Rubik Master (PWA)

Học giải Rubik 3×3 từ cơ bản đến nâng cao, khối 3D kéo xoay được, quét 6 mặt bằng camera/ảnh để tìm lời giải (thuật toán Kociemba qua [cubejs](https://github.com/ldez/cubejs), MIT).

- 3 cấp độ bài học, có công thức chạy thử trên khối.
- Cài lên màn hình chính điện thoại, dùng được offline.
- Không cần server, không cần build: chỉ là file tĩnh.

## Đưa lên GitHub và chia sẻ link

1. Tạo repo mới trên GitHub (ví dụ `rubik-master`), tải toàn bộ thư mục này lên nhánh `main`.
2. Vào **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Workflow `.github/workflows/pages.yml` tự triển khai. Sau 1-2 phút link có dạng
   `https://<tên-github>.github.io/rubik-master/`.
4. Gửi link cho mọi người. Camera cần HTTPS, GitHub Pages đã có sẵn HTTPS.

Cài như app: mở link trên điện thoại, chọn **Thêm vào màn hình chính** (iOS Safari) hoặc **Cài đặt ứng dụng** (Chrome Android).

## Chạy thử trên máy

    python3 -m http.server 8000

Mở http://localhost:8000 (localhost được phép dùng camera).

## Cấu trúc

    index.html        giao diện + logic
    lib/              cubejs (cube.js, solve.js)
    sw.js             service worker (offline)
    manifest.json     cấu hình PWA
    icons/            biểu tượng app

Khi sửa file, đổi `V` trong `sw.js` (ví dụ `rubik-master-v2`) để người dùng nhận bản mới.

Giấy phép: MIT. cubejs cũng theo giấy phép MIT.
