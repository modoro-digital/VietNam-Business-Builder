### PROMPT 06: Chính sách hoàn tiền/bảo hành (Refund & Warranty Policy)

#### Mô tả
Chính sách hoàn tiền và bảo hành — điều kiện, quy trình, thời hạn, trách nhiệm, ngoại lệ. Tài liệu vừa dùng nội bộ (CS team follow) vừa công bố cho KH (website, hợp đồng).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ có bảo hành không? Thời hạn?
2. Điều kiện hoàn tiền hiện tại? (trong 7 ngày / 30 ngày / không hoàn)
3. Phương thức hoàn tiền? (tiền mặt / chuyển khoản / credit / đổi hàng)
4. Ai duyệt hoàn tiền? Hạn mức duyệt?
5. Có trường hợp ngoại lệ nào? (hàng sale, custom, digital...)
6. Luật bảo vệ người tiêu dùng áp dụng? (Luật BVQLNTD 2023)

#### Template gợi ý
Cấu trúc POL:
- **Chính sách hoàn tiền**: Điều kiện, thời hạn, quy trình, phương thức, timeline xử lý
- **Chính sách bảo hành**: Phạm vi, thời hạn, điều kiện mất bảo hành, quy trình claim
- **Đổi/trả hàng**: Điều kiện, thời hạn, chi phí vận chuyển
- **Ngoại lệ**: Các trường hợp không áp dụng
- **Trách nhiệm**: DN vs KH
- **Cơ sở pháp lý**: Tham chiếu luật BVQLNTD

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách hoàn tiền & bảo hành (Refund & Warranty Policy).

CONTEXT:
- DN: [Tên] — SP/DV: [liệt kê]
- Bảo hành: [thời hạn] — Phạm vi: [mô tả]
- Hoàn tiền: [điều kiện] — Thời hạn: [ngày]
- Phương thức hoàn: [tiền mặt / CK / credit / đổi hàng]
- Duyệt hoàn tiền: [ai] — Hạn mức: [VNĐ]
- Ngoại lệ: [liệt kê]

FORMAT:
- Refund policy: Bảng Điều kiện | Thời hạn | % hoàn | Phương thức | Timeline xử lý
- Warranty policy: Bảng SP | Thời hạn BH | Phạm vi | Điều kiện mất BH | Quy trình claim
- Refund process: Flowchart Mermaid — Yêu cầu → Kiểm tra điều kiện → Duyệt → Xử lý → Hoàn thành
- Warranty claim process: Flowchart — Báo lỗi → Kiểm tra BH → Sửa/Đổi → Giao lại
- Exception list: Trường hợp | Lý do không áp dụng | Giải pháp thay thế
- Customer-facing version: Bản rút gọn — ngôn ngữ thân thiện, có thể post lên website
- Internal version: Bản đầy đủ — bao gồm hạn mức duyệt, escalation

TONE: Rõ ràng, công bằng, bảo vệ cả KH và DN.
LENGTH: 4-6 trang A4.
```



---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
