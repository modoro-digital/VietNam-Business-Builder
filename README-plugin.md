# Business Builder Plugin

> **Đóng gói doanh nghiệp — AI tự động tạo 191 tài liệu vận hành cho doanh nghiệp từ bộ câu hỏi đầu vào**

**Tác giả:** Quốc MODORO  
**Phiên bản:** 0.3.0  
**Kích thước:** ~380KB · 207 files

---

## Tổng quan

Business Builder là plugin dành cho Claude, giúp doanh nghiệp Việt Nam **hệ thống hóa toàn bộ tài liệu vận hành** — từ pháp lý, chiến lược, tài chính, nhân sự, vận hành, kinh doanh, marketing, chăm sóc khách hàng, sản phẩm, đào tạo, báo cáo, đến tăng trưởng & đầu tư.

Hệ thống bao gồm **13 skill** được tổ chức theo **kiến trúc 5 tầng**, tạo ra **191 tài liệu chuẩn hóa** bao phủ mọi khía cạnh vận hành doanh nghiệp. Mọi tài liệu đều tuân thủ **quy tắc đặt tên và lưu trữ chuẩn hóa**.

## Kiến trúc 5 tầng

```
┌─────────────────────────────────────────┐
│  TẦNG 0: ORCHESTRATOR (Bộ não)          │
│  bp-orchestrator — Điều phối tổng thể   │
└──────────────────┬──────────────────────┘
                   │
┌──────────────────┴──────────────────────┐
│  TẦNG 1: NỀN MÓNG                       │
│  bp-governance (19 tài liệu)            │
│  bp-strategy (18 tài liệu)              │
└──────────────────┬──────────────────────┘
                   │
┌──────────────────┴──────────────────────┐
│  TẦNG 2: BỘ MÁY                         │
│  bp-finance (20) · bp-people (22)        │
│  bp-operations (20)                      │
└──────────────────┬──────────────────────┘
                   │
┌──────────────────┴──────────────────────┐
│  TẦNG 3: ĐỘNG CƠ                        │
│  bp-sales (17) · bp-marketing (10)       │
│  bp-customer (12)                        │
└──────────────────┬──────────────────────┘
                   │
┌──────────────────┴──────────────────────┐
│  TẦNG 4: TỐI ƯU                         │
│  bp-product-tech (13) · bp-training (10) │
│  bp-reporting (10)                       │
└──────────────────┬──────────────────────┘
                   │
┌──────────────────┴──────────────────────┐
│  TẦNG 5: NHÂN RỘNG                      │
│  bp-growth (12)                          │
└─────────────────────────────────────────┘
```

## 13 Skills

| # | Skill | Mô tả | Trigger phrases |
|---|-------|-------|-----------------|
| 0 | `bp-orchestrator` | Bộ điều phối tổng thể — thu thập thông tin, đánh giá scope, gọi 12 skill con | "đóng gói doanh nghiệp", "hệ thống hóa DN" |
| 1 | `bp-governance` | Quản trị & Pháp lý — điều lệ, quy chế, hợp đồng mẫu, tuân thủ | "tạo điều lệ", "đóng gói pháp lý" |
| 2 | `bp-strategy` | Chiến lược & Kế hoạch — SWOT, BMC, OKR, business plan, risk | "kế hoạch kinh doanh", "phân tích SWOT" |
| 3 | `bp-finance` | Tài chính & Kế toán — ngân sách, cashflow, SOP kế toán, BCTC | "ngân sách", "cashflow", "SOP kế toán" |
| 4 | `bp-people` | Nhân sự & Con người — org chart, JD, tuyển dụng, onboarding, KPI | "sơ đồ tổ chức", "sổ tay nhân viên" |
| 5 | `bp-operations` | Hành chính & Vận hành — SOP cốt lõi, NCC, kho, văn phòng | "tạo SOP", "sổ tay vận hành" |
| 6 | `bp-sales` | Kinh doanh & Bán hàng — quy trình bán hàng, pipeline, CRM, đại lý | "quy trình bán hàng", "kịch bản sales" |
| 7 | `bp-marketing` | Marketing & Thương hiệu — kế hoạch marketing, content, ads, SEO | "kế hoạch marketing", "content calendar" |
| 8 | `bp-customer` | Khách hàng & Dịch vụ — CX, xử lý khiếu nại, loyalty, referral | "chăm sóc khách hàng", "NPS survey" |
| 9 | `bp-product-tech` | Sản phẩm & Công nghệ — catalog, roadmap, tech stack, an ninh mạng | "roadmap sản phẩm", "chính sách IT" |
| 10 | `bp-training` | Đào tạo & Phát triển — training plan, mentoring, knowledge management | "kế hoạch đào tạo", "mentoring program" |
| 11 | `bp-reporting` | Báo cáo & Đo lường — KPI dictionary, dashboard, QBR, annual report | "từ điển KPI", "báo cáo quản trị" |
| 12 | `bp-growth` | Tăng trưởng & Đầu tư — pitch deck, franchise, exit strategy | "gọi vốn", "nhượng quyền", "pitch deck" |

