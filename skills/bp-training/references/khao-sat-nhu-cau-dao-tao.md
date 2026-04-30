### PROMPT 02: Training Needs Assessment (Khảo sát Nhu cầu Đào tạo)

#### Mô tả
Mẫu khảo sát và phân tích nhu cầu đào tạo ở 3 cấp: tổ chức (organizational), phòng ban (departmental), cá nhân (individual). Kết quả TNA là input chính cho Annual Training Plan. Dựa trên gap analysis giữa năng lực hiện tại và năng lực yêu cầu.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN có Competency Framework / Bảng năng lực chưa? (từ 04-People)
2. Nguồn dữ liệu nhu cầu: Performance review / Manager request / Employee survey / Business strategy?
3. Tần suất khảo sát TNA? (hàng năm / 6 tháng / theo dự án)
4. Ai điền khảo sát? (nhân viên tự đánh giá / quản lý đánh giá / cả hai)
5. Có phân biệt kỹ năng cứng vs mềm không?
6. Output mong muốn: báo cáo tổng hợp hay danh sách ưu tiên?

#### Template gợi ý
Cấu trúc FRM:
- **Phần 1** — Hướng dẫn sử dụng: Ai điền, khi nào, cách điền
- **Phần 2** — Organizational Needs: Chiến lược DN → năng lực cần xây dựng
- **Phần 3** — Departmental Needs: Phòng ban × Kỹ năng → Gap
- **Phần 4** — Individual Assessment: Nhân viên tự đánh giá + Manager đánh giá
- **Phần 5** — Gap Analysis Summary: Tổng hợp gap lớn nhất cần đào tạo
- **Phần 6** — Priority Matrix: Impact × Urgency → Ưu tiên đào tạo
- **Phụ lục**: Danh sách năng lực tham khảo, Hướng dẫn cho Manager

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Training Needs Assessment Form (Mẫu Khảo sát Nhu cầu Đào tạo).

CONTEXT:
- DN: [Tên] — Nhân sự: [số] — Số phòng ban: [số]
- Competency Framework: [Có/Không] — Nguồn: [04-People hoặc tự build]
- Nguồn dữ liệu: [Performance review / Manager / Survey / Strategy]
- Tần suất TNA: [hàng năm / 6 tháng]
- Người đánh giá: [tự đánh giá / manager / 360]

FORMAT:
- Organizational analysis: Bảng Strategic Goal | Required Capability | Current Level (1-5) | Gap | Priority
- Departmental analysis: Bảng Phòng ban | Kỹ năng | Required Level | Current Level | Gap | # Staff affected
- Individual assessment form:
  - Self-rating: Kỹ năng | Tự đánh giá (1-5) | Mong muốn phát triển (Yes/No) | Ghi chú
  - Manager rating: Kỹ năng | Đánh giá (1-5) | Priority (H/M/L) | Recommended training
- Gap heatmap template: Phòng ban × Kỹ năng → Color-coded (🟢 OK / 🟡 Gap nhỏ / 🔴 Gap lớn)
- Priority matrix: 2×2 — High Impact + Urgent = P1 | High Impact + Not Urgent = P2 | Low Impact + Urgent = P3 | Low = P4
- Summary report template: Top 10 gaps | Affected population | Recommended interventions | Budget estimate

TONE: Khảo sát dễ điền, phân tích có hệ thống.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
