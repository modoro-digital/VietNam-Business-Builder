### PROMPT 01: Reporting Policy & Standards (Chính sách & Chuẩn mực Báo cáo)

#### Mô tả
Chính sách quy định toàn bộ hệ thống báo cáo trong DN — loại báo cáo, tần suất, format chuẩn, deadline, trách nhiệm của từng bộ phận, quy trình duyệt, và chuẩn mực chất lượng dữ liệu. Là "luật chơi" cho reporting — đảm bảo thông tin đúng, đủ, đúng hạn, và đúng người.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN hiện có bao nhiêu loại báo cáo? (daily / weekly / monthly / quarterly / annual)
2. Ai nhận báo cáo? (CEO / BGĐ / HĐQT / Cổ đông / Cơ quan quản lý)
3. Format hiện tại: tự do hay có template? Tool gì? (Excel / Google Sheets / BI tool / ERP)
4. Vấn đề chính: số liệu không khớp / báo cáo trễ / format không nhất quán / thừa báo cáo?
5. Có audit requirements không? (kiểm toán nội bộ / ngoài / cơ quan nhà nước)
6. Chính sách bảo mật dữ liệu báo cáo?

#### Template gợi ý
Cấu trúc POL:
- **Điều 1-3** — Mục đích, Phạm vi, Thuật ngữ
- **Điều 4** — Phân loại báo cáo: Operational / Financial / Strategic / Compliance / Ad-hoc
- **Điều 5** — Reporting Calendar: Bảng loại × tần suất × deadline × owner × audience
- **Điều 6** — Format & Template Standards: Chuẩn hóa header, structure, visualization
- **Điều 7** — Data Quality Standards: Accuracy, completeness, timeliness, consistency
- **Điều 8** — Review & Approval Process: Ai duyệt, timeline duyệt
- **Điều 9** — Distribution & Confidentiality: Ai nhận, kênh gửi, phân loại mật
- **Điều 10** — Archive & Retention: Lưu trữ, thời hạn, truy xuất
- **Điều 11** — Exception Reporting: Báo cáo bất thường, triggers, escalation
- **Điều 12** — Xử lý vi phạm
- **Phụ lục**: Reporting calendar master, Report cover page template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Reporting Policy & Standards (Chính sách & Chuẩn mực Báo cáo).

CONTEXT:
- DN: [Tên] — Nhân sự: [số] — Số phòng ban: [số]
- Loại báo cáo: [daily / weekly / monthly / quarterly / annual]
- Audience: [CEO / BGĐ / HĐQT / Cổ đông / Cơ quan]
- Tool: [Excel / Google Sheets / BI tool / ERP]
- Vấn đề chính: [số liệu sai / trễ / format lộn xộn / thừa]
- Audit: [nội bộ / ngoài / cơ quan nhà nước]

FORMAT:
- Đánh số điều liên tục
- Report classification: Bảng Type | Description | Frequency | Deadline | Owner | Audience | Confidentiality
- Reporting calendar: Master calendar 12 tháng — Type | Jan | Feb | ... | Dec — highlight deadlines
- Template standards:
  - Header: Logo | Report name | Period | Version | Author | Date | Classification
  - Structure: Executive summary → KPIs → Detail → Variance analysis → Action items
  - Visualization rules: Chart types per data type, color coding, annotation standards
- Data quality checklist: ☐ Accuracy | ☐ Completeness | ☐ Timeliness | ☐ Consistency | ☐ Source verified
- Approval workflow: Mermaid — Data owner → Reviewer → Approver → Distribution
- Exception reporting: Trigger | Threshold | Escalation path | Response time
- Archive matrix: Report type | Retention period | Storage | Access | Destruction method

TONE: Governance-level, rõ ràng, enforce compliance.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
