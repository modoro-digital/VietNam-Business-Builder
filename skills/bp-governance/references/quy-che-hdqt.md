# PROMPT 07: Quy chế HĐQT (Board of Directors Regulations)

#### Mô tả
Quy chế nội bộ quy định cách thức hoạt động, thẩm quyền, quy trình ra quyết định của HĐQT/HĐTV. Bổ sung chi tiết cho Điều lệ, phục vụ quản trị thực tế hàng ngày.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hình DN & cơ cấu quản trị?
2. HĐQT/HĐTV có bao nhiêu người? Có thành viên độc lập không?
3. Tần suất họp: hàng tháng / hàng quý?
4. Có ủy ban chuyên trách không? (Kiểm toán, Nhân sự-Lương thưởng, Chiến lược)
5. Giới hạn quyết định tài chính: CEO được quyết đến bao nhiêu trước khi cần HĐQT duyệt?

#### Template gợi ý
Cấu trúc POL:
- **Chương I** — Phạm vi & Mục đích
- **Chương II** — Thành phần HĐQT: Số lượng, nhiệm kỳ, tiêu chuẩn, bầu/miễn nhiệm
- **Chương III** — Quyền hạn & Trách nhiệm: Danh sách quyền, giới hạn, reserved matters
- **Chương IV** — Cuộc họp: Triệu tập, agenda, quorum, biểu quyết, online meeting
- **Chương V** — Ủy ban chuyên trách: Thành lập, nhiệm vụ, báo cáo
- **Chương VI** — Quan hệ với BGĐ: Giám sát, ủy quyền, giới hạn tài chính
- **Chương VII** — Công bố thông tin & Xung đột lợi ích
- **Phụ lục**: Bảng phân quyền tài chính

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế HĐQT/HĐTV (Board Regulations).

CONTEXT:
- Loại hình: [loại] — Số thành viên HĐQT: [số] — Thành viên độc lập: [Có/Không]
- Tần suất họp: [tháng/quý]
- Ủy ban: [liệt kê nếu có]
- Giới hạn tài chính CEO: [số tiền]
- Cơ sở: Luật DN 2020 + Điều lệ công ty

FORMAT:
- Chia chương, đánh số điều
- Bảng phân quyền tài chính: Loại quyết định | CEO | CFO | HĐQT | ĐHCĐ + Mức tiền
- Reserved Matters list: Danh sách quyết định PHẢI qua HĐQT
- Quy trình ra quyết định: Flowchart mermaid

TONE: Chính thức, nội bộ, rõ ràng.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
