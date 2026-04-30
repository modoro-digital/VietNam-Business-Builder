### PROMPT 05: SOP Sales Process (Quy trình bán hàng)

#### Mô tả
Quy trình chuẩn hóa toàn bộ hoạt động bán hàng — từ tiếp nhận lead đến chốt đơn và bàn giao khách hàng. Đảm bảo mọi sales rep đều bán hàng theo cùng một quy trình đã được chứng minh hiệu quả, giảm phụ thuộc vào cá nhân.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Nguồn lead chính? (Marketing, referral, outbound, event, website)
2. Tiêu chí qualify lead? (BANT / MEDDIC / CHAMP / custom?)
3. Quy trình bán hiện tại có bao nhiêu bước? Mô tả?
4. Thời gian trung bình từng bước? Toàn bộ cycle?
5. Có handover giữa các team không? (SDR → AE → AM → CS?)
6. Công cụ hỗ trợ? (CRM, email, phone, chat?)
7. Tỷ lệ chuyển đổi từng bước hiện tại?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Thuật ngữ**: Lead, MQL, SQL, Opportunity, Deal, Won, Lost
- **Tổng quan quy trình**: 7 bước — Lead → Qualify → Demo/Consult → Proposal → Negotiate → Close → Handover
- **Chi tiết từng bước**: Mục tiêu, hành động cụ thể, output, tiêu chí chuyển bước, timeline, tools
- **Qualification Framework**: BANT hoặc MEDDIC — checklist áp dụng
- **Handover Protocol**: SDR → AE, AE → AM, Sales → CS
- **Escalation Rules**: Khi nào cần manager/director tham gia
- **Tracking & Reporting**: CRM stages, pipeline review cadence
- **Phụ lục**: Qualification checklist, Stage criteria, Handover template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Sales Process (Quy trình bán hàng).

CONTEXT:
- DN: [Tên] — Mô hình: [B2B / B2C / SaaS / Dịch vụ]
- Nguồn lead: [Marketing / Referral / Outbound / Event / Website]
- Qualification: [BANT / MEDDIC / CHAMP / Custom]
- Số bước hiện tại: [số] — Sales cycle: [ngày]
- Team structure: [SDR + AE + AM / All-in-one]
- CRM: [Tên phần mềm]

FORMAT:
- Flowchart tổng: Mermaid — 7 bước chính + decision points
- Per-step detail: Bảng Bước | Mục tiêu | Actions | Output | Exit Criteria | Timeline | Owner
- Qualification checklist: BANT/MEDDIC — Tiêu chí | Câu hỏi | Đạt/Không | Score
- Conversion funnel: Bảng Stage | Leads In | Converted | Rate | Avg Days | Bottleneck
- Handover template: Bảng thông tin cần chuyển giao giữa các role
- Escalation matrix: Tình huống | Escalate to | Timeline | Expected action
- Weekly pipeline review agenda: 5 mục check cố định

TONE: SOP chuẩn — step-by-step, rõ ràng, actionable.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
