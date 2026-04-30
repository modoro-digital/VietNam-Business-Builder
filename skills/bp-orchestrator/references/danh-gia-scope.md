# PROMPT 02: Scope Assessment (Quy trình đánh giá scope)

#### Mô tả
SOP hướng dẫn cách phân tích kết quả Intake Questionnaire để xác định: DN đang ở maturity level nào, nên ưu tiên tầng nào, skill con nào cần chạy trước, skill nào có thể skip hoặc customize.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Anh đã có maturity model riêng chưa, hay dùng model chuẩn?
2. Tiêu chí nào quyết định thứ tự ưu tiên? (urgency / impact / effort / cost)
3. Có trường hợp nào cần skip skill con hoàn toàn không? (VD: DN 1 người không cần HR)
4. Ai sẽ là người đánh giá scope? (AI tự động / Coach review / cả hai)

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi** — Khi nào dùng, ai dùng
- **Input** — Intake Questionnaire đã điền
- **Bước 1: Chấm điểm maturity** — 9 khía cạnh × thang 0-5, tham chiếu `maturity-scoring.md`
- **Bước 2: Xác định tầng ưu tiên** — Decision tree dựa trên score + mục tiêu DN
- **Bước 3: Customize skill list** — Bảng 12 skill × (Run/Skip/Customize) + lý do
- **Bước 4: Ước lượng timeline** — Công thức tính thời gian dựa trên scope
- **Output** — Scope Document (summary 1 trang) + Execution Plan

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP "Scope Assessment" cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- Đây là bước 2 trong flow Orchestrator: sau khi thu thập thông tin (Intake), trước khi tạo thư mục và gọi skill con
- Maturity model: [model riêng / chuẩn] — 9 khía cạnh: Chiến lược, Tài chính, Marketing, Bán hàng, Vận hành, Nhân sự, Công nghệ, Quản trị, Đào tạo
- Thang điểm: 0 (chưa có gì) → 5 (world-class, đã tự động hóa)
- Tiêu chí ưu tiên: [urgency/impact/effort/cost]
- 12 skill con: governance, strategy, finance, people, operations, sales, marketing, customer, product-tech, training, reporting, growth

FORMAT:
- SOP chuẩn: Mục đích → Phạm vi → Thuật ngữ → Quy trình từng bước → Flowchart (mermaid) → Output template
- Có decision tree rõ ràng: IF score < X THEN ưu tiên Y
- Bảng mapping: Maturity Score → Recommended Action per skill
- Song ngữ Việt-Anh cho thuật ngữ

TONE: Chuẩn mực, rõ ràng, dễ follow cho cả AI lẫn Coach.
LENGTH: 3-5 trang A4.
```
