# PROMPT 17: Business Continuity Plan — BCP (Kế hoạch duy trì kinh doanh liên tục)

#### Mô tả
Kế hoạch đảm bảo DN tiếp tục vận hành khi xảy ra sự cố lớn: mất trụ sở, mất hệ thống IT, mất key person, thiên tai, dịch bệnh. Focus: Recovery Time Objective (RTO), Recovery Point Objective (RPO), workaround procedures.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Business-critical processes? (top 5 quy trình không thể dừng)
2. Hệ thống IT critical? (website, CRM, email, ERP, payment...)
3. Có backup site / remote work capability không?
4. Recovery targets: Bao lâu chấp nhận được downtime? (RTO)
5. Data backup: Tần suất, location, recovery tested?
6. Key person dependencies: Ai mà nếu vắng thì bị tê liệt?

#### Template gợi ý
Cấu trúc SOP:
- **Business Impact Analysis (BIA)** — Bảng quy trình × impact nếu dừng × RTO/RPO
- **Critical Function Recovery** — Per function: Primary site → Backup site → Manual workaround
- **IT Disaster Recovery** — System × RTO × RPO × Backup method × Recovery steps
- **People Continuity** — Key person × Backup person × Cross-training status × Succession plan
- **Communication Plan** — Thông báo nhân viên, KH, đối tác khi kích hoạt BCP
- **BCP Activation Protocol** — Ai quyết định kích hoạt, trigger criteria, escalation
- **Testing Schedule** — Tabletop exercise, walkthrough, full test — annual calendar

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Business Continuity Plan (BCP).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- Critical processes: [liệt kê top 5]
- IT systems: [liệt kê critical systems]
- Remote work: [Có/Không] — Capability: [%]
- RTO acceptable: [giờ/ngày]
- Data backup: [method / frequency / location]
- Key person risks: [liệt kê]

FORMAT:
- BIA table: Process | Owner | Impact if down 1h/1d/1w | RTO | RPO | Priority
- Recovery procedures: Per critical function, step-by-step
- IT DR plan: System | RTO | RPO | Backup | Recovery Steps | Last Tested
- People matrix: Role | Primary | Backup | Cross-training | Succession
- Communication tree: Flowchart — who notifies whom
- Activation checklist: 15-step protocol
- Test schedule: Type | Frequency | Last Done | Next Due | Owner

TONE: Operational resilience — thorough, practical, testable.
LENGTH: 12-18 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
