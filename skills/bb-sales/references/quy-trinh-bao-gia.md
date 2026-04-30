### PROMPT 08: SOP Quy trình báo giá (Quotation Process SOP)

#### Mô tả
Quy trình chuẩn hóa từ lúc nhận yêu cầu báo giá đến khi gửi báo giá, follow up, và chốt đơn. Đảm bảo báo giá chính xác, kịp thời, đúng thẩm quyền, và theo dõi được trạng thái.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ai tiếp nhận yêu cầu báo giá? (Sales rep / Admin / Website form)
2. Thời gian phản hồi báo giá cam kết? (VD: 24h / 48h / 72h)
3. Ai tính giá? Ai duyệt giá? Có cần nhiều cấp duyệt không?
4. Báo giá gửi dạng gì? (PDF / Email / Hệ thống / In)
5. Hiệu lực báo giá? (7 ngày / 15 ngày / 30 ngày)
6. Quy trình follow up: bao nhiêu lần? Khoảng cách bao lâu?
7. Báo giá đặc biệt (giá ưu đãi, dự án lớn) — quy trình riêng?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Quy trình tổng**: Flowchart 8 bước — Tiếp nhận → Thu thập yêu cầu → Tính giá → Duyệt → Tạo báo giá → Gửi → Follow up → Chốt/Hủy
- **Chi tiết từng bước**: Action, owner, timeline, output
- **Phân cấp duyệt giá**: Giá chuẩn (auto) / Giá chiết khấu (Sales Manager) / Giá đặc biệt (Director)
- **SLA báo giá**: Cam kết thời gian phản hồi
- **Follow-up Protocol**: Lịch follow up + script mẫu
- **Tracking**: Template theo dõi trạng thái báo giá
- **Phụ lục**: Quotation request form, Price calculation sheet

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quy trình báo giá (Quotation Process).

CONTEXT:
- DN: [Tên] — SP/DV: [số loại]
- Tiếp nhận: [Sales rep / Admin / Website form]
- SLA phản hồi: [24h / 48h / 72h]
- Duyệt giá: [Sales rep / Manager / Director — tùy mức]
- Format: [PDF / Email / Hệ thống]
- Hiệu lực: [7 / 15 / 30 ngày]
- Follow up: [số lần] — Khoảng cách: [ngày]

FORMAT:
- Flowchart: Mermaid — 8 bước + decision points (giá chuẩn vs đặc biệt)
- Per-step: Bảng Bước | Action | Owner | Timeline | Output | Kiểm soát
- Approval matrix: Bảng Mức giá | Sales Rep | Sales Manager | Director | CEO
- SLA dashboard: Loại RFQ | SLA | Actual avg | Status (đạt/không)
- Follow-up schedule: Ngày 1 | Ngày 3 | Ngày 7 | Ngày 14 — Action + Script ngắn
- Tracking template: RFQ # | KH | SP | Value | Sent date | Status | Next action | Owner
- Error handling: Sai giá / Quá hạn / KH không phản hồi → Xử lý

TONE: SOP chuẩn — rõ ràng, step-by-step.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
