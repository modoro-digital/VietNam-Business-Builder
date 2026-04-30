### PROMPT 03: Sổ theo dõi tài sản (Asset Register / Tracking Sheet)

#### Mô tả
Template sổ theo dõi tài sản — quản lý toàn bộ tài sản của DN: từ bàn ghế, máy tính, đến xe cộ, máy móc. Theo dõi vị trí, người sử dụng, tình trạng, khấu hao.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có bao nhiêu loại tài sản chính? (IT, nội thất, phương tiện, máy móc...)
2. Quy tắc đánh mã tài sản? (VD: IT-NB-001 = IT-Notebook-001)
3. Phương pháp khấu hao? (Đường thẳng / Số dư giảm dần)
4. Tần suất kiểm kê? (6 tháng / 1 năm)
5. Quản lý trên phần mềm hay Excel?

#### Template gợi ý
Cấu trúc FRM:
- **Asset Register**: Mã TS | Tên | Loại | Ngày mua | Giá gốc | Khấu hao lũy kế | GTCL | Vị trí | Người dùng | Tình trạng (Đang dùng/Sửa chữa/Thanh lý/Mất)
- **Phân loại**: IT | Nội thất | Phương tiện | Máy móc | Khác
- **Bàn giao**: Mã TS | Từ | Đến | Ngày | Ký nhận
- **Thanh lý**: Mã TS | Lý do | Giá trị còn | Phương thức | Duyệt
- **Kiểm kê**: Mã TS | Sổ sách | Thực tế | Chênh lệch | Ghi chú

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sổ theo dõi tài sản (Asset Register).

CONTEXT:
- DN: [Tên] — Số loại TS: [số] — Tổng TS ước: [số]
- Mã hóa: [convention]
- Khấu hao: [Đường thẳng / Số dư giảm dần]
- Kiểm kê: [6 tháng / 1 năm]
- Tool: [PM / Excel]

FORMAT:
- Master register: 15+ cột, đủ info per tài sản
- Naming convention: Bảng Loại | Prefix | Ví dụ
- Khấu hao reference: Loại TS | Thời gian KH (năm) | PP KH (theo TT45/2013)
- Bàn giao form: 1/2 trang A4, ký nhận 2 bên
- Kiểm kê template: Bảng đối chiếu sổ sách vs thực tế
- Summary dashboard: Tổng TS | Giá trị | Đang dùng | Cần thanh lý | Chênh lệch

TONE: Quản lý, chính xác, dễ cập nhật.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
