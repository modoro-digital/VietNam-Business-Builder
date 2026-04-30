### PROMPT 02: Product Roadmap (Lộ trình Phát triển Sản phẩm)

#### Mô tả
Lộ trình phát triển sản phẩm theo quý/năm — liệt kê các milestones, tính năng mới, cải tiến, dependencies, và resource cần thiết. Roadmap là công cụ alignment giữa Product, Engineering, Sales, và Leadership.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Horizon roadmap? (3 tháng / 6 tháng / 12 tháng / 3 năm)
2. Bao nhiêu sản phẩm/product line cần roadmap?
3. Methodology phát triển? (Agile/Scrum / Waterfall / Hybrid)
4. Ai là stakeholders chính đọc roadmap này?
5. Có OKR/KPI sản phẩm hiện tại không? Liên kết thế nào?
6. Các constraints lớn? (budget, headcount, tech debt, market timing)

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Vision & Strategy: Tầm nhìn sản phẩm, strategic themes
- **Phần 2** — Now / Next / Later: Phân loại initiatives theo timeline
- **Phần 3** — Quarterly Roadmap: Q1-Q4 × Product lines × Milestones
- **Phần 4** — Feature Backlog: Prioritized list — MoSCoW hoặc RICE scoring
- **Phần 5** — Dependencies & Risks: Bảng dependency map, risk register
- **Phần 6** — Resource Allocation: Team × Quarter × % allocation
- **Phần 7** — Review & Update Cadence: Tần suất review, quy trình thay đổi roadmap
- **Phụ lục**: Initiative scoring template, Roadmap communication template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Product Roadmap (Lộ trình Phát triển Sản phẩm).

CONTEXT:
- DN: [Tên] — Số product lines: [số]
- Horizon: [3/6/12 tháng / 3 năm]
- Methodology: [Agile / Waterfall / Hybrid]
- Stakeholders: [Product, Engineering, Sales, Leadership]
- Constraints: [budget / headcount / tech debt / market]

FORMAT:
- Vision statement: 1 đoạn ngắn — why & where
- Now/Next/Later: 3 swim lanes × initiatives
- Quarterly view: Gantt-style table — Q×Product×Milestone×Owner×Status
- Backlog scoring: Initiative | Impact (1-5) | Effort (1-5) | RICE Score | Priority
- Dependency map: Mermaid diagram — Initiative A → B → C
- Resource table: Team | Q1 | Q2 | Q3 | Q4 — % allocation
- Risk register: Risk | Probability | Impact | Mitigation
- Review cadence: Monthly review + Quarterly reprioritization

TONE: Chiến lược, visual, alignment-focused.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
