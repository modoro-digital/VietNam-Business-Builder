### PROMPT 13: Checklist vận hành hàng ngày (Daily Operations Checklist)

#### Mô tả
Checklist công việc hàng ngày — mở cửa, kiểm tra, vận hành, đóng cửa. Đảm bảo không bỏ sót việc nào, nhất là khi thay người hoặc training NV mới.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hình hoạt động? (Văn phòng / Cửa hàng bán lẻ / Nhà máy / Kho / F&B)
2. Giờ hoạt động? (mở cửa – đóng cửa)
3. Có ca kíp không? Bao nhiêu ca?
4. Ai chịu trách nhiệm mở/đóng cửa?
5. Thiết bị nào cần kiểm tra hàng ngày? (máy POS, máy lạnh, hệ thống IT, máy móc SX...)
6. Có công việc đặc thù theo tuần/tháng không? (VD: kiểm kê thứ 6, vệ sinh tổng cuối tháng)
7. Quy trình sign-off hiện tại? (ai kiểm tra, ai ký duyệt)

#### Template gợi ý
Cấu trúc FRM:
- **Checklist mở cửa (AM)**: 8-12 mục — bật điện, kiểm tra thiết bị, chuẩn bị khu vực, mở hệ thống
- **Checklist trong ngày**: 5-8 mục — kiểm tra định kỳ, bổ sung vật tư, xử lý phát sinh
- **Checklist đóng cửa (PM)**: 8-12 mục — tắt thiết bị, khóa cửa, backup dữ liệu, kiểm tra an ninh
- **Bảng công việc theo tuần**: Thứ 2-CN × Task đặc thù
- **Bảng công việc theo tháng**: Tuần 1-4 × Task monthly
- **Sign-off**: Người thực hiện ký + Manager review + Ghi chú bất thường

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Checklist vận hành hàng ngày.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Giờ hoạt động: [giờ]
- Loại: [VP / Cửa hàng / Nhà máy / Kho]
- Ca kíp: [Có/Không] — Số ca: [số]
- Thiết bị cần kiểm tra: [liệt kê]

FORMAT:
- 3 bảng chính: Mở cửa (AM) | Trong ngày | Đóng cửa (PM)
- Mỗi mục: ☐ Task | Thời gian | Người thực hiện | Ghi chú
- Weekly tasks: Bảng riêng cho công việc theo tuần (VD: kiểm kê thứ 6)
- Monthly tasks: Bảng riêng cho công việc theo tháng
- Sign-off: Người thực hiện ký cuối ngày + Manager review
- Exception log: Ghi chú bất thường phát sinh trong ngày

TONE: Operational, checklist-style, dễ in và sử dụng ngay.
LENGTH: 2-3 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
