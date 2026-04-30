### PROMPT 01: SOP Quản lý văn phòng (Office Management SOP)

#### Mô tả
Quy trình chuẩn hóa quản lý văn phòng hàng ngày — bao gồm vệ sinh, bảo trì thiết bị, quản lý phòng họp, lễ tân, chìa khóa/access card, tiện ích (nước, điện, internet). Đảm bảo văn phòng luôn sẵn sàng, chuyên nghiệp.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Văn phòng thuê hay sở hữu? Diện tích? Số tầng?
2. Có admin/lễ tân chuyên trách không?
3. Dịch vụ outsource: vệ sinh, bảo vệ, IT?
4. Phòng họp: bao nhiêu phòng? Hệ thống đặt phòng?
5. Thiết bị chung: máy in, máy chiếu, bếp, đồ dùng VP?
6. Giờ mở/đóng cửa VP?

#### Template gợi ý
Cấu trúc SOP:
- **Quản lý hàng ngày**: Mở cửa, đóng cửa, checklist vệ sinh, kiểm tra thiết bị
- **Phòng họp**: Đặt phòng, chuẩn bị, dọn dẹp, quy tắc sử dụng
- **Thiết bị & Tiện ích**: Bảo trì định kỳ, xử lý hỏng, liên hệ kỹ thuật
- **Lễ tân & Khách**: Tiếp đón, đăng ký, hướng dẫn
- **Chìa khóa & Access**: Cấp phát, thu hồi, mất/hỏng
- **Nhà cung cấp VP**: Vệ sinh, bảo vệ, nước uống, văn phòng phẩm

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quản lý văn phòng (Office Management).

CONTEXT:
- DN: [Tên] — VP: [thuê/sở hữu] — Diện tích: [m²] — [số] tầng
- Admin: [Có/Không] — Outsource: [vệ sinh/bảo vệ/IT]
- Phòng họp: [số] phòng — Đặt phòng: [Google Calendar/Slack/bảng tay]
- Giờ VP: [giờ]

FORMAT:
- Checklist mở cửa: 5-8 mục ☐ + thời gian + người thực hiện
- Checklist đóng cửa: 5-8 mục ☐
- Phòng họp booking rules: Bảng Phòng | Sức chứa | Thiết bị | Booking method | Rules
- Bảo trì schedule: Bảng Thiết bị | Tần suất | Người phụ trách | NCC bảo trì | Liên hệ
- Xử lý sự cố VP: Flowchart — Loại sự cố → Mức độ → Người xử lý → Thời gian
- NCC directory: Dịch vụ | NCC | Liên hệ | HĐ số | Hạn HĐ

TONE: Operational, thực tế, dễ follow.
LENGTH: 5-7 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
