# PROMPT 14: Strategic Roadmap (Lộ trình chiến lược)

#### Mô tả
Lộ trình phát triển DN theo timeline 1-3-5 năm. Kết hợp milestones từ tất cả lĩnh vực: sản phẩm, thị trường, nhân sự, công nghệ, tài chính. Dạng Gantt-like, dễ truyền thông cho toàn team và investors.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Horizon: 1 năm / 3 năm / 5 năm? (hoặc chia giai đoạn)
2. Key milestones đã xác định? (VD: ra sản phẩm mới, mở thị trường mới, gọi vốn, IPO...)
3. Dependencies giữa các milestone?
4. Phân chia theo giai đoạn: Foundation → Growth → Scale → Exit?
5. Muốn roadmap theo swimlane (1 lane per department) hay timeline đơn?
6. Có trigger milestones (milestone phụ thuộc điều kiện thay vì thời gian) không?

#### Template gợi ý
Cấu trúc MAN:
- **Executive View** — 1 trang, timeline với 5-7 key milestones, high-level
- **Detailed Roadmap** — Swimlane view: Product | Market | People | Finance | Tech — mỗi lane có milestones
- **Phase Descriptions** — Mỗi giai đoạn: Objectives + Key Activities + Exit Criteria + Budget Estimate
- **Dependencies Map** — Milestone X phải xong trước khi bắt đầu Y
- **Risk & Contingency** — Per phase: What could delay + Contingency plan
- **Quarterly Breakdown** — Chi tiết Q1-Q2-Q3-Q4 cho năm đầu tiên
- **Review Cadence** — Tần suất review roadmap: Monthly (tactical) + Quarterly (strategic) + Annual (vision)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Strategic Roadmap.

CONTEXT:
- DN: [Tên] — Stage: [startup/growth/mature]
- Horizon: [1/3/5 năm]
- Key Milestones: [liệt kê với target date]
- Dependencies: [milestone A → B → C]
- Giai đoạn: [VD: Foundation Q1-Q2 → Growth Q3-Q4 → Scale Year 2]
- Format: [Swimlane / Timeline / Phase-based]

FORMAT:
- Executive 1-pager: Timeline + 5-7 key milestones
- Swimlane roadmap: 5 lanes (Product, Market, People, Finance, Tech) × time
- Phase cards: Phase name | Duration | Objectives | Key Activities | Exit Criteria | Budget
- Milestone table: # | Milestone | Lane | Start | End | Dependencies | Owner | Status
- Dependencies: Mermaid Gantt hoặc DAG diagram
- Year 1 quarterly detail: Q1-Q4 breakdown với monthly actions
- Review template: Quarterly roadmap review form

TONE: Visionary yet practical — ambitious milestones, realistic timelines.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
