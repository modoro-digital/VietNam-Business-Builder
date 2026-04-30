### PROMPT 02: SOP Onboard Khách hàng (Customer Onboarding SOP)

#### Mô tả
Quy trình onboarding khách hàng mới — từ lúc ký hợp đồng/mua hàng đến khi KH đạt "first value" và ổn định sử dụng. Giai đoạn onboarding quyết định 90% khả năng giữ chân KH dài hạn.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ chính cần onboard? Độ phức tạp?
2. Thời gian onboarding trung bình? (1 ngày / 1 tuần / 1 tháng)
3. Handoff từ Sales sang CS diễn ra thế nào?
4. KH cần training không? Online hay offline?
5. "First value" — KH đạt giá trị đầu tiên khi nào? Dấu hiệu nào?
6. Tỷ lệ churn trong 90 ngày đầu?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Welcome: Email chào mừng, giới thiệu CS assigned, timeline onboarding
- **Bước 2** — Setup: Thiết lập tài khoản, cấu hình, cài đặt ban đầu
- **Bước 3** — Training: Hướng dẫn sử dụng, tài liệu, video
- **Bước 4** — First Value: Hỗ trợ KH đạt kết quả đầu tiên
- **Bước 5** — Check-in: Gọi/gặp check-in Day 7, Day 14, Day 30
- **Bước 6** — Stabilize: Chuyển sang chế độ chăm sóc thường xuyên

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Onboard Khách hàng (Customer Onboarding).

CONTEXT:
- DN: [Tên] — Sản phẩm/DV: [tên] — Độ phức tạp: [thấp/TB/cao]
- Thời gian onboard: [ngày/tuần/tháng]
- Handoff Sales → CS: [quy trình hiện tại]
- Training: [online / offline / self-serve] — Thời lượng: [giờ]
- First value milestone: [mô tả]
- Churn 90 ngày: [%]

FORMAT:
- Flowchart 6 bước: Mermaid — Welcome → Setup → Training → First Value → Check-in → Stabilize
- Timeline: Gantt-style — Day 0 → Day 7 → Day 14 → Day 30 → Day 60 → Day 90
- Welcome email template: Subject + body + CTA
- Handoff checklist: 10 items Sales phải transfer cho CS
- Check-in script: 3 scripts cho Day 7, 14, 30 — câu hỏi + action
- Success criteria: Milestone | Metric | Target | Check method
- Risk signals: 5-7 dấu hiệu KH sắp churn trong onboarding + action

TONE: Warm, supportive, proactive.
LENGTH: 6-8 trang A4.
```



---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
