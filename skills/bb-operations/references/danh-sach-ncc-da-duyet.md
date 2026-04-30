### PROMPT 08: Danh sách NCC đã duyệt (Approved Vendor List — AVL)

#### Mô tả
Registry tổng hợp tất cả NCC đã qua đánh giá và được phê duyệt. Chỉ được đặt hàng từ NCC trong danh sách này (trừ trường hợp đặc biệt có duyệt GĐ).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện tại có bao nhiêu NCC đang làm việc?
2. Phân loại NCC theo nhóm nào? (ngành hàng / dịch vụ / khu vực)
3. Thông tin nào cần lưu cho mỗi NCC? (MST, liên hệ, HĐ khung, score...)
4. Ai có quyền thêm/xóa NCC khỏi danh sách?
5. Tần suất review danh sách? (6 tháng / 1 năm)
6. Có NCC nào đang bị suspend hoặc blacklist không?

#### Template gợi ý
Cấu trúc FRM:
- **Master Registry**: Bảng tổng hợp toàn bộ NCC — mã, tên, MST, ngành hàng, liên hệ, HĐ, score, status
- **Phân nhóm**: Theo ngành hàng/dịch vụ — mỗi nhóm liệt kê top NCC
- **Status tracking**: Active 🟢 | Under Review 🟡 | Suspended 🟠 | Blacklisted 🔴
- **Quick lookup**: Ngành hàng → Top 3 NCC recommended (dựa trên score)
- **Quy trình thêm/xóa**: Flowchart đơn giản — Đề xuất → Đánh giá → Duyệt → Cập nhật AVL
- **Update log**: Ngày | Thay đổi | Lý do | Người cập nhật

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Approved Vendor List (Danh sách NCC đã duyệt).

CONTEXT:
- DN: [Tên] — Số NCC: [số]
- Phân loại: [ngành hàng / dịch vụ / khu vực]
- Người duyệt: [chức danh]
- Review cycle: [6 tháng / 1 năm]

FORMAT:
- Registry: # | NCC | MST | Ngành hàng | Liên hệ | SĐT | Email | HĐ khung # | Hạn HĐ | Score | Status
- Phân nhóm: Theo ngành hàng/dịch vụ
- Status: Active 🟢 | Under Review 🟡 | Suspended 🟠 | Blacklisted 🔴
- Quick lookup: Ngành hàng → Top 3 NCC recommended
- Quy trình cập nhật: Flowchart thêm/xóa NCC
- Update log: Ngày | Thay đổi | Người cập nhật

TONE: Registry, reference material, dễ tra cứu.
LENGTH: 2-4 trang A4.

CROSS-REFERENCE: Liên kết với Scorecard NCC (P-OPS-07) để lấy score đánh giá.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
