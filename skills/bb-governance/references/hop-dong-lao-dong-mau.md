# PROMPT 12: Hợp đồng lao động mẫu (Employment Contract Template)

#### Mô tả
Template hợp đồng lao động chuẩn theo Bộ luật Lao động 2019 (có hiệu lực từ 01/01/2021). Bao gồm 3 loại: thử việc, xác định thời hạn, không xác định thời hạn. Customize theo ngành và quy mô DN.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hợp đồng cần tạo? (Thử việc / Xác định / Không xác định / Tất cả)
2. Ngành nghề? (ảnh hưởng điều kiện lao động đặc thù)
3. Có chế độ bổ sung ngoài luật không? (VD: bảo hiểm sức khỏe private, thưởng cổ phiếu, remote working)
4. Có điều khoản non-compete sau khi nghỉ việc không?
5. Thang lương, bảng lương đã có chưa?

#### Template gợi ý
Cấu trúc FRM (mỗi loại HĐ):
- **Điều 1** — Thông tin các bên: Người sử dụng LĐ + Người LĐ
- **Điều 2** — Loại HĐ, thời hạn, ngày bắt đầu
- **Điều 3** — Công việc, địa điểm, chức danh
- **Điều 4** — Lương, phụ cấp, thưởng, hình thức trả, kỳ trả
- **Điều 5** — Thời giờ làm việc, nghỉ ngơi, nghỉ phép
- **Điều 6** — BHXH, BHYT, BH thất nghiệp, chế độ bổ sung
- **Điều 7** — Đào tạo, nâng bậc
- **Điều 8** — Bảo mật, sở hữu trí tuệ, non-compete
- **Điều 9** — Chấm dứt HĐ, thời hạn báo trước
- **Điều 10** — Kỷ luật lao động
- **Điều 11** — Giải quyết tranh chấp
- **Phần ký**: 2 bên, mỗi bên giữ 1 bản

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template hợp đồng lao động (Employment Contract).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Quy mô: [số nhân sự]
- Loại HĐ: [Thử việc / Xác định / Không xác định / Tất cả 3 loại]
- Chế độ bổ sung: [liệt kê]
- Non-compete: [Có/Không] — Thời hạn: [tháng]
- Cơ sở pháp lý: BLLĐ 2019 (45/2019/QH14), NĐ 145/2020/NĐ-CP

FORMAT:
- Template form: Trường điền = [___], lựa chọn = ☐
- 3 version riêng biệt: Thử việc / Xác định / Không xác định
- Bảng tham chiếu: Điều khoản → Điều luật tương ứng BLLĐ
- Phụ lục: Job Description template, Bảng phụ cấp, NDA nhân sự
- Lưu ý highlight: Những điều khoản CẦN customize theo DN (không dùng y nguyên template)

TONE: Pháp lý, chuẩn mực, dễ điền.
LENGTH: 5-7 trang A4 mỗi loại.

LƯU Ý: Template tham khảo — CẦN rà soát pháp lý trước khi sử dụng.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
