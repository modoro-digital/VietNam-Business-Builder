### PROMPT 10: Training ROI Report (Báo cáo ROI Đào tạo)

#### Mô tả
Báo cáo đo lường hiệu quả đầu tư đào tạo — tổng hợp chi phí, lợi ích (tangible & intangible), tính ROI, và đề xuất cải thiện. Sử dụng Phillips ROI Methodology (mở rộng Kirkpatrick Level 5). Báo cáo này giúp CEO/CFO thấy đào tạo là đầu tư chứ không phải chi phí.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Báo cáo cho chương trình cụ thể hay tổng hợp cả năm?
2. Tổng chi phí đào tạo? (trainer, venue, materials, lost productivity, travel, technology)
3. Lợi ích đo lường được: tăng doanh thu / giảm chi phí / giảm turnover / tăng năng suất?
4. Có dữ liệu baseline (trước đào tạo) không?
5. Isolation method: Control group / Trend analysis / Expert estimation?
6. Audience báo cáo: CEO/CFO / HR Director / Board?

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — ROI headline number, key findings, recommendations
- **Phần 1** — Program Overview: Mô tả chương trình, mục tiêu, participants
- **Phần 2** — Cost Analysis: Tất cả chi phí fully-loaded
- **Phần 3** — Benefits Analysis: Tangible & intangible benefits
- **Phần 4** — ROI Calculation: Formula, isolation, conversion to monetary value
- **Phần 5** — Kirkpatrick Results: L1-L4 summary
- **Phần 6** — Intangible Benefits: Không quy đổi tiền nhưng có giá trị
- **Phần 7** — Recommendations: Cải thiện, scale, hoặc discontinue
- **Phụ lục**: Detailed calculations, Data sources, Methodology notes

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Training ROI Report (Báo cáo ROI Đào tạo).

CONTEXT:
- DN: [Tên] — Báo cáo cho: [chương trình cụ thể / tổng hợp năm]
- Tổng chi phí đào tạo: [số]
- Lợi ích đo được: [tăng DT / giảm CP / giảm turnover / tăng NS]
- Baseline data: [Có/Không]
- Isolation method: [control group / trend / expert estimate]
- Audience: [CEO / CFO / HR Director / Board]

FORMAT:
- Executive summary: 1 trang — ROI %, BCR, key findings, top 3 recommendations
- Cost analysis: Fully-loaded cost table
  - Direct: Trainer fees | Materials | Venue | Technology | Certification
  - Indirect: Participant time (salary × hours) | Manager time | Travel | Admin
  - Total cost per participant = Total / # participants
- Benefits analysis:
  - Tangible: Bảng Benefit | Measurement | Before | After | Change | Monetary value | Confidence %
  - Isolation: Method used per benefit — Attribution % to training
  - Annualized: Project benefits over 12 months
- ROI calculation:
  - BCR (Benefit-Cost Ratio) = Total Benefits / Total Costs
  - ROI % = (Net Benefits / Total Costs) × 100%
  - Payback period = Total Costs / Monthly benefit
  - Show calculation step-by-step
- Kirkpatrick summary: Bảng Level | Metric | Result | Target | Status
  - L1: Satisfaction score | L2: Knowledge gain % | L3: Application rate % | L4: Business impact
- Intangible benefits: List — Employee engagement, morale, teamwork, innovation, employer brand
- Sensitivity analysis: Bảng Scenario | Assumption change | Impact on ROI — Best / Base / Worst case
- Recommendations:
  - Scale: Programs with high ROI → Expand audience
  - Improve: Programs with low L3 → Add follow-up coaching
  - Discontinue: Programs with negative ROI → Replace or redesign
- Trend: Year-over-year training investment vs ROI trend
- Benchmark: Industry average training spend per employee, ROI benchmarks

TONE: Executive, data-driven, kết luận rõ ràng — đào tạo = đầu tư.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
