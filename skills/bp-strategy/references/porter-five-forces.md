# PROMPT 07: Porter Five Forces (Phân tích 5 áp lực cạnh tranh)

#### Mô tả
Phân tích 5 áp lực cạnh tranh theo Michael Porter: (1) Đối thủ hiện tại, (2) Đối thủ tiềm năng, (3) Sản phẩm thay thế, (4) Quyền lực nhà cung cấp, (5) Quyền lực người mua. Đánh giá sức hấp dẫn & mức độ cạnh tranh ngành.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ngành/phân khúc cụ thể đang phân tích?
2. Đối thủ trực tiếp chính? (3-5 tên, ước lượng thị phần)
3. Rào cản gia nhập ngành? (vốn, công nghệ, giấy phép, thương hiệu...)
4. Có sản phẩm/dịch vụ thay thế nào đang đe dọa?
5. Nhà cung cấp chính? Có phụ thuộc vào 1-2 NCC lớn không?
6. Khách hàng có nhiều lựa chọn thay thế không? Switching cost cao/thấp?

#### Template gợi ý
Cấu trúc RPT:
- **Dashboard** — 5 forces radar chart data (mỗi force: 1-5 scale)
- **Force 1: Competitive Rivalry** — Số đối thủ, tốc độ tăng trưởng ngành, khác biệt hóa, rào cản rút lui
- **Force 2: Threat of New Entrants** — Rào cản gia nhập, economies of scale, capital requirements
- **Force 3: Threat of Substitutes** — Sản phẩm thay thế, switching cost, price-performance trade-off
- **Force 4: Bargaining Power of Suppliers** — Tập trung NCC, chi phí chuyển đổi, backward integration
- **Force 5: Bargaining Power of Buyers** — Tập trung KH, chi phí chuyển đổi, thông tin thị trường
- **Implications** — Chiến lược phản ứng cho mỗi force
- **Overall Assessment** — Ngành hấp dẫn hay không, nên compete/niche/exit?

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Porter Five Forces Analysis.

CONTEXT:
- DN: [Tên] — Ngành/Phân khúc: [cụ thể]
- Đối thủ trực tiếp: [tên + ước lượng thị phần]
- Rào cản gia nhập: [liệt kê]
- Sản phẩm thay thế: [liệt kê]
- NCC chính: [liệt kê + mức phụ thuộc]
- Đặc điểm KH: [tập trung/phân tán, switching cost]

FORMAT:
- Radar chart data: 5 forces × score 1-5 (1=Low pressure, 5=High pressure)
- Mỗi force: 1 trang — Factor analysis table: Factor | Evidence | Score (1-5)
- Overall Industry Attractiveness score: Trung bình 5 forces
- Strategic Implications: Bảng Force | Level | Our Response
- Comparison: Vẽ 2 radar — Industry average vs Our position

TONE: Analytical, academic-meets-practical.
LENGTH: 6-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
