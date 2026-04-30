### PROMPT 04: SOP Quản lý kho (Warehouse/Inventory Management SOP)

#### Mô tả
Quy trình quản lý kho — nhập kho, xuất kho, kiểm kê, quản lý tồn kho min/max, FIFO/LIFO, xử lý hàng hỏng/hết hạn. Áp dụng cho cả kho hàng hóa và kho vật tư.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại kho? (hàng hóa / nguyên vật liệu / thành phẩm / hỗn hợp)
2. Phần mềm quản lý kho? (phần mềm kế toán tích hợp / WMS riêng / Excel)
3. Phương pháp tính giá xuất kho? (FIFO / Bình quân gia quyền / Đích danh)
4. Số lượng SKU? Có hàng hết hạn sử dụng không?
5. Tần suất kiểm kê? (hàng tháng / quý / năm)
6. Có nhiều kho / chi nhánh không?

#### Template gợi ý
Cấu trúc SOP:
- **Nhập kho**: Kiểm tra → Đối chiếu PO → Nhận hàng → Nhập phần mềm → Sắp xếp
- **Xuất kho**: Yêu cầu xuất → Duyệt → Lấy hàng (FIFO) → Giao → Cập nhật
- **Kiểm kê**: Lịch kiểm kê → Đếm → Đối chiếu → Xử lý chênh lệch → Báo cáo
- **Quản lý tồn kho**: Min/Max level, Reorder point, Safety stock
- **Hàng hỏng/hết hạn**: Phát hiện → Cách ly → Xử lý → Báo cáo
- **An toàn kho**: PCCC, sắp xếp, quy tắc vào ra

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quản lý kho (Warehouse Management).

CONTEXT:
- DN: [Tên] — Loại kho: [hàng hóa / NVL / thành phẩm]
- Phần mềm: [tên / Excel]
- Tính giá xuất: [FIFO / Bình quân / Đích danh]
- SKU: [số] — Hết hạn: [Có/Không]
- Kiểm kê: [tần suất]
- Đa kho: [Có/Không] — Số kho: [số]

FORMAT:
- Flowchart nhập kho: Mermaid — 6 bước + kiểm soát
- Flowchart xuất kho: Mermaid — 5 bước + FIFO highlight
- Checklist kiểm kê: Bảng SKU | Sổ sách | Thực đếm | Chênh lệch | Nguyên nhân
- Min/Max template: SKU | Min | Max | Reorder Point | Lead Time | Current Stock | Status
- Xử lý hàng hỏng: Decision tree — Hết hạn → Hỏng → Lỗi NCC → Action
- Phiếu nhập/xuất kho template: 2 mẫu chuẩn

TONE: SOP chuẩn, logistics-focused.
LENGTH: 6-8 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
