# P-PPL-21: KPI cá nhân template (Individual KPI Template)

#### Mô tả
Template KPI cá nhân theo Balanced Scorecard 4 perspectives — giúp NV và Manager thiết lập, theo dõi, và đánh giá KPIs hàng quý/năm. Mỗi KPI có formula, target, trọng số, actual, và score tự tính.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Framework: BSC 4 perspectives hay KPI đơn giản?
2. Số KPIs per người: 5-8 (recommended) hay nhiều hơn?
3. Format SMART đầy đủ không? (Specific, Measurable, Achievable, Relevant, Time-bound)
4. Trọng số: Manager quyết hay NV tự đề xuất?
5. Scoring: Linear (đạt 80% target = 80 điểm) hay Step (≥100% = A, 80-99% = B...)?
6. Có link với OKR công ty không?

#### Template gợi ý
Cấu trúc FRM:
- **Header**: NV | Chức danh | Phòng ban | Kỳ đánh giá | Manager
- **BSC 4 Perspectives**: Financial | Customer | Internal Process | Learning & Growth
- **Mỗi KPI**: Tên | Formula | Unit | Target | Weight | Actual | Score
- **Tổng score**: Weighted average → Rating conversion
- **Comments**: NV tự nhận xét + Manager nhận xét
- **Sign-off**: NV + Manager + HR

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo KPI cá nhân template (Individual KPI Template — BSC).

CONTEXT:
- DN: [Tên]
- Framework: [BSC 4 perspectives / Simple KPI]
- Số KPIs: [5-8]
- Scoring: [Linear / Step]
- Link OKR: [Có/Không]

FORMAT:
- Template 1-2 trang A4
- BSC layout: 4 quadrants — Financial | Customer | Internal Process | Learning
- Mỗi KPI row: # | Perspective | KPI Name | Formula | Unit | Target | Weight% | Actual | Achievement% | Score
- Weight validation: Sum = 100%
- Score formula: Achievement% × Weight = Weighted Score → Sum all = Total
- Rating conversion: Total ≥90 = A (Outstanding) | 80-89 = B (Good) | 70-79 = C (Meets) | 60-69 = D (Below) | <60 = E (Poor)
- SMART checklist: Mỗi KPI tự kiểm tra 5 tiêu chí SMART ☐
- Example KPIs: 2-3 ví dụ per perspective cho vị trí Sales/Marketing/Operations

TONE: Performance management, analytical, dễ điền.
LENGTH: 2-3 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
