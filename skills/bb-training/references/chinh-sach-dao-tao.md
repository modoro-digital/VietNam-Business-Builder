### PROMPT 01: Training Policy (Chính sách Đào tạo)

#### Mô tả
Chính sách đào tạo tổng thể của DN — quy định nguyên tắc, mục tiêu, quyền & nghĩa vụ của công ty và nhân viên trong đào tạo, ngân sách đào tạo, cam kết phục vụ sau đào tạo, quy trình đề xuất & phê duyệt, và cơ chế đánh giá. Là nền tảng pháp lý nội bộ cho toàn bộ hoạt động L&D.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN có ngân sách đào tạo riêng không? Tỷ lệ % trên quỹ lương hoặc doanh thu?
2. Nhân viên có cam kết phục vụ sau đào tạo không? (ví dụ: đào tạo > 10 triệu → cam kết 12 tháng)
3. Hình thức đào tạo: nội bộ (in-house) / bên ngoài / online / kết hợp?
4. Ai có quyền đề xuất đào tạo? Quy trình duyệt?
5. Có chính sách hỗ trợ nhân viên tự học không? (học phí, thời gian, chứng chỉ)
6. Có ràng buộc pháp lý đặc thù ngành? (an toàn lao động, PCCC, chứng chỉ hành nghề...)

#### Template gợi ý
Cấu trúc POL:
- **Điều 1-3** — Mục đích, Phạm vi áp dụng, Thuật ngữ & Định nghĩa
- **Điều 4** — Nguyên tắc đào tạo: Liên tục, Có kế hoạch, Gắn với chiến lược, Đo lường được
- **Điều 5** — Phân loại đào tạo: Bắt buộc (compliance) / Kỹ năng nghề / Phát triển cá nhân / Lãnh đạo
- **Điều 6** — Quyền & Nghĩa vụ: Công ty cam kết gì / Nhân viên cam kết gì
- **Điều 7** — Ngân sách: Phương pháp xác định, phê duyệt, tracking
- **Điều 8** — Quy trình đề xuất & phê duyệt đào tạo
- **Điều 9** — Cam kết phục vụ sau đào tạo & Hoàn trả chi phí
- **Điều 10** — Đánh giá hiệu quả đào tạo (tham chiếu Kirkpatrick)
- **Điều 11** — Lưu trữ hồ sơ đào tạo
- **Điều 12** — Xử lý vi phạm
- **Phụ lục**: Bản cam kết đào tạo, Đơn đề xuất đào tạo mẫu

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Training Policy (Chính sách Đào tạo).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- Ngân sách đào tạo: [% quỹ lương hoặc số tiền cố định]
- Cam kết phục vụ: [có/không] — Chi tiết: [điều kiện]
- Hình thức: [nội bộ / bên ngoài / online / kết hợp]
- Đào tạo bắt buộc ngành: [loại chứng chỉ/giấy phép]
- Hỗ trợ tự học: [có/không] — [chi tiết]

FORMAT:
- Đánh số điều liên tục, ngôn ngữ rõ ràng
- Training classification matrix: Loại | Bắt buộc/Tự nguyện | Đối tượng | Tần suất | Ngân sách | Ví dụ
- Budget allocation: Category | % Budget | Approval level | Cap per person
- Approval flowchart: Mermaid — Đề xuất → Line Manager → HR → Finance → CEO (theo mức)
- Cam kết phục vụ: Bảng Chi phí đào tạo | Thời gian cam kết | Hoàn trả nếu nghỉ sớm
- Training hours target: Bảng Level | Min hours/year | Mandatory | Optional
- Record retention: Bảng Loại hồ sơ | Thời gian lưu | Format | Storage
- Acknowledgment form: Cam kết tuân thủ chính sách đào tạo

TONE: Chính sách rõ ràng, cân bằng giữa quyền lợi NV và lợi ích DN.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
