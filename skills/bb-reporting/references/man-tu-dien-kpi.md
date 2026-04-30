### PROMPT 02: KPI Dictionary (Từ điển KPI)

#### Mô tả
Tài liệu master định nghĩa toàn bộ KPIs trong DN — theo Balanced Scorecard 4 perspectives. Mỗi KPI có: tên, mã, định nghĩa, công thức, đơn vị, nguồn dữ liệu, tần suất đo, target, owner, và dashboard link. Là "nguồn sự thật duy nhất" về cách đo lường hiệu suất.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN đã có danh sách KPI chưa? Bao nhiêu KPIs?
2. Phân loại theo: BSC 4 perspectives / Phòng ban / Quy trình?
3. Có OKR system không? KPI gắn với OKR thế nào?
4. Nguồn dữ liệu: manual / ERP / CRM / BI tool?
5. Top 5-10 KPIs quan trọng nhất (CEO dashboard)?
6. Có cascading KPIs (công ty → phòng ban → cá nhân) không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Tổng quan: Triết lý đo lường, BSC framework, cascading model
- **Phần 2** — Financial KPIs: Revenue, Profit, Cash flow, ROI, Cost ratios
- **Phần 3** — Customer KPIs: NPS, CSAT, Retention, CAC, CLV, Market share
- **Phần 4** — Internal Process KPIs: Productivity, Quality, Cycle time, SLA compliance
- **Phần 5** — Learning & Growth KPIs: Training hours, Employee engagement, Innovation rate
- **Phần 6** — CEO Scorecard: Top 10-15 company-level KPIs
- **Phần 7** — Cascading Guide: Company → Department → Individual
- **Phần 8** — Review & Update Process: Thêm/sửa/xóa KPI
- **Phụ lục**: KPI card template, Glossary of metrics terms

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo KPI Dictionary (Từ điển KPI).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Số phòng ban: [số]
- KPI framework: [BSC / OKR / phòng ban / hybrid]
- Số KPIs ước tính: [số]
- Data sources: [manual / ERP / CRM / BI / spreadsheet]
- CEO top KPIs: [liệt kê top 5-10]
- Cascading: [Có/Không]

FORMAT:
- KPI overview: Bảng tóm tắt — BSC Perspective | # KPIs | Key metrics
- KPI Card (1 card per KPI):
  - KPI Name | KPI Code | BSC Perspective | Department
  - Definition: Đo lường cái gì, tại sao quan trọng
  - Formula: Công thức tính rõ ràng + ví dụ số
  - Unit: %, VNĐ, số, ngày, điểm
  - Data source: Hệ thống nào, bảng nào, trường nào
  - Frequency: Daily / Weekly / Monthly / Quarterly
  - Target: Threshold 🔴 | Target 🟡 | Stretch 🟢
  - Owner: Ai chịu trách nhiệm
  - Dashboard: Link hoặc vị trí trên dashboard
  - Related KPIs: Leading/Lagging indicators liên quan
- CEO Scorecard: 10-15 KPIs trên 1 trang — Perspective | KPI | Current | Target | Trend | Status
- Cascading example: 1 company KPI → 3 dept KPIs → 5 individual KPIs
- KPI lifecycle: Propose → Define → Validate → Implement → Review → Retire
- Glossary: 20-30 thuật ngữ metrics phổ biến — Revenue vs Billing vs Collections, Gross vs Net, Leading vs Lagging

TONE: Reference document, chính xác, dễ tra cứu.
LENGTH: 10-15 trang A4 (tùy số KPIs).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
