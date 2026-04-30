### PROMPT 05: Marketing Budget Allocation (Phân bổ ngân sách marketing)

#### Mô tả
Tài liệu phân bổ ngân sách marketing — chia theo kênh, theo chiến dịch, theo quý. Bao gồm ROI benchmarks cho từng kênh, triggers để tái phân bổ ngân sách, và quy trình duyệt chi tiêu marketing.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tổng ngân sách marketing năm? (VNĐ hoặc % doanh thu?)
2. Phân bổ hiện tại? (% cho online vs offline vs tools?)
3. Kênh nào đang cho ROI tốt nhất? Kênh nào kém?
4. Có seasonal peaks không? (Tết, 11/11, Black Friday, mùa cao điểm ngành?)
5. Quy trình duyệt chi tiêu? (< X triệu: Marketing Manager | > X: CMO | > Y: CEO?)
6. Có contingency fund không? (% ngân sách dự phòng?)

#### Template gợi ý
Cấu trúc MAN:
- **Budget Overview**: Tổng ngân sách, % doanh thu, so sánh YoY
- **Channel Allocation**: Breakdown theo kênh — Paid, Organic, Content, Tools, Events, HR
- **Campaign Budget**: Breakdown theo chiến dịch lớn trong năm
- **Quarterly Breakdown**: Q1-Q4 phân bổ theo mùa vụ
- **ROI Benchmarks**: Target ROI/ROAS cho từng kênh
- **Reallocation Triggers**: Điều kiện để chuyển ngân sách giữa các kênh
- **Approval Process**: Quy trình duyệt chi tiêu theo hạn mức

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Marketing Budget Allocation (Phân bổ ngân sách marketing).

CONTEXT:
- DN: [Tên] — Tổng budget marketing: [số VNĐ / % doanh thu]
- Phân bổ hiện tại: Online [%] | Offline [%] | Tools [%]
- ROI kênh tốt nhất: [kênh] — ROI kênh kém: [kênh]
- Seasonal peaks: [liệt kê tháng/sự kiện]
- Approval: < [X] triệu (Marketing Manager) | > [X] (CMO) | > [Y] (CEO)
- Contingency: [%]

FORMAT:
- Budget summary: Bảng 1 trang — Tổng | Online | Offline | Content | Tools | Events | Contingency
- Channel breakdown: Bảng Kênh | Budget Q1 | Q2 | Q3 | Q4 | Total | % | Target ROI
- Campaign budget: Bảng Campaign | Timing | Budget | Channels | Expected ROI | Owner
- Monthly cash flow: Bảng Tháng × Kênh — dự kiến chi tiêu
- ROI benchmarks: Bảng Kênh | Industry Avg ROI | Our Target | Min Acceptable | Action if Below
- Reallocation rules: Decision tree — Performance < X% → Review → Reallocate → To where
- Approval matrix: Giá trị | Approver | Timeline | Chứng từ cần

TONE: Financial, data-driven, ROI-focused.
LENGTH: 5-7 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
