# P-FIN-08: Scenario Planning 3 kịch bản (3-Scenario Financial Planning)

#### Mô tả
Phân tích tài chính theo 3 kịch bản: Best Case (lạc quan), Base Case (thực tế), Worst Case (bi quan). Mỗi kịch bản có giả định riêng, P&L dự kiến, cashflow impact, và action plan cụ thể.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Biến số chính ảnh hưởng doanh thu? (VD: số KH mới, giá bán, conversion rate)
2. Biến số chính ảnh hưởng chi phí? (VD: giá nguyên liệu, lương, thuê mặt bằng)
3. Rủi ro lớn nhất hiện tại? (thị trường, đối thủ, pháp lý, nhân sự)
4. Đã từng gặp kịch bản xấu nhất chưa? Diễn ra thế nào?
5. KPI trigger: khi nào chuyển từ Base sang Worst case plan?

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — 3 kịch bản tóm tắt trong 1 bảng
- **Assumptions Matrix** — Bảng biến số × 3 kịch bản
- **Best Case** — Giả định, P&L, Cashflow, Headcount, Investment
- **Base Case** — Giả định, P&L, Cashflow, Headcount, Investment
- **Worst Case** — Giả định, P&L, Cashflow, Headcount, Cost-cutting plan
- **Trigger Points** — KPI nào → chuyển kịch bản
- **Action Plan per Scenario** — Bảng hành động cụ thể
- **Dashboard** — So sánh 3 kịch bản trên 1 trang

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Scenario Planning 3 kịch bản tài chính.

CONTEXT:
- DN: [Tên] — Doanh thu hiện tại: [số/năm]
- Biến số doanh thu: [liệt kê + range]
- Biến số chi phí: [liệt kê + range]
- Rủi ro chính: [liệt kê]
- Thời kỳ dự báo: [12 tháng / 3 năm]

FORMAT:
- Comparison table: KPI | Best | Base | Worst — cho 10+ KPIs
- Assumptions matrix: Biến số | Best | Base | Worst + Probability %
- Mini P&L per scenario: Revenue → COGS → GP → SGA → EBITDA → NI
- Cashflow summary per scenario: 12 tháng × 3 kịch bản
- Trigger dashboard: Bảng KPI | Threshold Best→Base | Threshold Base→Worst | Current
- Action cards: Mỗi kịch bản 5-7 actions cụ thể
- Waterfall: Revenue difference breakdown Best vs Worst

TONE: Chiến lược, analytical, hướng quyết định.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
