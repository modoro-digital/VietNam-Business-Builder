### PROMPT 05: SOP Xử lý khiếu nại (Complaint Management SOP)

#### Mô tả
Quy trình xử lý khiếu nại KH — từ tiếp nhận, phân loại mức độ nghiêm trọng, điều tra nguyên nhân, giải quyết, phản hồi KH, theo dõi, đến cải tiến quy trình. Theo ISO 9001 Clause 10.2 — mọi khiếu nại là cơ hội cải tiến.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Kênh tiếp nhận khiếu nại? (hotline, email, chat, social media, trực tiếp)
2. Trung bình bao nhiêu khiếu nại/tháng? Loại phổ biến nhất?
3. Thời gian giải quyết hiện tại? Target?
4. Ai có quyền quyết định bồi thường/hoàn tiền? Hạn mức?
5. Có hệ thống ticket/CRM tracking không?
6. Đã từng có khiếu nại leo thang nghiêm trọng chưa?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Tiếp nhận: Ghi nhận, xác nhận với KH, tạo ticket
- **Bước 2** — Phân loại: Severity (Critical/High/Medium/Low), Category
- **Bước 3** — Điều tra: Thu thập thông tin, xác minh, root cause
- **Bước 4** — Giải quyết: Đề xuất giải pháp, duyệt, thực hiện
- **Bước 5** — Phản hồi: Thông báo KH kết quả, xin lỗi nếu cần
- **Bước 6** — Theo dõi: Follow-up sau 3-7 ngày, đảm bảo KH hài lòng
- **Bước 7** — Cải tiến: Root cause analysis, preventive action, cập nhật SOP

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Xử lý khiếu nại (Complaint Management).

CONTEXT:
- DN: [Tên] — Kênh tiếp nhận: [hotline / email / chat / social / trực tiếp]
- Khiếu nại/tháng: [số] — Loại phổ biến: [mô tả]
- Thời gian giải quyết hiện tại: [giờ/ngày] — Target: [giờ/ngày]
- Quyền bồi thường: [ai] — Hạn mức: [VNĐ]
- Ticket system: [tên / chưa có]

FORMAT:
- Flowchart 7 bước: Mermaid — Tiếp nhận → Phân loại → Điều tra → Giải quyết → Phản hồi → Theo dõi → Cải tiến
- Severity matrix: Level | Mô tả | Ví dụ | Response time | Resolution time | Escalate to
- Response scripts: 4 scripts theo severity — lời chào + xác nhận + cam kết thời gian
- Escalation path: Level 1 (Support Agent) → Level 2 (CS Team Lead) → Level 3 (CS Manager) → Level 4 (CEO)
- Root cause template: 5 Whys + Fishbone → Corrective action → Preventive action
- KPI tracking: Resolution time | FCR | Escalation rate | Repeat complaint rate | CSAT post-resolution
- Compensation matrix: Loại khiếu nại | Mức bồi thường | Approver | Điều kiện

TONE: Empathetic, solution-oriented, process-driven.
LENGTH: 6-8 trang A4.
```



---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
