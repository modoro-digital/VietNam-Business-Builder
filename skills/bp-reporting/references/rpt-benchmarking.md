### PROMPT 09: Benchmarking Report (Báo cáo So sánh Chuẩn Ngành)

#### Mô tả
Báo cáo so sánh hiệu suất DN với chuẩn ngành (industry benchmarks) và đối thủ cạnh tranh — giúp CEO hiểu vị trí tương đối và xác định cơ hội cải thiện. Bao gồm financial benchmarks, operational metrics, HR metrics, và customer metrics.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ngành nghề cụ thể? (để tìm benchmark phù hợp)
2. Quy mô DN? (doanh thu, nhân sự — để so sánh đúng peer group)
3. Đối thủ cạnh tranh chính? (3-5 đối thủ)
4. Metrics nào muốn benchmark? (financial / operational / HR / customer)
5. Nguồn benchmark data: báo cáo ngành / survey / public data / industry association?
6. Tần suất: hàng năm / hàng quý?

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — Overall positioning, key gaps, top opportunities
- **Phần 1** — Methodology: Sources, peer group definition, limitations
- **Phần 2** — Financial Benchmarks: Revenue growth, margins, ROI vs industry
- **Phần 3** — Operational Benchmarks: Productivity, quality, cycle time vs peers
- **Phần 4** — People Benchmarks: Compensation, turnover, engagement vs market
- **Phần 5** — Customer Benchmarks: NPS, retention, CAC vs peers
- **Phần 6** — Gap Analysis & Recommendations: Prioritized improvement areas
- **Phụ lục**: Data sources, detailed comparison tables

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Benchmarking Report (Báo cáo So sánh Chuẩn Ngành).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Quy mô: [doanh thu / nhân sự]
- Đối thủ: [3-5 tên]
- Metrics benchmark: [financial / operational / HR / customer]
- Nguồn data: [báo cáo ngành / survey / public / association]
- Tần suất: [hàng năm / quý]

FORMAT:
- Executive summary: 1 trang — Vị trí tổng thể (trên/dưới median), top 3 gaps, top 3 strengths, key actions
- Methodology:
  - Peer group: Criteria | # companies | Source | Limitations
  - Data period: [năm] — Confidence level per metric
- Financial benchmarks:
  - Bảng: Metric | Our DN | Peer Median | Top Quartile | Bottom Quartile | Gap | Percentile rank
  - Metrics: Revenue growth | Gross margin | EBITDA margin | Net margin | ROE | ROA | Revenue/employee
  - Spider/Radar chart: Our DN vs Peer Median — 6-8 financial metrics
- Operational benchmarks:
  - Bảng: Metric | Our DN | Peer Median | Best-in-class | Gap
  - Metrics: Productivity | Quality rate | Cycle time | SLA compliance | Automation %
- People benchmarks:
  - Bảng: Metric | Our DN | Market Median | Gap
  - Metrics: Revenue/employee | Turnover % | Avg salary by role | Training hours | Engagement score | Time-to-hire
- Customer benchmarks:
  - Bảng: Metric | Our DN | Industry Avg | Top Performer | Gap
  - Metrics: NPS | CSAT | Retention rate | CAC | CLV | Response time
- Gap analysis matrix: 2×2 — High gap + High impact = Priority 1 | categorize all gaps
- Recommendations: Priority | Gap area | Current | Target | Action | Timeline | Investment | Expected ROI
- Trend: Year-over-year benchmarking comparison — Are we closing gaps or falling behind?

TONE: Analytical, objective, data-driven, actionable.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
