# Quy Tắc Lưu Trữ Tài Liệu Tài Liệu

> **Nguyên tắc bắt buộc:** Mỗi tài liệu được tạo bởi Business Builder plugin PHẢI tuân thủ quy tắc đặt tên và lưu đúng thư mục vào đúng thư mục. Sau khi tạo tài liệu, PHẢI cập nhật file "Hướng Dẫn Sử Dụng Thư Mục" nếu có thay đổi cấu trúc.

---

## 1. QUY TẮC ĐẶT TÊN FILE

### Format chuẩn
```
[Thời gian] [Loại] - [Tên tài liệu] - [Phòng/Version]
```

### Mã thời gian

| Ký hiệu | Ý nghĩa | Ví dụ |
|----------|---------|-------|
| `[STANDARD]` | Tài liệu cố định, không có hạn sử dụng | SOP, JD, Quy chế |
| `[2025]` | Tài liệu theo năm | Kế hoạch năm, OKR, Ngân sách |
| `[2025-Q1]` | Tài liệu theo quý | Báo cáo quý |
| `[2025-04]` | Tài liệu theo tháng | Báo cáo tháng, biên bản họp |

### Mã loại tài liệu

| Mã | Loại | Mã | Loại |
|----|------|-----|------|
| **SOP** | Quy trình/Hướng dẫn | **JD** | Mô tả công việc |
| **QC** | Quy chế/Chính sách | **BC** | Báo cáo |
| **KH** | Kế hoạch | **HĐ** | Hợp đồng |
| **BB** | Biên bản | **TL** | Tài liệu/Slide |

### Phân loại tài liệu

| Loại | Đặc điểm | Mã thời gian |
|------|----------|-------------|
| **Cố định** | Ít thay đổi, chỉ cập nhật khi thay đổi chính sách lớn | `[STANDARD]` |
| **Theo năm** | Cập nhật định kỳ theo năm hoặc quý | `[2025]`, `[2025-Q1]` |
| **Liên tục** | Cập nhật thường xuyên (tuần/tháng) | `[2025-04]` |

### Ví dụ đặt tên chuẩn
- `[STANDARD] SOP - Quy trình tiếp nhận khách hàng mới - CSKH v2.0`
- `[2025] KH - Kế hoạch kinh doanh năm 2025 - CEO`
- `[2025-Q1] BC - Báo cáo doanh thu Q1.2025 - Sales`
- `[STANDARD] QC - Nội quy lao động - HR v1.0`
- `[STANDARD] JD - Mô tả công việc - Marketing Manager v1.2`

---

## 2. CẤU TRÚC THƯ MỤC CHUẨN

| Mã | Thư mục | Phân quyền |
|----|---------|-----------|
| 00 | Hội đồng Điều hành | CEO + GĐ các khối |
| 01 | Nhân sự | GĐ HC + NS |
| 02 | Tài chính & Kế toán | GĐ HC + TC/KT |
| 03 | Hành chính & Vận hành | Toàn công ty (view) |
| 04 | Kinh doanh & Marketing | GĐ KD + MKT + Sales |
| 05 | Sản phẩm & Công nghệ | GĐ CN + Dev |
| 06 | Khách hàng & Dịch vụ | GĐ CSKH + Support |
| 07 | Công ty thành viên & Dự án | Theo phân quyền dự án |
| 08 | Đào tạo & Phát triển | Toàn công ty |
| 09 | Báo cáo tổng hợp | Ban lãnh đạo |
| _ARCHIVE | Tài liệu cũ | Toàn công ty (chỉ đọc) |

---

## 3. MAPPING: SKILL → THƯ MỤC DRIVE

