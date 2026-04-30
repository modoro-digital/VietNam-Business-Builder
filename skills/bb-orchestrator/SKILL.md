---
name: bb-orchestrator
description: >
  Bộ điều phối tổng thể quy trình Đóng Gói Doanh Nghiệp — thu thập thông tin, đánh giá scope,
  tạo cây thư mục chuẩn 200+ tài liệu, và gọi tuần tự 12 skill con. Use when the user asks to
  "đóng gói doanh nghiệp", "tạo bộ tài liệu vận hành", "business packaging", "hệ thống hóa doanh nghiệp",
  "xây dựng tài liệu từ A-Z", "tạo SOP toàn bộ", or needs a complete business documentation system.
metadata:
  version: "0.1.0"
  author: "Quốc MODORO"
---

# BP Orchestrator — Bộ Điều Phối Tổng Thể

## Vai trò

Skill này là **"bộ não trung tâm"** của toàn bộ hệ thống Đóng Gói Doanh Nghiệp. Không tạo tài liệu vận hành cụ thể — thay vào đó điều phối toàn bộ quy trình từ thu thập thông tin đến bàn giao.

## Kiến trúc 5 tầng

```
Tầng 0: ORCHESTRATOR (Brain/Meta) ← Skill này
Tầng 1: Nền Móng — 01-Governance, 02-Strategy
Tầng 2: Bộ Máy — 03-Finance, 04-People, 05-Operations
Tầng 3: Động Cơ — 06-Sales, 07-Marketing, 08-Customer
Tầng 4: Tối Ưu — 09-Product-Tech, 10-Training, 11-Reporting
Tầng 5: Nhân Rộng — 12-Growth
```

## Prompt files trong references/

| File | Mô tả |
|------|-------|
| `bo-cau-hoi-intake.md` | Bộ câu hỏi thu thập thông tin DN — 5 nhóm: cơ bản, giai đoạn, cấu trúc hiện tại, ưu tiên, đặc thù ngành |
| `danh-gia-scope.md` | Quy trình đánh giá scope & xác định tầng ưu tiên dựa trên maturity model |
| `cay-thu-muc-chuan.md` | Hướng dẫn tạo cây thư mục chuẩn — cấu trúc folder, naming convention |
| `luong-thuc-thi.md` | Luồng thực thi: trình tự gọi 12 skill con, dependency, trigger |
| `cham-diem-truong-thanh.md` | Maturity scoring — đánh giá mức độ trưởng thành DN qua 5 tầng |
| `checklist-chat-luong.md` | Checklist kiểm tra chất lượng toàn bộ output |
| `bang-thuat-ngu.md` | Bảng thuật ngữ chuẩn hóa toàn hệ thống |
| `bao-cao-ban-giao.md` | Template báo cáo bàn giao tổng kết |

## Quy trình sử dụng

### Bước 1: Thu thập thông tin
- Đọc file `${CLAUDE_PLUGIN_ROOT}/skills/bb-orchestrator/references/bo-cau-hoi-intake.md`
- Hỏi user lần lượt 5 nhóm câu hỏi: thông tin cơ bản DN, giai đoạn phát triển, cấu trúc hiện tại, ưu tiên, đặc thù ngành
- Ghi nhận tất cả câu trả lời làm **context chung** cho toàn bộ 12 skill

### Bước 2: Đánh giá scope & chấm điểm trưởng thành
- Đọc `${CLAUDE_PLUGIN_ROOT}/skills/bb-orchestrator/references/danh-gia-scope.md` và `cham-diem-truong-thanh.md`
- Xác định DN đang ở tầng nào, cần ưu tiên tầng nào
- Đề xuất scope (toàn bộ hay từng phần) và thứ tự thực hiện

### Bước 3: Tạo cây thư mục chuẩn
- Đọc `${CLAUDE_PLUGIN_ROOT}/skills/bb-orchestrator/references/cay-thu-muc-chuan.md`
- Tạo scaffold toàn bộ cấu trúc thư mục cho DN

### Bước 4: Gọi tuần tự 12 skill con
- Đọc `${CLAUDE_PLUGIN_ROOT}/skills/bb-orchestrator/references/luong-thuc-thi.md`
- Gọi skill theo thứ tự: 01 → 02 → 03 → 04 → 05 → 06 → 07 → 08 → 09 → 10 → 11 → 12
- Mỗi skill nhận context chung từ Bước 1 + output của skill trước

