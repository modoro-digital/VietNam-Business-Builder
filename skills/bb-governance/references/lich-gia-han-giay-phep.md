# PROMPT 19: Lịch gia hạn giấy phép (License Renewal Calendar)

#### Mô tả
Calendar view tổng hợp tất cả giấy phép, chứng chỉ, hợp đồng bảo hiểm, đăng ký cần gia hạn định kỳ. Alert system trước 90/60/30/15 ngày.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tổng hợp từ file nào? (Danh sách giấy phép con + Danh mục bảo hiểm + ĐKKD)
2. Ai nhận alert? (Admin / Pháp chế / Giám đốc)
3. Alert qua kênh nào? (Email / Calendar / Slack / Zalo)
4. Có budget cho từng lần gia hạn không?

#### Template gợi ý
Cấu trúc FRM:
- **Calendar 12 tháng**: Bảng tháng × items cần gia hạn
- **Registry chi tiết**: # | Item | Loại | Ngày hết hạn | Lead time gia hạn | Chi phí | Owner | Status
- **Alert rules**: 90 ngày (thông báo), 60 ngày (bắt đầu hồ sơ), 30 ngày (submit), 15 ngày (escalate)
- **Quy trình gia hạn tóm tắt**: Per loại giấy phép
- **Dashboard**: Tổng items | Sắp hết hạn | Quá hạn | OK

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Lịch gia hạn giấy phép (License Renewal Calendar).

CONTEXT:
- Nguồn data: [Giấy phép con + Bảo hiểm + ĐKKD + Hợp đồng]
- Alert recipient: [chức danh]
- Alert channel: [Email / Calendar / Slack / Zalo]
- Budget tracking: [Có/Không]

FORMAT:
- Calendar view: 12 tháng, mỗi ô chứa items hết hạn trong tháng đó
- Registry table: Đầy đủ cột, sort theo ngày hết hạn ascending
- Color coding: 🟢 OK (>90 ngày) | 🟡 Attention (30-90 ngày) | 🟠 Urgent (15-30 ngày) | 🔴 Critical (<15 ngày) | ⚫ Expired
- Alert workflow: Flowchart 4 mốc (90-60-30-15)
- Dashboard summary: KPI cards
- Auto-fill: Từ data các file liên quan trong 01-bb-governance

TONE: Operational, action-oriented.
LENGTH: 3-5 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
