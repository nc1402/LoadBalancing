# DrayTek Load Balancing – Không Chỉ Là Cân Bằng Tải

Bản phát hành: **v2.1 (SEO + Google Form)** – ngày 12/11/2026.

## 1. Triển khai ngay trên GitHub Pages

1. Giải nén ZIP. Tải các file/thư mục trong gốc ZIP lên **root** của repository GitHub, không tải nguyên ZIP lên.
2. Trong repository: **Settings → Pages → Build and deployment → Deploy from a branch**; chọn nhánh `main`, thư mục `/ (root)`.
3. Đợi GitHub Pages xuất bản và mở URL GitHub Pages để kiểm tra toàn bộ hình, các demo JavaScript và CTA.
4. Trang `index.html` sử dụng đường dẫn tương đối, hoạt động với GitHub Pages ở thư mục gốc hoặc `/repository/`.

## 2. Google Form – đã cập nhật

Toàn bộ CTA **tư vấn/báo giá** tại header, Hero và cuối trang đã liên kết tới:

https://docs.google.com/forms/d/e/1FAIpQLScSM56ZVHF-ZzfcVAm9LuB1AHoc5-35wcTRRTK-Qw1XIHQ1vQ/viewform

Nút xem mô phỏng, điều hướng nội dung và link hướng dẫn kỹ thuật vẫn giữ chức năng ban đầu. Website không gửi dữ liệu cá nhân về máy chủ riêng.

## 3. SEO cho domain chính thức (quan trọng)

Đã bổ sung tiêu đề SEO, description, Open Graph, Twitter Card, ảnh social 1200×630, structured data, robot meta, favicon và tối ưu semantic HTML.

**Bạn chưa cung cấp URL triển khai chính thức** nên bản ZIP *không cố ý thêm canonical trỏ tới domain bất kỳ*. Khi đã có URL công khai, chạy lệnh sau **trước khi commit**:

```bash
python tools/configure_seo.py --site-url https://TEN-USER.github.io/TEN-REPO/
```

Hoặc nếu chạy domain riêng:

```bash
python tools/configure_seo.py --site-url https://landing.yourdomain.vn/
```

Lệnh cập nhật **canonical, og:url, og:image (absolute URL), twitter:image, JSON-LD WebPage URL** và tạo `sitemap.xml` chính xác. Sau đó tải/commit lại `index.html`, `robots.txt`, `sitemap.xml`.

Không nhập domain giả ví dụ vào sản phẩm đang chạy. Nếu chưa biết URL cuối, bạn có thể triển khai bình thường, nhưng social preview và canonical nên được hoàn thiện sau bằng lệnh này. Đây là khuyến nghị phù hợp với Google Search Central về canonical và sitemap URL tuyệt đối.

**Lưu ý:** Với GitHub Pages dạng `/REPO/`, `robots.txt` trong repo không thay thế được `robots.txt` ở root của `username.github.io`; `sitemap.xml` vẫn có thể gửi URL trực tiếp trong Google Search Console.

## 4. Thư mục

```text
index.html                 Landing Page (10 khu vực, mô phỏng tương tác)
css/style.css              UI/UX AN PHÁT + nhấn đỏ DrayTek
js/main.js                 Các demo IP/Session, SLA, Policy, WAN Pool
images/illustrations/     10 minh họa chính thức dạng WebP
images/products/          Ảnh gốc ba router
images/brand/             Logo, favicon
images/social/            Ảnh Open Graph 1200×630
robots.txt                Cho phép lập chỉ mục
sitemap.xml               Được tạo khi biết URL chính thức
tools/configure_seo.py     Công cụ gắn canonical/social/structured data
```

## 5. Kiểm tra sau triển khai

- Xem trên desktop/mobile (375 px, 768 px, 1440 px).
- Kiểm tra bốn mô phỏng hoạt động và không có lỗi trong Console.
- Kiểm tra CTA ở nav/Hero/Footer đều mở Google Form.
- Kiểm tra ảnh WebP và ảnh social hiển thị đầy đủ.
- Khi đã điền URL chính thức: xem source HTML để kiểm tra canonical và og:image tuyệt đối; submit sitemap trong Search Console.

*Ghi chú:* Mô phỏng kỹ thuật dùng cho giải thích nguyên lý, không thay thế việc xác thực tính năng trên firmware/model DrayTek thực tế.
