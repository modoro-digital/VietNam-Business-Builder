# P-FIN-17: Balance Sheet (Bảng Cân đối Kế toán)

#### Mô tả
Template Bảng Cân đối Kế toán theo chuẩn mực kế toán VN. Phân tích cơ cấu tài sản, nguồn vốn, và sự thay đổi qua các kỳ.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Chế độ kế toán? (TT200 / TT133)
2. Cần so sánh kỳ nào? (Cuối kỳ vs Đầu năm / Cuối kỳ trước)
3. Có tài sản cố định lớn không? (bất động sản, máy móc, phương tiện)
4. Có vay nợ dài hạn không? (ngân hàng, trái phiếu)
5. Tần suất lập? (hàng quý / hàng năm)

#### Template gợi ý
Cấu trúc RPT:
- **Balance Sheet Statement** — Mẫu B01-DN (TT200) / B01-DNN (TT133)
- **Tài sản**: Ngắn hạn (tiền, phải thu, hàng tồn, khác) + Dài hạn (TSCĐ, đầu tư, khác)
- **Nguồn vốn**: Nợ phải trả (ngắn hạn + dài hạn) + Vốn chủ sở hữu
- **Phân tích cơ cấu**: % từng khoản / Tổng tài sản
- **Phân tích biến động**: So sánh 2 kỳ, giải thích thay đổi lớn
- **Key Ratios**: Current Ratio, Quick Ratio, D/E, ROE, ROA

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Balance Sheet (Bảng Cân đối Kế toán).

CONTEXT:
- DN: [Tên] — Chế độ: [TT200 / TT133]
- So sánh: [Đầu năm / Cuối kỳ trước]
- TSCĐ: [Có/Không] — Giá trị lớn: [liệt kê]
- Vay nợ: [Có/Không] — Chi tiết: [ngắn hạn / dài hạn]

FORMAT:
- BS template theo mẫu B01-DN hoặc B01-DNN — 2 cột (Cuối kỳ | Đầu năm)
- Cơ cấu phân tích: % column cho mỗi khoản / Tổng
- Biến động: Thay đổi $ | Thay đổi % | Commentary
- Ratio cards: Current Ratio | Quick Ratio | D/E | ROE | ROA + benchmark
- Chart data: Tài sản structure pie + Nguồn vốn structure pie
- Working Capital analysis: CA - CL = NWC, trend

TONE: Tài chính chính thức.
LENGTH: 3-5 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
