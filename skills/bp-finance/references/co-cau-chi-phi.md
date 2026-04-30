# P-FIN-05: Cơ cấu chi phí CCSC (Cost Structure Breakdown)

#### Mô tả
Tài liệu phân tích chi tiết cơ cấu chi phí của DN — phân loại thành chi phí cố định/biến đổi, trực tiếp/gián tiếp, COGS/SGA. Là cơ sở cho ngân sách, định giá, và ra quyết định tài chính.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ngành nghề & mô hình kinh doanh? (sản xuất / dịch vụ / thương mại / SaaS)
2. Các khoản chi phí lớn nhất hiện tại?
3. Có P&L hiện tại để phân tích không?
4. Cần phân tích theo phòng ban / sản phẩm / dự án?
5. Có chi phí mùa vụ / biến động lớn theo tháng không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Tổng quan cơ cấu chi phí: Pie chart data, top 10 khoản lớn nhất
- **Phần 2** — Phân loại: Cố định vs Biến đổi, Trực tiếp vs Gián tiếp
- **Phần 3** — COGS (Giá vốn hàng bán): Chi tiết từng thành phần
- **Phần 4** — SGA (Chi phí bán hàng & Quản lý): Chi tiết
- **Phần 5** — Chi phí theo phòng ban: Breakdown per department
- **Phần 6** — Phân tích xu hướng: MoM, YoY, % doanh thu
- **Phần 7** — Cơ hội tối ưu: Nhận diện chi phí có thể cắt giảm
- **Phụ lục**: Template chi phí chi tiết, Benchmark ngành

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Cơ cấu chi phí CCSC (Cost Structure Breakdown).

CONTEXT:
- DN: [Tên] — Mô hình: [Sản xuất / Dịch vụ / Thương mại / SaaS]
- Doanh thu: [số/năm] — Số phòng ban: [số]
- Khoản lớn nhất: [liệt kê top 5]
- Mùa vụ: [Có/Không]

FORMAT:
- Summary: Bảng tổng quan COGS | SGA | Other → % doanh thu
- Fixed vs Variable: Bảng mỗi khoản + phân loại + số tiền + % tổng
- Pie chart data: Top 10 khoản chi phí
- Per-department: Bảng Phòng ban | Nhân sự | Chi phí | % tổng | Cost per head
- Trend template: 12 tháng × khoản chi phí chính
- Optimization matrix: Khoản CP | Khả năng cắt | Impact | Priority

TONE: Phân tích, data-driven, khách quan.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
