### PROMPT 02: SOP Mua sắm tài sản (Asset Procurement SOP)

#### Mô tả
Quy trình mua sắm tài sản/thiết bị — từ phát sinh nhu cầu, lập đề xuất, duyệt, lấy báo giá so sánh, đặt mua, nghiệm thu, đến bàn giao sử dụng và đưa vào quản lý tài sản.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phân cấp duyệt mua sắm? (< 5 triệu: TP | < 20 triệu: GĐ | > 20 triệu: HĐQT?)
2. Cần bao nhiêu báo giá so sánh? (2 / 3 / 5?)
3. Quy trình thanh toán: tạm ứng hay thanh toán sau giao hàng?
4. Có ủy ban mua sắm (procurement committee) không?
5. Ngưỡng phân loại TSCĐ: bao nhiêu VNĐ? (thường 30 triệu theo TT45)

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Đề xuất mua sắm: Form đề xuất + justification
- **Bước 2** — Phê duyệt: Theo hạn mức + kiểm tra budget
- **Bước 3** — Lấy báo giá: Số lượng báo giá, bảng so sánh
- **Bước 4** — Chọn NCC & Đặt hàng: Tiêu chí chọn, PO
- **Bước 5** — Nhận hàng & Nghiệm thu: Kiểm tra, biên bản
- **Bước 6** — Thanh toán: Chứng từ, quy trình
- **Bước 7** — Bàn giao & Quản lý: Gắn mã, nhập sổ, bàn giao user

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Mua sắm tài sản (Asset Procurement).

CONTEXT:
- DN: [Tên] — Phân cấp: < [X] triệu (TP) | < [Y] triệu (GĐ) | > [Y] (HĐQT)
- Số báo giá: [2/3/5]
- Thanh toán: [tạm ứng / sau giao hàng]
- Ngưỡng TSCĐ: [30 triệu / custom]
- Procurement committee: [Có/Không]

FORMAT:
- Flowchart 7 bước: Mermaid — highlight approval gates
- Form đề xuất template: Người đề xuất | Mô tả | Lý do | Số lượng | Budget line | Ước giá
- Bảng so sánh báo giá: NCC | Giá | Thời gian giao | Bảo hành | Thanh toán | Điểm
- Biên bản nghiệm thu template: Hàng nhận | Số lượng | Chất lượng | Chênh lệch | Ký nhận
- Decision matrix: Giá trị < X → Quy trình nhanh | > X → Quy trình đầy đủ
- Timeline: Từ đề xuất → nhận hàng target [ngày]

TONE: SOP chuẩn, kiểm soát chi phí.
LENGTH: 5-7 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