### Bước 5: Kiểm tra & bàn giao
- Đọc `${CLAUDE_PLUGIN_ROOT}/skills/bb-orchestrator/references/checklist-chat-luong.md`
- Verify completeness — đối chiếu output thực tế vs kỳ vọng
- Tạo báo cáo bàn giao theo `${CLAUDE_PLUGIN_ROOT}/skills/bb-orchestrator/references/bao-cao-ban-giao.md`

## Ma trận phân quyền

| Hành động | Orchestrator |
|-----------|:----------:|
| Đọc prompt files | ✅ |
| Hỏi user | ✅ |
| Tạo thư mục | ✅ |
| Gọi skill khác | ✅ |
| Tạo tài liệu vận hành | ❌ (delegate cho skill con) |
| Sửa output skill con | ❌ |

## Quy Tắc Lưu Trữ

> **BẮT BUỘC:** Mọi tài liệu tạo bởi Business Builder PHẢI tuân thủ quy tắc đặt tên và lưu trữ chuẩn hóa.

📋 **File tham chiếu đầy đủ:** `${CLAUDE_PLUGIN_ROOT}/skills/bb-orchestrator/references/quy-tac-luu-tru-drive.md`

### Quy trình sau khi tạo tài liệu

1. **Đặt tên file** theo format: `[Thời gian] [Loại] - [Tên tài liệu] - [Phòng/Version]`
2. **Xác định thư mục** đích theo mapping trong file tham chiếu
3. **Kiểm tra trùng** — nếu đã có file tương tự, cập nhật version (v1.0 → v1.1)
4. **Upload/lưu** file vào đúng subfolder vào đúng thư mục
5. **Cập nhật Hướng dẫn Sử dụng** nếu tạo subfolder mới hoặc thay đổi cấu trúc

### Mã loại tài liệu

| Mã | Loại | Mã | Loại |
|----|------|-----|------|
| **SOP** | Quy trình | **JD** | Mô tả công việc |
| **QC** | Quy chế/Chính sách | **BC** | Báo cáo |
| **KH** | Kế hoạch | **HĐ** | Hợp đồng |
| **BB** | Biên bản | **TL** | Tài liệu/Slide |

### Mã thời gian

| Ký hiệu | Dùng cho |
|----------|---------|
| `[STANDARD]` | Tài liệu cố định (SOP, JD, Quy chế) |
| `[YYYY]` | Tài liệu theo năm (KH, OKR, Ngân sách) |
| `[YYYY-QX]` | Tài liệu theo quý |
| `[YYYY-MM]` | Tài liệu theo tháng |


### Quy tắc định dạng output

Orchestrator điều phối 12 skill con. Mỗi skill con tuân thủ quy tắc output riêng (xem SKILL.md từng skill).

**Nguyên tắc chung:**
- Tài liệu văn bản (SOP, QC, MAN, POL) → tạo file **.docx**
- Bảng biểu, template số liệu, tracker (FRM có bảng tính) → tạo file **.xlsx**
- KHÔNG tạo file .md cho tài liệu chính thức

## Nền Tảng Tiêu Chuẩn

Mọi tài liệu tạo bởi hệ thống Business Builder PHẢI tuân thủ các chuẩn mực sau. Orchestrator chịu trách nhiệm đảm bảo **tất cả 12 skill con** đều align với nền tảng này:

**Chuẩn quốc tế:**
- **ISO 9001:2015** — Tiếp cận theo quy trình (process approach), thông tin được tài liệu hóa (documented information), tư duy dựa trên rủi ro (risk-based thinking) xuyên suốt mọi tầng
- **EOS/Traction** (Gino Wickman) — 6 thành phần: Vision, People, Data, Issues, Process, Traction — khung điều phối toàn bộ hệ thống đóng gói
- **E-Myth** (Michael Gerber) — Mọi tài liệu phải đạt chuẩn "franchise-ready" — ai cũng có thể vận hành mà không phụ thuộc cá nhân
- **McKinsey 7S** — Đảm bảo 7 yếu tố Strategy, Structure, Systems, Skills, Staff, Style, Shared Values được phản ánh đồng bộ qua 12 skill
- **SYSTEMology** (David Jenyns) — Quy trình hệ thống hóa: xác định → ghi nhận → tối ưu → chuyển giao — áp dụng khi xây dựng mọi SOP
- **Franchise Ops Manual Standards** (IFA) — Mỗi SOP phải đủ chi tiết để người mới có thể thực hiện mà không cần hướng dẫn thêm

