# PROMPT 13: Hợp đồng dịch vụ mẫu (Service Agreement Template)

#### Mô tả
Template hợp đồng dịch vụ B2B, dùng cho mua/bán dịch vụ, thuê freelancer, outsource. Customize theo loại dịch vụ và ngành.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN là bên cung cấp hay bên mua dịch vụ? (hoặc cả hai?)
2. Loại dịch vụ phổ biến nhất? (tư vấn, IT, marketing, logistics...)
3. Thanh toán: milestone, monthly, completion?
4. Cần SLA (Service Level Agreement) kèm theo không?
5. Có yếu tố quốc tế không? (luật áp dụng, currency, timezone)

#### Template gợi ý
Cấu trúc FRM:
- **Điều 1** — Các bên, Đại diện
- **Điều 2** — Phạm vi dịch vụ (SOW / Scope of Work)
- **Điều 3** — Thời hạn, Lịch trình, Milestone
- **Điều 4** — Giá trị hợp đồng, Phương thức thanh toán, Thuế
- **Điều 5** — Nghĩa vụ các bên
- **Điều 6** — SLA & KPIs (nếu có)
- **Điều 7** — Bảo mật & Sở hữu trí tuệ
- **Điều 8** — Bồi thường & Giới hạn trách nhiệm
- **Điều 9** — Chấm dứt hợp đồng
- **Điều 10** — Bất khả kháng (Force Majeure)
- **Điều 11** — Giải quyết tranh chấp
- **Phụ lục**: SOW template, SLA template, Bảng giá

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template hợp đồng dịch vụ (Service Agreement).

CONTEXT:
- DN: [Tên] — Vai trò: [Provider / Client / cả hai]
- Loại dịch vụ: [tư vấn / IT / marketing / logistics / khác]
- Thanh toán: [milestone / monthly / completion]
- SLA: [Có/Không]
- Quốc tế: [Có/Không] — Luật áp dụng: [Luật VN / khác]

FORMAT:
- Template form: Trường điền = [___]
- SOW attachment template riêng
- SLA template (nếu có): Metric | Target | Measurement | Penalty
- Bảng giá mẫu: Dịch vụ | Đơn vị | Đơn giá | Ghi chú
- Payment schedule template: Milestone | Deliverable | % | Amount | Due date

TONE: Chuyên nghiệp, cân bằng quyền lợi 2 bên.
LENGTH: 6-8 trang A4 + phụ lục.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
