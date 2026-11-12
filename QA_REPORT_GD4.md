# QA Giai đoạn 4 — DrayTek Load Balancing

- **Trình duyệt kiểm thử:** Chromium Headless (bản có sẵn trong môi trường)
- **Desktop:** 1440 × 900 — không tràn ngang
- **Mobile:** 390 × 844 — không tràn ngang, menu mở/đóng
- **Ảnh:** 10 ảnh WebP minh họa và 3 ảnh sản phẩm + logo, kiểm tra tải đủ khi tải eager (14 ảnh)
- **JavaScript:** không có lỗi runtime trong phiên kiểm thử
- **Đã kiểm tra thao tác:**
  - Chuyển IP-Based / Session-Based; tạo 12 session; reset còn 6 session
  - SLA Quality Lab: chuyển sang failed khi vượt ngưỡng; reset trở về passed
  - Policy Route: thay đổi kết quả khi chọn Guest/Backup
  - SLA Policy: chọn ERP và đánh dấu WAN1 suy giảm, thể hiện Secondary WAN2
  - WAN Pool: chuyển từ Staff sang Guest, cập nhật danh sách WAN
  - Hamburger mobile mở với `aria-expanded=true`
- **Nội dung kỹ thuật:** so sánh IP/Session, không hứa cộng tốc độ một TCP session; giới hạn mô phỏng không phải thông số firmware; quy định kiểm thử model/firmware trước triển khai.
- **CTA:** mailto:sales@anphat.vn, website liên hệ https://www.anphat.vn/anphat.vn/lien-he-voi-chung-toi.

**Giới hạn:** chưa kiểm thử trên hosting GitHub Pages thực tế, không đo Core Web Vitals từ mạng Internet, chưa kiểm chứng tính năng trên từng thiết bị vật lý. Những bước đó thuộc Giai đoạn 5.
