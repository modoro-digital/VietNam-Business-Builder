### PROMPT 02: Financial Model & Valuation (Mô hình Tài chính & Định giá)

#### Mô tả
Mô hình tài chính 3-5 năm và định giá DN — revenue model, P&L projection, cashflow projection, và 2-3 phương pháp định giá (DCF, comparable companies, comparable transactions). Nền tảng cho pitch deck và negotiation với nhà đầu tư.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Revenue model? (subscription / transaction / project / hybrid)
2. Unit economics hiện tại? (CAC, LTV, ARPU, churn, payback period)
3. Tài chính 2-3 năm gần nhất? (revenue, costs, profit, cash)
4. Growth assumptions? (realistic, per channel/product)
5. Headcount plan? (hiring roadmap, cost per hire)
6. CapEx planned? (technology, infrastructure, expansion)
7. Comparable companies? (public or recent fundraises in same space)

#### Template gợi ý
Cấu trúc RPT:
- **Phần 1** — Model Assumptions: Revenue drivers, cost drivers, macro assumptions
- **Phần 2** — Revenue Model: Bottom-up build — customers × ARPU × retention → Revenue
- **Phần 3** — P&L Projection: 5-year monthly (Year 1) + quarterly (Year 2-3) + annual (Year 4-5)
- **Phần 4** — Cashflow Projection: Operating, investing, financing → Cash balance
- **Phần 5** — Unit Economics Dashboard: CAC, LTV, LTV/CAC, Payback, Gross Margin
- **Phần 6** — Scenario Analysis: Bull / Base / Bear cases
- **Phần 7** — Valuation: DCF, Comparable Companies, Comparable Transactions
- **Phần 8** — Sensitivity Analysis: Key variables × valuation impact
- **Phụ lục**: Detailed assumptions log, Historical financials, Cap table impact

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Financial Model & Valuation.

CONTEXT:
- DN: [Tên] — Revenue model: [subscription/transaction/project]
- Current metrics: Revenue [___] | Growth [___]% | Gross Margin [___]%
- Unit economics: CAC [___] | LTV [___] | Churn [___]%
- Historical: [2-3 năm revenue + costs]
- Headcount: Current [___] → Year 5 [___]
- Comparable: [3-5 companies + multiples]

FORMAT:
- Assumptions page: Driver | Year 1 | Y2 | Y3 | Y4 | Y5 | Source/Rationale
- Revenue build: Customer segment × growth rate × ARPU × retention → Revenue per segment → Total
- P&L: Revenue → COGS → GP → SGA (detail: S&M, G&A, R&D) → EBITDA → D&A → EBIT → Tax → NI
- Cashflow: CFO | CFI | CFF → Net → Balance
- Unit economics: Bảng CAC | LTV | LTV/CAC | Payback | Gross Margin — per segment
- DCF: WACC calculation | FCF projection | Terminal value | Enterprise value | Equity value
- Comps table: Company | Revenue | Growth | Margin | EV/Revenue | EV/EBITDA
- Sensitivity: WACC × Growth rate → Valuation matrix
- Scenario comparison: Metric | Bull | Base | Bear → Valuation range

TONE: Financial, rigorous, investor-grade.
LENGTH: 8-12 trang A4 (+ spreadsheet template description).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
