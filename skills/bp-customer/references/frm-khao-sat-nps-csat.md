### PROMPT 04: Khảo sát NPS/CSAT (NPS & CSAT Survey Templates)

#### Mô tả
Template khảo sát đo lường sự hài lòng và trung thành KH — NPS (Net Promoter Score), CSAT (Customer Satisfaction Score), CES (Customer Effort Score). Kèm framework phân tích và lập kế hoạch hành động.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Đã từng đo NPS/CSAT chưa? Kết quả?
2. Kênh khảo sát ưu tiên? (email / in-app / SMS / gọi điện)
3. Tần suất khảo sát mong muốn? (sau mỗi giao dịch / hàng quý / hàng năm)
4. Số KH cần khảo sát? Tỷ lệ phản hồi mong đợi?
5. Ai sẽ phân tích kết quả và lập action plan?

#### Template gợi ý
Cấu trúc FRM:
- **NPS Survey**: 1 câu hỏi core (0-10) + 1 câu hỏi mở "Tại sao?" + phân loại Promoter/Passive/Detractor
- **CSAT Survey**: 3-5 câu hỏi theo dimension (sản phẩm, dịch vụ, tốc độ, nhân viên, overall)
- **CES Survey**: "Bạn dễ dàng giải quyết vấn đề đến mức nào?" (1-7)
- **Analysis Framework**: Công thức tính, benchmark ngành, trend analysis
- **Action Planning**: Score range → Action → Owner → Timeline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Khảo sát NPS/CSAT/CES.

CONTEXT:
- DN: [Tên] — B2B/B2C: [loại]
- Đã đo: [NPS=X / CSAT=X% / Chưa]
- Kênh: [email / in-app / SMS / gọi]
- Tần suất: [transactional / quarterly / annual]
- Số KH: [số] — Response rate target: [%]

FORMAT:
- NPS survey template: 1 câu core + 1 follow-up open + thank you page
- CSAT survey template: 5 câu rated (1-5) + 1 open + conditional logic
- CES survey template: 1 câu core (1-7) + 1 follow-up
- Scoring guide: NPS formula (% Promoter - % Detractor) | CSAT formula (satisfied/total) | CES formula
- Benchmark: Industry average NPS/CSAT + target setting
- Analysis template: Bảng Period | NPS | CSAT | CES | Trend | Top issues | Actions
- Action matrix: Score range | Urgency | Action | Owner | Timeline
- Closing the loop: Quy trình phản hồi KH sau khảo sát — Detractor (24h) | Passive (1 tuần) | Promoter (cảm ơn + referral)

TONE: Data-driven, actionable, customer-focused.
LENGTH: 5-7 trang A4.
```



---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
