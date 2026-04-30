### PROMPT 14: Báo cáo doanh số (Sales Report Template)

#### Mô tả
Template báo cáo doanh số theo 3 tần suất (daily/weekly/monthly) — theo dõi performance theo rep, sản phẩm, kênh bán, và so sánh với target. Bao gồm variance analysis và action items.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tần suất báo cáo cần? (daily / weekly / monthly / tất cả)
2. KPIs cần theo dõi? (revenue, deals, conversion, activities, pipeline...)
3. Breakdown theo gì? (per rep / per product / per channel / per region)
4. So sánh gì? (vs target / vs prior period / vs prior year)
5. Ai nhận báo cáo? (Sales Manager / Director / CEO)
6. Format? (Excel / Dashboard / Email / Markdown)

#### Template gợi ý
Cấu trúc FRM:
- **Daily Flash Report**: Revenue hôm nay | # Deals closed | Pipeline movement | Top activities
- **Weekly Report**: Revenue WTD | Deals W/L | Pipeline changes | Rep ranking | Actions next week
- **Monthly Report**: Revenue MTD | vs Target | vs Prior | Breakdown per rep/product/channel | Variance analysis | Forecast next month
- **KPI Dashboard**: Visual summary — cards + charts + tables
- **Variance Analysis**: Top 5 positive + negative variances + root cause + actions
- **Rep Leaderboard**: Ranking by revenue, deals, activities
- **Product Performance**: Revenue + margin per product/service

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Báo cáo doanh số (Sales Report Template).

CONTEXT:
- DN: [Tên] — Team size: [số rep]
- Tần suất: [daily / weekly / monthly / all]
- KPIs: [liệt kê]
- Breakdown: [rep / product / channel / region]
- So sánh: [target / prior / prior year]
- Audience: [Sales Manager / Director / CEO]

FORMAT:
- Daily flash: 1 bảng compact — Revenue | Deals | Pipeline | Activities — 5 phút đọc
- Weekly: 1 trang — Revenue WTD vs Target | Win/Loss | Pipeline Δ | Rep ranking | Actions
- Monthly: 2-3 trang — Revenue MTD | vs Target | vs Prior | Breakdown tables | Variance top 5 | Forecast
- KPI cards: Revenue | # Deals | Win Rate | Avg Deal | Pipeline | Activities — Actual | Target | Δ | Status
- Rep leaderboard: Rank | Rep | Revenue | % Quota | Deals | Win Rate | Activity Score
- Product table: Product | Revenue | Units | Margin % | vs Target | Trend
- Variance analysis: KPI | Actual | Target | Var $ | Var % | Root Cause | Action

TONE: Data-driven, concise, executive-friendly.
LENGTH: Daily 1 trang | Weekly 1-2 trang | Monthly 2-3 trang.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
