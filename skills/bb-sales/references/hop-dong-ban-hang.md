### PROMPT 10: Hợp đồng bán hàng (Sales Contract Template)

#### Mô tả
Template hợp đồng bán hàng / cung cấp dịch vụ chuẩn — bao gồm các điều khoản pháp lý cơ bản, phụ lục mô tả sản phẩm/dịch vụ, và biên bản nghiệm thu. Đảm bảo bảo vệ quyền lợi cả hai bên, giảm rủi ro tranh chấp.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hợp đồng? (mua bán hàng hóa / cung cấp dịch vụ / thuê dịch vụ / subscription)
2. Điều khoản thanh toán mặc định? (đặt cọc, thanh toán theo milestone, COD)
3. Bảo hành / Warranty? (thời hạn, điều kiện, phạm vi)
4. Phạt vi phạm? (% giá trị HĐ / ngày)
5. Giải quyết tranh chấp? (thương lượng → trọng tài → tòa án)
6. Có cần phụ lục kỹ thuật / SLA không?
7. Pháp nhân ký? (cá nhân / công ty — người đại diện, chức vụ)

#### Template gợi ý
Cấu trúc FRM:
- **Phần mở đầu**: Căn cứ pháp lý, thông tin 2 bên (Bên A - Bán, Bên B - Mua)
- **Điều 1** — Đối tượng hợp đồng: Mô tả SP/DV
- **Điều 2** — Giá trị hợp đồng & Phương thức thanh toán
- **Điều 3** — Thời gian & Địa điểm thực hiện
- **Điều 4** — Quyền và nghĩa vụ Bên A
- **Điều 5** — Quyền và nghĩa vụ Bên B
- **Điều 6** — Bảo hành & Hỗ trợ
- **Điều 7** — Bảo mật thông tin
- **Điều 8** — Phạt vi phạm & Bồi thường thiệt hại
- **Điều 9** — Bất khả kháng
- **Điều 10** — Chấm dứt hợp đồng
- **Điều 11** — Giải quyết tranh chấp
- **Điều 12** — Điều khoản chung
- **Phụ lục 1**: Chi tiết SP/DV + Giá
- **Phụ lục 2**: SLA (nếu có)
- **Biên bản nghiệm thu / Biên bản bàn giao**

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Hợp đồng bán hàng (Sales Contract Template).

CONTEXT:
- DN: [Tên] — MST: [số] — Người đại diện: [tên + chức vụ]
- Loại HĐ: [mua bán hàng hóa / cung cấp DV / subscription]
- Thanh toán: [đặt cọc % + milestone / COD / Net X]
- Bảo hành: [thời hạn] — Phạm vi: [mô tả]
- Phạt vi phạm: [% / ngày]
- Tranh chấp: [thương lượng → trọng tài / tòa án]
- Phụ lục SLA: [Có/Không]

FORMAT:
- Chia điều rõ ràng, đánh số khoản liên tục
- Thông tin 2 bên: Bảng Bên A | Bên B — Tên, MST, Địa chỉ, Đại diện, Chức vụ, SĐT, Email
- Bảng giá phụ lục: STT | Hạng mục | ĐVT | SL | Đơn giá | Thành tiền | VAT | Tổng
- Lịch thanh toán: Đợt | % | Số tiền | Điều kiện | Deadline
- SLA (nếu có): Bảng Metric | Target | Measurement | Penalty
- Biên bản nghiệm thu: Header + Nội dung bàn giao + Kết quả kiểm tra + Chữ ký
- Placeholder: [___] cho mọi thông tin tùy biến

TONE: Pháp lý — chính xác, chặt chẽ, cân bằng quyền lợi 2 bên.
LENGTH: 6-10 trang A4 (HĐ + Phụ lục + Biên bản).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
