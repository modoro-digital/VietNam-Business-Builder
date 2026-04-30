### PROMPT 12: Improvement Proposal Form (Mẫu Đề xuất Cải tiến)

#### Mô tả
Template để bất kỳ nhân viên nào đề xuất ý tưởng cải tiến — mô tả vấn đề, root cause, giải pháp đề xuất, impact dự kiến, và resources cần thiết. Form phải đơn giản, dễ điền để không cản trở việc đề xuất.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Form điền trên gì? (giấy / Google Forms / Notion / phần mềm nội bộ)
2. Mức độ chi tiết: đơn giản (1 trang) hay chi tiết (2-3 trang)?
3. Có cần phần phân tích root cause trong form không?
4. Ai review form? Timeline review?
5. Có category/classification cho cải tiến không?

#### Template gợi ý
Cấu trúc FRM:
- **Header** — Tiêu đề đề xuất, Người đề xuất, Phòng ban, Ngày, Mã số
- **Phần 1** — Vấn đề hiện tại: Mô tả vấn đề, tần suất, impact
- **Phần 2** — Root Cause: Phân tích nguyên nhân gốc (5 Whys / Fishbone)
- **Phần 3** — Giải pháp đề xuất: Mô tả giải pháp, cách triển khai
- **Phần 4** — Impact dự kiến: Tiết kiệm thời gian / chi phí / tăng chất lượng
- **Phần 5** — Resources cần: Ngân sách, nhân lực, thời gian, tool
- **Phần 6** — Đánh giá (do reviewer điền): Score, priority, decision, feedback
- **Footer** — Approval chain

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Improvement Proposal Form (Mẫu Đề xuất Cải tiến).

CONTEXT:
- DN: [Tên] — Format: [giấy / digital / hybrid]
- Chi tiết: [đơn giản 1 trang / chi tiết 2-3 trang]
- Root cause: [Có/Không]
- Reviewer: [chức danh] — Timeline review: [X ngày]

FORMAT:
- 1 template fillable — tối đa 2 trang A4
- Header: Mã đề xuất [IMP-YYYY-NNN] | Người đề xuất | Phòng ban | Ngày
- Problem: [___] + gợi ý "Mô tả vấn đề trong 2-3 câu"
- Root cause: Sơ đồ 5 Whys đơn giản (Why 1 → Why 2 → ... → Root Cause)
- Solution: [___] + gợi ý "Mô tả giải pháp step-by-step"
- Impact: Bảng — Metric | Before | After (expected) | Improvement %
- Resources: Budget [___] | People [___] | Time [___] | Tools [___]
- Reviewer section: Impact score (1-5) | Effort score (1-5) | Priority | Decision (Approve/Defer/Reject) | Comments
- Approval: Reviewer signature + Date + Manager signature + Date

TONE: Đơn giản, khuyến khích, dễ điền — ai cũng có thể dùng.
LENGTH: 1-2 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
