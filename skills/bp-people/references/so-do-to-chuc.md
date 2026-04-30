# P-PPL-01: Sơ đồ tổ chức (Organization Chart)

#### Mô tả
Sơ đồ tổ chức chính thức của DN — thể hiện cấu trúc phòng ban, tuyến báo cáo (reporting lines), span of control. Là "bản đồ quyền lực" giúp mọi người hiểu ai báo cáo ai, ai chịu trách nhiệm gì.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Cơ cấu hiện tại có bao nhiêu phòng ban/bộ phận?
2. Tổng nhân sự hiện tại? Phân bổ theo phòng ban?
3. Cấu trúc: Functional (theo chức năng) / Divisional (theo sản phẩm/địa bàn) / Matrix?
4. Có vị trí nào đang trống (vacant) cần tuyển?
5. Có kế hoạch thay đổi cơ cấu trong 6-12 tháng tới?
6. Mối quan hệ đặc biệt: dotted-line, kiêm nhiệm, outsource?

#### Template gợi ý
Cấu trúc MAN:
- **Tổng quan**: Loại cấu trúc, số cấp quản lý, tổng headcount
- **Org Chart**: Sơ đồ dạng Mermaid — từ HĐQT/CEO xuống phòng ban
- **Bảng chi tiết**: Phòng ban | Trưởng phòng | Headcount | Chức năng chính | Reporting to
- **Span of Control**: Phân tích — mỗi manager quản lý bao nhiêu người
- **Vacant Positions**: Vị trí đang trống + timeline tuyển dụng
- **Planned Changes**: Thay đổi dự kiến + timeline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sơ đồ tổ chức (Organization Chart).

CONTEXT:
- DN: [Tên] — Quy mô: [nhân sự] — Cấu trúc: [Functional / Divisional / Matrix]
- Phòng ban: [liệt kê]
- Headcount per dept: [chi tiết]
- Vị trí trống: [liệt kê]
- Thay đổi dự kiến: [mô tả]

FORMAT:
- Mermaid org chart: Từ HĐQT → CEO → C-level → Trưởng phòng → Team
- Bảng chi tiết: Dept | Head | HC | Function | Reports to | Dotted line
- Span of control: Manager | Direct reports | Ratio → Highlight nếu >7
- Color coding: Filled 🟢 | Vacant 🔴 | Planned 🟡
- Metrics: Total HC | Mgr:Staff ratio | Avg span of control | Layers

TONE: Chính thức, visual, rõ ràng.
LENGTH: 3-5 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
