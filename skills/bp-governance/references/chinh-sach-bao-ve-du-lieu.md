# PROMPT 18: Chính sách bảo vệ dữ liệu (Data Protection Policy)

#### Mô tả
Chính sách bảo vệ dữ liệu cá nhân — tuân thủ Nghị định 13/2023/NĐ-CP (Bảo vệ dữ liệu cá nhân Việt Nam) và tham khảo GDPR. Quy định thu thập, xử lý, lưu trữ, chia sẻ, xóa dữ liệu cá nhân.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN thu thập những loại dữ liệu cá nhân nào? (khách hàng, nhân sự, đối tác)
2. Kênh thu thập: website, app, cửa hàng, telesales, social media?
3. Dữ liệu lưu ở đâu? (server VN / cloud nước ngoài)
4. Có chia sẻ dữ liệu với bên thứ 3 không? (quảng cáo, analytics, đối tác)
5. Có DPO (Data Protection Officer) hoặc người phụ trách không?
6. Có hoạt động xuyên biên giới không? (cần tuân thủ GDPR?)

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích, Phạm vi, Cam kết
- **Phần 2** — Định nghĩa: Dữ liệu cá nhân, Dữ liệu nhạy cảm, Chủ thể, Bên kiểm soát, Bên xử lý
- **Phần 3** — Nguyên tắc xử lý: Hợp pháp, Minh bạch, Giới hạn mục đích, Tối thiểu hóa, Chính xác, Hạn chế lưu trữ, Bảo mật
- **Phần 4** — Thu thập: Loại dữ liệu, Mục đích, Cơ sở pháp lý, Đồng ý
- **Phần 5** — Lưu trữ & Bảo mật: Thời hạn, Biện pháp kỹ thuật, Access control
- **Phần 6** — Chia sẻ với bên thứ 3: Điều kiện, DPA template
- **Phần 7** — Quyền của chủ thể: Truy cập, Chỉnh sửa, Xóa, Di chuyển, Rút đồng ý
- **Phần 8** — Xử lý sự cố rò rỉ: Quy trình 72 giờ
- **Phần 9** — Vai trò & Trách nhiệm: DPO, IT, HR, Marketing
- **Phụ lục**: Consent form, Data mapping template, Breach notification template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách bảo vệ dữ liệu (Data Protection Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Dữ liệu thu thập: [loại: KH, NV, ĐT]
- Kênh: [website / app / offline / social]
- Storage: [server VN / cloud / hybrid]
- Chia sẻ bên thứ 3: [Có/Không] — [liệt kê]
- DPO: [Có/Không]
- Xuyên biên giới: [Có/Không]
- Cơ sở pháp lý: NĐ 13/2023/NĐ-CP + GDPR (nếu có yếu tố EU)

FORMAT:
- Chia phần rõ ràng, có mục lục
- Data Mapping table: Loại DL | Nguồn | Mục đích | CSPL | Thời hạn lưu | Chia sẻ
- Quyền chủ thể: Bảng quyền + cách thực hiện + SLA phản hồi
- Breach Response flowchart: Phát hiện → 72h → Thông báo → Khắc phục
- Phụ lục: Consent form, Data Processing Agreement template, Breach report template

TONE: Compliance — nghiêm túc, minh bạch, bảo vệ quyền lợi.
LENGTH: 12-18 trang A4.

CROSS-REFERENCE: Đây là chính sách pháp lý bảo vệ dữ liệu. Quy chế bảo mật nhân sự xem bp-people/Quy chế bảo mật thông tin. Chính sách an ninh mạng kỹ thuật xem bp-product-tech/Chính sách an ninh mạng.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
