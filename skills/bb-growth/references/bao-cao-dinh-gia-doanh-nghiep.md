### PROMPT 12: Business Valuation Report (Báo cáo Định giá Doanh nghiệp)

#### Mô tả
Báo cáo định giá DN toàn diện — sử dụng 3+ phương pháp, phân tích premium/discount, và đưa ra valuation range. Dùng cho gọi vốn, M&A, exit planning, hoặc mục đích nội bộ (ESOP, shareholder buyout).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mục đích định giá? (gọi vốn / M&A / nội bộ / pháp lý)
2. Financial statements 3-5 năm gần nhất?
3. Revenue model & growth trajectory?
4. Comparable companies hoặc recent transactions trong ngành?
5. IP, brand, hoặc intangible assets đáng kể?
6. Control premium hay minority discount áp dụng?

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — Valuation range, phương pháp, key findings
- **Company Overview** — History, business model, competitive position
- **Industry Analysis** — Market size, trends, multiples
- **Financial Analysis** — Historical performance, normalization adjustments, trends
- **Valuation — Method 1: DCF** — FCF projections, WACC, terminal value
- **Valuation — Method 2: Comparable Companies** — Trading multiples analysis
- **Valuation — Method 3: Comparable Transactions** — M&A multiples
- **Valuation — Method 4 (optional): Asset-based** — Adjusted book value
- **Premium & Discount Analysis** — Control, marketability, key person
- **Valuation Summary** — Weighted average, range, recommended fair value
- **Phụ lục**: Detailed financials, Comparable company data, DCF model details, Assumptions

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Business Valuation Report.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Mục đích: [gọi vốn / M&A / nội bộ]
- Revenue: [3 năm] — Profit: [3 năm] — Growth: [%]
- Comparable: [3-5 companies + multiples]
- Intangibles: [IP / Brand / Technology / khác]
- Premium/Discount: [control / minority / marketability]

FORMAT:
- Executive summary: 1 trang — Valuation range: [low] — [mid] — [high] + method weights
- Financial normalization: Adjustments table — Item | Reported | Adjustment | Normalized | Reason
- DCF model: FCF projection 5 years | WACC components | Terminal value (growth/exit multiple) | Enterprise value | Equity value
- Comparable companies: Company | Revenue | EBITDA | Growth | EV/Revenue | EV/EBITDA | Implied value
- Comparable transactions: Transaction | Date | Revenue | Price | EV/Revenue | EV/EBITDA | Implied value
- Premium/Discount: Type | Basis | % Applied | Impact on value
- Football field chart data: Method | Low | Mid | High → Visual range comparison
- Sensitivity analysis: WACC (rows) × Terminal growth (columns) → Valuation matrix
- Weighted conclusion: Method | Value | Weight | Weighted value → Fair value estimate

⚠️ NOTE: Định giá chính thức cần thẩm định viên có chứng chỉ (theo NĐ 89/2013/NĐ-CP). Template mang tính tham khảo.

TONE: Analytical, professional, valuation-grade.
LENGTH: 10-15 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
