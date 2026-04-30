### PROMPT 13: SOP Review & Cập nhật SOP (SOP Review & Update Process)

#### Mô tả
Meta-SOP — quy trình quản lý, review, và cập nhật toàn bộ SOP trong DN. Đảm bảo SOP luôn up-to-date, phản ánh đúng thực tế vận hành, có version control, và được review định kỳ.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện tại có bao nhiêu SOP? Lưu trữ ở đâu? (Notion / Drive / SharePoint / bản cứng)
2. Tần suất review SOP? (6 tháng / 1 năm / khi có thay đổi)
3. Ai có quyền sửa SOP? Quy trình duyệt thay đổi?
4. Có hệ thống version control không? (v1.0, v1.1...)
5. Có audit trail cho các thay đổi không?
6. Khi nào SOP được retire/archive?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi** — Áp dụng cho MỌI SOP, POL, MAN, FRM trong DN
- **SOP Inventory**: Bảng danh sách tất cả SOP — mã, tên, owner, version, last review, next review
- **Review Schedule**: Calendar review — SOP nào review khi nào
- **Trigger-based Review**: Sự kiện nào trigger review ngoài lịch? (sự cố, audit finding, law change)
- **Quy trình Review & Update**: Flowchart — Trigger → Draft changes → Review → Approve → Publish → Train → Archive old
- **Version Control**: Quy tắc đánh version, changelog format
- **Distribution & Training**: Cách thông báo SOP mới/cập nhật, đào tạo affected staff
- **Retirement**: Khi nào retire, quy trình archive, retention period

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Review & Cập nhật SOP.

CONTEXT:
- DN: [Tên] — Số SOP hiện tại: [số] — Lưu trữ: [platform]
- Review frequency: [6 tháng / 1 năm]
- Ai sửa SOP: [SOP owner / centralized team]
- Version control: [Có/Không]

FORMAT:
- SOP inventory template: Mã SOP | Tên | Category | Owner | Version | Effective date | Last review | Next review | Status
- Review calendar: 12 tháng × SOP list → Highlight review months
- Review trigger list: Event | Type (Scheduled/Triggered) | Action | Owner
- Update flowchart: Mermaid — Trigger → Draft → Peer Review → Approve → Publish → Notify → Train → Archive
- Version control rules: Major (v1→v2) vs Minor (v1.0→v1.1) | Changelog format
- Change log template: Version | Date | Section | Change description | Changed by | Approved by
- Distribution checklist: ☐ Update master | ☐ Notify users | ☐ Remove old version | ☐ Train if needed | ☐ Update training materials
- Retirement criteria: Conditions | Archive location | Retention period | Approver

TONE: Meta-SOP — structured, governance-focused.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
