### PROMPT 17: Marketing Performance Report (Báo cáo hiệu quả Marketing)

#### Mô tả
Template báo cáo hiệu quả marketing định kỳ (tuần / tháng / quý) — tổng hợp KPI từ tất cả kênh (SEO, Ads, Social, Email, Affiliate), so sánh với mục tiêu, phân tích driver, và đề xuất action. Là input chính cho cuộc họp marketing review hàng tháng và board meeting hàng quý.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tần suất báo cáo: tuần / tháng / quý? Hay cả ba?
2. Audience của báo cáo: Marketing team / Leadership / Board / Investor?
3. Các kênh marketing đang chạy: list cụ thể (FB Ads, Google Ads, SEO, Email, ...)?
4. KPI Bắc Đẩu (North Star Metric) là gì? (CAC / LTV / ROAS / MQL / Revenue?)
5. Có dashboard real-time không (Looker Studio / Power BI)? Hay làm thủ công?
6. So sánh với benchmark nào: kỳ trước / mục tiêu / industry / competitor?
7. Format ưa thích: PowerPoint / Google Slides / PDF / Notion?

#### Template gợi ý
Cấu trúc Report:
- **Executive Summary (1 slide)**: 3 bullet wins, 3 bullet concerns, 1 recommendation
- **North Star Metric**: Trend chart + variance vs target + driver analysis
- **Funnel Performance**: TOFU → MOFU → BOFU conversion rates + leaks
- **Channel Performance**: Bảng kênh × spend × output × ROI × YoY
- **Campaign Highlights**: Top 3 best/worst campaigns + learnings
- **Content Performance**: Top performing content + drop-off content
- **Brand Health**: Brand search volume, share of voice, sentiment
- **Customer Insights**: Persona insights from data, behavior changes
- **Budget Utilization**: Plan vs actual spend per channel
- **Action Items & Next Period**: 5 ưu tiên cho period tiếp theo
- **Appendix**: Data tables, methodology, definitions

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Marketing Performance Report Template.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Tần suất: [tuần / tháng / quý]
- Audience: [team / leadership / board]
- Kênh: [list]
- North Star Metric: [metric]
- Tool dashboard: [Looker Studio / Power BI / Excel]
- Format output: [PPT / Slides / PDF]

FORMAT:
- Executive summary: 1 trang/slide — 3 wins | 3 concerns | 1 recommendation
- North Star tracker: Line chart 12 tháng + bảng Variance vs Target + Driver decomposition
- Funnel waterfall: TOFU visits → MOFU leads → SQL → Customer + conversion % each stage
- Channel performance table: Kênh | Spend | Impressions | Clicks | Leads | CAC | ROAS | YoY%
- Campaign highlights: Top 3 best (KPI + learning) + Top 3 worst (KPI + lesson)
- Content scorecard: Bảng URL/Post | Views | Engagement | Conversion | Action
- Brand health: 3-4 brand metrics with trend
- Budget utilization: Bảng Kênh | Plan | Actual | Variance | Reason
- Action items: Bảng Priority | Action | Owner | Deadline | Expected Impact
- Appendix: Data definitions, calculation methodology

TONE: Executive-level, BLUF, data-driven, có insight không chỉ data dump.
LENGTH: 8-12 slides (PPT) hoặc 6-8 trang A4 (PDF).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
