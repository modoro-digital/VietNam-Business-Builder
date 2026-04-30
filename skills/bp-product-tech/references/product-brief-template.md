### PROMPT 04: Product Brief Template (Mẫu Brief Sản phẩm)

#### Mô tả
Template chuẩn để mô tả một sản phẩm/tính năng mới trước khi bắt đầu phát triển. Brief là tài liệu alignment giữa Product, Dev, Design, Marketing — đảm bảo mọi người cùng hiểu "chúng ta đang xây gì, cho ai, tại sao".

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Brief cho loại gì? (SP hoàn toàn mới / tính năng mới / cải tiến SP hiện tại)
2. Ai viết brief? (PM / Founder / đội nào?)
3. Ai đọc và duyệt brief?
4. Có cần phần technical spec trong brief hay tách riêng?
5. Mức độ chi tiết mong muốn? (1 trang / 3-5 trang)

#### Template gợi ý
Cấu trúc FRM:
- **Header** — Tên SP/Feature, Author, Date, Status (Draft/Review/Approved)
- **Problem Statement** — Vấn đề gì? Ai gặp? Impact bao lớn?
- **Target Customer** — Persona, segment, Jobs-to-be-Done
- **Proposed Solution** — Mô tả high-level, key features, differentiators
- **Success Metrics** — KPIs đo lường thành công: adoption, revenue, NPS
- **Scope** — In scope / Out of scope / Future considerations
- **Competitive Landscape** — Đối thủ giải quyết vấn đề này thế nào?
- **Go-to-Market** — Pricing direction, channel, messaging (high-level)
- **Timeline & Resources** — Estimate effort, team needed, milestones
- **Risks & Assumptions** — Giả định cần validate, rủi ro chính
- **Approval** — Sign-off section

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Product Brief Template.

CONTEXT:
- DN: [Tên] — Loại brief: [SP mới / Feature / Cải tiến]
- Người viết: [PM / Founder / Team]
- Người duyệt: [chức danh]
- Technical spec: [Kèm / Tách riêng]
- Độ dài: [1 trang / 3-5 trang]

FORMAT:
- 1 template fillable — mỗi section có [placeholder] + hướng dẫn ngắn
- Problem: Framework — [Ai] gặp vấn đề [gì] khi [tình huống] dẫn đến [hậu quả]
- Solution: Feature list dạng bảng — Feature | Description | Priority (P0/P1/P2)
- Metrics: Bảng KPI | Definition | Target | Measurement method
- Scope: 2 cột — ✅ In Scope | ❌ Out of Scope
- Timeline: Milestone | Date | Owner | Dependencies
- Risk register: Risk | Probability | Impact | Mitigation
- Approval: Role | Name | Date | Signature | Comments

TONE: Structured, concise, actionable — dễ điền, dễ đọc.
LENGTH: 3-5 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
