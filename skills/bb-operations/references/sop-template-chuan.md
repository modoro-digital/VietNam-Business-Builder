### PROMPT 11: SOP Template chuẩn (Standard SOP Template)

#### Mô tả
Template chuẩn hóa format cho MỌI SOP trong DN. Đảm bảo mọi quy trình đều được viết cùng cấu trúc, dễ đọc, dễ cập nhật, dễ training.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Naming convention cho SOP? (VD: SOP-[Dept]-[###])
2. Versioning: v1.0 → v1.1 (minor) → v2.0 (major) hay convention khác?
3. Ai là người duyệt SOP? (TP / GĐ / cả hai)
4. Có logo DN để đặt vào header không?
5. Tần suất review SOP? (6 tháng / 1 năm)
6. Ngôn ngữ: chỉ tiếng Việt hay song ngữ Việt-Anh?

#### Template gợi ý
Cấu trúc FRM (meta-template):
- **Trang 1 — SOP Template**: Header (Logo, Tên, Mã, Version, Ngày, Owner, Duyệt) → 7 section chuẩn → Footer
- **Trang 2 — Hướng dẫn điền**: Mẹo viết SOP hiệu quả, dos/don'ts, ví dụ
- **7 section chuẩn cho mọi SOP**:
  1. Mục đích (1-2 câu)
  2. Phạm vi (áp dụng cho ai, khi nào)
  3. Thuật ngữ & Viết tắt (bảng)
  4. Trách nhiệm (RACI table)
  5. Quy trình (Flowchart + Bước chi tiết)
  6. Biểu mẫu liên quan (link)
  7. Lịch sử thay đổi (version log)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Template chuẩn (Standard SOP Template).

CONTEXT:
- DN: [Tên]
- Naming convention: [SOP-Dept-###]
- Versioning: [v1.0 → v1.1 → v2.0]
- Người duyệt: [chức danh]
- Review cycle: [6 tháng / 1 năm]

FORMAT:
- 1 trang template + 1 trang hướng dẫn điền
- Header: Logo | Tên SOP | Mã | Version | Ngày ban hành | Ngày review | Owner | Duyệt bởi
- Body sections:
  1. Mục đích (1-2 câu)
  2. Phạm vi (áp dụng cho ai, khi nào)
  3. Thuật ngữ & Viết tắt (bảng)
  4. Trách nhiệm (RACI table)
  5. Quy trình (Flowchart + Bước chi tiết)
  6. Biểu mẫu liên quan (link)
  7. Lịch sử thay đổi (version log)
- Footer: "Tài liệu nội bộ — Cấm sao chép" + Page number
- Hướng dẫn: Mẹo viết SOP hiệu quả, dos/don'ts

TONE: Meta-template, hướng dẫn chuẩn hóa.
LENGTH: 2-3 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
