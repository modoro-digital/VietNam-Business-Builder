# PROMPT 05: Phân tích SWOT (SWOT Analysis)

#### Mô tả
Phân tích Strengths-Weaknesses-Opportunities-Threats toàn diện, kèm chiến lược kết hợp SO (tận dụng cơ hội bằng thế mạnh), ST (dùng thế mạnh chống đe dọa), WO (khắc phục yếu điểm nhờ cơ hội), WT (phòng thủ).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phạm vi phân tích? (toàn DN / 1 sản phẩm / 1 thị trường)
2. Đối thủ cạnh tranh chính? (2-3 tên)
3. Thế mạnh DN tự nhận? (anh nghĩ DN mình giỏi nhất ở đâu?)
4. Điểm yếu lớn nhất? (anh biết mình yếu ở đâu?)
5. Xu hướng thị trường/ngành đang thấy? (cơ hội)
6. Rủi ro/đe dọa lo ngại nhất?
7. Có data hỗ trợ không? (doanh thu, thị phần, khảo sát KH, NPS)

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — 5 dòng: Top 3 insights từ SWOT
- **Ma trận SWOT** — Bảng 2×2 chuẩn, mỗi ô 5-8 items
- **Chi tiết từng ô** — Mỗi item: Description + Evidence + Impact (High/Medium/Low)
- **TOWS Matrix** — 4 chiến lược kết hợp: SO, ST, WO, WT
- **Priority Actions** — Top 5 hành động ưu tiên dựa trên SWOT
- **Data Sources** — Nguồn thông tin đã dùng

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SWOT Analysis cho doanh nghiệp.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Quy mô: [doanh thu, nhân sự]
- Phạm vi: [toàn DN / sản phẩm X / thị trường Y]
- Đối thủ: [liệt kê 2-3]
- Strengths (chủ DN nhận): [liệt kê]
- Weaknesses (chủ DN nhận): [liệt kê]
- Opportunities (thị trường): [liệt kê]
- Threats (lo ngại): [liệt kê]
- Data hỗ trợ: [nếu có]

FORMAT:
- Ma trận SWOT 2×2: Mỗi ô 5-8 items, ngắn gọn
- Detail table: Mỗi item = Description (1-2 câu) + Evidence + Impact (H/M/L)
- TOWS Matrix: 4 ô chiến lược, mỗi ô 3-5 strategies cụ thể
- Priority Actions: Top 5, ranked, mỗi action có Owner + Timeline + Expected Impact
- Visualization data: Radar chart / Impact matrix data

TONE: Analytical, evidence-based, actionable.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
