### PROMPT 05: Operational Dashboard Design (Thiết kế Dashboard Vận hành)

#### Mô tả
Tài liệu hướng dẫn thiết kế và xây dựng dashboard vận hành — từ xác định metrics, layout design, data sources, refresh frequency, đến user access. Áp dụng nguyên tắc data visualization best practices (Stephen Few, Edward Tufte). Dashboard là "bảng điều khiển" real-time cho quản lý.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Dashboard cho ai? (CEO / COO / Trưởng phòng / Team)
2. Tool: Excel / Google Sheets / Power BI / Tableau / Looker / Metabase?
3. Metrics chính muốn track real-time?
4. Data sources: ERP / CRM / spreadsheet / manual / API?
5. Refresh frequency: real-time / daily / weekly?
6. Mobile access cần không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Dashboard Strategy: Objectives, audience, tiered dashboards (strategic/tactical/operational)
- **Phần 2** — Metrics Selection: Chọn metrics đúng — leading vs lagging, actionable vs vanity
- **Phần 3** — Layout Design: Wireframe, visual hierarchy, F-pattern, above-the-fold
- **Phần 4** — Visualization Best Practices: Chart type selection, color, labels, interactivity
- **Phần 5** — Data Architecture: Sources, ETL, data model, refresh
- **Phần 6** — Dashboard Catalog: Danh sách tất cả dashboards, owner, audience, metrics
- **Phần 7** — Governance: Access control, maintenance, update process
- **Phụ lục**: Wireframe templates, Chart selection guide, Color palette

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Operational Dashboard Design Guide (Hướng dẫn Thiết kế Dashboard).

CONTEXT:
- DN: [Tên] — Dashboard audience: [CEO / COO / Trưởng phòng / Team]
- Tool: [Power BI / Tableau / Looker / Google Sheets / Excel]
- Data sources: [ERP / CRM / spreadsheet / API]
- Refresh: [real-time / daily / weekly]
- Mobile: [Có/Không]

FORMAT:
- Dashboard tiers: Strategic (CEO, monthly) → Tactical (Manager, weekly) → Operational (Team, daily)
- Metrics selection framework: Bảng Business question | Metric | Type (Leading/Lagging) | Source | Refresh | Actionability
- CEO dashboard wireframe: Layout mockup — 4-6 KPI cards top + 2-3 trend charts + 1 table
- Department dashboard wireframe: 6-8 KPI cards + 4-6 charts + filters (date, segment, region)
- Chart selection guide:
  - Comparison: Bar chart | Column chart
  - Trend over time: Line chart | Area chart
  - Composition: Pie/Donut (max 5 slices) | Stacked bar
  - Distribution: Histogram | Box plot
  - Relationship: Scatter plot | Bubble chart
  - KPI status: Traffic light cards | Gauge | Bullet chart
- Design principles:
  - Visual hierarchy: Most important = top-left, largest
  - Data-ink ratio: Maximize data, minimize decoration (Tufte)
  - Color: Max 5-7 colors, semantic (green=good, red=bad), colorblind-safe
  - Labels: Direct labeling > legends, meaningful titles, units
  - Interactivity: Drill-down | Filters | Tooltips | Cross-filtering
- Data architecture: Mermaid — Source systems → ETL/Pipeline → Data warehouse → Dashboard tool → Users
- Dashboard catalog: Bảng Dashboard name | Audience | Tier | Metrics | Data source | Refresh | Owner | URL
- Governance: Access matrix (dashboard × role), review schedule, change request process
- Performance: Load time targets, optimization tips, caching strategy

TONE: Technical + design-oriented, visual-first thinking.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
