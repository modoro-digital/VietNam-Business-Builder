# PROMPT 17: Danh mục bảo hiểm DN (Corporate Insurance Portfolio)

#### Mô tả
Danh mục tổng hợp tất cả bảo hiểm DN đang có hoặc cần mua. Bao gồm: tài sản, trách nhiệm, nhân sự, gián đoạn kinh doanh, cyber, D&O. Giúp quản lý portfolio bảo hiểm tập trung.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện đang có bảo hiểm gì? (liệt kê)
2. Ngành nghề & tài sản chính? (xác định rủi ro cần bảo hiểm)
3. Quy mô nhân sự? (ảnh hưởng BH nhân sự)
4. Budget bảo hiểm hàng năm?
5. Có hoạt động quốc tế không? (cần BH quốc tế)

#### Template gợi ý
Cấu trúc FRM:
- **Bảng portfolio**: # | Loại BH | Nhà BH | Số HĐ | Coverage | Premium/năm | Ngày bắt đầu | Ngày hết hạn | Status
- **Phân nhóm**: BH bắt buộc / BH khuyến nghị / BH tùy chọn
- **Gap Analysis**: Bảng rủi ro chưa được bảo hiểm
- **Renewal Calendar**: Timeline 12 tháng
- **Cost Summary**: Tổng premium, so sánh YoY
- **Claim History**: Bảng lịch sử bồi thường

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Danh mục bảo hiểm DN (Corporate Insurance Portfolio).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số] — Tài sản chính: [liệt kê]
- BH hiện có: [liệt kê]
- Budget: [số/năm]
- Quốc tế: [Có/Không]

FORMAT:
- Portfolio table: Đầy đủ cột như template
- BH bắt buộc theo luật VN: BHXH, BHYT, BH thất nghiệp, BH cháy nổ (nếu áp dụng)
- BH khuyến nghị: Tùy ngành — bảng mapping Ngành → Loại BH khuyến nghị
- Gap Analysis: Risk | Current Coverage | Gap | Recommended | Est. Premium
- Renewal calendar: Gantt-style hoặc list theo tháng
- Total Cost of Insurance: Pie chart data

TONE: Quản lý, thực tế.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
