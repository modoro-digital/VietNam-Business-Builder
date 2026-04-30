### PROMPT 04: Financial Reporting Package (Bộ Báo cáo Tài chính)

#### Mô tả
Bộ báo cáo tài chính đầy đủ gồm Báo cáo Kết quả Kinh doanh (P&L), Bảng Cân đối Kế toán (Balance Sheet), Báo cáo Lưu chuyển Tiền tệ (Cash Flow Statement), và phân tích chênh lệch (Variance Analysis). Format chuẩn theo VAS/IFRS, phục vụ quản trị nội bộ và compliance.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Chuẩn kế toán áp dụng? (VAS / IFRS / cả hai)
2. Kỳ báo cáo? (hàng tháng / quý / năm)
3. Có consolidated report (nhiều pháp nhân) không?
4. So sánh: vs Budget / vs Prior period / vs YoY?
5. Phần mềm kế toán? (MISA / SAP / QuickBooks / manual)
6. Audience: CFO / BGĐ / Kiểm toán / Cổ đông / Ngân hàng?

#### Template gợi ý
Cấu trúc FRM:
- **Phần 1** — Management Commentary: Tóm tắt tình hình tài chính, key highlights
- **Phần 2** — Income Statement (P&L): Revenue → COGS → Gross Profit → OPEX → EBITDA → Net Income
- **Phần 3** — Balance Sheet: Assets | Liabilities | Equity — snapshot
- **Phần 4** — Cash Flow Statement: Operating | Investing | Financing — Indirect method
- **Phần 5** — Variance Analysis: Budget vs Actual — top variances explained
- **Phần 6** — Financial Ratios: Profitability, Liquidity, Leverage, Efficiency
- **Phần 7** — Forecast Update: Revised forecast dựa trên actual performance
- **Phụ lục**: Detailed schedules, Notes to financial statements

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Financial Reporting Package (Bộ Báo cáo Tài chính).

CONTEXT:
- DN: [Tên] — Chuẩn KT: [VAS / IFRS]
- Kỳ báo cáo: [tháng / quý / năm]
- Consolidated: [Có/Không] — Số pháp nhân: [số]
- So sánh: [vs Budget / vs Prior / vs YoY]
- Phần mềm KT: [tên]
- Audience: [CFO / BGĐ / Kiểm toán / Cổ đông]

FORMAT:
- Management commentary: 1 trang — Revenue trend, profitability, cash position, outlook, risks
- Income Statement: Format chuẩn VAS/IFRS
  - Revenue (by product/segment) | COGS | Gross Profit | Gross Margin %
  - OPEX (by category: Personnel, Marketing, Admin, R&D, Depreciation)
  - EBITDA | EBIT | Interest | Tax | Net Income | Net Margin %
  - Columns: Actual MTD | Budget MTD | Variance | Actual YTD | Budget YTD | Prior YTD
- Balance Sheet:
  - Current Assets: Cash | AR | Inventory | Prepaid
  - Non-current Assets: PPE | Intangible | Investments
  - Current Liabilities: AP | Accrued | Short-term debt | Tax payable
  - Non-current Liabilities: Long-term debt | Provisions
  - Equity: Capital | Retained earnings | Current year profit
  - Columns: Current period | Prior period | Change | Change %
- Cash Flow Statement (indirect):
  - Operating: Net income ± adjustments ± working capital changes = Operating CF
  - Investing: Capex | Asset sales | Investments = Investing CF
  - Financing: Debt | Equity | Dividends = Financing CF
  - Net change + Opening = Closing cash
- Variance analysis: Top 10 variances — Line item | Budget | Actual | Variance | % | Root cause | Action
- Financial ratios dashboard:
  - Profitability: Gross margin | Net margin | ROE | ROA | ROIC
  - Liquidity: Current ratio | Quick ratio | Cash conversion cycle
  - Leverage: Debt/Equity | Interest coverage | Debt service coverage
  - Efficiency: AR days | AP days | Inventory turns | Revenue per employee
  - Bảng: Ratio | Current | Target | Industry avg | Trend
- Forecast update: Revised full-year estimate — Revenue | EBITDA | Net Income | Cash — vs original budget

TONE: Financial, precise, audit-ready.
LENGTH: 8-12 trang A4.

CROSS-REFERENCE: Đây là format báo cáo tài chính. Dữ liệu và dashboard chi tiết xem bb-finance/Dashboard tài chính tháng.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
