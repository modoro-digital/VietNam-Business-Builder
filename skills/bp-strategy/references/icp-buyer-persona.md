# PROMPT 09: Ideal Customer Profile — ICP & Buyer Persona

#### Mô tả
Chân dung khách hàng lý tưởng ở 2 cấp: ICP (cấp công ty/tổ chức cho B2B, hoặc segment cho B2C) và Buyer Persona (cấp cá nhân ra quyết định). Là nền tảng cho Sales targeting, Marketing messaging, Product development.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. B2B hay B2C? (hoặc cả hai)
2. Top 5 khách hàng hiện tại tốt nhất? (mô tả: ngành, quy mô, vì sao họ mua)
3. Top 3 khách hàng xấu nhất? (mô tả: vì sao không phù hợp)
4. Quy trình ra quyết định mua? (ai quyết, ai ảnh hưởng, bao lâu)
5. Pain points chính mà KH tìm đến DN?
6. Kênh KH thường dùng để tìm giải pháp? (Google, referral, social, event...)
7. Có data KH nào? (CRM, survey, interview)

#### Template gợi ý
Cấu trúc FRM:
- **ICP (Company-level, B2B)** — Industry, Size (revenue/employee), Geography, Tech stack, Budget, Buying trigger, Disqualification criteria
- **Buyer Persona (Individual-level)** — 2-3 personas, mỗi persona có:
  - Tên + Avatar (fictional)
  - Demographics: Tuổi, chức danh, thu nhập, học vấn
  - Goals & Challenges: 3 mục tiêu + 3 thách thức
  - Decision criteria: Tiêu chí đánh giá khi mua
  - Objections: 3-5 phản đối thường gặp + cách xử lý
  - Content preferences: Kênh, format, tần suất
  - Quote: 1 câu đại diện ("Tôi cần...")
  - Journey map: Awareness → Consideration → Decision → Post-purchase
- **Anti-Persona** — Profile khách hàng KHÔNG phù hợp (tránh waste effort)
- **Scoring Model** — Lead scoring criteria dựa trên ICP fit

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo ICP & Buyer Persona.

CONTEXT:
- DN: [Tên] — Model: [B2B / B2C / B2B2C]
- Top 5 KH tốt: [mô tả ngắn mỗi KH]
- Top 3 KH xấu: [mô tả ngắn + lý do]
- Quy trình mua: [mô tả]
- Pain points KH: [liệt kê]
- Kênh KH dùng: [liệt kê]
- Data nguồn: [CRM / survey / interview / ước lượng]

FORMAT:
- ICP card: 1 trang, visual, key criteria + thresholds
- Buyer Persona: 2-3 personas × 1 trang mỗi persona (visual card format)
- Anti-Persona: 1/2 trang — "DON'T sell to..."
- Objection Handling: Bảng Objection | Root cause | Response
- Journey Map per persona: 4 stages × Touchpoints/Actions/Emotions/Needs
- Lead Scoring: Criteria | Weight | Score range | Threshold (MQL/SQL)

TONE: Marketing strategy — empathetic, data-informed, actionable.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
