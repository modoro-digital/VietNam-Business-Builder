### PROMPT 09: SOP Đặt hàng (Purchase Order SOP)

#### Mô tả
Quy trình đặt hàng (PO) — từ khi phát sinh nhu cầu đến khi nhận hàng và thanh toán. Liên kết với SOP Mua sắm tài sản (cho TS lớn) và SOP Quản lý kho (nhập kho).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phân cấp duyệt PO theo giá trị? (VD: < 5tr TP duyệt, < 20tr GĐ, > 20tr HĐQT)
2. Phần mềm quản lý PO? (ERP / phần mềm kế toán / Excel / email)
3. Chỉ đặt hàng NCC trong AVL hay cho phép ngoại lệ?
4. Cần bao nhiêu báo giá so sánh trước khi đặt? (1/2/3)
5. Quy trình 3-way matching hiện tại? (PO vs Phiếu nhận vs Invoice)
6. Thời gian xử lý PO trung bình hiện tại?
7. Có PO khẩn cấp không? Quy trình như thế nào?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Phát sinh nhu cầu: Ai đề xuất, form đề xuất
- **Bước 2** — Kiểm tra AVL: NCC có trong danh sách đã duyệt?
- **Bước 3** — Lấy báo giá: So sánh 2-3 NCC
- **Bước 4** — Duyệt PO: Theo hạn mức phân cấp
- **Bước 5** — Gửi PO cho NCC: Xác nhận đơn hàng
- **Bước 6** — Nhận hàng & Nghiệm thu: Kiểm tra số lượng, chất lượng
- **Bước 7** — 3-way matching: PO vs Phiếu nhận vs Invoice
- **Bước 8** — Thanh toán: Chuyển hồ sơ sang kế toán
- **Exception**: PO khẩn cấp, PO vượt hạn mức, PO ngoài AVL

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Đặt hàng (Purchase Order Process).

CONTEXT:
- DN: [Tên] — Phân cấp duyệt PO: [chi tiết]
- Phần mềm: [ERP / Excel / email]
- NCC: Chỉ từ AVL / Ngoại lệ có quy trình
- Số báo giá cần: [1/2/3]

FORMAT:
- Flowchart: Mermaid — Yêu cầu → Kiểm tra AVL → Báo giá → So sánh → Duyệt PO → Gửi NCC → Nhận hàng → Nghiệm thu → Thanh toán
- PO template: # PO | Ngày | NCC | Items | Qty | Đơn giá | Tổng | Giao hàng | TT | Duyệt bởi
- 3-way matching: PO vs Phiếu nhận hàng vs Invoice → Approve payment
- Exception handling: PO khẩn cấp, PO vượt hạn mức, PO ngoài AVL
- Approval matrix: Giá trị PO → Cấp duyệt
- Lead time tracking: Từ yêu cầu → nhận hàng = target [ngày]

TONE: SOP chuẩn, procurement.
LENGTH: 4-6 trang A4.

CROSS-REFERENCE: Liên kết với AVL (P-OPS-08) và SOP Quản lý kho (P-OPS-04).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
