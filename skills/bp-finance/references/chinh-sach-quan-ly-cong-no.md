# P-FIN-03: Chính sách quản lý công nợ (Accounts Receivable/Payable Management Policy)

#### Mô tả
Chính sách toàn diện về quản lý công nợ phải thu (AR) và phải trả (AP). Quy định điều khoản thanh toán, hạn mức tín dụng khách hàng, quy trình thu hồi nợ, trích lập dự phòng nợ xấu, và quản lý thanh toán nhà cung cấp.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mô hình kinh doanh? (B2B công nợ dài / B2C thu ngay / Hybrid)
2. Điều khoản thanh toán phổ biến? (COD, Net 15, Net 30, Net 60?)
3. Tình trạng công nợ hiện tại? (% nợ quá hạn, nợ xấu)
4. Có bộ phận thu hồi nợ riêng không?
5. Tiêu chí cấp tín dụng cho khách hàng? (doanh số, lịch sử, bảo lãnh...)
6. Chính sách chiết khấu thanh toán sớm?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích, Phạm vi, Thuật ngữ
- **Phần 2** — Quản lý công nợ phải thu (AR): Cấp tín dụng, hạn mức, điều khoản, chiết khấu
- **Phần 3** — Thu hồi nợ: Quy trình 4 bước (nhắc nhở → đốc thúc → cảnh báo → xử lý pháp lý)
- **Phần 4** — Trích lập dự phòng nợ xấu: Tiêu chí, tỷ lệ, quy trình xóa nợ
- **Phần 5** — Quản lý công nợ phải trả (AP): Ưu tiên thanh toán, tận dụng chiết khấu, quản lý cashflow
- **Phần 6** — Đối soát công nợ: Tần suất, quy trình, xử lý chênh lệch
- **Phần 7** — Vai trò & Trách nhiệm
- **Phụ lục**: Bảng aging analysis template, Mẫu thư đòi nợ, Credit application form

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách quản lý công nợ (AR/AP Management Policy).

CONTEXT:
- DN: [Tên] — Mô hình: [B2B / B2C / Hybrid]
- Điều khoản thanh toán: [COD / Net 15 / Net 30 / Net 60]
- Tình trạng nợ: [% quá hạn] — Nợ xấu: [% hoặc số tiền]
- Bộ phận thu hồi nợ: [Có/Không]
- Chiết khấu thanh toán sớm: [Có/Không] — [chi tiết]

FORMAT:
- Chia phần rõ ràng, có mục lục
- Credit scoring: Bảng tiêu chí | Trọng số | Điểm → Hạn mức tín dụng
- Aging buckets: Current | 1-30 | 31-60 | 61-90 | 91-120 | >120 ngày
- Thu hồi nợ escalation: Flowchart 4 bước + timeline + người phụ trách
- Trích lập dự phòng: Bảng tuổi nợ × % trích lập (theo TT48/2019)
- AP payment priority matrix: Nhà CC chiến lược > Nhà CC thường > Khác

TONE: Chuyên nghiệp, tài chính, chặt chẽ.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
