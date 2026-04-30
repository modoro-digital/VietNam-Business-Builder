# PROMPT 13: BCG Matrix (Ma trận BCG)

#### Mô tả
Phân loại sản phẩm/dịch vụ/SBU theo BCG Matrix: Stars (ngôi sao), Cash Cows (bò sữa), Question Marks (dấu hỏi), Dogs (chó). Dựa trên 2 trục: Market Growth Rate và Relative Market Share. Hỗ trợ quyết định đầu tư/rút lui.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Danh sách sản phẩm/dịch vụ/SBU cần phân loại?
2. Doanh thu mỗi sản phẩm? Tốc độ tăng trưởng?
3. Thị phần ước lượng vs đối thủ lớn nhất?
4. Market growth rate của từng phân khúc?
5. Đầu tư hiện tại cho mỗi sản phẩm?

#### Template gợi ý
Cấu trúc RPT:
- **BCG Matrix Plot** — 2×2, data points cho từng sản phẩm (bubble size = revenue)
- **Product Cards** — Mỗi sản phẩm: Quadrant | Revenue | Growth | Market Share | Recommendation
- **Strategy per Quadrant** — Stars (Invest), Cash Cows (Harvest), Question Marks (Invest/Divest decision), Dogs (Divest/Niche)
- **Portfolio Balance** — Phân bổ revenue & investment theo quadrant
- **Action Plan** — Per product: Invest more / Maintain / Reduce / Exit + Timeline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo BCG Matrix Analysis.

CONTEXT:
- DN: [Tên]
- Products/SBU: [Liệt kê: Tên | Revenue | Growth % | Market Share vs #1 competitor]
- Market Growth Rate benchmark: [ngành = %]
- Market Share benchmark: [relative to largest competitor]

FORMAT:
- Matrix data: Product | Revenue | Growth Rate | Relative Market Share | Quadrant
- Visual description: 2×2 plot với bubble chart data
- Product analysis: 1/2 trang per product — Why it's in this quadrant + Evidence + Recommendation
- Portfolio balance: Pie chart data — % Revenue in Stars/Cash Cows/QM/Dogs
- Investment reallocation: From → To table
- 12-month action plan per product

TONE: Strategic portfolio management — decisive, data-driven.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
