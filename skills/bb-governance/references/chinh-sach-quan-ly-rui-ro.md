# PROMPT 10: Chính sách quản lý rủi ro (Risk Management Policy)

#### Mô tả
Framework toàn diện để nhận diện, đánh giá, xử lý và giám sát rủi ro ở cấp DN. Theo chuẩn ISO 31000:2018, customize cho DN Việt Nam.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ngành nghề & quy mô? (xác định profile rủi ro)
2. Đã từng gặp sự cố nghiêm trọng nào chưa? (VD: mất data, kiện tụng, sự cố sản xuất)
3. Có bộ phận quản lý rủi ro riêng không?
4. Khẩu vị rủi ro (Risk Appetite): DN thuộc loại risk-averse hay risk-taking?
5. Có cần risk register template kèm theo không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích, Phạm vi, Cam kết của lãnh đạo
- **Phần 2** — Thuật ngữ & Định nghĩa (theo ISO 31000)
- **Phần 3** — Framework quản lý rủi ro: Nhận diện → Phân tích → Đánh giá → Xử lý → Giám sát
- **Phần 4** — Phân loại rủi ro: Chiến lược / Tài chính / Vận hành / Tuân thủ / Uy tín / Công nghệ
- **Phần 5** — Ma trận rủi ro: Likelihood (1-5) × Impact (1-5) = Risk Score
- **Phần 6** — Chiến lược xử lý: Tránh / Giảm thiểu / Chuyển giao / Chấp nhận
- **Phần 7** — Vai trò & Trách nhiệm
- **Phần 8** — Báo cáo & Rà soát định kỳ
- **Phụ lục**: Risk Register template, Heat Map template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách quản lý rủi ro (Risk Management Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Quy mô: [nhân sự, doanh thu]
- Sự cố đã gặp: [liệt kê hoặc "chưa"]
- Bộ phận RM: [Có/Không]
- Risk Appetite: [Conservative / Moderate / Aggressive]
- Chuẩn tham khảo: ISO 31000:2018

FORMAT:
- Chia phần rõ ràng, có mục lục
- Risk Matrix 5×5: Likelihood × Impact, color-coded (Green/Yellow/Orange/Red)
- Risk Categories: 6 loại với ví dụ cụ thể cho ngành DN
- Treatment strategies: Bảng: Risk | Strategy | Action | Owner | Timeline | KRI
- Risk Register template: # | Mô tả | Loại | L | I | Score | Strategy | Owner | Status
- Quy trình báo cáo: Flowchart khi phát hiện rủi ro mới

TONE: Chuyên nghiệp, ISO-aligned, thực tế.
LENGTH: 10-15 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
