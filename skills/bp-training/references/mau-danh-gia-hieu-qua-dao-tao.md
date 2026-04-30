### PROMPT 07: Training Evaluation Form (Mẫu Đánh giá Hiệu quả Đào tạo)

#### Mô tả
Bộ form đánh giá hiệu quả đào tạo theo mô hình Kirkpatrick 4 cấp — Level 1: Reaction (học viên hài lòng?), Level 2: Learning (học được gì?), Level 3: Behavior (áp dụng được chưa?), Level 4: Results (kết quả kinh doanh?). Mỗi cấp có form và timing riêng.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện tại có đánh giá đào tạo không? Ở mức nào? (chỉ satisfaction survey / không có)
2. Muốn đánh giá đến cấp nào? (L1-L2 cho hầu hết / L3-L4 cho chương trình quan trọng)
3. Ai phát và thu form? (trainer / HR / LMS tự động)
4. Format: giấy / Google Forms / LMS / phần mềm?
5. Có cần so sánh pre-test vs post-test không?
6. Manager có tham gia đánh giá behavior change không?

#### Template gợi ý
Cấu trúc FRM:
- **Phần 1** — Hướng dẫn sử dụng: Mỗi level dùng khi nào, ai điền, timeline
- **Phần 2** — Level 1 — Reaction Form: Satisfaction survey ngay sau đào tạo
- **Phần 3** — Level 2 — Learning Assessment: Pre-test / Post-test / Knowledge check
- **Phần 4** — Level 3 — Behavior Change Form: Manager + Self-assessment sau 30-90 ngày
- **Phần 5** — Level 4 — Results Measurement: Business KPIs trước vs sau đào tạo
- **Phần 6** — Summary Dashboard: Tổng hợp 4 levels cho mỗi chương trình
- **Phụ lục**: Scale reference, Sample analysis report

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Training Evaluation Form (Mẫu Đánh giá Hiệu quả Đào tạo).

CONTEXT:
- DN: [Tên] — Đánh giá hiện tại: [mô tả mức hiện tại]
- Đánh giá đến cấp: [L1-L2 hầu hết / L3-L4 chương trình lớn]
- Format: [giấy / digital / LMS]
- Manager tham gia: [Có/Không]
- Pre/Post test: [Có/Không]

FORMAT:
- Usage guide: Bảng Level | Timing | Who fills | Who collects | Purpose
- Level 1 — Reaction Form (ngay sau đào tạo):
  - Rating scale: 1-5 Likert — 8-12 câu
  - Categories: Content relevance | Trainer quality | Materials | Logistics | Overall satisfaction
  - Open questions: "Điều hữu ích nhất?" | "Cần cải thiện?" | "Đề xuất?"
  - NPS question: "Bạn có giới thiệu khóa này cho đồng nghiệp? (0-10)"
- Level 2 — Learning Assessment:
  - Pre-test: 10 câu MCQ/True-False — đo baseline
  - Post-test: 10 câu tương đương — đo knowledge gain
  - Learning gain formula: (Post - Pre) / (Max - Pre) × 100%
  - Practical assessment: Rubric — Criteria | Excellent | Good | Needs Improvement | Not Demonstrated
- Level 3 — Behavior Change (30-90 ngày sau):
  - Self-assessment: "Tôi đã áp dụng kỹ năng X..." — Rating 1-5 + Evidence/Example
  - Manager assessment: "NV đã thể hiện hành vi X..." — Rating 1-5 + Observation
  - Application rate: % kỹ năng đã áp dụng / tổng kỹ năng học
  - Barriers: "Điều gì cản trở việc áp dụng?" — checklist + open
- Level 4 — Results (3-6 tháng sau):
  - KPI tracking: Metric | Before training | After training | Change % | Attribution %
  - Business impact examples: Revenue, productivity, quality, customer satisfaction, employee retention
- Summary dashboard: Program | L1 Score | L2 Gain % | L3 Application % | L4 Impact | ROI estimate
- Trend analysis: Program × Quarter → Score trends

TONE: Đo lường khoa học, dễ điền, actionable insights.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