### bp-governance (Quản Trị & Pháp Lý)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Điều lệ công ty | 00 | 00.1 Hồ sơ pháp lý | `[STANDARD] QC - Điều lệ công ty - CEO v1.0` |
| Checklist ĐKKD | 00 | 00.1 Hồ sơ pháp lý | `[STANDARD] TL - Checklist hồ sơ ĐKKD - CEO v1.0` |
| Giấy phép con | 00 | 00.1 Hồ sơ pháp lý | `[STANDARD] TL - Danh sách giấy phép con - HC v1.0` |
| Thỏa thuận cổ đông | 00 | 00.1 Hồ sơ pháp lý | `[STANDARD] HĐ - Thỏa thuận cổ đông - CEO v1.0` |
| Quy chế HĐQT | 00 | 00.5 Cơ cấu tổ chức | `[STANDARD] QC - Quy chế HĐQT - CEO v1.0` |
| Quy chế BGĐ | 00 | 00.5 Cơ cấu tổ chức | `[STANDARD] QC - Quy chế Ban Giám đốc - CEO v1.0` |
| RACI | 00 | 00.5 Cơ cấu tổ chức | `[STANDARD] TL - Ma trận phân quyền RACI - CEO v1.0` |
| Hợp đồng lao động mẫu | 01 | 01.4 Hợp đồng LĐ mẫu | `[STANDARD] HĐ - Hợp đồng lao động mẫu - HR v1.0` |
| Hợp đồng dịch vụ mẫu | 02 | 02.4 Hợp đồng & Chứng từ | `[STANDARD] HĐ - Hợp đồng dịch vụ mẫu - HC v1.0` |
| NDA mẫu | 02 | 02.4 Hợp đồng & Chứng từ | `[STANDARD] HĐ - NDA bảo mật thông tin - HC v1.0` |
| Hợp đồng đại lý mẫu | 04 | 04.3 Tài liệu bán hàng | `[STANDARD] HĐ - Hợp đồng đại lý mẫu - Sales v1.0` |
| Hợp đồng HTKD | 02 | 02.4 Hợp đồng & Chứng từ | `[STANDARD] HĐ - Hợp đồng hợp tác kinh doanh - HC v1.0` |
| Quy tắc đạo đức KD | 03 | 03.3 Nội quy & Quy định | `[STANDARD] QC - Quy tắc đạo đức kinh doanh - CEO v1.0` |
| CS quản lý rủi ro | 00 | 00.2 Chiến lược & KH | `[STANDARD] QC - Chính sách quản lý rủi ro - CEO v1.0` |
| Bảo hiểm DN | 02 | 02.4 Hợp đồng & Chứng từ | `[STANDARD] TL - Danh mục bảo hiểm DN - HC v1.0` |
| Bảo vệ dữ liệu | 03 | 03.3 Nội quy & Quy định | `[STANDARD] QC - Chính sách bảo vệ dữ liệu - IT v1.0` |

### bp-strategy (Chiến Lược & Kế Hoạch)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Hồ sơ năng lực | 04 | 04.3 Tài liệu bán hàng | `[YYYY] TL - Hồ sơ năng lực công ty - CEO vX.0` |
| Tầm nhìn sứ mệnh | 00 | 00.2 Chiến lược & KH | `[STANDARD] TL - Tầm nhìn Sứ mệnh Giá trị - CEO v1.0` |
| Brand Identity | 04 | 04.4 Brand Assets | `[STANDARD] TL - Hướng dẫn nhận diện thương hiệu - MKT v1.0` |
| Kế hoạch kinh doanh | 00 | 00.2 Chiến lược & KH | `[YYYY] KH - Kế hoạch kinh doanh - CEO` |
| OKR | 00 | 00.3 OKR & KPI | `[YYYY] KH - OKR công ty - CEO` |
| SWOT, BMC, Porter | 00 | 00.2 Chiến lược & KH | `[YYYY] TL - Phân tích SWOT - CEO` |
| Roadmap chiến lược | 00 | 00.2 Chiến lược & KH | `[YYYY] KH - Lộ trình chiến lược 3-5 năm - CEO` |

