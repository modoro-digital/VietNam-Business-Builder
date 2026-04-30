### PROMPT 08: Quarterly Business Review Template (Đánh giá Kinh doanh Quý)

#### Mô tả
Mẫu Quarterly Business Review (QBR) — đánh giá toàn diện hiệu suất kinh doanh theo quý, so sánh actual vs plan, phân tích nguyên nhân, rút bài học, và điều chỉnh kế hoạch quý tiếp. QBR là cơ chế "course correction" quan trọng nhất, kết hợp backward-looking (review) với forward-looking (planning).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ai tham gia QBR? (BGĐ only / + Trưởng phòng / toàn công ty)
2. Thời lượng QBR? (half-day / full-day / 2 hours)
3. Mỗi phòng ban trình bày riêng hay chỉ tổng hợp?
4. Có scoring/rating cho mỗi objective không?
5. OKR system: dùng OKR hay KPI-based?
6. Output QBR: action plan / updated forecast / revised priorities?

#### Template gợi ý
Cấu trúc FRM:
- **Phần 1** — Quarter Summary: Headline results, key achievements, key misses
- **Phần 2** — Financial Review: Revenue, P&L, cash flow vs plan + variance analysis
- **Phần 3** — OKR/KPI Scorecard: Objective × Key Result → Score + commentary
- **Phần 4** — Department Reviews: Each dept 1-2 pages — wins, misses, lessons, asks
- **Phần 5** — Customer & Market: NPS, churn, market trends, competitive moves
- **Phần 6** — Lessons Learned: Start / Stop / Continue
- **Phần 7** — Next Quarter Plan: Priorities, OKRs, resource needs, risks
- **Phụ lục**: Detailed department data, customer feedback summary

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quarterly Business Review Template (QBR).

CONTEXT:
- DN: [Tên] — QBR participants: [BGĐ / + Trưởng phòng / toàn công ty]
- Thời lượng: [X giờ] — Format: [presentation / workshop / hybrid]
- OKR/KPI system: [OKR / KPI / hybrid]
- Dept presentations: [Có/Không]
- Output: [action plan / updated forecast / revised priorities]

FORMAT:
- Quarter headline: 1 slide — Q[X] [Year] | Revenue: [actual vs target] | Key metric 1-3 | Overall rating (🟢🟡🔴)
- Financial review:
  - Revenue: Actual | Target | % | vs Prior Q | vs YoY — by product/segment
  - P&L: Revenue → Gross Profit → EBITDA → Net Income — variance waterfall
  - Cash flow: Opening → Operating → Investing → Financing → Closing
  - Unit economics: CAC | CLV | LTV:CAC | Payback period — trend
- OKR/KPI Scorecard:
  - Company OKRs: Objective | KR1 score | KR2 score | KR3 score | Overall | Commentary
  - Scoring: 0-0.3 (🔴 Miss) | 0.4-0.6 (🟡 Progress) | 0.7-1.0 (🟢 Achieved)
  - Quarter-over-quarter trend per OKR
- Department review template (per dept):
  - Dept KPIs: 5-8 metrics — Actual vs Target | Status
  - Top 3 wins: What | Impact | Replicable?
  - Top 3 misses: What | Root cause | Action
  - Resource needs: Ask | Justification | Priority
- Customer & Market:
  - NPS/CSAT trend: Score | Trend | Top feedback themes
  - Churn analysis: Rate | Revenue impact | Reasons | Save rate
  - Market intel: Competitive moves | Industry trends | Regulatory changes
- Lessons Learned:
  - Start doing: Activity | Expected impact | Owner
  - Stop doing: Activity | Why | Alternative
  - Continue doing: Activity | Why working | How to amplify
- Next Quarter Plan:
  - Updated OKRs/priorities: Objective | Key Results | Owner | Dependencies
  - Resource allocation: Dept | Headcount | Budget | Key initiatives
  - Risk register: Risk | Probability | Impact | Mitigation | Owner
  - Key dates/milestones: Date | Event | Owner | Dependencies

TONE: Strategic, honest (celebrate wins AND confront misses), action-oriented.
LENGTH: 10-15 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
