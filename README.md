# PixMark — Chèn watermark, đóng dấu ảnh online

Công cụ **đóng dấu watermark chữ** lên ảnh của [VIG Digital](https://vigdigital.com) — chữ ký, thương hiệu, hoặc watermark **lặp kín chống lấy cắp**. Xử lý **ngay trên trình duyệt, không upload**. Kèm nén nhẹ để đăng web.

▶️ **Dùng ngay:** https://tools.vigdigital.com/pixmark/

## Tính năng

- **Watermark chữ**: gõ chữ ký / tên thương hiệu, đóng dấu lên ảnh.
- **2 kiểu**: 1 vị trí (lưới 9 điểm) hoặc **lặp kín** nghiêng −30° (chống lấy cắp).
- Màu **trắng / đen / hồng** + viền/bóng để đọc rõ trên mọi nền.
- Chỉnh **độ mờ** và **cỡ chữ**; **nhớ cài đặt** (localStorage).
- **Xoay / lật** ảnh; xử lý **hàng loạt**, tải về `.zip`.
- Kèm **nén nhẹ** (WebP/JPEG) để ảnh nhẹ hơn khi đăng web.
- 100% client-side — **không upload**, không lưu ảnh.

Hỗ trợ JPG, PNG, WebP · tối đa 20 ảnh/lượt, ≤ 25MB/ảnh.

<details>
<summary>Kỹ thuật</summary>

- Static HTML, không build step, light-mode. Dùng chung design-system [VIG Tools](https://tools.vigdigital.com) (`/shared/vig-tools.css` + `vig-tools.js`).
- Nén ảnh bằng [jSquash](https://github.com/jamsinclair/jSquash) (mozjpeg + webp WASM, self-host trong `assets/codecs`).
- Watermark vẽ bằng Canvas 2D (overlay trước khi encode); xoay/lật qua canvas transform.
- Bộ đếm lượt: `count.php` + `count.txt` (state runtime, **không** commit/deploy đè).

</details>

---

MIT © VIG Digital. Vui lòng giữ dòng ghi nguồn trong `index.html`.
