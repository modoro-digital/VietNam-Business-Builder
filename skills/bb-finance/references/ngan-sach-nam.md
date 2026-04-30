# P-FIN-06: Ngân sách năm Budget (Annual Budget)

#### Mô tả
Ngân sách năm tổng hợp — lập budget doanh thu và chi phí theo phòng ban, theo quý. Bao gồm quy trình lập, phê duyệt, theo dõi variance, và điều chỉnh ngân sách.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Năm tài chính? (theo năm dương lịch hay khác?)
2. Phương pháp lập ngân sách? (Top-down / Bottom-up / Zero-based)
3. Bao nhiêu phòng ban/trung tâm chi phí cần budget riêng?
4. Có revenue budget không hay chỉ expense budget?
5. Tần suất review variance? (Monthly / Quarterly)
6. Quy trình lập: Timeline từ khi bắt đầu đến khi HĐQT duyệt?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Hướng dẫn lập ngân sách: Phương pháp, assumptions, timeline
- **Phần 2** — Revenue Budget: Theo sản phẩm/kênh × 12 tháng
- **Phần 3** — Expense Budget tổng hợp: COGS + SGA × 12 tháng
- **Phần 4** — Departmental Budget: Mỗi phòng ban 1 bảng chi tiết
- **Phần 5** — CapEx Budget: Đầu tư tài sản, dự án
- **Phần 6** — Budget Summary: P&L dự kiến, Key ratios
- **Phần 7** — Variance Tracking: Template theo dõi Budget vs Actual
- **Phần 8** — Quy trình phê duyệt & Điều chỉnh giữa kỳ
- **Phụ lục**: Template budget per department, Assumption log

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Ngân sách năm (Annual Budget).

CONTEXT:
- DN: [Tên] — Năm tài chính: [năm]
- Phương pháp: [Top-down / Bottom-up / Zero-based]
- Số trung tâm chi phí: [số] — Danh sách: [liệt kê]
- Revenue budget: [Có/Không]
- Variance review: [Monthly / Quarterly]

FORMAT:
- Revenue budget: Sản phẩm/Kênh × Q1-Q2-Q3-Q4 × Monthly breakdown
- Expense budget: Khoản CP × 12 tháng × Phòng ban
- Departmental template: Budget line | Annual | Q1 | Q2 | Q3 | Q4 | Notes
- P&L budget: Revenue → COGS → Gross Profit → SGA → EBITDA → Net Income
- Variance tracker: Budget | Actual | Variance $ | Variance % | Explanation
- Key assumptions log: Assumption | Source | Sensitivity | Impact if wrong
- Approval workflow: Flowchart + Timeline (T-60 đến T-0)

TONE: Tài chính, có cấu trúc, dễ điền số.
LENGTH: 8-12 trang A4 (+ templates).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
