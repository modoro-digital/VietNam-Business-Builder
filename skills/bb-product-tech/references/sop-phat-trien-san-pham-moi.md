### PROMPT 03: SOP Quy trình Phát triển Sản phẩm Mới (New Product Development SOP)

#### Mô tả
Quy trình chuẩn hóa từ khi có ý tưởng sản phẩm mới đến khi launch ra thị trường. Bao gồm các gate/checkpoint, tiêu chí go/no-go, vai trò từng bộ phận, và timeline chuẩn.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại sản phẩm phát triển? (phần mềm / vật lý / dịch vụ / hybrid)
2. Cycle time trung bình từ idea đến launch? (tuần / tháng)
3. Ai có quyền đề xuất SP mới? (chỉ PM / tất cả nhân viên / leadership only)
4. Quy trình duyệt hiện tại? (có stage-gate hay freestyle?)
5. Có MVP/Beta testing trước khi full launch không?
6. Budget phát triển SP mới thường là bao nhiêu?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Stage 1 — Ideation**: Thu thập ý tưởng, screening, feasibility check
- **Gate 1 — Concept Approval**: Tiêu chí go/no-go, ai duyệt
- **Stage 2 — Research & Planning**: Market research, technical feasibility, business case
- **Gate 2 — Business Case Approval**: ROI, resource commitment
- **Stage 3 — Development**: Build/produce, prototype, internal testing
- **Gate 3 — Product Review**: QC, UAT, beta feedback
- **Stage 4 — Launch Prep**: GTM plan, training, pricing, collateral
- **Gate 4 — Launch Decision**: Final go/no-go
- **Stage 5 — Launch & Review**: Go-to-market, 30/60/90 review
- **Phụ lục**: Stage-gate checklist, RACI per stage

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quy trình Phát triển Sản phẩm Mới.

CONTEXT:
- DN: [Tên] — Loại SP: [phần mềm / vật lý / dịch vụ]
- Cycle time mục tiêu: [X tuần/tháng]
- Ai đề xuất: [PM / tất cả NV / leadership]
- Budget SP mới: [range]
- MVP/Beta: [Có/Không]

FORMAT:
- Stage-Gate flowchart: Mermaid — 5 stages + 4 gates
- Mỗi stage: Input | Activities | Output | Owner | Timeline
- Mỗi gate: Criteria checklist ☐ | Decision maker | Go/Kill/Pivot
- RACI matrix: Stage × Role (PM, Dev, QC, Marketing, Sales, Finance, CEO)
- Timeline template: Gantt cho 1 SP mẫu
- Budget template: Stage | Cost items | Estimate | Actual | Variance
- KPI post-launch: Metric | Target | Actual | Review date

TONE: SOP chuẩn — rõ ràng, step-by-step, có gate kiểm soát.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
