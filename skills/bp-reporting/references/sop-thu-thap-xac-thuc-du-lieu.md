### PROMPT 06: Data Collection & Validation SOP (Quy trình Thu thập & Xác thực Dữ liệu)

#### Mô tả
Quy trình chuẩn hóa việc thu thập, kiểm tra, và xác thực dữ liệu trước khi đưa vào báo cáo. Đảm bảo "garbage in, garbage out" không xảy ra. Bao gồm data ownership, input standards, validation rules, reconciliation, và error handling.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Nguồn dữ liệu chính? (ERP / CRM / spreadsheet / manual input / external)
2. Ai nhập dữ liệu? (nhân viên / manager / kế toán / automated)
3. Vấn đề dữ liệu thường gặp? (trùng / thiếu / sai format / nhập trễ / không khớp)
4. Có data dictionary/data standards không?
5. Quy trình reconciliation hiện tại? (cross-check giữa các hệ thống)
6. Tần suất data quality review?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Data Ownership**: RACI cho từng loại dữ liệu
- **Collection Standards**: Format, đơn vị, naming convention, input deadline
- **Validation Rules**: Automated checks, manual review, cross-system reconciliation
- **Error Handling**: Phát hiện → Ghi nhận → Sửa → Verify → Root cause → Prevent
- **Data Quality Metrics**: Accuracy, completeness, timeliness, consistency — KPIs
- **Review Process**: Tần suất, checklist, sign-off
- **Phụ lục**: Data dictionary template, Validation checklist, Error log template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Data Collection & Validation SOP.

CONTEXT:
- DN: [Tên] — Nguồn dữ liệu: [ERP / CRM / spreadsheet / manual]
- Người nhập: [NV / manager / kế toán / automated]
- Vấn đề chính: [trùng / thiếu / sai format / trễ / không khớp]
- Data dictionary: [Có/Không]
- Reconciliation: [cross-check hiện tại]

FORMAT:
- Data ownership matrix: Bảng Data domain | Source system | Data owner | Data steward | Input by | Validate by
- Collection standards per data type:
  - Format: Date (DD/MM/YYYY) | Currency (VNĐ, không dấu chấm) | Text (Title Case) | Phone (0xxx)
  - Naming convention: Entity naming rules + examples
  - Input deadline: Data type | Source | Deadline | Frequency | Responsible
- Validation rules engine:
  - Automated: Rule | Check type (Range/Format/Uniqueness/Referential) | System | Action if fail
  - Manual: Checklist ☐ per report — 10-15 items: Completeness | Accuracy | Consistency | Timeliness
  - Reconciliation: System A vs System B | Metric | Tolerance | Frequency | Investigator
- Error handling flowchart: Mermaid — Detect → Log → Classify (Critical/Major/Minor) → Fix → Verify → Root cause → Preventive action
- Error log template: Date | Data domain | Error type | Description | Impact | Root cause | Fix | Fixed by | Verified by
- Data quality scorecard: Dimension | Definition | Measurement | Target | Current | Status
  - Accuracy: % records without errors
  - Completeness: % required fields filled
  - Timeliness: % data submitted by deadline
  - Consistency: % cross-system matches
  - Uniqueness: % duplicate-free records
- Review calendar: Monthly data quality review | Quarterly deep audit | Annual data governance review
- RACI per activity: Collect | Validate | Reconcile | Report | Fix errors | Set standards

TONE: SOP chi tiết, data governance–oriented.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
