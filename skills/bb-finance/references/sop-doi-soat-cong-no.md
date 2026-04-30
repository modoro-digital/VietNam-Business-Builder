# P-FIN-11: SOP Đối soát công nợ (Accounts Reconciliation SOP)

#### Mô tả
Quy trình đối soát công nợ định kỳ giữa DN với khách hàng (AR) và nhà cung cấp (AP). Đảm bảo số liệu trên sổ sách khớp với đối tác, phát hiện sai lệch kịp thời.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tần suất đối soát? (hàng tháng / quý / khi có chênh lệch)
2. Số lượng KH/NCC cần đối soát thường xuyên?
3. Hình thức đối soát: email / gặp trực tiếp / gửi biên bản?
4. Phần mềm hỗ trợ? (tự động tạo bảng đối soát hay thủ công?)
5. Tình trạng chênh lệch hiện tại có phổ biến không?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Lịch đối soát**: Calendar — ai đối soát với ai, khi nào
- **Quy trình đối soát AR**: 5 bước — Xuất data → Gửi xác nhận → Nhận phản hồi → Xử lý chênh lệch → Ký biên bản
- **Quy trình đối soát AP**: 5 bước tương tự
- **Xử lý chênh lệch**: Decision tree — loại chênh lệch → nguyên nhân → cách xử lý
- **Template biên bản đối soát**
- **Escalation**: Khi không thống nhất

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Đối soát công nợ.

CONTEXT:
- DN: [Tên] — Số KH đối soát: [số] — Số NCC đối soát: [số]
- Tần suất: [tháng / quý]
- Hình thức: [email / trực tiếp / online]
- Phần mềm: [tên]

FORMAT:
- Calendar đối soát: Bảng Tuần/Tháng × Đối tượng
- Flowchart AR: Mermaid — 5 bước + timeline
- Flowchart AP: Mermaid — 5 bước + timeline
- Xử lý chênh lệch: Decision tree — Chênh lệch thời gian / số lượng / giá / khác → Action
- Template biên bản: Header + Bảng chi tiết + Chênh lệch + Chữ ký 2 bên
- Aging report template kèm đối soát
- KPI: % đối soát hoàn thành / tháng, % chênh lệch / tổng dư nợ

TONE: SOP chuẩn, rõ ràng.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
