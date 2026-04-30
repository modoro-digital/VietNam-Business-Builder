# P-FIN-20: Thuyết minh BCTC (Notes to Financial Statements)

#### Mô tả
Template Thuyết minh Báo cáo Tài chính — giải thích chi tiết các chính sách kế toán áp dụng, chi tiết số liệu trên BCTC, và các sự kiện quan trọng. Bắt buộc theo Luật Kế toán VN.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Chế độ kế toán? (TT200 / TT133)
2. Chính sách kế toán đặc thù? (VD: phương pháp khấu hao, tính giá HTK, ghi nhận doanh thu)
3. Có giao dịch đặc biệt trong kỳ? (sáp nhập, thanh lý, kiện tụng, cam kết lớn)
4. Có bên liên quan cần công bố không? (giao dịch nội bộ, cổ đông lớn)
5. Có sự kiện sau ngày lập BCTC cần thuyết minh?

#### Template gợi ý
Cấu trúc RPT:
- **Phần I** — Thông tin DN: Tên, MST, ngành, vốn, nhân sự
- **Phần II** — Chuẩn mực & Chế độ kế toán áp dụng
- **Phần III** — Chính sách kế toán chủ yếu: Ngoại tệ, HTK, TSCĐ, Doanh thu, Chi phí, Thuế
- **Phần IV** — Chi tiết khoản mục BCTC: Mỗi khoản trọng yếu → breakdown chi tiết
- **Phần V** — Giao dịch bên liên quan
- **Phần VI** — Cam kết & Nợ tiềm tàng
- **Phần VII** — Sự kiện sau ngày BCTC
- **Phần VIII** — Thông tin bổ sung: Segment, EPS, cổ tức

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Thuyết minh BCTC (Notes to Financial Statements).

CONTEXT:
- DN: [Tên] — MST: [số] — Chế độ: [TT200 / TT133]
- Chính sách đặc thù: [liệt kê]
- Giao dịch đặc biệt: [liệt kê hoặc "không có"]
- Bên liên quan: [Có/Không]
- Cơ sở: Luật Kế toán 2015, VAS, TT200/TT133

FORMAT:
- Theo mẫu B09-DN (TT200) / B09-DNN (TT133)
- Chia phần rõ ràng, đánh số mục liên tục
- Chính sách kế toán: Mỗi chính sách 1 đoạn ngắn, rõ ràng
- Chi tiết khoản mục: Bảng Khoản mục | Đầu kỳ | Tăng | Giảm | Cuối kỳ
- Bên liên quan: Bảng Tên | Quan hệ | Giao dịch | Giá trị | Dư nợ
- Placeholder cho từng phần: [Điền thông tin DN cụ thể]
- Lưu ý kiểm toán: Highlight khoản mục trọng yếu

TONE: Kế toán chuẩn mực, chính thức, đủ để nộp kiểm toán.
LENGTH: 8-15 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
