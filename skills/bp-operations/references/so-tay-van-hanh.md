### PROMPT 10: Operations Manual (Sổ tay Vận hành Tổng thể)

#### Mô tả
Tài liệu tổng quan mô tả toàn bộ hệ thống vận hành DN — nguyên tắc, cấu trúc quy trình, KPIs vận hành, escalation. Đây là "bible" để ai vào cũng hiểu DN vận hành thế nào. Theo triết lý E-Myth: "Document everything so anyone can run it."

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN hoạt động trong lĩnh vực gì? (sản xuất / dịch vụ / thương mại / SaaS)
2. Có bao nhiêu quy trình cốt lõi tạo ra giá trị cho KH? (EOS: thường 3-7)
3. KPIs vận hành chính? (On-time delivery, Quality rate, Utilization...)
4. Có ca kíp không? Có nhiều site/chi nhánh?
5. Điểm đau vận hành lớn nhất hiện tại?

#### Template gợi ý
Cấu trúc MAN:
- **Chương 1** — Tổng quan: Sứ mệnh vận hành, nguyên tắc, đội ngũ key
- **Chương 2** — Chuỗi giá trị: Value chain diagram, core processes map
- **Chương 3** — Danh mục quy trình: SOP registry — tên, mã, version, owner
- **Chương 4** — KPIs vận hành: Dashboard metrics, targets, measurement
- **Chương 5** — Escalation: Ma trận escalation theo mức độ sự cố
- **Chương 6** — Cải tiến liên tục: PDCA cycle, suggestion box, Kaizen events
- **Chương 7** — Tools & Systems: Phần mềm, thiết bị, hạ tầng
- **Phụ lục**: Process map tổng, SOP index, Contact directory

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Operations Manual (Sổ tay Vận hành Tổng thể).

CONTEXT:
- DN: [Tên] — Lĩnh vực: [SX / DV / TM / SaaS]
- Core processes: [số] — Tên: [liệt kê]
- KPIs chính: [liệt kê]
- Ca kíp: [Có/Không] — Multi-site: [Có/Không]
- Pain points: [liệt kê]

FORMAT:
- Value chain diagram: Mermaid — từ input → core processes → output → customer
- SOP registry: Bảng Mã SOP | Tên | Phòng ban | Owner | Version | Last updated | Status
- KPI dashboard: Bảng KPI | Target | Actual | Status 🟢🟡🔴 | Trend
- Escalation matrix: Mức độ (1-4) | Mô tả | Thời gian xử lý | Người xử lý | Thông báo
- PDCA template: Plan-Do-Check-Act cho cải tiến
- Organization for Ops: Mini org chart cho team vận hành

TONE: E-Myth style — hệ thống hóa, bất kỳ ai cũng follow được.
LENGTH: 10-15 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
