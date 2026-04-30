### PROMPT 04: Unit Economics (Phân tích đơn vị kinh tế)

#### Mô tả
Phân tích unit economics chi tiết — đo lường hiệu quả kinh doanh ở cấp đơn vị: chi phí thu hút 1 khách hàng (CAC), giá trị trọn đời (LTV), thời gian hoàn vốn (Payback Period), và biên lợi nhuận per channel. Là cơ sở để ra quyết định đầu tư marketing/sales.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Doanh thu trung bình mỗi khách hàng/đơn hàng? (ARPU / Average Order Value)
2. Tần suất mua lại? Tỷ lệ khách quay lại?
3. Chi phí marketing + sales trung bình để có 1 khách hàng?
4. Thời gian trung bình từ lead → khách hàng?
5. Tỷ lệ churn / retention hiện tại?
6. Breakdown chi phí theo kênh? (online ads, content, events, sales team)

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — Key metrics: CAC, LTV, LTV/CAC ratio, Payback Period
- **Phần 1** — Customer Acquisition Cost (CAC): Tổng + per channel breakdown
- **Phần 2** — Lifetime Value (LTV): Calculation, assumptions, sensitivity
- **Phần 3** — LTV/CAC Ratio: Benchmark (>3x healthy), trend, per segment
- **Phần 4** — Payback Period: Months to recover CAC, per channel
- **Phần 5** — Contribution Margin per Channel: Revenue - Variable cost per channel
- **Phần 6** — Cohort Analysis: Retention curve, revenue per cohort
- **Phần 7** — Recommendations: Kênh nào scale, kênh nào optimize, kênh nào cắt
- **Phụ lục**: Calculation methodology, Data sources, Benchmark references

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Unit Economics Report (Phân tích đơn vị kinh tế).

CONTEXT:
- DN: [Tên] — Mô hình: [B2B / B2C / SaaS / E-commerce]
- ARPU/AOV: [số/tháng hoặc /đơn]
- Tần suất mua: [lần/năm] — Retention: [%]
- Chi phí M+S: [số/tháng] — Số KH mới/tháng: [số]
- Conversion rate: [%] — Sales cycle: [ngày]
- Kênh: [liệt kê + chi phí mỗi kênh]

FORMAT:
- Summary dashboard: 6 KPI cards — CAC | LTV | LTV/CAC | Payback | ARPU | Churn
- CAC breakdown: Bảng Kênh | Spend | Leads | Customers | CAC | % Total
- LTV calculation: ARPU × Avg Lifespan × Gross Margin — sensitivity ±10/20%
- LTV/CAC per segment: Bảng Segment | LTV | CAC | Ratio | Verdict (Healthy/Watch/Cut)
- Payback period: Bảng Kênh | CAC | Monthly Revenue | Payback Months
- Cohort table: Month 0-12 × Cohort → Retention % + Revenue
- Recommendation matrix: Kênh | LTV/CAC | Action (Scale/Optimize/Cut) | Priority

TONE: Analytical, data-driven, hướng quyết định đầu tư.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
