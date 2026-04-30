# PROMPT 18: Scenario Planning (Hoạch định kịch bản)

#### Mô tả
3 kịch bản chiến lược: Lạc quan (Best Case), Cơ sở (Base Case), Bi quan (Worst Case). Mỗi kịch bản có giả định, tác động, action plan, financial projection. Giúp DN chuẩn bị cho nhiều tương lai có thể xảy ra.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Biến số chính ảnh hưởng DN nhất? (thị trường, quy định, công nghệ, cạnh tranh, kinh tế vĩ mô)
2. Financial projections hiện tại (base case)?
3. Best case scenario theo anh là gì? (what if everything goes right)
4. Worst case scenario? (what keeps you up at night)
5. Trigger points: Dấu hiệu nào cho biết đang đi vào kịch bản nào?
6. Có pivot options nào? (nếu kịch bản xấu xảy ra, DN có thể chuyển hướng thế nào?)

#### Template gợi ý
Cấu trúc RPT:
- **Key Uncertainties** — 3-5 biến số chính, mỗi biến có range (high/base/low)
- **3 Scenarios** — Mỗi kịch bản 2-3 trang:
  - Narrative: Mô tả bằng lời — "Năm 2027, thị trường..."
  - Assumptions: Bảng biến số × giá trị
  - Impact on business: Revenue, cost, market share, headcount
  - Financial projection: P&L summary
  - Strategic response: Hành động cụ thể
  - Trigger indicators: Dấu hiệu đang vào kịch bản này
- **Comparison Dashboard** — 3 scenarios side-by-side: Key metrics × Best/Base/Worst
- **Decision Framework** — "If [trigger], then [action]" rules
- **Review Cadence** — Quarterly update assumptions + check triggers

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Scenario Planning.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Key variables: [liệt kê 3-5: VD market growth, regulation, competition, technology, economy]
- Base case projections: Revenue [số] | EBITDA [số] | Headcount [số]
- Best case vision: [mô tả]
- Worst case fear: [mô tả]
- Pivot options: [liệt kê]
- Time horizon: [1-3 năm]

FORMAT:
- Scenario matrix: Variable × Best/Base/Worst values
- 3 scenario narratives: 1-2 trang mỗi kịch bản, storytelling format
- Financial comparison: Bảng 3 cột — Revenue, EBITDA, Cash, Headcount, Market Share
- Trigger dashboard: Indicator | Best trigger | Worst trigger | Current | Trend
- Decision rules: "IF indicator > X THEN activate Plan B"
- Quarterly review checklist: 10 items to re-evaluate

TONE: Strategic foresight — thoughtful, balanced, preparing not predicting.
LENGTH: 10-15 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
