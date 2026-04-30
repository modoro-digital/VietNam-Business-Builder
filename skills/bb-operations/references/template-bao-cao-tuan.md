### PROMPT 19: Template Báo cáo tuần (Weekly Report Template)

#### Mô tả
Template báo cáo tuần cho trưởng phòng/nhân viên — tóm tắt KPIs, done/doing/blocked, highlights, concerns, kế hoạch tuần tới.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ai sử dụng template này? (Trưởng phòng báo cáo GĐ / Nhân viên báo cáo TP / Cả hai)
2. KPIs nào cần báo cáo hàng tuần? (doanh số, SLA, chất lượng, tiến độ dự án...)
3. Deadline nộp báo cáo? (Thứ 6 chiều / Thứ 2 sáng)
4. Format hiện tại? (Email / Excel / Google Docs / họp miệng)
5. GĐ/TP muốn thấy gì nhất trong báo cáo tuần?
6. Thời gian tối đa để đọc 1 báo cáo? (2 phút / 5 phút)

#### Template gợi ý
Cấu trúc FRM:
- **Header**: Tuần # | Ngày | Phòng ban | Người báo cáo
- **KPI Snapshot**: Bảng KPI × Target × Actual × % × Status (🟢🟡🔴)
- **Done this week**: 5-7 items hoàn thành
- **In progress**: 3-5 items đang làm + % tiến độ
- **Blocked**: 1-3 items bị stuck + cần ai giúp
- **Highlights**: 1-2 thành tích/tin tốt
- **Concerns**: 1-2 rủi ro/vấn đề cần escalate
- **Next week plan**: Top 5 ưu tiên
- **Sign-off**: 1 trang A4, đọc trong 2 phút

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Báo cáo tuần (Weekly Report).

CONTEXT:
- DN: [Tên] — Dùng cho: [TP→GĐ / NV→TP / Cả hai]
- KPIs theo dõi: [liệt kê]
- Deadline: [thứ/giờ]
- Format: [Excel / Docs / Email]

FORMAT:
- Header: Tuần [#] | [Ngày-Ngày] | Phòng ban | Người báo cáo
- KPI Snapshot: Bảng KPI | Target tuần | Actual | % | Status 🟢🟡🔴
- Done this week: 5-7 bullets — completed tasks
- In progress: 3-5 bullets — ongoing + % done
- Blocked: 1-3 bullets — obstacles + cần ai giúp
- Highlights: 1-2 wins
- Concerns: 1-2 risks/issues cần escalate
- Next week plan: Top 5 priorities
- Scannable in 2 minutes — 1 trang A4

TONE: Executive, concise, status-focused.
LENGTH: 1 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
