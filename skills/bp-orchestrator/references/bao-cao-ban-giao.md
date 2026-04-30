# PROMPT 06: Handover Report (Báo cáo bàn giao)

#### Mô tả
Template báo cáo tổng kết sau khi hoàn thành toàn bộ dự án đóng gói. Tóm tắt những gì đã tạo, hướng dẫn sử dụng, và next steps cho DN.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Bàn giao cho ai? (Chủ DN / CEO / COO / Team quản lý)
2. Format mong muốn? (PDF report / Presentation / Markdown)
3. Cần training session kèm theo không?
4. Có commitment follow-up sau bàn giao không? (30/60/90 ngày)

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — 1 trang: DN nào, scope gì, kết quả tổng quan
- **Deliverables Inventory** — Bảng liệt kê toàn bộ files đã tạo, phân theo tầng
- **Maturity Before/After** — Spider chart: 9 khía cạnh, score trước vs sau
- **Quick Start Guide** — Top 10 files nên đọc đầu tiên
- **Implementation Roadmap** — Lộ trình triển khai: tuần 1-2-3-4 nên làm gì
- **FAQ** — 10 câu hỏi thường gặp khi bắt đầu dùng bộ tài liệu
- **Support & Next Steps** — Liên hệ hỗ trợ, lịch follow-up

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo template Handover Report cho dự án Đóng Gói Doanh Nghiệp.

CONTEXT:
- DN: [Tên DN] — Ngành: [ngành] — Quy mô: [số nhân sự]
- Scope: [Full / Selective] — Skills đã chạy: [danh sách]
- Bàn giao cho: [Chức danh người nhận]
- Follow-up: [Có/Không] — [30/60/90 ngày]

FORMAT:
- Professional report layout: Cover page → TOC → Body → Appendix
- Executive Summary: 1 trang, bullet points, highlight key wins
- Deliverables table: Tầng | Skill | Files | Status | Priority sử dụng
- Spider/Radar chart data: 9 khía cạnh × before/after scores
- Quick Start: Top 10 files + vì sao nên đọc đầu tiên
- Implementation Roadmap: Gantt-style theo tuần
- FAQ: Q&A format, 10 câu
- Appendix: Full file list, glossary reference

TONE: Executive — chuyên nghiệp, tự tin, hướng hành động.
LENGTH: 8-12 trang A4.
```
