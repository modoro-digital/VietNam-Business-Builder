# P-PPL-20: Chính sách đánh giá hiệu suất (Performance Evaluation Policy)

#### Mô tả
Chính sách đánh giá hiệu suất NV — quy định tần suất, phương pháp, thang đánh giá, liên kết với lương/thăng tiến, và quy trình appeal. Là nền tảng cho KPI, 360, và toàn bộ hệ thống performance management.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tần suất đánh giá? (Quý / 6 tháng / Năm)
2. Phương pháp: MBO / OKR / KPI / BSC / Mixed?
3. Thang đánh giá: 1-5 (Outstanding → Poor) hay A-E?
4. Liên kết lương: đánh giá ảnh hưởng tăng lương bao nhiêu %?
5. Liên kết thăng tiến: cần mấy kỳ đánh giá tốt để lên level?
6. Có appeal/khiếu nại kết quả đánh giá không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích: Cải thiện hiệu suất, phát triển NV, cơ sở cho lương/thăng tiến
- **Phần 2** — Phạm vi & Đối tượng: Áp dụng cho ai, từ khi nào (sau thử việc)
- **Phần 3** — Phương pháp: MBO/OKR/KPI/BSC — khi nào dùng cái nào
- **Phần 4** — Chu kỳ & Timeline: Calendar đánh giá, deadline mỗi bước
- **Phần 5** — Thang đánh giá: Rating scale + mô tả chi tiết mỗi mức
- **Phần 6** — Quy trình: NV tự đánh giá → Manager đánh giá → Calibration → Feedback → Sign-off
- **Phần 7** — Liên kết C&B: Rating → % tăng lương, thưởng, thăng tiến
- **Phần 8** — Appeal mechanism: Quy trình khiếu nại kết quả
- **Phụ lục**: Calendar đánh giá, Rating distribution guideline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách đánh giá hiệu suất (Performance Evaluation Policy).

CONTEXT:
- DN: [Tên] — Nhân sự: [số]
- Tần suất: [Quý / 6 tháng / Năm]
- Phương pháp: [MBO / OKR / KPI / BSC / Mixed]
- Thang: [1-5 / A-E]
- Liên kết lương: [mô tả]
- Liên kết thăng tiến: [mô tả]
- Appeal: [Có/Không]

FORMAT:
- Rating scale: Bảng Score | Label | Mô tả | % NV kỳ vọng (bell curve guide)
- Quy trình flowchart: Mermaid — Set goals → Mid-review → Self-assess → Manager assess → Calibrate → Feedback → Sign-off
- Calendar: Timeline 12 tháng × milestones đánh giá
- C&B linkage matrix: Rating | % tăng lương | Thưởng multiplier | Thăng tiến eligible
- Calibration guide: Forced distribution vs Absolute scale — pros/cons
- Appeal flowchart: NV khiếu nại → HR review → Committee → Quyết định cuối
- FAQ: 10 câu phổ biến — "KPI chưa có thì đánh giá thế nào?", "Mới vào 3 tháng có đánh giá?"

TONE: Công bằng, minh bạch, phát triển — không phải trừng phạt.
LENGTH: 6-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
