# PROMPT 05: Quality Checklist (Checklist kiểm tra chất lượng)

#### Mô tả
Form checklist để verify mỗi skill con đã tạo đủ output, đúng format, đúng nội dung. Dùng sau khi hoàn thành mỗi skill và sau khi hoàn thành toàn bộ hệ thống.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tiêu chuẩn chất lượng nào áp dụng? (ISO 9001 / internal standard / custom)
2. Ai sẽ check? (AI auto-check / Coach / cả hai)
3. Mức pass/fail: % hoàn thành tối thiểu để coi là "done"?
4. Có cần scoring hay chỉ cần pass/fail per item?

#### Template gợi ý
Cấu trúc FRM:
- **Per-Skill Checklist** — 12 bảng, mỗi bảng liệt kê files expected + criteria
- **Cross-Skill Checklist** — Consistency check: thuật ngữ, format, cross-references
- **Completeness Score** — Tổng files tạo / tổng files expected × 100%
- **Quality Score** — Dựa trên criteria: Accuracy, Completeness, Consistency, Usability
- **Issues Log** — Bảng ghi nhận issues + severity + action required

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quality Checklist cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- 12 skill con, mỗi skill tạo ra 5-20 files
- Tổng: 200+ files cần kiểm tra
- Tiêu chuẩn: [ISO 9001 / internal / custom]
- Checker: [AI / Coach / cả hai]
- Pass threshold: [% tối thiểu]

FORMAT:
- Per-skill checklist: Bảng | File | Có/Không | Đúng format | Đủ nội dung | Notes
- Cross-skill checklist: Thuật ngữ nhất quán | Cross-ref đúng | Naming convention | Version
- Summary scorecard: Skill × 4 criteria = matrix score
- Issues log template: # | Skill | File | Issue | Severity | Action | Owner | Due
- Final sign-off section: Coach signature + Chủ DN signature + Date

TONE: Nghiêm túc, chuẩn mực, kiểu audit.
LENGTH: 8-10 trang A4 (bao gồm 12 per-skill tables).
```
