### PROMPT 16: Marketing Automation Playbook

#### Mô tả
Playbook triển khai hệ thống Marketing Automation — định nghĩa các automation flow chuẩn (welcome, lead nurturing, abandoned cart, win-back, post-purchase), segmentation rules, lead scoring, và tích hợp với CRM/Sales. Mục tiêu: scale marketing không cần scale headcount.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Công cụ Marketing Automation đang dùng/dự kiến: HubSpot / Mailchimp / Klaviyo / Ybai / Active Campaign / khác?
2. CRM hiện tại: Salesforce / HubSpot / Zoho / Excel / khác?
3. Loại business: B2B (long sales cycle) hay B2C (short cycle)?
4. Số lượng leads/contacts hiện có?
5. Volume email/tháng?
6. Các flow muốn ưu tiên: Welcome / Nurture / Abandoned cart / Win-back / Post-purchase?
7. Đang gặp pain point gì với marketing thủ công?

#### Template gợi ý
Cấu trúc MAN:
- **Marketing Automation Strategy**: Why automate, mục tiêu, ROI expectation
- **Tech Stack & Integration**: MA tool ↔ CRM ↔ Website ↔ Ads ↔ E-commerce
- **Data Architecture**: Database structure, custom fields, tags, lists vs segments
- **Segmentation Framework**: Demographic / Behavioral / Lifecycle / RFM
- **Lead Scoring Model**: Demographic score + Behavioral score → MQL threshold
- **Core Automation Flows**: 7 flow chuẩn — mỗi flow có goal, trigger, sequence, exit
  - Welcome series (3-5 email)
  - Lead nurturing (educate → trust → convert)
  - Abandoned cart (e-commerce)
  - Post-purchase (onboarding + upsell)
  - Win-back (re-engagement)
  - Birthday/Anniversary
  - Re-permission (compliance)
- **A/B Testing Framework**: Subject line, send time, content, CTA
- **Compliance**: GDPR/PDP Vietnam (Nghị định 13/2023), opt-in, unsubscribe
- **KPI & Optimization**: Open rate, CTR, conversion, churn, LTV impact
- **Governance**: Frequency cap, suppression list, brand voice rules

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Marketing Automation Playbook.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- MA tool: [HubSpot / Mailchimp / Klaviyo / Ybai / khác]
- CRM: [Salesforce / HubSpot / Zoho / Excel]
- Business model: [B2B / B2C]
- Database size: [n contacts]
- Email volume: [n/tháng]
- Priority flows: [list]

FORMAT:
- Tech stack diagram: Sơ đồ tích hợp giữa các tool
- Data model: Bảng Field | Type | Source | Use case
- Segmentation matrix: 5-7 segment chính + criteria
- Lead scoring: Bảng Action | Points + threshold MQL/SQL
- 7 flow blueprints: mỗi flow 1 trang — Goal | Trigger | Sequence diagram | Wait time | Exit | KPI
- A/B test plan: Bảng Test | Hypothesis | Variant A/B | Sample size | Duration
- Compliance checklist: GDPR + Nghị định 13/2023 (Bảo vệ dữ liệu cá nhân VN)
- KPI dashboard: 8-10 metric chính + benchmark ngành
- Governance rules: Frequency cap, suppression, brand voice
- Roadmap triển khai: 90 ngày — Week 1-12 task breakdown

TONE: Thực tiễn, có ví dụ cụ thể, kèm template content.
LENGTH: 12-15 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
