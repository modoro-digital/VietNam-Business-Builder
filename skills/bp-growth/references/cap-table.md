### PROMPT 04: Cap Table (Bảng Cơ cấu Sở hữu)

#### Mô tả
Bảng cơ cấu sở hữu cổ phần DN — tracking ai sở hữu bao nhiêu %, loại cổ phần gì, vesting schedule, và dilution impact qua các vòng gọi vốn. Cap table sạch là yêu cầu bắt buộc từ mọi nhà đầu tư.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hình DN? (TNHH / Cổ phần / cả hai)
2. Cổ đông hiện tại? (tên, % sở hữu, loại cổ phần)
3. Đã có vòng gọi vốn nào chưa? (chi tiết từng vòng)
4. Có ESOP (Employee Stock Option Plan) không? Pool size?
5. Có convertible notes / SAFE chưa convert không?
6. Vesting schedule cho founders? (cliff, vesting period)

#### Template gợi ý
Cấu trúc RPT:
- **Phần 1** — Current Cap Table: Bảng cổ đông hiện tại — fully diluted
- **Phần 2** — Historical: Từng vòng — pre-money, investment, post-money, new shares, % dilution
- **Phần 3** — ESOP Pool: Allocated, granted, exercised, available
- **Phần 4** — Convertible Instruments: Notes/SAFE details, conversion scenarios
- **Phần 5** — Pro-forma: Next round → new cap table simulation
- **Phần 6** — Dilution Waterfall: Chart showing founder dilution qua các vòng
- **Phần 7** — Vesting Schedules: Per shareholder — cliff, monthly/quarterly, acceleration
- **Phụ lục**: Share class rights, Voting rights, Liquidation preference

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Cap Table.

CONTEXT:
- DN: [Tên] — Loại hình: [TNHH / CP]
- Vốn điều lệ: [số]
- Cổ đông: [Tên | % | Loại CP | Ngày]
- Vòng gọi vốn: [liệt kê: Vòng | Valuation | Amount | Investor]
- ESOP: [Có/Không] — Pool: [%]
- Convertibles: [Có/Không] — Chi tiết: [amount, cap, discount]

FORMAT:
- Current cap table: Shareholder | Share class | # Shares | % Ownership (basic) | % Ownership (fully diluted) | Investment | Vesting status
- Historical rounds: Round | Date | Pre-money | Investment | Post-money | New shares | Price/share | Lead investor
- ESOP tracking: Grantee | Grant date | # Options | Vesting schedule | Exercised | Remaining | Exercise price
- Convertible tracker: Holder | Instrument | Amount | Cap | Discount | Conversion trigger | Estimated shares
- Pro-forma simulation: Current → After Series [X] → After ESOP refresh → Fully diluted
- Dilution waterfall: Chart data — Founding | Seed | Series A | ESOP → % per group
- Vesting: Shareholder | Total | Cliff | Vesting period | Monthly/Quarterly | Accelerated if [event]
- Rights summary: Share class | Voting | Dividend | Liquidation preference | Anti-dilution | Board seat

⚠️ LEGAL NOTE: Cap table should be reviewed by corporate lawyer. VN law: Luật DN 2020, Chương IV (Công ty CP) hoặc Chương III (TNHH).

TONE: Financial, precise, legal-aware.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
