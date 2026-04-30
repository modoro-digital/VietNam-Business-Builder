### PROMPT 15: SOP Xử lý Sự cố (Incident Management SOP)

#### Mô tả
Quy trình xử lý mọi loại sự cố — từ IT down, mất điện, tai nạn, đến khiếu nại KH nghiêm trọng. Phân loại mức độ, escalation path, xử lý, báo cáo, và root cause analysis.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại sự cố thường gặp nhất? (IT / ATVSLĐ / Khách hàng / Vận hành / Tài chính)
2. Hiện tại có bao nhiêu cấp escalation?
3. Có đội ngũ oncall / trực ca không?
4. Thời gian phản hồi mong muốn cho sự cố nghiêm trọng? (15 phút / 1 giờ / 4 giờ)
5. Đã từng xảy ra sự cố lớn chưa? Rút kinh nghiệm gì?
6. Có phần mềm quản lý sự cố không? (Jira, Freshdesk, Excel...)
7. Ai là người quyết định cuối cùng khi sự cố nghiêm trọng?

#### Template gợi ý
Cấu trúc SOP:
- **Phân loại sự cố**: Severity 1 (Critical) → 2 (High) → 3 (Medium) → 4 (Low) + Ví dụ mỗi mức
- **Escalation matrix**: Severity × Response time × Resolver × Escalate to × Notify
- **Quy trình xử lý**: Phát hiện → Phân loại → Thông báo → Xử lý → Khắc phục → Báo cáo
- **Incident report template**: Form báo cáo sự cố chuẩn
- **Root Cause Analysis**: 5 Whys + Fishbone diagram guide
- **Post-incident review**: Checklist review sau sự cố
- **Preventive actions**: Đăng ký hành động phòng ngừa

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Xử lý Sự cố (Incident Management).

CONTEXT:
- DN: [Tên] — Loại sự cố phổ biến: [IT / ATVSLĐ / KH / Vận hành]
- Số cấp escalation: [3-4]
- Oncall: [Có/Không]
- Response time target: [thời gian]

FORMAT:
- Phân loại sự cố: Severity 1-4 + Ví dụ mỗi mức
- Escalation matrix: Severity | Response time | Resolver | Escalate to | Notify
- Flowchart: Mermaid — Phát hiện → Phân loại → Xử lý → Khắc phục → RCA → Preventive
- Incident report template: Thời gian | Mô tả | Severity | Impact | Root Cause | Action | Owner | Status
- RCA template: 5 Whys + Fishbone diagram guide
- Post-incident review: Checklist 8 câu hỏi
- Preventive action log: Action | Owner | Due | Status

TONE: Khẩn cấp, rõ ràng, action-oriented.
LENGTH: 5-7 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
