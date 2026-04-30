# P-PPL-08: Chính sách nghỉ phép (Leave Policy)

#### Mô tả
Chính sách quy định chi tiết các loại nghỉ phép — phép năm, ốm đau, thai sản, hiếu hỷ, nghỉ không lương, nghỉ bù. Tuân thủ BLLĐ 2019, đồng thời có thể quy định bổ sung thuận lợi hơn cho NV.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phép năm: 12 ngày (luật) hay nhiều hơn? Có tăng theo thâm niên?
2. Nghỉ ốm: Có cần giấy BS từ ngày thứ mấy?
3. Thai sản: Theo luật (6 tháng) hay có bổ sung?
4. Hiếu hỷ: Mấy ngày mỗi trường hợp? (luật: tang 3 ngày, cưới 3 ngày)
5. Nghỉ không lương: Max bao nhiêu ngày? Điều kiện?
6. Quy trình xin phép: App / Email / Giấy? Cần duyệt trước bao lâu?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Phép năm: Số ngày, tích lũy, cách tính, chuyển phép, mua phép
- **Phần 2** — Nghỉ ốm đau: Chế độ BHXH, giấy tờ cần, số ngày tối đa
- **Phần 3** — Thai sản: Quyền lợi nữ + nam (nghỉ chăm vợ), trước/sau sinh
- **Phần 4** — Hiếu hỷ: Tang, cưới, con cái — số ngày + chế độ
- **Phần 5** — Nghỉ không lương: Điều kiện, giới hạn, ảnh hưởng BHXH
- **Phần 6** — Nghỉ bù, nghỉ lễ: Lịch nghỉ lễ quốc gia, quy tắc nghỉ bù
- **Phần 7** — Quy trình xin phép: Flowchart + timeline báo trước
- **Phụ lục**: Bảng tổng hợp loại nghỉ, Form đơn xin phép

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách nghỉ phép (Leave Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- Phép năm: [số ngày] — Tăng thâm niên: [Có/Không]
- Ốm đau: Giấy BS từ ngày thứ [số]
- Nghỉ không lương max: [số ngày]
- Quy trình: [App / Email / Giấy] — Báo trước: [số ngày]
- Cơ sở pháp lý: BLLĐ 2019 (Điều 113-116), Luật BHXH 2014

FORMAT:
- Bảng tổng hợp 1 trang: Loại nghỉ | Số ngày | Có lương | Chứng từ | Báo trước | Duyệt bởi
- Phép năm calculator: Tháng vào làm → số ngày phép năm đầu tiên (pro-rata)
- Flowchart xin phép: NV submit → Manager duyệt → HR ghi nhận → Trừ phép
- Nghỉ ốm/thai sản: Bảng quyền lợi BHXH chi tiết + quy trình claim
- Calendar lễ: 11 ngày nghỉ lễ quốc gia + quy tắc hoán đổi khi trùng T7/CN
- FAQ: 10 câu phổ biến — "Phép chưa dùng hết có mất?", "Nghỉ không lương ảnh hưởng BHXH?"

TONE: Rõ ràng, công bằng, reference pháp lý cụ thể.
LENGTH: 5-7 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