### bp-finance (Tài Chính & Kế Toán)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Chính sách tài chính | 02 | 02.1 Quy chế & CS TC | `[STANDARD] QC - Chính sách tài chính - TC v1.0` |
| Quy chế chi tiêu | 02 | 02.1 Quy chế & CS TC | `[STANDARD] QC - Quy chế chi tiêu nội bộ - TC v1.0` |
| Ngân sách năm | 02 | 02.2 Ngân sách & KH TC | `[YYYY] KH - Ngân sách năm - TC` |
| Cashflow forecast | 02 | 02.2 Ngân sách & KH TC | `[YYYY] BC - Cashflow forecast 12 tháng - TC` |
| SOP thu chi | 03 | 03.1 Quy trình & SOP | `[STANDARD] SOP - Quy trình thu chi - TC v1.0` |
| SOP kế toán tháng | 03 | 03.1 Quy trình & SOP | `[STANDARD] SOP - Quy trình kế toán tháng - TC v1.0` |
| Báo cáo P&L | 02 | 02.3 Báo cáo TC | `[YYYY-MM] BC - Báo cáo Lãi lỗ - TC` |
| Bảng cân đối kế toán | 02 | 02.3 Báo cáo TC | `[YYYY-MM] BC - Bảng cân đối kế toán - TC` |
| Dashboard tài chính | 02 | 02.3 Báo cáo TC | `[YYYY-MM] BC - Dashboard tài chính - TC` |

### bp-people (Nhân Sự & Con Người)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Sơ đồ tổ chức | 00 | 00.5 Cơ cấu tổ chức | `[YYYY] TL - Sơ đồ tổ chức - HR` |
| JD template | 01 | 01.2 Mô tả công việc | `[STANDARD] JD - Template chung - HR v1.0` |
| Nội quy lao động | 01 | 01.1 Quy chế & CS NS | `[STANDARD] QC - Nội quy lao động - HR v1.0` |
| Quy chế lương thưởng 🔒 | 01 | 01.3 Lương thưởng 🔒 | `[YYYY] QC - Quy chế lương thưởng - HR` |
| Sổ tay nhân viên | 01 | 01.5 Onboarding | `[STANDARD] TL - Sổ tay nhân viên - HR v1.0` |
| SOP tuyển dụng | 03 | 03.1 Quy trình & SOP | `[STANDARD] SOP - Quy trình tuyển dụng - HR v1.0` |
| Checklist onboarding | 01 | 01.5 Onboarding | `[STANDARD] SOP - Checklist onboarding 30-60-90 - HR v1.0` |
| Đánh giá hiệu suất | 01 | 01.6 Đánh giá hiệu suất | `[YYYY] QC - Chính sách đánh giá hiệu suất - HR` |

### bp-operations (Hành Chính & Vận Hành)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Sổ tay vận hành | 03 | 03.1 Quy trình & SOP | `[STANDARD] SOP - Sổ tay vận hành - Ops v1.0` |
| SOP cốt lõi | 03 | 03.1 Quy trình & SOP | `[STANDARD] SOP - Quy trình cốt lõi - Ops v1.0` |
| SOP template chuẩn | 03 | 03.2 Biểu mẫu & Templates | `[STANDARD] TL - SOP template chuẩn - Ops v1.0` |
| Nội quy văn phòng | 03 | 03.3 Nội quy & Quy định | `[STANDARD] QC - Nội quy văn phòng - HC v1.0` |
| Quản lý tài sản | 03 | 03.4 Văn phòng & CSVC | `[STANDARD] SOP - Quản lý tài sản - HC v1.0` |
| Quy chế họp hành | 03 | 03.3 Nội quy & Quy định | `[STANDARD] QC - Quy chế họp hành - CEO v1.0` |
| Template biên bản họp | 03 | 03.2 Biểu mẫu & Templates | `[STANDARD] TL - Template biên bản họp - HC v1.0` |
| Template báo cáo tuần | 03 | 03.2 Biểu mẫu & Templates | `[STANDARD] TL - Template báo cáo tuần - HC v1.0` |

