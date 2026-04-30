### PROMPT 08: SOP Phân loại khách hàng (Customer Tiering SOP)

#### Mô tả
Quy trình phân loại KH thành các tier A/B/C/D — dựa trên criteria (revenue, frequency, potential, engagement). Mỗi tier có chế độ chăm sóc khác nhau. Migration rules khi KH lên/xuống tier.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện tại có phân loại KH chưa? Theo tiêu chí nào?
2. Doanh thu trung bình mỗi KH? Range min-max?
3. Tần suất mua hàng? Range?
4. Có muốn tính tiềm năng (potential) không, hay chỉ dựa trên lịch sử?
5. Bao nhiêu tier? (3: VIP/Standard/Basic hay 4: A/B/C/D)
6. Mỗi tier được chăm sóc khác nhau thế nào?

#### Template gợi ý
Cấu trúc SOP:
- **Tiêu chí phân loại**: Revenue (40%) + Frequency (25%) + Potential (20%) + Engagement (15%)
- **Tier definitions**: A (Top 10%) → B (Next 20%) → C (Next 40%) → D (Bottom 30%)
- **Benefits per tier**: Dedicated CSM, response priority, exclusive offers, events
- **Migration rules**: Đánh giá lại quarterly, điều kiện lên/xuống tier
- **Data sources**: CRM, billing, support tickets, engagement metrics

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Phân loại khách hàng (Customer Tiering).

CONTEXT:
- DN: [Tên] — Số KH: [số] — Revenue range: [min-max VNĐ/tháng]
- Phân loại hiện tại: [có/không] — Tiêu chí: [mô tả]
- Số tier: [3/4] — Tên tier: [VIP/Gold/Silver/Bronze hoặc A/B/C/D]
- Tần suất đánh giá: [quarterly / semi-annual]

FORMAT:
- Scoring model: Bảng Criteria | Weight | Scoring rule (1-10) | Data source
- Tier matrix: Tier | Score range | % KH | Revenue contribution | Mô tả | Color code
- Benefits matrix: Tier | Dedicated CSM | Response SLA | Discount | Events | Gifts | Review freq
- Migration rules: Điều kiện lên tier (2 quý liên tiếp ≥ threshold) | Xuống tier | Grace period
- Implementation: Bước 1 (data collection) → 2 (scoring) → 3 (assignment) → 4 (communication) → 5 (review)
- Dashboard: Tier distribution | Revenue by tier | Movement (up/down/stable) | At-risk customers

TONE: Strategic, data-driven, fair.
LENGTH: 5-7 trang A4.
```



---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
