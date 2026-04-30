# P-FIN-15: Bảng kê thuế GTGT (VAT Declaration Sheet)

#### Mô tả
Template bảng kê thuế GTGT đầu vào/đầu ra theo mẫu kê khai của Tổng cục Thuế. Hướng dẫn kê khai đúng, đủ, đúng hạn — giảm rủi ro bị phạt thuế.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phương pháp tính thuế GTGT? (Khấu trừ / Trực tiếp)
2. Kỳ kê khai? (Hàng tháng / Hàng quý — phụ thuộc doanh thu)
3. Phần mềm hỗ trợ kê khai? (HTKK, iHTKK, eTax, phần mềm kế toán tích hợp)
4. Có hàng hóa/dịch vụ thuộc diện thuế suất 0%, 5%, 8%, 10% không?
5. Có hoạt động XNK chịu thuế GTGT nhập khẩu không?

#### Template gợi ý
Cấu trúc FRM:
- **Hướng dẫn tổng quan**: Mẫu nào, nộp ở đâu, deadline, mức phạt chậm nộp
- **Bảng kê đầu ra** (Phụ lục 01-1/GTGT): Hóa đơn bán ra, giá trị, thuế suất, tiền thuế
- **Bảng kê đầu vào** (Phụ lục 01-2/GTGT): Hóa đơn mua vào, giá trị, thuế suất, tiền thuế được khấu trừ
- **Tờ khai 01/GTGT**: Tóm tắt thuế đầu ra - đầu vào = thuế phải nộp
- **Checklist trước khi nộp**: 10 mục kiểm tra
- **Lưu ý**: Hóa đơn không hợp lệ, hóa đơn quá hạn kê khai, kê khai bổ sung

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Bảng kê thuế GTGT (VAT Declaration Sheet).

CONTEXT:
- DN: [Tên] — MST: [số]
- Phương pháp: [Khấu trừ / Trực tiếp]
- Kỳ kê khai: [Tháng / Quý]
- Phần mềm: [HTKK / eTax / PM kế toán]
- Thuế suất áp dụng: [0% / 5% / 8% / 10%]
- XNK: [Có/Không]

FORMAT:
- Bảng kê đầu ra: STT | Hóa đơn số | Ngày | KH | MST KH | Giá trị CTV | Thuế suất | Tiền thuế
- Bảng kê đầu vào: STT | Hóa đơn số | Ngày | NCC | MST NCC | Giá trị CTV | Thuế suất | Tiền thuế
- Tờ khai tóm tắt: Tổng đầu ra | Tổng đầu vào | Thuế phải nộp | Thuế còn khấu trừ
- Pre-submission checklist: 10 mục ☐
- Lịch nộp thuế: 12 tháng × deadline + reminder T-5 ngày
- FAQ: 10 tình huống kê khai thường gặp

TONE: Thuế — chính xác, tuân thủ, reference cụ thể.
LENGTH: 5-7 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
