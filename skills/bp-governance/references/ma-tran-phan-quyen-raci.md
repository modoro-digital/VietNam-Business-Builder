# PROMPT 09: Ma trận phân quyền RACI (Decision Authority Matrix)

#### Mô tả
Ma trận RACI (Responsible-Accountable-Consulted-Informed) cho tất cả quyết định quan trọng trong DN. Xác định rõ ai làm, ai chịu trách nhiệm, ai cần hỏi ý kiến, ai cần thông báo — cho mỗi loại quyết định.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sơ đồ tổ chức hiện tại? (các cấp quản lý)
2. Danh sách quyết định quan trọng thường gặp? (VD: tuyển dụng, chi tiêu, ký HĐ, ra sản phẩm mới...)
3. Hiện tại có vấn đề gì về phân quyền? (VD: CEO bottleneck, không rõ ai quyết)
4. Muốn phân theo lĩnh vực hay theo cấp quyết định?

#### Template gợi ý
Cấu trúc FRM:
- **Hướng dẫn đọc**: R/A/C/I nghĩa là gì, quy tắc "Mỗi hàng chỉ 1 chữ A"
- **Ma trận theo lĩnh vực**: Bảng cho mỗi lĩnh vực (Tài chính, Nhân sự, Kinh doanh, Vận hành, Marketing...)
- **Mỗi bảng**: Quyết định | HĐQT | CEO | CFO | HR Dir | Sales Dir | Ops Dir | Trưởng phòng | Nhân viên
- **Escalation rules**: Khi nào quyết định phải escalate lên cấp trên
- **Conflict resolution**: Khi 2 người cùng claim "A" cho 1 quyết định

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Ma trận phân quyền RACI (Decision Authority Matrix).

CONTEXT:
- Cơ cấu tổ chức: [mô tả hoặc link OrgChart]
- Số cấp quản lý: [số] — Danh sách chức danh: [liệt kê]
- Pain points hiện tại: [VD: CEO phải duyệt mọi thứ]
- Phân loại: [theo lĩnh vực / theo cấp / cả hai]

FORMAT:
- Legend: R=Responsible (Thực hiện), A=Accountable (Chịu trách nhiệm), C=Consulted (Tham vấn), I=Informed (Thông báo)
- Ma trận per domain: 6-8 bảng (Tài chính, Nhân sự, Kinh doanh, Marketing, Vận hành, IT, Pháp lý, Chiến lược)
- Mỗi bảng: 8-15 quyết định × 6-8 vai trò
- Mỗi ô: R / A / C / I / — (không liên quan)
- Quy tắc: Highlight nếu 1 hàng thiếu A, hoặc 1 cột có quá nhiều A (bottleneck)
- Summary: Bảng tổng kết workload per role

TONE: Structured, analytical.
LENGTH: 8-12 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
