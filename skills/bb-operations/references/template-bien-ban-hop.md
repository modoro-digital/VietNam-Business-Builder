### PROMPT 18: Template Biên bản họp (Meeting Minutes Template)

#### Mô tả
Template biên bản họp chuẩn — ghi nhận quyết định, action items, owner, deadline. Khác với BB họp HĐQT (pháp lý) ở bb-governance, đây là template cho họp nội bộ hàng ngày/tuần.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại họp nào cần biên bản? (Daily standup / Weekly / Monthly / Project / All-hands)
2. Ai ghi biên bản? (thư ký cố định / luân phiên / người dự tự ghi)
3. Biên bản gửi cho ai sau họp? (chỉ người dự / cả team / lưu trữ chung)
4. Cần track action items từ biên bản không? (Yes/No — nếu Yes, dùng tool gì?)
5. Có yêu cầu ký duyệt biên bản không?
6. Lưu trữ biên bản ở đâu? (Google Drive / SharePoint / Notion / bản cứng)

#### Template gợi ý
Cấu trúc FRM:
- **Header**: Loại họp | Ngày | Giờ bắt đầu-kết thúc | Địa điểm/Link | Chủ trì | Ghi chép
- **Tham dự**: Bảng Tên | Chức danh | Có mặt ☐ | Vắng (có lý do)
- **Agenda**: Numbered items + thời gian dự kiến mỗi mục
- **Nội dung thảo luận**: Mỗi agenda item → Tóm tắt thảo luận | Quyết định | Action items
- **Bảng Action Items**: # | Action | Owner | Due date | Priority | Status
- **Next meeting**: Ngày | Giờ | Agenda dự kiến
- **Ký duyệt**: Chủ trì ký + Người ghi ký (nếu cần)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Biên bản họp nội bộ (Meeting Minutes).

CONTEXT:
- DN: [Tên] — Loại họp: [Daily / Weekly / Monthly / Project]
- Người ghi: [cố định / luân phiên]
- Lưu trữ: [Google Drive / SharePoint / Notion]
- Track action items: [Có/Không]

FORMAT:
- Header: Loại họp | Ngày | Giờ | Địa điểm/Link | Chủ trì | Ghi chép
- Tham dự: Tên | Chức danh | Có mặt ☐
- Agenda: Numbered items + time box
- Nội dung: Mỗi agenda item → Thảo luận | Quyết định | Action item
- Action items summary: Bảng # | Action | Owner | Due | Priority | Status
- Next meeting: Ngày | Agenda dự kiến
- 1 trang A4 max — concise, action-focused

TONE: Ngắn gọn, action-focused, dễ scan.
LENGTH: 1-2 trang A4.

CROSS-REFERENCE: Liên kết với Quy chế Họp hành (P-OPS-17) về agenda format và L10 meeting.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
