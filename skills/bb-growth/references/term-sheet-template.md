### PROMPT 05: Term Sheet Template (Mẫu Điều khoản Đầu tư)

#### Mô tả
Template điều khoản đầu tư — non-binding document tóm tắt terms & conditions trước khi ký hợp đồng chính thức. Bao gồm valuation, investment amount, instrument type, investor rights, governance, và protective provisions.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại instrument? (Equity / Convertible Note / SAFE / Hybrid)
2. Pre-money valuation range?
3. Board composition mong muốn?
4. Key investor rights nào chấp nhận / không chấp nhận?
5. Vesting cho founders: đã có hay cần thêm?
6. Luật áp dụng? (VN / Singapore / Delaware)

#### Template gợi ý
Cấu trúc FRM:
- **Preamble** — Parties, date, non-binding notice
- **Investment Terms** — Amount, valuation, price per share, type of security
- **Capitalization** — Pre & post-money cap table
- **Investor Rights** — Information rights, pro-rata, anti-dilution, registration
- **Governance** — Board composition, observer rights, protective provisions
- **Founder Terms** — Vesting, non-compete, key man insurance
- **Closing Conditions** — Due diligence, legal, regulatory
- **Other** — Exclusivity period, expenses, confidentiality, governing law

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Term Sheet Template.

CONTEXT:
- DN: [Tên] — Instrument: [Equity / Note / SAFE]
- Valuation: [pre-money] — Raise: [amount]
- Board: [current + proposed]
- Governing law: [VN / SG / US]

FORMAT:
- Bilingual template (Việt-Anh) nếu có yếu tố nước ngoài
- Investment terms: Bảng tóm tắt — Item | Term | Notes
  - Security type, Price/share, Amount, Pre-money, Post-money, Shares issued
- Cap table impact: Before | After — per shareholder
- Investor rights: Checklist ☐ — Information | Pro-rata | Anti-dilution (type) | Registration | Tag-along | Drag-along
- Governance: Board seats | Observer | Protective provisions (veto list)
- Founder: Vesting schedule | Non-compete | ESOP commitment | Key man
- Conditions: Due diligence scope | Timeline | Exclusivity period
- Definitions: Key terms defined — Liquidation event, Qualified financing, Material adverse change
- Signature block: Company | Investor | Date

⚠️ LEGAL NOTE: Term sheet PHẢI được review bởi luật sư. Template chỉ mang tính tham khảo.

TONE: Legal-lite — clear, balanced, professional.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
