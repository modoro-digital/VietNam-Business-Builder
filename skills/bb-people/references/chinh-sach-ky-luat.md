### PROMPT 26: Disciplinary Policy (Chính sách kỷ luật)

#### Mô tả
Chính sách kỷ luật lao động — định nghĩa các hình thức kỷ luật, quy trình xử lý vi phạm, quyền và nghĩa vụ của nhân viên trong quá trình điều tra. Tuân thủ chặt chẽ Bộ luật Lao động 2019 (Điều 122-128) để tránh khiếu nại lao động, bồi thường, và rủi ro pháp lý.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Đã có Nội quy lao động được Sở LĐTBXH duyệt chưa?
2. Có Công đoàn cơ sở không?
3. Số lượng nhân viên: dưới 10 hay từ 10 trở lên (ảnh hưởng yêu cầu Nội quy bằng văn bản)?
4. Các loại vi phạm thường gặp (đi muộn, nghỉ không phép, gian lận, đánh nhau, tiết lộ bí mật)?
5. Đã từng có vụ kỷ luật/sa thải nào dẫn đến tranh chấp chưa?
6. Có hệ thống chấm công, camera, log để có evidence không?
7. Mức độ nghiêm khắc mong muốn: Strict (zero-tolerance một số lỗi) hay Lenient (warning trước)?

#### Template gợi ý
Cấu trúc POL:
- **Mục đích & Phạm vi**: Áp dụng cho ai, không áp dụng cho ai
- **Cơ sở Pháp lý**: Bộ luật Lao động 2019 (Điều 117-128) + Nội quy LĐ + HĐLĐ
- **Nguyên tắc Kỷ luật**: 5 nguyên tắc (Đúng người, đúng thời điểm, một lỗi một hình thức, có chứng cứ, công khai-minh bạch)
- **4 Hình thức Kỷ luật** (theo Bộ luật LĐ 2019 Điều 124):
  - Khiển trách
  - Kéo dài thời hạn nâng lương ≤ 6 tháng
  - Cách chức
  - Sa thải
- **Bảng Phân loại Vi phạm**: Bảng Hành vi vi phạm × Hình thức kỷ luật áp dụng
- **Quy trình Xử lý Kỷ luật** (theo Điều 122):
  - Bước 1: Lập biên bản vi phạm
  - Bước 2: Mời họp xử lý kỷ luật (báo trước ít nhất 5 ngày)
  - Bước 3: Tổ chức họp (có sự tham gia của Công đoàn, người vi phạm, đại diện NSDLĐ)
  - Bước 4: Lập biên bản họp
  - Bước 5: Ban hành Quyết định kỷ luật (trong thời hiệu)
  - Bước 6: Thông báo và lưu hồ sơ
- **Thời hiệu Xử lý**: 6 tháng (có thể kéo dài đến 12 tháng với một số hành vi)
- **Quyền của NLĐ**: Tự bào chữa, mời luật sư, kháng cáo
- **Quy trình Khiếu nại nội bộ**: Trong 30 ngày kể từ ngày nhận quyết định
- **Mẫu biểu đính kèm**: Biên bản vi phạm, Thư mời họp, Biên bản họp, Quyết định kỷ luật
- **Pháp lý**: Toàn văn các điều khoản BLLĐ 2019 liên quan

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách Kỷ luật lao động.

CONTEXT:
- DN: [Tên] — Quy mô: [n nhân viên]
- Có Nội quy LĐ: [đã đăng ký Sở LĐ / chưa]
- Công đoàn cơ sở: [có/không]
- Vi phạm thường gặp: [list]
- Mức độ nghiêm khắc: [Strict / Balanced / Lenient]

FORMAT:
- Cơ sở pháp lý: Trích Điều 117-128 BLLĐ 2019
- Nguyên tắc: 5 nguyên tắc kỷ luật
- 4 hình thức kỷ luật: Định nghĩa từng loại + điều kiện áp dụng + hệ quả
- Bảng phân loại vi phạm: Cột Hành vi | Mức độ (Nhẹ/Vừa/Nặng) | Hình thức kỷ luật | Cơ sở
  • Vi phạm về thời gian (đi muộn, nghỉ không phép)
  • Vi phạm về kỷ luật làm việc (uống rượu, đánh nhau, vắng mặt không lý do)
  • Vi phạm về tài sản (trộm cắp, hư hỏng cố ý)
  • Vi phạm về bảo mật (tiết lộ bí mật KD, pass, dữ liệu KH)
  • Vi phạm về đạo đức (quấy rối, gian lận, hối lộ)
- Quy trình 6 bước: Flowchart + timeline mỗi bước
- Thời hiệu: Bảng Hành vi | Thời hiệu (6 tháng / 12 tháng)
- Quyền NLĐ: Bullet list rõ ràng
- Quy trình khiếu nại: Flowchart 4 bước
- Mẫu biểu: 4 mẫu hoàn chỉnh (Biên bản VP, Mời họp, Biên bản họp, QĐ kỷ luật)
- Phụ lục: Toàn văn Điều 117-128 BLLĐ 2019

TONE: Trang trọng, chính xác pháp lý, không có khoảng xám.
LENGTH: 15-20 trang A4 (bao gồm phụ lục pháp luật).
LƯU Ý: Nên review bởi luật sư lao động trước khi áp dụng chính thức.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