### bp-sales (Kinh Doanh & Bán Hàng)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Chiến lược kinh doanh | 04 | 04.1 Chiến lược KD | `[YYYY] KH - Chiến lược kinh doanh - Sales` |
| Quy trình bán hàng | 03 | 03.1 Quy trình & SOP | `[STANDARD] SOP - Quy trình bán hàng - Sales v1.0` |
| Kịch bản bán hàng | 04 | 04.3 Tài liệu bán hàng | `[STANDARD] TL - Kịch bản bán hàng - Sales v1.0` |
| Sổ tay bán hàng | 04 | 04.3 Tài liệu bán hàng | `[STANDARD] TL - Sổ tay bán hàng - Sales v1.0` |
| Pipeline tracker | 04 | 04.6 Pipeline & Sales | `[YYYY-QX] BC - Pipeline tracker - Sales` |
| Báo cáo doanh số | 04 | 04.5 Báo cáo KD | `[YYYY-MM] BC - Báo cáo doanh số - Sales` |
| Chính sách đại lý | 04 | 04.1 Chiến lược KD | `[STANDARD] QC - Chính sách đại lý - Sales v1.0` |

### bp-marketing (Marketing & Thương Hiệu)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Kế hoạch marketing năm | 04 | 04.2 KH & Campaign MKT | `[YYYY] KH - Kế hoạch Marketing - MKT` |
| Chiến lược nội dung | 04 | 04.2 KH & Campaign MKT | `[YYYY] KH - Chiến lược nội dung - MKT` |
| Brand Assets | 04 | 04.4 Brand Assets & TH | `[STANDARD] TL - Hướng dẫn nhận diện thương hiệu - MKT v1.0` |
| Lịch nội dung | 04 | 04.2 KH & Campaign MKT | `[YYYY-QX] KH - Lịch nội dung - MKT` |
| SOP chạy Ads | 03 | 03.1 Quy trình & SOP | `[STANDARD] SOP - Quy trình chạy Ads - MKT v1.0` |

### bp-customer (Khách Hàng & Dịch Vụ)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| CX Standards | 06 | 06.1 Quy trình CSKH | `[STANDARD] QC - Tiêu chuẩn trải nghiệm KH - CSKH v1.0` |
| SOP onboard KH | 06 | 06.1 Quy trình CSKH | `[STANDARD] SOP - Onboarding khách hàng - CSKH v1.0` |
| SOP xử lý khiếu nại | 06 | 06.1 Quy trình CSKH | `[STANDARD] SOP - Xử lý khiếu nại - CSKH v1.0` |
| SOP chăm sóc sau bán | 06 | 06.1 Quy trình CSKH | `[STANDARD] SOP - Chăm sóc sau bán hàng - CSKH v1.0` |
| Tài liệu đào tạo KH | 06 | 06.2 Tài liệu ĐT KH | `[STANDARD] TL - Hướng dẫn sử dụng - CSKH v1.0` |
| Báo cáo CSKH | 06 | 06.4 Báo cáo CSKH | `[YYYY-MM] BC - Báo cáo CSKH - CSKH` |

### bp-product-tech (Sản Phẩm & Công Nghệ)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Danh mục sản phẩm | 05 | 05.1 Roadmap & KH SP | `[YYYY] TL - Danh mục sản phẩm dịch vụ - Tech` |
| Roadmap sản phẩm | 05 | 05.1 Roadmap & KH SP | `[YYYY] KH - Roadmap phát triển sản phẩm - Tech` |
| Tech Stack Map | 05 | 05.4 Hạ tầng & HT | `[STANDARD] TL - Tech Stack Map - IT v1.0` |
| Chính sách CNTT | 05 | 05.3 Quy trình & Dev | `[STANDARD] QC - Chính sách CNTT - IT v1.0` |
| An ninh mạng | 05 | 05.3 Quy trình & Dev | `[STANDARD] QC - Chính sách an ninh mạng - IT v1.0` |
| SOP backup | 05 | 05.3 Quy trình & Dev | `[STANDARD] SOP - Backup dữ liệu - IT v1.0` |

