# PROMPT 02: ĐKKD Scan Checklist (Checklist hồ sơ đăng ký kinh doanh)

#### Mô tả
Checklist giúp DN rà soát, scan, lưu trữ số hóa toàn bộ hồ sơ pháp lý gốc. Đảm bảo không thiếu giấy tờ nào, mỗi bản scan đều có metadata đầy đủ.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hình DN? (ảnh hưởng danh sách giấy tờ cần có)
2. DN đã hoạt động bao lâu? (DN lâu năm có nhiều giấy tờ bổ sung/thay đổi)
3. Có chi nhánh/văn phòng đại diện không?
4. Lưu trữ số ở đâu? (Google Drive / NAS / SharePoint)
5. Naming convention cho file scan? (VD: DKKD_2024_v1.pdf)

#### Template gợi ý
Cấu trúc FRM:
- **Bảng checklist chính**: # | Tên giấy tờ | Bắt buộc? | Có bản gốc? | Đã scan? | Đường dẫn file | Ngày scan | Ghi chú
- **Phân loại**: (A) Hồ sơ thành lập, (B) Thay đổi ĐKKD, (C) Giấy phép con, (D) Thuế, (E) Khác
- **Hướng dẫn scan**: Độ phân giải, format (PDF), naming, folder structure
- **Checklist metadata**: Mỗi file scan cần: ngày cấp, cơ quan cấp, số hiệu, hạn hiệu lực

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo ĐKKD Scan Checklist — checklist rà soát & số hóa hồ sơ pháp lý.

CONTEXT:
- Loại hình DN: [loại hình]
- Năm thành lập: [năm] — Số lần thay đổi ĐKKD: [số]
- Chi nhánh: [có/không] — Số lượng: [số]
- Storage: [Google Drive / NAS / SharePoint]
- Naming: [convention]

FORMAT:
- Bảng checklist: checkbox ☐ cho mỗi mục
- Phân 5 nhóm: (A) Thành lập, (B) Thay đổi, (C) Giấy phép con, (D) Thuế, (E) Khác
- Mỗi mục: Tên | Số hiệu | Ngày cấp | Cơ quan | Hạn | Bản gốc ☐ | Scan ☐ | Link
- Hướng dẫn scan: 300dpi, PDF/A, naming = [Loại]_[Số]_[Ngày].pdf
- Tổng kết: __/__ giấy tờ đã đủ, __/__ đã scan

TONE: Hành chính, rõ ràng, dạng form.
LENGTH: 3-5 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