## Cách sử dụng

### Đóng gói toàn bộ DN
Nói: **"Đóng gói doanh nghiệp"** hoặc **"Hệ thống hóa toàn bộ tài liệu DN"**  
→ `bp-orchestrator` sẽ thu thập thông tin và gọi tuần tự 12 skill con.

### Tạo tài liệu cụ thể
Nói: **"Tạo điều lệ công ty"**, **"Viết kế hoạch kinh doanh"**, **"Thiết kế dashboard KPI"**  
→ Skill tương ứng sẽ được kích hoạt.

### Quy trình mỗi skill
1. **Xác định** tài liệu cần tạo
2. **Thu thập** thông tin DN qua bộ câu hỏi trong prompt file
3. **Sinh tài liệu** theo template chuẩn hóa
4. **Review & tinh chỉnh** theo feedback

## Quy tắc lưu trữ

Mỗi tài liệu được tạo bởi plugin đều tuân thủ quy tắc đặt tên chuẩn:

```
[Thời gian] [Loại] - [Tên tài liệu] - [Phòng/Version]
```

**Mã thời gian:** `[STANDARD]` (cố định) · `[YYYY]` (theo năm) · `[YYYY-QX]` (theo quý) · `[YYYY-MM]` (theo tháng)

**Mã loại:** SOP (quy trình) · QC (quy chế) · KH (kế hoạch) · BC (báo cáo) · JD (mô tả CV) · HĐ (hợp đồng) · BB (biên bản) · TL (tài liệu)

Mỗi skill có bảng mapping cụ thể: tài liệu → thư mục Drive (00-09) → subfolder → tên file chuẩn. Chi tiết đầy đủ trong `skills/bp-orchestrator/references/quy-tac-luu-tru-drive.md`.

## Nền tảng lý thuyết

Plugin được xây dựng dựa trên các tiêu chuẩn BẮT BUỘC:

**Chuẩn quốc tế:**
- **ISO 9001:2015** — Hệ thống quản lý chất lượng, process approach
- **EOS/Traction** — Hệ thống vận hành doanh nghiệp 6 thành phần
- **E-Myth** — Xây dựng DN như franchise prototype, hệ thống không phụ thuộc cá nhân
- **McKinsey 7S** — Alignment 7 yếu tố tổ chức
- **SYSTEMology** — 4 bước hệ thống hóa: xác định → ghi nhận → tối ưu → chuyển giao
- **Franchise Ops Manual Standards** (IFA) — SOP chi tiết đến mức nhân viên mới làm đúng ngay lần đầu

**Pháp luật Việt Nam:**
- **Luật Doanh nghiệp 2020** (59/2020/QH14)
- **Bộ luật Lao động 2019** (45/2019/QH14)
- **Luật Kế toán 2015** (88/2015/QH13)

## Tác giả

**Quốc MODORO** — CEO & Founder, MODORO Technology Corporation  
Chuyên gia 3A Marketing (Affiliate, AI, Automation)  
Website: lebaoquoc.com · modoro.com.vn · ybai.vn  
Liên hệ hỗ trợ: https://bio.ybai.me/777777
