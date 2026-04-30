# PROMPT 01: Intake Questionnaire (Bộ câu hỏi thu thập thông tin DN)

#### Mô tả
Bộ câu hỏi có cấu trúc để thu thập toàn bộ thông tin cần thiết từ chủ doanh nghiệp trước khi bắt đầu đóng gói. Đây là bước quan trọng nhất — "garbage in, garbage out". Chia thành 5 nhóm câu hỏi, từ cơ bản đến chuyên sâu.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Anh muốn bộ câu hỏi ở dạng nào? (Google Form / Markdown checklist / PDF form / Interactive prompt)
2. Ngành nghề cụ thể của DN? (để customize câu hỏi đặc thù ngành)
3. Ai sẽ là người điền? (chủ DN trực tiếp / trợ lý / team?)
4. Có cần version tiếng Anh song song không?
5. Mức độ chi tiết mong muốn? (Quick scan ~20 câu / Standard ~50 câu / Deep dive ~100 câu)

#### Template gợi ý
Cấu trúc 5 nhóm câu hỏi:
- **Nhóm 1 — Thông tin cơ bản** (10-15 câu): Tên DN, ngành, năm thành lập, doanh thu, nhân sự, địa bàn, pháp nhân
- **Nhóm 2 — Giai đoạn phát triển** (8-10 câu): Stage hiện tại (startup/growth/mature), mục tiêu 1-3-5 năm, đã gọi vốn chưa, có kế hoạch mở chuỗi/nhượng quyền không
- **Nhóm 3 — Cấu trúc hiện tại** (10-15 câu): Có sơ đồ tổ chức chưa, bao nhiêu phòng ban, quy trình nào đã chuẩn hóa, công cụ đang dùng (CRM, ERP, kế toán...)
- **Nhóm 4 — Ưu tiên & Pain points** (8-10 câu): Top 3 vấn đề lớn nhất, lĩnh vực muốn ưu tiên đóng gói, budget & timeline
- **Nhóm 5 — Đặc thù ngành** (5-10 câu): Quy định ngành, giấy phép đặc biệt, seasonal patterns, đặc điểm nhân sự ngành

Format: Markdown với checkbox, mỗi câu có hint/ví dụ. Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo bộ câu hỏi thu thập thông tin doanh nghiệp (Intake Questionnaire) cho dự án Đóng Gói Doanh Nghiệp.

CONTEXT:
- Mục đích: Thu thập đủ thông tin để AI + Business Coach xác định scope đóng gói và customize 200+ tài liệu cho DN cụ thể
- Người điền: [Chủ DN / Trợ lý] — ngành [ngành nghề]
- Mức độ: [Quick/Standard/Deep dive]

FORMAT:
- Markdown với checkbox [ ] cho mỗi câu hỏi
- Mỗi câu có: Câu hỏi chính → Gợi ý/ví dụ (in nghiêng) → Ô trả lời
- Chia rõ 5 nhóm, đánh số liên tục
- Song ngữ Việt-Anh cho thuật ngữ chuyên ngành
- Cuối mỗi nhóm có "Ghi chú bổ sung" dạng free-text

TONE: Chuyên nghiệp nhưng thân thiện, dễ hiểu cho chủ DN không chuyên.
LENGTH: [20/50/100] câu hỏi tùy mức độ đã chọn.

OUTPUT: File markdown hoàn chỉnh, sẵn sàng gửi cho chủ DN điền.
```
