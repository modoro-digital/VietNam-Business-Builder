# P-PPL-04: Headcount Plan (Kế hoạch Nhân sự)

#### Mô tả
Kế hoạch nhân sự tổng thể — hiện tại bao nhiêu, cần tuyển bao nhiêu, khi nào, budget bao nhiêu. Liên kết trực tiếp với chiến lược kinh doanh và ngân sách.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Headcount hiện tại theo phòng ban?
2. Kế hoạch kinh doanh 12 tháng tới? (tăng trưởng doanh thu → cần thêm nhân sự?)
3. Tỷ lệ nghỉ việc (turnover) hiện tại?
4. Budget nhân sự (payroll) hiện tại % doanh thu?
5. Có kế hoạch mở chi nhánh / sản phẩm mới cần team mới?

#### Template gợi ý
Cấu trúc MAN:
- **Current State**: Bảng phòng ban × HC hiện tại × Chi phí
- **Gap Analysis**: So sánh HC hiện tại vs HC cần thiết theo chiến lược
- **Hiring Plan**: Timeline tuyển theo quý — vị trí | dept | Q1 | Q2 | Q3 | Q4 | Priority
- **Budget Impact**: Payroll forecast — hiện tại + incremental + total
- **Turnover Forecast**: Dự báo nghỉ việc + replacement plan
- **Ratios**: Revenue per employee, Cost per hire, Time to fill

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Headcount Plan (Kế hoạch Nhân sự).

CONTEXT:
- DN: [Tên] — HC hiện tại: [số] — Per dept: [chi tiết]
- Kế hoạch tăng trưởng: [mô tả]
- Turnover: [%/năm]
- Payroll/Revenue ratio: [%]
- Mở rộng: [chi nhánh / sản phẩm mới nếu có]

FORMAT:
- Current state: Dept | Current HC | Avg Salary | Total Cost | Revenue/employee
- Gap analysis: Dept | Current | Needed | Gap | Priority | Justification
- Hiring timeline: Gantt-style Q1-Q4 × vị trí
- Budget forecast: Monthly payroll × 12 tháng → Total + YoY change
- Turnover model: Dept | Rate | Expected exits | Replacement cost
- Summary KPIs: Total HC plan | New hires | Budget impact | Cost per hire

TONE: Chiến lược, data-driven, liên kết với business plan.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
