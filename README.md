# Mô hình Đại lý chuyên ngành Hoa Sen Home

Landing page tĩnh giới thiệu 3 mô hình: Thiết bị Nhà Tắm – Nhà Bếp, Ốp lát, Điện nước.

## Cấu trúc

```
index.html                  Toàn bộ trang (HTML + CSS + JS trong 1 file)
vercel.json                 Cấu hình cache cho ảnh/PDF
assets/img/tb|ol|dn/        Ảnh phối cảnh: NN.webp (ảnh lớn), NN-t.webp (ảnh nhỏ), layout.webp (mặt bằng)
assets/pages/tb|ol|dn/      12 trang dự toán dạng ảnh (để xem trực tiếp trên điện thoại)
assets/pdf/                 3 file PDF dự toán gốc để tải về
```

tb = Thiết bị Nhà Tắm – Nhà Bếp · ol = Ốp lát · dn = Điện nước

## Đưa lên Vercel

Cách 1 (GitHub):
1. Tạo repo mới trên GitHub, upload toàn bộ thư mục này (giữ nguyên cấu trúc).
2. Vào vercel.com → Add New → Project → chọn repo → Deploy. Không cần chỉnh gì thêm (Framework: Other).

Cách 2 (Vercel CLI):
```
npm i -g vercel
cd thu-muc-nay
vercel --prod
```

## Sửa nội dung thường gặp

- Đổi link tour 3D-360: tìm `ai.hoasenhome.vn` trong `index.html` (mỗi mô hình có 2 chỗ: ô 3D-360 và nút "Tour 3D-360").
- Đổi giá: tìm số tiền (ví dụ `239,7`) trong `index.html`.
- Thay file PDF: chép đè file trong `assets/pdf/` (giữ nguyên tên). Nếu số trang đổi, render lại ảnh trang vào `assets/pages/` và sửa `pages: 12` trong phần `MODELS` cuối file.
- Thêm/bớt ảnh: đặt tên nối tiếp `NN.webp` + `NN-t.webp` và sửa `count` trong phần `MODELS` cuối file.
