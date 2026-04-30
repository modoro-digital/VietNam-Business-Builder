### PROMPT 17: Quy chế Họp hành — EOS Meeting Pulse (Meeting Policy)

#### Mô tả
Quy chế họp theo framework EOS Meeting Pulse — chuẩn hóa loại họp, tần suất, agenda, quy tắc. Giảm họp vô nghĩa, tăng họp hiệu quả. Áp dụng L10 Meeting format.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện tại có bao nhiêu cuộc họp/tuần? Cảm thấy quá nhiều/quá ít?
2. Loại họp cần có? (Daily standup / Weekly / Monthly / Quarterly / Annual)
3. Bao nhiêu người trung bình mỗi cuộc họp?
4. Có vấn đề gì với họp hiện tại? (quá dài, không có quyết định, không follow-up)
5. Muốn áp dụng L10 Meeting (EOS) không?

#### Template gợi ý
Cấu trúc POL:
- **Nguyên tắc họp**: Start/end on time, agenda trước, action items sau, no devices rule
- **Loại họp**: Daily Standup (15 min) | Weekly L10 (90 min) | Monthly Review (2h) | Quarterly Planning (1 ngày)
- **L10 Meeting format**: Segue (5 min) → Scorecard (5 min) → Rock review (5 min) → Customer/Employee headlines (5 min) → To-do review (5 min) → IDS (60 min) → Conclude (5 min)
- **Quy tắc**: Ai triệu tập, ai phải dự, thay thế khi vắng, hủy họp
- **Action items**: Format Ai | Làm gì | Khi nào | Status
- **Metrics**: % họp đúng giờ, % action items hoàn thành

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế Họp hành (Meeting Policy — EOS Meeting Pulse).

CONTEXT:
- DN: [Tên] — Họp hiện tại: [số buổi/tuần] — Vấn đề: [mô tả]
- Loại họp cần: [Daily / Weekly / Monthly / Quarterly / Annual]
- L10 format: [Có/Không]
- Nhân sự tham gia trung bình: [số]

FORMAT:
- Meeting matrix: Loại | Tần suất | Thời lượng | Participants | Facilitator | Agenda template
- L10 agenda card: 1 trang — 7 segments × time box
- Daily standup template: 3 câu hỏi (Yesterday | Today | Blockers)
- Quy tắc poster: 10 rules — in 1 trang A3
- Action items tracker: Bảng từ họp → task → owner → due → status
- Meeting effectiveness survey: 5 câu, chạy monthly

TONE: EOS-inspired, hiệu quả, action-oriented.
LENGTH: 5-7 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
