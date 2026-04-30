# P-FIN-10: SOP Quy trình thu chi (Cash Receipt & Disbursement SOP)

#### Mô tả
Quy trình chuẩn hóa cho mọi giao dịch thu chi trong DN — từ phát sinh, lập chứng từ, phê duyệt, thực hiện thu/chi, đến hạch toán và lưu trữ. Đảm bảo không có giao dịch nào "thoát" khỏi hệ thống kiểm soát.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phương thức thanh toán phổ biến? (Tiền mặt / CK ngân hàng / Ví điện tử / Thẻ)
2. Phần mềm kế toán? (tự động hạch toán hay thủ công?)
3. Số cấp duyệt chi? (1 cấp / 2 cấp / 3 cấp)
4. Có quỹ tiền mặt tại DN không? Hạn mức tồn quỹ?
5. Tần suất nộp tiền ngân hàng?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Thuật ngữ & Viết tắt**
- **Quy trình THU**: Flowchart 6 bước — Phát sinh → Lập phiếu → Xác nhận → Thu → Hạch toán → Lưu
- **Quy trình CHI**: Flowchart 8 bước — Đề nghị → Duyệt → Lập phiếu → Chi → Chứng từ gốc → Hạch toán → Đối chiếu → Lưu
- **Quy định quỹ tiền mặt**: Hạn mức, kiểm quỹ, nộp NH
- **Chứng từ bắt buộc**: Danh sách per loại giao dịch
- **Lưu trữ**: Thời hạn, cách sắp xếp, số hóa

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quy trình thu chi.

CONTEXT:
- DN: [Tên] — Phương thức TT: [TM / CK / Ví ĐT / Thẻ]
- Phần mềm: [MISA / Fast / SAP / Excel]
- Số cấp duyệt chi: [số]
- Quỹ tiền mặt: [Có/Không] — Hạn mức: [số]
- Cơ sở pháp lý: Luật Kế toán 2015, TT200/TT133

FORMAT:
- Flowchart THU: Mermaid — 6 bước rõ ràng
- Flowchart CHI: Mermaid — 8 bước rõ ràng, highlight điểm kiểm soát
- Bảng chứng từ: Loại GD | Chứng từ cần | Ai lập | Ai duyệt | Số bản
- Quy định quỹ TM: Hạn mức | Tần suất kiểm | Quy trình nộp NH
- Checklist cuối ngày: 5 mục kiểm tra cho kế toán
- Error handling: Bảng lỗi phổ biến | Cách xử lý | Escalation

TONE: SOP chuẩn — rõ ràng, step-by-step, không mơ hồ.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
