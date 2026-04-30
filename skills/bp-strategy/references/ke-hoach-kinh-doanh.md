# PROMPT 10: Business Plan (Kế hoạch kinh doanh)

#### Mô tả
Kế hoạch kinh doanh tổng thể — tài liệu chiến lược quan trọng nhất, tổng hợp mọi khía cạnh: thị trường, sản phẩm, marketing, vận hành, tài chính, nhân sự. Dùng cho quản lý nội bộ, gọi vốn, vay ngân hàng.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mục đích chính: nội bộ / gọi vốn / vay ngân hàng / đối tác?
2. Time horizon: 1 năm / 3 năm / 5 năm?
3. Tổng quan thị trường: TAM/SAM/SOM (ước lượng)?
4. Financial projections: có sẵn hay cần tạo?
5. Go-to-market strategy đã có chưa?
6. Đã có data nào từ các file trước? (SWOT, BMC, ICP, Competitive)

#### Template gợi ý
Cấu trúc MAN (20-40 trang):
- **Executive Summary** — 2 trang, BLUF, standalone readable
- **Company Overview** — Tham chiếu Company Profile
- **Market Analysis** — TAM/SAM/SOM, trends, customer segments
- **Products & Services** — Mô tả, roadmap, USP
- **Competitive Analysis** — Tham chiếu Competitive Landscape
- **Marketing & Sales Strategy** — Go-to-market, pricing, channels, customer acquisition
- **Operations Plan** — Quy trình, supply chain, technology
- **Management Team** — Key people, org chart, hiring plan
- **Financial Plan** — P&L 3-5 năm, Cash flow, Break-even, Funding requirements
- **Risk Analysis** — Top 5 risks + mitigation
- **Milestones & Timeline** — Key milestones, Gantt chart
- **Appendix** — Financial models detail, market research data, CV key people

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Business Plan.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Stage: [startup/growth/mature]
- Mục đích: [nội bộ / gọi vốn / vay / đối tác]
- Time horizon: [1/3/5 năm]
- Market: TAM [số] | SAM [số] | SOM [số]
- Financial data: [có sẵn / cần tạo projection]
- Data từ files trước: [liệt kê files đã tạo trong 02-bp-strategy]

FORMAT:
- Executive Summary: 2 trang, standalone, highlight key numbers
- Each section: Key insight → Supporting data → Implications → Actions
- Financial tables: P&L, Cash Flow, Balance Sheet — 3 scenarios (Base/Optimistic/Conservative)
- Visuals: Market size pie chart, Growth projection line chart, Org chart, Timeline Gantt
- Tham chiếu cross-reference: Link đến files chi tiết (SWOT, BMC, ICP, Competitive)
- Appendix: Detailed financial model assumptions

TONE: Professional, persuasive (nếu gọi vốn), evidence-based.
LENGTH: 20-40 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
