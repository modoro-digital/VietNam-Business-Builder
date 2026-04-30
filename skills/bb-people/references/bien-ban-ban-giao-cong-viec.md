# P-PPL-19: Biên bản bàn giao công việc (Work Handover Record)

#### Mô tả
Template biên bản bàn giao công việc khi NV nghỉ việc hoặc chuyển vị trí — ghi nhận đầy đủ: công việc đang làm, tài sản, tài khoản, tài liệu, công nợ, khách hàng đang quản lý. Có chữ ký 3 bên: NV nghỉ + Người nhận + Trưởng phòng.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Các hạng mục bàn giao bắt buộc? (tùy vị trí: Sales bàn giao KH, Kế toán bàn giao sổ sách)
2. Bàn giao tài sản: laptop, điện thoại, xe, thẻ — quy trình kiểm tra?
3. Bàn giao tài khoản: email, CRM, phần mềm, MXH công ty — ai tiếp nhận?
4. Có cần bàn giao công nợ / khách hàng đang chăm sóc không?
5. Ai ký duyệt biên bản? (3 bên hay thêm HR?)

#### Template gợi ý
Cấu trúc FRM:
- **Header**: Thông tin NV bàn giao + Người nhận + Ngày
- **Phần 1** — Công việc đang thực hiện: Task | Status | Deadline | Ghi chú
- **Phần 2** — Tài sản: Mã TS | Tên | Tình trạng | Ghi chú
- **Phần 3** — Tài khoản & Mật khẩu: Hệ thống | Account | Đã chuyển quyền ☐
- **Phần 4** — Tài liệu: Danh mục | Vị trí lưu | Đã bàn giao ☐
- **Phần 5** — Công nợ & Khách hàng: KH | Dư nợ | Status | Người tiếp nhận
- **Chữ ký**: NV bàn giao | Người nhận | Trưởng phòng | HR (nếu cần)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Biên bản bàn giao công việc (Work Handover Record).

CONTEXT:
- DN: [Tên]
- Hạng mục bắt buộc: [Công việc / Tài sản / Tài khoản / Tài liệu / Công nợ-KH]
- Ký duyệt: [3 bên / 4 bên (thêm HR)]

FORMAT:
- 1 form template 2-3 trang A4
- Header: DN info | NV bàn giao (tên, chức danh, phòng ban, ngày cuối) | Người nhận (tên, chức danh)
- Bảng công việc: # | Task | Status (Hoàn thành/Đang làm/Chờ) | Deadline | Ghi chú cho người nhận
- Bảng tài sản: # | Mã TS | Tên | Serial# | Tình trạng | Đã thu hồi ☐
- Bảng tài khoản: # | Hệ thống | Username | Đã reset MK ☐ | Đã chuyển quyền ☐
- Bảng tài liệu: # | Tên TL | Vị trí lưu (folder/drive) | Đã bàn giao ☐
- Bảng KH/Công nợ: # | KH | Công nợ | Status | Người tiếp nhận | Ghi chú
- Footer chữ ký: 3-4 ô ký — Người bàn giao | Người nhận | TP | HR
- Ghi chú: Vấn đề tồn đọng + timeline giải quyết

TONE: Form chính thức, đầy đủ, tránh tranh chấp sau nghỉ việc.
LENGTH: 2-3 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
