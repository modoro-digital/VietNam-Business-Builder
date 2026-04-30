### PROMPT 03: Monthly Management Report Template (Báo cáo Quản trị Hàng tháng)

#### Mô tả
Mẫu báo cáo quản trị hàng tháng cho BGĐ — tổng hợp hiệu suất toàn DN trong 1 trang executive summary + chi tiết theo phòng ban. Bao gồm KPI scorecard, financial highlights, operational metrics, key wins, issues, và action items.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ai đọc báo cáo hàng tháng? (CEO / BGĐ / Trưởng phòng)
2. Deadline submit? (ngày mấy hàng tháng)
3. Top KPIs muốn thấy trên trang 1? (doanh thu, lợi nhuận, cash flow, NPS...)
4. Có so sánh vs Budget / vs tháng trước / vs cùng kỳ?
5. Có phần narrative (viết comment) hay chỉ số liệu?
6. Tool tạo báo cáo? (Excel / PowerPoint / BI dashboard / document)

#### Template gợi ý
Cấu trúc FRM:
- **Trang 1** — Executive Summary: Scorecard KPIs, traffic light status, key headlines
- **Trang 2** — Financial Overview: P&L summary, revenue trend, expense breakdown, cash position
- **Trang 3** — Sales & Marketing: Pipeline, conversion, revenue by channel, campaign results
- **Trang 4** — Operations: Productivity, quality, SLA, incidents
- **Trang 5** — People: Headcount, turnover, hiring, engagement
- **Trang 6** — Key Wins / Issues / Action Items: RAID log (Risks, Actions, Issues, Decisions)
- **Phụ lục**: Detailed data tables, variance explanations

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Monthly Management Report Template (Báo cáo Quản trị Hàng tháng).

CONTEXT:
- DN: [Tên] — Audience: [CEO / BGĐ / Trưởng phòng]
- Deadline: [ngày X hàng tháng]
- Top KPIs: [liệt kê 8-12 KPIs trang 1]
- Comparison: [vs Budget / vs Prior month / vs YoY]
- Narrative: [Có/Không]
- Tool: [Excel / PPT / BI / document]

FORMAT:
- Page 1 — Executive Dashboard:
  - Company scorecard: 8-12 KPIs — KPI | Actual | Target | Variance | Trend (↑↓→) | Status (🟢🟡🔴)
  - Headlines: 3 key wins + 3 key concerns — 1 sentence each
  - CEO commentary: 3-5 câu tóm tắt tháng
- Page 2 — Financial:
  - P&L summary: Revenue | COGS | Gross Profit | OPEX | EBITDA | Net Profit — Actual vs Budget vs Prior
  - Revenue waterfall: Prior month → New sales + Upsell - Churn = Current month
  - Cash position: Opening | Inflows | Outflows | Closing | Runway (months)
  - Top 5 expense variances: Line item | Budget | Actual | Variance | Explanation
- Page 3 — Sales & Marketing:
  - Pipeline: Stage | # Deals | Value | Conversion % | Avg deal size
  - Revenue by channel/product: Bảng + trend chart
  - Marketing: Leads | MQLs | SQLs | CAC | Campaign ROI
- Page 4 — Operations:
  - Productivity: Output / FTE | Utilization % | Cycle time
  - Quality: Defect rate | First pass yield | Customer complaints
  - SLA: Service | Target | Actual | Breaches
- Page 5 — People:
  - Headcount: Plan vs Actual | New hires | Leavers | Turnover %
  - Open positions: Role | Days open | Status
  - Engagement pulse: Score | Trend
- Page 6 — RAID:
  - Risks: Risk | Impact | Probability | Mitigation | Owner
  - Actions: Action | Owner | Due | Status
  - Issues: Issue | Impact | Resolution | Owner
  - Decisions needed: Decision | Context | Options | Recommendation

TONE: Executive, visual, 1 page per section, no fluff.
LENGTH: 6-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
