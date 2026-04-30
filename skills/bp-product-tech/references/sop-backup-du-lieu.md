### PROMPT 09: SOP Backup Dữ liệu (Data Backup SOP)

#### Mô tả
Quy trình backup và phục hồi dữ liệu — lịch backup, phương pháp (full/incremental/differential), storage location, kiểm tra phục hồi định kỳ, và xác định RPO/RTO cho từng hệ thống.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hệ thống/dữ liệu nào cần backup? (database, files, email, code, configs)
2. Backup hiện tại: tự động hay thủ công? Tool gì?
3. Storage: local / cloud / cả hai? Capacity?
4. Đã bao giờ cần restore chưa? Kết quả?
5. RPO mong muốn? (mất tối đa bao nhiêu dữ liệu: 1 giờ / 1 ngày)
6. RTO mong muốn? (phục hồi trong bao lâu: 1 giờ / 4 giờ / 1 ngày)

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Phân loại dữ liệu**: Criticality levels — Critical / Important / Normal
- **Backup Schedule**: Bảng hệ thống × tần suất × phương pháp × retention
- **Quy trình Backup**: Step-by-step cho mỗi loại backup
- **Storage & Rotation**: Primary / Secondary / Offsite — 3-2-1 rule
- **Quy trình Restore**: Step-by-step phục hồi + timeline
- **Disaster Recovery Test**: Tần suất test, checklist, báo cáo kết quả
- **RPO/RTO Matrix**: Hệ thống × RPO × RTO × Current capability × Gap
- **Phụ lục**: Backup log template, Restore test report template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Backup Dữ liệu.

CONTEXT:
- DN: [Tên] — Hệ thống cần backup: [liệt kê]
- Tool backup: [tên]
- Storage: [local / cloud / hybrid] — Capacity: [GB/TB]
- RPO target: [thời gian] — RTO target: [thời gian]
- Restore history: [Có/Không]

FORMAT:
- Data classification: Bảng System | Data type | Criticality | RPO | RTO
- Backup schedule: System | Method (Full/Incr/Diff) | Frequency | Time | Retention | Storage
- 3-2-1 rule diagram: 3 copies × 2 media × 1 offsite
- Backup procedure: Step-by-step per system — numbered steps
- Restore procedure: Step-by-step — numbered steps + estimated time
- DR test checklist: 10-15 mục ☐ + Scenario | Expected | Actual | Pass/Fail
- RPO/RTO dashboard: System | Target RPO | Actual RPO | Target RTO | Actual RTO | Status 🟢🟡🔴
- Backup log: Date | System | Type | Size | Duration | Status | Operator

TONE: SOP technical, rõ ràng, testable.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
