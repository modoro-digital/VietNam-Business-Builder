### PROMPT 12: Sales Pipeline Tracker (Template theo dõi pipeline)

#### Mô tả
Template theo dõi pipeline bán hàng — tracking từng deal qua các stage, giá trị, xác suất chốt, dự báo doanh thu, và conversion rates. Là công cụ quản lý hàng ngày của Sales Manager và báo cáo tuần cho lãnh đạo.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Các stage trong pipeline? (VD: Lead → Qualified → Proposal → Negotiation → Closed Won/Lost)
2. Probability mặc định mỗi stage? (VD: Lead 10%, Qualified 25%, Proposal 50%...)
3. Giá trị deal trung bình?
4. Số deals trung bình trong pipeline?
5. Tần suất review pipeline? (daily / weekly)
6. Cần forecast không? (monthly / quarterly / annual)
7. Tracking theo rep / team / kênh?

#### Template gợi ý
Cấu trúc FRM:
- **Pipeline View**: Deal | Company | Contact | Value | Stage | Probability | Weighted | Age | Next Action | Owner | Close Date
- **Stage Summary**: Bảng Stage | # Deals | Total Value | Weighted Value | Avg Age | Conversion %
- **Forecast View**: Monthly / Quarterly — Commit | Upside | Pipeline | Target | Gap
- **Rep Scorecard**: Per rep — Pipeline value | # Deals | Win rate | Avg deal size | Activity metrics
- **Conversion Funnel**: Stage-to-stage conversion + trend
- **Stale Deals Alert**: Deals > X ngày không chuyển stage
- **Weekly Review Template**: Agenda + dashboard + action items

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sales Pipeline Tracker.

CONTEXT:
- DN: [Tên] — Stages: [liệt kê + probability %]
- Avg deal size: [số] — Avg deals in pipeline: [số]
- Sales cycle: [ngày] — Review: [daily / weekly]
- Team size: [số rep] — Tracking: [per rep / team / kênh]
- Forecast: [monthly / quarterly / annual]

FORMAT:
- Pipeline table: 12+ cột — Deal | Company | Value | Stage | Prob | Weighted | Age | Next Action | Owner | Close Date | Source | Notes
- Stage summary: Bảng Stage | # Deals | $ Value | $ Weighted | Avg Age | Conv % → chart data
- Forecast: Bảng Month | Commit | Best Case | Pipeline | Target | Gap | Gap %
- Rep scorecard: Bảng Rep | Pipeline $ | # Deals | Win Rate | Avg Deal | Activities | Quota %
- Conversion waterfall: Lead → MQL → SQL → Proposal → Won — % each step
- Stale alert: Rules — IF stage_age > [X days] THEN flag 🔴
- Weekly review template: 5 sections — Wins | Lost | Moved | Stuck | Actions

TONE: Operational — tracking, analytical, action-oriented.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
