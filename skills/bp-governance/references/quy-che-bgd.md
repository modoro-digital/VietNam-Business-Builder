# PROMPT 08: Quy chế BGĐ (Executive Management Regulations)

#### Mô tả
Quy chế hoạt động của Ban Giám đốc (CEO, các Phó GĐ, Giám đốc chức năng). Quy định phân công, ủy quyền, giới hạn quyết định, quy trình phối hợp giữa các thành viên BGĐ.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. BGĐ gồm bao nhiêu người? Chức danh cụ thể?
2. CEO có phải là Chủ tịch HĐQT không? (kiêm nhiệm?)
3. Phân công lĩnh vực phụ trách của mỗi Phó GĐ?
4. Giới hạn ký duyệt tài chính của từng cấp BGĐ?
5. Quy trình ủy quyền khi vắng mặt?

#### Template gợi ý
Cấu trúc POL:
- **Điều 1-3** — Phạm vi, mục đích, thuật ngữ
- **Điều 4-6** — Cơ cấu BGĐ: Thành phần, bổ nhiệm, miễn nhiệm
- **Điều 7-10** — Quyền & Trách nhiệm: CEO, Phó GĐ, GĐ chức năng — mỗi người 1 điều
- **Điều 11-13** — Phân quyền quyết định: Bảng chi tiết theo loại quyết định × cấp BGĐ
- **Điều 14-15** — Cuộc họp BGĐ: Tần suất, nghị sự, biên bản
- **Điều 16-17** — Ủy quyền & Thay thế khi vắng mặt
- **Điều 18** — Báo cáo cho HĐQT
- **Phụ lục**: Bảng phân quyền ký duyệt

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế BGĐ (Executive Management Regulations).

CONTEXT:
- BGĐ: [liệt kê chức danh + tên]
- CEO kiêm Chủ tịch: [Có/Không]
- Phân công: [VD: Phó GĐ Kinh doanh phụ trách Sales+Marketing, Phó GĐ Vận hành phụ trách Ops+HR]
- Giới hạn ký: CEO [số] | Phó GĐ [số] | GĐ chức năng [số]

FORMAT:
- Đánh số điều liên tục
- Bảng phân quyền: Loại quyết định | GĐ CN | Phó GĐ | CEO | HĐQT
- Bảng ủy quyền: Người ủy | Người được ủy | Phạm vi | Thời hạn
- Sơ đồ báo cáo: Mermaid org chart

TONE: Nội bộ, chính thức.
LENGTH: 6-10 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
