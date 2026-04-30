# P-FIN-14: Bảng theo dõi công nợ (AR/AP Tracking Sheet)

#### Mô tả
Template bảng theo dõi công nợ phải thu (AR) và phải trả (AP) — dạng aging report. Theo dõi từng khách hàng/nhà cung cấp, phân loại theo tuổi nợ, alert overdue.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Cần track AR, AP, hay cả hai?
2. Phần mềm kế toán có sẵn báo cáo công nợ không? (supplement hay thay thế?)
3. Aging buckets muốn phân: 30/60/90/120+ hay custom?
4. Cần thêm cột nào? (VD: người phụ trách, hạn mức tín dụng, ghi chú follow-up)
5. Tần suất cập nhật? (daily / weekly / monthly)

#### Template gợi ý
Cấu trúc FRM:
- **AR Aging Report**: KH | Tổng nợ | Current | 1-30 | 31-60 | 61-90 | >90 | Hạn mức | Status | PIC | Next action
- **AP Aging Report**: NCC | Tổng nợ | Current | 1-30 | 31-60 | 61-90 | >90 | Due date | Priority | PIC
- **Summary Dashboard**: Total AR | Total AP | Net | Overdue % | DSO | DPO
- **Alert Rules**: Màu sắc + hành động per aging bucket
- **Follow-up Log**: KH/NCC | Date | Action | Result | Next step

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Bảng theo dõi công nợ (AR/AP Tracking Sheet).

CONTEXT:
- DN: [Tên] — Track: [AR / AP / Both]
- Số KH: [số] — Số NCC: [số]
- Aging buckets: [30/60/90/120+ hoặc custom]
- Cập nhật: [daily / weekly / monthly]
- Supplement phần mềm: [Có/Không]

FORMAT:
- AR table: 12+ cột, sort by overdue desc
- AP table: 12+ cột, sort by due date asc
- Color coding: 🟢 Current | 🟡 1-30 | 🟠 31-60 | 🔴 61-90 | ⚫ >90
- Summary KPIs: Total AR | Total AP | DSO | DPO | Overdue ratio
- Follow-up log template: Bảng tracking hành động thu nợ
- Top 10 Overdue: Highlight KH/NCC nợ lớn nhất
- Trend: MoM comparison data

TONE: Operational, tracking-focused.
LENGTH: 3-5 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
