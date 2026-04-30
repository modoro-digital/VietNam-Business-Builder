### PROMPT 09: Knowledge Management System Guide (Hướng dẫn Hệ thống Quản lý Tri thức)

#### Mô tả
Hướng dẫn xây dựng và vận hành hệ thống quản lý tri thức (KMS) — nơi lưu trữ, tổ chức, chia sẻ, và cập nhật toàn bộ kiến thức của tổ chức. Bao gồm taxonomy, contribution guidelines, quality standards, và governance. Đảm bảo kiến thức không mất khi nhân viên nghỉ, và mọi người dễ dàng tìm thấy thông tin cần thiết.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện tại kiến thức lưu ở đâu? (Google Drive / Notion / SharePoint / wiki / đầu người)
2. Có knowledge base/wiki hiện tại không? Platform gì?
3. Loại kiến thức nào quan trọng nhất? (quy trình / sản phẩm / khách hàng / kỹ thuật / best practices)
4. Ai contribute nội dung? (subject matter experts / tất cả NV / team chuyên trách)
5. Vấn đề lớn nhất: kiến thức mất khi NV nghỉ / không tìm thấy / outdated / không ai dùng?
6. Có AI/chatbot hỗ trợ tìm kiếm kiến thức không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Vision & Objectives: Tại sao KMS, mục tiêu, success criteria
- **Phần 2** — Knowledge Taxonomy: Phân loại kiến thức — Explicit vs Tacit, Categories, Tags
- **Phần 3** — Platform & Architecture: Tool selection, structure, search, access control
- **Phần 4** — Content Standards: Template articles, quality criteria, review process
- **Phần 5** — Contribution Process: Ai viết, quy trình submit → review → publish
- **Phần 6** — Governance: Owner, maintenance, update cycle, retirement
- **Phần 7** — Adoption Strategy: Training, gamification, KPIs
- **Phần 8** — Knowledge Capture: Exit interviews, after-action reviews, lessons learned
- **Phụ lục**: Article template, Taxonomy tree, Platform comparison

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Knowledge Management System Guide (Hướng dẫn Hệ thống Quản lý Tri thức).

CONTEXT:
- DN: [Tên] — Nhân sự: [số]
- Kiến thức hiện tại: [Google Drive / Notion / wiki / đầu người]
- Platform KMS: [đã chọn / cần tư vấn]
- Loại kiến thức ưu tiên: [quy trình / sản phẩm / kỹ thuật / best practices]
- Contributors: [SMEs / tất cả NV / team chuyên trách]
- Vấn đề chính: [mất khi NV nghỉ / không tìm thấy / outdated]

FORMAT:
- KMS vision: 1 đoạn — "Mọi nhân viên tìm thấy thông tin đúng trong X phút"
- Knowledge taxonomy:
  - Level 1: Categories (Process, Product, Customer, Technical, HR, Leadership)
  - Level 2: Sub-categories per L1
  - Level 3: Article types (How-to, FAQ, Policy, Template, Case study, Lesson learned)
  - Tagging convention: [Category]-[Sub]-[Type]-[Audience]
- Platform architecture: Mermaid — Structure of spaces/databases/folders
- Content standards:
  - Article template: Title | Summary (2 lines) | Body | Author | Date | Review date | Tags | Related articles
  - Quality criteria: Accurate | Current | Actionable | Searchable | Reviewed
  - Writing guidelines: Plain language, max 1000 words, include visuals, link to related
- Contribution workflow: Mermaid — Draft → Peer review → SME approve → Publish → Schedule review
- Governance model:
  - Roles: KMS Owner | Content leads per dept | Contributors | Reviewers
  - Review cycle: Bảng Content type | Review frequency | Owner | Archive after
  - Metrics: Bảng Usage | Contribution | Quality | Search effectiveness
- Knowledge capture processes:
  - Exit interview checklist: Critical knowledge areas | Documentation status | Handover plan
  - After-Action Review: What happened | What was expected | Why different | Lessons | Actions
  - Communities of Practice: Topic | Members | Meeting cadence | Output
- Adoption plan:
  - Launch: Communicate | Train | Seed content | Quick wins
  - Sustain: Gamification | Recognition | KPIs in reviews | Leadership modeling
  - KPIs: Active users % | Articles created/month | Search success rate | Time-to-find-info | Content freshness %

TONE: Practical, adoption-focused, balance structure with usability.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
