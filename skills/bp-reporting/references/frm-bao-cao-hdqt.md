### PROMPT 07: Board Report Template (Báo cáo HĐQT)

#### Mô tả
Mẫu báo cáo cho Hội đồng Quản trị / Advisory Board — tổng hợp tình hình DN ở cấp chiến lược, bao gồm financial performance, strategic progress, key risks, và decisions cần Board approval. Ngắn gọn, strategic-level, focus vào governance và oversight.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Cấu trúc HĐQT/Board? (số thành viên, independent directors, committees)
2. Tần suất họp Board? (hàng quý / 6 tháng / năm)
3. Board quan tâm chính: financial performance / strategy / risk / compliance / ESG?
4. Có Board committees không? (Audit / Compensation / Nomination / Risk)
5. Quyết định nào cần Board approve? (investment > X / hiring C-level / M&A)
6. Format hiện tại? Thời lượng trình bày?

#### Template gợi ý
Cấu trúc FRM:
- **Cover Page** — Meeting details, agenda, attendance
- **CEO Report** — 1-2 trang: Strategic highlights, key achievements, challenges
- **Financial Summary** — 1 trang: P&L, Balance Sheet highlights, cash position, forecast
- **Strategic Initiatives Update** — Progress vs plan, milestones, pivots
- **Risk Dashboard** — Top 5 risks, status changes, new risks, mitigation progress
- **Compliance & Governance** — Regulatory updates, audit findings, compliance status
- **Decisions Required** — Clear ask: What, Why, Options, Recommendation
- **Appendix** — Detailed financials, committee reports

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Board Report Template (Báo cáo HĐQT).

CONTEXT:
- DN: [Tên] — Board: [số thành viên] — Tần suất họp: [quý / 6 tháng]
- Committees: [Audit / Compensation / Risk / Không có]
- Focus: [financial / strategy / risk / compliance / ESG]
- Approval thresholds: [investment > X / C-level hiring / M&A]
- Thời lượng: [X phút trình bày + X phút Q&A]

FORMAT:
- Cover page: DN name | Board Meeting # | Date | Location | Time | Quorum status
- Agenda: # | Item | Presenter | Time | Type (Information/Discussion/Decision)
- CEO Report (1-2 trang):
  - Period highlights: 3-5 bullet — kết quả nổi bật
  - Strategic scorecard: Initiative | Status (🟢🟡🔴) | Commentary | Next milestone
  - Market & competitive update: Key trends, competitive moves, market position
  - Outlook: Next quarter priorities, opportunities, concerns
- Financial Summary (1 trang):
  - Key metrics: Revenue | EBITDA | Net Income | Cash — Actual vs Budget vs YoY
  - P&L waterfall: Revenue → Gross Profit → EBITDA → Net Income — highlight variances
  - Cash position: Runway, burn rate, upcoming major payments
  - Forecast: Revised full-year estimate vs original budget
- Risk Dashboard:
  - Top 5 risks: Risk | Category | Likelihood | Impact | Trend (↑↓→) | Mitigation | Owner
  - New risks since last meeting
  - Closed/downgraded risks
  - Risk heat map: 5×5 matrix — Likelihood × Impact
- Compliance section:
  - Regulatory update: New regulations | Impact | Action taken | Status
  - Audit findings: Finding | Severity | Remediation | Due date | Status
  - Litigation: Case | Status | Exposure | Counsel recommendation
- Decisions Required:
  - For each decision: Background (2-3 sentences) | Options (2-3) | Recommendation | Financial impact | Risk
  - Resolution template: "RESOLVED, that the Board hereby approves..."
- Committee Reports (if applicable): 1 paragraph summary per committee
- Minutes template: Attendees | Decisions | Action items | Next meeting

TONE: Board-level, concise, decision-focused, governance-oriented.
LENGTH: 6-10 trang A4 (excl. appendix).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
