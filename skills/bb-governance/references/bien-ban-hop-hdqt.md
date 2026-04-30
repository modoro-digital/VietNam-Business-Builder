# PROMPT 05: Biên bản họp HĐQT Template (Board Meeting Minutes Template)

#### Mô tả
Template chuẩn hóa cho biên bản họp HĐQT/HĐTV. Đảm bảo mọi cuộc họp đều được ghi nhận đúng format pháp lý, đủ nội dung bắt buộc theo Luật DN 2020.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hình DN? (quy định biên bản họp khác nhau cho TNHH vs Cổ phần)
2. Số thành viên HĐQT/HĐTV?
3. Có thư ký HĐQT chuyên trách không?
4. Cuộc họp thường có bao nhiêu nội dung/quyết định?
5. Cần bilingual (Việt-Anh) không? (cho DN có cổ đông nước ngoài)

#### Template gợi ý
Cấu trúc FRM:
- **Header**: Logo, Tên DN, Mã số thuế, "BIÊN BẢN HỌP [HĐQT/HĐTV]"
- **Thông tin cuộc họp**: Số BB, Ngày/Giờ, Địa điểm (hoặc Online), Chủ tọa, Thư ký
- **Danh sách tham dự**: Bảng: Tên | Chức danh | Tỷ lệ sở hữu/biểu quyết | Có mặt ☐
- **Nội dung cuộc họp**: Theo agenda — mỗi mục có: Trình bày | Thảo luận | Biểu quyết | Kết quả
- **Quyết định**: Đánh số, nội dung rõ ràng, % đồng ý
- **Ý kiến bảo lưu** (nếu có)
- **Chữ ký**: Chủ tọa + Thư ký + Tham dự (nếu yêu cầu)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Biên bản họp HĐQT/HĐTV.

CONTEXT:
- Loại hình DN: [loại] — Loại cuộc họp: [HĐQT / HĐTV / Đại hội cổ đông]
- Số thành viên: [số]
- Bilingual: [Có/Không]
- Cơ sở pháp lý: Luật DN 2020, Điều [số điều tương ứng]

FORMAT:
- Template dạng form: các trường để điền được đánh dấu [___]
- Header chuyên nghiệp: Logo placeholder, thông tin DN
- Bảng tham dự: Tên | Chức danh | % biểu quyết | Có mặt/Ủy quyền
- Mỗi nội dung: Số TT | Nội dung | Người trình bày | Kết quả biểu quyết (Đồng ý __ / Không __ / Trắng __)
- Footer: Chữ ký chủ tọa & thư ký, dòng xác nhận pháp lý
- Phụ lục: Checklist nội dung bắt buộc theo luật

TONE: Pháp lý-hành chính, trang trọng.
LENGTH: 3-4 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
