### PROMPT 16: Chính sách Chất lượng (Quality Policy — ISO-aligned)

#### Mô tả
Chính sách chất lượng tổng thể — cam kết, mục tiêu, KPIs chất lượng, PDCA, cải tiến liên tục. Aligned với ISO 9001:2015 (có thể dùng ngay nếu DN muốn đi ISO).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN đã có chứng nhận ISO 9001 chưa? (Đang có / Muốn đạt / Không cần nhưng muốn align)
2. Sản phẩm/dịch vụ chính cần kiểm soát chất lượng?
3. Tỷ lệ lỗi/khiếu nại hiện tại? (nếu có số liệu)
4. Có bộ phận QC/QA riêng không? Bao nhiêu người?
5. Đã có KPIs chất lượng nào đang theo dõi?
6. Khách hàng có yêu cầu tiêu chuẩn chất lượng đặc biệt không?
7. Quy trình xử lý sản phẩm/dịch vụ không đạt hiện tại?

#### Template gợi ý
Cấu trúc POL:
- **Cam kết chất lượng**: Quality statement từ CEO — 1 đoạn, in poster
- **Phạm vi áp dụng**: Sản phẩm/dịch vụ, bộ phận, quy trình nào
- **Mục tiêu chất lượng**: SMART × 5-8 mục tiêu theo năm
- **KPIs chất lượng**: Bảng KPI | Target | Cách đo | Tần suất | Owner
- **Chu trình PDCA**: Plan-Do-Check-Act cho mỗi quy trình chính
- **Vòng lặp phản hồi KH**: Thu thập → Phân tích → Cải tiến → Đo lường
- **Xử lý không phù hợp**: Phát hiện → Cách ly → RCA → Khắc phục → Phòng ngừa
- **Management review**: Tần suất, agenda, đầu ra mong đợi
- **Đào tạo chất lượng**: Kế hoạch nâng cao nhận thức QMS

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách Chất lượng (Quality Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- ISO 9001: [Đang có / Muốn đạt / Không cần nhưng muốn align]
- SP/DV chính: [liệt kê]
- QC/QA team: [Có/Không] — Số người: [số]
- KPIs chất lượng hiện có: [liệt kê]
- Tỷ lệ lỗi hiện tại: [%]

FORMAT:
- Quality statement: 1 đoạn cam kết — in poster treo VP
- Mục tiêu chất lượng: SMART × 5-8 mục tiêu
- KPIs: Bảng KPI | Target | Measurement | Frequency | Owner
- PDCA cycle: Diagram + hướng dẫn áp dụng cho mỗi process
- Customer feedback loop: Flowchart — Thu thập → Phân tích → Cải tiến → Đo lường
- Nonconformity handling: Quy trình xử lý SP/DV không phù hợp + RCA
- Management review: Tần suất, agenda, output
- Cơ sở: ISO 9001:2015 clauses 5.2, 6.2

TONE: ISO-aligned, chuyên nghiệp, cam kết.
LENGTH: 5-8 trang A4.

CROSS-REFERENCE: Đây là chính sách chất lượng (cam kết, mục tiêu, KPIs). SOP kiểm soát chất lượng thực thi xem bb-product-tech/SOP Kiểm soát Chất lượng.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
