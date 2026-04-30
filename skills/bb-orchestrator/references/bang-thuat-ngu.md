# PROMPT 08: Master Glossary (Bảng thuật ngữ chuẩn hóa)

#### Mô tả
Bảng thuật ngữ thống nhất cho toàn bộ hệ thống 200+ tài liệu. Đảm bảo mọi skill con dùng cùng một thuật ngữ, cùng một cách viết tắt, cùng một định nghĩa. Tránh tình trạng "KPI" trong file A nghĩa khác file B.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN có thuật ngữ nội bộ riêng không? (VD: gọi nhân viên là "partner", gọi khách hàng là "member")
2. Ngôn ngữ chính của tài liệu: tiếng Việt có thuật ngữ Anh, hay full song ngữ?
3. Có acronyms nội bộ cần đưa vào không?
4. Muốn phân loại theo chủ đề hay theo alphabet?

#### Template gợi ý
Cấu trúc MAN:
- **Quy tắc sử dụng** — Cách dùng glossary, khi nào tham chiếu
- **Bảng thuật ngữ chính** — Term | Viết tắt | Định nghĩa (Việt) | Definition (English) | Ví dụ | Dùng trong skill #
- **Phân loại theo chủ đề** — 9 nhóm theo 9 khía cạnh DN
- **Thuật ngữ nội bộ DN** — Section riêng cho terms đặc thù
- **Danh sách viết tắt** — Quick reference A-Z
- **Version log** — Ai sửa gì khi nào

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Master Glossary cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- Hệ thống 200+ tài liệu, 12 skill con, 9 khía cạnh DN
- Ngôn ngữ: Tiếng Việt + thuật ngữ chuyên ngành song ngữ Việt-Anh
- DN: [Tên DN] — thuật ngữ nội bộ: [liệt kê nếu có]

FORMAT:
- Bảng chính: # | Thuật ngữ | Viết tắt | Định nghĩa (VI) | Definition (EN) | Ví dụ sử dụng | Xuất hiện trong Skill
- Phân nhóm theo 9 khía cạnh + 1 nhóm "Chung"
- Quick Reference Card: 1 trang A4, chỉ chứa viết tắt + nghĩa ngắn
- Thuật ngữ cơ bản ban đầu: ~100-150 terms phổ biến trong kinh doanh
- Để trống section "Thuật ngữ nội bộ DN" để chủ DN bổ sung

TONE: Reference material — ngắn gọn, chính xác, dễ tra cứu.
LENGTH: 10-15 trang A4 (bao gồm ~150 terms ban đầu).
```
