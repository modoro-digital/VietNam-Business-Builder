# P-FIN-07: Cashflow Forecast 12 tháng (12-Month Cash Flow Forecast)

#### Mô tả
Dự báo dòng tiền 12 tháng tiếp theo — chi tiết dòng tiền vào (thu bán hàng, thu nợ, vay...) và dòng tiền ra (chi mua hàng, lương, thuế, trả nợ...). Xác định tháng nào căng thẳng tiền mặt, cần vay hoặc chậm chi.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Số dư tiền mặt & ngân hàng hiện tại?
2. Nguồn thu chính? (bán hàng / dự án / subscription / đầu tư)
3. Tần suất thu: hàng ngày / tuần / tháng? Có mùa vụ?
4. Các khoản chi lớn cố định hàng tháng? (lương, thuê mặt bằng, vay...)
5. Có kế hoạch chi lớn trong 12 tháng tới? (mua tài sản, đầu tư, trả nợ gốc)
6. Dự trữ tiền mặt tối thiểu mong muốn?

#### Template gợi ý
Cấu trúc RPT:
- **Assumptions** — Giả định về tăng trưởng, collection rate, payment terms
- **Cash Inflow** — Bảng 12 tháng: Từng nguồn thu × từng tháng
- **Cash Outflow** — Bảng 12 tháng: Từng khoản chi × từng tháng
- **Net Cashflow** — Inflow - Outflow = Net per tháng
- **Cumulative Balance** — Số dư lũy kế — highlight tháng âm
- **Sensitivity Analysis** — What-if: doanh thu giảm 10/20/30%
- **Action Plan** — Đối với tháng thiếu hụt: giải pháp cụ thể

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Cashflow Forecast 12 tháng.

CONTEXT:
- DN: [Tên] — Số dư hiện tại: [số]
- Nguồn thu: [liệt kê + ước tính/tháng]
- Chi cố định: [liệt kê + số/tháng]
- Chi lớn sắp tới: [liệt kê + thời điểm]
- Dự trữ tối thiểu: [số]
- Mùa vụ: [Có/Không] — [mô tả pattern]

FORMAT:
- Bảng chính: 12 cột (tháng) × hàng (từng khoản thu/chi)
- Color coding: Tháng dư 🟢 | Tháng thiếu 🔴 | Tháng cận kề 🟡
- Chart data: Line chart — Inflow vs Outflow vs Balance
- Minimum cash line: Đường ngang → alert khi balance < minimum
- Sensitivity table: Base case ±10%, ±20%, ±30%
- Action triggers: IF balance < [X] THEN [action]

TONE: Thực tế, action-oriented, cảnh báo rõ.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
