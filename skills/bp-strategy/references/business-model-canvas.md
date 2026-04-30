# PROMPT 06: Business Model Canvas (BMC)

#### Mô tả
Mô hình kinh doanh theo 9 khối Osterwalder: Customer Segments, Value Propositions, Channels, Customer Relationships, Revenue Streams, Key Resources, Key Activities, Key Partnerships, Cost Structure. Cái nhìn 1-trang về cách DN tạo ra, cung cấp, và thu giá trị.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN có bao nhiêu dòng sản phẩm/dịch vụ chính? (mỗi dòng có thể cần BMC riêng)
2. Khách hàng chính là ai? (B2B/B2C/B2B2C, segments)
3. Giá trị cốt lõi DN mang lại cho khách hàng? (giải quyết vấn đề gì?)
4. Kênh bán hàng/phân phối hiện tại?
5. Nguồn doanh thu: bán hàng, subscription, commission, licensing...?
6. Chi phí lớn nhất: nhân sự, COGS, marketing, công nghệ...?
7. Đối tác chiến lược hiện tại?

#### Template gợi ý
Cấu trúc FRM:
- **Canvas 1 trang** — Bảng 9 khối layout chuẩn Osterwalder
- **Chi tiết từng khối** — Mỗi khối 1/2-1 trang mở rộng:
  - Current state (hiện tại)
  - Desired state (mong muốn)
  - Gap & Actions (cần làm gì để đạt)
- **Revenue Model detail** — Bảng: Revenue stream | % tổng DT | Pricing model | Unit economics
- **Cost Structure detail** — Fixed vs Variable, % breakdown
- **Assumptions & Risks** — Giả định nào cần validate?

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Business Model Canvas (BMC).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Sản phẩm/Dịch vụ: [liệt kê dòng chính]
- Khách hàng: [segments]
- Value Proposition: [giá trị cốt lõi]
- Channels: [kênh hiện tại]
- Revenue: [nguồn + tỷ lệ]
- Cost: [chi phí lớn nhất]
- Partners: [đối tác chính]

FORMAT:
- Canvas 1-page: Bảng 9 khối, mỗi khối 3-5 bullet points ngắn gọn
- Deep-dive: 9 sections mở rộng, mỗi section có Current/Desired/Gap
- Revenue model: Bảng stream × pricing × unit economics
- Key Metrics per block: VD: Customer Segments → TAM/SAM/SOM, Revenue → MRR/ARPU/LTV
- Validation checklist: Giả định nào ĐÃ validate? Giả định nào CẦN test?

TONE: Strategic, concise, visual.
LENGTH: 5-8 trang A4 (1 trang canvas + 7 trang detail).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
