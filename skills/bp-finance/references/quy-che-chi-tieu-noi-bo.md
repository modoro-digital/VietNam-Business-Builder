# P-FIN-02: Quy chế chi tiêu nội bộ (Internal Spending Regulations)

#### Mô tả
Quy chế chi tiết về hạn mức, quy trình duyệt chi, danh mục chi phí được phép, và các quy định kiểm soát chi tiêu hàng ngày. Đây là file được TOÀN BỘ nhân viên sử dụng — phải rõ ràng, dễ hiểu, dễ tra cứu.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hạn mức chi tiêu không cần duyệt của mỗi cấp? (VD: NV < 500K, TP < 5 triệu, GĐ < 50 triệu)
2. Danh mục chi phí phổ biến? (VD: văn phòng phẩm, đi lại, tiếp khách, hội nghị...)
3. Chi phí nào cần duyệt đặc biệt? (VD: quảng cáo > X triệu, mua tài sản > Y triệu)
4. Quy trình duyệt: email / phần mềm / giấy? Bao nhiêu cấp duyệt?
5. Có advance (tạm ứng) không? Quy định hoàn ứng trong bao lâu?
6. Chi tiêu ngoài danh mục — quy trình xin phê duyệt đặc biệt?

#### Template gợi ý
Cấu trúc POL:
- **Điều 1-3** — Mục đích, Phạm vi, Thuật ngữ
- **Điều 4** — Nguyên tắc chi tiêu: Có trong budget, đúng mục đích, đủ chứng từ, đã phê duyệt
- **Điều 5** — Phân cấp duyệt chi: Bảng hạn mức chi tiết theo cấp × loại chi phí
- **Điều 6** — Danh mục chi phí: Liệt kê + định mức từng loại (VD: tiếp khách max 500K/lần)
- **Điều 7** — Quy trình duyệt chi: Flowchart từ lúc phát sinh → duyệt → chi → hoàn chứng từ
- **Điều 8** — Tạm ứng & Hoàn ứng: Hạn mức, thời hạn, xử lý khi không hoàn ứng
- **Điều 9** — Chi tiêu đặc biệt: Ngoài danh mục, vượt hạn mức, khẩn cấp
- **Điều 10** — Xử lý vi phạm: Mức phạt, trách nhiệm bồi thường
- **Phụ lục**: Bảng định mức chi phí, Mẫu giấy đề nghị thanh toán

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế chi tiêu nội bộ (Internal Spending Regulations).

CONTEXT:
- DN: [Tên] — Quy mô: [nhân sự] — Doanh thu: [số/năm]
- Hạn mức duyệt chi: NV [___] | TP [___] | GĐ [___] | HĐQT [___]
- Quy trình duyệt: [email / phần mềm / giấy]
- Số cấp duyệt: [số]
- Tạm ứng: [Có/Không] — Thời hạn hoàn ứng: [ngày]

FORMAT:
- Đánh số điều liên tục, ngôn ngữ rõ ràng cho mọi cấp nhân viên
- Bảng phân cấp: Loại chi phí | < X triệu (NV) | < Y triệu (TP) | < Z triệu (GĐ) | > Z triệu (HĐQT)
- Bảng định mức: Loại | Định mức/lần | Định mức/tháng | Ghi chú
- Flowchart duyệt chi: Mermaid — Phát sinh → Đề nghị → Duyệt → Chi → Chứng từ → Hạch toán
- FAQ: 10 tình huống phổ biến (VD: taxi lúc tối khuya, tiếp khách ngoài định mức...)

TONE: Rõ ràng, dễ hiểu, thực tế — ai cũng đọc được.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