### bp-training (Đào Tạo & Phát Triển)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Chính sách đào tạo | 08 | 08.1 Tài liệu ĐT nội bộ | `[STANDARD] QC - Chính sách đào tạo - HR v1.0` |
| Kế hoạch ĐT năm | 08 | 08.1 Tài liệu ĐT nội bộ | `[YYYY] KH - Kế hoạch đào tạo - HR` |
| ĐT hội nhập | 01 | 01.5 Onboarding | `[STANDARD] SOP - Đào tạo nhân viên mới - HR v1.0` |
| Phát triển lãnh đạo | 08 | 08.1 Tài liệu ĐT nội bộ | `[YYYY] KH - Phát triển lãnh đạo - HR` |

### bp-reporting (Báo Cáo & Đo Lường)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Chính sách báo cáo | 03 | 03.3 Nội quy & Quy định | `[STANDARD] QC - Chính sách báo cáo - CEO v1.0` |
| KPI Dictionary | 00 | 00.3 OKR & KPI | `[YYYY] TL - Từ điển KPI toàn công ty - CEO` |
| Báo cáo quản trị tháng | 09 | 09.2 Báo cáo tháng | `[YYYY-MM] BC - Báo cáo quản trị tháng - CEO` |
| Báo cáo HĐQT | 09 | 09.3 Báo cáo quý & Năm | `[YYYY-QX] BC - Báo cáo HĐQT - CEO` |
| QBR | 09 | 09.3 Báo cáo quý & Năm | `[YYYY-QX] BC - Đánh giá kinh doanh quý - CEO` |
| Báo cáo tuần | 09 | 09.1 Báo cáo tuần | `[YYYY-MM] BC - Báo cáo tuần - [Phòng ban]` |

### bp-growth (Tăng Trưởng & Đầu Tư)

| Tài liệu | Thư mục Drive | Subfolder | Tên file gợi ý |
|-----------|--------------|-----------|----------------|
| Pitch Deck | 04 | 04.3 Tài liệu bán hàng | `[YYYY] TL - Pitch Deck gọi vốn - CEO` |
| Investment Memo | 00 | 00.2 Chiến lược & KH | `[YYYY] TL - Investment Memo - CEO` |
| Cap Table | 00 | 00.1 Hồ sơ pháp lý | `[YYYY] TL - Cap Table - CEO` |
| Franchise Blueprint | 04 | 04.1 Chiến lược KD | `[STANDARD] TL - Mô hình nhượng quyền - CEO v1.0` |

---

## 4. QUY TRÌNH SAU KHI TẠO TÀI LIỆU

1. **Đặt tên file** theo format chuẩn ở Mục 1
2. **Xác định thư mục** đích theo mapping ở Mục 3
3. **Kiểm tra trùng** — nếu đã có file tương tự, cập nhật version (v1.0 → v1.1)
4. **Upload/lưu** file vào đúng subfolder vào đúng thư mục
5. **Cập nhật Hướng dẫn Sử dụng** nếu tạo subfolder mới hoặc thay đổi cấu trúc

## 5. LƯU Ý QUAN TRỌNG

- Tài liệu có ký hiệu 🔒 chỉ những người được phân quyền mới truy cập
- Không xóa file cũ — đổi tên thêm `_old` hoặc di chuyển vào `_ARCHIVE`
- Tài liệu [Liên tục]: tạo file mới theo chu kỳ, không ghi đè file cũ
- `[YYYY]` thay bằng năm thực tế, `[MM]` thay bằng tháng, `[QX]` thay bằng quý
