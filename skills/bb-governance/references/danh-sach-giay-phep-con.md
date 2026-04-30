# PROMPT 03: Danh sách giấy phép con (Sub-licenses & Permits Registry)

#### Mô tả
Danh mục tổng hợp tất cả giấy phép con, chứng chỉ hành nghề, điều kiện kinh doanh mà DN cần có ngoài ĐKKD. Cập nhật tình trạng, hạn, cơ quan quản lý.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ngành nghề kinh doanh chính & phụ? (mỗi ngành có giấy phép khác nhau)
2. Có hoạt động nào thuộc "ngành nghề kinh doanh có điều kiện" không? (Phụ lục IV Luật Đầu tư)
3. Có xuất nhập khẩu không? Có hoạt động liên quan PCCC, ATTP, Môi trường không?
4. Địa bàn hoạt động? (mỗi tỉnh/thành có yêu cầu riêng)

#### Template gợi ý
Cấu trúc FRM:
- **Bảng registry**: # | Tên giấy phép | Cơ quan cấp | Số hiệu | Ngày cấp | Ngày hết hạn | Tình trạng (Đang hiệu lực/Sắp hết hạn/Đã hết hạn) | Người phụ trách | Ghi chú
- **Phân nhóm**: Theo lĩnh vực (PCCC, ATTP, Môi trường, Lao động, Ngành đặc thù...)
- **Alert calendar**: Bảng cảnh báo gia hạn trước 90/60/30 ngày
- **Quy trình gia hạn**: Tóm tắt hồ sơ & thời gian xử lý cho mỗi loại

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Danh sách giấy phép con (Sub-licenses & Permits Registry).

CONTEXT:
- DN: [Tên] — Ngành: [ngành chính + phụ]
- Ngành có điều kiện: [Có/Không] — Chi tiết: [liệt kê]
- XNK: [Có/Không] — PCCC: [Có/Không] — ATTP: [Có/Không] — Môi trường: [Có/Không]
- Địa bàn: [tỉnh/thành]

FORMAT:
- Registry table: # | Giấy phép | Cơ quan | Số | Ngày cấp | Hạn | Status (🟢🟡🔴) | Owner | Notes
- Alert section: Sắp hết hạn trong 90 ngày → highlight đỏ
- Phân nhóm theo lĩnh vực
- Quy trình gia hạn tóm tắt: Loại | Hồ sơ cần | Thời gian | Chi phí | Nộp tại
- Để trống để DN điền thông tin thực tế

TONE: Hành chính, chuẩn mực.
LENGTH: 3-5 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
