# PROMPT 16: Crisis Management Plan (Quy trình xử lý khủng hoảng)

#### Mô tả
Playbook xử lý khủng hoảng — cho các kịch bản: khủng hoảng truyền thông, sự cố sản phẩm, rò rỉ dữ liệu, kiện tụng, thiên tai, mất key person. Mỗi kịch bản có protocol riêng, đảm bảo phản ứng nhanh & nhất quán.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Đã từng gặp khủng hoảng chưa? (loại gì, xử lý thế nào)
2. Có PR/truyền thông nội bộ hay outsource?
3. Ai là Crisis Commander (người chỉ huy khủng hoảng)?
4. Có Luật sư thường trực không?
5. Kênh truyền thông chính cần quản lý khi khủng hoảng?
6. Kịch bản nào lo ngại nhất? (VD: product recall, data breach, negative viral, legal...)

#### Template gợi ý
Cấu trúc SOP:
- **Crisis Classification** — Level 1 (minor) → 2 (moderate) → 3 (severe) → 4 (existential)
- **Crisis Team** — Roles & Contact: Commander, Spokesperson, Legal, Ops, HR, IT, Communications
- **Communication Cascade** — Ai gọi ai, trong bao lâu, qua kênh nào — "First 60 minutes" protocol
- **Scenario Playbooks** — 6-8 kịch bản, mỗi kịch bản có:
  - Trigger / Indicators
  - Severity level
  - Immediate actions (First 1 hour)
  - Short-term actions (24-72 hours)
  - Communication templates (internal, customer, media, authority)
  - Recovery steps
- **Holding Statements** — Template statements dùng ngay khi chưa có thông tin đầy đủ
- **Post-Crisis Review** — Template After-Action Review (AAR)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Crisis Management Plan.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Crisis history: [mô tả hoặc "chưa có"]
- PR: [nội bộ / agency: tên]
- Crisis Commander: [chức danh]
- Luật sư: [Có/Không — tên nếu có]
- Kênh truyền thông: [liệt kê: Facebook, website, báo chí...]
- Kịch bản lo ngại: [liệt kê top 3]

FORMAT:
- Crisis Level matrix: Level | Description | Authority | Response time | Communication scope
- Team contact card: Role | Name | Phone | Email | Backup
- "First 60 Minutes" checklist: 10 bước bắt buộc
- 6-8 Scenario playbooks: Mỗi kịch bản 1-2 trang
- Communication templates: Internal memo, Customer email, Press statement, Social media post
- Holding statement library: 5 generic statements dùng được ngay
- AAR template: What happened | What went well | What went wrong | Improvements | Owner

TONE: Emergency protocol — clear, decisive, no ambiguity.
LENGTH: 15-20 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
