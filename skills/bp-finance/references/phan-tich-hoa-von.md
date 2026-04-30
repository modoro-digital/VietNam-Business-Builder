# P-FIN-09: Break-Even Analysis (Phân tích Hòa vốn)

#### Mô tả
Phân tích điểm hòa vốn (BEP) cho DN tổng thể và từng sản phẩm/dịch vụ. Xác định bao nhiêu doanh số, bao nhiêu đơn hàng cần để cover toàn bộ chi phí. Bao gồm sensitivity analysis khi thay đổi giá bán hoặc chi phí.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Danh sách sản phẩm/dịch vụ + giá bán mỗi loại?
2. Chi phí biến đổi trên mỗi đơn vị? (COGS, hoa hồng, vận chuyển...)
3. Tổng chi phí cố định hàng tháng?
4. Có sản phẩm nào cross-subsidize sản phẩm khác không?
5. Target margin mong muốn?

#### Template gợi ý
Cấu trúc RPT:
- **Tổng quan** — BEP tổng DN: Doanh số hòa vốn / tháng, / năm
- **Per Product** — BEP từng SP: Contribution margin, BEP units, BEP revenue
- **Sensitivity** — Thay đổi giá bán ±5%, ±10% → BEP thay đổi bao nhiêu
- **Margin of Safety** — Khoảng cách giữa doanh số thực và BEP
- **Visualization** — Data cho chart: Tổng chi phí vs Doanh thu vs BEP line
- **Recommendations** — Sản phẩm nào nên push, nào nên giảm

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Break-Even Analysis.

CONTEXT:
- DN: [Tên] — Số SP/DV: [số]
- SP chính: [Tên | Giá bán | Biến phí/đv | Contribution margin]
- Chi phí cố định: [số/tháng] — Chi tiết: [liệt kê top 5]
- Target margin: [%]

FORMAT:
- BEP Summary: Bảng DN tổng | Per SP → BEP units | BEP revenue | Contribution margin %
- Formula rõ ràng: BEP = Fixed Cost / (Price - Variable Cost per Unit)
- Sensitivity table: Giá bán ±5/10/15% × Biến phí ±5/10/15% = BEP matrix
- Margin of Safety: Current Revenue | BEP Revenue | MoS % | Interpretation
- Chart data: X = Units, Y1 = Total Revenue, Y2 = Total Cost, intersection = BEP
- Product ranking: Contribution margin desc → Recommend push order

TONE: Analytical, data-driven, dễ hiểu cho non-finance.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
