### PROMPT 10: Customer Health Score (Điểm sức khỏe KH)

#### Mô tả
Template đo lường "sức khỏe" quan hệ KH — scoring dimensions (usage, engagement, support, payment, NPS), trọng số, công thức tính, ngưỡng cảnh báo, và hành động theo từng mức score. Công cụ chủ động phát hiện KH có nguy cơ churn trước khi quá muộn.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Data nào đang có? (usage logs, login frequency, support tickets, payment history, NPS)
2. Đâu là dấu hiệu sớm nhất của KH sắp churn?
3. Có CRM/CS platform tracking được health score không?
4. Bao nhiêu KH cần monitor? Tần suất cập nhật score?
5. Ai sẽ action khi health score giảm?

#### Template gợi ý
Cấu trúc FRM:
- **Scoring Dimensions**: Usage (30%) | Engagement (20%) | Support (20%) | Payment (15%) | NPS/Feedback (15%)
- **Sub-metrics per dimension**: 3-5 metrics mỗi dimension, scoring 1-10
- **Calculation**: Weighted average → Score 0-100
- **Thresholds**: Green (≥70) — Healthy | Yellow (50-69) — At Risk | Red (<50) — Critical
- **Actions per range**: Green → nurture/upsell | Yellow → proactive outreach | Red → save team intervention

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Customer Health Score Template.

CONTEXT:
- DN: [Tên] — Data available: [usage / engagement / support / payment / NPS]
- Churn signals: [mô tả]
- Platform: [CRM / CS tool / manual]
- Số KH monitor: [số] — Update frequency: [daily / weekly / monthly]
- Action owner: [CS Manager / CSM / AI auto-alert]

FORMAT:
- Scoring model: Bảng Dimension | Weight | Sub-metrics | Scoring rule (1-10) | Data source | Update freq
- Calculation example: Walkthrough 1 KH cụ thể — input → weighted score → final score
- Threshold matrix: Score range | Status | Color | Description | Required action | Timeline | Owner
- Dashboard view: Customer | Score | Trend (↑↓→) | Status | Last contact | Next action | CSM
- Alert system: Auto-trigger khi score giảm ≥15 points/month hoặc xuống Red
- Cohort analysis: Score distribution per tier | Average score by segment | Trend over time
- Playbook per status: Green (3 actions) | Yellow (5 actions) | Red (7 actions) — scripts + offers

TONE: Analytical, proactive, early-warning focused.
LENGTH: 5-7 trang A4.
```



---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
