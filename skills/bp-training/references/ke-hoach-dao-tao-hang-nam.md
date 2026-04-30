### PROMPT 03: Annual Training Plan (Kế hoạch Đào tạo Hàng năm)

#### Mô tả
Kế hoạch đào tạo tổng thể theo năm — tổng hợp từ TNA, chiến lược DN, yêu cầu compliance, và ngân sách. Bao gồm lịch trình chi tiết, phân bổ ngân sách, trainer assignments, KPIs, và calendar đào tạo 12 tháng.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tổng ngân sách đào tạo năm? Phân bổ theo phòng ban hay theo loại?
2. Đào tạo bắt buộc hàng năm? (PCCC, ATLĐ, compliance, chứng chỉ ngành)
3. Có trainer nội bộ không? Bao nhiêu người?
4. Phương thức đào tạo ưu tiên? (classroom / e-learning / on-the-job / blended)
5. KPIs đào tạo hiện tại? (số giờ đào tạo/NV, tỷ lệ hoàn thành, satisfaction score)
6. Có learning management system (LMS) không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Executive Summary: Mục tiêu đào tạo năm, liên kết chiến lược, ngân sách tổng
- **Phần 2** — Training Objectives: OKR/KPIs đào tạo năm
- **Phần 3** — Training Calendar: 12 tháng × Chương trình × Đối tượng × Trainer
- **Phần 4** — Budget Breakdown: Theo loại đào tạo, theo phòng ban, theo quý
- **Phần 5** — Trainer Pool: Nội bộ & bên ngoài — chuyên môn, availability
- **Phần 6** — Delivery Methods: Phân bổ % theo classroom / e-learning / OJT / coaching
- **Phần 7** — Evaluation Plan: Mỗi chương trình đánh giá cấp Kirkpatrick nào
- **Phần 8** — Risk & Contingency: Rủi ro (budget cut, trainer unavailable) + kế hoạch B
- **Phụ lục**: Training calendar template, Budget tracking template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Annual Training Plan (Kế hoạch Đào tạo Hàng năm).

CONTEXT:
- DN: [Tên] — Nhân sự: [số] — Năm: [năm]
- Ngân sách: [tổng] — Phân bổ: [theo phòng ban / theo loại]
- Đào tạo bắt buộc: [liệt kê: PCCC, ATLĐ, ...]
- Trainer nội bộ: [số người] — Bên ngoài: [có/không]
- LMS: [tên / chưa có]
- Phương thức: [classroom / e-learning / blended / OJT]

FORMAT:
- Executive summary: 1 trang — mục tiêu, ngân sách, key programs, KPIs
- Training OKRs: Bảng Objective | Key Result | Target | Measurement
- Calendar: 12 tháng × Program | Target group | # Participants | Duration | Trainer | Method | Budget | Status
- Budget breakdown:
  - By category: Mandatory | Technical | Soft skills | Leadership | Total → % allocation
  - By quarter: Q1 | Q2 | Q3 | Q4 | Total → Planned vs Actual
  - By department: Dept | Headcount | Budget | Per capita | Programs
- Trainer pool: Name | Expertise | Internal/External | Rate | Availability | Rating
- Method mix: Pie chart data — Classroom % | E-learning % | OJT % | Coaching % | Self-study %
- Evaluation plan: Program | Kirkpatrick Level | Method | Timing | Owner
- KPI dashboard: Metric | Target | Q1 | Q2 | Q3 | Q4 | YTD
  - Training hours/employee, Completion rate, Satisfaction score, Budget utilization, Skill gap closure %
- Risk register: Risk | Impact | Probability | Mitigation | Owner

TONE: Kế hoạch chi tiết, actionable, có thể track hàng quý.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
