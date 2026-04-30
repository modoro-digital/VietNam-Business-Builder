# P-FIN-19: Dashboard Tài chính tháng (Monthly Financial Dashboard)

#### Mô tả
Dashboard tài chính tổng hợp 1 trang — executive summary cho Giám đốc/HĐQT. Gồm KPI cards, trend charts, traffic light indicators, và key highlights/actions.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Top 8-10 KPIs tài chính muốn theo dõi? (VD: Revenue, GP%, NI, Cashflow, AR/AP, DSO...)
2. So sánh gì? (vs Budget / vs Prior Month / vs Prior Year)
3. Format: PDF 1 trang / Google Sheets live / PowerBI / Markdown?
4. Ai đọc? (Giám đốc hàng tháng / HĐQT hàng quý)
5. Có cần phần commentary hay chỉ số liệu?

#### Template gợi ý
Cấu trúc RPT:
- **Header** — Tháng/Năm, DN, "DASHBOARD TÀI CHÍNH"
- **KPI Cards** — 8-10 cards: Metric | Actual | Target | Variance | ↑↓ | 🟢🟡🔴
- **P&L Summary** — Mini P&L: Revenue → GP → EBITDA → NI (actual vs budget)
- **Cashflow Summary** — Inflow | Outflow | Net | Balance → trend line
- **AR/AP Summary** — Total | Overdue | DSO | DPO
- **Top 3 Highlights** — Điểm tích cực
- **Top 3 Concerns** — Điểm cần chú ý + Action required
- **Next Month Outlook** — Dự báo / kế hoạch

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Dashboard Tài chính tháng.

CONTEXT:
- DN: [Tên]
- KPIs: [liệt kê 8-10 KPIs]
- So sánh: [Budget / Prior / Both]
- Format: [PDF 1 trang / Sheets / Markdown]
- Audience: [GĐ / HĐQT]

FORMAT:
- 1 trang A4 duy nhất — compact, visual, scannable
- KPI cards: 2 hàng × 4-5 cột — Metric | Value | vs Target | Trend | Status light
- Mini P&L: 6 dòng max — Revenue → COGS → GP → SGA → EBITDA → NI
- Cash position: Balance + trend sparkline data
- AR/AP: Pie chart data (Current vs Overdue)
- Traffic light: 🟢 On track | 🟡 Watch | 🔴 Action needed
- Commentary: Max 3 bullets highlights + 3 bullets concerns
- Action items: Owner | Due date

TONE: Executive — concise, visual, action-oriented.
LENGTH: 1 trang A4 (+ 1 trang hướng dẫn điền).

CROSS-REFERENCE: Dashboard dữ liệu tài chính. Format báo cáo chuẩn xem bb-reporting/Báo cáo tài chính và Báo cáo quản trị hàng tháng.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
