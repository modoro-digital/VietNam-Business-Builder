# PROMPT 15: Risk Register (Sổ đăng ký rủi ro)

#### Mô tả
Sổ đăng ký rủi ro chiến lược — danh mục tổng hợp, đánh giá, tracking tất cả rủi ro cấp DN. Khác với Risk Management Policy (01-governance) là framework/chính sách, đây là bảng THỰC TẾ liệt kê rủi ro cụ thể.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Đã có danh sách rủi ro từ Risk Management Policy chưa?
2. Top 5 rủi ro DN đang lo ngại nhất?
3. Ai sẽ là Risk Owner cho mỗi rủi ro?
4. Tần suất review: hàng tháng / hàng quý?
5. Có KRI (Key Risk Indicators) đã track chưa?

#### Template gợi ý
Cấu trúc FRM:
- **Risk Register Table**: ID | Category | Description | Likelihood (1-5) | Impact (1-5) | Score | Strategy | Mitigation Actions | Owner | KRI | Status | Last Review
- **Heat Map Data**: Bảng 5×5 với số lượng risks per cell
- **Top 10 Risks**: Card format — detailed analysis cho top 10
- **KRI Dashboard**: Metric | Threshold | Current | Trend (↑↓→)
- **Review Log**: Date | Reviewed by | Changes | New risks | Closed risks

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Risk Register.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Risk categories: [Strategy / Finance / Operations / Compliance / Reputation / Technology]
- Top 5 risks: [liệt kê]
- Risk Owners: [mapping]
- Review frequency: [monthly/quarterly]
- Existing KRIs: [liệt kê hoặc "chưa có"]

FORMAT:
- Main table: Full register với tất cả cột (12+ cột)
- Heat Map: 5×5 data grid, color-coded
- Top 10 Risk Cards: Mỗi risk = 1/2 trang detail — Root cause, Current controls, Residual risk, Action plan
- KRI tracking: Bảng indicators + trend arrows
- Review log: Template cho monthly/quarterly review
- Starter risks: Pre-populate 15-20 common risks per industry

TONE: Risk management — objective, vigilant, actionable.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
