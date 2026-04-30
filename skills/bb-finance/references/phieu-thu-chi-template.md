# P-FIN-13: Phiếu thu chi template (Cash Voucher Templates)

#### Mô tả
Bộ template phiếu thu, phiếu chi, ủy nhiệm chi, giấy đề nghị thanh toán — theo chuẩn mực kế toán VN. Đảm bảo đủ thông tin bắt buộc, dễ điền, dễ kiểm soát.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phần mềm kế toán tự in phiếu hay dùng phiếu tay?
2. Có cần song ngữ Việt-Anh không?
3. Quy định đánh số phiếu? (VD: PT-2024-001, PC-2024-001)
4. Mức chi tiền mặt tối đa? (theo quy định NH Nhà nước: > 20 triệu phải CK)
5. Có cần phiếu đề nghị tạm ứng riêng không?

#### Template gợi ý
Cấu trúc FRM — 4 mẫu phiếu:
- **Phiếu Thu** (PT): Theo mẫu TT200 — Header DN, số phiếu, ngày, người nộp, lý do, số tiền (số + chữ), tài khoản, chữ ký 4 bên
- **Phiếu Chi** (PC): Tương tự PT — người nhận, lý do chi, chứng từ kèm, chữ ký duyệt chi
- **Ủy nhiệm chi** (UNC): Mẫu ngân hàng — thông tin chuyển khoản, người thụ hưởng
- **Giấy đề nghị thanh toán** (ĐNTT): Người đề nghị, nội dung, số tiền, chứng từ đính kèm, cấp duyệt
- **(Tùy chọn) Giấy đề nghị tạm ứng**: Mục đích, số tiền, thời hạn hoàn ứng

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo bộ Phiếu thu chi template.

CONTEXT:
- DN: [Tên] — MST: [số]
- Phần mềm: [MISA / Fast / Tay]
- Bilingual: [Có/Không]
- Numbering: [convention]
- Tạm ứng: [Có/Không]
- Cơ sở: TT200/2014/TT-BTC hoặc TT133/2016/TT-BTC

FORMAT:
- 4-5 template riêng biệt, mỗi template 1 trang A4
- Header: Logo + Tên DN + MST + Địa chỉ
- Trường điền: [___] + gợi ý mẫu
- Số tiền: Bằng số + Bằng chữ
- Chữ ký: Đúng vị trí theo quy định (Giám đốc | KTT | Thủ quỹ | Người lập | Người nộp/nhận)
- Numbering format: [Loại]-[Năm]-[Số 3 chữ số]
- Hướng dẫn sử dụng ngắn gọn kèm mỗi mẫu

TONE: Kế toán chuẩn mực, form chính thức.
LENGTH: 5-7 trang A4 (mỗi mẫu 1 trang + 1-2 trang hướng dẫn).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
