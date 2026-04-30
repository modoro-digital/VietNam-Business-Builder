### PROMPT 07: Chính sách CNTT (IT Policy)

#### Mô tả
Chính sách quy định việc sử dụng thiết bị công nghệ, phần mềm, email, internet, và dữ liệu trong DN. Bao gồm quy định BYOD, acceptable use, data classification, và trách nhiệm của nhân viên. Là nền tảng cho an ninh thông tin và compliance.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN cấp thiết bị hay BYOD (nhân viên dùng máy cá nhân)?
2. Có email domain riêng? Quy định sử dụng email?
3. Chính sách internet? (filter / monitor / tự do)
4. Dữ liệu nhạy cảm? (khách hàng, tài chính, nhân sự — cần phân loại)
5. Có remote work không? Chính sách truy cập từ xa?
6. Phần mềm: cài tự do hay phải qua IT duyệt?

#### Template gợi ý
Cấu trúc POL:
- **Điều 1-3** — Mục đích, Phạm vi, Thuật ngữ
- **Điều 4** — Thiết bị & Phần cứng: Cấp phát, bảo quản, trả lại khi nghỉ, BYOD
- **Điều 5** — Phần mềm: Danh sách cho phép, cài đặt, license, cấm crack/pirate
- **Điều 6** — Email & Truyền thông: Sử dụng email công ty, chữ ký email, lưu trữ
- **Điều 7** — Internet: Acceptable use, restricted sites, monitoring notice
- **Điều 8** — Data Classification: Public / Internal / Confidential / Restricted
- **Điều 9** — Remote Access: VPN, MFA, thiết bị approved
- **Điều 10** — Incident Reporting: Báo cáo sự cố IT, mất thiết bị, data breach
- **Điều 11** — Xử lý vi phạm
- **Phụ lục**: Bản cam kết sử dụng IT, Danh sách phần mềm approved

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách CNTT (IT Policy).

CONTEXT:
- DN: [Tên] — Nhân sự: [số] — Remote: [Có/Không]
- Thiết bị: [Công ty cấp / BYOD / Hybrid]
- Email domain: [Có/Không] — Provider: [Google Workspace / M365 / khác]
- Dữ liệu nhạy cảm: [loại]
- Internet: [filter / monitor / tự do]

FORMAT:
- Đánh số điều liên tục, ngôn ngữ rõ ràng cho mọi NV
- Data classification matrix: Level | Definition | Examples | Handling | Storage | Sharing
- BYOD requirements: Bảng tiêu chuẩn thiết bị | OS version | Security apps | Enrollment
- Software whitelist: Bảng Category | Approved tools | Alternatives banned
- Email signature template: Chuẩn hóa format
- Incident reporting flowchart: Mermaid — Phát hiện → Báo cáo → Phân loại → Xử lý → Review
- Acknowledgment form: Cam kết ký bởi mỗi NV

TONE: Rõ ràng, dễ hiểu cho non-tech, có ví dụ cụ thể.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
