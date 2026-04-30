# PROMPT 06: Checklist tuân thủ pháp lý (Legal Compliance Checklist)

#### Mô tả
Checklist định kỳ (tháng/quý/năm) giúp DN rà soát tuân thủ pháp lý. Bao gồm: thuế, lao động, bảo hiểm xã hội, PCCC, môi trường, báo cáo tài chính, và các nghĩa vụ pháp lý khác.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ngành nghề? (mỗi ngành có compliance riêng)
2. Quy mô nhân sự? (ảnh hưởng nghĩa vụ lao động, BHXH)
3. Có hoạt động XNK, ngoại hối không?
4. Đã bị thanh tra/phạt lần nào chưa? (xác định vùng rủi ro)
5. Ai sẽ chịu trách nhiệm check hàng tháng?

#### Template gợi ý
Cấu trúc FRM:
- **Phân theo tần suất**: Hàng tháng | Hàng quý | Hàng năm | Khi có sự kiện
- **Phân theo lĩnh vực**: Thuế | Lao động-BHXH | PCCC | Môi trường | Ngành đặc thù | Báo cáo tài chính
- **Mỗi mục**: # | Nghĩa vụ | Hạn chót | Cơ quan | Người phụ trách | Status ☐ | Ghi chú
- **Calendar view**: Timeline 12 tháng, highlight deadline
- **Penalty reference**: Mức phạt nếu vi phạm (răn đe)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Legal Compliance Checklist — checklist tuân thủ pháp lý định kỳ.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- XNK: [Có/Không] — Ngoại hối: [Có/Không]
- Compliance owner: [Chức danh]
- Vùng rủi ro đặc biệt: [liệt kê nếu có]

FORMAT:
- 4 bảng theo tần suất: Monthly / Quarterly / Annually / Event-driven
- Mỗi bảng: # | Nghĩa vụ | Deadline | Cơ quan quản lý | Owner | Done ☐ | Mức phạt nếu vi phạm
- Calendar heatmap: 12 tháng × deadline intensity
- Traffic light status: 🟢 Done | 🟡 Upcoming (<30 ngày) | 🔴 Overdue
- Tổng kết: __/__ mục đã hoàn thành tháng này

TONE: Compliance — nghiêm túc, cảnh báo rủi ro.
LENGTH: 5-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
