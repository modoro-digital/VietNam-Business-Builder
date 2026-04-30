# P-PPL-10: Quy chế bảo mật thông tin (Information Security Policy)

#### Mô tả
Quy chế phân loại thông tin, quy tắc bảo mật, quyền truy cập, xử lý vi phạm bảo mật. Bổ sung cho NDA trong 01-Governance — NDA là cam kết pháp lý, còn đây là quy tắc hành vi hàng ngày về bảo mật.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phân loại thông tin: mấy mức? (VD: Public / Internal / Confidential / Secret)
2. Dữ liệu nhạy cảm: KH, tài chính, công nghệ, nhân sự — cái nào quan trọng nhất?
3. Chính sách BYOD (Bring Your Own Device): Cho phép không?
4. Social media: NV có được đăng về công ty không? Quy tắc?
5. Quy trình khi phát hiện rò rỉ/vi phạm bảo mật?
6. Có DPO (Data Protection Officer) hoặc IT Security riêng không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích, Phạm vi, Định nghĩa
- **Phần 2** — Phân loại thông tin: 4 mức + ví dụ mỗi mức + cách xử lý
- **Phần 3** — Quyền truy cập: Ma trận Role × Loại thông tin → Access level
- **Phần 4** — Quy tắc bảo mật hàng ngày: Password, khóa máy, clean desk, chia sẻ file
- **Phần 5** — BYOD & Thiết bị cá nhân: Cho phép/không, điều kiện
- **Phần 6** — Social media: Được/không được nói gì về công ty
- **Phần 7** — Xử lý sự cố bảo mật: Phát hiện → Báo cáo → Cách ly → Điều tra → Khắc phục
- **Phần 8** — Vi phạm & Hình thức xử lý: Nhắc nhở → Kỷ luật → Sa thải → Pháp lý

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế bảo mật thông tin (Information Security Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- Phân loại: [Public / Internal / Confidential / Secret]
- Dữ liệu nhạy cảm nhất: [KH / Tài chính / Công nghệ / Nhân sự]
- BYOD: [Cho phép / Không / Có điều kiện]
- DPO/IT Security: [Có/Không]
- Liên kết: NDA trong 01-Governance

FORMAT:
- Classification matrix: Mức | Định nghĩa | Ví dụ | Ai được access | Cách lưu trữ | Cách chia sẻ | Cách hủy
- Access control: Role × Info type = Read/Write/None — bảng ma trận
- Daily security rules: 10 quy tắc — poster-friendly, treo gần máy tính
- BYOD rules: Thiết bị | Cho phép | Điều kiện | MDM required
- Social media dos/don'ts: 5 được + 5 không
- Incident response flowchart: Mermaid — Phát hiện → Báo IT → Cách ly → GĐ → Điều tra → Report
- Violation penalties: Bảng Vi phạm | Mức 1 (nhắc) | Mức 2 (kỷ luật) | Mức 3 (sa thải/pháp lý)

TONE: Nghiêm túc, bảo mật, nhưng viết đủ dễ hiểu cho non-tech.
LENGTH: 6-8 trang A4.

CROSS-REFERENCE: Đây là quy chế bảo mật cho nhân sự. Chính sách bảo vệ dữ liệu pháp lý xem bb-governance/Chính sách bảo vệ dữ liệu. An ninh mạng kỹ thuật xem bb-product-tech/Chính sách an ninh mạng.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
