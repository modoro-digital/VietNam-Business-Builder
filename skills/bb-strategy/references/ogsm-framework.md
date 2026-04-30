# PROMPT 11: OGSM Framework

#### Mô tả
OGSM (Objectives-Goals-Strategies-Measures) — công cụ chiến lược 1 trang kết nối tầm nhìn dài hạn với hành động cụ thể. Đơn giản hơn Business Plan, dễ truyền thông cho toàn team.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Objective (mục tiêu lớn): DN muốn đạt được gì trong 3-5 năm tới?
2. Goals (mục tiêu đo lường): KPIs cụ thể kèm target?
3. Strategies (chiến lược): 3-5 cách tiếp cận chính?
4. Time period: Năm tài chính nào?
5. Đã có OKR riêng chưa? (OGSM ở cấp cao hơn OKR)

#### Template gợi ý
Cấu trúc FRM (1-2 trang):
- **Objective** — 1 câu, qualitative, inspiring (VD: "Trở thành nền tảng marketing #1 cho SME Việt Nam")
- **Goals** — 3-5 metrics, quantitative, time-bound (VD: "Doanh thu 100 tỷ 2026", "50.000 KH active")
- **Strategies** — 3-5 chiến lược lớn, mỗi chiến lược có description ngắn
- **Measures** — Mỗi strategy có 2-3 KPIs cụ thể + target + frequency đo
- **OGSM Map** — 1 trang visual: O → G1,G2,G3 → S1,S2,S3 → M1.1, M1.2...

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo OGSM Framework.

CONTEXT:
- DN: [Tên] — Objective: [mô tả mục tiêu lớn]
- Goals: [liệt kê KPIs + targets]
- Strategies: [liệt kê 3-5 chiến lược]
- Period: [năm/giai đoạn]
- Existing OKR: [Có/Không]

FORMAT:
- OGSM table: 4 cột (O|G|S|M), cascade rõ ràng
- 1-page overview: Fit on 1 trang A4, landscape orientation
- Detail page: Mỗi Strategy → Measures → Action items → Owner → Timeline
- Alignment check: Mỗi Measure phải link ngược lên Goal, mỗi Goal link lên Objective
- Quarterly review template: Kèm bảng review tiến độ

TONE: Strategic, concise, executive-friendly.
LENGTH: 2-4 trang A4 (1 trang OGSM + 1-3 trang detail).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
