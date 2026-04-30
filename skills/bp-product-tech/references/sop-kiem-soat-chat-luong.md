### PROMPT 05: SOP Quy trình Kiểm soát Chất lượng (Quality Control SOP)

#### Mô tả
Quy trình kiểm soát chất lượng sản phẩm/dịch vụ — từ tiêu chuẩn chất lượng, checklist kiểm tra, quy trình xử lý lỗi/nonconformance, đến tracking metrics. Áp dụng cho cả SP vật lý lẫn dịch vụ/phần mềm.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại sản phẩm cần QC? (vật lý / phần mềm / dịch vụ)
2. Có tiêu chuẩn chất lượng hiện tại không? (ISO, nội bộ, ngành)
3. Quy trình kiểm tra hiện tại? (incoming / in-process / final / post-delivery)
4. Tỷ lệ lỗi/return hiện tại? Mục tiêu?
5. Ai chịu trách nhiệm QC? (team riêng / mỗi người tự kiểm)
6. Có tracking tool không? (spreadsheet / phần mềm / manual)

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Tiêu chuẩn chất lượng**: Bảng tiêu chí per SP/DV — criteria, spec, tolerance
- **Quy trình QC Incoming**: Kiểm tra nguyên liệu/input đầu vào
- **Quy trình QC In-Process**: Kiểm tra trong quá trình sản xuất/cung cấp DV
- **Quy trình QC Final**: Kiểm tra sản phẩm hoàn thiện trước giao hàng
- **Xử lý Nonconformance**: Flowchart phát hiện → ghi nhận → phân tích → khắc phục → CAPA
- **Quality Metrics & Reporting**: KPIs theo dõi chất lượng
- **Phụ lục**: QC Checklist template, Nonconformance Report form, CAPA form

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Kiểm soát Chất lượng (Quality Control SOP).

CONTEXT:
- DN: [Tên] — Loại SP: [vật lý / phần mềm / dịch vụ]
- Tiêu chuẩn: [ISO / nội bộ / ngành]
- Quy trình hiện tại: [incoming / in-process / final]
- Tỷ lệ lỗi: [current %] — Target: [target %]
- QC team: [team riêng / self-check / hybrid]

FORMAT:
- Quality standards: Bảng SP | Criteria | Spec | Tolerance | Method
- QC flowchart: Mermaid — Incoming → In-Process → Final → Release
- Inspection checklist: Mỗi stage 1 bảng ☐ — Item | Criteria | Pass/Fail | Notes
- Nonconformance flow: Mermaid — Detect → Record → Analyze → Correct → CAPA → Close
- CAPA template: Issue | Root Cause (5 Whys / Fishbone) | Corrective Action | Preventive Action | Owner | Due
- Quality KPIs: Metric | Formula | Target | Frequency | Owner
  - Defect Rate, First Pass Yield, Customer Return Rate, CAPA Closure Rate
- Monthly QC report template: Summary + trend + top issues + actions

TONE: SOP chuẩn ISO, chi tiết, kiểm soát chặt.
LENGTH: 6-10 trang A4.

CROSS-REFERENCE: Đây là SOP thực thi kiểm soát chất lượng. Chính sách chất lượng tổng thể (cam kết, mục tiêu ISO) xem bp-operations/Chính sách Chất lượng.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
