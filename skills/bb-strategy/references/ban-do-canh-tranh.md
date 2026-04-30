# PROMPT 08: Competitive Landscape (Bản đồ cạnh tranh)

#### Mô tả
Bản đồ cạnh tranh chi tiết — so sánh DN với 3-5 đối thủ chính trên nhiều tiêu chí: sản phẩm, giá, kênh phân phối, marketing, công nghệ, nhân sự, thị phần. Xác định positioning và khoảng trống thị trường.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. 3-5 đối thủ chính muốn so sánh? (tên + website)
2. Tiêu chí so sánh quan trọng nhất? (giá / chất lượng / tốc độ / công nghệ / dịch vụ)
3. Có data cụ thể về đối thủ không? (doanh thu, thị phần, nhân sự)
4. USP hiện tại của DN so với đối thủ?
5. Khoảng trống thị trường (white space) mà DN đang nhắm?
6. Có muốn bao gồm indirect competitors (đối thủ gián tiếp) không?

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — Top 3 competitive insights
- **Competitor Profiles** — Mỗi đối thủ 1/2 trang: Overview, Products, Strengths, Weaknesses, Recent moves
- **Comparison Matrix** — Bảng: Tiêu chí (rows) × Competitors (columns), scoring hoặc descriptive
- **Positioning Map** — 2D plot: Axis 1 (VD: Price) × Axis 2 (VD: Quality) — data points cho DN + đối thủ
- **Feature Comparison** — Bảng chi tiết: Feature | Us ✅❌ | Competitor A ✅❌ | ...
- **SWOT per Competitor** — Mini SWOT cho mỗi đối thủ
- **White Space Analysis** — Khoảng trống mà không ai đang serve
- **Battlecard** — 1 trang tóm tắt cho Sales team: "When competing against X, say..."

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Competitive Landscape Analysis.

CONTEXT:
- DN: [Tên] — Positioning hiện tại: [mô tả]
- Đối thủ: [Tên 1 - website] | [Tên 2 - website] | [Tên 3 - website]
- Tiêu chí so sánh: [liệt kê 8-12 tiêu chí]
- Data đối thủ: [nguồn: công khai / ước lượng / industry report]
- USP của DN: [mô tả]
- White space target: [mô tả]

FORMAT:
- Competitor profiles: 1/2 trang mỗi đối thủ
- Comparison matrix: Tiêu chí × Competitors, dùng ⭐ (1-5) hoặc ✅/⚠️/❌
- Positioning map: 2D data (Axis 1: [___], Axis 2: [___]) + coordinates per player
- Feature comparison: Binary ✅/❌ cho 20-30 features
- Battlecards: 1 trang per đối thủ → "They say... We say..."
- White space: Underserved needs × Competitor coverage matrix

TONE: Intelligence report — objective, data-driven, actionable.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
