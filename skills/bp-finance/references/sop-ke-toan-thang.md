# P-FIN-12: SOP Kế toán tháng — Monthly Close (Month-End Closing SOP)

#### Mô tả
Quy trình kế toán tháng (monthly close) — checklist tất cả công việc kế toán cần hoàn thành trước khi "đóng sổ" mỗi tháng. Bao gồm hạch toán, đối chiếu, bút toán điều chỉnh, lập báo cáo.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Timeline close: ngày mấy hàng tháng phải xong? (VD: ngày 5 tháng sau)
2. Bao nhiêu kế toán viên tham gia close?
3. Phần mềm kế toán? Tự động hóa được bao nhiêu %?
4. Các bút toán điều chỉnh thường gặp? (khấu hao, phân bổ, trích trước, dự phòng)
5. Báo cáo nào cần nộp sau khi close? (nội bộ / thuế / ngân hàng)

#### Template gợi ý
Cấu trúc SOP:
- **Timeline Close** — Gantt: Day 1 → Day 5 (hoặc custom), mỗi ngày làm gì
- **Pre-Close Checklist** — Trước khi close: đối chiếu ngân hàng, kiểm quỹ, cut-off
- **Close Checklist** — Trong khi close: bút toán điều chỉnh, khấu hao, phân bổ, dự phòng
- **Post-Close Checklist** — Sau khi close: review, lập BC, nộp thuế
- **Reconciliation** — Đối chiếu: sổ cái vs sổ phụ, NH vs sổ sách, kho vs sổ sách
- **Reporting** — Danh sách BC cần nộp + deadline + người nhận
- **Sign-off** — Kế toán → KTT → CFO/GĐ

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Monthly Close (Kế toán tháng).

CONTEXT:
- DN: [Tên] — Timeline close: ngày [X] hàng tháng
- Số kế toán: [số] — Phần mềm: [tên]
- Bút toán điều chỉnh chính: [liệt kê]
- BC cần nộp: [nội bộ / thuế GTGT / thuế TNCN / ngân hàng]

FORMAT:
- Gantt chart: Day 1-5 × Tasks × Owner — Mermaid hoặc bảng
- Pre-Close checklist: 10-15 mục ☐ + Owner + Deadline
- Close checklist: 15-20 mục ☐ + Bút toán mẫu
- Post-Close checklist: 8-10 mục ☐ + BC + Deadline
- Reconciliation template: Sổ cái vs Sổ phụ vs Nguồn → Chênh lệch → Xử lý
- Sign-off sheet: Task | Done by | Reviewed by | Date | Notes
- Common errors: Bảng lỗi hay gặp + cách phòng tránh

TONE: SOP chuẩn, operational, checklist-oriented.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
