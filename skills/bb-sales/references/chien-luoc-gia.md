### PROMPT 02: Pricing Strategy (Chiến lược giá)

#### Mô tả
Chiến lược định giá toàn diện — xác định vị thế giá trên thị trường, phương pháp tính giá, cơ cấu chiết khấu, và quy trình điều chỉnh giá. Khác với Pricing Policy (chính sách nội bộ ở Finance), đây tập trung vào chiến lược cạnh tranh và go-to-market.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Vị thế giá mong muốn? (Premium / Mid-range / Value / Low-cost)
2. Cơ cấu giá hiện tại? (one-time / subscription / usage-based / hybrid)
3. Giá bán trung bình hiện tại? So với đối thủ ở đâu?
4. Chính sách chiết khấu hiện tại? (volume, loyalty, seasonal, early payment)
5. Ai có quyền discount? Hạn mức bao nhiêu %?
6. Tần suất thay đổi giá? Trigger thay đổi là gì?
7. Có sản phẩm loss-leader / freemium không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Pricing Objective: Maximize revenue / Market share / Profit margin / Penetration
- **Phần 2** — Price Positioning: Perceptual map vs đối thủ, value-price matrix
- **Phần 3** — Pricing Method: Cost-plus / Value-based / Competitive / Dynamic — khi nào dùng gì
- **Phần 4** — Price Architecture: Tiers, bundles, add-ons, upsell/cross-sell pricing
- **Phần 5** — Discount Framework: Bảng chiết khấu theo loại, approval levels, guardrails
- **Phần 6** — Competitive Pricing: Price comparison matrix, response playbook
- **Phần 7** — Price Review & Adjustment: Triggers, process, communication plan
- **Phụ lục**: Price list template, Discount calculator, Competitive price tracker

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Pricing Strategy (Chiến lược giá).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Số SP/DV: [số]
- Vị thế giá: [Premium / Mid / Value / Low-cost]
- Cơ cấu giá: [one-time / subscription / usage-based / hybrid]
- Giá TB: [số] — So với đối thủ: [cao hơn / ngang / thấp hơn X%]
- Chiết khấu hiện tại: [volume / loyalty / seasonal / early payment]
- Quyền discount: [Chức danh] — Max: [%]
- Loss-leader/Freemium: [Có/Không] — [mô tả]

FORMAT:
- Price positioning map: 2x2 matrix (Value vs Price) — plot DN + đối thủ
- Price architecture: Bảng Tier | Features | Price | Target segment | Margin %
- Discount framework: Bảng Loại CK | Điều kiện | % CK | Approval | Guardrail
- Competitive comparison: Bảng SP | DN Price | Competitor A | B | C | Positioning
- Price waterfall: List Price → Discount → Net Price → COGS → Margin (Mermaid/bảng)
- Decision tree: Khi nào raise/lower/hold price — flowchart
- Review calendar: Quarterly trigger checklist

TONE: Chiến lược, data-driven, cạnh tranh.
LENGTH: 6-10 trang A4.

CROSS-REFERENCE: Đây là chiến lược giá cạnh tranh. Chính sách định giá nội bộ (cost, margin floors, approval workflow) xem bb-finance/Chính sách định giá.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
