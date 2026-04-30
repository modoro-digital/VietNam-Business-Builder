# P-FIN-16: Báo cáo P&L (Income Statement / Profit & Loss Report)

#### Mô tả
Template Báo cáo Kết quả Kinh doanh theo chuẩn mực kế toán Việt Nam (TT200 hoặc TT133). Bao gồm phân tích variance (so sánh kỳ trước, so sánh budget), và executive commentary.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Chế độ kế toán áp dụng? (TT200 cho DN lớn / TT133 cho SME)
2. Cần so sánh gì? (kỳ trước / cùng kỳ năm trước / budget / cả 3)
3. Có cần P&L theo segment? (theo sản phẩm / phòng ban / kênh bán)
4. Tần suất lập? (hàng tháng / hàng quý / hàng năm)
5. Ai đọc báo cáo này? (Giám đốc / HĐQT / Ngân hàng / Kiểm toán)

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — 3-5 dòng highlight: doanh thu, lợi nhuận, variance chính
- **P&L Statement** — Bảng chuẩn TT200/TT133: Doanh thu → Giá vốn → Lợi nhuận gộp → Chi phí → EBIT → Thuế → LNST
- **Variance Analysis** — Actual vs Budget | Actual vs Prior | Actual vs Prior Year
- **Segment P&L** — Theo SP/Phòng ban/Kênh (nếu cần)
- **Key Ratios** — Gross Margin, Operating Margin, Net Margin, Revenue growth
- **Commentary** — Giải thích top 5 variance lớn nhất

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template P&L Report (Báo cáo Kết quả Kinh doanh).

CONTEXT:
- DN: [Tên] — Chế độ: [TT200 / TT133]
- So sánh: [Prior period / Budget / Prior year / All]
- Segment: [SP / Phòng ban / Kênh / Không]
- Tần suất: [Tháng / Quý / Năm]
- Audience: [GĐ / HĐQT / NH / Kiểm toán]

FORMAT:
- P&L template theo đúng mẫu B02-DN (TT200) hoặc B02-DNN (TT133)
- Variance columns: Actual | Budget | Var $ | Var % | Prior | Var $ | Var %
- Ratio dashboard: 6 KPIs chính + trend arrow ↑↓→
- Segment breakdown (nếu có): Mỗi segment 1 mini P&L
- Commentary template: Top 5 variances + Root cause + Action
- Chart data: Revenue & Profit trend 12 tháng

TONE: Tài chính chính thức, phù hợp nộp cho kiểm toán/ngân hàng.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
