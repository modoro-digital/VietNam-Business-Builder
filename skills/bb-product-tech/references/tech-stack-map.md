### PROMPT 06: Tech Stack Map (Bản đồ Công nghệ)

#### Mô tả
Tài liệu tổng hợp toàn bộ công nghệ, phần mềm, nền tảng, và hạ tầng IT mà DN đang sử dụng. Phân loại theo chức năng, ghi nhận license, chi phí, owner, và tình trạng. Là "bản đồ" để CTO/IT quản lý và lập kế hoạch technology investment.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Liệt kê tất cả phần mềm/tool đang dùng? (SaaS, on-premise, custom-built)
2. Hosting/Infrastructure? (AWS / GCP / Azure / On-premise / VPS / Shared hosting)
3. Phần mềm kế toán, CRM, ERP, HR đang dùng?
4. Communication tools? (Slack, Teams, Zalo, Email)
5. Tổng chi phí IT/tháng? License costs?
6. Có tech debt / legacy system cần thay thế không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Architecture Overview: Sơ đồ tổng quan hệ thống
- **Phần 2** — Stack by Category: Frontend, Backend, Database, Infrastructure, DevOps, SaaS tools
- **Phần 3** — Tool Inventory: Bảng chi tiết từng tool — tên, category, license, cost, users, owner, status
- **Phần 4** — Integration Map: Tool A ↔ Tool B — API / Zapier / manual
- **Phần 5** — Cost Summary: Chi phí IT tổng hợp, cost per employee
- **Phần 6** — Tech Debt & Modernization Plan: Legacy → Target, timeline
- **Phần 7** — Review Cadence: Tần suất review stack, renewal calendar
- **Phụ lục**: Tool evaluation criteria, Vendor comparison template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Tech Stack Map (Bản đồ Công nghệ).

CONTEXT:
- DN: [Tên] — Quy mô IT: [số người dùng]
- Hosting: [AWS / GCP / Azure / On-prem / VPS]
- Tools chính: [liệt kê top 10]
- Chi phí IT: [tổng/tháng]
- Tech debt: [mô tả]

FORMAT:
- Architecture diagram: Mermaid — Layer-based (Frontend → API → Backend → DB → Infra)
- Tool inventory: Bảng 10+ cột — Tool | Category | Type (SaaS/On-prem/Custom) | License | Cost/month | Users | Owner | Contract end | Status | Notes
- Integration map: Mermaid flowchart — Tool connections
- Cost dashboard: Category | Monthly | Annual | % Total IT | Cost/User
- Renewal calendar: Tool | Contract end | Auto-renew? | Action needed | Owner
- Tech debt register: System | Issue | Impact | Replacement | Timeline | Cost
- Evaluation scorecard: Criteria | Weight | Tool A | Tool B → Score

TONE: Technical, inventory-style, dễ tra cứu và cập nhật.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
