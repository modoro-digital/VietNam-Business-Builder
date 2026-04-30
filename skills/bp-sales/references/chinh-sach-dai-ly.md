### PROMPT 15: Chính sách đại lý/partner (Agent/Partner Policy)

#### Mô tả
Chính sách toàn diện dành cho đại lý và đối tác phân phối — quy định điều kiện trở thành đại lý, quyền lợi, nghĩa vụ, cơ cấu hoa hồng, territory, KPIs, và quy trình đánh giá. Là "luật chơi" rõ ràng cho mối quan hệ đối tác.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại đối tác? (đại lý bán hàng / distributor / reseller / affiliate / referral partner)
2. Tiêu chí trở thành đối tác? (vốn, kinh nghiệm, nhân sự, vùng miền)
3. Cơ cấu hoa hồng? (% doanh thu / CK theo volume / tiered commission)
4. Có phân territory không? (độc quyền / không độc quyền)
5. KPIs cho đối tác? (doanh số tối thiểu / tháng, quý)
6. Chính sách hỗ trợ? (marketing, training, co-branding, tools)
7. Thời hạn đánh giá? Điều kiện chấm dứt?
8. Cấp bậc đối tác? (Silver / Gold / Platinum?)

#### Template gợi ý
Cấu trúc POL:
- **Điều 1-3** — Mục đích, Phạm vi, Định nghĩa các loại đối tác
- **Điều 4** — Điều kiện & Quy trình trở thành đối tác
- **Điều 5** — Cấp bậc đối tác: Bảng tier + điều kiện + quyền lợi
- **Điều 6** — Quyền lợi đối tác: Hoa hồng, hỗ trợ marketing, training, tools, co-branding
- **Điều 7** — Nghĩa vụ đối tác: Doanh số tối thiểu, báo cáo, brand compliance, chăm sóc KH
- **Điều 8** — Cơ cấu hoa hồng: Bảng chi tiết tier × sản phẩm × %
- **Điều 9** — Territory & Exclusivity: Quy định vùng, xử lý xung đột
- **Điều 10** — Đánh giá & Xếp hạng: KPIs, tần suất, thưởng/phạt
- **Điều 11** — Chấm dứt & Thanh lý: Điều kiện, quy trình, nghĩa vụ sau chấm dứt
- **Phụ lục**: Đơn đăng ký đại lý, Bảng hoa hồng chi tiết, KPI scorecard

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách đại lý/partner (Agent/Partner Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Loại đối tác: [đại lý / distributor / reseller / affiliate / referral]
- Tiêu chí: [vốn / kinh nghiệm / nhân sự / vùng miền]
- Hoa hồng: [% / tiered / hybrid]
- Territory: [độc quyền / không] — Vùng: [liệt kê]
- KPIs: [doanh số min / tháng, quý]
- Cấp bậc: [Silver / Gold / Platinum hoặc custom]
- Hỗ trợ: [marketing / training / tools / co-brand]

FORMAT:
- Đánh số điều liên tục, ngôn ngữ rõ ràng
- Tier matrix: Bảng Cấp | Điều kiện | Hoa hồng % | Hỗ trợ Marketing | Training | Territory
- Commission table: SP | Cấp 1 % | Cấp 2 % | Cấp 3 % | Bonus condition
- KPI scorecard: KPI | Target | Weight | Measurement | Frequency
- Territory map: Vùng | Đại lý | Exclusive? | Population | Market size
- Evaluation timeline: Q1 Review | Mid-year | Annual | Re-certification
- Termination flowchart: Mermaid — Warning → Probation → Termination → Settlement
- Đơn đăng ký: 1 trang form

TONE: Chuyên nghiệp, rõ ràng, công bằng, hấp dẫn cho đối tác tiềm năng.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
