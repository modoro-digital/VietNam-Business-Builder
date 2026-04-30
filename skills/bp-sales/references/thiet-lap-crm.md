### PROMPT 13: CRM Setup Guide (Hướng dẫn thiết lập CRM)

#### Mô tả
Hướng dẫn thiết lập CRM cho đội sales — bao gồm custom fields, pipeline stages, automation rules, dashboards, và data hygiene rules. Đảm bảo CRM phục vụ đúng quy trình bán hàng đã chuẩn hóa, không biến thành "bãi rác data".

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. CRM đang dùng hoặc dự định dùng? (HubSpot / Salesforce / Zoho / Pipedrive / Ybai CRM / Custom)
2. Số users dự kiến? Vai trò? (Admin, Manager, Rep)
3. Pipeline stages đã xác định?
4. Custom fields cần thiết ngoài mặc định? (industry, source, deal type...)
5. Cần automation gì? (auto-assign lead, follow-up reminder, stage notification)
6. Dashboards cần: cho rep, cho manager, cho CEO?
7. Integration cần: email, phone, website, chat, marketing tools?

#### Template gợi ý
Cấu trúc FRM:
- **Phần 1** — CRM Strategy: Mục tiêu sử dụng, adoption metrics, governance
- **Phần 2** — Contact & Company Fields: Required fields, custom fields, field types, picklist values
- **Phần 3** — Pipeline Setup: Stages, probability, required fields per stage, exit criteria
- **Phần 4** — Automation Rules: Lead assignment, task creation, notifications, follow-up sequences
- **Phần 5** — Dashboards: Rep dashboard, Manager dashboard, Executive dashboard — KPIs per role
- **Phần 6** — Data Hygiene: Naming conventions, dedup rules, update frequency, data owner
- **Phần 7** — Integration Map: Email, phone, website, marketing, accounting
- **Phần 8** — User Management: Roles, permissions, training plan
- **Phụ lục**: Field reference table, Automation flowcharts, Dashboard mockups

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo CRM Setup Guide (Hướng dẫn thiết lập CRM).

CONTEXT:
- DN: [Tên] — CRM: [Tên phần mềm]
- Users: [số] — Roles: [Admin / Manager / Rep]
- Pipeline stages: [liệt kê]
- Custom fields: [liệt kê]
- Automation: [liệt kê nhu cầu]
- Integration: [email / phone / website / marketing]

FORMAT:
- Field reference: Bảng Field Name | Type | Required | Picklist Values | Description | Where to fill
- Pipeline config: Bảng Stage | Probability | Required Fields | Exit Criteria | Auto-actions
- Automation rules: Bảng Trigger | Condition | Action | Owner | Priority
- Dashboard specs per role:
  - Rep: My pipeline | My activities | My quota
  - Manager: Team pipeline | Forecast | Rep performance
  - CEO: Revenue trend | Win rate | Pipeline health
- Data hygiene: Bảng Rule | Check frequency | Responsible | Action if violation
- Integration map: Mermaid diagram — CRM ↔ Email ↔ Phone ↔ Website ↔ Marketing
- Training plan: Bảng Week | Topic | Duration | Audience | Format

TONE: Hướng dẫn kỹ thuật — rõ ràng, step-by-step, screenshot-friendly.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
