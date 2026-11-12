# DrayTek Load Balancing — Không Chỉ Là Cân Bằng Tải

## Triển khai

1. Giải nén vào thư mục website hoặc repository GitHub Pages.
2. Đảm bảo `index.html`, `css/`, `js/`, `images/` ở cùng cấp.
3. Mở `index.html` trực tiếp bằng trình duyệt hoặc bật GitHub Pages từ branch chứa thư mục.
4. Website chỉ dùng HTML/CSS/JavaScript; không yêu cầu server, API, cơ sở dữ liệu hay bước build.

## Các mô phỏng tương tác

- IP-Based vs Session-Based: chuyển chế độ, sinh thêm session, theo dõi phân phối WAN.
- SLA Load Balancing: thay đổi latency/jitter/packet loss, chuyển trạng thái WAN1 trong LB Pool.
- Policy Route: chọn Banking, Backup, Guest, Game để xem cách chọn path.
- SLA Policy Route: chọn profile dịch vụ, mô phỏng WAN1 không đạt SLA và Primary/Secondary path.
- WAN Pool: chuyển nhóm Nhân viên/Khách/Server/Backup để đổi danh sách WAN.
- Mobile menu, FAQ accordion, animation theo scroll.

## Hình ảnh

- 10 hình đã duyệt đặt trong `images/illustrations/01-...webp` tới `10-...webp`.
- Ảnh thiết bị giữ trong `images/products/` theo bản chụp do AN PHÁT cung cấp.
- Logo trong `images/brand/anphat.png`; favicon cắt tỷ lệ từ logo gốc trong `images/brand/favicon.png`.

## Thông tin cần biết trước khi phát hành

- Mô phỏng minh họa nguyên lý định tuyến và chỉ dùng dữ liệu giả lập; không điều khiển router thật.
- Ngưỡng SLA trong demo không phải ngưỡng mặc định sản phẩm.
- 'WAN Pool' là cách giải thích nhóm WAN được phép dùng, không đồng nghĩa một tên menu mặc định trên DrayOS 5.
- Luồng TCP đơn lẻ không được 'bonding' qua 2 WAN trong IP/Session-based Load Balancing.
- Chuyển WAN có thể làm thay đổi Public IP và ảnh hưởng các session đang hoạt động.
- Trước khi chạy quảng cáo chính thức, xác nhận tên model, firmware và chi tiết tính năng hỗ trợ thực tế.
- CTA hiện tại: mailto:sales@anphat.vn và trang liên hệ chính thức của AN PHÁT. Có thể thay bằng Google Form chiến dịch khi bạn cung cấp đường dẫn riêng.
- Web font Be Vietnam Pro tải từ Google Fonts khi có mạng; hệ thống có fallback font.

## Nguồn kỹ thuật chính

- https://www.anphat.vn/internet-iptv-wan-lan-nat-port-co-ban/drayos-5-cau-hinh-load-balacing-nhieu-duong-truyen-internet
- https://www.anphat.vn/can-bang-tai-load-balancing-drayos5/drayos-5-tu-dong-loai-bo-wan-khong-dat-sla-ra-khoi-lb-pool
- https://www.anphat.vn/can-bang-tai-load-balancing-drayos5/drayos-5-huong-dan-dinh-tuyen-dich-vu-policy-route-theo-sla
- https://www.anphat.vn/can-bang-tai-load-balancing-drayos5/drayos-5-huong-dan-dinh-tuyen-dich-vu-theo-ip/-port/-domain

## File dự án

- `index.html`: toàn bộ nội dung, SEO, social metadata.
- `css/style.css`: giao diện và responsive.
- `js/main.js`: mô phỏng và tương tác.
- `images/`: toàn bộ hình minh họa và ảnh sản phẩm.

## Công việc Giai đoạn 5 sau khi duyệt

- Đối chiếu SEO title/description theo URL GitHub Pages hoặc domain xuất bản.
- Sau khi chọn URL thật, đổi `og:image` thành URL tuyệt đối để mạng xã hội tạo preview chính xác.
- Xác nhận đường dẫn Google Form hoặc đầu mối nhận báo giá của chiến dịch và thay CTA nếu cần.
- Kiểm tra thực tế trên GitHub Pages và các trình duyệt/thiết bị người dùng mục tiêu.


## Cập nhật bản Deploy v2
- Tích hợp bộ hình chính thức đã duyệt.
- Tăng kích thước chữ tại các khu vực nhỏ.
- Tăng tỷ trọng màu đỏ DrayTek trong tiêu đề, nhãn nhấn và CTA.
