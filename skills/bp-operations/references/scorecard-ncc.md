### PROMPT 07: Scorecard NCC (Vendor Scorecard)

#### Mô tả
Bảng đánh giá NCC theo tiêu chí có trọng số — Chất lượng, Giá cả, Giao hàng, Dịch vụ, Tài chính. Dùng cho đánh giá lần đầu và re-evaluation.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Trọng số các tiêu chí? (VD: CL 30% + Giá 25% + Giao hàng 20% + DV 15% + TC 10%)
2. Thang điểm: 1-5 hay 1-10?
3. Ngưỡng đạt: minimum score bao nhiêu?
4. Có rubric mô tả chi tiết mỗi mức điểm không?

#### Template gợi ý
Cấu trúc FRM:
- **Scorecard matrix**: 5 nhóm tiêu chí × 3-5 sub-criteria × Trọng số × Điểm
- **Rubric chi tiết**: Mỗi sub-criteria × mỗi mức điểm = mô tả hành vi cụ thể
- **Weighted score calculator**: Công thức tính điểm tổng hợp
- **Rating scale**: ≥X Approved 🟢 | ≥Y Conditional 🟡 | <Y Rejected 🔴
- **Comparison view**: NCC A vs B vs C trên cùng 1 bảng
- **Trend tracking**: Score kỳ này vs kỳ trước → xu hướng

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Vendor Scorecard (Bảng đánh giá NCC).

CONTEXT:
- DN: [Tên] — Trọng số: CL [%] | Giá [%] | Giao hàng [%] | DV [%] | TC [%]
- Thang điểm: [1-5 / 1-10]
- Ngưỡng đạt: [score]

FORMAT:
- Scorecard matrix: 5 nhóm tiêu chí × 3-5 sub-criteria mỗi nhóm × Trọng số × Điểm
- Rubric: Mỗi sub-criteria × mỗi mức điểm = mô tả cụ thể (VD: CL=5 "Zero defects in 6 months")
- Weighted score calculator: Formula rõ ràng
- Rating scale: ≥[X] Approved 🟢 | ≥[Y] Conditional 🟡 | <[Y] Rejected 🔴
- Comparison view: NCC A vs B vs C trên cùng 1 bảng
- Trend: Score kỳ này vs kỳ trước

TONE: Objective, quantitative, structured.
LENGTH: 3-4 trang A4.

CROSS-REFERENCE: Liên kết với SOP Đánh giá NCC (P-OPS-06) và AVL (P-OPS-08).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
