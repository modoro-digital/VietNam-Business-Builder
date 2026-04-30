# P-PPL-13: Scorecard đánh giá ứng viên (Candidate Evaluation Scorecard)

#### Mô tả
Bảng đánh giá ứng viên sau phỏng vấn — tổng hợp điểm theo tiêu chí có trọng số, đưa ra quyết định Go/No-Go khách quan. Dùng cho từng interviewer và tổng hợp panel.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Bao nhiêu tiêu chí đánh giá? (thường 8-12)
2. Trọng số mỗi tiêu chí? (VD: Kinh nghiệm 25%, Culture fit 20%, Kỹ năng 20%...)
3. Thang điểm: 1-5 hay 1-10?
4. Bao nhiêu interviewer cùng đánh giá? (cần form cá nhân + form tổng hợp)
5. Quyết định: Majority vote hay consensus?

#### Template gợi ý
Cấu trúc FRM:
- **Individual Scorecard**: 1 form per interviewer — Tiêu chí × Điểm × Notes
- **Panel Summary**: Tổng hợp tất cả interviewers — so sánh trên 1 bảng
- **Decision Framework**: Score thresholds → Hire / Maybe / No Hire
- **Comparison View**: Ứng viên A vs B vs C — side by side

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Scorecard đánh giá ứng viên (Candidate Evaluation Scorecard).

CONTEXT:
- DN: [Tên] — Số tiêu chí: [8-12]
- Trọng số: [VD: KN 25% | Kỹ năng 20% | Culture 20% | Communication 15% | Problem Solving 10% | Motivation 10%]
- Thang điểm: [1-5 / 1-10]
- Số interviewers: [số]
- Quyết định: [Majority / Consensus]

FORMAT:
- Individual form: Bảng Tiêu chí | Trọng số | Điểm 1-5 | Evidence/Notes
- Rubric mỗi tiêu chí: Score 1 (mô tả) → 3 (mô tả) → 5 (mô tả)
- Weighted score: Formula rõ ràng — Sum(Weight × Score) = Total
- Panel summary: Bảng Tiêu chí | Interviewer 1 | 2 | 3 | Average | Weighted
- Decision thresholds: ≥[X] Strongly Hire 🟢 | ≥[Y] Hire 🟡 | ≥[Z] Maybe 🟠 | <[Z] No Hire 🔴
- Comparison matrix: 3 ứng viên × 12 tiêu chí — highlight top scorer per tiêu chí

TONE: Objective, quantitative, bias-free.
LENGTH: 2-3 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
