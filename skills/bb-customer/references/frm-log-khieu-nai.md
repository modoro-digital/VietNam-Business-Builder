### PROMPT 07: Log khiếu nại tracker (Complaint Log & Tracker)

#### Mô tả
Template tracking toàn bộ khiếu nại — ticket ID, severity, category, status, SLA compliance, resolution, root cause. Dùng để theo dõi realtime và phân tích trend hàng tháng/quý.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phân loại khiếu nại theo category nào? (sản phẩm, giao hàng, dịch vụ, thanh toán, thái độ NV)
2. Bao nhiêu cấp severity? (3 hay 4 cấp)
3. SLA target theo severity?
4. Có cần tích hợp với CRM/helpdesk không?
5. Ai review log hàng tuần?

#### Template gợi ý
Cấu trúc FRM:
- **Complaint Log**: Ticket ID | Ngày | KH | Kênh | Category | Severity | Mô tả | Assigned to | Status | SLA deadline | Resolution | Root cause
- **Dashboard summary**: Tổng ticket | Open | In progress | Resolved | Overdue SLA | Avg resolution time
- **Trend analysis**: Monthly — Category breakdown, severity breakdown, SLA compliance rate
- **Root cause analysis**: Pareto chart — top 5 nguyên nhân, tần suất, corrective actions

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Log khiếu nại tracker (Complaint Log & Tracker).

CONTEXT:
- DN: [Tên] — Categories: [liệt kê]
- Severity levels: [3/4] — SLA: [chi tiết per level]
- CRM/Helpdesk: [tên / chưa có]
- Reviewer: [ai] — Tần suất review: [tuần/tháng]

FORMAT:
- Master log: Bảng 15+ cột — Ticket# | Date | Customer | Channel | Category | Severity | Description | Assigned | Status | SLA deadline | SLA met? | Resolution date | Resolution | Root cause | Follow-up
- Status definitions: New 🔵 | In Progress 🟡 | Escalated 🟠 | Resolved 🟢 | Closed ⚫ | Reopened 🔴
- SLA dashboard: Bảng Severity | SLA target | Avg actual | Compliance % | Trend
- Weekly summary: Template — Total | New | Resolved | Open | Overdue | Top category | Top root cause
- Monthly report: Category pie chart guide | Severity distribution | SLA trend | Action items
- Escalation alert: Trigger conditions — auto-escalate khi quá SLA hoặc severity = Critical

TONE: Tracking, analytical, data-driven.
LENGTH: 4-5 trang A4.
```



---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
