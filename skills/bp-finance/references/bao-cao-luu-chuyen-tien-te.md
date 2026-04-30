# P-FIN-18: Cash Flow Statement (Báo cáo Lưu chuyển Tiền tệ)

#### Mô tả
Template Báo cáo Lưu chuyển Tiền tệ theo chuẩn VN — phân tích 3 dòng tiền: hoạt động kinh doanh, hoạt động đầu tư, hoạt động tài chính. Hỗ trợ cả phương pháp trực tiếp và gián tiếp.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phương pháp lập? (Trực tiếp / Gián tiếp — hầu hết DN VN dùng gián tiếp)
2. Chế độ kế toán? (TT200 / TT133)
3. Có hoạt động đầu tư lớn không? (mua/bán TSCĐ, góp vốn liên doanh)
4. Có hoạt động tài chính? (vay/trả nợ, phát hành CP, chia cổ tức)

#### Template gợi ý
Cấu trúc RPT:
- **Phần I** — Dòng tiền từ HĐKD: LNTT → Điều chỉnh (KH, dự phòng, lãi vay...) → Thay đổi vốn lưu động → Tiền thuần HĐKD
- **Phần II** — Dòng tiền từ HĐ Đầu tư: Mua/bán TSCĐ, đầu tư, cho vay
- **Phần III** — Dòng tiền từ HĐ Tài chính: Vay/trả nợ, phát hành CP, cổ tức
- **Tổng hợp** — Net Cash Flow = I + II + III → Tiền đầu kỳ + Net = Tiền cuối kỳ
- **Phân tích** — Free Cash Flow, Cash Conversion Ratio

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Cash Flow Statement (Báo cáo Lưu chuyển Tiền tệ).

CONTEXT:
- DN: [Tên] — Phương pháp: [Trực tiếp / Gián tiếp]
- Chế độ: [TT200 / TT133]
- HĐ đầu tư: [Có/Không] — Chi tiết: [mô tả]
- HĐ tài chính: [Có/Không] — Chi tiết: [mô tả]

FORMAT:
- CFS template theo mẫu B03-DN (TT200) / B03-DNN (TT133)
- 3 phần rõ ràng: HĐKD | HĐ Đầu tư | HĐ Tài chính
- Reconciliation: Tiền đầu kỳ + Net Cash = Tiền cuối kỳ (= Balance Sheet)
- Analysis: Free Cash Flow = CFO - CapEx
- Cash Conversion: NI → CFO → Ratio → Interpretation
- Chart data: 3 dòng tiền × 12 tháng, stacked bar

TONE: Tài chính chính thức.
LENGTH: 3-5 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
