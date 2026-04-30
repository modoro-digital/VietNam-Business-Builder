<p align="center">
  <a href="https://modoro.com.vn">
    <img src="https://modoro.com.vn/wp-content/uploads/2023/02/logo-modoro-corp-300x56.png" alt="MODORO Technology Corporation" width="240">
  </a>
</p>

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

### Cách 3 — Kéo thả file `.plugin`

1. [Tải file `business-builder.plugin`](https://github.com/modoro-digital/VietNam-Business-Builder/raw/main/business-builder.plugin) về máy.
2. Mở **Claude Cowork** hoặc **Claude Code**.
3. Kéo thả file `business-builder.plugin` vào cửa sổ Claude.
4. Xác nhận cài đặt khi được hỏi.

Sau khi cài, restart Claude Code và kiểm tra với `/plugin` — sẽ thấy 13 skills `bb-*` xuất hiện.

---

## Cấu trúc 13 Skills

| # | Skill | Tầng | Files | Mô tả |
|---|-------|------|-------|-------|
| 0 | `bb-orchestrator` | Meta | 10 | Điều phối tổng thể, gọi tuần tự 12 skill con |
| 1 | `bb-governance` | 1 | 20 | Quản trị công ty & Pháp lý |
| 2 | `bb-strategy` | 1 | 19 | Chiến lược & Kế hoạch kinh doanh |
| 3 | `bb-finance` | 2 | 21 | Tài chính & Kế toán |
| 4 | `bb-people` | 2 | 23 | Nhân sự & Con người |
| 5 | `bb-operations` | 2 | 21 | Hành chính & Vận hành |
| 6 | `bb-sales` | 3 | 18 | Kinh doanh & Bán hàng |
| 7 | `bb-marketing` | 3 | 11 | Marketing & Thương hiệu |
| 8 | `bb-customer` | 3 | 13 | Khách hàng & Dịch vụ |
| 9 | `bb-product-tech` | 4 | 14 | Sản phẩm & Công nghệ |
| 10 | `bb-training` | 4 | 11 | Đào tạo & Phát triển |
| 11 | `bb-reporting` | 4 | 11 | Báo cáo & Đo lường |
| 12 | `bb-growth` | 5 | 13 | Tăng trưởng & Đầu tư |

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

## Tác giả

<img src="https://lebaoquoc.com/wp-content/uploads/2023/03/profile-quoc.png" alt="Quốc MODORO" width="160" align="right" style="border-radius:8px; margin-left:16px;">

**Lê Bảo Quốc — Quốc MODORO**
CEO & Founder, MODORO Technology Corporation

Chuyên gia **3A Marketing** (Affiliate · AI · Automation) với hơn 10 năm xây dựng hệ thống doanh nghiệp tự động. Sáng lập Ybai — nền tảng marketing all-in-one đã triển khai cho 2.000+ doanh nghiệp và 100.000+ cộng tác viên tại Việt Nam và Úc.

- **Bio link:** [bio.ybai.me/777777](https://bio.ybai.me/777777)
- **Website:** [lebaoquoc.com](https://lebaoquoc.com) · [9bizclaw.com](https://www.9bizclaw.com) · [modoro.com.vn](https://modoro.com.vn) · [ybai.vn](https://ybai.vn) · [pdca.me](https://pdca.me)

---

## Tài liệu hướng dẫn

- **Hướng dẫn sử dụng chi tiết (PDF):** [Xem tại Google Drive](https://drive.google.com/file/d/12jpfVJrzjJPJGLgMOvHuLHPKfXRK77_-/view?usp=sharing)
- **Tài liệu kiến trúc:** [BLUEPRINT.md](BLUEPRINT.md)
- **Hướng dẫn plugin:** [README-plugin.md](README-plugin.md)

---

## 💬 Cộng đồng 3A SYSTEM — HỆ THỐNG KINH DOANH 1 NGƯỜI

Tham gia nhóm Zalo để học hỏi, chia sẻ và nhận hỗ trợ từ cộng đồng doanh nhân ứng dụng AI vào vận hành doanh nghiệp.

<p align="center">
  <a href="https://zalo.me/g/fbhqms222"><strong>👥 Tham gia nhóm Zalo ngay</strong></a>
</p>

---

## 🎁 QUÀ TẶNG ĐẶC BIỆT

<p align="center">
  <a href="https://ybai.co/s13f1d7482">
    <img src="https://w.ladicdn.com/s700x700/613b06ad7d0d9c0012053ddf/modoro-tl-ai-20260407073950-txhp4.png" alt="Workshop Làm chủ trợ lý AI OpenClaw" width="600">
  </a>
</p>

Bạn vẫn đang tự xử lý mọi việc mỗi ngày… trong khi người khác đã có AI làm thay phần lớn?

Còn bạn thì sao? Inbox vẫn đầy, công việc vẫn phải tự theo dõi, deadline vẫn tự nhớ… ngày nào cũng quá tải.

Mình từng như vậy: có dùng AI, nhưng không biết cài OpenClaw, không hiểu cách vận hành, càng làm càng rối.

Cho đến khi nhận ra: **Vấn đề không phải thiếu công cụ, mà là chưa có hệ thống để AI làm việc cho mình.**

Workshop **"Làm chủ trợ lý AI OpenClaw"** cho mình cách đi từ cài đặt, kết nối, tự động hoá công việc thực tế.

Từ email, giao việc, nhắc lịch đến workflow… mọi thứ gọn và nhanh hơn hẳn.

Nếu bạn vẫn đang làm thủ công hoặc dùng AI rời rạc, thì có thể bạn đang chậm hơn người khác rất nhiều rồi.

<p align="center">
  <a href="https://ybai.co/s13f1d7482"><strong>👉 Đăng ký tại đây</strong></a>
</p>

---

## License

[MIT License](LICENSE) © 2026 MODORO Technology Corporation — Quốc MODORO.

> Tự do sử dụng, sửa đổi, phân phối — kể cả mục đích thương mại. Yêu cầu giữ nguyên copyright notice.
