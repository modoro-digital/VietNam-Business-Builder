### PROMPT 01: Product/Service Catalog (Danh mục Sản phẩm & Dịch vụ)

#### Mô tả
Tài liệu master chứa toàn bộ danh mục sản phẩm/dịch vụ của DN — mô tả chi tiết, đối tượng mục tiêu, pricing tổng quan, lifecycle stage, và cross-reference với các tài liệu khác. Đây là "nguồn sự thật duy nhất" (single source of truth) về portfolio DN.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN có bao nhiêu sản phẩm/dịch vụ? Phân loại thế nào? (theo ngành, theo đối tượng, theo mức giá)
2. Mỗi SP/DV đang ở giai đoạn nào? (Development / Launch / Growth / Mature / Decline)
3. SP/DV nào là flagship? SP/DV nào cross-sell/upsell với nhau?
4. Có version/tier khác nhau không? (Basic / Pro / Enterprise)
5. Kênh phân phối từng SP/DV? (Online / Offline / Hybrid / Đại lý / Affiliate)
6. Tần suất cập nhật catalog? Ai chịu trách nhiệm maintain?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Tổng quan Portfolio: Bảng tóm tắt toàn bộ SP/DV, revenue contribution, lifecycle stage
- **Phần 2** — Chi tiết từng SP/DV: Tên, Mã SP, Mô tả, Target Customer, USP, Pricing, Kênh bán, Status
- **Phần 3** — Product Matrix: Cross-sell/Upsell map, Bundle options
- **Phần 4** — Lifecycle Dashboard: Sơ đồ BCG hoặc PLM cho từng SP
- **Phần 5** — Competitive Positioning: SP mình vs đối thủ — feature comparison
- **Phần 6** — Quy trình cập nhật Catalog: Ai, khi nào, approval flow
- **Phụ lục**: Product one-pager template, SKU naming convention

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Product/Service Catalog (Danh mục Sản phẩm & Dịch vụ).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Số SP/DV: [số]
- Phân loại: [theo ngành / đối tượng / mức giá]
- Flagship: [tên SP]
- Tiers: [Basic/Pro/Enterprise hoặc không]
- Kênh phân phối: [Online / Offline / Hybrid / Đại lý]

FORMAT:
- Portfolio summary: Bảng SP | Mã | Category | Revenue % | Lifecycle | Status
- Product card: Mỗi SP 1 block — Tên | Mô tả | Target | USP | Price Range | Kênh | KPIs
- Cross-sell matrix: Bảng SP×SP → Combo/Bundle opportunity
- Lifecycle map: Sơ đồ vị trí từng SP trên BCG matrix hoặc PLM curve
- Competitive comparison: Feature matrix SP mình vs 2-3 đối thủ chính
- SKU naming: Convention rõ ràng + ví dụ
- Update log: Template Version | Date | Changed by | Changes

TONE: Rõ ràng, dễ tra cứu, dùng được cho cả Sales lẫn Marketing.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
