# P-PPL-22: Form đánh giá 360 độ (360-Degree Feedback Form)

#### Mô tả
Form đánh giá 360 độ — thu thập phản hồi từ 4 góc: tự đánh giá (Self), cấp trên (Manager), đồng nghiệp (Peer), cấp dưới (Direct Report). Đánh giá theo năng lực (competencies) thay vì KPI — bổ sung cho KPI template.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Năng lực cần đánh giá? (VD: Leadership, Communication, Teamwork, Problem Solving, Innovation, Integrity...)
2. Số competencies: 8-12 hay nhiều hơn?
3. Thang điểm: 1-5 hay 1-7?
4. Có open comments không? (bắt buộc hay tùy chọn)
5. Ẩn danh: Peer và Direct Report có ẩn danh không?
6. Tần suất: Hàng năm / 6 tháng?

#### Template gợi ý
Cấu trúc FRM:
- **Form Self**: NV tự đánh giá — 20-25 statements × scale 1-5
- **Form Manager**: Cấp trên đánh giá — cùng statements
- **Form Peer**: Đồng nghiệp (2-3 người) — cùng statements + ẩn danh
- **Form Direct Report**: Cấp dưới (nếu có) — cùng statements + ẩn danh
- **Summary**: Radar chart data — so sánh Self vs Manager vs Peer vs DR
- **Development Plan**: Gap analysis → 2-3 điểm cần cải thiện → Action plan

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Form đánh giá 360 độ (360-Degree Feedback Form).

CONTEXT:
- DN: [Tên] — Competencies: [liệt kê 8-12]
- Thang điểm: [1-5 / 1-7]
- Open comments: [Bắt buộc / Tùy chọn]
- Ẩn danh Peer/DR: [Có/Không]
- Tần suất: [6 tháng / Năm]

FORMAT:
- 4 form riêng: Self | Manager | Peer | Direct Report
- Mỗi competency: 2-3 behavioral statements × scale 1-5
  VD: "Leadership" → "Truyền cảm hứng cho team đạt mục tiêu" [1-2-3-4-5]
- Rubric per score: 1 = Hiếm khi thể hiện | 3 = Thường xuyên | 5 = Luôn luôn, role model
- Open comment section: "Điểm mạnh nhất?" + "Cần cải thiện gì?" + "Lời khuyên?"
- Summary template: Bảng Competency | Self | Manager | Peer Avg | DR Avg | Gap (Self vs Others)
- Radar chart data: 8-12 axes × 4 sources
- Development plan: Top 3 gaps → Action | Timeline | Support needed | Success measure

TONE: Constructive, development-focused, không phải performance review tiêu cực.
LENGTH: 4-6 trang A4 (4 forms + summary + dev plan).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
