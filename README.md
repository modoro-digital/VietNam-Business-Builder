# Business Builder — Plugin Đóng Gói Doanh Nghiệp

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-0.3.0-blue.svg)](CHANGELOG.md)
[![Plugin Type](https://img.shields.io/badge/Claude-Plugin-orange.svg)](.claude-plugin/plugin.json)
[![Made in](https://img.shields.io/badge/Made%20in-Vietnam-red.svg)](https://modoro.com.vn)

> **Đóng gói doanh nghiệp tự động** — Plugin AI cho Claude Code/Cowork tự sinh **191 tài liệu vận hành** chuẩn hóa cho doanh nghiệp Việt Nam, theo kiến trúc 5 tầng (ISO 9001, EOS, McKinsey 7S, SYSTEMology) và tuân thủ pháp luật Việt Nam.

---

## Mô tả

Bộ **13 skills** AI tự động hóa việc đóng gói doanh nghiệp:
- **Input:** Thông tin chủ DN qua prompt (ngành nghề, quy mô, mục tiêu...).
- **Output:** Bộ **191 tài liệu vận hành** hoàn chỉnh trong cây thư mục có hướng dẫn — từ điều lệ, OKR, JD, SOP, quy trình, KPI, đến pitch deck và financial model.

Phù hợp cho: **chủ DN SME**, **business coach**, **consultant**, **CEO startup** muốn hệ thống hóa doanh nghiệp một cách bài bản trong vài ngày thay vì vài tháng.

---

## Cài đặt

### Cách 1 — Clone từ GitHub
```bash
git clone https://github.com/modoro-digital/VietNam-Business-Builder.git
cp -r VietNam-Business-Builder ~/.claude/plugins/business-builder
```

### Cách 2 — Cài qua Claude Code (khi marketplace ra mắt)
```
/plugin install modoro-digital/VietNam-Business-Builder
```

Sau khi cài, restart Claude Code và kiểm tra với `/plugin` — sẽ thấy 13 skills `bp-*` xuất hiện.

---

## Cấu trúc 13 Skills

| # | Skill | Tầng | Files | Mô tả |
|---|-------|------|-------|-------|
| 0 | `bp-orchestrator` | Meta | 10 | Điều phối tổng thể, gọi tuần tự 12 skill con |
| 1 | `bp-governance` | 1 | 20 | Quản trị công ty & Pháp lý |
| 2 | `bp-strategy` | 1 | 19 | Chiến lược & Kế hoạch kinh doanh |
| 3 | `bp-finance` | 2 | 21 | Tài chính & Kế toán |
| 4 | `bp-people` | 2 | 23 | Nhân sự & Con người |
| 5 | `bp-operations` | 2 | 21 | Hành chính & Vận hành |
| 6 | `bp-sales` | 3 | 18 | Kinh doanh & Bán hàng |
| 7 | `bp-marketing` | 3 | 11 | Marketing & Thương hiệu |
| 8 | `bp-customer` | 3 | 13 | Khách hàng & Dịch vụ |
| 9 | `bp-product-tech` | 4 | 14 | Sản phẩm & Công nghệ |
| 10 | `bp-training` | 4 | 11 | Đào tạo & Phát triển |
| 11 | `bp-reporting` | 4 | 11 | Báo cáo & Đo lường |
| 12 | `bp-growth` | 5 | 13 | Tăng trưởng & Đầu tư |

**Tổng: 205 file Markdown · 191 prompt files · 13 skills · 5 tầng kiến trúc**

---

## Kiến trúc 5 tầng

```
┌─────────────────────────────────────────────────────────────┐
│  Tầng Meta:  ORCHESTRATOR — Bộ não điều phối                │
├─────────────────────────────────────────────────────────────┤
│  Tầng 1:  NỀN MÓNG — Governance + Strategy                  │
│  Tầng 2:  BỘ MÁY — Finance + People + Operations            │
│  Tầng 3:  ĐỘNG CƠ — Sales + Marketing + Customer            │
│  Tầng 4:  TỐI ƯU — Product-Tech + Training + Reporting      │
│  Tầng 5:  NHÂN RỘNG — Growth                                │
└─────────────────────────────────────────────────────────────┘
```

Chi tiết kiến trúc xem [BLUEPRINT.md](BLUEPRINT.md).

---

## Trigger phrases

**Trigger chính (gọi orchestrator):**
- "đóng gói doanh nghiệp"
- "hệ thống hóa DN"
- "tạo bộ tài liệu vận hành"

**Trigger từng skill:** xem bảng trigger phrases trong [README-plugin.md](README-plugin.md).

---

## Build Order khuyến nghị

1. **Phase 1 (Foundation):** `orchestrator` → `governance` → `strategy`
2. **Phase 2 (Core Ops):** `finance` → `people` → `operations`
3. **Phase 3 (Revenue):** `sales` → `marketing` → `customer`
4. **Phase 4 (Systems & Scale):** `product-tech` → `training` → `reporting` → `growth`

---

## Frameworks & Standards tham chiếu

**Quản trị & Vận hành:**
- ISO 9001:2015 — Hệ thống quản lý chất lượng
- EOS / Traction — Entrepreneurial Operating System
- E-Myth Revisited — Michael Gerber
- McKinsey 7S Framework
- SYSTEMology — David Jenyns
- Franchise Operations Manual Standards

**Tuân thủ pháp luật Việt Nam:**
- Luật Doanh nghiệp 2020
- Bộ luật Lao động 2019
- Luật Kế toán 2015

---

## Đóng góp

Plugin này được duy trì bởi **MODORO Technology Corporation**. Mọi đóng góp đều được hoan nghênh:

- **Báo lỗi / Đề xuất:** [Open an Issue](https://github.com/modoro-digital/VietNam-Business-Builder/issues)
- **Cải tiến / PR:** Fork repo và gửi Pull Request
- **Thảo luận:** [GitHub Discussions](https://github.com/modoro-digital/VietNam-Business-Builder/discussions)

---

## Liên hệ

- **Tác giả:** Quốc MODORO (Lê Bảo Quốc) — CEO & Founder, MODORO Technology Corporation
- **Bio link:** [bio.ybai.me/777777](https://bio.ybai.me/777777)
- **Website:** [modoro.com.vn](https://modoro.com.vn) · [ybai.vn](https://ybai.vn) · [pdca.me](https://pdca.me)

---

## License

[MIT License](LICENSE) © 2026 MODORO Technology Corporation — Quốc MODORO.

> Tự do sử dụng, sửa đổi, phân phối — kể cả mục đích thương mại. Yêu cầu giữ nguyên copyright notice.
