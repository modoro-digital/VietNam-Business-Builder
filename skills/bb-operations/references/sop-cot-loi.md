### PROMPT 12: SOP Cốt lõi 1-2-3 (Core Process SOPs)

#### Mô tả
3 SOP cốt lõi tạo ra giá trị trực tiếp cho khách hàng — tùy theo ngành nghề DN. Đây là "core processes" trong EOS: những quy trình mà nếu làm đúng, DN thành công; nếu làm sai, DN thất bại.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. 3 quy trình cốt lõi nhất của DN là gì? (VD: Bán hàng → Giao hàng → Hỗ trợ sau bán)
2. Mỗi quy trình hiện tại có bao nhiêu bước?
3. Điểm bottleneck / hay lỗi ở đâu?
4. Ai là owner mỗi quy trình?
5. KPI đo lường mỗi quy trình?

#### Template gợi ý
Cấu trúc SOP — Mỗi SOP theo SOP Template chuẩn (P-OPS-11):
- **Process map**: Flowchart end-to-end 5-10 bước chính
- **Swimlane diagram**: Vai trò × Bước — ai làm gì ở mỗi bước
- **Chi tiết từng bước**: Input | Action | Output | Tool | Time | Quality check
- **Exception handling**: 3-5 tình huống bất thường + cách xử lý
- **KPI per process**: 3-5 metrics + target + cách đo
- **Handover points**: Điểm bàn giao giữa các bộ phận — input/output rõ ràng
- EOS style: "Documented, Simplified, Followed By All"

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo 3 SOP Cốt lõi theo EOS Core Process.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- 3 Core Processes: [Tên 1] | [Tên 2] | [Tên 3]
- Bottlenecks: [mô tả]
- KPIs: [mỗi process]

FORMAT — Mỗi SOP theo SOP Template chuẩn:
- Process map: Mermaid end-to-end — 5-10 bước chính
- Swimlane: Vai trò × Bước — ai làm gì
- Chi tiết mỗi bước: Input | Action | Output | Tool | Time | Quality check
- Exception handling: 3-5 tình huống bất thường + cách xử lý
- KPI per process: 3-5 metrics + target + measurement method
- EOS style: "Documented, Simplified, Followed By All"

TONE: Operational, cụ thể, actionable.
LENGTH: 4-6 trang A4 per SOP (12-18 trang tổng).

CROSS-REFERENCE: Sử dụng SOP Template chuẩn (P-OPS-11) làm format.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
