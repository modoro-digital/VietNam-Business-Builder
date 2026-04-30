# P-FIN-04: Chính sách định giá sản phẩm (Pricing Policy)

#### Mô tả
Chính sách quy định phương pháp, quy trình, và thẩm quyền định giá sản phẩm/dịch vụ. Bao gồm chiến lược giá, cơ cấu giá, chính sách chiết khấu, và quy trình điều chỉnh giá.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ chính? Có bao nhiêu SKU / service line?
2. Phương pháp định giá hiện tại? (Cost-plus / Value-based / Competitor-based / Dynamic)
3. Cơ cấu giá: Giá bán lẻ / Giá đại lý / Giá OEM / Giá dự án?
4. Chính sách chiết khấu? (theo volume / theo đối tượng / theo thanh toán)
5. Tần suất review giá? Ai có quyền thay đổi giá?
6. Có sản phẩm chạy theo mùa / theo thị trường không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục tiêu định giá: Lợi nhuận mục tiêu, vị thế thị trường, penetration/skimming
- **Phần 2** — Phương pháp định giá: Cost-plus, Value-based, Competitive — khi nào dùng cái nào
- **Phần 3** — Cơ cấu giá: Price list structure, tier pricing, bundle pricing
- **Phần 4** — Chính sách chiết khấu: Bảng chiết khấu theo loại
- **Phần 5** — Quy trình duyệt giá: Giá mới, điều chỉnh giá, giá đặc biệt
- **Phần 6** — Giá cho kênh phân phối: Đại lý, OEM, Affiliate, Direct
- **Phần 7** — Review & Điều chỉnh: Tần suất, trigger, quy trình
- **Phụ lục**: Price list template, Discount approval form, Margin calculator

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách định giá sản phẩm (Pricing Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Số SKU/service: [số]
- Phương pháp hiện tại: [Cost-plus / Value-based / Competitive / Dynamic]
- Cơ cấu giá: [Retail / Wholesale / OEM / Project]
- Chiết khấu: [volume / đối tượng / thanh toán]
- Review giá: [tần suất] — Người quyết: [chức danh]

FORMAT:
- Pricing framework: Sơ đồ Cost → Markup → List Price → Discount → Net Price
- Bảng chiết khấu: Đối tượng | Volume từ-đến | % CK | Approval cần
- Margin analysis: Bảng SP | Cost | Price | Margin % | Min Price Floor
- Decision tree: Flowchart khi nào dùng Cost-plus vs Value-based vs Competitive
- Price approval workflow: Mermaid flowchart
- Competitive price tracking template

TONE: Chiến lược + thực tế, cân bằng giữa lợi nhuận và cạnh tranh.
LENGTH: 6-10 trang A4.

CROSS-REFERENCE: Đây là chính sách định giá nội bộ (cost, margin, approval). Chiến lược giá cạnh tranh go-to-market xem bb-sales/Chiến lược giá.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
