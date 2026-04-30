### PROMPT 06: Sales Script (Kịch bản bán hàng)

#### Mô tả
Bộ kịch bản bán hàng chuẩn hóa cho từng kênh (telesales, tư vấn trực tiếp, online chat) và từng sản phẩm/buyer persona. Không phải "đọc thuộc lòng" mà là framework để sales rep navigate cuộc hội thoại hiệu quả.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Kênh bán hàng chính cần script? (telesales / face-to-face / online chat / video call)
2. Sản phẩm/dịch vụ cần script? (liệt kê top 3)
3. Buyer persona chính? (chức danh, pain points, buying triggers)
4. Thời lượng trung bình 1 cuộc tư vấn?
5. Objections phổ biến nhất? (top 5)
6. Call-to-action mong muốn? (đặt hẹn / demo / mua ngay / trial)
7. Có script hiện tại không? Điểm yếu?

#### Template gợi ý
Cấu trúc FRM:
- **Nguyên tắc sử dụng script**: Guidelines — adapt, không đọc thuộc
- **Script Telesales**: Opening → Discovery → Presentation → Close → Follow-up
- **Script Tư vấn trực tiếp**: Chào hỏi → Khám phá nhu cầu → Demo/Trình bày → Xử lý từ chối → Chốt
- **Script Online Chat**: Auto-greeting → Quick qualify → Value proposition → CTA → Chuyển offline
- **Per Persona Variations**: Persona A → adjust messaging, Persona B → adjust messaging
- **Power Phrases**: Câu hỏi hay, câu chốt hay, câu xử lý từ chối hay
- **Anti-patterns**: Những câu KHÔNG được nói
- **Phụ lục**: Roleplay scenarios, Scoring rubric

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sales Script (Kịch bản bán hàng).

CONTEXT:
- DN: [Tên] — SP/DV: [liệt kê top 3]
- Kênh: [telesales / face-to-face / chat / video call]
- Persona: [Tên persona | Chức danh | Pain point | Trigger]
- Thời lượng TB: [phút]
- Objections top 5: [liệt kê]
- CTA: [đặt hẹn / demo / mua / trial]

FORMAT:
- Script structure per kênh: Flowchart giai đoạn + thời lượng mỗi giai đoạn
- Verbatim script: Câu chào → Câu mở → Discovery questions (5-7 câu) → Pitch → Close
- Branching: IF khách nói X THEN → response A; IF khách nói Y THEN → response B
- Persona variations: Bảng Giai đoạn | Persona A | Persona B | Persona C
- Power phrases: 10 câu hỏi hay + 10 câu chốt hay + 10 câu bridge
- Anti-patterns: 10 câu KHÔNG được nói + lý do + thay thế bằng gì
- Practice scenarios: 3 roleplay tình huống (easy / medium / hard)
- Scoring: Bảng tiêu chí đánh giá cuộc gọi/tư vấn

TONE: Tự nhiên, tư vấn (không "sale"), chuyên nghiệp.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
