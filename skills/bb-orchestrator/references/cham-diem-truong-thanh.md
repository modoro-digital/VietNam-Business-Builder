# PROMPT 07: Maturity Scoring (Bảng chấm điểm mức độ trưởng thành)

#### Mô tả
Form chấm điểm mức độ trưởng thành (maturity level) của DN theo 9 khía cạnh. Dùng ở bước Scope Assessment để xác định ưu tiên, và ở Handover Report để so sánh before/after.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có muốn customize 9 khía cạnh hay dùng chuẩn? (Chiến lược, Tài chính, Marketing, Bán hàng, Vận hành, Nhân sự, Công nghệ, Quản trị, Đào tạo)
2. Thang điểm: 0-5 hay 1-10?
3. Mỗi level cần mô tả chi tiết (rubric) không?
4. Có cần benchmark theo ngành không?

#### Template gợi ý
Cấu trúc FRM:
- **Scoring Matrix** — Bảng 9 khía cạnh × 6 levels (0-5), mỗi ô có mô tả cụ thể
- **Level Definitions** — Level 0 (Ad-hoc) → 1 (Initial) → 2 (Defined) → 3 (Managed) → 4 (Optimized) → 5 (World-class)
- **Scoring Guide** — Hướng dẫn cách chấm: evidence-based, ví dụ cụ thể
- **Summary Spider Chart** — Template data cho radar chart
- **Benchmark Reference** — So sánh với trung bình ngành (nếu có)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Maturity Scoring Framework cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- 9 khía cạnh: [liệt kê hoặc dùng chuẩn]
- Thang điểm: [0-5 / 1-10]
- Mục đích: Đánh giá trước khi đóng gói (baseline) và sau khi hoàn thành (progress)

FORMAT:
- Bảng tổng quan: 9 khía cạnh × Score × Evidence × Notes
- Rubric chi tiết: Mỗi khía cạnh × mỗi level = mô tả 2-3 dòng + ví dụ cụ thể
  - VD: Marketing Level 2 = "Có fanpage, đăng bài không đều, chưa có content calendar"
- Spider chart data template: Dạng bảng dữ liệu để vẽ radar chart
- Interpretation guide: Tổng điểm → Recommended action
  - 0-15: "Startup mode — cần xây từ nền móng"
  - 16-30: "Growing — cần hệ thống hóa"
  - 31-45: "Mature — tối ưu & tự động hóa"

TONE: Objective, evidence-based, không judgmental.
LENGTH: 5-8 trang A4.
```
