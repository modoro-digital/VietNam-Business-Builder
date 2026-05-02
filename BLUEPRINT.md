# BLUEPRINT: BỘ SKILL "ĐÓNG GÓI DOANH NGHIỆP"
## Business Packaging System — About Me Project

**Version:** 1.3 | **Date:** 2026-04-30 | **Author:** MODORO × Claude

---

## MỤC LỤC

- [I. Tổng Quan](#i-tổng-quan)
- [II. Kiến Trúc 5 Tầng](#ii-kiến-trúc-5-tầng)
- [III. Cây Thư Mục & Danh Mục Tài Liệu](#iii-cây-thư-mục--danh-mục-tài-liệu)
- [IV. Tổng Hợp Thống Kê](#iv-tổng-hợp-thống-kê)
- [V. Kiến Trúc Skill Set](#v-kiến-trúc-skill-set)
- [VI. Flow Vận Hành](#vi-flow-vận-hành)
- [VII. Thứ Tự Build](#vii-thứ-tự-build)
- [VIII. Prompts Chi Tiết](#viii-prompts-chi-tiết)
  - [VIII.1 — bb-orchestrator](#viii1--bb-orchestrator-điều-phối-tổng-thể)
  - [VIII.2 — bb-governance](#viii2--bb-governance-quản-trị--pháp-lý)
  - [VIII.3 — bb-strategy](#viii3--bb-strategy-chiến-lược--kế-hoạch)
  - [VIII.4 — bb-finance](#viii4--bb-finance-tài-chính--kế-toán)
  - [VIII.5 — bb-people](#viii5--bb-people-nhân-sự--con-người)
  - [VIII.6 — bb-operations](#viii6--bb-operations-hành-chính--vận-hành)
  - [VIII.7 — bb-sales](#viii7--bb-sales-kinh-doanh--bán-hàng)
  - [VIII.8 — bb-marketing](#viii8--bb-marketing-marketing--thương-hiệu)
  - [VIII.9 — bb-customer](#viii9--bb-customer-khách-hàng--dịch-vụ)
  - [VIII.10–VIII.13 — Placeholder](#viii10viii13--placeholder-cho-các-phase-sau)
- [IX. Nguồn Tham Khảo](#ix-nguồn-tham-khảo)

---

## I. TỔNG QUAN

### Mục tiêu

Xây dựng bộ skill AI tự động hóa việc "đóng gói doanh nghiệp" — biến thông tin thô từ chủ DN thành bộ tài liệu vận hành hoàn chỉnh, chuyên nghiệp, sẵn sàng triển khai.

### Đối tượng sử dụng

- Chủ doanh nghiệp SME (2–100 nhân sự)
- Doanh thu 500 triệu – 50 tỷ/năm
- Đang cần hệ thống hóa nhưng không có thời gian/nguồn lực tự làm

### Nguyên lý thiết kế

> **BẮT BUỘC:** Mọi tài liệu tạo bởi Business Builder PHẢI tuân thủ đồng thời cả hai nhóm chuẩn dưới đây. Không có ngoại lệ.

**A. Chuẩn quốc tế (Framework & Methodology):**

| # | Chuẩn | Vai trò trong hệ thống |
|---|-------|----------------------|
| 1 | **ISO 9001:2015** | Hệ thống tài liệu 4 tầng (Policy → Manual → Procedure → Record), Process Approach, tư duy dựa trên rủi ro |
| 2 | **EOS / Traction** (Gino Wickman) | 6 thành phần: Vision, People, Data, Issues, Process, Traction — quyết định build order |
| 3 | **E-Myth Revisited** (Michael Gerber) | Turnkey franchise model — "Work ON not IN your business", franchise-ready mindset |
| 4 | **McKinsey 7S Framework** | Alignment 7 yếu tố: Strategy, Structure, Systems, Skills, Staff, Style, Shared Values |
| 5 | **SYSTEMology** (David Jenyns) | Phương pháp hệ thống hóa quy trình: xác định → ghi nhận → tối ưu → chuyển giao |
| 6 | **Franchise Ops Manual Standards** (IFA) | Chuẩn tài liệu vận hành nhượng quyền quốc tế — đảm bảo mọi SOP đủ chi tiết để người mới follow |

**B. Pháp luật Việt Nam (Tuân thủ bắt buộc):**

| # | Văn bản | Phạm vi áp dụng |
|---|---------|-----------------|
| 1 | **Luật Doanh nghiệp 2020** (59/2020/QH14) | Governance — điều lệ, ĐKKD, quy chế quản trị, cơ cấu tổ chức |
| 2 | **Bộ luật Lao động 2019** (45/2019/QH14) | People — hợp đồng lao động, nội quy, chính sách nghỉ phép, kỷ luật |
| 3 | **Luật Kế toán 2015** (88/2015/QH13) | Finance — SOP kế toán, BCTC, chế độ kế toán (TT200/TT133) |

**Nguyên tắc thiết kế:**

1. Function-based, không phải department-based
2. Progressive disclosure — Từ nền tảng → nâng cao
3. Actionable documents — Mỗi tài liệu phải dùng được ngay
4. Franchise-ready mindset — Mọi SOP đủ chi tiết để nhân bản
5. Dual compliance — Đạt chuẩn quốc tế + tuân thủ pháp luật VN đồng thời

---

## II. KIẾN TRÚC 5 TẦNG

```
  ┌─────────────────────────────────────────────┐
  │  Tầng 5: TĂNG TRƯỞNG (Growth)              │
  │  Investor-ready, M&A, nhượng quyền          │
  │  [12-bb-growth]                              │
  ├─────────────────────────────────────────────┤
  │  Tầng 4: HỆ THỐNG (Systems)                │
  │  Quy trình, công nghệ, cải tiến             │
  │  [09-product-tech] [10-training]             │
  │  [11-reporting]                              │
  ├─────────────────────────────────────────────┤
  │  Tầng 3: ĐỘNG CƠ (Revenue Engine)          │
  │  Sales, Marketing, Khách hàng                │
  │  [06-sales] [07-marketing] [08-customer]     │
  ├─────────────────────────────────────────────┤
  │  Tầng 2: BỘ MÁY (Operations)               │
  │  Nhân sự, Tài chính, Vận hành               │
  │  [03-finance] [04-people] [05-operations]    │
  ├─────────────────────────────────────────────┤
  │  Tầng 1: NỀN MÓNG (Foundation)             │
  │  Pháp lý, Chiến lược, Quản trị              │
  │  [01-governance] [02-strategy]               │
  └─────────────────────────────────────────────┘
```

**Logic:** Tầng dưới vững trước khi lên tầng trên. Tầng 1–2 bắt buộc. Tầng 3–5 progressive.

---

## III. CÂY THƯ MỤC & DANH MỤC TÀI LIỆU

```
dong-goi-doanh-nghiep/
├── README.md                          # Tổng quan skill set
├── BLUEPRINT.md                       # ← BẠN ĐANG ĐỌC FILE NÀY
│
├── 00-bb-orchestrator/                # Meta — Điều phối tổng thể
│   ├── README.md                      # Giải thích + Prompts
│   ├── intake-questionnaire.md        # FRM — Bộ câu hỏi thu thập info DN
│   ├── scope-assessment.md            # SOP — Đánh giá scope & ưu tiên
│   ├── directory-scaffold.md          # SOP — Tạo cây thư mục chuẩn
│   ├── execution-flow.md              # SOP — Luồng thực thi 12 skill con
│   ├── quality-checklist.md           # FRM — Checklist kiểm tra chất lượng
│   ├── handover-report.md             # RPT — Báo cáo bàn giao
│   ├── maturity-scoring.md            # FRM — Bảng chấm điểm maturity
│   └── master-glossary.md             # MAN — Bảng thuật ngữ chuẩn hóa
│
├── 01-bb-governance/                  # Tầng 1 — Quản Trị & Pháp Lý
│   ├── README.md
│   ├── 00.1-legal/                    # Hồ sơ pháp lý (6 files)
│   │   ├── dieu-le-cong-ty.md         # POL
│   │   ├── dkkd-scan-checklist.md     # FRM
│   │   ├── danh-sach-giay-phep-con.md # FRM
│   │   ├── thoa-thuan-co-dong.md      # POL
│   │   ├── bb-hop-hdqt-template.md    # FRM
│   │   └── checklist-tuan-thu-phap-ly.md # FRM
│   ├── 00.2-governance/               # Quản trị (5 files)
│   │   ├── quy-che-hdqt.md            # POL
│   │   ├── quy-che-bgd.md             # POL
│   │   ├── ma-tran-phan-quyen-raci.md # FRM
│   │   ├── chinh-sach-quan-ly-rui-ro.md # POL
│   │   └── quy-tac-dao-duc-kinh-doanh.md # POL
│   ├── 00.3-contracts/                # Hợp đồng mẫu (5 files)
│   │   ├── hd-lao-dong-mau.md         # FRM
│   │   ├── hd-dich-vu-mau.md          # FRM
│   │   ├── nda-mau.md                 # FRM
│   │   ├── hd-dai-ly-mau.md           # FRM
│   │   └── hd-hop-tac-kinh-doanh-mau.md # FRM
│   └── 00.4-insurance-compliance/     # Bảo hiểm & Tuân thủ (3 files)
│       ├── danh-muc-bao-hiem-dn.md    # FRM
│       ├── chinh-sach-bao-ve-du-lieu.md # POL
│       └── lich-gia-han-giay-phep.md  # FRM
│
├── 02-bb-strategy/                    # Tầng 1 — Chiến Lược & Kế Hoạch
│   ├── README.md
│   ├── 01.1-identity/                 # Bản sắc DN (4 files)
│   │   ├── company-profile.md         # MAN
│   │   ├── tam-nhin-su-menh-gia-tri.md # POL
│   │   ├── brand-identity-guidelines.md # MAN
│   │   └── elevator-pitch.md          # FRM
│   ├── 01.2-analysis/                 # Phân tích chiến lược (5 files)
│   │   ├── swot-analysis.md           # RPT
│   │   ├── business-model-canvas.md   # FRM
│   │   ├── porter-five-forces.md      # RPT
│   │   ├── competitive-landscape.md   # RPT
│   │   └── ideal-customer-profile.md  # FRM
│   ├── 01.3-planning/                 # Kế hoạch KD (5 files)
│   │   ├── business-plan.md           # MAN
│   │   ├── ogsm-framework.md          # FRM
│   │   ├── okr-template.md            # FRM
│   │   ├── bcg-matrix.md              # RPT
│   │   └── strategic-roadmap.md       # MAN
│   └── 01.4-risk/                     # Quản lý rủi ro chiến lược (4 files)
│       ├── risk-register.md           # FRM
│       ├── crisis-management-plan.md  # SOP
│       ├── business-continuity-plan.md # SOP
│       └── scenario-planning.md       # RPT
│
├── 03-bb-finance/                     # Tầng 2 — Tài Chính & Kế Toán (20 files)
│   ├── README.md
│   ├── chinh-sach-tai-chinh.md        # POL — Chính sách tài chính tổng quát
│   ├── quy-che-chi-tieu-noi-bo.md     # POL — Quy chế chi tiêu nội bộ
│   ├── chinh-sach-quan-ly-cong-no.md  # POL — Chính sách quản lý công nợ
│   ├── chinh-sach-dinh-gia.md         # POL — Chính sách định giá sản phẩm
│   ├── co-cau-chi-phi.md              # MAN — Cơ cấu chi phí CCSC
│   ├── ngan-sach-nam.md               # MAN — Ngân sách năm (Annual Budget)
│   ├── cashflow-forecast-12-thang.md  # RPT — Cashflow Forecast 12 tháng
│   ├── scenario-planning-tai-chinh.md # RPT — Scenario Planning 3 kịch bản
│   ├── phan-tich-hoa-von.md           # RPT — Break-Even Analysis
│   ├── sop-thu-chi.md                 # SOP — Quy trình thu chi
│   ├── sop-doi-soat-cong-no.md        # SOP — Đối soát công nợ
│   ├── sop-ke-toan-thang.md           # SOP — Kế toán tháng (Monthly Close)
│   ├── phieu-thu-chi-template.md      # FRM — Phiếu thu chi template
│   ├── bang-theo-doi-cong-no.md       # FRM — Bảng theo dõi công nợ
│   ├── bang-ke-thue-gtgt.md           # FRM — Bảng kê thuế GTGT
│   ├── bao-cao-pl.md                  # RPT — Báo cáo Kết quả KD (P&L)
│   ├── bang-can-doi-ke-toan.md        # RPT — Bảng Cân đối Kế toán
│   ├── bao-cao-luu-chuyen-tien-te.md  # RPT — Báo cáo Lưu chuyển Tiền tệ
│   ├── dashboard-tai-chinh-thang.md   # RPT — Dashboard tài chính tháng
│   └── thuyet-minh-bctc.md            # RPT — Thuyết minh BCTC
│
├── 04-bb-people/                      # Tầng 2 — Nhân Sự & Con Người (22 files)
│   ├── README.md
│   ├── so-do-to-chuc.md               # MAN — Sơ đồ tổ chức (Org Chart)
│   ├── jd-template-chung.md           # FRM — JD Template chung
│   ├── jd-vi-tri-chu-chot.md          # FRM — JD các vị trí chủ chốt
│   ├── headcount-plan.md              # MAN — Headcount Plan
│   ├── noi-quy-lao-dong.md            # POL — Nội quy lao động
│   ├── quy-che-luong-thuong.md        # POL — Quy chế lương thưởng
│   ├── chinh-sach-phuc-loi.md         # POL — Chính sách phúc lợi
│   ├── chinh-sach-nghi-phep.md        # POL — Chính sách nghỉ phép
│   ├── chinh-sach-lam-viec-tu-xa.md   # POL — Chính sách làm việc từ xa
│   ├── quy-che-bao-mat-thong-tin.md   # POL — Quy chế bảo mật thông tin
│   ├── sop-tuyen-dung.md              # SOP — Quy trình tuyển dụng
│   ├── bo-cau-hoi-phong-van.md        # FRM — Bộ câu hỏi phỏng vấn
│   ├── scorecard-danh-gia-ung-vien.md # FRM — Scorecard đánh giá ứng viên
│   ├── thu-moi-nhan-viec.md           # FRM — Thư mời nhận việc (Offer Letter)
│   ├── sop-tiep-nhan-nv-moi.md        # SOP — Quy trình tiếp nhận NV mới
│   ├── so-tay-nhan-vien.md            # MAN — Sổ tay nhân viên (Employee Handbook)
│   ├── checklist-onboarding-30-60-90.md # FRM — Checklist Onboarding 30-60-90
│   ├── sop-nghi-viec.md               # SOP — Quy trình nghỉ việc
│   ├── bien-ban-ban-giao-cong-viec.md # FRM — Biên bản bàn giao công việc
│   ├── chinh-sach-danh-gia-hieu-suat.md # POL — Chính sách đánh giá hiệu suất
│   ├── kpi-ca-nhan-template.md        # FRM — KPI cá nhân template
│   └── form-danh-gia-360.md           # FRM — Form đánh giá 360 độ
│
├── 05-bb-operations/                  # Tầng 2 — Hành Chính & Vận Hành (20 files)
│   ├── README.md
│   ├── sop-quan-ly-van-phong.md       # SOP — Quản lý văn phòng
│   ├── sop-mua-sam-tai-san.md         # SOP — Mua sắm tài sản
│   ├── so-theo-doi-tai-san.md         # FRM — Sổ theo dõi tài sản
│   ├── sop-quan-ly-kho.md             # SOP — Quản lý kho
│   ├── noi-quy-van-phong.md           # POL — Nội quy văn phòng
│   ├── sop-danh-gia-nha-cung-cap.md   # SOP — Đánh giá nhà cung cấp
│   ├── scorecard-ncc.md               # FRM — Scorecard NCC
│   ├── danh-sach-ncc-da-duyet.md      # FRM — Danh sách NCC đã duyệt
│   ├── sop-dat-hang.md                # SOP — Đặt hàng
│   ├── so-tay-van-hanh.md             # MAN — Sổ tay vận hành (Operations Manual)
│   ├── sop-template-chuan.md          # SOP — SOP Template chuẩn
│   ├── sop-cot-loi.md                 # SOP — SOP cốt lõi (Core Processes)
│   ├── checklist-van-hanh-hang-ngay.md # FRM — Checklist vận hành hàng ngày
│   ├── chinh-sach-an-toan-lao-dong.md # POL — Chính sách an toàn lao động
│   ├── sop-xu-ly-su-co.md             # SOP — Xử lý sự cố
│   ├── chinh-sach-chat-luong.md       # POL — Chính sách chất lượng
│   ├── quy-che-hop-hanh.md            # POL — Quy chế họp hành
│   ├── template-bien-ban-hop.md       # FRM — Template biên bản họp
│   ├── template-bao-cao-tuan.md       # FRM — Template báo cáo tuần
│   └── sop-truyen-thong-noi-bo.md     # SOP — Truyền thông nội bộ
│
├── 06-bb-sales/                       # Tầng 3 — Kinh Doanh & Bán Hàng (17 files)
│   ├── README.md
│   ├── chien-luoc-kinh-doanh.md       # MAN — Chiến lược kinh doanh & Target
│   ├── chien-luoc-gia.md              # MAN — Chiến lược giá (Pricing Strategy)
│   ├── chien-luoc-kenh-phan-phoi.md   # MAN — Chiến lược kênh phân phối
│   ├── phan-tich-don-vi-kinh-te.md    # RPT — Phân tích đơn vị kinh tế (Unit Economics)
│   ├── quy-trinh-ban-hang.md          # SOP — Quy trình bán hàng (Sales Process)
│   ├── kich-ban-ban-hang.md           # FRM — Kịch bản bán hàng (Sales Script)
│   ├── xu-ly-tu-choi.md               # FRM — Xử lý từ chối (Objection Handling)
│   ├── quy-trinh-bao-gia.md           # SOP — Quy trình báo giá
│   ├── mau-de-xuat-bao-gia.md         # FRM — Mẫu đề xuất báo giá (Proposal)
│   ├── hop-dong-ban-hang.md           # FRM — Hợp đồng bán hàng
│   ├── so-tay-ban-hang.md             # MAN — Sổ tay bán hàng (Sales Playbook)
│   ├── theo-doi-pipeline.md           # FRM — Theo dõi Pipeline
│   ├── thiet-lap-crm.md              # FRM — Thiết lập CRM
│   ├── bao-cao-doanh-so.md            # FRM — Báo cáo doanh số
│   ├── chinh-sach-dai-ly.md           # POL — Chính sách đại lý
│   ├── hop-dong-dai-ly.md             # FRM — Hợp đồng đại lý
│   └── onboard-doi-tac.md             # SOP — Onboard đối tác
│
├── 07-bb-marketing/                   # Tầng 3 — Marketing & Thương Hiệu (10 files)
│   ├── README.md
│   ├── ke-hoach-marketing-nam.md      # MAN — Kế hoạch Marketing năm
│   ├── chien-luoc-noi-dung.md         # MAN — Chiến lược nội dung (Content Strategy)
│   ├── ban-do-hanh-trinh-khach-hang.md # RPT — Bản đồ hành trình KH (Customer Journey)
│   ├── phan-tich-doi-thu-marketing.md # RPT — Phân tích đối thủ Marketing
│   ├── phan-bo-ngan-sach-marketing.md # MAN — Phân bổ ngân sách Marketing
│   ├── quy-trinh-chay-ads.md          # SOP — Quy trình chạy Ads
│   ├── quy-trinh-seo.md              # SOP — Quy trình SEO
│   ├── quy-trinh-email-marketing.md   # SOP — Quy trình Email Marketing
│   ├── so-tay-mang-xa-hoi.md          # MAN — Sổ tay mạng xã hội (Social Playbook)
│   └── lich-noi-dung.md               # FRM — Lịch nội dung (Content Calendar)
│
├── 08-bb-customer/                    # Tầng 3 — Khách Hàng & Dịch Vụ (12 files)
│   ├── README.md
│   ├── man-customer-experience-standards.md # MAN — Tiêu chuẩn trải nghiệm KH
│   ├── sop-onboard-khach-hang.md      # SOP — Onboard khách hàng
│   ├── sop-cham-soc-sau-ban.md        # SOP — Chăm sóc sau bán
│   ├── frm-khao-sat-nps-csat.md       # FRM — Khảo sát NPS/CSAT
│   ├── sop-xu-ly-khieu-nai.md         # SOP — Xử lý khiếu nại
│   ├── pol-hoan-tien-bao-hanh.md      # POL — Chính sách hoàn tiền & bảo hành
│   ├── frm-log-khieu-nai.md           # FRM — Log khiếu nại
│   ├── sop-phan-loai-kh.md            # SOP — Phân loại khách hàng
│   ├── man-loyalty-retention.md       # MAN — Loyalty & Retention Program
│   ├── frm-customer-health-score.md   # FRM — Customer Health Score
│   ├── man-referral-program.md        # MAN — Referral Program
│   └── sop-thu-thap-review.md         # SOP — Thu thập review & testimonial
│
├── 09-bb-product-tech/                # Tầng 4 — Sản Phẩm & Công Nghệ (13 files)
│   ├── README.md
│   ├── danh-muc-san-pham-dich-vu.md   # MAN — Danh mục sản phẩm/dịch vụ
│   ├── lo-trinh-phat-trien-san-pham.md # MAN — Lộ trình phát triển sản phẩm
│   ├── sop-phat-trien-san-pham-moi.md # SOP — Phát triển sản phẩm mới
│   ├── product-brief-template.md      # FRM — Product Brief Template
│   ├── sop-kiem-soat-chat-luong.md    # SOP — Kiểm soát chất lượng
│   ├── tech-stack-map.md              # MAN — Tech Stack Map
│   ├── chinh-sach-cntt.md             # POL — Chính sách CNTT
│   ├── chinh-sach-an-ninh-mang.md     # POL — Chính sách an ninh mạng
│   ├── sop-backup-du-lieu.md          # SOP — Backup dữ liệu
│   ├── danh-sach-tai-khoan-he-thong.md # MAN — Danh sách tài khoản hệ thống
│   ├── kaizen-board.md                # MAN — Kaizen Board
│   ├── mau-de-xuat-cai-tien.md        # FRM — Mẫu đề xuất cải tiến
│   └── sop-review-cap-nhat-sop.md     # SOP — Review & cập nhật SOP
│
├── 10-bb-training/                    # Tầng 4 — Đào Tạo & Phát Triển (10 files)
│   ├── README.md
│   ├── chinh-sach-dao-tao.md          # POL — Chính sách đào tạo
│   ├── khao-sat-nhu-cau-dao-tao.md    # FRM — Khảo sát nhu cầu đào tạo
│   ├── ke-hoach-dao-tao-hang-nam.md   # MAN — Kế hoạch đào tạo hàng năm
│   ├── chuong-trinh-dao-tao-hoi-nhap.md # SOP — Chương trình đào tạo hội nhập
│   ├── chuong-trinh-phat-trien-lanh-dao.md # MAN — Chương trình phát triển lãnh đạo
│   ├── mau-tai-lieu-dao-tao.md        # FRM — Mẫu tài liệu đào tạo
│   ├── mau-danh-gia-hieu-qua-dao-tao.md # FRM — Mẫu đánh giá hiệu quả đào tạo
│   ├── chuong-trinh-mentoring-coaching.md # SOP — Chương trình Mentoring/Coaching
│   ├── huong-dan-he-thong-quan-ly-tri-thuc.md # MAN — Hệ thống quản lý tri thức
│   └── bao-cao-roi-dao-tao.md         # RPT — Báo cáo ROI đào tạo
│
├── 11-bb-reporting/                   # Tầng 4 — Báo Cáo & Đo Lường (10 files)
│   ├── README.md
│   ├── pol-chinh-sach-bao-cao.md      # POL — Chính sách báo cáo
│   ├── man-tu-dien-kpi.md             # MAN — Từ điển KPI
│   ├── sop-thu-thap-xac-thuc-du-lieu.md # SOP — Thu thập & xác thực dữ liệu
│   ├── frm-bao-cao-quan-tri-hang-thang.md # FRM — Báo cáo quản trị hàng tháng
│   ├── frm-bao-cao-tai-chinh.md       # FRM — Báo cáo tài chính
│   ├── man-thiet-ke-dashboard.md      # MAN — Thiết kế Dashboard
│   ├── frm-bao-cao-hdqt.md            # FRM — Báo cáo HĐQT
│   ├── frm-danh-gia-kinh-doanh-quy.md # FRM — Đánh giá kinh doanh quý
│   ├── rpt-benchmarking.md            # RPT — Benchmarking Report
│   └── frm-bao-cao-thuong-nien.md     # FRM — Báo cáo thường niên
│
└── 12-bb-growth/                      # Tầng 5 — Tăng Trưởng & Đầu Tư (12 files)
    ├── README.md
    ├── pitch-deck.md                  # MAN — Pitch Deck
    ├── mo-hinh-tai-chinh-dinh-gia.md  # RPT — Mô hình tài chính & định giá
    ├── investment-memo.md             # MAN — Investment Memo
    ├── cap-table.md                   # RPT — Cap Table
    ├── term-sheet-template.md         # FRM — Term Sheet Template
    ├── thiet-ke-mo-hinh-nhuong-quyen.md # MAN — Thiết kế mô hình nhượng quyền
    ├── so-tay-van-hanh-nhuong-quyen.md # MAN — Sổ tay vận hành nhượng quyền
    ├── phan-tich-mo-rong-thi-truong.md # RPT — Phân tích mở rộng thị trường
    ├── hop-dong-nhuong-quyen-mau.md   # FRM — Hợp đồng nhượng quyền mẫu
    ├── lua-chon-thoat-von.md          # MAN — Lựa chọn thoát vốn (Exit Strategy)
    ├── ke-hoach-ke-nhiem.md           # MAN — Kế hoạch kế nhiệm (Succession Plan)
    └── bao-cao-dinh-gia-doanh-nghiep.md # RPT — Báo cáo định giá doanh nghiệp
```

### Loại tài liệu (Document Types)

| Mã | Loại | Mô tả |
|-----|------|-------|
| POL | Policy | Chính sách — quy định nền tảng, ít thay đổi |
| MAN | Manual | Sổ tay — hướng dẫn chi tiết, tham khảo dài hạn |
| SOP | Standard Operating Procedure | Quy trình — từng bước thực hiện |
| FRM | Form/Template | Biểu mẫu — điền và dùng ngay |
| RPT | Report | Báo cáo — phân tích, đánh giá, tổng kết |

---

## IV. TỔNG HỢP THỐNG KÊ

| Skill | Tầng | Số files | POL | MAN | SOP | FRM | RPT | Status |
|-------|------|----------|-----|-----|-----|-----|-----|--------|
| 00-orchestrator | Meta | 8 | — | 1 | 3 | 3 | 1 | ✅ Done |
| 01-governance | 1 | 19 | 6 | — | — | 10 | — | ✅ Done |
| 02-strategy | 1 | 18 | 1 | 4 | 2 | 5 | 5 | ✅ Done |
| 03-finance | 2 | 20 | 4 | 2 | 3 | 3 | 8 | ✅ Done |
| 04-people | 2 | 22 | 7 | 3 | 3 | 8 | — | ⚠️ 22/27 (thiếu 5 files từ 03.5–03.6) |
| 05-operations | 2 | 20 | 4 | 1 | 9 | 6 | — | ✅ Done |
| 06-sales | 3 | 17 | 1 | 4 | 3 | 8 | 1 | ✅ Done |
| 07-marketing | 3 | 10 | — | 4 | 3 | 1 | 2 | ⚠️ 10/18 (thiếu 8 files từ 06.3–06.4) |
| 08-customer | 3 | 12 | 1 | 3 | 5 | 3 | — | ✅ Done |
| 09-product-tech | 4 | 13 | 2 | 5 | 4 | 2 | — | ✅ Done |
| 10-training | 4 | 10 | 1 | 3 | 2 | 3 | 1 | ✅ Done |
| 11-reporting | 4 | 10 | 1 | 2 | 1 | 5 | 1 | ✅ Done |
| 12-growth | 5 | 12 | — | 6 | — | 2 | 4 | ✅ Done |
| **TỔNG** | | **204** | **28** | **38** | **38** | **59** | **23** | **13/13 done** |

> **Lưu ý:** 04-bb-people thiếu 5 files (career-path, training-plan-nam, culture-code, chuong-trinh-gan-ket-nv, khao-sat-hai-long-nv). 07-bb-marketing thiếu 8 files (06.3 Tài liệu bán hàng + 06.4 Đo lường). Tổng khi hoàn thành đầy đủ: **204 files**.

---

## V. KIẾN TRÚC SKILL SET

### Mô hình tổng thể

```
                    ┌─────────────────────┐
                    │  00 ORCHESTRATOR     │
                    │  (Brain / Meta)      │
                    └──────────┬──────────┘
                               │ Gọi tuần tự
        ┌──────────────────────┼──────────────────────┐
        ▼                      ▼                      ▼
  ┌──────────┐          ┌──────────┐          ┌──────────┐
  │ Tầng 1   │          │ Tầng 2   │          │ Tầng 3   │
  │ Nền Móng │          │ Bộ Máy   │          │ Động Cơ  │
  │ 01-02    │          │ 03-04-05 │          │ 06-07-08 │
  └──────────┘          └──────────┘          └──────────┘
        ┌──────────────────────┼──────────────────────┐
        ▼                      ▼
  ┌──────────┐          ┌──────────┐
  │ Tầng 4   │          │ Tầng 5   │
  │ Hệ Thống │          │ Tăng     │
  │ 09-10-11 │          │ Trưởng   │
  └──────────┘          │ 12       │
                        └──────────┘
```

### Mỗi skill folder chứa

| File | Nội dung |
|------|----------|
| `README.md` | A. Giải thích thư mục → B. Danh sách file → C. Ma trận phân quyền → D. Prompts chi tiết |
| `*.md` (output files) | Tài liệu thực tế được tạo ra khi chạy skill |

### Dependency Map giữa các skill

```
01-governance ──┬──→ 02-strategy ──┬──→ 03-finance
                │                  ├──→ 04-people
                │                  ├──→ 06-sales
                │                  └──→ 07-marketing
                │
                └──→ 03-finance
                └──→ 05-operations

04-people ──→ 10-training
03-finance ──→ 11-reporting
06-sales + 07-marketing ──→ 08-customer
09-product-tech ──→ 11-reporting
All skills ──→ 12-growth
```

---

## VI. FLOW VẬN HÀNH

### Flow tổng thể của Orchestrator

```
START
  │
  ▼
[1] Chạy Intake Questionnaire → Thu thập thông tin DN
  │
  ▼
[2] Chạy Maturity Scoring → Chấm điểm 9 khía cạnh
  │
  ▼
[3] Chạy Scope Assessment → Xác định scope & ưu tiên
  │
  ▼
[4] Chạy Directory Scaffold → Tạo cây thư mục
  │
  ▼
[5] Chạy Execution Flow → Xác nhận thứ tự skill con
  │
  ▼
[6] GỌI SKILL CON 01→12 (theo thứ tự đã xác định)
  │   ├── Sau mỗi skill: Chạy Quality Checklist (per-skill)
  │   └── Tại checkpoint: Dừng để review & approve
  │
  ▼
[7] Chạy Quality Checklist (toàn bộ) → Verify completeness
  │
  ▼
[8] Tạo Handover Report → Bàn giao
  │
  ▼
END
```

### Checkpoint Gates

| Gate | Vị trí | Mục đích |
|------|--------|----------|
| Gate 1 | Sau Intake + Maturity | Xác nhận thông tin DN đầy đủ |
| Gate 2 | Sau Scope Assessment | Duyệt scope & ưu tiên trước khi build |
| Gate 3 | Sau Tầng 1 (01-02) | Review nền móng trước khi lên bộ máy |
| Gate 4 | Sau Tầng 2 (03-05) | Review core ops trước khi lên revenue |
| Gate 5 | Sau Tầng 3 (06-08) | Review revenue engine trước khi lên systems |
| Gate 6 | Sau tất cả | Quality check tổng thể + Handover |

---

## VII. THỨ TỰ BUILD

### Build Order — Phát triển bộ Skill Set

| Phase | Skills | Tầng | Mô tả | Status |
|-------|--------|------|-------|--------|
| Phase 1 | 00 → 01 → 02 | Meta + T1 | Foundation: Orchestrator + Nền Móng | ✅ **DONE** |
| Phase 2 | 03 → 04 → 05 | T2 | Core Ops: Tài chính + Nhân sự + Vận hành | ✅ **DONE** |
| Phase 3 | 06 → 07 → 08 | T3 | Revenue: Sales + Marketing + Khách hàng | ✅ **DONE** |
| Phase 4 | 09 → 10 → 11 → 12 | T4 + T5 | Systems & Scale: Product + Training + Reporting + Growth | ✅ **DONE** |

### Ước lượng effort per phase

| Phase | Skills | Files ước tính | Files thực tế | Thời gian |
|-------|--------|---------------|--------------|-----------|
| Phase 1 | 3 | 45 | 45 | ✅ Hoàn thành |
| Phase 2 | 3 | 67 | 62 | ✅ Hoàn thành (thiếu 5 files 04-people) |
| Phase 3 | 3 | 47 | 39 | ✅ Hoàn thành (thiếu 8 files 07-marketing) |
| Phase 4 | 4 | ~50-60 | 45 | ✅ Hoàn thành |
| **Tổng** | **13** | **~209** | **204** | **Đầy đủ** |

---

## VIII. PROMPTS CHI TIẾT

> **Ghi chú:** Phần này chứa TOÀN BỘ prompts từ các README files đã hoàn thành. Mỗi section tương ứng 1 skill folder. Nội dung giữ nguyên 100%, không rút gọn.

---

### VIII.1 — BP Orchestrator (Điều phối tổng thể)

> **Tầng:** Meta / Brain — không thuộc tầng nào trong kiến trúc 5 tầng, mà là bộ điều phối toàn bộ hệ thống.

#### A. Giải thích thư mục

**BP Orchestrator** là "bộ não trung tâm" của toàn bộ hệ thống Đóng Gói Doanh Nghiệp. Skill này không tạo ra tài liệu vận hành cụ thể — thay vào đó, nó:

1. **Thu thập thông tin đầu vào** từ chủ doanh nghiệp qua prompt tương tác
2. **Phân tích & xác định scope** — doanh nghiệp đang ở đâu, cần gì, ưu tiên gì
3. **Tạo cây thư mục chuẩn** — scaffold toàn bộ cấu trúc 200+ tài liệu
4. **Gọi tuần tự 12 skill con** (01→12) theo thứ tự dependencies
5. **Kiểm tra & bàn giao** — verify completeness, tạo báo cáo tổng kết

**Tại sao quan trọng:**

- **ISO 9001:2015** yêu cầu tiếp cận theo quy trình (Process Approach) và tư duy dựa trên rủi ro — Orchestrator đảm bảo mọi skill con đều tuân thủ logic này.
- **EOS/Traction** nhấn mạnh bắt đầu từ Vision → xuống People → Process → Traction — Orchestrator giữ đúng trình tự này.
- **E-Myth** phân biệt rõ "làm trong DN" vs "làm trên DN" — Orchestrator giúp chủ DN nhìn toàn cảnh thay vì chìm vào chi tiết.
- **McKinsey 7S** yêu cầu alignment 7 yếu tố — Orchestrator kiểm tra sự đồng bộ giữa các tầng.

#### B. Danh sách file sẽ tạo

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 1 | `intake-questionnaire.md` | FRM | Bộ câu hỏi thu thập thông tin DN — 5 nhóm: cơ bản, giai đoạn, cấu trúc hiện tại, ưu tiên, đặc thù ngành |
| 2 | `scope-assessment.md` | SOP | Quy trình đánh giá scope & xác định tầng ưu tiên dựa trên maturity model |
| 3 | `directory-scaffold.md` | SOP | Hướng dẫn tạo cây thư mục chuẩn — cấu trúc folder, naming convention, file numbering |
| 4 | `execution-flow.md` | SOP | Luồng thực thi: trình tự gọi 12 skill con, điều kiện trigger, xử lý dependency |
| 5 | `quality-checklist.md` | FRM | Checklist kiểm tra completeness sau khi hoàn thành — per-skill và tổng thể |
| 6 | `handover-report.md` | RPT | Template báo cáo bàn giao — tổng kết những gì đã tạo, hướng dẫn sử dụng, next steps |
| 7 | `maturity-scoring.md` | FRM | Bảng chấm điểm mức độ trưởng thành DN theo 9 khía cạnh (0-5 scale) |
| 8 | `master-glossary.md` | MAN | Bảng thuật ngữ chuẩn hóa toàn bộ hệ thống — đảm bảo consistency xuyên suốt 200+ file |

#### C. Ma trận phân quyền

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| Intake Questionnaire | AI + Business Coach | Chủ DN | Chủ DN, Coach | AI, Coach |
| Scope Assessment | AI (auto-score) | Business Coach | Chủ DN, Coach, Team Lead | Coach |
| Directory Scaffold | AI (auto-generate) | Chủ DN | Toàn công ty | AI, Coach |
| Execution Flow | AI | Business Coach | Coach, AI Operator | Coach |
| Quality Checklist | AI | Business Coach | Coach, Chủ DN | Coach |
| Handover Report | AI | Business Coach + Chủ DN | Toàn công ty | Coach |
| Maturity Scoring | AI + Business Coach | Chủ DN | Coach, HĐQT | Coach, Chủ DN |
| Master Glossary | AI | Business Coach | Toàn công ty | Coach |

#### D. Prompts cho từng file

---

##### PROMPT 01: Intake Questionnaire (Bộ câu hỏi thu thập thông tin DN)

**Mô tả:**
Bộ câu hỏi có cấu trúc để thu thập toàn bộ thông tin cần thiết từ chủ doanh nghiệp trước khi bắt đầu đóng gói. Đây là bước quan trọng nhất — "garbage in, garbage out". Chia thành 5 nhóm câu hỏi, từ cơ bản đến chuyên sâu.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Anh muốn bộ câu hỏi ở dạng nào? (Google Form / Markdown checklist / PDF form / Interactive prompt)
2. Ngành nghề cụ thể của DN? (để customize câu hỏi đặc thù ngành)
3. Ai sẽ là người điền? (chủ DN trực tiếp / trợ lý / team?)
4. Có cần version tiếng Anh song song không?
5. Mức độ chi tiết mong muốn? (Quick scan ~20 câu / Standard ~50 câu / Deep dive ~100 câu)

**Template gợi ý:**
Cấu trúc 5 nhóm câu hỏi:
- **Nhóm 1 — Thông tin cơ bản** (10-15 câu): Tên DN, ngành, năm thành lập, doanh thu, nhân sự, địa bàn, pháp nhân
- **Nhóm 2 — Giai đoạn phát triển** (8-10 câu): Stage hiện tại (startup/growth/mature), mục tiêu 1-3-5 năm, đã gọi vốn chưa, có kế hoạch mở chuỗi/nhượng quyền không
- **Nhóm 3 — Cấu trúc hiện tại** (10-15 câu): Có sơ đồ tổ chức chưa, bao nhiêu phòng ban, quy trình nào đã chuẩn hóa, công cụ đang dùng (CRM, ERP, kế toán...)
- **Nhóm 4 — Ưu tiên & Pain points** (8-10 câu): Top 3 vấn đề lớn nhất, lĩnh vực muốn ưu tiên đóng gói, budget & timeline
- **Nhóm 5 — Đặc thù ngành** (5-10 câu): Quy định ngành, giấy phép đặc biệt, seasonal patterns, đặc điểm nhân sự ngành

Format: Markdown với checkbox, mỗi câu có hint/ví dụ. Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo bộ câu hỏi thu thập thông tin doanh nghiệp (Intake Questionnaire) cho dự án Đóng Gói Doanh Nghiệp.

CONTEXT:
- Mục đích: Thu thập đủ thông tin để AI + Business Coach xác định scope đóng gói và customize 200+ tài liệu cho DN cụ thể
- Người điền: [Chủ DN / Trợ lý] — ngành [ngành nghề]
- Mức độ: [Quick/Standard/Deep dive]

FORMAT:
- Markdown với checkbox [ ] cho mỗi câu hỏi
- Mỗi câu có: Câu hỏi chính → Gợi ý/ví dụ (in nghiêng) → Ô trả lời
- Chia rõ 5 nhóm, đánh số liên tục
- Song ngữ Việt-Anh cho thuật ngữ chuyên ngành
- Cuối mỗi nhóm có "Ghi chú bổ sung" dạng free-text

TONE: Chuyên nghiệp nhưng thân thiện, dễ hiểu cho chủ DN không chuyên.
LENGTH: [20/50/100] câu hỏi tùy mức độ đã chọn.

OUTPUT: File markdown hoàn chỉnh, sẵn sàng gửi cho chủ DN điền.
```

---

##### PROMPT 02: Scope Assessment (Quy trình đánh giá scope)

**Mô tả:**
SOP hướng dẫn cách phân tích kết quả Intake Questionnaire để xác định: DN đang ở maturity level nào, nên ưu tiên tầng nào, skill con nào cần chạy trước, skill nào có thể skip hoặc customize.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Anh đã có maturity model riêng chưa, hay dùng model chuẩn?
2. Tiêu chí nào quyết định thứ tự ưu tiên? (urgency / impact / effort / cost)
3. Có trường hợp nào cần skip skill con hoàn toàn không? (VD: DN 1 người không cần HR)
4. Ai sẽ là người đánh giá scope? (AI tự động / Coach review / cả hai)

**Template gợi ý:**
Cấu trúc SOP:
- **Mục đích & Phạm vi** — Khi nào dùng, ai dùng
- **Input** — Intake Questionnaire đã điền
- **Bước 1: Chấm điểm maturity** — 9 khía cạnh × thang 0-5, tham chiếu `maturity-scoring.md`
- **Bước 2: Xác định tầng ưu tiên** — Decision tree dựa trên score + mục tiêu DN
- **Bước 3: Customize skill list** — Bảng 12 skill × (Run/Skip/Customize) + lý do
- **Bước 4: Ước lượng timeline** — Công thức tính thời gian dựa trên scope
- **Output** — Scope Document (summary 1 trang) + Execution Plan

Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo SOP "Scope Assessment" cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- Đây là bước 2 trong flow Orchestrator: sau khi thu thập thông tin (Intake), trước khi tạo thư mục và gọi skill con
- Maturity model: [model riêng / chuẩn] — 9 khía cạnh: Chiến lược, Tài chính, Marketing, Bán hàng, Vận hành, Nhân sự, Công nghệ, Quản trị, Đào tạo
- Thang điểm: 0 (chưa có gì) → 5 (world-class, đã tự động hóa)
- Tiêu chí ưu tiên: [urgency/impact/effort/cost]
- 12 skill con: governance, strategy, finance, people, operations, sales, marketing, customer, product-tech, training, reporting, growth

FORMAT:
- SOP chuẩn: Mục đích → Phạm vi → Thuật ngữ → Quy trình từng bước → Flowchart (mermaid) → Output template
- Có decision tree rõ ràng: IF score < X THEN ưu tiên Y
- Bảng mapping: Maturity Score → Recommended Action per skill
- Song ngữ Việt-Anh cho thuật ngữ

TONE: Chuẩn mực, rõ ràng, dễ follow cho cả AI lẫn Coach.
LENGTH: 3-5 trang A4.
```

---

##### PROMPT 03: Directory Scaffold (Cây thư mục chuẩn)

**Mô tả:**
SOP hướng dẫn tạo cây thư mục hoàn chỉnh cho DN — bao gồm naming convention, numbering system, và template README cho mỗi folder. Đảm bảo 200+ file được tổ chức logic, dễ tìm, dễ maintain.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. DN muốn lưu trữ ở đâu? (Google Drive / SharePoint / Notion / Local folder / Git repo)
2. Có naming convention riêng không? (VD: [Dept]-[Type]-[Name]-v[Version])
3. Ngôn ngữ file name: tiếng Việt, tiếng Anh, hay mã số?
4. Cần version control không? (v1, v2... hay date-based?)
5. Có cần phân quyền truy cập theo folder không?

**Template gợi ý:**
Cấu trúc SOP:
- **Naming Convention** — Quy tắc đặt tên: `[##]-[Category]-[Type]-[Name].[ext]`
- **Numbering System** — 00-12 cho skill, 00.1-00.x cho sub-groups
- **Folder Structure** — Tree view đầy đủ 5 tầng
- **README Template** — Mỗi folder có README mô tả contents
- **File Types** — POL/MAN/SOP/FRM/RPT + extension mapping
- **Auto-generation Script** — Pseudocode/script tạo toàn bộ cây thư mục

Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo SOP "Directory Scaffold" — hướng dẫn tạo cây thư mục chuẩn cho bộ Đóng Gói Doanh Nghiệp.

CONTEXT:
- Hệ thống 13 skill (00-12), mỗi skill có sub-groups, mỗi sub-group có 3-8 files
- Tổng: 200+ files cần tổ chức logic
- Storage: [Google Drive / SharePoint / Notion / Local / Git]
- Naming: [convention cụ thể hoặc dùng chuẩn]
- Ngôn ngữ: [Việt / Anh / Code]

FORMAT:
- Full tree view dạng ASCII art — đến level 3 (Skill → Sub-group → File)
- Bảng mapping: Folder → Description → Owner → Access Level
- Naming convention reference card (1 trang, in ra dán lên tường)
- Script tạo thư mục tự động (bash/python) nếu dùng local/Git
- Template README.md cho mỗi folder

TONE: Technical, chính xác, dễ follow.
LENGTH: 4-6 trang A4 + appendix (tree view full).
```

---

##### PROMPT 04: Execution Flow (Luồng thực thi)

**Mô tả:**
SOP mô tả chi tiết luồng thực thi: thứ tự gọi 12 skill con, điều kiện trigger mỗi skill, dependencies giữa các skill, cách xử lý khi 1 skill fail hoặc bị skip.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Muốn chạy tuần tự (sequential) hay song song (parallel) khi có thể?
2. Có checkpoint review giữa các tầng không? (VD: dừng sau Tầng 1 để chủ DN duyệt)
3. Khi 1 skill fail, hành xử thế nào? (retry / skip / halt all)
4. Ai approve kết quả mỗi skill trước khi chuyển sang skill tiếp?
5. Có time-box cho mỗi skill không? (VD: mỗi skill tối đa 2 giờ)

**Template gợi ý:**
Cấu trúc SOP:
- **Execution Modes** — Full run / Selective run / Single skill
- **Dependency Map** — Skill nào phụ thuộc skill nào (DAG diagram)
- **Trigger Conditions** — Khi nào skill được activate
- **Checkpoint Gates** — Điểm dừng để review & approve
- **Error Handling** — Retry logic, fallback, escalation
- **Progress Tracking** — Status dashboard (% complete per skill)
- **Flowchart** — Mermaid diagram toàn bộ luồng

Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo SOP "Execution Flow" — luồng thực thi cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- 12 skill con (01→12) được gọi bởi Orchestrator (00)
- 5 tầng: Nền Móng (01-02) → Bộ Máy (03-05) → Động Cơ (06-08) → Hệ Thống (09-11) → Tăng Trưởng (12)
- Mode: [Sequential / Parallel where possible]
- Checkpoint: [Có / Không] — tại [vị trí checkpoint]
- Error handling: [retry/skip/halt]
- Approver: [Chủ DN / Coach / Auto]

FORMAT:
- Flowchart tổng thể dạng Mermaid
- Dependency matrix (12×12): skill X cần output từ skill Y
- Bảng Trigger Conditions: Skill | Pre-conditions | Input required | Output expected
- Error handling decision tree
- Progress tracking template (bảng status)
- Estimated timeline per skill & per tier

TONE: Technical, process-oriented, không mơ hồ.
LENGTH: 5-7 trang A4.
```

---

##### PROMPT 05: Quality Checklist (Checklist kiểm tra chất lượng)

**Mô tả:**
Form checklist để verify mỗi skill con đã tạo đủ output, đúng format, đúng nội dung. Dùng sau khi hoàn thành mỗi skill và sau khi hoàn thành toàn bộ hệ thống.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Tiêu chuẩn chất lượng nào áp dụng? (ISO 9001 / internal standard / custom)
2. Ai sẽ check? (AI auto-check / Coach / cả hai)
3. Mức pass/fail: % hoàn thành tối thiểu để coi là "done"?
4. Có cần scoring hay chỉ cần pass/fail per item?

**Template gợi ý:**
Cấu trúc FRM:
- **Per-Skill Checklist** — 12 bảng, mỗi bảng liệt kê files expected + criteria
- **Cross-Skill Checklist** — Consistency check: thuật ngữ, format, cross-references
- **Completeness Score** — Tổng files tạo / tổng files expected × 100%
- **Quality Score** — Dựa trên criteria: Accuracy, Completeness, Consistency, Usability
- **Issues Log** — Bảng ghi nhận issues + severity + action required

Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo Quality Checklist cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- 12 skill con, mỗi skill tạo ra 5-20 files
- Tổng: 200+ files cần kiểm tra
- Tiêu chuẩn: [ISO 9001 / internal / custom]
- Checker: [AI / Coach / cả hai]
- Pass threshold: [% tối thiểu]

FORMAT:
- Per-skill checklist: Bảng | File | Có/Không | Đúng format | Đủ nội dung | Notes
- Cross-skill checklist: Thuật ngữ nhất quán | Cross-ref đúng | Naming convention | Version
- Summary scorecard: Skill × 4 criteria = matrix score
- Issues log template: # | Skill | File | Issue | Severity | Action | Owner | Due
- Final sign-off section: Coach signature + Chủ DN signature + Date

TONE: Nghiêm túc, chuẩn mực, kiểu audit.
LENGTH: 8-10 trang A4 (bao gồm 12 per-skill tables).
```

---

##### PROMPT 06: Handover Report (Báo cáo bàn giao)

**Mô tả:**
Template báo cáo tổng kết sau khi hoàn thành toàn bộ dự án đóng gói. Tóm tắt những gì đã tạo, hướng dẫn sử dụng, và next steps cho DN.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Bàn giao cho ai? (Chủ DN / CEO / COO / Team quản lý)
2. Format mong muốn? (PDF report / Presentation / Markdown)
3. Cần training session kèm theo không?
4. Có commitment follow-up sau bàn giao không? (30/60/90 ngày)

**Template gợi ý:**
Cấu trúc RPT:
- **Executive Summary** — 1 trang: DN nào, scope gì, kết quả tổng quan
- **Deliverables Inventory** — Bảng liệt kê toàn bộ files đã tạo, phân theo tầng
- **Maturity Before/After** — Spider chart: 9 khía cạnh, score trước vs sau
- **Quick Start Guide** — Top 10 files nên đọc đầu tiên
- **Implementation Roadmap** — Lộ trình triển khai: tuần 1-2-3-4 nên làm gì
- **FAQ** — 10 câu hỏi thường gặp khi bắt đầu dùng bộ tài liệu
- **Support & Next Steps** — Liên hệ hỗ trợ, lịch follow-up

Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo template Handover Report cho dự án Đóng Gói Doanh Nghiệp.

CONTEXT:
- DN: [Tên DN] — Ngành: [ngành] — Quy mô: [số nhân sự]
- Scope: [Full / Selective] — Skills đã chạy: [danh sách]
- Bàn giao cho: [Chức danh người nhận]
- Follow-up: [Có/Không] — [30/60/90 ngày]

FORMAT:
- Professional report layout: Cover page → TOC → Body → Appendix
- Executive Summary: 1 trang, bullet points, highlight key wins
- Deliverables table: Tầng | Skill | Files | Status | Priority sử dụng
- Spider/Radar chart data: 9 khía cạnh × before/after scores
- Quick Start: Top 10 files + vì sao nên đọc đầu tiên
- Implementation Roadmap: Gantt-style theo tuần
- FAQ: Q&A format, 10 câu
- Appendix: Full file list, glossary reference

TONE: Executive — chuyên nghiệp, tự tin, hướng hành động.
LENGTH: 8-12 trang A4.
```

---

##### PROMPT 07: Maturity Scoring (Bảng chấm điểm mức độ trưởng thành)

**Mô tả:**
Form chấm điểm mức độ trưởng thành (maturity level) của DN theo 9 khía cạnh. Dùng ở bước Scope Assessment để xác định ưu tiên, và ở Handover Report để so sánh before/after.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Có muốn customize 9 khía cạnh hay dùng chuẩn? (Chiến lược, Tài chính, Marketing, Bán hàng, Vận hành, Nhân sự, Công nghệ, Quản trị, Đào tạo)
2. Thang điểm: 0-5 hay 1-10?
3. Mỗi level cần mô tả chi tiết (rubric) không?
4. Có cần benchmark theo ngành không?

**Template gợi ý:**
Cấu trúc FRM:
- **Scoring Matrix** — Bảng 9 khía cạnh × 6 levels (0-5), mỗi ô có mô tả cụ thể
- **Level Definitions** — Level 0 (Ad-hoc) → 1 (Initial) → 2 (Defined) → 3 (Managed) → 4 (Optimized) → 5 (World-class)
- **Scoring Guide** — Hướng dẫn cách chấm: evidence-based, ví dụ cụ thể
- **Summary Spider Chart** — Template data cho radar chart
- **Benchmark Reference** — So sánh với trung bình ngành (nếu có)

Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo Maturity Scoring Framework cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- 9 khía cạnh: [liệt kê hoặc dùng chuẩn]
- Thang điểm: [0-5 / 1-10]
- Mục đích: Đánh giá trước khi đóng gói (baseline) và sau khi hoàn thành (progress)

FORMAT:
- Bảng tổng quan: 9 khía cạnh × Score × Evidence × Notes
- Rubric chi tiết: Mỗi khía cạnh × mỗi level = mô tả 2-3 dòng + ví dụ cụ thể
  - VD: Marketing Level 2 = "Có fanpage, đăng bài không đều, chưa có content calendar"
- Spider chart data template: Dạng bảng dữ liệu để vẽ radar chart
- Interpretation guide: Tổng điểm → Recommended action
  - 0-15: "Startup mode — cần xây từ nền móng"
  - 16-30: "Growing — cần hệ thống hóa"
  - 31-45: "Mature — tối ưu & tự động hóa"

TONE: Objective, evidence-based, không judgmental.
LENGTH: 5-8 trang A4.
```

---

##### PROMPT 08: Master Glossary (Bảng thuật ngữ chuẩn hóa)

**Mô tả:**
Bảng thuật ngữ thống nhất cho toàn bộ hệ thống 200+ tài liệu. Đảm bảo mọi skill con dùng cùng một thuật ngữ, cùng một cách viết tắt, cùng một định nghĩa. Tránh tình trạng "KPI" trong file A nghĩa khác file B.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. DN có thuật ngữ nội bộ riêng không? (VD: gọi nhân viên là "partner", gọi khách hàng là "member")
2. Ngôn ngữ chính của tài liệu: tiếng Việt có thuật ngữ Anh, hay full song ngữ?
3. Có acronyms nội bộ cần đưa vào không?
4. Muốn phân loại theo chủ đề hay theo alphabet?

**Template gợi ý:**
Cấu trúc MAN:
- **Quy tắc sử dụng** — Cách dùng glossary, khi nào tham chiếu
- **Bảng thuật ngữ chính** — Term | Viết tắt | Định nghĩa (Việt) | Definition (English) | Ví dụ | Dùng trong skill #
- **Phân loại theo chủ đề** — 9 nhóm theo 9 khía cạnh DN
- **Thuật ngữ nội bộ DN** — Section riêng cho terms đặc thù
- **Danh sách viết tắt** — Quick reference A-Z
- **Version log** — Ai sửa gì khi nào

Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo Master Glossary cho hệ thống Đóng Gói Doanh Nghiệp.

CONTEXT:
- Hệ thống 200+ tài liệu, 12 skill con, 9 khía cạnh DN
- Ngôn ngữ: Tiếng Việt + thuật ngữ chuyên ngành song ngữ Việt-Anh
- DN: [Tên DN] — thuật ngữ nội bộ: [liệt kê nếu có]

FORMAT:
- Bảng chính: # | Thuật ngữ | Viết tắt | Định nghĩa (VI) | Definition (EN) | Ví dụ sử dụng | Xuất hiện trong Skill
- Phân nhóm theo 9 khía cạnh + 1 nhóm "Chung"
- Quick Reference Card: 1 trang A4, chỉ chứa viết tắt + nghĩa ngắn
- Thuật ngữ cơ bản ban đầu: ~100-150 terms phổ biến trong kinh doanh
- Để trống section "Thuật ngữ nội bộ DN" để chủ DN bổ sung

TONE: Reference material — ngắn gọn, chính xác, dễ tra cứu.
LENGTH: 10-15 trang A4 (bao gồm ~150 terms ban đầu).
```

---

#### Ghi chú triển khai Orchestrator

**Flow tổng thể:**
```
START → [1] Intake → [2] Maturity Scoring → [3] Scope Assessment → [4] Directory Scaffold → [5] Execution Flow → [6] Gọi 12 skill con → [7] Quality Checklist → [8] Handover Report → END
```

**Dependencies nội bộ:**
- `scope-assessment.md` phụ thuộc `intake-questionnaire.md` + `maturity-scoring.md`
- `execution-flow.md` phụ thuộc `scope-assessment.md`
- `directory-scaffold.md` phụ thuộc `scope-assessment.md`
- `quality-checklist.md` phụ thuộc `directory-scaffold.md`
- `handover-report.md` phụ thuộc `quality-checklist.md`
- `master-glossary.md` độc lập — tạo sớm, cập nhật liên tục

---

### VIII.2 — BP Governance (Quản Trị & Pháp Lý)

> **Tầng 1: Nền Móng** — Đây là skill đầu tiên được chạy, thiết lập nền tảng pháp lý và quản trị cho mọi hoạt động DN.

#### A. Giải thích thư mục

**BP Governance** xây dựng toàn bộ "bộ khung xương pháp lý" của doanh nghiệp — từ giấy tờ thành lập, cấu trúc quản trị, đến hợp đồng mẫu và tuân thủ. Không có tầng này, mọi hoạt động kinh doanh đều xây trên cát.

Skill này tạo ra 19 tài liệu chia thành 4 nhóm:

| Nhóm | Tên | Số files | Mô tả |
|------|-----|----------|-------|
| 00.1 | Hồ sơ pháp lý | 6 | Giấy tờ gốc, giấy phép, cổ đông, tuân thủ |
| 00.2 | Quản trị | 5 | Quy chế HĐQT/BGĐ, phân quyền, rủi ro, đạo đức |
| 00.3 | Hợp đồng mẫu | 5 | Templates hợp đồng chuẩn: lao động, dịch vụ, NDA, đại lý, hợp tác |
| 00.4 | Bảo hiểm & Tuân thủ | 3 | Bảo hiểm DN, bảo vệ dữ liệu, lịch gia hạn |

**Tại sao quan trọng:**

- **ISO 9001:2015** — Clause 4.1 (Context of Organization), 5.1 (Leadership), 7.5 (Documented Information) đều yêu cầu nền tảng quản trị rõ ràng.
- **EOS/Traction** — "Accountability Chart" bắt đầu từ cấu trúc quản trị cấp cao nhất.
- **E-Myth** — "Work ON your business" bắt đầu bằng việc xây dựng "Legal & Organizational Foundation".
- **McKinsey 7S** — "Structure" và "Systems" là 2 trong 7 yếu tố cần alignment, bắt đầu từ governance.
- **Luật Doanh nghiệp Việt Nam 2020** — Quy định bắt buộc về điều lệ, ĐKKD, quy chế quản trị cho từng loại hình DN.

#### B. Danh sách file sẽ tạo

**00.1 — Hồ sơ pháp lý (Legal Foundation)**

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 1 | `dieu-le-cong-ty.md` | POL | Điều lệ công ty — văn bản gốc quy định tổ chức, hoạt động, quyền & nghĩa vụ thành viên/cổ đông |
| 2 | `dkkd-scan-checklist.md` | FRM | Checklist hồ sơ ĐKKD — danh sách giấy tờ cần scan lưu trữ + metadata |
| 3 | `danh-sach-giay-phep-con.md` | FRM | Danh mục tất cả giấy phép con/chứng chỉ ngành — tình trạng, hạn, cơ quan cấp |
| 4 | `thoa-thuan-co-dong.md` | POL | Thỏa thuận cổ đông (Shareholders Agreement) — vesting, exit, dilution, voting |
| 5 | `bb-hop-hdqt-template.md` | FRM | Template biên bản họp HĐQT/HĐTV — chuẩn format, nội dung bắt buộc |
| 6 | `checklist-tuan-thu-phap-ly.md` | FRM | Checklist tuân thủ pháp lý định kỳ — hàng tháng/quý/năm |

**00.2 — Quản trị (Corporate Governance)**

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 7 | `quy-che-hdqt.md` | POL | Quy chế hoạt động HĐQT/HĐTV — thẩm quyền, quy trình họp, biểu quyết |
| 8 | `quy-che-bgd.md` | POL | Quy chế BGĐ — phân công, ủy quyền, giới hạn quyết định |
| 9 | `ma-tran-phan-quyen-raci.md` | FRM | Ma trận phân quyền quyết định (RACI) — ai Responsible, Accountable, Consulted, Informed |
| 10 | `chinh-sach-quan-ly-rui-ro.md` | POL | Chính sách quản lý rủi ro — framework nhận diện, đánh giá, xử lý rủi ro |
| 11 | `quy-tac-dao-duc-kinh-doanh.md` | POL | Quy tắc đạo đức kinh doanh (Code of Ethics) — COI, anti-bribery, whistleblower |

**00.3 — Hợp đồng mẫu (Contract Templates)**

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 12 | `hd-lao-dong-mau.md` | FRM | Hợp đồng lao động mẫu — theo Bộ luật Lao động 2019, đủ loại: thử việc, xác định, không xác định |
| 13 | `hd-dich-vu-mau.md` | FRM | Hợp đồng dịch vụ mẫu — cho B2B, freelancer, outsource |
| 14 | `nda-mau.md` | FRM | Thỏa thuận bảo mật (NDA) — one-way, mutual, cho nhân sự & đối tác |
| 15 | `hd-dai-ly-mau.md` | FRM | Hợp đồng đại lý/phân phối — commission, territory, exclusivity |
| 16 | `hd-hop-tac-kinh-doanh-mau.md` | FRM | Hợp đồng hợp tác kinh doanh (BCC) — góp vốn, phân lợi nhuận, quản lý chung |

**00.4 — Bảo hiểm & Tuân thủ (Insurance & Compliance)**

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 17 | `danh-muc-bao-hiem-dn.md` | FRM | Danh mục bảo hiểm DN — loại bảo hiểm, nhà cung cấp, mức coverage, premium, hạn |
| 18 | `chinh-sach-bao-ve-du-lieu.md` | POL | Chính sách bảo vệ dữ liệu (Data Protection Policy) — PDPA, thu thập, lưu trữ, xóa |
| 19 | `lich-gia-han-giay-phep.md` | FRM | Lịch gia hạn giấy phép & chứng chỉ — calendar view, alert trước 60/30/15 ngày |

#### C. Ma trận phân quyền

**00.1 — Hồ sơ pháp lý**

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| Điều lệ công ty | Luật sư + AI draft | HĐQT/HĐTV | Toàn công ty | HĐQT + Luật sư |
| ĐKKD scan checklist | Admin/Kế toán | Giám đốc | Admin, Kế toán, Luật sư | Admin |
| Danh sách giấy phép con | Admin/Pháp chế | Giám đốc | Toàn công ty | Pháp chế, Admin |
| Thỏa thuận cổ đông | Luật sư | Tất cả cổ đông | Cổ đông, HĐQT | Luật sư + HĐQT |
| BB họp HĐQT template | AI + Thư ký | Chủ tịch HĐQT | HĐQT, BGĐ | Thư ký HĐQT |
| Checklist tuân thủ pháp lý | AI + Pháp chế | Giám đốc | BGĐ, Pháp chế, Admin | Pháp chế |

**00.2 — Quản trị**

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| Quy chế HĐQT | Luật sư + AI draft | HĐQT | HĐQT, BGĐ | HĐQT + Luật sư |
| Quy chế BGĐ | Giám đốc + AI draft | HĐQT | BGĐ, Trưởng phòng | Giám đốc |
| Ma trận phân quyền RACI | AI + Giám đốc | HĐQT/Giám đốc | Toàn công ty | Giám đốc |
| Chính sách quản lý rủi ro | AI + Giám đốc | HĐQT | BGĐ, Trưởng phòng | Giám đốc |
| Quy tắc đạo đức kinh doanh | AI + HR + Giám đốc | HĐQT | Toàn công ty | HR + Giám đốc |

**00.3 — Hợp đồng mẫu**

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| HĐ lao động mẫu | Luật sư + AI draft | Giám đốc + Luật sư | HR, BGĐ | Luật sư |
| HĐ dịch vụ mẫu | Luật sư + AI draft | Giám đốc | Sales, BGĐ | Luật sư |
| NDA mẫu | Luật sư + AI draft | Giám đốc | Toàn công ty | Luật sư |
| HĐ đại lý mẫu | Luật sư + AI draft | Giám đốc + Sales Director | Sales, BGĐ | Luật sư + Sales |
| HĐ hợp tác kinh doanh | Luật sư + AI draft | HĐQT/Giám đốc | BGĐ, Pháp chế | Luật sư + HĐQT |

**00.4 — Bảo hiểm & Tuân thủ**

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| Danh mục bảo hiểm DN | Admin/Kế toán + AI | Giám đốc + CFO | Admin, Kế toán, BGĐ | Admin |
| Chính sách bảo vệ dữ liệu | AI + IT/Pháp chế | Giám đốc | Toàn công ty | IT + Pháp chế |
| Lịch gia hạn giấy phép | Admin + AI | Giám đốc | Admin, Pháp chế, Kế toán | Admin |

#### D. Prompts cho từng file

---

##### PROMPT 01: Điều lệ công ty (Company Charter / Articles of Association)

**Mô tả:**
Văn bản pháp lý nền tảng quy định tổ chức và hoạt động của công ty. Theo Luật Doanh nghiệp 2020, điều lệ là tài liệu bắt buộc khi đăng ký DN. File này tạo ra bản điều lệ chuẩn, customize theo loại hình và đặc thù DN.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Loại hình DN? (TNHH 1TV / TNHH 2+TV / Cổ phần / Hợp danh)
2. Vốn điều lệ? Tỷ lệ góp vốn của từng thành viên/cổ đông?
3. Ngành nghề kinh doanh chính? (mã ngành CPC/VSIC)
4. Cơ cấu quản lý hiện tại? (HĐQT + BGĐ / Chủ tịch + GĐ / GĐ duy nhất)
5. Có điều khoản đặc biệt nào cần đưa vào? (VD: vesting cổ phần, quyền phủ quyết, điều kiện chuyển nhượng)
6. DN đã có điều lệ cũ cần cập nhật hay tạo mới hoàn toàn?

**Template gợi ý:**
Cấu trúc điều lệ chuẩn theo Luật DN 2020:
- **Chương I** — Quy định chung: Tên, trụ sở, ngành nghề, vốn điều lệ, người đại diện
- **Chương II** — Thành viên/Cổ đông: Quyền, nghĩa vụ, góp vốn, chuyển nhượng
- **Chương III** — Cơ cấu tổ chức quản lý: HĐQT/HĐTV, BGĐ, Ban kiểm soát
- **Chương IV** — Cuộc họp & Ra quyết định: Triệu tập, quorum, biểu quyết
- **Chương V** — Tài chính: Năm tài chính, phân phối lợi nhuận, quỹ dự phòng
- **Chương VI** — Giải thể, phá sản, tổ chức lại
- **Chương VII** — Điều khoản thi hành

Confirm cấu trúc trước khi tạo.

**Prompt tạo file:**
```
Tạo Điều lệ công ty (Articles of Association) cho doanh nghiệp.

CONTEXT:
- Loại hình: [TNHH 1TV / TNHH 2+TV / Cổ phần / Hợp danh]
- Vốn điều lệ: [số tiền] — Tỷ lệ góp: [chi tiết từng thành viên/cổ đông]
- Ngành nghề: [mã ngành + mô tả]
- Cơ cấu quản lý: [mô tả]
- Điều khoản đặc biệt: [liệt kê]
- Cơ sở pháp lý: Luật Doanh nghiệp 2020 (Luật số 59/2020/QH14)

FORMAT:
- Chia chương rõ ràng, đánh số điều liên tục (Điều 1, 2, 3...)
- Ngôn ngữ pháp lý chuẩn mực nhưng dễ hiểu
- Highlight các điều khoản customize (khác chuẩn) bằng [NOTE]
- Footer: "Điều lệ này có hiệu lực kể từ ngày ký"
- Phần ký: Chữ ký tất cả thành viên/cổ đông sáng lập

TONE: Pháp lý chính thức, nghiêm túc.
LENGTH: 15-25 trang A4 tùy loại hình DN.

LƯU Ý: Đây là template tham khảo. DN CẦN nhờ luật sư rà soát trước khi sử dụng chính thức.
```

---

##### PROMPT 02: ĐKKD Scan Checklist (Checklist hồ sơ đăng ký kinh doanh)

**Mô tả:**
Checklist giúp DN rà soát, scan, lưu trữ số hóa toàn bộ hồ sơ pháp lý gốc. Đảm bảo không thiếu giấy tờ nào, mỗi bản scan đều có metadata đầy đủ.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Loại hình DN? (ảnh hưởng danh sách giấy tờ cần có)
2. DN đã hoạt động bao lâu? (DN lâu năm có nhiều giấy tờ bổ sung/thay đổi)
3. Có chi nhánh/văn phòng đại diện không?
4. Lưu trữ số ở đâu? (Google Drive / NAS / SharePoint)
5. Naming convention cho file scan? (VD: DKKD_2024_v1.pdf)

**Prompt tạo file:**
```
Tạo ĐKKD Scan Checklist — checklist rà soát & số hóa hồ sơ pháp lý.

CONTEXT:
- Loại hình DN: [loại hình]
- Năm thành lập: [năm] — Số lần thay đổi ĐKKD: [số]
- Chi nhánh: [có/không] — Số lượng: [số]
- Storage: [Google Drive / NAS / SharePoint]
- Naming: [convention]

FORMAT:
- Bảng checklist: checkbox ☐ cho mỗi mục
- Phân 5 nhóm: (A) Thành lập, (B) Thay đổi, (C) Giấy phép con, (D) Thuế, (E) Khác
- Mỗi mục: Tên | Số hiệu | Ngày cấp | Cơ quan | Hạn | Bản gốc ☐ | Scan ☐ | Link
- Hướng dẫn scan: 300dpi, PDF/A, naming = [Loại]_[Số]_[Ngày].pdf
- Tổng kết: __/__ giấy tờ đã đủ, __/__ đã scan

TONE: Hành chính, rõ ràng, dạng form.
LENGTH: 3-5 trang A4.
```

---

##### PROMPT 03: Danh sách giấy phép con (Sub-licenses & Permits Registry)

**Mô tả:**
Danh mục tổng hợp tất cả giấy phép con, chứng chỉ hành nghề, điều kiện kinh doanh mà DN cần có ngoài ĐKKD. Cập nhật tình trạng, hạn, cơ quan quản lý.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Ngành nghề kinh doanh chính & phụ? (mỗi ngành có giấy phép khác nhau)
2. Có hoạt động nào thuộc "ngành nghề kinh doanh có điều kiện" không? (Phụ lục IV Luật Đầu tư)
3. Có xuất nhập khẩu không? Có hoạt động liên quan PCCC, ATTP, Môi trường không?
4. Địa bàn hoạt động? (mỗi tỉnh/thành có yêu cầu riêng)

**Prompt tạo file:**
```
Tạo Danh sách giấy phép con (Sub-licenses & Permits Registry).

CONTEXT:
- DN: [Tên] — Ngành: [ngành chính + phụ]
- Ngành có điều kiện: [Có/Không] — Chi tiết: [liệt kê]
- XNK: [Có/Không] — PCCC: [Có/Không] — ATTP: [Có/Không] — Môi trường: [Có/Không]
- Địa bàn: [tỉnh/thành]

FORMAT:
- Registry table: # | Giấy phép | Cơ quan | Số | Ngày cấp | Hạn | Status (🟢🟡🔴) | Owner | Notes
- Alert section: Sắp hết hạn trong 90 ngày → highlight đỏ
- Phân nhóm theo lĩnh vực
- Quy trình gia hạn tóm tắt: Loại | Hồ sơ cần | Thời gian | Chi phí | Nộp tại
- Để trống để DN điền thông tin thực tế

TONE: Hành chính, chuẩn mực.
LENGTH: 3-5 trang A4.
```

---

##### PROMPT 04: Thỏa thuận cổ đông (Shareholders Agreement)

**Mô tả:**
Văn bản pháp lý bổ sung cho Điều lệ, quy định chi tiết mối quan hệ giữa các cổ đông/thành viên: vesting, exit mechanism, anti-dilution, drag-along, tag-along, deadlock resolution. Đặc biệt quan trọng cho startup và DN có nhiều cổ đông.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Có bao nhiêu cổ đông/thành viên? Tỷ lệ sở hữu mỗi người?
2. Có cổ đông nào là nhà đầu tư tài chính (không điều hành) không?
3. Có vesting schedule cho founder/key person không? (VD: 4 năm, cliff 1 năm)
4. Có kế hoạch gọi vốn thêm không? (ảnh hưởng anti-dilution clause)
5. Deadlock resolution: Muốn dùng cơ chế nào? (Russian roulette / Texas shoot-out / Mediation)
6. DN đã có thỏa thuận cổ đông cũ chưa?

**Prompt tạo file:**
```
Tạo Thỏa thuận cổ đông (Shareholders Agreement).

CONTEXT:
- DN: [Tên] — Loại hình: [loại]
- Cổ đông/Thành viên: [Tên - Tỷ lệ - Vai trò (điều hành/tài chính)]
- Vesting: [Có/Không] — Schedule: [chi tiết]
- Kế hoạch gọi vốn: [Có/Không]
- Deadlock mechanism: [Russian roulette / Texas shoot-out / Mediation]

FORMAT:
- Chia phần rõ ràng, đánh số điều liên tục
- Bảng tóm tắt cổ đông: Tên | % | Loại cổ phần | Vai trò | Vesting status
- Ngôn ngữ pháp lý song ngữ Việt-Anh cho thuật ngữ quan trọng
- Phụ lục: Vesting Schedule, Reserved Matters List, Cap Table template

TONE: Pháp lý chính thức, chặt chẽ.
LENGTH: 12-20 trang A4.

LƯU Ý: Template tham khảo — CẦN luật sư rà soát trước khi ký kết.
```

---

##### PROMPT 05: Biên bản họp HĐQT Template (Board Meeting Minutes Template)

**Mô tả:**
Template chuẩn hóa cho biên bản họp HĐQT/HĐTV. Đảm bảo mọi cuộc họp đều được ghi nhận đúng format pháp lý, đủ nội dung bắt buộc theo Luật DN 2020.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Loại hình DN? (quy định biên bản họp khác nhau cho TNHH vs Cổ phần)
2. Số thành viên HĐQT/HĐTV?
3. Có thư ký HĐQT chuyên trách không?
4. Cuộc họp thường có bao nhiêu nội dung/quyết định?
5. Cần bilingual (Việt-Anh) không? (cho DN có cổ đông nước ngoài)

**Prompt tạo file:**
```
Tạo Template Biên bản họp HĐQT/HĐTV.

CONTEXT:
- Loại hình DN: [loại] — Loại cuộc họp: [HĐQT / HĐTV / Đại hội cổ đông]
- Số thành viên: [số]
- Bilingual: [Có/Không]
- Cơ sở pháp lý: Luật DN 2020, Điều [số điều tương ứng]

FORMAT:
- Template dạng form: các trường để điền được đánh dấu [___]
- Header chuyên nghiệp: Logo placeholder, thông tin DN
- Bảng tham dự: Tên | Chức danh | % biểu quyết | Có mặt/Ủy quyền
- Mỗi nội dung: Số TT | Nội dung | Người trình bày | Kết quả biểu quyết (Đồng ý __ / Không __ / Trắng __)
- Footer: Chữ ký chủ tọa & thư ký, dòng xác nhận pháp lý
- Phụ lục: Checklist nội dung bắt buộc theo luật

TONE: Pháp lý-hành chính, trang trọng.
LENGTH: 3-4 trang A4.
```

---

##### PROMPT 06: Checklist tuân thủ pháp lý (Legal Compliance Checklist)

**Mô tả:**
Checklist định kỳ (tháng/quý/năm) giúp DN rà soát tuân thủ pháp lý. Bao gồm: thuế, lao động, bảo hiểm xã hội, PCCC, môi trường, báo cáo tài chính, và các nghĩa vụ pháp lý khác.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Ngành nghề? (mỗi ngành có compliance riêng)
2. Quy mô nhân sự? (ảnh hưởng nghĩa vụ lao động, BHXH)
3. Có hoạt động XNK, ngoại hối không?
4. Đã bị thanh tra/phạt lần nào chưa? (xác định vùng rủi ro)
5. Ai sẽ chịu trách nhiệm check hàng tháng?

**Prompt tạo file:**
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

##### PROMPT 07: Quy chế HĐQT (Board of Directors Regulations)

**Mô tả:**
Quy chế nội bộ quy định cách thức hoạt động, thẩm quyền, quy trình ra quyết định của HĐQT/HĐTV. Bổ sung chi tiết cho Điều lệ, phục vụ quản trị thực tế hàng ngày.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Loại hình DN & cơ cấu quản trị?
2. HĐQT/HĐTV có bao nhiêu người? Có thành viên độc lập không?
3. Tần suất họp: hàng tháng / hàng quý?
4. Có ủy ban chuyên trách không? (Kiểm toán, Nhân sự-Lương thưởng, Chiến lược)
5. Giới hạn quyết định tài chính: CEO được quyết đến bao nhiêu trước khi cần HĐQT duyệt?

**Prompt tạo file:**
```
Tạo Quy chế HĐQT/HĐTV (Board Regulations).

CONTEXT:
- Loại hình: [loại] — Số thành viên HĐQT: [số] — Thành viên độc lập: [Có/Không]
- Tần suất họp: [tháng/quý]
- Ủy ban: [liệt kê nếu có]
- Giới hạn tài chính CEO: [số tiền]
- Cơ sở: Luật DN 2020 + Điều lệ công ty

FORMAT:
- Chia chương, đánh số điều
- Bảng phân quyền tài chính: Loại quyết định | CEO | CFO | HĐQT | ĐHCĐ + Mức tiền
- Reserved Matters list: Danh sách quyết định PHẢI qua HĐQT
- Quy trình ra quyết định: Flowchart mermaid

TONE: Chính thức, nội bộ, rõ ràng.
LENGTH: 8-12 trang A4.
```

---

##### PROMPT 08: Quy chế BGĐ (Executive Management Regulations)

**Mô tả:**
Quy chế hoạt động của Ban Giám đốc (CEO, các Phó GĐ, Giám đốc chức năng). Quy định phân công, ủy quyền, giới hạn quyết định, quy trình phối hợp giữa các thành viên BGĐ.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. BGĐ gồm bao nhiêu người? Chức danh cụ thể?
2. CEO có phải là Chủ tịch HĐQT không? (kiêm nhiệm?)
3. Phân công lĩnh vực phụ trách của mỗi Phó GĐ?
4. Giới hạn ký duyệt tài chính của từng cấp BGĐ?
5. Quy trình ủy quyền khi vắng mặt?

**Prompt tạo file:**
```
Tạo Quy chế BGĐ (Executive Management Regulations).

CONTEXT:
- BGĐ: [liệt kê chức danh + tên]
- CEO kiêm Chủ tịch: [Có/Không]
- Phân công: [VD: Phó GĐ Kinh doanh phụ trách Sales+Marketing, Phó GĐ Vận hành phụ trách Ops+HR]
- Giới hạn ký: CEO [số] | Phó GĐ [số] | GĐ chức năng [số]

FORMAT:
- Đánh số điều liên tục
- Bảng phân quyền: Loại quyết định | GĐ CN | Phó GĐ | CEO | HĐQT
- Bảng ủy quyền: Người ủy | Người được ủy | Phạm vi | Thời hạn
- Sơ đồ báo cáo: Mermaid org chart

TONE: Nội bộ, chính thức.
LENGTH: 6-10 trang A4.
```

---

##### PROMPT 09: Ma trận phân quyền RACI (Decision Authority Matrix)

**Mô tả:**
Ma trận RACI (Responsible-Accountable-Consulted-Informed) cho tất cả quyết định quan trọng trong DN. Xác định rõ ai làm, ai chịu trách nhiệm, ai cần hỏi ý kiến, ai cần thông báo — cho mỗi loại quyết định.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Sơ đồ tổ chức hiện tại? (các cấp quản lý)
2. Danh sách quyết định quan trọng thường gặp? (VD: tuyển dụng, chi tiêu, ký HĐ, ra sản phẩm mới...)
3. Hiện tại có vấn đề gì về phân quyền? (VD: CEO bottleneck, không rõ ai quyết)
4. Muốn phân theo lĩnh vực hay theo cấp quyết định?

**Prompt tạo file:**
```
Tạo Ma trận phân quyền RACI (Decision Authority Matrix).

CONTEXT:
- Cơ cấu tổ chức: [mô tả hoặc link OrgChart]
- Số cấp quản lý: [số] — Danh sách chức danh: [liệt kê]
- Pain points hiện tại: [VD: CEO phải duyệt mọi thứ]
- Phân loại: [theo lĩnh vực / theo cấp / cả hai]

FORMAT:
- Legend: R=Responsible (Thực hiện), A=Accountable (Chịu trách nhiệm), C=Consulted (Tham vấn), I=Informed (Thông báo)
- Ma trận per domain: 6-8 bảng (Tài chính, Nhân sự, Kinh doanh, Marketing, Vận hành, IT, Pháp lý, Chiến lược)
- Mỗi bảng: 8-15 quyết định × 6-8 vai trò
- Mỗi ô: R / A / C / I / — (không liên quan)
- Quy tắc: Highlight nếu 1 hàng thiếu A, hoặc 1 cột có quá nhiều A (bottleneck)
- Summary: Bảng tổng kết workload per role

TONE: Structured, analytical.
LENGTH: 8-12 trang A4.
```

---

##### PROMPT 10: Chính sách quản lý rủi ro (Risk Management Policy)

**Mô tả:**
Framework toàn diện để nhận diện, đánh giá, xử lý và giám sát rủi ro ở cấp DN. Theo chuẩn ISO 31000:2018, customize cho DN Việt Nam.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Ngành nghề & quy mô? (xác định profile rủi ro)
2. Đã từng gặp sự cố nghiêm trọng nào chưa? (VD: mất data, kiện tụng, sự cố sản xuất)
3. Có bộ phận quản lý rủi ro riêng không?
4. Khẩu vị rủi ro (Risk Appetite): DN thuộc loại risk-averse hay risk-taking?
5. Có cần risk register template kèm theo không?

**Prompt tạo file:**
```
Tạo Chính sách quản lý rủi ro (Risk Management Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Quy mô: [nhân sự, doanh thu]
- Sự cố đã gặp: [liệt kê hoặc "chưa"]
- Bộ phận RM: [Có/Không]
- Risk Appetite: [Conservative / Moderate / Aggressive]
- Chuẩn tham khảo: ISO 31000:2018

FORMAT:
- Chia phần rõ ràng, có mục lục
- Risk Matrix 5×5: Likelihood × Impact, color-coded (Green/Yellow/Orange/Red)
- Risk Categories: 6 loại với ví dụ cụ thể cho ngành DN
- Treatment strategies: Bảng: Risk | Strategy | Action | Owner | Timeline | KRI
- Risk Register template: # | Mô tả | Loại | L | I | Score | Strategy | Owner | Status
- Quy trình báo cáo: Flowchart khi phát hiện rủi ro mới

TONE: Chuyên nghiệp, ISO-aligned, thực tế.
LENGTH: 10-15 trang A4.
```

---

##### PROMPT 11: Quy tắc đạo đức kinh doanh (Code of Business Ethics)

**Mô tả:**
Bộ quy tắc ứng xử và đạo đức kinh doanh cho toàn bộ nhân sự. Bao gồm: xung đột lợi ích (COI), chống hối lộ-tham nhũng, bảo mật, tố giác vi phạm (whistleblower), trách nhiệm xã hội.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. DN có giá trị cốt lõi (Core Values) rõ ràng chưa?
2. Ngành có rủi ro đạo đức đặc thù không? (VD: dược phẩm, tài chính, xây dựng)
3. Có cần cơ chế tố giác ẩn danh (Whistleblower hotline) không?
4. Có làm việc với chính phủ/khu vực công không? (tăng yêu cầu anti-bribery)
5. Có nhân sự/đối tác nước ngoài không? (cần comply FCPA, UK Bribery Act?)

**Prompt tạo file:**
```
Tạo Quy tắc đạo đức kinh doanh (Code of Business Ethics).

CONTEXT:
- DN: [Tên] — Core Values: [liệt kê]
- Ngành: [ngành] — Rủi ro đặc thù: [liệt kê]
- Whistleblower: [Có/Không] — Kênh: [email / hotline / form ẩn danh]
- Đối tác khu vực công: [Có/Không]
- Compliance quốc tế: [FCPA / UK Bribery Act / Không]

FORMAT:
- Mở đầu bằng thông điệp CEO (1/2 trang, giọng cá nhân, cam kết)
- Chia phần rõ ràng, mỗi phần có: Nguyên tắc → Ví dụ cụ thể → Câu hỏi tự kiểm
- "Bài test 5 câu hỏi" cho mỗi tình huống: Có hợp pháp không? → Có đúng chính sách không? → Sẽ thấy thế nào nếu lên báo? → Có công bằng với các bên không? → Bạn có tự hào về quyết định này không?
- Phụ lục: Form COI + Form Whistleblower + FAQ 10 câu
- Design: Thân thiện, dễ đọc — không quá luật sư

TONE: Trang trọng nhưng gần gũi, truyền cảm hứng hành xử đúng.
LENGTH: 12-18 trang A4.
```

---

##### PROMPT 12: Hợp đồng lao động mẫu (Employment Contract Template)

**Mô tả:**
Template hợp đồng lao động chuẩn theo Bộ luật Lao động 2019 (có hiệu lực từ 01/01/2021). Bao gồm 3 loại: thử việc, xác định thời hạn, không xác định thời hạn.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Loại hợp đồng cần tạo? (Thử việc / Xác định / Không xác định / Tất cả)
2. Ngành nghề? (ảnh hưởng điều kiện lao động đặc thù)
3. Có chế độ bổ sung ngoài luật không? (VD: bảo hiểm sức khỏe private, thưởng cổ phiếu, remote working)
4. Có điều khoản non-compete sau khi nghỉ việc không?
5. Thang lương, bảng lương đã có chưa?

**Prompt tạo file:**
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

##### PROMPT 13: Hợp đồng dịch vụ mẫu (Service Agreement Template)

**Mô tả:**
Template hợp đồng dịch vụ B2B, dùng cho mua/bán dịch vụ, thuê freelancer, outsource.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. DN là bên cung cấp hay bên mua dịch vụ? (hoặc cả hai?)
2. Loại dịch vụ phổ biến nhất? (tư vấn, IT, marketing, logistics...)
3. Thanh toán: milestone, monthly, completion?
4. Cần SLA (Service Level Agreement) kèm theo không?
5. Có yếu tố quốc tế không? (luật áp dụng, currency, timezone)

**Prompt tạo file:**
```
Tạo Template hợp đồng dịch vụ (Service Agreement).

CONTEXT:
- DN: [Tên] — Vai trò: [Provider / Client / cả hai]
- Loại dịch vụ: [tư vấn / IT / marketing / logistics / khác]
- Thanh toán: [milestone / monthly / completion]
- SLA: [Có/Không]
- Quốc tế: [Có/Không] — Luật áp dụng: [Luật VN / khác]

FORMAT:
- Template form: Trường điền = [___]
- SOW attachment template riêng
- SLA template (nếu có): Metric | Target | Measurement | Penalty
- Bảng giá mẫu: Dịch vụ | Đơn vị | Đơn giá | Ghi chú
- Payment schedule template: Milestone | Deliverable | % | Amount | Due date

TONE: Chuyên nghiệp, cân bằng quyền lợi 2 bên.
LENGTH: 6-8 trang A4 + phụ lục.
```

---

##### PROMPT 14: NDA mẫu (Non-Disclosure Agreement Template)

**Mô tả:**
Template thỏa thuận bảo mật (NDA) — 2 version: one-way (một chiều) và mutual (hai chiều). Dùng cho nhân sự, đối tác, nhà cung cấp, nhà đầu tư.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Cần loại NDA nào? (One-way / Mutual / cả hai)
2. Đối tượng ký: nhân sự / đối tác kinh doanh / nhà đầu tư / freelancer?
3. Thời hạn bảo mật sau khi kết thúc quan hệ? (1 năm / 2 năm / vô thời hạn)
4. Phạm vi thông tin mật: tất cả hay chỉ loại cụ thể?
5. Mức phạt vi phạm: cố định hay tỷ lệ theo thiệt hại?

**Prompt tạo file:**
```
Tạo Template NDA (Non-Disclosure Agreement).

CONTEXT:
- DN: [Tên]
- Loại: [One-way / Mutual / cả hai]
- Đối tượng: [nhân sự / đối tác / nhà đầu tư / freelancer]
- Thời hạn bảo mật: [thời gian sau khi kết thúc]
- Mức phạt: [cố định: VNĐ / tỷ lệ theo thiệt hại]

FORMAT:
- 2 version riêng: One-way + Mutual (nếu chọn cả hai)
- Ngắn gọn, đi thẳng vào vấn đề — NDA không cần dài
- Highlight: Định nghĩa "Thông tin mật" phải RẤT CỤ THỂ
- Appendix: Danh mục loại thông tin mật per department

TONE: Pháp lý, chặt chẽ, ngắn gọn.
LENGTH: 3-4 trang A4 mỗi version.
```

---

##### PROMPT 15: Hợp đồng đại lý mẫu (Agency/Distribution Agreement Template)

**Mô tả:**
Template hợp đồng đại lý/phân phối — quy định commission, territory, exclusivity, quota, termination.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Mô hình phân phối? (Đại lý bán hàng / Nhà phân phối mua đi bán lại / Affiliate)
2. Exclusive hay Non-exclusive?
3. Territory: theo tỉnh/vùng/toàn quốc?
4. Commission structure: % / fixed / tiered?
5. Có quota (chỉ tiêu) bắt buộc không?
6. Sản phẩm/dịch vụ phân phối là gì?

**Prompt tạo file:**
```
Tạo Template hợp đồng đại lý (Agency/Distribution Agreement).

CONTEXT:
- DN: [Tên] — Sản phẩm: [mô tả]
- Mô hình: [Đại lý / Nhà PP / Affiliate]
- Exclusive: [Có/Không]
- Territory: [scope]
- Commission: [structure chi tiết]
- Quota: [Có/Không] — Mức: [chi tiết]

FORMAT:
- Template form: Trường điền = [___]
- Bảng commission: Level | Doanh số từ-đến | % Commission
- Territory map placeholder
- KPI dashboard: Metric | Target | Actual | Achievement %
- Quy trình đặt hàng: Flowchart

TONE: Thương mại, cân bằng, rõ ràng.
LENGTH: 8-12 trang A4 + phụ lục.
```

---

##### PROMPT 16: Hợp đồng hợp tác kinh doanh mẫu (Business Cooperation Contract - BCC)

**Mô tả:**
Template BCC — hợp đồng hợp tác kinh doanh không thành lập pháp nhân mới. Quy định góp vốn, phân công, phân lợi nhuận, quản lý chung.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Mục đích hợp tác? (dự án cụ thể / kinh doanh chung / R&D / market entry)
2. Các bên góp gì? (tiền / tài sản / công nghệ / nhân lực / thương hiệu)
3. Tỷ lệ phân chia lợi nhuận/lỗ?
4. Ai quản lý hoạt động hàng ngày?
5. Thời hạn hợp tác? Điều kiện kết thúc?
6. Có đối tác nước ngoài không? (cần tuân thủ Luật Đầu tư)

**Prompt tạo file:**
```
Tạo Template BCC (Business Cooperation Contract).

CONTEXT:
- Mục đích: [mô tả]
- Các bên: [Tên + Góp vốn/tài sản/nguồn lực]
- Tỷ lệ lợi nhuận/lỗ: [chi tiết]
- Quản lý: [Bên A / Bên B / Ban điều hành chung]
- Đối tác nước ngoài: [Có/Không]
- Cơ sở pháp lý: Bộ luật Dân sự 2015, Luật Đầu tư 2020 (nếu có yếu tố nước ngoài)

FORMAT:
- Đánh số điều rõ ràng
- Bảng góp vốn: Bên | Loại góp | Giá trị | Tỷ lệ % | Thời hạn góp
- Bảng phân công: Mảng | Responsible | Accountable | Budget
- P&L sharing: Formula rõ ràng + ví dụ tính
- Exit mechanism: Điều kiện rút, mua lại phần góp, thanh lý

TONE: Pháp lý, chặt chẽ, cân bằng.
LENGTH: 10-15 trang A4.
```

---

##### PROMPT 17: Danh mục bảo hiểm DN (Corporate Insurance Portfolio)

**Mô tả:**
Danh mục tổng hợp tất cả bảo hiểm DN đang có hoặc cần mua.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Hiện đang có bảo hiểm gì? (liệt kê)
2. Ngành nghề & tài sản chính? (xác định rủi ro cần bảo hiểm)
3. Quy mô nhân sự? (ảnh hưởng BH nhân sự)
4. Budget bảo hiểm hàng năm?
5. Có hoạt động quốc tế không? (cần BH quốc tế)

**Prompt tạo file:**
```
Tạo Danh mục bảo hiểm DN (Corporate Insurance Portfolio).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số] — Tài sản chính: [liệt kê]
- BH hiện có: [liệt kê]
- Budget: [số/năm]
- Quốc tế: [Có/Không]

FORMAT:
- Portfolio table: Đầy đủ cột như template
- BH bắt buộc theo luật VN: BHXH, BHYT, BH thất nghiệp, BH cháy nổ (nếu áp dụng)
- BH khuyến nghị: Tùy ngành — bảng mapping Ngành → Loại BH khuyến nghị
- Gap Analysis: Risk | Current Coverage | Gap | Recommended | Est. Premium
- Renewal calendar: Gantt-style hoặc list theo tháng
- Total Cost of Insurance: Pie chart data

TONE: Quản lý, thực tế.
LENGTH: 4-6 trang A4.
```

---

##### PROMPT 18: Chính sách bảo vệ dữ liệu (Data Protection Policy)

**Mô tả:**
Chính sách bảo vệ dữ liệu cá nhân — tuân thủ Nghị định 13/2023/NĐ-CP (Bảo vệ dữ liệu cá nhân Việt Nam) và tham khảo GDPR.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. DN thu thập những loại dữ liệu cá nhân nào? (khách hàng, nhân sự, đối tác)
2. Kênh thu thập: website, app, cửa hàng, telesales, social media?
3. Dữ liệu lưu ở đâu? (server VN / cloud nước ngoài)
4. Có chia sẻ dữ liệu với bên thứ 3 không? (quảng cáo, analytics, đối tác)
5. Có DPO (Data Protection Officer) hoặc người phụ trách không?
6. Có hoạt động xuyên biên giới không? (cần tuân thủ GDPR?)

**Prompt tạo file:**
```
Tạo Chính sách bảo vệ dữ liệu (Data Protection Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Dữ liệu thu thập: [loại: KH, NV, ĐT]
- Kênh: [website / app / offline / social]
- Storage: [server VN / cloud / hybrid]
- Chia sẻ bên thứ 3: [Có/Không] — [liệt kê]
- DPO: [Có/Không]
- Xuyên biên giới: [Có/Không]
- Cơ sở pháp lý: NĐ 13/2023/NĐ-CP + GDPR (nếu có yếu tố EU)

FORMAT:
- Chia phần rõ ràng, có mục lục
- Data Mapping table: Loại DL | Nguồn | Mục đích | CSPL | Thời hạn lưu | Chia sẻ
- Quyền chủ thể: Bảng quyền + cách thực hiện + SLA phản hồi
- Breach Response flowchart: Phát hiện → 72h → Thông báo → Khắc phục
- Phụ lục: Consent form, Data Processing Agreement template, Breach report template

TONE: Compliance — nghiêm túc, minh bạch, bảo vệ quyền lợi.
LENGTH: 12-18 trang A4.
```

---

##### PROMPT 19: Lịch gia hạn giấy phép (License Renewal Calendar)

**Mô tả:**
Calendar view tổng hợp tất cả giấy phép, chứng chỉ, hợp đồng bảo hiểm, đăng ký cần gia hạn định kỳ. Alert system trước 90/60/30/15 ngày.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Tổng hợp từ file nào? (Danh sách giấy phép con + Danh mục bảo hiểm + ĐKKD)
2. Ai nhận alert? (Admin / Pháp chế / Giám đốc)
3. Alert qua kênh nào? (Email / Calendar / Slack / Zalo)
4. Có budget cho từng lần gia hạn không?

**Prompt tạo file:**
```
Tạo Lịch gia hạn giấy phép (License Renewal Calendar).

CONTEXT:
- Nguồn data: [Giấy phép con + Bảo hiểm + ĐKKD + Hợp đồng]
- Alert recipient: [chức danh]
- Alert channel: [Email / Calendar / Slack / Zalo]
- Budget tracking: [Có/Không]

FORMAT:
- Calendar view: 12 tháng, mỗi ô chứa items hết hạn trong tháng đó
- Registry table: Đầy đủ cột, sort theo ngày hết hạn ascending
- Color coding: 🟢 OK (>90 ngày) | 🟡 Attention (30-90 ngày) | 🟠 Urgent (15-30 ngày) | 🔴 Critical (<15 ngày) | ⚫ Expired
- Alert workflow: Flowchart 4 mốc (90-60-30-15)
- Dashboard summary: KPI cards
- Auto-fill: Từ data các file liên quan trong 01-bb-governance

TONE: Operational, action-oriented.
LENGTH: 3-5 trang A4.
```

---

#### Ghi chú triển khai Governance

**Dependencies:**
- `dieu-le-cong-ty.md` là file gốc — nhiều file khác tham chiếu (quy chế HĐQT, BGĐ, thỏa thuận cổ đông)
- `checklist-tuan-thu-phap-ly.md` tổng hợp nghĩa vụ từ tất cả file khác trong nhóm
- `lich-gia-han-giay-phep.md` tổng hợp từ `danh-sach-giay-phep-con.md` + `danh-muc-bao-hiem-dn.md`
- `ma-tran-phan-quyen-raci.md` sẽ được tham chiếu bởi hầu hết skill con phía sau

**Lưu ý pháp lý:**
> **QUAN TRỌNG**: Tất cả tài liệu pháp lý trong skill này là TEMPLATE THAM KHẢO. Doanh nghiệp CẦN nhờ luật sư chuyên nghiệp rà soát trước khi sử dụng chính thức. AI tạo draft để tiết kiệm 70-80% thời gian, nhưng 20-30% cuối cùng cần chuyên gia pháp lý.

**Thứ tự tạo khuyến nghị:**
1. Điều lệ → 2. ĐKKD Checklist → 3. Giấy phép con → 4. Thỏa thuận cổ đông → 5. BB HĐQT Template
6. Quy chế HĐQT → 7. Quy chế BGĐ → 8. RACI → 9. Risk Management → 10. Code of Ethics
11. HĐ lao động → 12. HĐ dịch vụ → 13. NDA → 14. HĐ đại lý → 15. BCC
16. Bảo hiểm → 17. Data Protection → 18. Checklist tuân thủ → 19. Lịch gia hạn

---

### VIII.3 — BP Strategy (Chiến Lược & Kế Hoạch)

> **Tầng 1: Nền Móng** — Cùng với Governance, Strategy tạo nền tảng định hướng cho toàn bộ hoạt động DN.

#### A. Giải thích thư mục

**BP Strategy** xây dựng toàn bộ "bản đồ chiến lược" của doanh nghiệp — từ bản sắc (ai là chúng ta), phân tích (chúng ta đang ở đâu), kế hoạch (chúng ta đi đâu), đến quản lý rủi ro (nếu xảy ra sự cố thì sao). Không có tầng này, DN hoạt động theo phản xạ thay vì theo chiến lược.

Skill này tạo ra 18 tài liệu chia thành 4 nhóm:

| Nhóm | Tên | Số files | Mô tả |
|------|-----|----------|-------|
| 01.1 | Bản sắc DN | 4 | Company Profile, VMV, Brand Identity, Elevator Pitch |
| 01.2 | Phân tích chiến lược | 5 | SWOT, BMC, Porter, Competitive Landscape, ICP |
| 01.3 | Kế hoạch KD | 5 | Business Plan, OGSM, OKR, BCG Matrix, Roadmap |
| 01.4 | Quản lý rủi ro chiến lược | 4 | Risk Register, Crisis Management, BCP, Scenario Planning |

**Tại sao quan trọng:**

- **ISO 9001:2015** — Clause 4.1 (Understanding the Organization & Context), 6.1 (Actions to Address Risks and Opportunities) yêu cầu DN phải có chiến lược rõ ràng và quản lý rủi ro.
- **EOS/Traction** — Component "Vision" là nền tảng: Core Values → Core Focus → 10-Year Target → Marketing Strategy → 3-Year Picture → 1-Year Plan → Quarterly Rocks.
- **E-Myth** — "Strategic Objective" là bước đầu tiên trong xây dựng DN hoạt động như một franchise: Vision → Purpose → Strategy.
- **McKinsey 7S** — "Strategy" là 1 trong 3 "hard S" (Strategy-Structure-Systems) quyết định alignment toàn tổ chức.
- **Blue Ocean Strategy** — Tạo không gian thị trường mới thay vì cạnh tranh đỏ — cần phân tích chiến lược sâu.

**Mối quan hệ với các skill khác:**
- **Input từ**: 00-Orchestrator (Intake data, Maturity Score), 01-Governance (pháp nhân, cơ cấu quản trị)
- **Output cho**: 03-Finance (mục tiêu tài chính từ Business Plan), 04-People (cơ cấu tổ chức từ Strategy), 06-Sales (ICP, mục tiêu doanh số), 07-Marketing (Brand Identity, positioning), 12-Growth (Roadmap, kế hoạch đầu tư)

#### B. Danh sách file sẽ tạo

**01.1 — Bản sắc DN (Corporate Identity)**

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 1 | `company-profile.md` | MAN | Hồ sơ năng lực công ty — tổng quan DN, lịch sử, năng lực, thành tựu |
| 2 | `tam-nhin-su-menh-gia-tri.md` | POL | Tầm nhìn (Vision), Sứ mệnh (Mission), Giá trị cốt lõi (Core Values) |
| 3 | `brand-identity-guidelines.md` | MAN | Hướng dẫn nhận diện thương hiệu — logo, màu sắc, typography, tone of voice |
| 4 | `elevator-pitch.md` | FRM | Bài giới thiệu ngắn 30-60-90 giây — cho nhiều ngữ cảnh |

**01.2 — Phân tích chiến lược (Strategic Analysis)**

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 5 | `swot-analysis.md` | RPT | Phân tích SWOT + chiến lược kết hợp SO/ST/WO/WT |
| 6 | `business-model-canvas.md` | FRM | Business Model Canvas (BMC) — 9 khối mô hình kinh doanh |
| 7 | `porter-five-forces.md` | RPT | Phân tích 5 áp lực cạnh tranh Porter |
| 8 | `competitive-landscape.md` | RPT | Bản đồ cạnh tranh — đối thủ chính, positioning |
| 9 | `ideal-customer-profile.md` | FRM | Ideal Customer Profile (ICP) & Buyer Persona |

**01.3 — Kế hoạch kinh doanh (Business Planning)**

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 10 | `business-plan.md` | MAN | Kế hoạch kinh doanh tổng thể |
| 11 | `ogsm-framework.md` | FRM | OGSM (Objectives-Goals-Strategies-Measures) — bảng chiến lược 1 trang |
| 12 | `okr-template.md` | FRM | OKR (Objectives & Key Results) — theo quý, cascade |
| 13 | `bcg-matrix.md` | RPT | BCG Matrix — phân loại sản phẩm Stars/Cash Cows/QM/Dogs |
| 14 | `strategic-roadmap.md` | MAN | Lộ trình chiến lược — timeline 1-3-5 năm |

**01.4 — Quản lý rủi ro chiến lược (Strategic Risk Management)**

| # | File | Loại | Mô tả |
|---|------|------|-------|
| 15 | `risk-register.md` | FRM | Sổ đăng ký rủi ro — danh mục, đánh giá, biện pháp, owner |
| 16 | `crisis-management-plan.md` | SOP | Quy trình xử lý khủng hoảng — playbook cho các kịch bản |
| 17 | `business-continuity-plan.md` | SOP | Kế hoạch duy trì kinh doanh liên tục (BCP) |
| 18 | `scenario-planning.md` | RPT | Hoạch định kịch bản — 3 kịch bản lạc quan/cơ sở/bi quan |

#### C. Ma trận phân quyền

**01.1 — Bản sắc DN**

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| Company Profile | Marketing + AI draft | CEO/Giám đốc | Toàn công ty, Đối tác, Khách hàng | Marketing + CEO |
| Tầm nhìn/Sứ mệnh/Giá trị | CEO + HĐQT + AI draft | HĐQT | Toàn công ty | CEO + HĐQT |
| Brand Identity Guidelines | Marketing/Design + AI | CEO + Marketing Director | Toàn công ty, Agency, Đối tác | Marketing/Design |
| Elevator Pitch | CEO + AI draft | CEO | Sales, Marketing, HR (tuyển dụng) | CEO |

**01.2 — Phân tích chiến lược**

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| SWOT Analysis | AI + CEO/Strategy team | CEO + HĐQT | BGĐ, Trưởng phòng | Strategy team |
| Business Model Canvas | AI + CEO | CEO + HĐQT | BGĐ, Investors | CEO |
| Porter Five Forces | AI + Strategy team | CEO | BGĐ, Marketing | Strategy team |
| Competitive Landscape | AI + Marketing + Sales | CEO + Sales Director | Sales, Marketing, BGĐ | Marketing |
| Ideal Customer Profile | AI + Marketing + Sales | CEO + Marketing Director | Sales, Marketing, Product | Marketing + Sales |

**01.3 — Kế hoạch KD**

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| Business Plan | AI + CEO + CFO | HĐQT | BGĐ, Investors, Ngân hàng | CEO + CFO |
| OGSM Framework | AI + CEO | CEO + HĐQT | BGĐ, Trưởng phòng | CEO |
| OKR Template | AI + CEO → cascade xuống | CEO (company) / Directors (dept) | Toàn công ty | Từng cấp sở hữu OKR |
| BCG Matrix | AI + CEO + Product team | CEO | BGĐ, Product, Marketing | CEO + Product |
| Strategic Roadmap | AI + CEO | HĐQT | BGĐ, Trưởng phòng, Investors | CEO |

**01.4 — Quản lý rủi ro chiến lược**

| File | Tạo bởi | Duyệt bởi | Đọc | Sửa |
|------|---------|-----------|-----|-----|
| Risk Register | AI + Strategy/Risk team | CEO + HĐQT | BGĐ, Trưởng phòng | Risk Owner per mục |
| Crisis Management Plan | AI + CEO + PR + Legal | CEO + HĐQT | BGĐ, PR, HR, Legal | CEO + Crisis Team |
| Business Continuity Plan | AI + COO + IT | CEO | BGĐ, IT, Ops, HR | COO + IT |
| Scenario Planning | AI + CEO + CFO | HĐQT | BGĐ | CEO + CFO |

#### D. Prompts cho từng file

---

##### PROMPT 01: Company Profile (Hồ sơ năng lực công ty)

**Mô tả:**
Tài liệu giới thiệu tổng quan doanh nghiệp — dùng gửi đối tác, khách hàng, nhà đầu tư, cơ quan chức năng.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Đối tượng chính sẽ đọc? (đối tác B2B / nhà đầu tư / khách hàng / tuyển dụng / tất cả)
2. DN muốn nhấn mạnh điều gì nhất? (công nghệ / kinh nghiệm / quy mô / giá trị / đội ngũ)
3. Có case study/khách hàng tiêu biểu nào muốn đưa vào?
4. Số liệu key: doanh thu, nhân sự, năm kinh nghiệm, số dự án, số khách hàng?
5. Format mong muốn? (Markdown report / PDF thiết kế / Presentation)
6. Có logo, hình ảnh, video giới thiệu không?

**Prompt tạo file:**
```
Tạo Company Profile (Hồ sơ năng lực công ty).

CONTEXT:
- DN: [Tên đầy đủ] — Tên viết tắt/thương hiệu: [tên]
- Thành lập: [năm] — MST: [số] — Trụ sở: [địa chỉ]
- Ngành: [ngành chính]
- Đối tượng chính: [đối tác B2B / nhà đầu tư / khách hàng / tất cả]
- USP: [điểm khác biệt chính]
- Số liệu key: Doanh thu [số] | Nhân sự [số] | Khách hàng [số] | Dự án [số]
- Case study: [tóm tắt 2-3 case]
- Giải thưởng/Media: [liệt kê]

FORMAT:
- Professional document, có thể convert sang PDF đẹp
- Mỗi section: Header + 1-2 paragraphs + data points
- Infographic-ready: Key numbers dạng "10+ năm | 500+ khách hàng | 50+ nhân sự"
- Logo wall placeholder: [Logo 1] [Logo 2] ...
- Case study format: Challenge → Solution → Result (mỗi case 1/2 trang)
- CTA cuối: Liên hệ hợp tác

TONE: Chuyên nghiệp, tự tin, không khoe khoang. Storytelling nhẹ.
LENGTH: 10-15 trang A4.
```

---

##### PROMPT 02: Tầm nhìn / Sứ mệnh / Giá trị cốt lõi (VMV)

**Mô tả:**
Bộ VMV là kim chỉ nam cho mọi quyết định trong DN. Vision (đi đến đâu), Mission (tại sao tồn tại), Core Values (niềm tin không thỏa hiệp).

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. DN đã có VMV chưa? (cần tạo mới / cập nhật / formalize)
2. Founder story: Tại sao bắt đầu DN này? Động lực cốt lõi?
3. DN sẽ trông như thế nào trong 10-20 năm?
4. 3-5 giá trị mà team THỰC SỰ sống theo (không phải treo tường)?
5. Có "kẻ thù chung" hoặc vấn đề xã hội mà DN muốn giải quyết không?
6. Ai là stakeholder chính? (nhân viên, khách hàng, cộng đồng, cổ đông)

**Prompt tạo file:**
```
Tạo bộ VMV — Tầm nhìn / Sứ mệnh / Giá trị cốt lõi.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Founder story: [tóm tắt]
- VMV hiện tại (nếu có): Vision: [___] | Mission: [___] | Values: [___]
- Tham vọng 10-20 năm: [mô tả]
- Giá trị thực tế team đang sống: [liệt kê]
- Vấn đề xã hội DN muốn giải quyết: [mô tả]
- Stakeholder chính: [liệt kê theo thứ tự ưu tiên]

FORMAT:
- Vision: 1 câu, ≤20 từ, inspire & stretch
- Mission: 1-2 câu, trả lời What/Who/How/Why
- Core Values: 3-5 giá trị × (Tên + Định nghĩa + Hành vi DO + Hành vi DON'T + Ví dụ)
- Brand Promise: 1 câu, customer-facing
- Purpose: 1 câu, Simon Sinek "Why"
- Test: Mỗi statement qua bộ lọc — Specific? Memorable? Authentic? Differentiating? Actionable?
- Phụ lục: VMV communication plan — cách truyền tải cho team

TONE: Truyền cảm hứng nhưng chân thực, không sáo rỗng.
LENGTH: 3-5 trang A4.
```

---

##### PROMPT 03: Brand Identity Guidelines

**Mô tả:**
Bộ guidelines đảm bảo thương hiệu được thể hiện nhất quán trên mọi điểm chạm.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Đã có logo & bộ nhận diện chưa?
2. Màu sắc chủ đạo? (hex codes nếu có)
3. Font chữ đang dùng?
4. Tính cách thương hiệu?
5. Tone of voice: formal/casual, serious/playful, authoritative/friendly?
6. Điểm chạm chính: website, social media, brochure, namecard, email, office?
7. Có DO/DON'T nào rõ ràng?

**Prompt tạo file:**
```
Tạo Brand Identity Guidelines.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Logo: [Có/Chưa] — File: [link nếu có]
- Màu sắc: Primary [hex] | Secondary [hex] | Accent [hex]
- Font: Heading [font] | Body [font]
- Tính cách: [3-5 tính từ]
- Tone of voice: [mô tả]
- Điểm chạm chính: [liệt kê]
- Do/Don't hiện tại: [liệt kê]

FORMAT:
- Structured manual, visual-heavy (mô tả ví dụ dù không có hình)
- Color swatches: HEX + RGB + CMYK + Pantone (nếu có)
- Typography specimens: Size hierarchy table
- Tone matrix: Context | We say... | We don't say...
- Application mockup descriptions: Mô tả chi tiết cách áp dụng trên mỗi touchpoint
- Do/Don't: ✅ "Làm thế này" vs ❌ "Không làm thế này"
- Checklist cuối: 10 câu self-check trước khi publish bất kỳ material nào

TONE: Hướng dẫn — rõ ràng, visual, không mơ hồ.
LENGTH: 15-25 trang A4.
```

---

##### PROMPT 04: Elevator Pitch

**Mô tả:**
Bộ elevator pitch cho nhiều ngữ cảnh: 30 giây (networking), 60 giây (nhà đầu tư), 90 giây (đối tác).

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Một câu mô tả DN dễ hiểu nhất?
2. Điểm khác biệt lớn nhất so với đối thủ?
3. Proof point mạnh nhất?
4. CTA mong muốn?
5. Cần version nào? (Nhà đầu tư / Khách hàng / Đối tác / Tuyển dụng / Media / Tất cả)
6. Ngôn ngữ: Tiếng Việt / Tiếng Anh / cả hai?

**Prompt tạo file:**
```
Tạo bộ Elevator Pitch cho doanh nghiệp.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- 1-liner: "[Chúng tôi giúp [ai] [làm gì] bằng [cách gì]]"
- USP: [điểm khác biệt]
- Proof points: [số liệu/khách hàng/giải thưởng]
- Audiences: [Investor / Customer / Partner / Recruit / Media]
- Ngôn ngữ: [VI / EN / cả hai]

FORMAT:
- 3 versions: 30s (~75 từ) / 60s (~150 từ) / 90s (~225 từ)
- Customize per audience: 5 audiences × 3 lengths = 15 variations (hoặc chọn combo)
- Mỗi pitch: Script đầy đủ + ghi chú (nhấn mạnh từ nào, pause ở đâu)
- Đánh giá: ☐ Clear? ☐ Memorable? ☐ Differentiating? ☐ Has CTA? ☐ Under time?
- Practice guide: Cách luyện trước gương, record & review

TONE: Tự tin, conversational, không đọc thuộc lòng.
LENGTH: 3-5 trang A4.
```

---

##### PROMPT 05: Phân tích SWOT

**Mô tả:**
Phân tích Strengths-Weaknesses-Opportunities-Threats toàn diện, kèm chiến lược kết hợp SO/ST/WO/WT.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Phạm vi phân tích? (toàn DN / 1 sản phẩm / 1 thị trường)
2. Đối thủ cạnh tranh chính? (2-3 tên)
3. Thế mạnh DN tự nhận?
4. Điểm yếu lớn nhất?
5. Xu hướng thị trường/ngành đang thấy?
6. Rủi ro/đe dọa lo ngại nhất?
7. Có data hỗ trợ không?

**Prompt tạo file:**
```
Tạo SWOT Analysis cho doanh nghiệp.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Quy mô: [doanh thu, nhân sự]
- Phạm vi: [toàn DN / sản phẩm X / thị trường Y]
- Đối thủ: [liệt kê 2-3]
- Strengths (chủ DN nhận): [liệt kê]
- Weaknesses (chủ DN nhận): [liệt kê]
- Opportunities (thị trường): [liệt kê]
- Threats (lo ngại): [liệt kê]
- Data hỗ trợ: [nếu có]

FORMAT:
- Ma trận SWOT 2×2: Mỗi ô 5-8 items, ngắn gọn
- Detail table: Mỗi item = Description (1-2 câu) + Evidence + Impact (H/M/L)
- TOWS Matrix: 4 ô chiến lược, mỗi ô 3-5 strategies cụ thể
- Priority Actions: Top 5, ranked, mỗi action có Owner + Timeline + Expected Impact
- Visualization data: Radar chart / Impact matrix data

TONE: Analytical, evidence-based, actionable.
LENGTH: 5-8 trang A4.
```

---

##### PROMPT 06: Business Model Canvas (BMC)

**Mô tả:**
Mô hình kinh doanh theo 9 khối Osterwalder. Cái nhìn 1-trang về cách DN tạo ra, cung cấp, và thu giá trị.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. DN có bao nhiêu dòng sản phẩm/dịch vụ chính?
2. Khách hàng chính là ai?
3. Giá trị cốt lõi DN mang lại cho khách hàng?
4. Kênh bán hàng/phân phối hiện tại?
5. Nguồn doanh thu?
6. Chi phí lớn nhất?
7. Đối tác chiến lược hiện tại?

**Prompt tạo file:**
```
Tạo Business Model Canvas (BMC).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Sản phẩm/Dịch vụ: [liệt kê dòng chính]
- Khách hàng: [segments]
- Value Proposition: [giá trị cốt lõi]
- Channels: [kênh hiện tại]
- Revenue: [nguồn + tỷ lệ]
- Cost: [chi phí lớn nhất]
- Partners: [đối tác chính]

FORMAT:
- Canvas 1-page: Bảng 9 khối, mỗi khối 3-5 bullet points ngắn gọn
- Deep-dive: 9 sections mở rộng, mỗi section có Current/Desired/Gap
- Revenue model: Bảng stream × pricing × unit economics
- Key Metrics per block: VD: Customer Segments → TAM/SAM/SOM, Revenue → MRR/ARPU/LTV
- Validation checklist: Giả định nào ĐÃ validate? Giả định nào CẦN test?

TONE: Strategic, concise, visual.
LENGTH: 5-8 trang A4 (1 trang canvas + 7 trang detail).
```

---

##### PROMPT 07: Porter Five Forces

**Mô tả:**
Phân tích 5 áp lực cạnh tranh theo Michael Porter. Đánh giá sức hấp dẫn & mức độ cạnh tranh ngành.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Ngành/phân khúc cụ thể đang phân tích?
2. Đối thủ trực tiếp chính? (3-5 tên, ước lượng thị phần)
3. Rào cản gia nhập ngành?
4. Có sản phẩm/dịch vụ thay thế nào đang đe dọa?
5. Nhà cung cấp chính? Có phụ thuộc vào 1-2 NCC lớn không?
6. Khách hàng có nhiều lựa chọn thay thế không? Switching cost cao/thấp?

**Prompt tạo file:**
```
Tạo Porter Five Forces Analysis.

CONTEXT:
- DN: [Tên] — Ngành/Phân khúc: [cụ thể]
- Đối thủ trực tiếp: [tên + ước lượng thị phần]
- Rào cản gia nhập: [liệt kê]
- Sản phẩm thay thế: [liệt kê]
- NCC chính: [liệt kê + mức phụ thuộc]
- Đặc điểm KH: [tập trung/phân tán, switching cost]

FORMAT:
- Radar chart data: 5 forces × score 1-5 (1=Low pressure, 5=High pressure)
- Mỗi force: 1 trang — Factor analysis table: Factor | Evidence | Score (1-5)
- Overall Industry Attractiveness score: Trung bình 5 forces
- Strategic Implications: Bảng Force | Level | Our Response
- Comparison: Vẽ 2 radar — Industry average vs Our position

TONE: Analytical, academic-meets-practical.
LENGTH: 6-8 trang A4.
```

---

##### PROMPT 08: Competitive Landscape

**Mô tả:**
Bản đồ cạnh tranh chi tiết — so sánh DN với 3-5 đối thủ chính trên nhiều tiêu chí.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. 3-5 đối thủ chính muốn so sánh?
2. Tiêu chí so sánh quan trọng nhất?
3. Có data cụ thể về đối thủ không?
4. USP hiện tại của DN so với đối thủ?
5. Khoảng trống thị trường (white space) mà DN đang nhắm?
6. Có muốn bao gồm indirect competitors không?

**Prompt tạo file:**
```
Tạo Competitive Landscape Analysis.

CONTEXT:
- DN: [Tên] — Positioning hiện tại: [mô tả]
- Đối thủ: [Tên 1 - website] | [Tên 2 - website] | [Tên 3 - website]
- Tiêu chí so sánh: [liệt kê 8-12 tiêu chí]
- Data đối thủ: [nguồn: công khai / ước lượng / industry report]
- USP của DN: [mô tả]
- White space target: [mô tả]

FORMAT:
- Competitor profiles: 1/2 trang mỗi đối thủ
- Comparison matrix: Tiêu chí × Competitors, dùng ⭐ (1-5) hoặc ✅/⚠️/❌
- Positioning map: 2D data (Axis 1: [___], Axis 2: [___]) + coordinates per player
- Feature comparison: Binary ✅/❌ cho 20-30 features
- Battlecards: 1 trang per đối thủ → "They say... We say..."
- White space: Underserved needs × Competitor coverage matrix

TONE: Intelligence report — objective, data-driven, actionable.
LENGTH: 8-12 trang A4.
```

---

##### PROMPT 09: Ideal Customer Profile — ICP & Buyer Persona

**Mô tả:**
Chân dung khách hàng lý tưởng ở 2 cấp: ICP (cấp công ty/tổ chức cho B2B, hoặc segment cho B2C) và Buyer Persona (cấp cá nhân ra quyết định).

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. B2B hay B2C? (hoặc cả hai)
2. Top 5 khách hàng hiện tại tốt nhất?
3. Top 3 khách hàng xấu nhất?
4. Quy trình ra quyết định mua?
5. Pain points chính mà KH tìm đến DN?
6. Kênh KH thường dùng để tìm giải pháp?
7. Có data KH nào? (CRM, survey, interview)

**Prompt tạo file:**
```
Tạo ICP & Buyer Persona.

CONTEXT:
- DN: [Tên] — Model: [B2B / B2C / B2B2C]
- Top 5 KH tốt: [mô tả ngắn mỗi KH]
- Top 3 KH xấu: [mô tả ngắn + lý do]
- Quy trình mua: [mô tả]
- Pain points KH: [liệt kê]
- Kênh KH dùng: [liệt kê]
- Data nguồn: [CRM / survey / interview / ước lượng]

FORMAT:
- ICP card: 1 trang, visual, key criteria + thresholds
- Buyer Persona: 2-3 personas × 1 trang mỗi persona (visual card format)
- Anti-Persona: 1/2 trang — "DON'T sell to..."
- Objection Handling: Bảng Objection | Root cause | Response
- Journey Map per persona: 4 stages × Touchpoints/Actions/Emotions/Needs
- Lead Scoring: Criteria | Weight | Score range | Threshold (MQL/SQL)

TONE: Marketing strategy — empathetic, data-informed, actionable.
LENGTH: 8-12 trang A4.
```

---

##### PROMPT 10: Business Plan

**Mô tả:**
Kế hoạch kinh doanh tổng thể — tài liệu chiến lược quan trọng nhất.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Mục đích chính: nội bộ / gọi vốn / vay ngân hàng / đối tác?
2. Time horizon: 1 năm / 3 năm / 5 năm?
3. Tổng quan thị trường: TAM/SAM/SOM?
4. Financial projections: có sẵn hay cần tạo?
5. Go-to-market strategy đã có chưa?
6. Đã có data nào từ các file trước?

**Prompt tạo file:**
```
Tạo Business Plan.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Stage: [startup/growth/mature]
- Mục đích: [nội bộ / gọi vốn / vay / đối tác]
- Time horizon: [1/3/5 năm]
- Market: TAM [số] | SAM [số] | SOM [số]
- Financial data: [có sẵn / cần tạo projection]
- Data từ files trước: [liệt kê files đã tạo trong 02-bb-strategy]

FORMAT:
- Executive Summary: 2 trang, standalone, highlight key numbers
- Each section: Key insight → Supporting data → Implications → Actions
- Financial tables: P&L, Cash Flow, Balance Sheet — 3 scenarios (Base/Optimistic/Conservative)
- Visuals: Market size pie chart, Growth projection line chart, Org chart, Timeline Gantt
- Tham chiếu cross-reference: Link đến files chi tiết (SWOT, BMC, ICP, Competitive)
- Appendix: Detailed financial model assumptions

TONE: Professional, persuasive (nếu gọi vốn), evidence-based.
LENGTH: 20-40 trang A4.
```

---

##### PROMPT 11: OGSM Framework

**Mô tả:**
OGSM (Objectives-Goals-Strategies-Measures) — công cụ chiến lược 1 trang.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Objective (mục tiêu lớn)?
2. Goals (mục tiêu đo lường)?
3. Strategies (chiến lược)?
4. Time period?
5. Đã có OKR riêng chưa?

**Prompt tạo file:**
```
Tạo OGSM Framework.

CONTEXT:
- DN: [Tên] — Objective: [mô tả mục tiêu lớn]
- Goals: [liệt kê KPIs + targets]
- Strategies: [liệt kê 3-5 chiến lược]
- Period: [năm/giai đoạn]
- Existing OKR: [Có/Không]

FORMAT:
- OGSM table: 4 cột (O|G|S|M), cascade rõ ràng
- 1-page overview: Fit on 1 trang A4, landscape orientation
- Detail page: Mỗi Strategy → Measures → Action items → Owner → Timeline
- Alignment check: Mỗi Measure phải link ngược lên Goal, mỗi Goal link lên Objective
- Quarterly review template: Kèm bảng review tiến độ

TONE: Strategic, concise, executive-friendly.
LENGTH: 2-4 trang A4.
```

---

##### PROMPT 12: OKR Template

**Mô tả:**
Hệ thống OKR theo quý — cascade từ Company → Department → Individual.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. OKR cho cấp nào?
2. Quý nào?
3. Company-level objectives?
4. Phòng ban nào cần OKR?
5. Đã từng dùng OKR chưa?
6. Scoring system: 0-1.0 (Google style) / % / RAG?

**Prompt tạo file:**
```
Tạo OKR Template.

CONTEXT:
- DN: [Tên] — OKR level: [Company / Department / Individual / All]
- Quarter: [Q_/20__]
- Company Objectives: [liệt kê 3-5]
- Departments: [liệt kê]
- OKR maturity: [Mới dùng lần đầu / Đã quen]
- Scoring: [0-1.0 / % / RAG]

FORMAT:
- OKR Primer: 1 trang, visual, rules of thumb
- OKR Sheet: O | KR1 | KR2 | KR3 | Score | Owner
- Cascade view: Company → Dept → Individual alignment map
- Confidence meter: Weekly template với traffic light
- Quarterly retrospective: What worked | What didn't | Adjust for next Q
- Common mistakes: Top 10 OKR mistakes + how to avoid

TONE: Goal-setting — ambitious, measurable, inspiring.
LENGTH: 5-8 trang A4.
```

---

##### PROMPT 13: BCG Matrix

**Mô tả:**
Phân loại sản phẩm/dịch vụ/SBU theo BCG Matrix: Stars, Cash Cows, Question Marks, Dogs.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Danh sách sản phẩm/dịch vụ/SBU cần phân loại?
2. Doanh thu mỗi sản phẩm? Tốc độ tăng trưởng?
3. Thị phần ước lượng vs đối thủ lớn nhất?
4. Market growth rate của từng phân khúc?
5. Đầu tư hiện tại cho mỗi sản phẩm?

**Prompt tạo file:**
```
Tạo BCG Matrix Analysis.

CONTEXT:
- DN: [Tên]
- Products/SBU: [Liệt kê: Tên | Revenue | Growth % | Market Share vs #1 competitor]
- Market Growth Rate benchmark: [ngành = %]
- Market Share benchmark: [relative to largest competitor]

FORMAT:
- Matrix data: Product | Revenue | Growth Rate | Relative Market Share | Quadrant
- Visual description: 2×2 plot với bubble chart data
- Product analysis: 1/2 trang per product — Why it's in this quadrant + Evidence + Recommendation
- Portfolio balance: Pie chart data — % Revenue in Stars/Cash Cows/QM/Dogs
- Investment reallocation: From → To table
- 12-month action plan per product

TONE: Strategic portfolio management — decisive, data-driven.
LENGTH: 4-6 trang A4.
```

---

##### PROMPT 14: Strategic Roadmap

**Mô tả:**
Lộ trình phát triển DN theo timeline 1-3-5 năm.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Horizon: 1 năm / 3 năm / 5 năm?
2. Key milestones đã xác định?
3. Dependencies giữa các milestone?
4. Phân chia theo giai đoạn?
5. Muốn roadmap theo swimlane hay timeline đơn?
6. Có trigger milestones không?

**Prompt tạo file:**
```
Tạo Strategic Roadmap.

CONTEXT:
- DN: [Tên] — Stage: [startup/growth/mature]
- Horizon: [1/3/5 năm]
- Key Milestones: [liệt kê với target date]
- Dependencies: [milestone A → B → C]
- Giai đoạn: [VD: Foundation Q1-Q2 → Growth Q3-Q4 → Scale Year 2]
- Format: [Swimlane / Timeline / Phase-based]

FORMAT:
- Executive 1-pager: Timeline + 5-7 key milestones
- Swimlane roadmap: 5 lanes (Product, Market, People, Finance, Tech) × time
- Phase cards: Phase name | Duration | Objectives | Key Activities | Exit Criteria | Budget
- Milestone table: # | Milestone | Lane | Start | End | Dependencies | Owner | Status
- Dependencies: Mermaid Gantt hoặc DAG diagram
- Year 1 quarterly detail: Q1-Q4 breakdown với monthly actions
- Review template: Quarterly roadmap review form

TONE: Visionary yet practical — ambitious milestones, realistic timelines.
LENGTH: 6-10 trang A4.
```

---

##### PROMPT 15: Risk Register

**Mô tả:**
Sổ đăng ký rủi ro chiến lược — danh mục tổng hợp, đánh giá, tracking tất cả rủi ro cấp DN.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Đã có danh sách rủi ro từ Risk Management Policy chưa?
2. Top 5 rủi ro DN đang lo ngại nhất?
3. Ai sẽ là Risk Owner cho mỗi rủi ro?
4. Tần suất review: hàng tháng / hàng quý?
5. Có KRI (Key Risk Indicators) đã track chưa?

**Prompt tạo file:**
```
Tạo Risk Register.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Risk categories: [Strategy / Finance / Operations / Compliance / Reputation / Technology]
- Top 5 risks: [liệt kê]
- Risk Owners: [mapping]
- Review frequency: [monthly/quarterly]
- Existing KRIs: [liệt kê hoặc "chưa có"]

FORMAT:
- Main table: Full register với tất cả cột (12+ cột)
- Heat Map: 5×5 data grid, color-coded
- Top 10 Risk Cards: Mỗi risk = 1/2 trang detail — Root cause, Current controls, Residual risk, Action plan
- KRI tracking: Bảng indicators + trend arrows
- Review log: Template cho monthly/quarterly review
- Starter risks: Pre-populate 15-20 common risks per industry

TONE: Risk management — objective, vigilant, actionable.
LENGTH: 6-10 trang A4.
```

---

##### PROMPT 16: Crisis Management Plan

**Mô tả:**
Playbook xử lý khủng hoảng — cho các kịch bản: khủng hoảng truyền thông, sự cố sản phẩm, rò rỉ dữ liệu, kiện tụng, thiên tai, mất key person.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Đã từng gặp khủng hoảng chưa?
2. Có PR/truyền thông nội bộ hay outsource?
3. Ai là Crisis Commander?
4. Có Luật sư thường trực không?
5. Kênh truyền thông chính cần quản lý khi khủng hoảng?
6. Kịch bản nào lo ngại nhất?

**Prompt tạo file:**
```
Tạo Crisis Management Plan.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Crisis history: [mô tả hoặc "chưa có"]
- PR: [nội bộ / agency: tên]
- Crisis Commander: [chức danh]
- Luật sư: [Có/Không — tên nếu có]
- Kênh truyền thông: [liệt kê: Facebook, website, báo chí...]
- Kịch bản lo ngại: [liệt kê top 3]

FORMAT:
- Crisis Level matrix: Level | Description | Authority | Response time | Communication scope
- Team contact card: Role | Name | Phone | Email | Backup
- "First 60 Minutes" checklist: 10 bước bắt buộc
- 6-8 Scenario playbooks: Mỗi kịch bản 1-2 trang
- Communication templates: Internal memo, Customer email, Press statement, Social media post
- Holding statement library: 5 generic statements dùng được ngay
- AAR template: What happened | What went well | What went wrong | Improvements | Owner

TONE: Emergency protocol — clear, decisive, no ambiguity.
LENGTH: 15-20 trang A4.
```

---

##### PROMPT 17: Business Continuity Plan (BCP)

**Mô tả:**
Kế hoạch đảm bảo DN tiếp tục vận hành khi xảy ra sự cố lớn.

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Business-critical processes? (top 5)
2. Hệ thống IT critical?
3. Có backup site / remote work capability không?
4. Recovery targets: Bao lâu chấp nhận được downtime? (RTO)
5. Data backup: Tần suất, location, recovery tested?
6. Key person dependencies?

**Prompt tạo file:**
```
Tạo Business Continuity Plan (BCP).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- Critical processes: [liệt kê top 5]
- IT systems: [liệt kê critical systems]
- Remote work: [Có/Không] — Capability: [%]
- RTO acceptable: [giờ/ngày]
- Data backup: [method / frequency / location]
- Key person risks: [liệt kê]

FORMAT:
- BIA table: Process | Owner | Impact if down 1h/1d/1w | RTO | RPO | Priority
- Recovery procedures: Per critical function, step-by-step
- IT DR plan: System | RTO | RPO | Backup | Recovery Steps | Last Tested
- People matrix: Role | Primary | Backup | Cross-training | Succession
- Communication tree: Flowchart — who notifies whom
- Activation checklist: 15-step protocol
- Test schedule: Type | Frequency | Last Done | Next Due | Owner

TONE: Operational resilience — thorough, practical, testable.
LENGTH: 12-18 trang A4.
```

---

##### PROMPT 18: Scenario Planning

**Mô tả:**
3 kịch bản chiến lược: Lạc quan (Best Case), Cơ sở (Base Case), Bi quan (Worst Case).

**Thông tin cần thu thập (hỏi người dùng trước khi tạo):**
1. Biến số chính ảnh hưởng DN nhất?
2. Financial projections hiện tại (base case)?
3. Best case scenario theo anh là gì?
4. Worst case scenario?
5. Trigger points?
6. Có pivot options nào?

**Prompt tạo file:**
```
Tạo Scenario Planning.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Key variables: [liệt kê 3-5: VD market growth, regulation, competition, technology, economy]
- Base case projections: Revenue [số] | EBITDA [số] | Headcount [số]
- Best case vision: [mô tả]
- Worst case fear: [mô tả]
- Pivot options: [liệt kê]
- Time horizon: [1-3 năm]

FORMAT:
- Scenario matrix: Variable × Best/Base/Worst values
- 3 scenario narratives: 1-2 trang mỗi kịch bản, storytelling format
- Financial comparison: Bảng 3 cột — Revenue, EBITDA, Cash, Headcount, Market Share
- Trigger dashboard: Indicator | Best trigger | Worst trigger | Current | Trend
- Decision rules: "IF indicator > X THEN activate Plan B"
- Quarterly review checklist: 10 items to re-evaluate

TONE: Strategic foresight — thoughtful, balanced, preparing not predicting.
LENGTH: 10-15 trang A4.
```

---

#### Ghi chú triển khai Strategy

**Dependencies nội bộ:**
- `tam-nhin-su-menh-gia-tri.md` → tham chiếu bởi hầu hết file khác trong bộ đóng gói
- `company-profile.md` → tham chiếu `tam-nhin-su-menh-gia-tri.md` + `brand-identity-guidelines.md`
- `business-plan.md` → tổng hợp từ SWOT, BMC, ICP, Competitive, OGSM, BCG, Roadmap
- `ideal-customer-profile.md` → sẽ được dùng bởi 06-Sales, 07-Marketing, 08-Customer
- `strategic-roadmap.md` → tham chiếu bởi mọi skill con khi xác định timeline

**Dependencies với skill khác:**
- **Từ 01-Governance**: Cơ cấu quản trị, pháp nhân → ảnh hưởng Company Profile, Business Plan
- **Cho 03-Finance**: Business Plan → Financial projections, Scenario Planning → Budget scenarios
- **Cho 06-Sales**: ICP → Sales targeting, Competitive Landscape → Battlecards
- **Cho 07-Marketing**: Brand Identity → Marketing materials, Elevator Pitch → Messaging
- **Cho 12-Growth**: Roadmap → Investment timeline, Scenario Planning → Fundraising strategy

**Thứ tự tạo khuyến nghị:**
1. VMV → 2. Company Profile → 3. Brand Identity → 4. Elevator Pitch
5. SWOT → 6. BMC → 7. Porter → 8. Competitive Landscape → 9. ICP
10. OGSM → 11. OKR → 12. BCG → 13. Roadmap → 14. Business Plan
### VIII.4 — BP Finance (Tài Chính & Kế Toán)

> **Tầng 2: Bộ Máy** — 20 tài liệu: Chính sách tài chính (4), Kế hoạch & Dự báo (5), Kế toán vận hành (6), Báo cáo tài chính (5).

---

### PROMPT 01: Chính sách tài chính tổng quát (General Financial Policy)

#### Mô tả
Văn bản chính sách cấp cao nhất về quản lý tài chính DN. Thiết lập nguyên tắc, phân cấp phê duyệt, kiểm soát nội bộ, và trách nhiệm giải trình tài chính. Là "hiến pháp tài chính" mà mọi quy trình, quy chế tài chính khác phải tuân thủ.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Quy mô doanh thu năm? (xác định mức độ phức tạp kiểm soát nội bộ)
2. Cơ cấu tổ chức tài chính hiện tại? (có CFO riêng hay kế toán trưởng kiêm? Outsource kế toán?)
3. Phân cấp phê duyệt hiện tại? (CEO duyệt tất cả hay đã phân quyền?)
4. Ngân hàng giao dịch chính? Có internet banking / chữ ký số?
5. Phần mềm kế toán đang dùng? (MISA, Fast, SAP, Excel...)
6. Có kiểm toán nội bộ / kiểm toán độc lập hàng năm không?

#### Template gợi ý
Cấu trúc POL:
- **Chương I** — Mục đích, Phạm vi, Đối tượng áp dụng
- **Chương II** — Nguyên tắc quản lý tài chính: Minh bạch, Tiết kiệm, Hiệu quả, Tuân thủ pháp luật
- **Chương III** — Tổ chức bộ máy tài chính-kế toán: Cơ cấu, chức năng, nhiệm vụ
- **Chương IV** — Phân cấp phê duyệt tài chính: Bảng hạn mức theo cấp (NV → TP → GĐ → HĐQT)
- **Chương V** — Kiểm soát nội bộ: Nguyên tắc 4 mắt, tách biệt nhiệm vụ, kiểm tra chéo
- **Chương VI** — Quản lý tài sản & vốn: Tiền mặt, ngân hàng, tài sản cố định, đầu tư
- **Chương VII** — Chế độ báo cáo: Loại báo cáo, tần suất, người nhận
- **Chương VIII** — Kiểm toán & Giám sát
- **Phụ lục**: Bảng phân cấp phê duyệt chi tiết, Sơ đồ bộ máy kế toán

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách tài chính tổng quát (General Financial Policy) cho doanh nghiệp.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Doanh thu: [số/năm] — Nhân sự: [số]
- Bộ máy tài chính: [CFO riêng / KTT kiêm / Outsource]
- Phần mềm kế toán: [MISA / Fast / SAP / Excel / khác]
- Phân cấp hiện tại: [mô tả]
- Kiểm toán: [Nội bộ / Độc lập / Chưa có]
- Cơ sở pháp lý: Luật Kế toán 2015, Luật DN 2020, Chuẩn mực kế toán VN (VAS)

FORMAT:
- Chia chương, đánh số điều liên tục
- Bảng phân cấp phê duyệt: Loại chi phí | Nhân viên | Trưởng phòng | CFO/KTT | Giám đốc | HĐQT + Hạn mức VNĐ
- Sơ đồ bộ máy kế toán: Mermaid org chart
- Nguyên tắc kiểm soát nội bộ: Checklist áp dụng
- Chế độ báo cáo: Bảng Loại BC | Tần suất | Người lập | Người nhận | Deadline

TONE: Chính thức, chuẩn mực, phù hợp luật VN.
LENGTH: 10-15 trang A4.
```

---

### PROMPT 02: Quy chế chi tiêu nội bộ (Internal Spending Regulations)

#### Mô tả
Quy chế chi tiết về hạn mức, quy trình duyệt chi, danh mục chi phí được phép, và các quy định kiểm soát chi tiêu hàng ngày. Đây là file được TOÀN BỘ nhân viên sử dụng — phải rõ ràng, dễ hiểu, dễ tra cứu.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hạn mức chi tiêu không cần duyệt của mỗi cấp? (VD: NV < 500K, TP < 5 triệu, GĐ < 50 triệu)
2. Danh mục chi phí phổ biến? (VD: văn phòng phẩm, đi lại, tiếp khách, hội nghị...)
3. Chi phí nào cần duyệt đặc biệt? (VD: quảng cáo > X triệu, mua tài sản > Y triệu)
4. Quy trình duyệt: email / phần mềm / giấy? Bao nhiêu cấp duyệt?
5. Có advance (tạm ứng) không? Quy định hoàn ứng trong bao lâu?
6. Chi tiêu ngoài danh mục — quy trình xin phê duyệt đặc biệt?

#### Template gợi ý
Cấu trúc POL:
- **Điều 1-3** — Mục đích, Phạm vi, Thuật ngữ
- **Điều 4** — Nguyên tắc chi tiêu: Có trong budget, đúng mục đích, đủ chứng từ, đã phê duyệt
- **Điều 5** — Phân cấp duyệt chi: Bảng hạn mức chi tiết theo cấp × loại chi phí
- **Điều 6** — Danh mục chi phí: Liệt kê + định mức từng loại (VD: tiếp khách max 500K/lần)
- **Điều 7** — Quy trình duyệt chi: Flowchart từ lúc phát sinh → duyệt → chi → hoàn chứng từ
- **Điều 8** — Tạm ứng & Hoàn ứng: Hạn mức, thời hạn, xử lý khi không hoàn ứng
- **Điều 9** — Chi tiêu đặc biệt: Ngoài danh mục, vượt hạn mức, khẩn cấp
- **Điều 10** — Xử lý vi phạm: Mức phạt, trách nhiệm bồi thường
- **Phụ lục**: Bảng định mức chi phí, Mẫu giấy đề nghị thanh toán

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế chi tiêu nội bộ (Internal Spending Regulations).

CONTEXT:
- DN: [Tên] — Quy mô: [nhân sự] — Doanh thu: [số/năm]
- Hạn mức duyệt chi: NV [___] | TP [___] | GĐ [___] | HĐQT [___]
- Quy trình duyệt: [email / phần mềm / giấy]
- Số cấp duyệt: [số]
- Tạm ứng: [Có/Không] — Thời hạn hoàn ứng: [ngày]

FORMAT:
- Đánh số điều liên tục, ngôn ngữ rõ ràng cho mọi cấp nhân viên
- Bảng phân cấp: Loại chi phí | < X triệu (NV) | < Y triệu (TP) | < Z triệu (GĐ) | > Z triệu (HĐQT)
- Bảng định mức: Loại | Định mức/lần | Định mức/tháng | Ghi chú
- Flowchart duyệt chi: Mermaid — Phát sinh → Đề nghị → Duyệt → Chi → Chứng từ → Hạch toán
- FAQ: 10 tình huống phổ biến (VD: taxi lúc tối khuya, tiếp khách ngoài định mức...)

TONE: Rõ ràng, dễ hiểu, thực tế — ai cũng đọc được.
LENGTH: 6-10 trang A4.
```

---

### PROMPT 03: Chính sách quản lý công nợ (Accounts Receivable/Payable Management Policy)

#### Mô tả
Chính sách toàn diện về quản lý công nợ phải thu (AR) và phải trả (AP). Quy định điều khoản thanh toán, hạn mức tín dụng khách hàng, quy trình thu hồi nợ, trích lập dự phòng nợ xấu, và quản lý thanh toán nhà cung cấp.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mô hình kinh doanh? (B2B công nợ dài / B2C thu ngay / Hybrid)
2. Điều khoản thanh toán phổ biến? (COD, Net 15, Net 30, Net 60?)
3. Tình trạng công nợ hiện tại? (% nợ quá hạn, nợ xấu)
4. Có bộ phận thu hồi nợ riêng không?
5. Tiêu chí cấp tín dụng cho khách hàng? (doanh số, lịch sử, bảo lãnh...)
6. Chính sách chiết khấu thanh toán sớm?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích, Phạm vi, Thuật ngữ
- **Phần 2** — Quản lý công nợ phải thu (AR): Cấp tín dụng, hạn mức, điều khoản, chiết khấu
- **Phần 3** — Thu hồi nợ: Quy trình 4 bước (nhắc nhở → đốc thúc → cảnh báo → xử lý pháp lý)
- **Phần 4** — Trích lập dự phòng nợ xấu: Tiêu chí, tỷ lệ, quy trình xóa nợ
- **Phần 5** — Quản lý công nợ phải trả (AP): Ưu tiên thanh toán, tận dụng chiết khấu, quản lý cashflow
- **Phần 6** — Đối soát công nợ: Tần suất, quy trình, xử lý chênh lệch
- **Phần 7** — Vai trò & Trách nhiệm
- **Phụ lục**: Bảng aging analysis template, Mẫu thư đòi nợ, Credit application form

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách quản lý công nợ (AR/AP Management Policy).

CONTEXT:
- DN: [Tên] — Mô hình: [B2B / B2C / Hybrid]
- Điều khoản thanh toán: [COD / Net 15 / Net 30 / Net 60]
- Tình trạng nợ: [% quá hạn] — Nợ xấu: [% hoặc số tiền]
- Bộ phận thu hồi nợ: [Có/Không]
- Chiết khấu thanh toán sớm: [Có/Không] — [chi tiết]

FORMAT:
- Chia phần rõ ràng, có mục lục
- Credit scoring: Bảng tiêu chí | Trọng số | Điểm → Hạn mức tín dụng
- Aging buckets: Current | 1-30 | 31-60 | 61-90 | 91-120 | >120 ngày
- Thu hồi nợ escalation: Flowchart 4 bước + timeline + người phụ trách
- Trích lập dự phòng: Bảng tuổi nợ × % trích lập (theo TT48/2019)
- AP payment priority matrix: Nhà CC chiến lược > Nhà CC thường > Khác

TONE: Chuyên nghiệp, tài chính, chặt chẽ.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 04: Chính sách định giá sản phẩm (Pricing Policy)

#### Mô tả
Chính sách quy định phương pháp, quy trình, và thẩm quyền định giá sản phẩm/dịch vụ. Bao gồm chiến lược giá, cơ cấu giá, chính sách chiết khấu, và quy trình điều chỉnh giá.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ chính? Có bao nhiêu SKU / service line?
2. Phương pháp định giá hiện tại? (Cost-plus / Value-based / Competitor-based / Dynamic)
3. Cơ cấu giá: Giá bán lẻ / Giá đại lý / Giá OEM / Giá dự án?
4. Chính sách chiết khấu? (theo volume / theo đối tượng / theo thanh toán)
5. Tần suất review giá? Ai có quyền thay đổi giá?
6. Có sản phẩm chạy theo mùa / theo thị trường không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục tiêu định giá: Lợi nhuận mục tiêu, vị thế thị trường, penetration/skimming
- **Phần 2** — Phương pháp định giá: Cost-plus, Value-based, Competitive — khi nào dùng cái nào
- **Phần 3** — Cơ cấu giá: Price list structure, tier pricing, bundle pricing
- **Phần 4** — Chính sách chiết khấu: Bảng chiết khấu theo loại
- **Phần 5** — Quy trình duyệt giá: Giá mới, điều chỉnh giá, giá đặc biệt
- **Phần 6** — Giá cho kênh phân phối: Đại lý, OEM, Affiliate, Direct
- **Phần 7** — Review & Điều chỉnh: Tần suất, trigger, quy trình
- **Phụ lục**: Price list template, Discount approval form, Margin calculator

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách định giá sản phẩm (Pricing Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Số SKU/service: [số]
- Phương pháp hiện tại: [Cost-plus / Value-based / Competitive / Dynamic]
- Cơ cấu giá: [Retail / Wholesale / OEM / Project]
- Chiết khấu: [volume / đối tượng / thanh toán]
- Review giá: [tần suất] — Người quyết: [chức danh]

FORMAT:
- Pricing framework: Sơ đồ Cost → Markup → List Price → Discount → Net Price
- Bảng chiết khấu: Đối tượng | Volume từ-đến | % CK | Approval cần
- Margin analysis: Bảng SP | Cost | Price | Margin % | Min Price Floor
- Decision tree: Flowchart khi nào dùng Cost-plus vs Value-based vs Competitive
- Price approval workflow: Mermaid flowchart
- Competitive price tracking template

TONE: Chiến lược + thực tế, cân bằng giữa lợi nhuận và cạnh tranh.
LENGTH: 6-10 trang A4.
```

---

### PROMPT 05: Cơ cấu chi phí CCSC (Cost Structure Breakdown)

#### Mô tả
Tài liệu phân tích chi tiết cơ cấu chi phí của DN — phân loại thành chi phí cố định/biến đổi, trực tiếp/gián tiếp, COGS/SGA. Là cơ sở cho ngân sách, định giá, và ra quyết định tài chính.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ngành nghề & mô hình kinh doanh? (sản xuất / dịch vụ / thương mại / SaaS)
2. Các khoản chi phí lớn nhất hiện tại?
3. Có P&L hiện tại để phân tích không?
4. Cần phân tích theo phòng ban / sản phẩm / dự án?
5. Có chi phí mùa vụ / biến động lớn theo tháng không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Tổng quan cơ cấu chi phí: Pie chart data, top 10 khoản lớn nhất
- **Phần 2** — Phân loại: Cố định vs Biến đổi, Trực tiếp vs Gián tiếp
- **Phần 3** — COGS (Giá vốn hàng bán): Chi tiết từng thành phần
- **Phần 4** — SGA (Chi phí bán hàng & Quản lý): Chi tiết
- **Phần 5** — Chi phí theo phòng ban: Breakdown per department
- **Phần 6** — Phân tích xu hướng: MoM, YoY, % doanh thu
- **Phần 7** — Cơ hội tối ưu: Nhận diện chi phí có thể cắt giảm
- **Phụ lục**: Template chi phí chi tiết, Benchmark ngành

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Cơ cấu chi phí CCSC (Cost Structure Breakdown).

CONTEXT:
- DN: [Tên] — Mô hình: [Sản xuất / Dịch vụ / Thương mại / SaaS]
- Doanh thu: [số/năm] — Số phòng ban: [số]
- Khoản lớn nhất: [liệt kê top 5]
- Mùa vụ: [Có/Không]

FORMAT:
- Summary: Bảng tổng quan COGS | SGA | Other → % doanh thu
- Fixed vs Variable: Bảng mỗi khoản + phân loại + số tiền + % tổng
- Pie chart data: Top 10 khoản chi phí
- Per-department: Bảng Phòng ban | Nhân sự | Chi phí | % tổng | Cost per head
- Trend template: 12 tháng × khoản chi phí chính
- Optimization matrix: Khoản CP | Khả năng cắt | Impact | Priority

TONE: Phân tích, data-driven, khách quan.
LENGTH: 5-8 trang A4.
```

---

### PROMPT 06: Ngân sách năm Budget (Annual Budget)

#### Mô tả
Ngân sách năm tổng hợp — lập budget doanh thu và chi phí theo phòng ban, theo quý. Bao gồm quy trình lập, phê duyệt, theo dõi variance, và điều chỉnh ngân sách.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Năm tài chính? (theo năm dương lịch hay khác?)
2. Phương pháp lập ngân sách? (Top-down / Bottom-up / Zero-based)
3. Bao nhiêu phòng ban/trung tâm chi phí cần budget riêng?
4. Có revenue budget không hay chỉ expense budget?
5. Tần suất review variance? (Monthly / Quarterly)
6. Quy trình lập: Timeline từ khi bắt đầu đến khi HĐQT duyệt?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Hướng dẫn lập ngân sách: Phương pháp, assumptions, timeline
- **Phần 2** — Revenue Budget: Theo sản phẩm/kênh × 12 tháng
- **Phần 3** — Expense Budget tổng hợp: COGS + SGA × 12 tháng
- **Phần 4** — Departmental Budget: Mỗi phòng ban 1 bảng chi tiết
- **Phần 5** — CapEx Budget: Đầu tư tài sản, dự án
- **Phần 6** — Budget Summary: P&L dự kiến, Key ratios
- **Phần 7** — Variance Tracking: Template theo dõi Budget vs Actual
- **Phần 8** — Quy trình phê duyệt & Điều chỉnh giữa kỳ
- **Phụ lục**: Template budget per department, Assumption log

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Ngân sách năm (Annual Budget).

CONTEXT:
- DN: [Tên] — Năm tài chính: [năm]
- Phương pháp: [Top-down / Bottom-up / Zero-based]
- Số trung tâm chi phí: [số] — Danh sách: [liệt kê]
- Revenue budget: [Có/Không]
- Variance review: [Monthly / Quarterly]

FORMAT:
- Revenue budget: Sản phẩm/Kênh × Q1-Q2-Q3-Q4 × Monthly breakdown
- Expense budget: Khoản CP × 12 tháng × Phòng ban
- Departmental template: Budget line | Annual | Q1 | Q2 | Q3 | Q4 | Notes
- P&L budget: Revenue → COGS → Gross Profit → SGA → EBITDA → Net Income
- Variance tracker: Budget | Actual | Variance $ | Variance % | Explanation
- Key assumptions log: Assumption | Source | Sensitivity | Impact if wrong
- Approval workflow: Flowchart + Timeline (T-60 đến T-0)

TONE: Tài chính, có cấu trúc, dễ điền số.
LENGTH: 8-12 trang A4 (+ templates).
```

---

### PROMPT 07: Cashflow Forecast 12 tháng (12-Month Cash Flow Forecast)

#### Mô tả
Dự báo dòng tiền 12 tháng tiếp theo — chi tiết dòng tiền vào (thu bán hàng, thu nợ, vay...) và dòng tiền ra (chi mua hàng, lương, thuế, trả nợ...). Xác định tháng nào căng thẳng tiền mặt, cần vay hoặc chậm chi.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Số dư tiền mặt & ngân hàng hiện tại?
2. Nguồn thu chính? (bán hàng / dự án / subscription / đầu tư)
3. Tần suất thu: hàng ngày / tuần / tháng? Có mùa vụ?
4. Các khoản chi lớn cố định hàng tháng? (lương, thuê mặt bằng, vay...)
5. Có kế hoạch chi lớn trong 12 tháng tới? (mua tài sản, đầu tư, trả nợ gốc)
6. Dự trữ tiền mặt tối thiểu mong muốn?

#### Template gợi ý
Cấu trúc RPT:
- **Assumptions** — Giả định về tăng trưởng, collection rate, payment terms
- **Cash Inflow** — Bảng 12 tháng: Từng nguồn thu × từng tháng
- **Cash Outflow** — Bảng 12 tháng: Từng khoản chi × từng tháng
- **Net Cashflow** — Inflow - Outflow = Net per tháng
- **Cumulative Balance** — Số dư lũy kế — highlight tháng âm
- **Sensitivity Analysis** — What-if: doanh thu giảm 10/20/30%
- **Action Plan** — Đối với tháng thiếu hụt: giải pháp cụ thể

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Cashflow Forecast 12 tháng.

CONTEXT:
- DN: [Tên] — Số dư hiện tại: [số]
- Nguồn thu: [liệt kê + ước tính/tháng]
- Chi cố định: [liệt kê + số/tháng]
- Chi lớn sắp tới: [liệt kê + thời điểm]
- Dự trữ tối thiểu: [số]
- Mùa vụ: [Có/Không] — [mô tả pattern]

FORMAT:
- Bảng chính: 12 cột (tháng) × hàng (từng khoản thu/chi)
- Color coding: Tháng dư 🟢 | Tháng thiếu 🔴 | Tháng cận kề 🟡
- Chart data: Line chart — Inflow vs Outflow vs Balance
- Minimum cash line: Đường ngang → alert khi balance < minimum
- Sensitivity table: Base case ±10%, ±20%, ±30%
- Action triggers: IF balance < [X] THEN [action]

TONE: Thực tế, action-oriented, cảnh báo rõ.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 08: Scenario Planning 3 kịch bản (3-Scenario Financial Planning)

#### Mô tả
Phân tích tài chính theo 3 kịch bản: Best Case (lạc quan), Base Case (thực tế), Worst Case (bi quan). Mỗi kịch bản có giả định riêng, P&L dự kiến, cashflow impact, và action plan cụ thể.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Biến số chính ảnh hưởng doanh thu? (VD: số KH mới, giá bán, conversion rate)
2. Biến số chính ảnh hưởng chi phí? (VD: giá nguyên liệu, lương, thuê mặt bằng)
3. Rủi ro lớn nhất hiện tại? (thị trường, đối thủ, pháp lý, nhân sự)
4. Đã từng gặp kịch bản xấu nhất chưa? Diễn ra thế nào?
5. KPI trigger: khi nào chuyển từ Base sang Worst case plan?

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — 3 kịch bản tóm tắt trong 1 bảng
- **Assumptions Matrix** — Bảng biến số × 3 kịch bản
- **Best Case** — Giả định, P&L, Cashflow, Headcount, Investment
- **Base Case** — Giả định, P&L, Cashflow, Headcount, Investment
- **Worst Case** — Giả định, P&L, Cashflow, Headcount, Cost-cutting plan
- **Trigger Points** — KPI nào → chuyển kịch bản
- **Action Plan per Scenario** — Bảng hành động cụ thể
- **Dashboard** — So sánh 3 kịch bản trên 1 trang

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Scenario Planning 3 kịch bản tài chính.

CONTEXT:
- DN: [Tên] — Doanh thu hiện tại: [số/năm]
- Biến số doanh thu: [liệt kê + range]
- Biến số chi phí: [liệt kê + range]
- Rủi ro chính: [liệt kê]
- Thời kỳ dự báo: [12 tháng / 3 năm]

FORMAT:
- Comparison table: KPI | Best | Base | Worst — cho 10+ KPIs
- Assumptions matrix: Biến số | Best | Base | Worst + Probability %
- Mini P&L per scenario: Revenue → COGS → GP → SGA → EBITDA → NI
- Cashflow summary per scenario: 12 tháng × 3 kịch bản
- Trigger dashboard: Bảng KPI | Threshold Best→Base | Threshold Base→Worst | Current
- Action cards: Mỗi kịch bản 5-7 actions cụ thể
- Waterfall: Revenue difference breakdown Best vs Worst

TONE: Chiến lược, analytical, hướng quyết định.
LENGTH: 6-10 trang A4.
```

---

### PROMPT 09: Break-Even Analysis (Phân tích Hòa vốn)

#### Mô tả
Phân tích điểm hòa vốn (BEP) cho DN tổng thể và từng sản phẩm/dịch vụ. Xác định bao nhiêu doanh số, bao nhiêu đơn hàng cần để cover toàn bộ chi phí. Bao gồm sensitivity analysis khi thay đổi giá bán hoặc chi phí.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Danh sách sản phẩm/dịch vụ + giá bán mỗi loại?
2. Chi phí biến đổi trên mỗi đơn vị? (COGS, hoa hồng, vận chuyển...)
3. Tổng chi phí cố định hàng tháng?
4. Có sản phẩm nào cross-subsidize sản phẩm khác không?
5. Target margin mong muốn?

#### Template gợi ý
Cấu trúc RPT:
- **Tổng quan** — BEP tổng DN: Doanh số hòa vốn / tháng, / năm
- **Per Product** — BEP từng SP: Contribution margin, BEP units, BEP revenue
- **Sensitivity** — Thay đổi giá bán ±5%, ±10% → BEP thay đổi bao nhiêu
- **Margin of Safety** — Khoảng cách giữa doanh số thực và BEP
- **Visualization** — Data cho chart: Tổng chi phí vs Doanh thu vs BEP line
- **Recommendations** — Sản phẩm nào nên push, nào nên giảm

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Break-Even Analysis.

CONTEXT:
- DN: [Tên] — Số SP/DV: [số]
- SP chính: [Tên | Giá bán | Biến phí/đv | Contribution margin]
- Chi phí cố định: [số/tháng] — Chi tiết: [liệt kê top 5]
- Target margin: [%]

FORMAT:
- BEP Summary: Bảng DN tổng | Per SP → BEP units | BEP revenue | Contribution margin %
- Formula rõ ràng: BEP = Fixed Cost / (Price - Variable Cost per Unit)
- Sensitivity table: Giá bán ±5/10/15% × Biến phí ±5/10/15% = BEP matrix
- Margin of Safety: Current Revenue | BEP Revenue | MoS % | Interpretation
- Chart data: X = Units, Y1 = Total Revenue, Y2 = Total Cost, intersection = BEP
- Product ranking: Contribution margin desc → Recommend push order

TONE: Analytical, data-driven, dễ hiểu cho non-finance.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 10: SOP Quy trình thu chi (Cash Receipt & Disbursement SOP)

#### Mô tả
Quy trình chuẩn hóa cho mọi giao dịch thu chi trong DN — từ phát sinh, lập chứng từ, phê duyệt, thực hiện thu/chi, đến hạch toán và lưu trữ. Đảm bảo không có giao dịch nào "thoát" khỏi hệ thống kiểm soát.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phương thức thanh toán phổ biến? (Tiền mặt / CK ngân hàng / Ví điện tử / Thẻ)
2. Phần mềm kế toán? (tự động hạch toán hay thủ công?)
3. Số cấp duyệt chi? (1 cấp / 2 cấp / 3 cấp)
4. Có quỹ tiền mặt tại DN không? Hạn mức tồn quỹ?
5. Tần suất nộp tiền ngân hàng?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Thuật ngữ & Viết tắt**
- **Quy trình THU**: Flowchart 6 bước — Phát sinh → Lập phiếu → Xác nhận → Thu → Hạch toán → Lưu
- **Quy trình CHI**: Flowchart 8 bước — Đề nghị → Duyệt → Lập phiếu → Chi → Chứng từ gốc → Hạch toán → Đối chiếu → Lưu
- **Quy định quỹ tiền mặt**: Hạn mức, kiểm quỹ, nộp NH
- **Chứng từ bắt buộc**: Danh sách per loại giao dịch
- **Lưu trữ**: Thời hạn, cách sắp xếp, số hóa

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quy trình thu chi.

CONTEXT:
- DN: [Tên] — Phương thức TT: [TM / CK / Ví ĐT / Thẻ]
- Phần mềm: [MISA / Fast / SAP / Excel]
- Số cấp duyệt chi: [số]
- Quỹ tiền mặt: [Có/Không] — Hạn mức: [số]
- Cơ sở pháp lý: Luật Kế toán 2015, TT200/TT133

FORMAT:
- Flowchart THU: Mermaid — 6 bước rõ ràng
- Flowchart CHI: Mermaid — 8 bước rõ ràng, highlight điểm kiểm soát
- Bảng chứng từ: Loại GD | Chứng từ cần | Ai lập | Ai duyệt | Số bản
- Quy định quỹ TM: Hạn mức | Tần suất kiểm | Quy trình nộp NH
- Checklist cuối ngày: 5 mục kiểm tra cho kế toán
- Error handling: Bảng lỗi phổ biến | Cách xử lý | Escalation

TONE: SOP chuẩn — rõ ràng, step-by-step, không mơ hồ.
LENGTH: 5-8 trang A4.
```

---

### PROMPT 11: SOP Đối soát công nợ (Accounts Reconciliation SOP)

#### Mô tả
Quy trình đối soát công nợ định kỳ giữa DN với khách hàng (AR) và nhà cung cấp (AP). Đảm bảo số liệu trên sổ sách khớp với đối tác, phát hiện sai lệch kịp thời.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tần suất đối soát? (hàng tháng / quý / khi có chênh lệch)
2. Số lượng KH/NCC cần đối soát thường xuyên?
3. Hình thức đối soát: email / gặp trực tiếp / gửi biên bản?
4. Phần mềm hỗ trợ? (tự động tạo bảng đối soát hay thủ công?)
5. Tình trạng chênh lệch hiện tại có phổ biến không?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Lịch đối soát**: Calendar — ai đối soát với ai, khi nào
- **Quy trình đối soát AR**: 5 bước — Xuất data → Gửi xác nhận → Nhận phản hồi → Xử lý chênh lệch → Ký biên bản
- **Quy trình đối soát AP**: 5 bước tương tự
- **Xử lý chênh lệch**: Decision tree — loại chênh lệch → nguyên nhân → cách xử lý
- **Template biên bản đối soát**
- **Escalation**: Khi không thống nhất

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Đối soát công nợ.

CONTEXT:
- DN: [Tên] — Số KH đối soát: [số] — Số NCC đối soát: [số]
- Tần suất: [tháng / quý]
- Hình thức: [email / trực tiếp / online]
- Phần mềm: [tên]

FORMAT:
- Calendar đối soát: Bảng Tuần/Tháng × Đối tượng
- Flowchart AR: Mermaid — 5 bước + timeline
- Flowchart AP: Mermaid — 5 bước + timeline
- Xử lý chênh lệch: Decision tree — Chênh lệch thời gian / số lượng / giá / khác → Action
- Template biên bản: Header + Bảng chi tiết + Chênh lệch + Chữ ký 2 bên
- Aging report template kèm đối soát
- KPI: % đối soát hoàn thành / tháng, % chênh lệch / tổng dư nợ

TONE: SOP chuẩn, rõ ràng.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 12: SOP Kế toán tháng — Monthly Close (Month-End Closing SOP)

#### Mô tả
Quy trình kế toán tháng (monthly close) — checklist tất cả công việc kế toán cần hoàn thành trước khi "đóng sổ" mỗi tháng. Bao gồm hạch toán, đối chiếu, bút toán điều chỉnh, lập báo cáo.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Timeline close: ngày mấy hàng tháng phải xong? (VD: ngày 5 tháng sau)
2. Bao nhiêu kế toán viên tham gia close?
3. Phần mềm kế toán? Tự động hóa được bao nhiêu %?
4. Các bút toán điều chỉnh thường gặp? (khấu hao, phân bổ, trích trước, dự phòng)
5. Báo cáo nào cần nộp sau khi close? (nội bộ / thuế / ngân hàng)

#### Template gợi ý
Cấu trúc SOP:
- **Timeline Close** — Gantt: Day 1 → Day 5 (hoặc custom), mỗi ngày làm gì
- **Pre-Close Checklist** — Trước khi close: đối chiếu ngân hàng, kiểm quỹ, cut-off
- **Close Checklist** — Trong khi close: bút toán điều chỉnh, khấu hao, phân bổ, dự phòng
- **Post-Close Checklist** — Sau khi close: review, lập BC, nộp thuế
- **Reconciliation** — Đối chiếu: sổ cái vs sổ phụ, NH vs sổ sách, kho vs sổ sách
- **Reporting** — Danh sách BC cần nộp + deadline + người nhận
- **Sign-off** — Kế toán → KTT → CFO/GĐ

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Monthly Close (Kế toán tháng).

CONTEXT:
- DN: [Tên] — Timeline close: ngày [X] hàng tháng
- Số kế toán: [số] — Phần mềm: [tên]
- Bút toán điều chỉnh chính: [liệt kê]
- BC cần nộp: [nội bộ / thuế GTGT / thuế TNCN / ngân hàng]

FORMAT:
- Gantt chart: Day 1-5 × Tasks × Owner — Mermaid hoặc bảng
- Pre-Close checklist: 10-15 mục ☐ + Owner + Deadline
- Close checklist: 15-20 mục ☐ + Bút toán mẫu
- Post-Close checklist: 8-10 mục ☐ + BC + Deadline
- Reconciliation template: Sổ cái vs Sổ phụ vs Nguồn → Chênh lệch → Xử lý
- Sign-off sheet: Task | Done by | Reviewed by | Date | Notes
- Common errors: Bảng lỗi hay gặp + cách phòng tránh

TONE: SOP chuẩn, operational, checklist-oriented.
LENGTH: 5-8 trang A4.
```

---

### PROMPT 13: Phiếu thu chi template (Cash Voucher Templates)

#### Mô tả
Bộ template phiếu thu, phiếu chi, ủy nhiệm chi, giấy đề nghị thanh toán — theo chuẩn mực kế toán VN. Đảm bảo đủ thông tin bắt buộc, dễ điền, dễ kiểm soát.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phần mềm kế toán tự in phiếu hay dùng phiếu tay?
2. Có cần song ngữ Việt-Anh không?
3. Quy định đánh số phiếu? (VD: PT-2024-001, PC-2024-001)
4. Mức chi tiền mặt tối đa? (theo quy định NH Nhà nước: > 20 triệu phải CK)
5. Có cần phiếu đề nghị tạm ứng riêng không?

#### Template gợi ý
Cấu trúc FRM — 4 mẫu phiếu:
- **Phiếu Thu** (PT): Theo mẫu TT200 — Header DN, số phiếu, ngày, người nộp, lý do, số tiền (số + chữ), tài khoản, chữ ký 4 bên
- **Phiếu Chi** (PC): Tương tự PT — người nhận, lý do chi, chứng từ kèm, chữ ký duyệt chi
- **Ủy nhiệm chi** (UNC): Mẫu ngân hàng — thông tin chuyển khoản, người thụ hưởng
- **Giấy đề nghị thanh toán** (ĐNTT): Người đề nghị, nội dung, số tiền, chứng từ đính kèm, cấp duyệt
- **(Tùy chọn) Giấy đề nghị tạm ứng**: Mục đích, số tiền, thời hạn hoàn ứng

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo bộ Phiếu thu chi template.

CONTEXT:
- DN: [Tên] — MST: [số]
- Phần mềm: [MISA / Fast / Tay]
- Bilingual: [Có/Không]
- Numbering: [convention]
- Tạm ứng: [Có/Không]
- Cơ sở: TT200/2014/TT-BTC hoặc TT133/2016/TT-BTC

FORMAT:
- 4-5 template riêng biệt, mỗi template 1 trang A4
- Header: Logo + Tên DN + MST + Địa chỉ
- Trường điền: [___] + gợi ý mẫu
- Số tiền: Bằng số + Bằng chữ
- Chữ ký: Đúng vị trí theo quy định (Giám đốc | KTT | Thủ quỹ | Người lập | Người nộp/nhận)
- Numbering format: [Loại]-[Năm]-[Số 3 chữ số]
- Hướng dẫn sử dụng ngắn gọn kèm mỗi mẫu

TONE: Kế toán chuẩn mực, form chính thức.
LENGTH: 5-7 trang A4 (mỗi mẫu 1 trang + 1-2 trang hướng dẫn).
```

---

### PROMPT 14: Bảng theo dõi công nợ (AR/AP Tracking Sheet)

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

### PROMPT 15: Bảng kê thuế GTGT (VAT Declaration Sheet)

#### Mô tả
Template bảng kê thuế GTGT đầu vào/đầu ra theo mẫu kê khai của Tổng cục Thuế. Hướng dẫn kê khai đúng, đủ, đúng hạn — giảm rủi ro bị phạt thuế.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phương pháp tính thuế GTGT? (Khấu trừ / Trực tiếp)
2. Kỳ kê khai? (Hàng tháng / Hàng quý — phụ thuộc doanh thu)
3. Phần mềm hỗ trợ kê khai? (HTKK, iHTKK, eTax, phần mềm kế toán tích hợp)
4. Có hàng hóa/dịch vụ thuộc diện thuế suất 0%, 5%, 8%, 10% không?
5. Có hoạt động XNK chịu thuế GTGT nhập khẩu không?

#### Template gợi ý
Cấu trúc FRM:
- **Hướng dẫn tổng quan**: Mẫu nào, nộp ở đâu, deadline, mức phạt chậm nộp
- **Bảng kê đầu ra** (Phụ lục 01-1/GTGT): Hóa đơn bán ra, giá trị, thuế suất, tiền thuế
- **Bảng kê đầu vào** (Phụ lục 01-2/GTGT): Hóa đơn mua vào, giá trị, thuế suất, tiền thuế được khấu trừ
- **Tờ khai 01/GTGT**: Tóm tắt thuế đầu ra - đầu vào = thuế phải nộp
- **Checklist trước khi nộp**: 10 mục kiểm tra
- **Lưu ý**: Hóa đơn không hợp lệ, hóa đơn quá hạn kê khai, kê khai bổ sung

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Bảng kê thuế GTGT (VAT Declaration Sheet).

CONTEXT:
- DN: [Tên] — MST: [số]
- Phương pháp: [Khấu trừ / Trực tiếp]
- Kỳ kê khai: [Tháng / Quý]
- Phần mềm: [HTKK / eTax / PM kế toán]
- Thuế suất áp dụng: [0% / 5% / 8% / 10%]
- XNK: [Có/Không]

FORMAT:
- Bảng kê đầu ra: STT | Hóa đơn số | Ngày | KH | MST KH | Giá trị CTV | Thuế suất | Tiền thuế
- Bảng kê đầu vào: STT | Hóa đơn số | Ngày | NCC | MST NCC | Giá trị CTV | Thuế suất | Tiền thuế
- Tờ khai tóm tắt: Tổng đầu ra | Tổng đầu vào | Thuế phải nộp | Thuế còn khấu trừ
- Pre-submission checklist: 10 mục ☐
- Lịch nộp thuế: 12 tháng × deadline + reminder T-5 ngày
- FAQ: 10 tình huống kê khai thường gặp

TONE: Thuế — chính xác, tuân thủ, reference cụ thể.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 16: Báo cáo P&L (Income Statement / Profit & Loss Report)

#### Mô tả
Template Báo cáo Kết quả Kinh doanh theo chuẩn mực kế toán Việt Nam (TT200 hoặc TT133). Bao gồm phân tích variance (so sánh kỳ trước, so sánh budget), và executive commentary.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Chế độ kế toán áp dụng? (TT200 cho DN lớn / TT133 cho SME)
2. Cần so sánh gì? (kỳ trước / cùng kỳ năm trước / budget / cả 3)
3. Có cần P&L theo segment? (theo sản phẩm / phòng ban / kênh bán)
4. Tần suất lập? (hàng tháng / hàng quý / hàng năm)
5. Ai đọc báo cáo này? (Giám đốc / HĐQT / Ngân hàng / Kiểm toán)

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — 3-5 dòng highlight: doanh thu, lợi nhuận, variance chính
- **P&L Statement** — Bảng chuẩn TT200/TT133: Doanh thu → Giá vốn → Lợi nhuận gộp → Chi phí → EBIT → Thuế → LNST
- **Variance Analysis** — Actual vs Budget | Actual vs Prior | Actual vs Prior Year
- **Segment P&L** — Theo SP/Phòng ban/Kênh (nếu cần)
- **Key Ratios** — Gross Margin, Operating Margin, Net Margin, Revenue growth
- **Commentary** — Giải thích top 5 variance lớn nhất

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template P&L Report (Báo cáo Kết quả Kinh doanh).

CONTEXT:
- DN: [Tên] — Chế độ: [TT200 / TT133]
- So sánh: [Prior period / Budget / Prior year / All]
- Segment: [SP / Phòng ban / Kênh / Không]
- Tần suất: [Tháng / Quý / Năm]
- Audience: [GĐ / HĐQT / NH / Kiểm toán]

FORMAT:
- P&L template theo đúng mẫu B02-DN (TT200) hoặc B02-DNN (TT133)
- Variance columns: Actual | Budget | Var $ | Var % | Prior | Var $ | Var %
- Ratio dashboard: 6 KPIs chính + trend arrow ↑↓→
- Segment breakdown (nếu có): Mỗi segment 1 mini P&L
- Commentary template: Top 5 variances + Root cause + Action
- Chart data: Revenue & Profit trend 12 tháng

TONE: Tài chính chính thức, phù hợp nộp cho kiểm toán/ngân hàng.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 17: Balance Sheet (Bảng Cân đối Kế toán)

#### Mô tả
Template Bảng Cân đối Kế toán theo chuẩn mực kế toán VN. Phân tích cơ cấu tài sản, nguồn vốn, và sự thay đổi qua các kỳ.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Chế độ kế toán? (TT200 / TT133)
2. Cần so sánh kỳ nào? (Cuối kỳ vs Đầu năm / Cuối kỳ trước)
3. Có tài sản cố định lớn không? (bất động sản, máy móc, phương tiện)
4. Có vay nợ dài hạn không? (ngân hàng, trái phiếu)
5. Tần suất lập? (hàng quý / hàng năm)

#### Template gợi ý
Cấu trúc RPT:
- **Balance Sheet Statement** — Mẫu B01-DN (TT200) / B01-DNN (TT133)
- **Tài sản**: Ngắn hạn (tiền, phải thu, hàng tồn, khác) + Dài hạn (TSCĐ, đầu tư, khác)
- **Nguồn vốn**: Nợ phải trả (ngắn hạn + dài hạn) + Vốn chủ sở hữu
- **Phân tích cơ cấu**: % từng khoản / Tổng tài sản
- **Phân tích biến động**: So sánh 2 kỳ, giải thích thay đổi lớn
- **Key Ratios**: Current Ratio, Quick Ratio, D/E, ROE, ROA

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Balance Sheet (Bảng Cân đối Kế toán).

CONTEXT:
- DN: [Tên] — Chế độ: [TT200 / TT133]
- So sánh: [Đầu năm / Cuối kỳ trước]
- TSCĐ: [Có/Không] — Giá trị lớn: [liệt kê]
- Vay nợ: [Có/Không] — Chi tiết: [ngắn hạn / dài hạn]

FORMAT:
- BS template theo mẫu B01-DN hoặc B01-DNN — 2 cột (Cuối kỳ | Đầu năm)
- Cơ cấu phân tích: % column cho mỗi khoản / Tổng
- Biến động: Thay đổi $ | Thay đổi % | Commentary
- Ratio cards: Current Ratio | Quick Ratio | D/E | ROE | ROA + benchmark
- Chart data: Tài sản structure pie + Nguồn vốn structure pie
- Working Capital analysis: CA - CL = NWC, trend

TONE: Tài chính chính thức.
LENGTH: 3-5 trang A4.
```

---

### PROMPT 18: Cash Flow Statement (Báo cáo Lưu chuyển Tiền tệ)

#### Mô tả
Template Báo cáo Lưu chuyển Tiền tệ theo chuẩn VN — phân tích 3 dòng tiền: hoạt động kinh doanh, hoạt động đầu tư, hoạt động tài chính. Hỗ trợ cả phương pháp trực tiếp và gián tiếp.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phương pháp lập? (Trực tiếp / Gián tiếp — hầu hết DN VN dùng gián tiếp)
2. Chế độ kế toán? (TT200 / TT133)
3. Có hoạt động đầu tư lớn không? (mua/bán TSCĐ, góp vốn liên doanh)
4. Có hoạt động tài chính? (vay/trả nợ, phát hành CP, chia cổ tức)

#### Template gợi ý
Cấu trúc RPT:
- **Phần I** — Dòng tiền từ HĐKD: LNTT → Điều chỉnh (KH, dự phòng, lãi vay...) → Thay đổi vốn lưu động → Tiền thuần HĐKD
- **Phần II** — Dòng tiền từ HĐ Đầu tư: Mua/bán TSCĐ, đầu tư, cho vay
- **Phần III** — Dòng tiền từ HĐ Tài chính: Vay/trả nợ, phát hành CP, cổ tức
- **Tổng hợp** — Net Cash Flow = I + II + III → Tiền đầu kỳ + Net = Tiền cuối kỳ
- **Phân tích** — Free Cash Flow, Cash Conversion Ratio

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Cash Flow Statement (Báo cáo Lưu chuyển Tiền tệ).

CONTEXT:
- DN: [Tên] — Phương pháp: [Trực tiếp / Gián tiếp]
- Chế độ: [TT200 / TT133]
- HĐ đầu tư: [Có/Không] — Chi tiết: [mô tả]
- HĐ tài chính: [Có/Không] — Chi tiết: [mô tả]

FORMAT:
- CFS template theo mẫu B03-DN (TT200) / B03-DNN (TT133)
- 3 phần rõ ràng: HĐKD | HĐ Đầu tư | HĐ Tài chính
- Reconciliation: Tiền đầu kỳ + Net Cash = Tiền cuối kỳ (= Balance Sheet)
- Analysis: Free Cash Flow = CFO - CapEx
- Cash Conversion: NI → CFO → Ratio → Interpretation
- Chart data: 3 dòng tiền × 12 tháng, stacked bar

TONE: Tài chính chính thức.
LENGTH: 3-5 trang A4.
```

---

### PROMPT 19: Dashboard Tài chính tháng (Monthly Financial Dashboard)

#### Mô tả
Dashboard tài chính tổng hợp 1 trang — executive summary cho Giám đốc/HĐQT. Gồm KPI cards, trend charts, traffic light indicators, và key highlights/actions.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Top 8-10 KPIs tài chính muốn theo dõi? (VD: Revenue, GP%, NI, Cashflow, AR/AP, DSO...)
2. So sánh gì? (vs Budget / vs Prior Month / vs Prior Year)
3. Format: PDF 1 trang / Google Sheets live / PowerBI / Markdown?
4. Ai đọc? (Giám đốc hàng tháng / HĐQT hàng quý)
5. Có cần phần commentary hay chỉ số liệu?

#### Template gợi ý
Cấu trúc RPT:
- **Header** — Tháng/Năm, DN, "DASHBOARD TÀI CHÍNH"
- **KPI Cards** — 8-10 cards: Metric | Actual | Target | Variance | ↑↓ | 🟢🟡🔴
- **P&L Summary** — Mini P&L: Revenue → GP → EBITDA → NI (actual vs budget)
- **Cashflow Summary** — Inflow | Outflow | Net | Balance → trend line
- **AR/AP Summary** — Total | Overdue | DSO | DPO
- **Top 3 Highlights** — Điểm tích cực
- **Top 3 Concerns** — Điểm cần chú ý + Action required
- **Next Month Outlook** — Dự báo / kế hoạch

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Dashboard Tài chính tháng.

CONTEXT:
- DN: [Tên]
- KPIs: [liệt kê 8-10 KPIs]
- So sánh: [Budget / Prior / Both]
- Format: [PDF 1 trang / Sheets / Markdown]
- Audience: [GĐ / HĐQT]

FORMAT:
- 1 trang A4 duy nhất — compact, visual, scannable
- KPI cards: 2 hàng × 4-5 cột — Metric | Value | vs Target | Trend | Status light
- Mini P&L: 6 dòng max — Revenue → COGS → GP → SGA → EBITDA → NI
- Cash position: Balance + trend sparkline data
- AR/AP: Pie chart data (Current vs Overdue)
- Traffic light: 🟢 On track | 🟡 Watch | 🔴 Action needed
- Commentary: Max 3 bullets highlights + 3 bullets concerns
- Action items: Owner | Due date

TONE: Executive — concise, visual, action-oriented.
LENGTH: 1 trang A4 (+ 1 trang hướng dẫn điền).
```

---

### PROMPT 20: Thuyết minh BCTC (Notes to Financial Statements)

#### Mô tả
Template Thuyết minh Báo cáo Tài chính — giải thích chi tiết các chính sách kế toán áp dụng, chi tiết số liệu trên BCTC, và các sự kiện quan trọng. Bắt buộc theo Luật Kế toán VN.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Chế độ kế toán? (TT200 / TT133)
2. Chính sách kế toán đặc thù? (VD: phương pháp khấu hao, tính giá HTK, ghi nhận doanh thu)
3. Có giao dịch đặc biệt trong kỳ? (sáp nhập, thanh lý, kiện tụng, cam kết lớn)
4. Có bên liên quan cần công bố không? (giao dịch nội bộ, cổ đông lớn)
5. Có sự kiện sau ngày lập BCTC cần thuyết minh?

#### Template gợi ý
Cấu trúc RPT:
- **Phần I** — Thông tin DN: Tên, MST, ngành, vốn, nhân sự
- **Phần II** — Chuẩn mực & Chế độ kế toán áp dụng
- **Phần III** — Chính sách kế toán chủ yếu: Ngoại tệ, HTK, TSCĐ, Doanh thu, Chi phí, Thuế
- **Phần IV** — Chi tiết khoản mục BCTC: Mỗi khoản trọng yếu → breakdown chi tiết
- **Phần V** — Giao dịch bên liên quan
- **Phần VI** — Cam kết & Nợ tiềm tàng
- **Phần VII** — Sự kiện sau ngày BCTC
- **Phần VIII** — Thông tin bổ sung: Segment, EPS, cổ tức

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Thuyết minh BCTC (Notes to Financial Statements).

CONTEXT:
- DN: [Tên] — MST: [số] — Chế độ: [TT200 / TT133]
- Chính sách đặc thù: [liệt kê]
- Giao dịch đặc biệt: [liệt kê hoặc "không có"]
- Bên liên quan: [Có/Không]
- Cơ sở: Luật Kế toán 2015, VAS, TT200/TT133

FORMAT:
- Theo mẫu B09-DN (TT200) / B09-DNN (TT133)
- Chia phần rõ ràng, đánh số mục liên tục
- Chính sách kế toán: Mỗi chính sách 1 đoạn ngắn, rõ ràng
- Chi tiết khoản mục: Bảng Khoản mục | Đầu kỳ | Tăng | Giảm | Cuối kỳ
- Bên liên quan: Bảng Tên | Quan hệ | Giao dịch | Giá trị | Dư nợ
- Placeholder cho từng phần: [Điền thông tin DN cụ thể]
- Lưu ý kiểm toán: Highlight khoản mục trọng yếu

TONE: Kế toán chuẩn mực, chính thức, đủ để nộp kiểm toán.
LENGTH: 8-15 trang A4.
```

---

## Ghi chú triển khai

### Dependencies
- `chinh-sach-tai-chinh-tong-quat.md` là file gốc — tất cả file khác phải tuân thủ nguyên tắc trong đây
- `quy-che-chi-tieu-noi-bo.md` là "sách gối đầu giường" của toàn công ty — phải rõ ràng, dễ hiểu
- `co-cau-chi-phi-ccsc.md` và `ngan-sach-nam-budget.md` là input cho `scenario-planning` và `break-even`
- `sop-ke-toan-thang.md` orchestrate các SOP thu chi, đối soát → tạo output cho 4 file báo cáo tài chính
- `rpt-dashboard-tai-chinh-thang.md` tổng hợp data từ P&L, BS, CFS

### Lưu ý pháp lý
> **QUAN TRỌNG**: Các template kế toán trong skill này tuân theo Chuẩn mực Kế toán Việt Nam (VAS), TT200/2014/TT-BTC (DN lớn) hoặc TT133/2016/TT-BTC (SME). DN CẦN xác nhận chế độ kế toán áp dụng trước khi sử dụng. Nên tham khảo kế toán trưởng/kiểm toán viên trước khi áp dụng chính thức.

### Thứ tự tạo khuyến nghị
1. Chính sách tài chính tổng quát → 2. Quy chế chi tiêu → 3. Chính sách công nợ → 4. Chính sách định giá
5. Cơ cấu chi phí → 6. Ngân sách năm → 7. Cashflow Forecast → 8. Scenario Planning → 9. Break-Even
10. SOP Thu chi → 11. SOP Đối soát → 12. SOP Monthly Close
13. Phiếu thu chi → 14. Bảng theo dõi công nợ → 15. Bảng kê thuế GTGT
16. P&L → 17. Balance Sheet → 18. Cash Flow Statement → 19. Thuyết minh BCTC → 20. Dashboard tài chính

---

### VIII.5 — BP People (Nhân Sự & Con Người)

> **Tầng 2: Bộ Máy** — 27 tài liệu: Cơ cấu tổ chức (4), Chính sách nhân sự (6), Tuyển dụng & Onboarding (7), Đánh giá & Phát triển (5), Văn hóa & Gắn kết (5).

---

### PROMPT 01: Sơ đồ tổ chức (Organization Chart)

#### Mô tả
Sơ đồ tổ chức chính thức của DN — thể hiện cấu trúc phòng ban, tuyến báo cáo (reporting lines), span of control. Là "bản đồ quyền lực" giúp mọi người hiểu ai báo cáo ai, ai chịu trách nhiệm gì.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Cơ cấu hiện tại có bao nhiêu phòng ban/bộ phận?
2. Tổng nhân sự hiện tại? Phân bổ theo phòng ban?
3. Cấu trúc: Functional (theo chức năng) / Divisional (theo sản phẩm/địa bàn) / Matrix?
4. Có vị trí nào đang trống (vacant) cần tuyển?
5. Có kế hoạch thay đổi cơ cấu trong 6-12 tháng tới?
6. Mối quan hệ đặc biệt: dotted-line, kiêm nhiệm, outsource?

#### Template gợi ý
Cấu trúc MAN:
- **Tổng quan**: Loại cấu trúc, số cấp quản lý, tổng headcount
- **Org Chart**: Sơ đồ dạng Mermaid — từ HĐQT/CEO xuống phòng ban
- **Bảng chi tiết**: Phòng ban | Trưởng phòng | Headcount | Chức năng chính | Reporting to
- **Span of Control**: Phân tích — mỗi manager quản lý bao nhiêu người
- **Vacant Positions**: Vị trí đang trống + timeline tuyển dụng
- **Planned Changes**: Thay đổi dự kiến + timeline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sơ đồ tổ chức (Organization Chart).

CONTEXT:
- DN: [Tên] — Quy mô: [nhân sự] — Cấu trúc: [Functional / Divisional / Matrix]
- Phòng ban: [liệt kê]
- Headcount per dept: [chi tiết]
- Vị trí trống: [liệt kê]
- Thay đổi dự kiến: [mô tả]

FORMAT:
- Mermaid org chart: Từ HĐQT → CEO → C-level → Trưởng phòng → Team
- Bảng chi tiết: Dept | Head | HC | Function | Reports to | Dotted line
- Span of control: Manager | Direct reports | Ratio → Highlight nếu >7
- Color coding: Filled 🟢 | Vacant 🔴 | Planned 🟡
- Metrics: Total HC | Mgr:Staff ratio | Avg span of control | Layers

TONE: Chính thức, visual, rõ ràng.
LENGTH: 3-5 trang A4.
```

---

### PROMPT 02: JD Template chung (Standard Job Description Template)

#### Mô tả
Template JD (Job Description) chuẩn hóa dùng cho MỌI vị trí trong DN. Đảm bảo format thống nhất, đủ thông tin, dễ tuyển dụng và đánh giá.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN có chuẩn năng lực (Competency Framework) chưa?
2. JD cần bilingual Việt-Anh không?
3. Có cần liên kết JD với thang lương không?
4. Format: Markdown / Word / Google Doc?

#### Template gợi ý
Cấu trúc FRM — Các section trong JD:
- **Header**: Chức danh (VI + EN), Phòng ban, Cấp bậc, Báo cáo cho, Quản lý trực tiếp
- **Mục đích vị trí**: 2-3 câu tóm tắt lý do tồn tại của vị trí
- **Trách nhiệm chính**: 5-8 bullets, ưu tiên theo tầm quan trọng
- **KPIs chính**: 3-5 KPIs đo lường hiệu quả
- **Yêu cầu**: Học vấn, kinh nghiệm, kỹ năng cứng, kỹ năng mềm, chứng chỉ
- **Năng lực cốt lõi**: Theo Competency Framework (nếu có)
- **Điều kiện làm việc**: Giờ làm, địa điểm, đi công tác, remote
- **Quyền lợi**: Lương range, phúc lợi highlights
- **Career Path**: Vị trí tiếp theo có thể thăng tiến

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo JD Template chung (Standard Job Description Template).

CONTEXT:
- DN: [Tên] — Competency Framework: [Có/Không]
- Bilingual: [Có/Không]
- Liên kết thang lương: [Có/Không]
- Format: [Markdown / Word / GDoc]

FORMAT:
- Template 1 trang A4 — trường điền [___]
- Header bảng: Chức danh | Dept | Level | Reports to | Manages | Date
- Trách nhiệm: Numbered list + % thời gian dành cho mỗi trách nhiệm
- KPIs: Bảng KPI | Target | Measurement | Frequency
- Yêu cầu: Chia Must-have vs Nice-to-have
- Năng lực: Bảng Competency | Level Required (Basic/Intermediate/Advanced/Expert)
- Hướng dẫn điền: 1 trang — mẹo viết JD hiệu quả

TONE: HR chuyên nghiệp, rõ ràng, hấp dẫn ứng viên.
LENGTH: 2 trang A4 (template + hướng dẫn).
```

---

### PROMPT 03: JD các vị trí chủ chốt (Key Position Job Descriptions)

#### Mô tả
4 bản JD chi tiết cho các vị trí chủ chốt thường gặp nhất ở SME: Giám đốc Kinh doanh, Trưởng phòng Marketing, Kế toán Trưởng, Nhân viên Kinh doanh. Customize theo ngành và quy mô DN.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ngành nghề DN? (ảnh hưởng yêu cầu chuyên môn)
2. Quy mô hiện tại? (JD cho DN 10 người khác DN 100 người)
3. Mức lương dự kiến cho mỗi vị trí? (để viết phần quyền lợi)
4. Vị trí nào đang cần tuyển gấp nhất?
5. Có cần thêm/bớt vị trí nào khác?

#### Template gợi ý
Mỗi JD theo format chuẩn ở PROMPT 02, nhưng chi tiết đầy đủ:
- **GĐ Kinh Doanh**: Quản lý đội sales, chiến lược bán hàng, target doanh số, phát triển kênh
- **TP Marketing**: Brand, digital marketing, content, budget marketing, ROI campaigns
- **Kế Toán Trưởng**: Hệ thống kế toán, BCTC, thuế, kiểm toán, tuân thủ
- **NV Kinh Doanh**: Tư vấn bán hàng, chăm sóc KH, đạt target, báo cáo

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo JD 4 vị trí chủ chốt.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Quy mô: [nhân sự]
- Mức lương: GĐ KD [range] | TP MKT [range] | KTT [range] | NV KD [range]
- Vị trí cần gấp: [tên vị trí]
- Thay đổi/bổ sung: [liệt kê nếu có]

FORMAT:
- 4 JD riêng biệt, mỗi JD 1.5-2 trang A4
- Theo format chuẩn: Header → Mục đích → Trách nhiệm (8-10 bullets) → KPIs (5) → Yêu cầu → Năng lực → Quyền lợi
- Customize theo ngành: VD Sales ở SaaS khác Sales ở FMCG
- KPIs cụ thể và đo lường được: VD "Đạt 100% target doanh số quý" thay vì "Bán hàng tốt"
- Trách nhiệm xếp theo % thời gian: 40% Selling | 20% Managing | 20% Planning | 20% Reporting

TONE: Chuyên nghiệp, hấp dẫn — vừa là tài liệu nội bộ vừa dùng tuyển dụng.
LENGTH: 6-8 trang A4 (4 JD × 1.5-2 trang).
```

---

### PROMPT 04: Headcount Plan (Kế hoạch Nhân sự)

#### Mô tả
Kế hoạch nhân sự tổng thể — hiện tại bao nhiêu, cần tuyển bao nhiêu, khi nào, budget bao nhiêu. Liên kết trực tiếp với chiến lược kinh doanh và ngân sách.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Headcount hiện tại theo phòng ban?
2. Kế hoạch kinh doanh 12 tháng tới? (tăng trưởng doanh thu → cần thêm nhân sự?)
3. Tỷ lệ nghỉ việc (turnover) hiện tại?
4. Budget nhân sự (payroll) hiện tại % doanh thu?
5. Có kế hoạch mở chi nhánh / sản phẩm mới cần team mới?

#### Template gợi ý
Cấu trúc MAN:
- **Current State**: Bảng phòng ban × HC hiện tại × Chi phí
- **Gap Analysis**: So sánh HC hiện tại vs HC cần thiết theo chiến lược
- **Hiring Plan**: Timeline tuyển theo quý — vị trí | dept | Q1 | Q2 | Q3 | Q4 | Priority
- **Budget Impact**: Payroll forecast — hiện tại + incremental + total
- **Turnover Forecast**: Dự báo nghỉ việc + replacement plan
- **Ratios**: Revenue per employee, Cost per hire, Time to fill

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Headcount Plan (Kế hoạch Nhân sự).

CONTEXT:
- DN: [Tên] — HC hiện tại: [số] — Per dept: [chi tiết]
- Kế hoạch tăng trưởng: [mô tả]
- Turnover: [%/năm]
- Payroll/Revenue ratio: [%]
- Mở rộng: [chi nhánh / sản phẩm mới nếu có]

FORMAT:
- Current state: Dept | Current HC | Avg Salary | Total Cost | Revenue/employee
- Gap analysis: Dept | Current | Needed | Gap | Priority | Justification
- Hiring timeline: Gantt-style Q1-Q4 × vị trí
- Budget forecast: Monthly payroll × 12 tháng → Total + YoY change
- Turnover model: Dept | Rate | Expected exits | Replacement cost
- Summary KPIs: Total HC plan | New hires | Budget impact | Cost per hire

TONE: Chiến lược, data-driven, liên kết với business plan.
LENGTH: 5-8 trang A4.
```

---

### PROMPT 05: Nội quy lao động (Internal Labor Regulations)

#### Mô tả
Nội quy lao động — văn bản BẮT BUỘC theo BLLĐ 2019 (Điều 118-122). DN từ 10 nhân viên trở lên phải ban hành bằng văn bản và đăng ký tại Sở LĐTBXH. Quy định thời giờ, kỷ luật, ATVSLĐ, bảo vệ tài sản, bí mật kinh doanh.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Giờ làm việc? (8h/ngày? Ca kíp? Flexible?)
2. Có làm thêm giờ thường xuyên không? (quy định OT)
3. Các hành vi kỷ luật cụ thể cần liệt kê? (ngành đặc thù có quy định riêng)
4. Có tài sản / bí mật kinh doanh đặc biệt cần bảo vệ?
5. Yêu cầu ATVSLĐ đặc thù ngành? (nhà máy / công trường / văn phòng)
6. Có trang phục / đồng phục bắt buộc không?

#### Template gợi ý
Cấu trúc POL — theo Điều 118 BLLĐ 2019:
- **Chương I** — Quy định chung: Phạm vi, đối tượng
- **Chương II** — Thời giờ làm việc, nghỉ ngơi: Giờ làm, nghỉ trưa, nghỉ tuần, OT
- **Chương III** — Trật tự tại nơi làm việc: Trang phục, hành vi, sử dụng tài sản
- **Chương IV** — An toàn, vệ sinh lao động: Quy tắc ATVSLĐ
- **Chương V** — Bảo vệ tài sản, bí mật kinh doanh, SHTT
- **Chương VI** — Phòng chống quấy rối tình dục (bắt buộc theo NĐ 145/2020)
- **Chương VII** — Kỷ luật lao động: Hình thức kỷ luật, quy trình xử lý
- **Chương VIII** — Trách nhiệm vật chất
- **Chương IX** — Điều khoản thi hành

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Nội quy lao động (Internal Labor Regulations).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- Giờ làm: [giờ bắt đầu-kết thúc] — Nghỉ: [thứ mấy]
- OT: [Có/Không] — Tần suất: [mô tả]
- ATVSLĐ đặc thù: [mô tả]
- Đồng phục: [Có/Không]
- Cơ sở pháp lý: BLLĐ 2019 (Điều 118-122), NĐ 145/2020

FORMAT:
- Chia chương theo đúng 8 nội dung bắt buộc của Điều 118
- Ngôn ngữ pháp lý nhưng dễ hiểu cho mọi NV
- Bảng giờ làm: Ngày | Giờ bắt đầu | Giờ kết thúc | Nghỉ trưa
- Bảng kỷ luật: Vi phạm | Mức độ | Hình thức xử lý | Ghi chú
- Phần phòng chống QRTD: Định nghĩa + Kênh tố cáo + Quy trình xử lý
- Footer: Ngày ban hành, đăng ký Sở LĐTBXH, có hiệu lực từ

TONE: Pháp lý, nghiêm túc, tuân thủ luật VN.
LENGTH: 12-18 trang A4.

LƯU Ý: PHẢI đăng ký tại Sở LĐTBXH trong 10 ngày kể từ ngày ban hành. Nên nhờ luật sư lao động rà soát.
```

---

### PROMPT 06: Quy chế lương thưởng (Compensation & Benefits Policy)

#### Mô tả
Quy chế chi tiết về cơ cấu lương (cứng + KPI + thưởng), thang bảng lương, quy trình xét lương, chính sách tăng lương, thưởng hiệu suất, thưởng cuối năm.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Cơ cấu lương hiện tại? (100% cứng / 70-30 / 50-50 cứng-KPI?)
2. Có thang bảng lương rõ ràng chưa?
3. Tần suất xét lương? (hàng năm / 6 tháng)
4. Chính sách thưởng: tháng 13? Thưởng KPI? Thưởng dự án? Equity?
5. Lương thử việc = bao nhiêu % lương chính thức?
6. Có benchmark lương theo thị trường không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Nguyên tắc trả lương: Công bằng, cạnh tranh, liên kết hiệu suất
- **Phần 2** — Cơ cấu thu nhập: Lương cứng + Lương KPI + Phụ cấp + Thưởng
- **Phần 3** — Thang bảng lương: Grade/Level × Min-Mid-Max
- **Phần 4** — Quy trình xét lương: Timeline, tiêu chí, approval
- **Phần 5** — Chính sách thưởng: Thưởng KPI, thưởng cuối năm, thưởng đột xuất
- **Phần 6** — Phụ cấp: Ăn trưa, đi lại, điện thoại, chức vụ, độc hại
- **Phần 7** — Lương thử việc, lương part-time, lương OT
- **Phụ lục**: Thang bảng lương chi tiết, Bảng phụ cấp

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế lương thưởng (Compensation & Benefits Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- Cơ cấu lương: [VD: 70% cứng + 30% KPI]
- Thang lương: [Có/Không] — Số bậc: [số]
- Xét lương: [tần suất]
- Thưởng: [tháng 13 / KPI / dự án / equity]
- Thử việc: [% lương chính thức]

FORMAT:
- Cơ cấu visual: Pie chart — Lương cứng | KPI | Phụ cấp | Thưởng
- Thang bảng lương: Bảng Grade | Level | Min | Mid | Max | Notes
- Quy trình xét lương: Flowchart — NV tự đánh giá → Manager review → HR calibration → GĐ approve
- Bảng thưởng: Loại thưởng | Điều kiện | Công thức | Thời điểm chi | Approval
- Bảng phụ cấp: Loại | Mức | Đối tượng | Ghi chú
- FAQ: 10 câu phổ biến về lương thưởng

TONE: Nội bộ, rõ ràng, công bằng — NV phải hiểu được quyền lợi.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 07: Chính sách phúc lợi (Employee Benefits Policy)

#### Mô tả
Chính sách phúc lợi toàn diện — bao gồm BHXH/BHYT/BHTN bắt buộc theo luật VN và phúc lợi bổ sung (BH sức khỏe private, du lịch, sinh nhật, hỗ trợ học tập, team building...). Đây là công cụ giữ chân nhân tài quan trọng bên cạnh lương.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có BH sức khỏe private bổ sung không? (hãng nào, mức nào?)
2. Có chương trình du lịch/nghỉ mát hàng năm không? Budget?
3. Phúc lợi sinh nhật/lễ tết: quà hiện vật hay tiền mặt? Mức?
4. Hỗ trợ học tập/đào tạo? (học phí, chứng chỉ, hội thảo)
5. Phúc lợi đặc biệt: gym, canteen, nursery, flexible hours?
6. Có phân cấp phúc lợi theo level/thâm niên không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích: Thu hút, giữ chân, tạo động lực
- **Phần 2** — Bảo hiểm bắt buộc: BHXH, BHYT, BHTN — tỷ lệ đóng DN/NV, quyền lợi
- **Phần 3** — Bảo hiểm bổ sung: BH sức khỏe, BH tai nạn private — hãng, mức, quyền lợi
- **Phần 4** — Phúc lợi tài chính: Hỗ trợ ăn trưa, xăng xe, điện thoại, nhà ở
- **Phần 5** — Phúc lợi tinh thần: Du lịch, teambuilding, sinh nhật, hiếu hỷ, quà lễ
- **Phần 6** — Phúc lợi phát triển: Đào tạo, chứng chỉ, hội thảo, sách
- **Phần 7** — Phúc lợi theo cấp bậc: Level → quyền lợi bổ sung
- **Phụ lục**: Bảng tổng hợp phúc lợi, So sánh với thị trường

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách phúc lợi (Employee Benefits Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- BH bổ sung: [Có/Không] — Hãng: [tên] — Mức: [basic/premium]
- Du lịch: [Có/Không] — Budget: [số/người/năm]
- Sinh nhật/lễ: [mức]
- Đào tạo: [có/không] — Budget: [số/người/năm]
- Phúc lợi đặc biệt: [liệt kê]
- Cơ sở pháp lý: Luật BHXH 2014, Luật BHYT 2008 (sửa đổi 2014)

FORMAT:
- Bảng tổng hợp 1 trang: Loại PL | Mô tả | Giá trị | Đối tượng | Tần suất
- BHXH/BHYT breakdown: Bảng tỷ lệ đóng DN | NV | Tổng — theo quy định hiện hành
- BH bổ sung: Bảng quyền lợi | Hạn mức | Cách sử dụng | Claim process
- Calendar phúc lợi: 12 tháng × sự kiện/quyền lợi (du lịch T6, thưởng Tết T1...)
- Per-level benefits: Bảng Level | Base benefits | Additional benefits
- FAQ: 10 câu phổ biến — "Bao giờ được hưởng BH?", "Du lịch có bắt buộc không?"

TONE: Thân thiện, positive — NV phải thấy đây là quyền lợi, không phải gánh nặng.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 08: Chính sách nghỉ phép (Leave Policy)

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

### PROMPT 09: Chính sách làm việc từ xa (Remote/Hybrid Work Policy)

#### Mô tả
Chính sách quy định điều kiện, quy tắc, và kỳ vọng khi nhân viên làm việc từ xa (Work From Home) hoặc hybrid. Bao gồm thiết bị, bảo mật, giờ làm, giao tiếp, đánh giá hiệu suất khi remote.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mô hình: Full remote / Hybrid (mấy ngày WFH/tuần) / Case-by-case?
2. Vị trí nào được phép remote? (Sales field OK, Kế toán cần tại VP?)
3. Có hỗ trợ thiết bị/chi phí internet cho NV WFH không?
4. Yêu cầu bảo mật: VPN? Không dùng WiFi công cộng? Khóa màn hình?
5. Cách giám sát/đánh giá: output-based hay time-tracking?
6. Chính sách về không gian làm việc tại nhà? (yên tĩnh, bàn ghế, ánh sáng)

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Phạm vi áp dụng: Ai được remote, điều kiện, phê duyệt
- **Phần 2** — Mô hình làm việc: Full remote / Hybrid / Flexible — quy tắc mỗi loại
- **Phần 3** — Thiết bị & Chi phí: DN cung cấp gì, NV tự chuẩn bị gì, hỗ trợ internet
- **Phần 4** — Giờ làm & Availability: Core hours, meeting hours, response time
- **Phần 5** — Bảo mật khi WFH: VPN, device lock, clean desk, guest restriction
- **Phần 6** — Giao tiếp & Collaboration: Tools, daily check-in, weekly sync
- **Phần 7** — Đánh giá hiệu suất: Output-based, KPIs, 1-on-1 frequency
- **Phần 8** — Thu hồi quyền remote: Khi nào, quy trình

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách làm việc từ xa (Remote/Hybrid Work Policy).

CONTEXT:
- DN: [Tên] — Mô hình: [Full remote / Hybrid / Case-by-case]
- WFH ngày/tuần: [số] — Vị trí eligible: [liệt kê]
- Hỗ trợ thiết bị: [Có/Không] — Chi phí: [mô tả]
- Bảo mật: VPN [Có/Không] — Giám sát: [output / time-tracking]
- Tools: [Slack/Teams/Zoom/Asana...]

FORMAT:
- Eligibility matrix: Phòng ban/Vị trí | Full Remote | Hybrid | Office only | Điều kiện
- Equipment checklist: Thiết bị | DN cung cấp | NV tự chuẩn bị | Hỗ trợ chi phí
- Core hours: Timeline visual — Flexible zone | Core hours (phải online) | Flexible zone
- Security checklist: 8-10 mục bảo mật bắt buộc khi WFH ☐
- Communication protocol: Loại vấn đề | Kênh | Response time expected
- Performance review: KPI remote-specific + 1-on-1 frequency tăng khi remote
- Revocation triggers: 3-5 điều kiện → thu hồi quyền remote + quy trình

TONE: Cân bằng tin tưởng & kiểm soát, hiện đại, linh hoạt nhưng rõ ràng.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 10: Quy chế bảo mật thông tin (Information Security Policy)

#### Mô tả
Quy chế phân loại thông tin, quy tắc bảo mật, quyền truy cập, xử lý vi phạm bảo mật. Bổ sung cho NDA trong 01-Governance — NDA là cam kết pháp lý, còn đây là quy tắc hành vi hàng ngày về bảo mật.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phân loại thông tin: mấy mức? (VD: Public / Internal / Confidential / Secret)
2. Dữ liệu nhạy cảm: KH, tài chính, công nghệ, nhân sự — cái nào quan trọng nhất?
3. Chính sách BYOD (Bring Your Own Device): Cho phép không?
4. Social media: NV có được đăng về công ty không? Quy tắc?
5. Quy trình khi phát hiện rò rỉ/vi phạm bảo mật?
6. Có DPO (Data Protection Officer) hoặc IT Security riêng không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích, Phạm vi, Định nghĩa
- **Phần 2** — Phân loại thông tin: 4 mức + ví dụ mỗi mức + cách xử lý
- **Phần 3** — Quyền truy cập: Ma trận Role × Loại thông tin → Access level
- **Phần 4** — Quy tắc bảo mật hàng ngày: Password, khóa máy, clean desk, chia sẻ file
- **Phần 5** — BYOD & Thiết bị cá nhân: Cho phép/không, điều kiện
- **Phần 6** — Social media: Được/không được nói gì về công ty
- **Phần 7** — Xử lý sự cố bảo mật: Phát hiện → Báo cáo → Cách ly → Điều tra → Khắc phục
- **Phần 8** — Vi phạm & Hình thức xử lý: Nhắc nhở → Kỷ luật → Sa thải → Pháp lý

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế bảo mật thông tin (Information Security Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Nhân sự: [số]
- Phân loại: [Public / Internal / Confidential / Secret]
- Dữ liệu nhạy cảm nhất: [KH / Tài chính / Công nghệ / Nhân sự]
- BYOD: [Cho phép / Không / Có điều kiện]
- DPO/IT Security: [Có/Không]
- Liên kết: NDA trong 01-Governance

FORMAT:
- Classification matrix: Mức | Định nghĩa | Ví dụ | Ai được access | Cách lưu trữ | Cách chia sẻ | Cách hủy
- Access control: Role × Info type = Read/Write/None — bảng ma trận
- Daily security rules: 10 quy tắc — poster-friendly, treo gần máy tính
- BYOD rules: Thiết bị | Cho phép | Điều kiện | MDM required
- Social media dos/don'ts: 5 được + 5 không
- Incident response flowchart: Mermaid — Phát hiện → Báo IT → Cách ly → GĐ → Điều tra → Report
- Violation penalties: Bảng Vi phạm | Mức 1 (nhắc) | Mức 2 (kỷ luật) | Mức 3 (sa thải/pháp lý)

TONE: Nghiêm túc, bảo mật, nhưng viết đủ dễ hiểu cho non-tech.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 11: SOP Tuyển dụng (Recruitment Process SOP)

#### Mô tả
Quy trình tuyển dụng end-to-end chuẩn hóa — từ khi phòng ban gửi yêu cầu nhân sự đến khi ứng viên nhận việc. Đảm bảo tuyển đúng người, đúng thời điểm, đúng ngân sách.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Bao nhiêu vòng phỏng vấn? (1 vòng / 2 vòng / 3 vòng)
2. Ai tham gia phỏng vấn mỗi vòng? (HR / Hiring Manager / CEO)
3. Kênh tuyển dụng chính? (website, TopCV, LinkedIn, referral, headhunter)
4. Time-to-hire mục tiêu? (từ khi đăng tin đến khi nhận việc)
5. Có probation review chính thức sau thử việc không?
6. Có chương trình Employee Referral không?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Yêu cầu nhân sự: Hiring Manager submit form → HR + Finance approve budget
- **Bước 2** — Đăng tin & Sourcing: Kênh, nội dung, budget quảng cáo
- **Bước 3** — Sàng lọc CV: Tiêu chí, công cụ, shortlist
- **Bước 4** — Phỏng vấn: Vòng 1 (HR screen) → Vòng 2 (Technical/Hiring Manager) → Vòng 3 (CEO nếu cần)
- **Bước 5** — Đánh giá & Quyết định: Scorecard tổng hợp, reference check
- **Bước 6** — Offer: Đàm phán, gửi offer letter, chờ accept
- **Bước 7** — Pre-boarding → Onboarding

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Tuyển dụng (Recruitment Process).

CONTEXT:
- DN: [Tên] — Số vòng PV: [số] — Kênh: [liệt kê]
- Người tham gia: Vòng 1 [___] | Vòng 2 [___] | Vòng 3 [___]
- Time-to-hire target: [ngày]
- Referral program: [Có/Không]

FORMAT:
- Flowchart tổng: Mermaid — 7 bước + decision points + timeline
- RACI per step: Bước | HR | Hiring Mgr | Finance | CEO
- Timeline: Gantt — Day 1 (đăng tin) → Day X (nhận việc)
- Templates kèm: Manpower Request Form, Interview Schedule, Reference Check Form
- KPIs tuyển dụng: Time to fill | Cost per hire | Quality of hire | Offer acceptance rate
- Checklist per step: Mỗi bước 3-5 mục cần hoàn thành

TONE: SOP chuẩn, process-driven, hiệu quả.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 12: Bộ câu hỏi phỏng vấn (Structured Interview Question Bank)

#### Mô tả
Bộ câu hỏi phỏng vấn cấu trúc (Structured Interview) — đảm bảo mọi ứng viên được hỏi cùng bộ câu hỏi, đánh giá công bằng. Chia thành câu hỏi chung (culture fit), theo nhóm năng lực, và theo vị trí cụ thể.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Core Values của DN? (câu hỏi culture fit xoay quanh values)
2. Competency Framework có chưa? (năng lực cốt lõi cần đánh giá)
3. Vị trí cần bộ câu hỏi riêng? (sales, marketing, kế toán, IT...)
4. Phong cách phỏng vấn: Behavioral (STAR) / Situational / Case study?
5. Có dùng bài test kỹ năng kèm không?

#### Template gợi ý
Cấu trúc FRM:
- **Phần A** — Câu hỏi chung (10-15 câu): Culture fit, motivation, career goal, teamwork
- **Phần B** — Câu hỏi theo năng lực (20 câu): Leadership, problem-solving, communication, adaptability, integrity
- **Phần C** — Câu hỏi theo vị trí (10 câu/vị trí): Sales, Marketing, Finance, Tech
- **Phần D** — Red flags & Deal breakers: Tín hiệu cảnh báo cần chú ý
- **Hướng dẫn**: Cách dùng STAR method để đánh giá câu trả lời

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Bộ câu hỏi phỏng vấn cấu trúc (Structured Interview Question Bank).

CONTEXT:
- DN: [Tên] — Core Values: [liệt kê]
- Competency Framework: [Có/Không] — Năng lực cốt lõi: [liệt kê]
- Vị trí sample: [Sales / Marketing / Kế toán / IT]
- Phong cách: [Behavioral STAR / Situational / Mixed]

FORMAT:
- 3 nhóm: Chung (culture fit) | Theo năng lực | Theo vị trí
- Mỗi câu: Câu hỏi + Gợi ý đánh giá (What to listen for) + Thang điểm 1-5
- STAR guide: Situation → Task → Action → Result — hướng dẫn interviewer probe
- 30 câu chung + 20 câu năng lực + 10 câu per vị trí sample
- Red flags checklist: 8-10 tín hiệu cảnh báo
- Rubric per câu: Điểm 1 (Yếu) → 3 (Đạt) → 5 (Xuất sắc) — mô tả cụ thể

TONE: HR chuyên nghiệp, objective, giúp interviewer không bị bias.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 13: Scorecard đánh giá ứng viên (Candidate Evaluation Scorecard)

#### Mô tả
Bảng đánh giá ứng viên sau phỏng vấn — tổng hợp điểm theo tiêu chí có trọng số, đưa ra quyết định Go/No-Go khách quan. Dùng cho từng interviewer và tổng hợp panel.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Bao nhiêu tiêu chí đánh giá? (thường 8-12)
2. Trọng số mỗi tiêu chí? (VD: Kinh nghiệm 25%, Culture fit 20%, Kỹ năng 20%...)
3. Thang điểm: 1-5 hay 1-10?
4. Bao nhiêu interviewer cùng đánh giá? (cần form cá nhân + form tổng hợp)
5. Quyết định: Majority vote hay consensus?

#### Template gợi ý
Cấu trúc FRM:
- **Individual Scorecard**: 1 form per interviewer — Tiêu chí × Điểm × Notes
- **Panel Summary**: Tổng hợp tất cả interviewers — so sánh trên 1 bảng
- **Decision Framework**: Score thresholds → Hire / Maybe / No Hire
- **Comparison View**: Ứng viên A vs B vs C — side by side

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Scorecard đánh giá ứng viên (Candidate Evaluation Scorecard).

CONTEXT:
- DN: [Tên] — Số tiêu chí: [8-12]
- Trọng số: [VD: KN 25% | Kỹ năng 20% | Culture 20% | Communication 15% | Problem Solving 10% | Motivation 10%]
- Thang điểm: [1-5 / 1-10]
- Số interviewers: [số]
- Quyết định: [Majority / Consensus]

FORMAT:
- Individual form: Bảng Tiêu chí | Trọng số | Điểm 1-5 | Evidence/Notes
- Rubric mỗi tiêu chí: Score 1 (mô tả) → 3 (mô tả) → 5 (mô tả)
- Weighted score: Formula rõ ràng — Sum(Weight × Score) = Total
- Panel summary: Bảng Tiêu chí | Interviewer 1 | 2 | 3 | Average | Weighted
- Decision thresholds: ≥[X] Strongly Hire 🟢 | ≥[Y] Hire 🟡 | ≥[Z] Maybe 🟠 | <[Z] No Hire 🔴
- Comparison matrix: 3 ứng viên × 12 tiêu chí — highlight top scorer per tiêu chí

TONE: Objective, quantitative, bias-free.
LENGTH: 2-3 trang A4.
```

---

### PROMPT 14: Thư mời nhận việc (Offer Letter)

#### Mô tả
Template thư mời nhận việc (Offer Letter) chuyên nghiệp — gửi cho ứng viên đã được chọn. Bao gồm chức danh, lương, phúc lợi, ngày bắt đầu, điều kiện, và hạn phản hồi. Đây là ấn tượng đầu tiên chính thức với NV tương lai.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có letterhead/branding chuẩn không?
2. Offer letter cần bilingual Việt-Anh không?
3. Thông tin nào bắt buộc có? (lương, thử việc, ngày bắt đầu, báo cáo cho ai)
4. Có kèm điều kiện gì? (background check, giấy khám sức khỏe, bằng cấp)
5. Hạn phản hồi offer: bao nhiêu ngày?
6. Ai ký offer? (GĐ / HR Manager)

#### Template gợi ý
Cấu trúc FRM:
- **Header**: Logo + "THƯ MỜI NHẬN VIỆC / OFFER LETTER"
- **Chào mừng**: Lời chúc mừng cá nhân hóa
- **Thông tin vị trí**: Chức danh, phòng ban, báo cáo cho, ngày bắt đầu
- **Compensation**: Lương gross/net, cơ cấu (cứng + KPI), thử việc
- **Benefits summary**: Top 5 phúc lợi nổi bật
- **Điều kiện**: Giấy tờ cần nộp, background check, thời hạn thử việc
- **Hạn phản hồi**: Ngày cụ thể
- **Chữ ký**: Giám đốc/HR Manager
- **Phụ lục**: Danh sách tài liệu kèm (HĐ lao động, JD, NDA)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Thư mời nhận việc (Offer Letter).

CONTEXT:
- DN: [Tên] — Bilingual: [Có/Không]
- Người ký: [GĐ / HR Manager]
- Điều kiện kèm: [background check / khám SK / bằng cấp]
- Hạn phản hồi: [số ngày]
- Tài liệu kèm: [HĐLĐ / JD / NDA / Nội quy]

FORMAT:
- Header: Logo + DN info + "THƯ MỜI NHẬN VIỆC"
- Body: Chúc mừng → Vị trí & Phòng ban → Ngày bắt đầu → Lương (Gross | Net | Cơ cấu) → Thử việc (% lương, thời gian) → Benefits highlights → Điều kiện → Hạn phản hồi
- Attachment checklist: Danh sách tài liệu NV cần mang ngày nhận việc
- Acceptance section: "Tôi đồng ý nhận vị trí..." + Chữ ký ứng viên + Ngày
- Chữ ký: Tên + Chức danh + DN
- Tone: Chuyên nghiệp nhưng ấm áp — tạo hào hứng cho NV mới

TONE: Chuyên nghiệp, welcome, ấn tượng tốt.
LENGTH: 2 trang A4.
```

---

### PROMPT 15: SOP Tiếp nhận nhân viên mới (New Employee Onboarding SOP)

#### Mô tả
Quy trình tiếp nhận NV mới end-to-end — từ trước ngày nhận việc (pre-boarding), ngày đầu tiên (Day 1), tuần đầu (Week 1), đến tháng đầu tiên (Month 1). Đảm bảo NV mới hòa nhập nhanh, productive sớm.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Trước ngày nhận việc: IT chuẩn bị gì? (email, laptop, access) Mất bao lâu?
2. Day 1: Ai đón? Tour VP? Welcome kit? Training gì?
3. Có buddy/mentor program không?
4. Thử việc bao lâu? (1 tháng / 2 tháng — tùy HĐLĐ)
5. Ai chịu trách nhiệm onboarding? (HR / Manager / Buddy)
6. Có orientation session chung cho batch NV mới không?

#### Template gợi ý
Cấu trúc SOP:
- **Pre-boarding (T-7 đến T-1)**: IT setup, email/access, workspace, welcome email, tài liệu đọc trước
- **Day 1**: Đón tiếp → Tour VP → Giới thiệu team → IT handover → Sổ tay NV → Lunch with manager
- **Week 1**: Training sản phẩm/quy trình → Gặp stakeholders → Buddy assign → Task đầu tiên
- **Month 1**: Check-in weekly → Training chuyên sâu → OKR/KPI cá nhân → Feedback 30 ngày
- **RACI**: HR | Manager | Buddy | IT | Admin — per task

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Tiếp nhận nhân viên mới (Onboarding SOP).

CONTEXT:
- DN: [Tên] — Buddy program: [Có/Không]
- IT setup time: [số ngày]
- Thử việc: [1 / 2 tháng]
- Batch orientation: [Có/Không]
- Người phụ trách: HR [___] | Manager [___] | Buddy [___]

FORMAT:
- Timeline visual: Pre-boarding → Day 1 → Week 1 → Month 1 — Mermaid/Gantt
- Pre-boarding checklist: 10-12 mục ☐ + Owner + Deadline (T-7 đến T-1)
- Day 1 schedule: Giờ × Hoạt động × Người phụ trách × Địa điểm
- Week 1 plan: Ngày × Topic × Trainer × Output
- RACI per phase: Task | HR | Manager | Buddy | IT | Admin
- Welcome email template: Gửi T-3 — giới thiệu team, địa chỉ, parking, dress code
- Feedback form 30 ngày: 10 câu hỏi cho NV mới + 5 câu cho Manager

TONE: Welcoming, organized, NV mới phải thấy "công ty này chuyên nghiệp."
LENGTH: 5-7 trang A4.
```

---

### PROMPT 16: Sổ tay nhân viên (Employee Handbook)

#### Mô tả
Sổ tay nhân viên (Employee Handbook) — tài liệu "all-in-one" cho NV mới và NV hiện tại. Tổng hợp tóm tắt mọi thông tin cần biết: giới thiệu công ty, văn hóa, chính sách, quy trình, phúc lợi, contacts. Tham chiếu đến file gốc thay vì copy full nội dung.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có thư chào mừng từ CEO không? (personal touch)
2. Giới thiệu công ty: lịch sử, sứ mệnh, tầm nhìn, giá trị đã có trong 02-Strategy?
3. Tone mong muốn: formal / friendly / startup-vibe?
4. Có cần bản digital (PDF đẹp) hay markdown là đủ?
5. Tần suất cập nhật: hàng năm / khi có thay đổi?

#### Template gợi ý
Cấu trúc MAN:
- **Lời chào CEO**: 1 trang — welcome letter cá nhân hóa
- **Về công ty**: Lịch sử, VMV, Core Values, Sản phẩm, Team (tóm tắt)
- **Văn hóa**: Culture Code tóm tắt, rituals, norms
- **Chính sách**: Tóm tắt + link đến file gốc — Lương, phúc lợi, nghỉ phép, remote, bảo mật
- **Quy trình**: Tóm tắt + link — Xin phép, thanh toán, báo cáo, mua sắm
- **Phúc lợi**: Highlight top benefits — bảng tóm 1 trang
- **FAQ**: 20 câu NV mới hay hỏi
- **Contacts**: HR, IT, Admin, quản lý trực tiếp

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sổ tay nhân viên (Employee Handbook).

CONTEXT:
- DN: [Tên] — CEO letter: [Có/Không]
- Tone: [Formal / Friendly / Startup-vibe]
- VMV + Core Values: [tóm tắt hoặc link 02-Strategy]
- Format: [Markdown / PDF]

FORMAT:
- Mục lục: Rõ ràng, clickable (nếu digital)
- CEO letter: 1 trang — personal, inspiring
- Về công ty: 2-3 trang — lịch sử timeline, VMV, team photo placeholder
- Văn hóa: 2 trang — values hành vi hóa, dos/don'ts
- Chính sách tóm tắt: 3-5 trang — mỗi chính sách 1/2 trang + "Chi tiết xem: [link file gốc]"
- Quy trình tóm tắt: 2-3 trang — flowchart đơn giản + link
- Benefits highlight: 1 trang bảng — Top 10 quyền lợi
- FAQ: 2 trang — 20 câu + trả lời ngắn
- Directory: 1 trang — Dept | Contact person | Email | SĐT

TONE: Sổ tay — dễ đọc, thân thiện, NV MUỐN đọc chứ không PHẢI đọc.
LENGTH: 20-30 trang A4.
```

---

### PROMPT 17: Checklist Onboarding 30-60-90 ngày (30-60-90 Day Onboarding Checklist)

#### Mô tả
Checklist mục tiêu và tasks cho NV mới theo 3 mốc: Day 30 (Học & Hiểu), Day 60 (Bắt đầu đóng góp), Day 90 (Tự chủ & Đánh giá chính thức). Giúp NV và Manager align kỳ vọng, đo lường tiến bộ.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Thử việc bao lâu? (30-60-90 phải nằm trong hoặc bao quát thời gian thử việc)
2. Vị trí sample để customize: Sales / Marketing / Kế toán / IT?
3. Ai đánh giá ở mỗi mốc? (Manager / HR / cả hai)
4. Có liên kết với KPI/OKR cá nhân không?
5. Hậu quả nếu không đạt mốc 90? (gia hạn thử việc / chấm dứt)

#### Template gợi ý
Cấu trúc FRM:
- **Day 30 — Học & Hiểu**: Hiểu sản phẩm, quy trình, team, tools. Output: có thể mô tả quy trình cốt lõi.
- **Day 60 — Bắt đầu đóng góp**: Tự thực hiện task, đóng góp ý tưởng, handle case đầu tiên. Output: có output đo lường được.
- **Day 90 — Tự chủ & Review**: Tự chủ hoàn toàn, đạt KPI cơ bản, đánh giá chính thức pass/fail.

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Checklist Onboarding 30-60-90 ngày.

CONTEXT:
- DN: [Tên] — Thử việc: [1 / 2 tháng]
- Vị trí sample: [Sales / Marketing / Kế toán / IT]
- Đánh giá bởi: [Manager / HR / Both]
- Liên kết KPI: [Có/Không]

FORMAT:
- 3 bảng riêng biệt (Day 30, 60, 90): Goal | Tasks | Support needed | Measurement | Status ☐
- Day 30: 8-10 tasks — học, quan sát, hiểu
- Day 60: 8-10 tasks — thực hành, đóng góp, feedback
- Day 90: 8-10 tasks — tự chủ, đạt KPI, review chính thức
- Check-in schedule: Tuần 1 (daily) → Tuần 2-4 (weekly) → Tháng 2-3 (bi-weekly)
- Review form per mốc: 5 câu Manager đánh giá + 5 câu NV tự đánh giá
- Decision at Day 90: Pass ✅ | Extend probation ⏳ | Terminate ❌ — criteria rõ ràng

TONE: Supportive, goal-oriented, NV mới thấy được lộ trình rõ ràng.
LENGTH: 3-4 trang A4.
```

---

### PROMPT 18: SOP Nghỉ việc (Offboarding / Resignation SOP)

#### Mô tả
Quy trình xử lý khi NV nghỉ việc — từ nhận đơn, bàn giao, thanh toán, đến exit interview. Tuân thủ BLLĐ 2019 về thời hạn báo trước, quyền lợi thanh toán. Đảm bảo DN không bị gián đoạn, NV nghỉ trọn vẹn.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Thời hạn báo trước: theo luật (30 ngày / 45 ngày) hay quy định riêng?
2. Ai nhận đơn nghỉ việc? (Manager trước hay HR trước?)
3. Quy trình bàn giao: bao nhiêu ngày? Ai giám sát?
4. Thanh toán: phép chưa dùng, lương, thưởng, BHXH — timeline?
5. Có exit interview không? Ai thực hiện?
6. Thu hồi tài sản/access: IT revoke, thẻ, chìa khóa — timeline?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Nhận đơn nghỉ việc: Form, báo trước, duyệt
- **Bước 2** — Thông báo nội bộ: Ai cần biết, khi nào, cách thức
- **Bước 3** — Bàn giao công việc: Danh mục, người nhận, timeline, biên bản
- **Bước 4** — Thu hồi tài sản & Access: IT, Admin, thẻ, chìa, tài liệu
- **Bước 5** — Thanh toán: Lương còn, phép chưa dùng, thưởng, BHXH
- **Bước 6** — Exit Interview: Câu hỏi, người thực hiện, báo cáo
- **Bước 7** — Cập nhật hệ thống: HR records, payroll, org chart

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Nghỉ việc (Offboarding / Resignation Process).

CONTEXT:
- DN: [Tên] — Báo trước: [30 / 45 ngày]
- Nhận đơn: [Manager / HR]
- Bàn giao: [số ngày]
- Exit interview: [Có/Không] — Người thực hiện: [HR / Manager]
- Cơ sở pháp lý: BLLĐ 2019 (Điều 35-38, 48)

FORMAT:
- Flowchart tổng: Mermaid — Đơn → Duyệt → Bàn giao → Thu hồi → Thanh toán → Exit PV → Close
- Timeline: Ngày nhận đơn (D0) → Bàn giao (D+X) → Ngày cuối (D+30/45) → Thanh toán (D+14 sau ngày cuối)
- Bàn giao checklist: Công việc | Tài sản | Tài khoản/MK | Tài liệu | Công nợ/KH
- IT revoke checklist: Email | Laptop | Access | Cloud | VPN | Badge — ☐ + Owner + Deadline
- Thanh toán checklist: Lương | Phép | Thưởng | BHXH sổ | Thuế TNCN quyết toán
- Exit interview: 10 câu hỏi + template báo cáo → HR summary cho Management
- Lưu ý pháp lý: Thời hạn trả sổ BHXH (≤14 ngày), thanh toán đầy đủ

TONE: SOP chuẩn, tuân thủ pháp luật, tôn trọng NV nghỉ.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 19: Biên bản bàn giao công việc (Work Handover Record)

#### Mô tả
Template biên bản bàn giao công việc khi NV nghỉ việc hoặc chuyển vị trí — ghi nhận đầy đủ: công việc đang làm, tài sản, tài khoản, tài liệu, công nợ, khách hàng đang quản lý. Có chữ ký 3 bên: NV nghỉ + Người nhận + Trưởng phòng.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Các hạng mục bàn giao bắt buộc? (tùy vị trí: Sales bàn giao KH, Kế toán bàn giao sổ sách)
2. Bàn giao tài sản: laptop, điện thoại, xe, thẻ — quy trình kiểm tra?
3. Bàn giao tài khoản: email, CRM, phần mềm, MXH công ty — ai tiếp nhận?
4. Có cần bàn giao công nợ / khách hàng đang chăm sóc không?
5. Ai ký duyệt biên bản? (3 bên hay thêm HR?)

#### Template gợi ý
Cấu trúc FRM:
- **Header**: Thông tin NV bàn giao + Người nhận + Ngày
- **Phần 1** — Công việc đang thực hiện: Task | Status | Deadline | Ghi chú
- **Phần 2** — Tài sản: Mã TS | Tên | Tình trạng | Ghi chú
- **Phần 3** — Tài khoản & Mật khẩu: Hệ thống | Account | Đã chuyển quyền ☐
- **Phần 4** — Tài liệu: Danh mục | Vị trí lưu | Đã bàn giao ☐
- **Phần 5** — Công nợ & Khách hàng: KH | Dư nợ | Status | Người tiếp nhận
- **Chữ ký**: NV bàn giao | Người nhận | Trưởng phòng | HR (nếu cần)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Biên bản bàn giao công việc (Work Handover Record).

CONTEXT:
- DN: [Tên]
- Hạng mục bắt buộc: [Công việc / Tài sản / Tài khoản / Tài liệu / Công nợ-KH]
- Ký duyệt: [3 bên / 4 bên (thêm HR)]

FORMAT:
- 1 form template 2-3 trang A4
- Header: DN info | NV bàn giao (tên, chức danh, phòng ban, ngày cuối) | Người nhận (tên, chức danh)
- Bảng công việc: # | Task | Status (Hoàn thành/Đang làm/Chờ) | Deadline | Ghi chú cho người nhận
- Bảng tài sản: # | Mã TS | Tên | Serial# | Tình trạng | Đã thu hồi ☐
- Bảng tài khoản: # | Hệ thống | Username | Đã reset MK ☐ | Đã chuyển quyền ☐
- Bảng tài liệu: # | Tên TL | Vị trí lưu (folder/drive) | Đã bàn giao ☐
- Bảng KH/Công nợ: # | KH | Công nợ | Status | Người tiếp nhận | Ghi chú
- Footer chữ ký: 3-4 ô ký — Người bàn giao | Người nhận | TP | HR
- Ghi chú: Vấn đề tồn đọng + timeline giải quyết

TONE: Form chính thức, đầy đủ, tránh tranh chấp sau nghỉ việc.
LENGTH: 2-3 trang A4.
```

---

### PROMPT 20: Chính sách đánh giá hiệu suất (Performance Evaluation Policy)

#### Mô tả
Chính sách đánh giá hiệu suất NV — quy định tần suất, phương pháp, thang đánh giá, liên kết với lương/thăng tiến, và quy trình appeal. Là nền tảng cho KPI, 360, và toàn bộ hệ thống performance management.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tần suất đánh giá? (Quý / 6 tháng / Năm)
2. Phương pháp: MBO / OKR / KPI / BSC / Mixed?
3. Thang đánh giá: 1-5 (Outstanding → Poor) hay A-E?
4. Liên kết lương: đánh giá ảnh hưởng tăng lương bao nhiêu %?
5. Liên kết thăng tiến: cần mấy kỳ đánh giá tốt để lên level?
6. Có appeal/khiếu nại kết quả đánh giá không?

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích: Cải thiện hiệu suất, phát triển NV, cơ sở cho lương/thăng tiến
- **Phần 2** — Phạm vi & Đối tượng: Áp dụng cho ai, từ khi nào (sau thử việc)
- **Phần 3** — Phương pháp: MBO/OKR/KPI/BSC — khi nào dùng cái nào
- **Phần 4** — Chu kỳ & Timeline: Calendar đánh giá, deadline mỗi bước
- **Phần 5** — Thang đánh giá: Rating scale + mô tả chi tiết mỗi mức
- **Phần 6** — Quy trình: NV tự đánh giá → Manager đánh giá → Calibration → Feedback → Sign-off
- **Phần 7** — Liên kết C&B: Rating → % tăng lương, thưởng, thăng tiến
- **Phần 8** — Appeal mechanism: Quy trình khiếu nại kết quả
- **Phụ lục**: Calendar đánh giá, Rating distribution guideline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách đánh giá hiệu suất (Performance Evaluation Policy).

CONTEXT:
- DN: [Tên] — Nhân sự: [số]
- Tần suất: [Quý / 6 tháng / Năm]
- Phương pháp: [MBO / OKR / KPI / BSC / Mixed]
- Thang: [1-5 / A-E]
- Liên kết lương: [mô tả]
- Liên kết thăng tiến: [mô tả]
- Appeal: [Có/Không]

FORMAT:
- Rating scale: Bảng Score | Label | Mô tả | % NV kỳ vọng (bell curve guide)
- Quy trình flowchart: Mermaid — Set goals → Mid-review → Self-assess → Manager assess → Calibrate → Feedback → Sign-off
- Calendar: Timeline 12 tháng × milestones đánh giá
- C&B linkage matrix: Rating | % tăng lương | Thưởng multiplier | Thăng tiến eligible
- Calibration guide: Forced distribution vs Absolute scale — pros/cons
- Appeal flowchart: NV khiếu nại → HR review → Committee → Quyết định cuối
- FAQ: 10 câu phổ biến — "KPI chưa có thì đánh giá thế nào?", "Mới vào 3 tháng có đánh giá?"

TONE: Công bằng, minh bạch, phát triển — không phải trừng phạt.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 21: KPI cá nhân template (Individual KPI Template)

#### Mô tả
Template KPI cá nhân theo Balanced Scorecard 4 perspectives — giúp NV và Manager thiết lập, theo dõi, và đánh giá KPIs hàng quý/năm. Mỗi KPI có formula, target, trọng số, actual, và score tự tính.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Framework: BSC 4 perspectives hay KPI đơn giản?
2. Số KPIs per người: 5-8 (recommended) hay nhiều hơn?
3. Format SMART đầy đủ không? (Specific, Measurable, Achievable, Relevant, Time-bound)
4. Trọng số: Manager quyết hay NV tự đề xuất?
5. Scoring: Linear (đạt 80% target = 80 điểm) hay Step (≥100% = A, 80-99% = B...)?
6. Có link với OKR công ty không?

#### Template gợi ý
Cấu trúc FRM:
- **Header**: NV | Chức danh | Phòng ban | Kỳ đánh giá | Manager
- **BSC 4 Perspectives**: Financial | Customer | Internal Process | Learning & Growth
- **Mỗi KPI**: Tên | Formula | Unit | Target | Weight | Actual | Score
- **Tổng score**: Weighted average → Rating conversion
- **Comments**: NV tự nhận xét + Manager nhận xét
- **Sign-off**: NV + Manager + HR

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo KPI cá nhân template (Individual KPI Template — BSC).

CONTEXT:
- DN: [Tên]
- Framework: [BSC 4 perspectives / Simple KPI]
- Số KPIs: [5-8]
- Scoring: [Linear / Step]
- Link OKR: [Có/Không]

FORMAT:
- Template 1-2 trang A4
- BSC layout: 4 quadrants — Financial | Customer | Internal Process | Learning
- Mỗi KPI row: # | Perspective | KPI Name | Formula | Unit | Target | Weight% | Actual | Achievement% | Score
- Weight validation: Sum = 100%
- Score formula: Achievement% × Weight = Weighted Score → Sum all = Total
- Rating conversion: Total ≥90 = A (Outstanding) | 80-89 = B (Good) | 70-79 = C (Meets) | 60-69 = D (Below) | <60 = E (Poor)
- SMART checklist: Mỗi KPI tự kiểm tra 5 tiêu chí SMART ☐
- Example KPIs: 2-3 ví dụ per perspective cho vị trí Sales/Marketing/Operations

TONE: Performance management, analytical, dễ điền.
LENGTH: 2-3 trang A4.
```

---

### PROMPT 22: Form đánh giá 360 độ (360-Degree Feedback Form)

#### Mô tả
Form đánh giá 360 độ — thu thập phản hồi từ 4 góc: tự đánh giá (Self), cấp trên (Manager), đồng nghiệp (Peer), cấp dưới (Direct Report). Đánh giá theo năng lực (competencies) thay vì KPI — bổ sung cho KPI template.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Năng lực cần đánh giá? (VD: Leadership, Communication, Teamwork, Problem Solving, Innovation, Integrity...)
2. Số competencies: 8-12 hay nhiều hơn?
3. Thang điểm: 1-5 hay 1-7?
4. Có open comments không? (bắt buộc hay tùy chọn)
5. Ẩn danh: Peer và Direct Report có ẩn danh không?
6. Tần suất: Hàng năm / 6 tháng?

#### Template gợi ý
Cấu trúc FRM:
- **Form Self**: NV tự đánh giá — 20-25 statements × scale 1-5
- **Form Manager**: Cấp trên đánh giá — cùng statements
- **Form Peer**: Đồng nghiệp (2-3 người) — cùng statements + ẩn danh
- **Form Direct Report**: Cấp dưới (nếu có) — cùng statements + ẩn danh
- **Summary**: Radar chart data — so sánh Self vs Manager vs Peer vs DR
- **Development Plan**: Gap analysis → 2-3 điểm cần cải thiện → Action plan

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Form đánh giá 360 độ (360-Degree Feedback Form).

CONTEXT:
- DN: [Tên] — Competencies: [liệt kê 8-12]
- Thang điểm: [1-5 / 1-7]
- Open comments: [Bắt buộc / Tùy chọn]
- Ẩn danh Peer/DR: [Có/Không]
- Tần suất: [6 tháng / Năm]

FORMAT:
- 4 form riêng: Self | Manager | Peer | Direct Report
- Mỗi competency: 2-3 behavioral statements × scale 1-5
  VD: "Leadership" → "Truyền cảm hứng cho team đạt mục tiêu" [1-2-3-4-5]
- Rubric per score: 1 = Hiếm khi thể hiện | 3 = Thường xuyên | 5 = Luôn luôn, role model
- Open comment section: "Điểm mạnh nhất?" + "Cần cải thiện gì?" + "Lời khuyên?"
- Summary template: Bảng Competency | Self | Manager | Peer Avg | DR Avg | Gap (Self vs Others)
- Radar chart data: 8-12 axes × 4 sources
- Development plan: Top 3 gaps → Action | Timeline | Support needed | Success measure

TONE: Constructive, development-focused, không phải performance review tiêu cực.
LENGTH: 4-6 trang A4 (4 forms + summary + dev plan).
```

---

### PROMPT 23: Career Path / Lộ trình thăng tiến (Career Progression Framework)

#### Mô tả
Tài liệu Career Path — mô tả lộ trình thăng tiến cho từng track nghề nghiệp trong DN. Phân biệt Individual Contributor (IC) track và Management track. Mỗi level có điều kiện, kỹ năng, salary band, và timeline kỳ vọng.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có bao nhiêu career track? (VD: Sales, Marketing, Tech, Operations, Finance)
2. Mỗi track có bao nhiêu level? (VD: Junior → Senior → Lead → Manager → Director)
3. Có IC track riêng không? (Senior → Principal → Staff — không cần quản lý người)
4. Điều kiện thăng tiến: thâm niên? đánh giá? chứng chỉ? dự án?
5. Salary band per level đã có chưa? (liên kết với thang bảng lương)
6. Timeline kỳ vọng: bao lâu ở mỗi level? (VD: Junior 1-2 năm → Senior 2-3 năm)

#### Template gợi ý
Cấu trúc MAN:
- **Tổng quan**: Triết lý phát triển nghề nghiệp, cam kết DN
- **Career Framework**: Sơ đồ tổng thể — tất cả tracks và levels
- **Per Track**: Level | Title | Scope | Key skills | Competency level | Salary band | Timeline
- **IC vs Management**: Rẽ nhánh từ level nào, điều kiện mỗi nhánh
- **Promotion Criteria**: Bảng checklist — đánh giá + thâm niên + skills + project
- **Cross-functional**: Có thể chuyển track không? Điều kiện?

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Career Path / Lộ trình thăng tiến (Career Progression Framework).

CONTEXT:
- DN: [Tên] — Tracks: [Sales / Marketing / Tech / Ops / Finance]
- Levels per track: [Junior → Senior → Lead → Manager → Director]
- IC track: [Có/Không]
- Salary band: [Có/Không] — Link thang lương: [Có/Không]
- Timeline: [VD: 1-2 năm per level]

FORMAT:
- Career map visual: Ladder diagram — tất cả tracks + levels + rẽ nhánh IC/Management
- Per-track detail: Bảng Level | Title | Scope (quản lý gì) | Key Skills | Min Experience | Salary Band
- IC vs Mgmt fork: Diagram — từ Senior → rẽ IC (Principal → Staff) hoặc Mgmt (Manager → Director)
- Promotion checklist: Bảng Criteria | Weight | Evidence required | Assessed by
  - Performance rating ≥ B liên tiếp [X] kỳ
  - Thâm niên ≥ [Y] năm tại level hiện tại
  - Competency đạt level tiếp theo
  - Project/đóng góp nổi bật
- Cross-functional rules: Điều kiện + quy trình chuyển track
- Example path: 2-3 ví dụ thực tế — "Sales Intern → NV KD → Senior → Sales Manager trong 5 năm"

TONE: Inspirational, rõ ràng — NV phải thấy con đường phía trước.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 24: Training Plan năm (Annual Training Plan)

#### Mô tả
Kế hoạch đào tạo năm — phân tích nhu cầu đào tạo (Training Needs Analysis), lịch đào tạo theo tháng, budget, nhà cung cấp đào tạo, và đo lường hiệu quả sau đào tạo (Kirkpatrick 4 levels).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có TNA (Training Needs Analysis) chưa? Gap skills nào lớn nhất?
2. Budget đào tạo: bao nhiêu % doanh thu hoặc số tuyệt đối?
3. Hình thức: In-house / External / Online / Mixed?
4. Chủ đề ưu tiên: Kỹ năng mềm? Chuyên môn? Leadership? Compliance?
5. Có mandatory training không? (ATVSLĐ, PCCC, compliance)
6. Cách đo ROI đào tạo: Kirkpatrick / đơn giản (pre-post test)?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Training Needs Analysis: Dept | Current skill | Required skill | Gap | Priority
- **Phần 2** — Training Calendar: 12 tháng × chủ đề × đối tượng × hình thức
- **Phần 3** — Budget: Chủ đề | Provider | Cost | Participants | Cost per head
- **Phần 4** — Provider list: Nội bộ (trainer) + Bên ngoài (đối tác)
- **Phần 5** — Mandatory Training: ATVSLĐ, PCCC, Compliance — timeline bắt buộc
- **Phần 6** — Đo lường hiệu quả: Kirkpatrick 4 levels (Reaction → Learning → Behavior → Results)
- **Phụ lục**: Training request form, Post-training evaluation form

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Training Plan năm (Annual Training Plan).

CONTEXT:
- DN: [Tên] — Nhân sự: [số]
- Budget: [số hoặc % doanh thu]
- Gap chính: [liệt kê top 3-5]
- Hình thức: [In-house / External / Online / Mixed]
- Mandatory: [ATVSLĐ / PCCC / Compliance / khác]
- Đo lường: [Kirkpatrick / Pre-post test / Đơn giản]

FORMAT:
- TNA matrix: Dept | Role | Current Level | Required Level | Gap | Training Need | Priority (H/M/L)
- Calendar 12 tháng: Bảng Tháng | Chủ đề | Đối tượng | Hình thức | Trainer | Duration | Budget
- Budget summary: Bảng Category | Budget | Actual | Variance — by topic + by dept
- Provider directory: Tên | Chuyên môn | Cost range | Rating | Contact
- Kirkpatrick tracker: Training | L1 (Survey) | L2 (Test score) | L3 (Behavior change) | L4 (Business impact)
- ROI formula: (Business Impact - Training Cost) / Training Cost × 100%
- Post-training eval form template: 10 câu (Reaction + Learning)

TONE: Đầu tư phát triển, strategic, data-driven.
LENGTH: 5-8 trang A4.
```

---

### PROMPT 25: Bộ quy tắc văn hóa DN (Culture Code)

#### Mô tả
Culture Code — tài liệu "hành vi hóa" Core Values của DN. Mỗi value được dịch thành hành vi cụ thể (Do this / Don't do this), kèm rituals, norms, và what we celebrate. Đây là "linh hồn" của DN — phải được sống hàng ngày, không chỉ treo trên tường.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Core Values hiện tại? (từ 02-Strategy VMV)
2. Mỗi value có hành vi cụ thể chưa? (VD: "Trung thực" = hành vi gì?)
3. Rituals hiện có? (Daily standup? Friday sharing? Monthly celebration?)
4. Norms giao tiếp? (gọi nhau thế nào? disagree thế nào? email vs chat?)
5. Celebrate gì? (đạt target, innovation, teamwork, tenure?)
6. Anti-patterns: Hành vi nào KHÔNG được chấp nhận?

#### Template gợi ý
Cấu trúc MAN:
- **Lời mở đầu CEO**: Tại sao văn hóa quan trọng
- **Core Values hành vi hóa**: Mỗi value → 3-5 Do this + 3-5 Don't do this
- **Rituals**: Daily | Weekly | Monthly | Quarterly | Annual — mô tả mỗi ritual
- **Norms**: Cách communicate, cách disagree, cách give feedback, cách celebrate
- **What We Celebrate**: Hành vi/kết quả nào được tôn vinh + cách tôn vinh
- **Anti-patterns**: Hành vi không được chấp nhận — dù giỏi đến đâu
- **Design**: Thân thiện, visual, poster-able — NV muốn đọc và share

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Culture Code (Bộ quy tắc Văn hóa DN).

CONTEXT:
- DN: [Tên] — Core Values: [liệt kê 3-5 values]
- Rituals hiện có: [liệt kê]
- Celebrate: [đạt target / innovation / tenure / teamwork]
- Anti-patterns: [liệt kê hành vi không chấp nhận]

FORMAT:
- CEO statement: 1 đoạn ngắn — "Tại sao chúng tôi tin vào..."
- Per Value (3-5 values): Tên value → Ý nghĩa (1 câu) → DO this (3-5 hành vi cụ thể) → DON'T do this (3-5 hành vi) → Ví dụ thực tế
- Rituals calendar: Bảng Tần suất | Ritual | Mô tả | Ai tổ chức | Purpose
- Communication norms: Bảng Tình huống | Cách đúng | Cách sai
  VD: "Không đồng ý" → "Trao đổi 1-on-1, đưa data" → "Nói xấu sau lưng"
- Recognition program: Loại | Tiêu chí | Phần thưởng | Tần suất | Nominated by
- Anti-patterns poster: 5-7 hành vi "Even if you're a top performer, this is NOT OK"
- Design note: Layout poster-friendly — có thể in A3 treo VP

TONE: Inspirational, authentic, sống động — KHÔNG phải corporate BS.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 26: Chương trình gắn kết NV (Employee Engagement Program)

#### Mô tả
Chương trình gắn kết NV 12 tháng — lịch hoạt động team building, recognition, wellbeing, learning, social. Mục tiêu: tăng eNPS, giảm turnover, xây dựng tinh thần đồng đội. Budget và measurement cho mỗi hoạt động.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Budget engagement/năm? (tổng hoặc per head)
2. Hoạt động hiện có? (team building, sinh nhật, sports day...)
3. Pain points gắn kết hiện tại? (NV không tham gia? Thiếu recognition? Burnout?)
4. Nhân sự remote nhiều không? (cần hoạt động virtual?)
5. Frequency mong muốn: 1 event/tháng? 1 event/quý?
6. eNPS hiện tại (nếu biết)?

#### Template gợi ý
Cấu trúc MAN:
- **Mục tiêu**: eNPS target, turnover target, participation rate
- **Categories**: Recognition | Team Building | Wellbeing | Learning | Social
- **12-Month Calendar**: Mỗi tháng 1 hoạt động chính + hoạt động thường xuyên
- **Budget per activity**: Bảng chi tiết
- **Virtual engagement**: Cho team remote/hybrid
- **Measurement**: Participation rate, eNPS before/after, NV feedback

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chương trình gắn kết NV (Employee Engagement Program).

CONTEXT:
- DN: [Tên] — Nhân sự: [số] — Remote: [% remote]
- Budget: [số/năm hoặc per head]
- Pain points: [thiếu recognition / burnout / low participation / team silo]
- eNPS hiện tại: [số hoặc "chưa đo"]
- Hoạt động hiện có: [liệt kê]

FORMAT:
- 12-month calendar: Bảng Tháng | Theme | Main Event | Category | Budget | Participants | Owner
  VD: T1 = New Year Kickoff | T6 = Mid-year Party | T12 = Year-end Gala
- Category breakdown: Bảng Category | Events/year | Budget allocation | Goal
  - Recognition: Employee of Month, Spot bonus, Shoutout channel
  - Team Building: Quarterly offsite, Monthly lunch
  - Wellbeing: Health day, Mental health workshop, Yoga
  - Learning: Book club, Lunch & Learn, Hackathon
  - Social: Birthday, Anniversary, Sports day
- Virtual engagement: 5 ideas cho remote team (virtual coffee, online game, remote happy hour)
- Budget summary: Total | Per head | % payroll | ROI expectation
- Measurement dashboard: KPI | Baseline | Target | Actual | Status
  - eNPS | Participation rate | Voluntary turnover | Absenteeism

TONE: Fun, engaging, positive — NV phải MUỐN tham gia.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 27: Khảo sát hài lòng NV / eNPS (Employee Satisfaction Survey / eNPS)

#### Mô tả
Bộ khảo sát hài lòng nhân viên kết hợp eNPS (Employee Net Promoter Score) — đo lường mức độ hài lòng và loyalty của NV qua 15-20 câu hỏi. Kết quả dùng để xác định drivers of engagement, action plan cải thiện.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tần suất khảo sát? (Quý / 6 tháng / Năm — recommend 6 tháng)
2. Ẩn danh hoàn toàn? (quan trọng để NV trả lời thật)
3. Drivers muốn đo: Manager, Growth, Compensation, Culture, Workload, Work-life balance?
4. Công cụ: Google Forms / Typeform / SurveyMonkey / Paper?
5. Ai xem kết quả? (HR only → BGĐ / Công bố toàn công ty?)
6. Có cam kết action plan sau khảo sát không? (nếu không → NV sẽ không tin lần sau)

#### Template gợi ý
Cấu trúc FRM:
- **Câu hỏi NPS**: 1 câu — "Trên thang 0-10, bạn có giới thiệu công ty cho bạn bè?"
- **Driver questions**: 14-19 câu × 5 drivers × scale 1-5
- **Open questions**: 2-3 câu mở — điểm tốt nhất, cần cải thiện, đề xuất
- **Cách tính eNPS**: (% Promoters 9-10 − % Detractors 0-6) × 100
- **Report template**: Dashboard 1 trang + driver breakdown
- **Action plan template**: Driver | Score | Gap | Action | Owner | Timeline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Khảo sát hài lòng NV / eNPS Survey.

CONTEXT:
- DN: [Tên] — Nhân sự: [số]
- Tần suất: [Quý / 6 tháng / Năm]
- Ẩn danh: [Có/Không]
- Drivers: [Manager / Growth / Comp / Culture / Workload / WLB]
- Tool: [Google Forms / Typeform / Paper]
- Kết quả cho: [HR only / BGĐ / Toàn công ty]

FORMAT:
- Câu 1 (eNPS): "Trên thang 0-10, bạn có giới thiệu [DN] cho bạn bè?" — Scale 0-10
- Câu 2-16 (Drivers): 3 câu per driver × 5 drivers × Scale 1 (Rất không đồng ý) → 5 (Rất đồng ý)
  - Manager: "Quản lý trực tiếp hỗ trợ tôi phát triển", "Tôi nhận phản hồi thường xuyên"...
  - Growth: "Tôi thấy cơ hội phát triển tại DN", "Tôi được đào tạo đủ"...
  - Compensation: "Lương công bằng so với thị trường", "Phúc lợi đáp ứng nhu cầu"...
  - Culture: "Tôi tự hào về văn hóa DN", "Giá trị cốt lõi được sống hàng ngày"...
  - Workload/WLB: "Khối lượng công việc hợp lý", "Tôi cân bằng được công việc-cuộc sống"...
- Câu 17-19 (Open): "Điều tốt nhất?" | "Cần cải thiện?" | "Đề xuất?"
- eNPS formula: Promoters (9-10) − Detractors (0-6) = eNPS → Benchmark: >50 Excellent | 10-50 Good | 0-10 OK | <0 Cần cải thiện ngay
- Report dashboard template: eNPS score | Per-driver score | Trend vs last survey | Top 3 strong | Top 3 weak
- Action plan template: Driver | Score | vs Benchmark | Gap | Action | Owner | Due | Status

TONE: Ẩn danh, safe, khuyến khích NV nói thật. Cam kết action plan = xây dựng trust.
LENGTH: 4-5 trang A4 (survey + report template + action plan).
```

---

## Ghi chú triển khai

### Dependencies
- `so-do-to-chuc.md` là file gốc — JD, Headcount, và tất cả file khác tham chiếu cơ cấu từ đây
- `noi-quy-lao-dong.md` là văn bản BẮT BUỘC — cần hoàn thành sớm và đăng ký Sở LĐTBXH
- `quy-che-luong-thuong.md` liên kết chặt với `chinh-sach-danh-gia-hieu-suat.md` và `kpi-ca-nhan-template.md`
- `so-tay-nhan-vien.md` tổng hợp nội dung từ hầu hết file khác → tạo cuối cùng
- `culture-code.md` cần input từ 02-Strategy (VMV, Core Values)

### Lưu ý pháp lý
> **QUAN TRỌNG**: Nội quy lao động và Quy chế lương thưởng là tài liệu có giá trị pháp lý. Nội quy phải đăng ký tại Sở LĐTBXH (Điều 119 BLLĐ 2019). Hợp đồng lao động phải tuân thủ BLLĐ 2019 và NĐ 145/2020. DN CẦN nhờ luật sư lao động rà soát trước khi ban hành chính thức.

### Thứ tự tạo khuyến nghị
1. Sơ đồ tổ chức → 2. JD Template → 3. JD vị trí chủ chốt → 4. Headcount Plan
5. Nội quy lao động → 6. Quy chế lương thưởng → 7. Phúc lợi → 8. Nghỉ phép → 9. Remote → 10. Bảo mật
11. SOP Tuyển dụng → 12. Bộ câu hỏi PV → 13. Scorecard → 14. Offer Letter
15. SOP Onboarding → 16. Checklist 30-60-90 → 17. Sổ tay NV (tổng hợp cuối cùng trong nhóm này)
18. SOP Nghỉ việc → 19. Biên bản bàn giao
20. Chính sách đánh giá → 21. KPI template → 22. Form 360 → 23. Career Path → 24. Training Plan
25. Culture Code → 26. Chương trình gắn kết → 27. Khảo sát eNPS

---

### VIII.6 — BP Operations (Hành Chính & Vận Hành)

> **Tầng 2: Bộ Máy** — 20 tài liệu: Hành chính văn phòng (5), Quản lý NCC (4), Quy trình vận hành cốt lõi (4), An toàn & Chất lượng (3), Họp & Giao tiếp nội bộ (4).

---

### PROMPT 01: SOP Quản lý văn phòng (Office Management SOP)

#### Mô tả
Quy trình chuẩn hóa quản lý văn phòng hàng ngày — bao gồm vệ sinh, bảo trì thiết bị, quản lý phòng họp, lễ tân, chìa khóa/access card, tiện ích (nước, điện, internet). Đảm bảo văn phòng luôn sẵn sàng, chuyên nghiệp.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Văn phòng thuê hay sở hữu? Diện tích? Số tầng?
2. Có admin/lễ tân chuyên trách không?
3. Dịch vụ outsource: vệ sinh, bảo vệ, IT?
4. Phòng họp: bao nhiêu phòng? Hệ thống đặt phòng?
5. Thiết bị chung: máy in, máy chiếu, bếp, đồ dùng VP?
6. Giờ mở/đóng cửa VP?

#### Template gợi ý
Cấu trúc SOP:
- **Quản lý hàng ngày**: Mở cửa, đóng cửa, checklist vệ sinh, kiểm tra thiết bị
- **Phòng họp**: Đặt phòng, chuẩn bị, dọn dẹp, quy tắc sử dụng
- **Thiết bị & Tiện ích**: Bảo trì định kỳ, xử lý hỏng, liên hệ kỹ thuật
- **Lễ tân & Khách**: Tiếp đón, đăng ký, hướng dẫn
- **Chìa khóa & Access**: Cấp phát, thu hồi, mất/hỏng
- **Nhà cung cấp VP**: Vệ sinh, bảo vệ, nước uống, văn phòng phẩm

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quản lý văn phòng (Office Management).

CONTEXT:
- DN: [Tên] — VP: [thuê/sở hữu] — Diện tích: [m²] — [số] tầng
- Admin: [Có/Không] — Outsource: [vệ sinh/bảo vệ/IT]
- Phòng họp: [số] phòng — Đặt phòng: [Google Calendar/Slack/bảng tay]
- Giờ VP: [giờ]

FORMAT:
- Checklist mở cửa: 5-8 mục ☐ + thời gian + người thực hiện
- Checklist đóng cửa: 5-8 mục ☐
- Phòng họp booking rules: Bảng Phòng | Sức chứa | Thiết bị | Booking method | Rules
- Bảo trì schedule: Bảng Thiết bị | Tần suất | Người phụ trách | NCC bảo trì | Liên hệ
- Xử lý sự cố VP: Flowchart — Loại sự cố → Mức độ → Người xử lý → Thời gian
- NCC directory: Dịch vụ | NCC | Liên hệ | HĐ số | Hạn HĐ

TONE: Operational, thực tế, dễ follow.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 02: SOP Mua sắm tài sản (Asset Procurement SOP)

#### Mô tả
Quy trình mua sắm tài sản/thiết bị — từ phát sinh nhu cầu, lập đề xuất, duyệt, lấy báo giá so sánh, đặt mua, nghiệm thu, đến bàn giao sử dụng và đưa vào quản lý tài sản.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phân cấp duyệt mua sắm? (< 5 triệu: TP | < 20 triệu: GĐ | > 20 triệu: HĐQT?)
2. Cần bao nhiêu báo giá so sánh? (2 / 3 / 5?)
3. Quy trình thanh toán: tạm ứng hay thanh toán sau giao hàng?
4. Có ủy ban mua sắm (procurement committee) không?
5. Ngưỡng phân loại TSCĐ: bao nhiêu VNĐ? (thường 30 triệu theo TT45)

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Đề xuất mua sắm: Form đề xuất + justification
- **Bước 2** — Phê duyệt: Theo hạn mức + kiểm tra budget
- **Bước 3** — Lấy báo giá: Số lượng báo giá, bảng so sánh
- **Bước 4** — Chọn NCC & Đặt hàng: Tiêu chí chọn, PO
- **Bước 5** — Nhận hàng & Nghiệm thu: Kiểm tra, biên bản
- **Bước 6** — Thanh toán: Chứng từ, quy trình
- **Bước 7** — Bàn giao & Quản lý: Gắn mã, nhập sổ, bàn giao user

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Mua sắm tài sản (Asset Procurement).

CONTEXT:
- DN: [Tên] — Phân cấp: < [X] triệu (TP) | < [Y] triệu (GĐ) | > [Y] (HĐQT)
- Số báo giá: [2/3/5]
- Thanh toán: [tạm ứng / sau giao hàng]
- Ngưỡng TSCĐ: [30 triệu / custom]
- Procurement committee: [Có/Không]

FORMAT:
- Flowchart 7 bước: Mermaid — highlight approval gates
- Form đề xuất template: Người đề xuất | Mô tả | Lý do | Số lượng | Budget line | Ước giá
- Bảng so sánh báo giá: NCC | Giá | Thời gian giao | Bảo hành | Thanh toán | Điểm
- Biên bản nghiệm thu template: Hàng nhận | Số lượng | Chất lượng | Chênh lệch | Ký nhận
- Decision matrix: Giá trị < X → Quy trình nhanh | > X → Quy trình đầy đủ
- Timeline: Từ đề xuất → nhận hàng target [ngày]

TONE: SOP chuẩn, kiểm soát chi phí.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 03: Sổ theo dõi tài sản (Asset Register / Tracking Sheet)

#### Mô tả
Template sổ theo dõi tài sản — quản lý toàn bộ tài sản của DN: từ bàn ghế, máy tính, đến xe cộ, máy móc. Theo dõi vị trí, người sử dụng, tình trạng, khấu hao.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có bao nhiêu loại tài sản chính? (IT, nội thất, phương tiện, máy móc...)
2. Quy tắc đánh mã tài sản? (VD: IT-NB-001 = IT-Notebook-001)
3. Phương pháp khấu hao? (Đường thẳng / Số dư giảm dần)
4. Tần suất kiểm kê? (6 tháng / 1 năm)
5. Quản lý trên phần mềm hay Excel?

#### Template gợi ý
Cấu trúc FRM:
- **Asset Register**: Mã TS | Tên | Loại | Ngày mua | Giá gốc | Khấu hao lũy kế | GTCL | Vị trí | Người dùng | Tình trạng (Đang dùng/Sửa chữa/Thanh lý/Mất)
- **Phân loại**: IT | Nội thất | Phương tiện | Máy móc | Khác
- **Bàn giao**: Mã TS | Từ | Đến | Ngày | Ký nhận
- **Thanh lý**: Mã TS | Lý do | Giá trị còn | Phương thức | Duyệt
- **Kiểm kê**: Mã TS | Sổ sách | Thực tế | Chênh lệch | Ghi chú

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sổ theo dõi tài sản (Asset Register).

CONTEXT:
- DN: [Tên] — Số loại TS: [số] — Tổng TS ước: [số]
- Mã hóa: [convention]
- Khấu hao: [Đường thẳng / Số dư giảm dần]
- Kiểm kê: [6 tháng / 1 năm]
- Tool: [PM / Excel]

FORMAT:
- Master register: 15+ cột, đủ info per tài sản
- Naming convention: Bảng Loại | Prefix | Ví dụ
- Khấu hao reference: Loại TS | Thời gian KH (năm) | PP KH (theo TT45/2013)
- Bàn giao form: 1/2 trang A4, ký nhận 2 bên
- Kiểm kê template: Bảng đối chiếu sổ sách vs thực tế
- Summary dashboard: Tổng TS | Giá trị | Đang dùng | Cần thanh lý | Chênh lệch

TONE: Quản lý, chính xác, dễ cập nhật.
LENGTH: 4-6 trang A4.
```

---

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

### PROMPT 05: Nội quy văn phòng (Office Rules & Regulations)

#### Mô tả
Nội quy sử dụng văn phòng — quy tắc ứng xử tại nơi làm việc, sử dụng tiện ích chung, phòng họp, bếp, parking, tiếp khách, PCCC. Khác với Nội quy lao động (bắt buộc pháp lý), đây là quy tắc nội bộ về sinh hoạt VP.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Văn phòng có đặc điểm gì? (co-working / riêng / nhà máy kèm VP)
2. Có parking riêng không?
3. Khách đến VP thường xuyên không? Quy trình đón tiếp?
4. Có khu vực restricted access không?
5. Chính sách hút thuốc, thú cưng, đồ ăn?

#### Template gợi ý
Cấu trúc POL:
- **Quy tắc chung**: Giờ ra vào, thẻ nhân viên, trang phục
- **Khu vực làm việc**: Ngăn nắp, tiếng ồn, điện thoại cá nhân
- **Phòng họp**: Đặt phòng, dọn dẹp, giới hạn thời gian
- **Khu vực chung**: Bếp, toilet, hành lang, thang máy
- **Khách & Đối tác**: Đăng ký, đón tiếp, khu vực cho phép
- **Parking & Di chuyển**: Quy tắc, vị trí
- **An toàn**: PCCC, lối thoát hiểm, sơ cấp cứu
- **Xử lý vi phạm**: Nhắc nhở → Cảnh cáo → Phạt

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Nội quy văn phòng (Office Rules).

CONTEXT:
- DN: [Tên] — Loại VP: [riêng / co-working / nhà máy + VP]
- Parking: [Có/Không]
- Khách thường xuyên: [Có/Không]
- Restricted area: [Có/Không]
- Đặc biệt: [hút thuốc / pet / dress code]

FORMAT:
- Poster-friendly: Có thể in 1 trang A3 treo VP
- Chia section rõ ràng, có icon placeholder
- Do / Don't format: Mỗi quy tắc có "Nên" và "Không nên"
- Bản đồ VP: Layout placeholder — exit, PCCC, sơ cấp cứu, restricted
- Emergency contacts: Bảng Loại | Liên hệ | SĐT

TONE: Thân thiện nhưng rõ ràng, dễ nhớ.
LENGTH: 3-5 trang A4 (+ bản poster 1 trang).
```

---

### PROMPT 06: SOP Đánh giá nhà cung cấp (Vendor Evaluation SOP)

#### Mô tả
Quy trình đánh giá và lựa chọn nhà cung cấp — tiêu chí đánh giá, quy trình approval, re-evaluation định kỳ, blacklist. Đảm bảo DN làm việc với NCC đáng tin cậy, chất lượng, giá hợp lý.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Bao nhiêu NCC đang làm việc? Ngành hàng chính?
2. Tiêu chí quan trọng nhất? (Giá / Chất lượng / Giao hàng / Dịch vụ?)
3. Tần suất re-evaluate? (6 tháng / 1 năm)
4. Ai quyết định chọn NCC? (Procurement / Committee / GĐ)
5. Có NCC single-source (chỉ có 1 NCC cho 1 mặt hàng) không?
6. Có yêu cầu NCC phải có ISO hoặc chứng nhận đặc biệt?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Xác định nhu cầu: Ngành hàng, specs, volume
- **Bước 2** — Tìm kiếm NCC: Nguồn, longlist
- **Bước 3** — Sơ tuyển: Criteria cơ bản, shortlist
- **Bước 4** — Đánh giá chi tiết: Scorecard, site visit, sample test
- **Bước 5** — Đàm phán & Chọn: HĐ khung, điều khoản
- **Bước 6** — Onboarding NCC: Setup hệ thống, test order
- **Bước 7** — Re-evaluation: Đánh giá định kỳ, adjust hoặc thay thế
- **Blacklist**: Tiêu chí đưa vào blacklist, quy trình

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Đánh giá nhà cung cấp (Vendor Evaluation).

CONTEXT:
- DN: [Tên] — Số NCC hiện tại: [số] — Ngành hàng: [liệt kê]
- Tiêu chí ưu tiên: [Giá / CL / Giao hàng / DV]
- Re-evaluate: [6 tháng / 1 năm]
- Approver: [Procurement / Committee / GĐ]
- Single-source: [Có/Không]
- ISO requirement: [Có/Không]

FORMAT:
- Flowchart 7 bước: Mermaid — từ nhu cầu đến re-evaluation
- Pre-qualification checklist: 10 tiêu chí Go/No-Go
- Scorecard tham chiếu: Link đến frm-scorecard-ncc.md
- Decision matrix: Score range → Approved / Conditional / Rejected
- Re-evaluation schedule: Calendar 12 tháng × NCC chính
- Blacklist criteria: 5-7 điều kiện → blacklist + quy trình appeal

TONE: Procurement chuyên nghiệp, objective, data-driven.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 07: Scorecard NCC (Vendor Scorecard)

#### Mô tả
Bảng đánh giá NCC theo tiêu chí có trọng số — Chất lượng, Giá cả, Giao hàng, Dịch vụ, Tài chính. Dùng cho đánh giá lần đầu và re-evaluation.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Trọng số các tiêu chí? (VD: CL 30% + Giá 25% + Giao hàng 20% + DV 15% + TC 10%)
2. Thang điểm: 1-5 hay 1-10?
3. Ngưỡng đạt: minimum score bao nhiêu?
4. Có rubric mô tả chi tiết mỗi mức điểm không?

#### Prompt tạo file
```
Tạo Vendor Scorecard (Bảng đánh giá NCC).

CONTEXT:
- DN: [Tên] — Trọng số: CL [%] | Giá [%] | Giao hàng [%] | DV [%] | TC [%]
- Thang điểm: [1-5 / 1-10]
- Ngưỡng đạt: [score]

FORMAT:
- Scorecard matrix: 5 nhóm tiêu chí × 3-5 sub-criteria mỗi nhóm × Trọng số × Điểm
- Rubric: Mỗi sub-criteria × mỗi mức điểm = mô tả cụ thể (VD: CL=5 "Zero defects in 6 months")
- Weighted score calculator: Formula rõ ràng
- Rating scale: ≥[X] Approved 🟢 | ≥[Y] Conditional 🟡 | <[Y] Rejected 🔴
- Comparison view: NCC A vs B vs C trên cùng 1 bảng
- Trend: Score kỳ này vs kỳ trước

TONE: Objective, quantitative, structured.
LENGTH: 3-4 trang A4.
```

---

### PROMPT 08: Danh sách NCC đã duyệt (Approved Vendor List — AVL)

#### Mô tả
Registry tổng hợp tất cả NCC đã qua đánh giá và được phê duyệt. Chỉ được đặt hàng từ NCC trong danh sách này (trừ trường hợp đặc biệt có duyệt GĐ).

#### Prompt tạo file
```
Tạo Approved Vendor List (Danh sách NCC đã duyệt).

CONTEXT:
- DN: [Tên] — Số NCC: [số]
- Phân loại: [ngành hàng / dịch vụ]

FORMAT:
- Registry: # | NCC | MST | Ngành hàng | Liên hệ | SĐT | Email | HĐ khung # | Hạn HĐ | Score | Status
- Phân nhóm: Theo ngành hàng/dịch vụ
- Status: Active 🟢 | Under Review 🟡 | Suspended 🟠 | Blacklisted 🔴
- Quick lookup: Ngành hàng → Top 3 NCC recommended
- Update log: Ngày | Thay đổi | Người cập nhật

TONE: Registry, reference material.
LENGTH: 2-4 trang A4.
```

---

### PROMPT 09: SOP Đặt hàng (Purchase Order SOP)

#### Mô tả
Quy trình đặt hàng (PO) — từ khi phát sinh nhu cầu đến khi nhận hàng và thanh toán. Liên kết với SOP Mua sắm tài sản (cho TS lớn) và SOP Quản lý kho (nhập kho).

#### Prompt tạo file
```
Tạo SOP Đặt hàng (Purchase Order Process).

CONTEXT:
- DN: [Tên] — Phân cấp duyệt PO: [chi tiết]
- Phần mềm: [ERP / Excel / email]
- NCC: Chỉ từ AVL / Ngoại lệ có quy trình

FORMAT:
- Flowchart: Mermaid — Yêu cầu → Kiểm tra AVL → Báo giá → So sánh → Duyệt PO → Gửi NCC → Nhận hàng → Nghiệm thu → Thanh toán
- PO template: # PO | Ngày | NCC | Items | Qty | Đơn giá | Tổng | Giao hàng | TT | Duyệt bởi
- 3-way matching: PO vs Phiếu nhận hàng vs Invoice → Approve payment
- Exception handling: PO khẩn cấp, PO vượt hạn mức, PO ngoài AVL
- Approval matrix: Giá trị PO → Cấp duyệt

TONE: SOP chuẩn, procurement.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 10: Operations Manual (Sổ tay Vận hành Tổng thể)

#### Mô tả
Tài liệu tổng quan mô tả toàn bộ hệ thống vận hành DN — nguyên tắc, cấu trúc quy trình, KPIs vận hành, escalation. Đây là "bible" để ai vào cũng hiểu DN vận hành thế nào. Theo triết lý E-Myth: "Document everything so anyone can run it."

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN hoạt động trong lĩnh vực gì? (sản xuất / dịch vụ / thương mại / SaaS)
2. Có bao nhiêu quy trình cốt lõi tạo ra giá trị cho KH? (EOS: thường 3-7)
3. KPIs vận hành chính? (On-time delivery, Quality rate, Utilization...)
4. Có ca kíp không? Có nhiều site/chi nhánh?
5. Điểm đau vận hành lớn nhất hiện tại?

#### Template gợi ý
Cấu trúc MAN:
- **Chương 1** — Tổng quan: Sứ mệnh vận hành, nguyên tắc, đội ngũ key
- **Chương 2** — Chuỗi giá trị: Value chain diagram, core processes map
- **Chương 3** — Danh mục quy trình: SOP registry — tên, mã, version, owner
- **Chương 4** — KPIs vận hành: Dashboard metrics, targets, measurement
- **Chương 5** — Escalation: Ma trận escalation theo mức độ sự cố
- **Chương 6** — Cải tiến liên tục: PDCA cycle, suggestion box, Kaizen events
- **Chương 7** — Tools & Systems: Phần mềm, thiết bị, hạ tầng
- **Phụ lục**: Process map tổng, SOP index, Contact directory

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Operations Manual (Sổ tay Vận hành Tổng thể).

CONTEXT:
- DN: [Tên] — Lĩnh vực: [SX / DV / TM / SaaS]
- Core processes: [số] — Tên: [liệt kê]
- KPIs chính: [liệt kê]
- Ca kíp: [Có/Không] — Multi-site: [Có/Không]
- Pain points: [liệt kê]

FORMAT:
- Value chain diagram: Mermaid — từ input → core processes → output → customer
- SOP registry: Bảng Mã SOP | Tên | Phòng ban | Owner | Version | Last updated | Status
- KPI dashboard: Bảng KPI | Target | Actual | Status 🟢🟡🔴 | Trend
- Escalation matrix: Mức độ (1-4) | Mô tả | Thời gian xử lý | Người xử lý | Thông báo
- PDCA template: Plan-Do-Check-Act cho cải tiến
- Organization for Ops: Mini org chart cho team vận hành

TONE: E-Myth style — hệ thống hóa, bất kỳ ai cũng follow được.
LENGTH: 10-15 trang A4.
```

---

### PROMPT 11: SOP Template chuẩn (Standard SOP Template)

#### Mô tả
Template chuẩn hóa format cho MỌI SOP trong DN. Đảm bảo mọi quy trình đều được viết cùng cấu trúc, dễ đọc, dễ cập nhật, dễ training.

#### Prompt tạo file
```
Tạo SOP Template chuẩn (Standard SOP Template).

CONTEXT:
- DN: [Tên]
- Naming convention: SOP-[Dept]-[###] — VD: SOP-OPS-001
- Versioning: v1.0 → v1.1 (minor) → v2.0 (major)

FORMAT:
- 1 trang template + 1 trang hướng dẫn điền
- Header: Logo | Tên SOP | Mã | Version | Ngày ban hành | Ngày review | Owner | Duyệt bởi
- Body sections:
  1. Mục đích (1-2 câu)
  2. Phạm vi (áp dụng cho ai, khi nào)
  3. Thuật ngữ & Viết tắt (bảng)
  4. Trách nhiệm (RACI table)
  5. Quy trình (Flowchart + Bước chi tiết)
  6. Biểu mẫu liên quan (link)
  7. Lịch sử thay đổi (version log)
- Footer: "Tài liệu nội bộ — Cấm sao chép" + Page number
- Hướng dẫn: Mẹo viết SOP hiệu quả, dos/don'ts

TONE: Meta-template, hướng dẫn chuẩn hóa.
LENGTH: 2-3 trang A4.
```

---

### PROMPT 12: SOP Cốt lõi 1-2-3 (Core Process SOPs)

#### Mô tả
3 SOP cốt lõi tạo ra giá trị trực tiếp cho khách hàng — tùy theo ngành nghề DN. Đây là "core processes" trong EOS: những quy trình mà nếu làm đúng, DN thành công; nếu làm sai, DN thất bại.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. 3 quy trình cốt lõi nhất của DN là gì? (VD: Bán hàng → Giao hàng → Hỗ trợ sau bán)
2. Mỗi quy trình hiện tại có bao nhiêu bước?
3. Điểm bottleneck / hay lỗi ở đâu?
4. Ai là owner mỗi quy trình?
5. KPI đo lường mỗi quy trình?

#### Prompt tạo file
```
Tạo 3 SOP Cốt lõi theo EOS Core Process.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- 3 Core Processes: [Tên 1] | [Tên 2] | [Tên 3]
- Bottlenecks: [mô tả]
- KPIs: [mỗi process]

FORMAT — Mỗi SOP theo SOP Template chuẩn:
- Process map: Mermaid end-to-end — 5-10 bước chính
- Swimlane: Vai trò × Bước — ai làm gì
- Chi tiết mỗi bước: Input | Action | Output | Tool | Time | Quality check
- Exception handling: 3-5 tình huống bất thường + cách xử lý
- KPI per process: 3-5 metrics + target + measurement method
- EOS style: "Documented, Simplified, Followed By All"

TONE: Operational, cụ thể, actionable.
LENGTH: 4-6 trang A4 per SOP (12-18 trang tổng).
```

---

### PROMPT 13: Checklist vận hành hàng ngày (Daily Operations Checklist)

#### Mô tả
Checklist công việc hàng ngày — mở cửa, kiểm tra, vận hành, đóng cửa. Đảm bảo không bỏ sót việc nào, nhất là khi thay người hoặc training NV mới.

#### Prompt tạo file
```
Tạo Checklist vận hành hàng ngày.

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Giờ hoạt động: [giờ]
- Loại: [VP / Cửa hàng / Nhà máy / Kho]

FORMAT:
- 3 bảng: Mở cửa (AM) | Trong ngày | Đóng cửa (PM)
- Mỗi mục: ☐ Task | Thời gian | Người thực hiện | Ghi chú
- Weekly tasks: Bảng riêng cho công việc theo tuần (VD: kiểm kê thứ 6)
- Monthly tasks: Bảng riêng cho công việc theo tháng
- Sign-off: Người thực hiện ký cuối ngày + Manager review

TONE: Operational, checklist-style, 1-2 trang max.
LENGTH: 2-3 trang A4.
```

---

### PROMPT 14: Chính sách An toàn Lao động (Occupational Safety Policy)

#### Mô tả
Chính sách ATVSLĐ — quy tắc an toàn, trang bị bảo hộ (PPE), sơ cấp cứu, PCCC, diễn tập. Theo Luật ATVSLĐ 2015 và các NĐ hướng dẫn.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hình: Văn phòng / Sản xuất / Kho / Xây dựng?
2. Có nhân viên làm việc trong môi trường nguy hiểm không?
3. PPE cần trang bị? (mũ, giày, kính, găng tay, khẩu trang...)
4. Có bộ phận ATVSLĐ riêng không?
5. Tần suất diễn tập PCCC?
6. Đã từng xảy ra tai nạn lao động chưa?

#### Prompt tạo file
```
Tạo Chính sách An toàn Lao động (OHS Policy).

CONTEXT:
- DN: [Tên] — Loại hình: [VP / SX / Kho / XD]
- Nguy hiểm: [Có/Không] — Loại: [mô tả]
- PPE: [liệt kê]
- ATVSLĐ team: [Có/Không]
- Diễn tập PCCC: [tần suất]
- Cơ sở pháp lý: Luật ATVSLĐ 2015, NĐ 39/2016

FORMAT:
- Cam kết lãnh đạo: 1 đoạn từ CEO
- Quy tắc an toàn: 10-15 quy tắc chính + poster-friendly
- PPE matrix: Vị trí/Công việc | PPE bắt buộc | PPE khuyến nghị
- Sơ cấp cứu: Kit location, trained person, quy trình
- PCCC: Bình chữa cháy location, lối thoát, diễn tập schedule
- Báo cáo tai nạn: Form template + quy trình 24h
- Training: Schedule đào tạo ATVSLĐ hàng năm

TONE: An toàn — nghiêm túc, rõ ràng, cảnh báo đủ.
LENGTH: 6-10 trang A4.
```

---

### PROMPT 15: SOP Xử lý Sự cố (Incident Management SOP)

#### Mô tả
Quy trình xử lý mọi loại sự cố — từ IT down, mất điện, tai nạn, đến khiếu nại KH nghiêm trọng. Phân loại mức độ, escalation path, xử lý, báo cáo, và root cause analysis.

#### Prompt tạo file
```
Tạo SOP Xử lý Sự cố (Incident Management).

CONTEXT:
- DN: [Tên] — Loại sự cố phổ biến: [IT / ATVSLĐ / KH / Vận hành]
- Số cấp escalation: [3-4]
- Oncall: [Có/Không]

FORMAT:
- Phân loại sự cố: Severity 1 (Critical) → 2 (High) → 3 (Medium) → 4 (Low) + Ví dụ mỗi mức
- Escalation matrix: Severity | Response time | Resolver | Escalate to | Notify
- Flowchart: Mermaid — Phát hiện → Phân loại → Xử lý → Khắc phục → RCA → Preventive
- Incident report template: Thời gian | Mô tả | Severity | Impact | Root Cause | Action | Owner | Status
- RCA template: 5 Whys + Fishbone diagram guide
- Post-incident review: Checklist 8 câu hỏi

TONE: Khẩn cấp, rõ ràng, action-oriented.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 16: Chính sách Chất lượng (Quality Policy — ISO-aligned)

#### Mô tả
Chính sách chất lượng tổng thể — cam kết, mục tiêu, KPIs chất lượng, PDCA, cải tiến liên tục. Aligned với ISO 9001:2015 (có thể dùng ngay nếu DN muốn đi ISO).

#### Prompt tạo file
```
Tạo Chính sách Chất lượng (Quality Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- ISO 9001: [Đang có / Muốn đạt / Không cần nhưng muốn align]
- KPIs chất lượng hiện có: [liệt kê]

FORMAT:
- Quality statement: 1 đoạn cam kết — in poster treo VP
- Mục tiêu chất lượng: SMART × 5-8 mục tiêu
- KPIs: Bảng KPI | Target | Measurement | Frequency | Owner
- PDCA cycle: Diagram + hướng dẫn áp dụng cho mỗi process
- Customer feedback loop: Flowchart — Thu thập → Phân tích → Cải tiến → Đo lường
- Nonconformity handling: Quy trình xử lý sản phẩm/dịch vụ không phù hợp
- Management review: Tần suất, agenda, output

TONE: ISO-aligned, chuyên nghiệp, cam kết.
LENGTH: 5-8 trang A4.
```

---

### PROMPT 17: Quy chế Họp hành — EOS Meeting Pulse (Meeting Policy)

#### Mô tả
Quy chế họp theo framework EOS Meeting Pulse — chuẩn hóa loại họp, tần suất, agenda, quy tắc. Giảm họp vô nghĩa, tăng họp hiệu quả. Áp dụng L10 Meeting format.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện tại có bao nhiêu cuộc họp/tuần? Cảm thấy quá nhiều/quá ít?
2. Loại họp cần có? (Daily standup / Weekly / Monthly / Quarterly / Annual)
3. Bao nhiêu người trung bình mỗi cuộc họp?
4. Có vấn đề gì với họp hiện tại? (quá dài, không có quyết định, không follow-up)
5. Muốn áp dụng L10 Meeting (EOS) không?

#### Template gợi ý
Cấu trúc POL:
- **Nguyên tắc họp**: Start/end on time, agenda trước, action items sau, no devices rule
- **Loại họp**: Daily Standup (15 min) | Weekly L10 (90 min) | Monthly Review (2h) | Quarterly Planning (1 ngày)
- **L10 Meeting format**: Segue (5 min) → Scorecard (5 min) → Rock review (5 min) → Customer/Employee headlines (5 min) → To-do review (5 min) → IDS (60 min) → Conclude (5 min)
- **Quy tắc**: Ai triệu tập, ai phải dự, thay thế khi vắng, hủy họp
- **Action items**: Format Ai | Làm gì | Khi nào | Status
- **Metrics**: % họp đúng giờ, % action items hoàn thành

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Quy chế Họp hành (Meeting Policy — EOS Meeting Pulse).

CONTEXT:
- DN: [Tên] — Họp hiện tại: [số buổi/tuần] — Vấn đề: [mô tả]
- Loại họp cần: [Daily / Weekly / Monthly / Quarterly / Annual]
- L10 format: [Có/Không]
- Nhân sự tham gia trung bình: [số]

FORMAT:
- Meeting matrix: Loại | Tần suất | Thời lượng | Participants | Facilitator | Agenda template
- L10 agenda card: 1 trang — 7 segments × time box
- Daily standup template: 3 câu hỏi (Yesterday | Today | Blockers)
- Quy tắc poster: 10 rules — in 1 trang A3
- Action items tracker: Bảng từ họp → task → owner → due → status
- Meeting effectiveness survey: 5 câu, chạy monthly

TONE: EOS-inspired, hiệu quả, action-oriented.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 18: Template Biên bản họp (Meeting Minutes Template)

#### Mô tả
Template biên bản họp chuẩn — ghi nhận quyết định, action items, owner, deadline. Khác với BB họp HĐQT (pháp lý) ở 01-Governance, đây là template cho họp nội bộ hàng ngày/tuần.

#### Prompt tạo file
```
Tạo Template Biên bản họp nội bộ.

FORMAT:
- Header: Loại họp | Ngày | Giờ | Địa điểm/Link | Chủ trì | Ghi chép
- Tham dự: Tên | Chức danh | Có mặt ☐
- Agenda: Numbered items
- Nội dung: Mỗi agenda item → Thảo luận | Quyết định | Action item
- Action items summary: Bảng # | Action | Owner | Due | Priority
- Next meeting: Ngày | Agenda dự kiến
- 1 trang A4 max — concise

TONE: Ngắn gọn, action-focused.
LENGTH: 1-2 trang A4.
```

---

### PROMPT 19: Template Báo cáo tuần (Weekly Report Template)

#### Mô tả
Template báo cáo tuần cho trưởng phòng/nhân viên — tóm tắt KPIs, done/doing/blocked, highlights, concerns, kế hoạch tuần tới.

#### Prompt tạo file
```
Tạo Template Báo cáo tuần (Weekly Report).

FORMAT:
- Header: Tuần [#] | [Ngày-Ngày] | Phòng ban | Người báo cáo
- KPI Snapshot: Bảng KPI | Target tuần | Actual | % | Status 🟢🟡🔴
- Done this week: 5-7 bullets — completed tasks
- In progress: 3-5 bullets — ongoing + % done
- Blocked: 1-3 bullets — obstacles + cần ai giúp
- Highlights: 1-2 wins
- Concerns: 1-2 risks/issues
- Next week plan: Top 5 priorities
- 1 trang A4 — scannable in 2 minutes

TONE: Executive, concise, status-focused.
LENGTH: 1 trang A4.
```

---

### PROMPT 20: SOP Truyền thông Nội bộ (Internal Communication SOP)

#### Mô tả
Quy trình truyền thông nội bộ — xác định kênh nào cho loại thông tin nào, cách announce tin quan trọng, escalation khi thông tin nhạy cảm.

#### Prompt tạo file
```
Tạo SOP Truyền thông Nội bộ (Internal Communication).

CONTEXT:
- DN: [Tên] — Kênh hiện có: [Email / Slack / Zalo / Intranet / Họp]
- Nhân sự: [số] — Multi-site: [Có/Không]
- Vấn đề hiện tại: [tin đồn / thiếu thông tin / quá nhiều kênh]

FORMAT:
- Channel matrix: Loại thông tin | Kênh chính | Kênh phụ | Tần suất | Người gửi
  - VD: Khẩn cấp → Zalo group + Gọi điện | Chính sách mới → Email all + Họp all-hands
- Announcement protocol: Flowchart — Tin quan trọng → Draft → Approve → Send → Q&A
- Escalation: Tin nhạy cảm (sa thải, restructure, khủng hoảng) → Quy trình đặc biệt
- Feedback channels: Suggestion box, anonymous survey, 1-on-1
- Content calendar: Bảng Tuần × Loại thông tin (Weekly update, Birthdays, Achievements...)
- Measurement: Employee awareness survey, message read rate

TONE: HR + Comms, inclusive, transparent.
LENGTH: 4-6 trang A4.
```

---

## Ghi chú triển khai

### Dependencies
- `operations-manual.md` là file tổng quan — tham chiếu đến tất cả SOP khác trong folder
- `sop-template-chuan.md` là format mà MỌI SOP trong toàn bộ hệ thống 200+ file phải tuân theo
- `sop-cot-loi.md` tùy thuộc ngành nghề DN — cần input từ Intake Questionnaire (00-Orchestrator)
- `quy-che-hop-hanh.md` ảnh hưởng đến cách vận hành hàng ngày của toàn DN — cần Giám đốc quyết định
- `frm-template-bao-cao-tuan.md` cung cấp data cho 11-Reporting (Dashboard tổng)

### Lưu ý
> **QUAN TRỌNG**: Operations là skill customize nhiều nhất theo ngành. SOP cốt lõi của công ty sản xuất (production line) hoàn toàn khác công ty dịch vụ (service delivery) hay công ty SaaS (product development). AI cần hỏi rõ ngành nghề trước khi tạo SOP cốt lõi.

> **EOS Meeting Pulse**: Nếu DN áp dụng EOS, quy chế họp nên theo đúng L10 format. Nếu không, vẫn nên có structure rõ ràng theo nguyên tắc: agenda trước, action items sau, không quá 90 phút.

### Thứ tự tạo khuyến nghị
1. SOP Template chuẩn (định format cho mọi SOP) → 2. Operations Manual (tổng quan)
3. SOP Quản lý VP → 4. Nội quy VP → 5. SOP Mua sắm → 6. Sổ theo dõi tài sản → 7. SOP Quản lý kho
8. SOP Đánh giá NCC → 9. Scorecard NCC → 10. Danh sách NCC → 11. SOP Đặt hàng
12. SOP Cốt lõi 1-2-3 (customize theo ngành) → 13. Checklist hàng ngày
14. Chính sách ATLĐ → 15. SOP Xử lý sự cố → 16. Chính sách chất lượng
17. Quy chế họp hành → 18. Template biên bản → 19. Template báo cáo tuần → 20. SOP Truyền thông NB

---

### VIII.7 — BP Sales (Kinh Doanh & Bán Hàng)

> **Tầng 3: Tăng Trưởng** — 17 tài liệu: Chiến lược kinh doanh (4), Quy trình bán hàng (6), Công cụ bán hàng (4), Đối tác & Kênh (3).

---

### PROMPT 01: Sales Strategy & Target (Chiến lược kinh doanh tổng thể)

#### Mô tả
Văn bản chiến lược cấp cao nhất về kinh doanh & bán hàng. Xác định mục tiêu doanh số, phân khúc thị trường ưu tiên, kênh bán trọng điểm, và KPIs đo lường. Là "kim chỉ nam" để toàn bộ đội sales align hành động với mục tiêu DN.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mục tiêu doanh số năm? (tổng + breakdown theo quý/tháng)
2. Phân khúc thị trường mục tiêu? (B2B / B2C / B2B2C? Ngành nào? Quy mô KH?)
3. Sản phẩm/dịch vụ bán chạy nhất hiện tại? Top 3 đóng góp doanh thu?
4. Kênh bán hiện tại? (direct sales, telesales, online, đại lý, affiliate?)
5. Đội ngũ sales hiện tại: bao nhiêu người? Chia theo kênh/vùng?
6. KPIs sales đang theo dõi? (revenue, deals, conversion rate, average deal size?)
7. Đối thủ cạnh tranh chính? Điểm khác biệt của mình?
8. Thách thức lớn nhất trong bán hàng hiện tại?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Tổng quan chiến lược: Tầm nhìn sales, mục tiêu 1-3 năm, North Star Metric
- **Phần 2** — Phân tích thị trường: TAM/SAM/SOM, phân khúc ưu tiên, buyer persona
- **Phần 3** — Mục tiêu doanh số: Tổng → Theo SP → Theo kênh → Theo vùng × 12 tháng
- **Phần 4** — Chiến lược kênh bán: Kênh nào ưu tiên, resource allocation, target per channel
- **Phần 5** — Go-to-Market: Cách tiếp cận từng phân khúc, messaging, positioning
- **Phần 6** — Tổ chức đội sales: Structure, role & responsibility, territory mapping
- **Phần 7** — KPIs & Scorecard: Leading indicators + Lagging indicators + Weekly scorecard
- **Phần 8** — Action Plan: 90 ngày đầu, quarterly milestones
- **Phụ lục**: Competitive landscape, Quota allocation template, Territory map

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sales Strategy & Target (Chiến lược kinh doanh tổng thể).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Doanh thu hiện tại: [số/năm]
- Mục tiêu doanh số: [số/năm] — Tăng trưởng: [%]
- Phân khúc: [B2B / B2C / B2B2C] — KH mục tiêu: [mô tả]
- SP/DV chính: [liệt kê top 3 + % doanh thu]
- Kênh bán: [direct / telesales / online / đại lý / affiliate]
- Đội sales: [số người] — Chia: [theo kênh / vùng]
- Đối thủ: [liệt kê top 3]

FORMAT:
- Mục tiêu: Bảng Tổng | Per SP | Per Kênh | Per Vùng × Q1-Q4
- TAM/SAM/SOM: Funnel chart data + số liệu ước tính
- Buyer persona: 2-3 persona cards (Demographics, Pain Points, Decision Process, Channels)
- Channel priority matrix: Kênh | Revenue target | CAC | LTV | Priority | Resource %
- Scorecard: Bảng KPI | Target | Weekly pace | Owner | Status
- 90-day action plan: Week 1-4 | Week 5-8 | Week 9-12 — milestones cụ thể
- Territory map: Vùng/Segment × Sales Rep × Quota

TONE: Chiến lược, executive-level, hướng hành động.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 02: Pricing Strategy (Chiến lược giá)

#### Mô tả
Chiến lược định giá toàn diện — xác định vị thế giá trên thị trường, phương pháp tính giá, cơ cấu chiết khấu, và quy trình điều chỉnh giá. Khác với Pricing Policy (chính sách nội bộ ở Finance), đây tập trung vào chiến lược cạnh tranh và go-to-market.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Vị thế giá mong muốn? (Premium / Mid-range / Value / Low-cost)
2. Cơ cấu giá hiện tại? (one-time / subscription / usage-based / hybrid)
3. Giá bán trung bình hiện tại? So với đối thủ ở đâu?
4. Chính sách chiết khấu hiện tại? (volume, loyalty, seasonal, early payment)
5. Ai có quyền discount? Hạn mức bao nhiêu %?
6. Tần suất thay đổi giá? Trigger thay đổi là gì?
7. Có sản phẩm loss-leader / freemium không?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Pricing Objective: Maximize revenue / Market share / Profit margin / Penetration
- **Phần 2** — Price Positioning: Perceptual map vs đối thủ, value-price matrix
- **Phần 3** — Pricing Method: Cost-plus / Value-based / Competitive / Dynamic — khi nào dùng gì
- **Phần 4** — Price Architecture: Tiers, bundles, add-ons, upsell/cross-sell pricing
- **Phần 5** — Discount Framework: Bảng chiết khấu theo loại, approval levels, guardrails
- **Phần 6** — Competitive Pricing: Price comparison matrix, response playbook
- **Phần 7** — Price Review & Adjustment: Triggers, process, communication plan
- **Phụ lục**: Price list template, Discount calculator, Competitive price tracker

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Pricing Strategy (Chiến lược giá).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Số SP/DV: [số]
- Vị thế giá: [Premium / Mid / Value / Low-cost]
- Cơ cấu giá: [one-time / subscription / usage-based / hybrid]
- Giá TB: [số] — So với đối thủ: [cao hơn / ngang / thấp hơn X%]
- Chiết khấu hiện tại: [volume / loyalty / seasonal / early payment]
- Quyền discount: [Chức danh] — Max: [%]
- Loss-leader/Freemium: [Có/Không] — [mô tả]

FORMAT:
- Price positioning map: 2x2 matrix (Value vs Price) — plot DN + đối thủ
- Price architecture: Bảng Tier | Features | Price | Target segment | Margin %
- Discount framework: Bảng Loại CK | Điều kiện | % CK | Approval | Guardrail
- Competitive comparison: Bảng SP | DN Price | Competitor A | B | C | Positioning
- Price waterfall: List Price → Discount → Net Price → COGS → Margin (Mermaid/bảng)
- Decision tree: Khi nào raise/lower/hold price — flowchart
- Review calendar: Quarterly trigger checklist

TONE: Chiến lược, data-driven, cạnh tranh.
LENGTH: 6-10 trang A4.
```

---

### PROMPT 03: Channel Strategy (Chiến lược kênh phân phối)

#### Mô tả
Chiến lược kênh phân phối toàn diện — xác định kênh direct/indirect, online/offline, đại lý, partnership, và cách phối hợp omnichannel. Mục tiêu là maximize coverage và conversion trong khi tối ưu chi phí phân phối.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Các kênh bán hiện tại? % doanh thu mỗi kênh?
2. Kênh nào đang hiệu quả nhất? Kênh nào chưa khai thác?
3. Có hệ thống đại lý/distributor không? Bao nhiêu? Ở đâu?
4. Bán online qua kênh nào? (website, marketplace, social commerce)
5. Có xung đột kênh (channel conflict) không? (VD: đại lý vs bán trực tiếp)
6. Kế hoạch mở rộng kênh trong 12 tháng tới?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Channel Portfolio: Bản đồ tất cả kênh hiện tại + tiềm năng
- **Phần 2** — Direct Channels: Sales team, website, showroom, telesales
- **Phần 3** — Indirect Channels: Đại lý, distributor, reseller, affiliate
- **Phần 4** — Digital Channels: E-commerce, marketplace, social commerce, app
- **Phần 5** — Omnichannel Integration: Customer journey xuyên kênh, data sync
- **Phần 6** — Channel Economics: Revenue, cost, margin per channel
- **Phần 7** — Channel Conflict Management: Rules, territory, pricing consistency
- **Phần 8** — Expansion Plan: Kênh mới, timeline, investment, expected ROI
- **Phụ lục**: Channel partner criteria, Territory map, Channel P&L template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Channel Strategy (Chiến lược kênh phân phối).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Số kênh hiện tại: [số]
- Kênh hiện tại: [liệt kê + % doanh thu mỗi kênh]
- Đại lý: [Có/Không] — Số lượng: [số] — Vùng: [liệt kê]
- Online: [website / marketplace / social / app]
- Channel conflict: [Có/Không] — [mô tả]
- Kế hoạch mở rộng: [kênh mới + timeline]

FORMAT:
- Channel map: Sơ đồ tổng quan DN → Kênh → Khách hàng (Mermaid)
- Channel scorecard: Bảng Kênh | Revenue | % Total | CAC | Margin | Growth | Priority
- Customer journey per channel: Awareness → Consider → Buy → Retain per kênh
- Channel economics: Bảng Kênh | Revenue | Direct Cost | Margin | ROI
- Conflict resolution matrix: Tình huống | Quy tắc | Ưu tiên
- Expansion roadmap: Timeline 12 tháng × Kênh mới × Milestones
- Resource allocation: Bảng Kênh | Headcount | Budget | % Total investment

TONE: Chiến lược, thực tế, hướng tối ưu kênh.
LENGTH: 6-10 trang A4.
```

---

### PROMPT 04: Unit Economics (Phân tích đơn vị kinh tế)

#### Mô tả
Phân tích unit economics chi tiết — đo lường hiệu quả kinh doanh ở cấp đơn vị: chi phí thu hút 1 khách hàng (CAC), giá trị trọn đời (LTV), thời gian hoàn vốn (Payback Period), và biên lợi nhuận per channel. Là cơ sở để ra quyết định đầu tư marketing/sales.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Doanh thu trung bình mỗi khách hàng/đơn hàng? (ARPU / Average Order Value)
2. Tần suất mua lại? Tỷ lệ khách quay lại?
3. Chi phí marketing + sales trung bình để có 1 khách hàng?
4. Thời gian trung bình từ lead → khách hàng?
5. Tỷ lệ churn / retention hiện tại?
6. Breakdown chi phí theo kênh? (online ads, content, events, sales team)

#### Template gợi ý
Cấu trúc RPT:
- **Executive Summary** — Key metrics: CAC, LTV, LTV/CAC ratio, Payback Period
- **Phần 1** — Customer Acquisition Cost (CAC): Tổng + per channel breakdown
- **Phần 2** — Lifetime Value (LTV): Calculation, assumptions, sensitivity
- **Phần 3** — LTV/CAC Ratio: Benchmark (>3x healthy), trend, per segment
- **Phần 4** — Payback Period: Months to recover CAC, per channel
- **Phần 5** — Contribution Margin per Channel: Revenue - Variable cost per channel
- **Phần 6** — Cohort Analysis: Retention curve, revenue per cohort
- **Phần 7** — Recommendations: Kênh nào scale, kênh nào optimize, kênh nào cắt
- **Phụ lục**: Calculation methodology, Data sources, Benchmark references

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Unit Economics Report (Phân tích đơn vị kinh tế).

CONTEXT:
- DN: [Tên] — Mô hình: [B2B / B2C / SaaS / E-commerce]
- ARPU/AOV: [số/tháng hoặc /đơn]
- Tần suất mua: [lần/năm] — Retention: [%]
- Chi phí M+S: [số/tháng] — Số KH mới/tháng: [số]
- Conversion rate: [%] — Sales cycle: [ngày]
- Kênh: [liệt kê + chi phí mỗi kênh]

FORMAT:
- Summary dashboard: 6 KPI cards — CAC | LTV | LTV/CAC | Payback | ARPU | Churn
- CAC breakdown: Bảng Kênh | Spend | Leads | Customers | CAC | % Total
- LTV calculation: ARPU × Avg Lifespan × Gross Margin — sensitivity ±10/20%
- LTV/CAC per segment: Bảng Segment | LTV | CAC | Ratio | Verdict (Healthy/Watch/Cut)
- Payback period: Bảng Kênh | CAC | Monthly Revenue | Payback Months
- Cohort table: Month 0-12 × Cohort → Retention % + Revenue
- Recommendation matrix: Kênh | LTV/CAC | Action (Scale/Optimize/Cut) | Priority

TONE: Analytical, data-driven, hướng quyết định đầu tư.
LENGTH: 5-8 trang A4.
```

---

### PROMPT 05: SOP Sales Process (Quy trình bán hàng)

#### Mô tả
Quy trình chuẩn hóa toàn bộ hoạt động bán hàng — từ tiếp nhận lead đến chốt đơn và bàn giao khách hàng. Đảm bảo mọi sales rep đều bán hàng theo cùng một quy trình đã được chứng minh hiệu quả, giảm phụ thuộc vào cá nhân.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Nguồn lead chính? (Marketing, referral, outbound, event, website)
2. Tiêu chí qualify lead? (BANT / MEDDIC / CHAMP / custom?)
3. Quy trình bán hiện tại có bao nhiêu bước? Mô tả?
4. Thời gian trung bình từng bước? Toàn bộ cycle?
5. Có handover giữa các team không? (SDR → AE → AM → CS?)
6. Công cụ hỗ trợ? (CRM, email, phone, chat?)
7. Tỷ lệ chuyển đổi từng bước hiện tại?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Thuật ngữ**: Lead, MQL, SQL, Opportunity, Deal, Won, Lost
- **Tổng quan quy trình**: 7 bước — Lead → Qualify → Demo/Consult → Proposal → Negotiate → Close → Handover
- **Chi tiết từng bước**: Mục tiêu, hành động cụ thể, output, tiêu chí chuyển bước, timeline, tools
- **Qualification Framework**: BANT hoặc MEDDIC — checklist áp dụng
- **Handover Protocol**: SDR → AE, AE → AM, Sales → CS
- **Escalation Rules**: Khi nào cần manager/director tham gia
- **Tracking & Reporting**: CRM stages, pipeline review cadence
- **Phụ lục**: Qualification checklist, Stage criteria, Handover template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Sales Process (Quy trình bán hàng).

CONTEXT:
- DN: [Tên] — Mô hình: [B2B / B2C / SaaS / Dịch vụ]
- Nguồn lead: [Marketing / Referral / Outbound / Event / Website]
- Qualification: [BANT / MEDDIC / CHAMP / Custom]
- Số bước hiện tại: [số] — Sales cycle: [ngày]
- Team structure: [SDR + AE + AM / All-in-one]
- CRM: [Tên phần mềm]

FORMAT:
- Flowchart tổng: Mermaid — 7 bước chính + decision points
- Per-step detail: Bảng Bước | Mục tiêu | Actions | Output | Exit Criteria | Timeline | Owner
- Qualification checklist: BANT/MEDDIC — Tiêu chí | Câu hỏi | Đạt/Không | Score
- Conversion funnel: Bảng Stage | Leads In | Converted | Rate | Avg Days | Bottleneck
- Handover template: Bảng thông tin cần chuyển giao giữa các role
- Escalation matrix: Tình huống | Escalate to | Timeline | Expected action
- Weekly pipeline review agenda: 5 mục check cố định

TONE: SOP chuẩn — step-by-step, rõ ràng, actionable.
LENGTH: 6-10 trang A4.
```

---

### PROMPT 06: Sales Script (Kịch bản bán hàng)

#### Mô tả
Bộ kịch bản bán hàng chuẩn hóa cho từng kênh (telesales, tư vấn trực tiếp, online chat) và từng sản phẩm/buyer persona. Không phải "đọc thuộc lòng" mà là framework để sales rep navigate cuộc hội thoại hiệu quả.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Kênh bán hàng chính cần script? (telesales / face-to-face / online chat / video call)
2. Sản phẩm/dịch vụ cần script? (liệt kê top 3)
3. Buyer persona chính? (chức danh, pain points, buying triggers)
4. Thời lượng trung bình 1 cuộc tư vấn?
5. Objections phổ biến nhất? (top 5)
6. Call-to-action mong muốn? (đặt hẹn / demo / mua ngay / trial)
7. Có script hiện tại không? Điểm yếu?

#### Template gợi ý
Cấu trúc FRM:
- **Nguyên tắc sử dụng script**: Guidelines — adapt, không đọc thuộc
- **Script Telesales**: Opening → Discovery → Presentation → Close → Follow-up
- **Script Tư vấn trực tiếp**: Chào hỏi → Khám phá nhu cầu → Demo/Trình bày → Xử lý từ chối → Chốt
- **Script Online Chat**: Auto-greeting → Quick qualify → Value proposition → CTA → Chuyển offline
- **Per Persona Variations**: Persona A → adjust messaging, Persona B → adjust messaging
- **Power Phrases**: Câu hỏi hay, câu chốt hay, câu xử lý từ chối hay
- **Anti-patterns**: Những câu KHÔNG được nói
- **Phụ lục**: Roleplay scenarios, Scoring rubric

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sales Script (Kịch bản bán hàng).

CONTEXT:
- DN: [Tên] — SP/DV: [liệt kê top 3]
- Kênh: [telesales / face-to-face / chat / video call]
- Persona: [Tên persona | Chức danh | Pain point | Trigger]
- Thời lượng TB: [phút]
- Objections top 5: [liệt kê]
- CTA: [đặt hẹn / demo / mua / trial]

FORMAT:
- Script structure per kênh: Flowchart giai đoạn + thời lượng mỗi giai đoạn
- Verbatim script: Câu chào → Câu mở → Discovery questions (5-7 câu) → Pitch → Close
- Branching: IF khách nói X THEN → response A; IF khách nói Y THEN → response B
- Persona variations: Bảng Giai đoạn | Persona A | Persona B | Persona C
- Power phrases: 10 câu hỏi hay + 10 câu chốt hay + 10 câu bridge
- Anti-patterns: 10 câu KHÔNG được nói + lý do + thay thế bằng gì
- Practice scenarios: 3 roleplay tình huống (easy / medium / hard)
- Scoring: Bảng tiêu chí đánh giá cuộc gọi/tư vấn

TONE: Tự nhiên, tư vấn (không "sale"), chuyên nghiệp.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 07: Objection Handling Guide (Bộ xử lý từ chối)

#### Mô tả
Bộ tài liệu tổng hợp top 20 lý do từ chối phổ biến nhất + cách xử lý hiệu quả cho từng lý do. Áp dụng LAER framework (Listen, Acknowledge, Explore, Respond) và reframe techniques để chuyển từ chối thành cơ hội.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Top 10 lý do từ chối phổ biến nhất hiện tại?
2. Objection nào khó xử lý nhất? Tỷ lệ recover?
3. Sản phẩm/dịch vụ nào hay bị từ chối nhất?
4. Đối thủ nào hay bị so sánh?
5. Chính sách linh hoạt? (giảm giá, trial, bảo hành, hoàn tiền?)
6. Sales team đang xử lý từ chối thế nào? Có training không?

#### Template gợi ý
Cấu trúc FRM:
- **LAER Framework**: Giải thích 4 bước — Listen, Acknowledge, Explore, Respond
- **Top 20 Objections**: Mỗi objection 1 card:
  - Objection statement
  - Loại: Price / Trust / Timing / Need / Competition / Authority
  - Tâm lý đằng sau
  - LAER response mẫu
  - Reframe technique
  - Follow-up question
- **Phân loại objection**: Bảng theo loại + tần suất
- **Reframe Techniques**: 7 kỹ thuật chuyển đổi góc nhìn
- **Do's & Don'ts**: Nguyên tắc khi xử lý từ chối
- **Practice**: Roleplay scenarios
- **Phụ lục**: Objection tracking sheet, Win/Loss analysis template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Objection Handling Guide (Bộ xử lý từ chối).

CONTEXT:
- DN: [Tên] — SP/DV: [liệt kê]
- Top 10 objections: [liệt kê]
- Objection khó nhất: [mô tả] — Recovery rate: [%]
- Đối thủ so sánh: [liệt kê]
- Chính sách linh hoạt: [giảm giá / trial / bảo hành / hoàn tiền]

FORMAT:
- LAER framework: Infographic 4 bước + ví dụ minh họa
- Objection cards: 20 cards — Objection | Loại | Tâm lý | Response mẫu | Reframe | Follow-up
- Classification matrix: Bảng Loại | Số lượng | Tần suất % | Độ khó | Recovery rate
- Reframe techniques: 7 kỹ thuật + ví dụ cụ thể cho từng kỹ thuật
- Comparison handler: Bảng Đối thủ | Điểm họ mạnh | Điểm ta mạnh hơn | Response
- Do's & Don'ts: 2 cột — 10 SHOULD + 10 SHOULD NOT
- Roleplay: 3 scenarios (Price / Competition / Timing) + script mẫu

TONE: Coaching — tự nhiên, empathetic, persuasive nhưng không manipulative.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 08: SOP Quy trình báo giá (Quotation Process SOP)

#### Mô tả
Quy trình chuẩn hóa từ lúc nhận yêu cầu báo giá đến khi gửi báo giá, follow up, và chốt đơn. Đảm bảo báo giá chính xác, kịp thời, đúng thẩm quyền, và theo dõi được trạng thái.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ai tiếp nhận yêu cầu báo giá? (Sales rep / Admin / Website form)
2. Thời gian phản hồi báo giá cam kết? (VD: 24h / 48h / 72h)
3. Ai tính giá? Ai duyệt giá? Có cần nhiều cấp duyệt không?
4. Báo giá gửi dạng gì? (PDF / Email / Hệ thống / In)
5. Hiệu lực báo giá? (7 ngày / 15 ngày / 30 ngày)
6. Quy trình follow up: bao nhiêu lần? Khoảng cách bao lâu?
7. Báo giá đặc biệt (giá ưu đãi, dự án lớn) — quy trình riêng?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Quy trình tổng**: Flowchart 8 bước — Tiếp nhận → Thu thập yêu cầu → Tính giá → Duyệt → Tạo báo giá → Gửi → Follow up → Chốt/Hủy
- **Chi tiết từng bước**: Action, owner, timeline, output
- **Phân cấp duyệt giá**: Giá chuẩn (auto) / Giá chiết khấu (Sales Manager) / Giá đặc biệt (Director)
- **SLA báo giá**: Cam kết thời gian phản hồi
- **Follow-up Protocol**: Lịch follow up + script mẫu
- **Tracking**: Template theo dõi trạng thái báo giá
- **Phụ lục**: Quotation request form, Price calculation sheet

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quy trình báo giá (Quotation Process).

CONTEXT:
- DN: [Tên] — SP/DV: [số loại]
- Tiếp nhận: [Sales rep / Admin / Website form]
- SLA phản hồi: [24h / 48h / 72h]
- Duyệt giá: [Sales rep / Manager / Director — tùy mức]
- Format: [PDF / Email / Hệ thống]
- Hiệu lực: [7 / 15 / 30 ngày]
- Follow up: [số lần] — Khoảng cách: [ngày]

FORMAT:
- Flowchart: Mermaid — 8 bước + decision points (giá chuẩn vs đặc biệt)
- Per-step: Bảng Bước | Action | Owner | Timeline | Output | Kiểm soát
- Approval matrix: Bảng Mức giá | Sales Rep | Sales Manager | Director | CEO
- SLA dashboard: Loại RFQ | SLA | Actual avg | Status (đạt/không)
- Follow-up schedule: Ngày 1 | Ngày 3 | Ngày 7 | Ngày 14 — Action + Script ngắn
- Tracking template: RFQ # | KH | SP | Value | Sent date | Status | Next action | Owner
- Error handling: Sai giá / Quá hạn / KH không phản hồi → Xử lý

TONE: SOP chuẩn — rõ ràng, step-by-step.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 09: Proposal Template (Template đề xuất/báo giá chuyên nghiệp)

#### Mô tả
Template proposal/báo giá chuyên nghiệp — không chỉ liệt kê giá mà còn trình bày giá trị, giải pháp, timeline, và điều khoản. Giúp sales rep tạo proposal ấn tượng, chuyên nghiệp, tăng tỷ lệ chốt đơn.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Proposal dùng cho loại bán hàng nào? (dự án / sản phẩm / dịch vụ / retainer)
2. Các phần bắt buộc trong proposal? (cover, summary, pricing, timeline, T&C)
3. Branding: logo, màu sắc, font chữ?
4. Có case study / testimonial để kèm theo không?
5. Điều khoản thanh toán mặc định?
6. Format: Word / PDF / Online / Phần mềm proposal?
7. Proposal trung bình dài bao nhiêu trang?

#### Template gợi ý
Cấu trúc FRM:
- **Cover Page**: Logo, tên KH, tên dự án, ngày, "Prepared by"
- **Executive Summary**: 1 trang — Problem, Solution, Value, Investment
- **About Us**: Giới thiệu DN ngắn gọn, credentials, differentiators
- **Understanding Your Needs**: Tóm tắt nhu cầu KH (customizable)
- **Proposed Solution**: Chi tiết giải pháp, scope, deliverables
- **Pricing & Investment**: Bảng giá rõ ràng, options/packages
- **Timeline & Milestones**: Gantt chart, key milestones
- **Case Studies**: 2-3 case studies tương tự
- **Terms & Conditions**: Thanh toán, warranty, liability, IP
- **Next Steps**: CTA rõ ràng — ký, thanh toán, kick-off
- **Phụ lục**: Technical specs, team profiles (nếu cần)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Proposal Template (Template đề xuất/báo giá chuyên nghiệp).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Loại: [dự án / sản phẩm / dịch vụ / retainer]
- Branding: [logo / màu / font]
- Case studies: [Có/Không] — Số lượng: [số]
- Thanh toán: [đặt cọc % / milestone / full upfront]
- Format: [Word / PDF / Online]
- Độ dài TB: [trang]

FORMAT:
- Cover page: Layout 1 trang — Logo, tên dự án, KH, ngày
- Executive Summary: 4 sections nhỏ — Problem | Solution | Value | Investment
- Solution section: Bảng Deliverable | Description | Timeline | Responsibility
- Pricing table: Hạng mục | Đơn vị | Số lượng | Đơn giá | Thành tiền — có subtotal, VAT, total
- Options/Packages: Bảng so sánh Basic | Standard | Premium (nếu có)
- Timeline: Gantt chart hoặc bảng Phase | Duration | Start | End | Milestone
- T&C: 10-12 điều khoản chuẩn, ngôn ngữ pháp lý nhưng dễ hiểu
- CTA: Next steps rõ ràng + contact info + deadline

TONE: Chuyên nghiệp, tư vấn, win-win.
LENGTH: 8-15 trang A4 (template có placeholder).
```

---

### PROMPT 10: Hợp đồng bán hàng (Sales Contract Template)

#### Mô tả
Template hợp đồng bán hàng / cung cấp dịch vụ chuẩn — bao gồm các điều khoản pháp lý cơ bản, phụ lục mô tả sản phẩm/dịch vụ, và biên bản nghiệm thu. Đảm bảo bảo vệ quyền lợi cả hai bên, giảm rủi ro tranh chấp.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hợp đồng? (mua bán hàng hóa / cung cấp dịch vụ / thuê dịch vụ / subscription)
2. Điều khoản thanh toán mặc định? (đặt cọc, thanh toán theo milestone, COD)
3. Bảo hành / Warranty? (thời hạn, điều kiện, phạm vi)
4. Phạt vi phạm? (% giá trị HĐ / ngày)
5. Giải quyết tranh chấp? (thương lượng → trọng tài → tòa án)
6. Có cần phụ lục kỹ thuật / SLA không?
7. Pháp nhân ký? (cá nhân / công ty — người đại diện, chức vụ)

#### Template gợi ý
Cấu trúc FRM:
- **Phần mở đầu**: Căn cứ pháp lý, thông tin 2 bên (Bên A - Bán, Bên B - Mua)
- **Điều 1** — Đối tượng hợp đồng: Mô tả SP/DV
- **Điều 2** — Giá trị hợp đồng & Phương thức thanh toán
- **Điều 3** — Thời gian & Địa điểm thực hiện
- **Điều 4** — Quyền và nghĩa vụ Bên A
- **Điều 5** — Quyền và nghĩa vụ Bên B
- **Điều 6** — Bảo hành & Hỗ trợ
- **Điều 7** — Bảo mật thông tin
- **Điều 8** — Phạt vi phạm & Bồi thường thiệt hại
- **Điều 9** — Bất khả kháng
- **Điều 10** — Chấm dứt hợp đồng
- **Điều 11** — Giải quyết tranh chấp
- **Điều 12** — Điều khoản chung
- **Phụ lục 1**: Chi tiết SP/DV + Giá
- **Phụ lục 2**: SLA (nếu có)
- **Biên bản nghiệm thu / Biên bản bàn giao**

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Hợp đồng bán hàng (Sales Contract Template).

CONTEXT:
- DN: [Tên] — MST: [số] — Người đại diện: [tên + chức vụ]
- Loại HĐ: [mua bán hàng hóa / cung cấp DV / subscription]
- Thanh toán: [đặt cọc % + milestone / COD / Net X]
- Bảo hành: [thời hạn] — Phạm vi: [mô tả]
- Phạt vi phạm: [% / ngày]
- Tranh chấp: [thương lượng → trọng tài / tòa án]
- Phụ lục SLA: [Có/Không]

FORMAT:
- Chia điều rõ ràng, đánh số khoản liên tục
- Thông tin 2 bên: Bảng Bên A | Bên B — Tên, MST, Địa chỉ, Đại diện, Chức vụ, SĐT, Email
- Bảng giá phụ lục: STT | Hạng mục | ĐVT | SL | Đơn giá | Thành tiền | VAT | Tổng
- Lịch thanh toán: Đợt | % | Số tiền | Điều kiện | Deadline
- SLA (nếu có): Bảng Metric | Target | Measurement | Penalty
- Biên bản nghiệm thu: Header + Nội dung bàn giao + Kết quả kiểm tra + Chữ ký
- Placeholder: [___] cho mọi thông tin tùy biến

TONE: Pháp lý — chính xác, chặt chẽ, cân bằng quyền lợi 2 bên.
LENGTH: 6-10 trang A4 (HĐ + Phụ lục + Biên bản).
```

---

### PROMPT 11: Sales Playbook (Sổ tay bán hàng)

#### Mô tả
Sổ tay bán hàng tổng hợp — "bible" cho đội sales. Gồm buyer persona chi tiết, competitive battlecard, value proposition, qualification criteria, và tất cả thông tin sales rep cần để bán hàng hiệu quả. Mỗi sales rep mới phải đọc trước khi bắt đầu bán.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ: mô tả ngắn, USP, giá?
2. Buyer personas: bao nhiêu persona chính? Mô tả từng persona?
3. Đối thủ cạnh tranh top 3-5? Điểm mạnh/yếu so với mình?
4. Value proposition: tại sao khách nên chọn mình?
5. Qualification criteria: tiêu chí KH lý tưởng?
6. Chu kỳ bán hàng trung bình?
7. Win rate hiện tại? Top lý do win/lose?

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Company & Product Overview: Sứ mệnh, USP, product portfolio
- **Phần 2** — Ideal Customer Profile (ICP): Industry, size, pain points, buying signals
- **Phần 3** — Buyer Personas: 2-4 persona cards chi tiết
- **Phần 4** — Value Proposition Canvas: Pains, Gains, Jobs-to-be-done → Our solution
- **Phần 5** — Competitive Battlecards: Per competitor — overview, strengths, weaknesses, how to win
- **Phần 6** — Qualification Criteria: BANT/MEDDIC scorecard
- **Phần 7** — Sales Messaging: Elevator pitch, email templates, LinkedIn outreach
- **Phần 8** — Win/Loss Analysis: Top reasons, patterns, lessons
- **Phần 9** — FAQ: Top 20 câu hỏi KH hay hỏi + câu trả lời
- **Phụ lục**: Product cheat sheet, Price card, Case study summaries

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Sales Playbook (Sổ tay bán hàng).

CONTEXT:
- DN: [Tên] — SP/DV: [liệt kê + USP]
- Personas: [số] — Mô tả: [từng persona]
- Đối thủ: [liệt kê top 3-5 + điểm mạnh/yếu]
- Value prop: [tại sao chọn mình]
- Qualification: [BANT / MEDDIC / Custom]
- Win rate: [%] — Top win reasons: [3] — Top lose reasons: [3]
- Sales cycle: [ngày]

FORMAT:
- ICP card: Industry | Size | Revenue | Pain Points | Buying Signals | Decision Makers
- Persona cards: 2-4 cards — Photo placeholder, Demographics, Goals, Pains, Objections, Preferred Channels
- Value Prop Canvas: Bảng Customer Jobs | Pains | Gains → Our Products | Pain Relievers | Gain Creators
- Battlecards per competitor: 1 trang/competitor — Overview | They say | We say | When they win | How we win
- Qualification scorecard: Bảng tiêu chí | Weight | Score 1-5 | Verdict (Go/No-go)
- Messaging library: Elevator pitch (30s/60s) + Email (cold/warm/follow-up) + LinkedIn message
- FAQ: 20 Q&A pairs, grouped by topic
- Win/Loss: Bảng Reason | Win % | Lose % | Action

TONE: Sales enablement — energizing, practical, reference-worthy.
LENGTH: 12-18 trang A4.
```

---

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

### PROMPT 13: CRM Setup Guide (Hướng dẫn thiết lập CRM)

#### Mô tả
Hướng dẫn thiết lập CRM cho đội sales — bao gồm custom fields, pipeline stages, automation rules, dashboards, và data hygiene rules. Đảm bảo CRM phục vụ đúng quy trình bán hàng đã chuẩn hóa, không biến thành "bãi rác data".

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. CRM đang dùng hoặc dự định dùng? (HubSpot / Salesforce / Zoho / Pipedrive / Ybai CRM / Custom)
2. Số users dự kiến? Vai trò? (Admin, Manager, Rep)
3. Pipeline stages đã xác định?
4. Custom fields cần thiết ngoài mặc định? (industry, source, deal type...)
5. Cần automation gì? (auto-assign lead, follow-up reminder, stage notification)
6. Dashboards cần: cho rep, cho manager, cho CEO?
7. Integration cần: email, phone, website, chat, marketing tools?

#### Template gợi ý
Cấu trúc FRM:
- **Phần 1** — CRM Strategy: Mục tiêu sử dụng, adoption metrics, governance
- **Phần 2** — Contact & Company Fields: Required fields, custom fields, field types, picklist values
- **Phần 3** — Pipeline Setup: Stages, probability, required fields per stage, exit criteria
- **Phần 4** — Automation Rules: Lead assignment, task creation, notifications, follow-up sequences
- **Phần 5** — Dashboards: Rep dashboard, Manager dashboard, Executive dashboard — KPIs per role
- **Phần 6** — Data Hygiene: Naming conventions, dedup rules, update frequency, data owner
- **Phần 7** — Integration Map: Email, phone, website, marketing, accounting
- **Phần 8** — User Management: Roles, permissions, training plan
- **Phụ lục**: Field reference table, Automation flowcharts, Dashboard mockups

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo CRM Setup Guide (Hướng dẫn thiết lập CRM).

CONTEXT:
- DN: [Tên] — CRM: [Tên phần mềm]
- Users: [số] — Roles: [Admin / Manager / Rep]
- Pipeline stages: [liệt kê]
- Custom fields: [liệt kê]
- Automation: [liệt kê nhu cầu]
- Integration: [email / phone / website / marketing]

FORMAT:
- Field reference: Bảng Field Name | Type | Required | Picklist Values | Description | Where to fill
- Pipeline config: Bảng Stage | Probability | Required Fields | Exit Criteria | Auto-actions
- Automation rules: Bảng Trigger | Condition | Action | Owner | Priority
- Dashboard specs per role:
  - Rep: My pipeline | My activities | My quota
  - Manager: Team pipeline | Forecast | Rep performance
  - CEO: Revenue trend | Win rate | Pipeline health
- Data hygiene: Bảng Rule | Check frequency | Responsible | Action if violation
- Integration map: Mermaid diagram — CRM ↔ Email ↔ Phone ↔ Website ↔ Marketing
- Training plan: Bảng Week | Topic | Duration | Audience | Format

TONE: Hướng dẫn kỹ thuật — rõ ràng, step-by-step, screenshot-friendly.
LENGTH: 6-10 trang A4.
```

---

### PROMPT 14: Báo cáo doanh số (Sales Report Template)

#### Mô tả
Template báo cáo doanh số theo 3 tần suất (daily/weekly/monthly) — theo dõi performance theo rep, sản phẩm, kênh bán, và so sánh với target. Bao gồm variance analysis và action items.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tần suất báo cáo cần? (daily / weekly / monthly / tất cả)
2. KPIs cần theo dõi? (revenue, deals, conversion, activities, pipeline...)
3. Breakdown theo gì? (per rep / per product / per channel / per region)
4. So sánh gì? (vs target / vs prior period / vs prior year)
5. Ai nhận báo cáo? (Sales Manager / Director / CEO)
6. Format? (Excel / Dashboard / Email / Markdown)

#### Template gợi ý
Cấu trúc FRM:
- **Daily Flash Report**: Revenue hôm nay | # Deals closed | Pipeline movement | Top activities
- **Weekly Report**: Revenue WTD | Deals W/L | Pipeline changes | Rep ranking | Actions next week
- **Monthly Report**: Revenue MTD | vs Target | vs Prior | Breakdown per rep/product/channel | Variance analysis | Forecast next month
- **KPI Dashboard**: Visual summary — cards + charts + tables
- **Variance Analysis**: Top 5 positive + negative variances + root cause + actions
- **Rep Leaderboard**: Ranking by revenue, deals, activities
- **Product Performance**: Revenue + margin per product/service

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Báo cáo doanh số (Sales Report Template).

CONTEXT:
- DN: [Tên] — Team size: [số rep]
- Tần suất: [daily / weekly / monthly / all]
- KPIs: [liệt kê]
- Breakdown: [rep / product / channel / region]
- So sánh: [target / prior / prior year]
- Audience: [Sales Manager / Director / CEO]

FORMAT:
- Daily flash: 1 bảng compact — Revenue | Deals | Pipeline | Activities — 5 phút đọc
- Weekly: 1 trang — Revenue WTD vs Target | Win/Loss | Pipeline Δ | Rep ranking | Actions
- Monthly: 2-3 trang — Revenue MTD | vs Target | vs Prior | Breakdown tables | Variance top 5 | Forecast
- KPI cards: Revenue | # Deals | Win Rate | Avg Deal | Pipeline | Activities — Actual | Target | Δ | Status
- Rep leaderboard: Rank | Rep | Revenue | % Quota | Deals | Win Rate | Activity Score
- Product table: Product | Revenue | Units | Margin % | vs Target | Trend
- Variance analysis: KPI | Actual | Target | Var $ | Var % | Root Cause | Action

TONE: Data-driven, concise, executive-friendly.
LENGTH: Daily 1 trang | Weekly 1-2 trang | Monthly 2-3 trang.
```

---

### PROMPT 15: Chính sách đại lý/partner (Agent/Partner Policy)

#### Mô tả
Chính sách toàn diện dành cho đại lý và đối tác phân phối — quy định điều kiện trở thành đại lý, quyền lợi, nghĩa vụ, cơ cấu hoa hồng, territory, KPIs, và quy trình đánh giá. Là "luật chơi" rõ ràng cho mối quan hệ đối tác.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại đối tác? (đại lý bán hàng / distributor / reseller / affiliate / referral partner)
2. Tiêu chí trở thành đối tác? (vốn, kinh nghiệm, nhân sự, vùng miền)
3. Cơ cấu hoa hồng? (% doanh thu / CK theo volume / tiered commission)
4. Có phân territory không? (độc quyền / không độc quyền)
5. KPIs cho đối tác? (doanh số tối thiểu / tháng, quý)
6. Chính sách hỗ trợ? (marketing, training, co-branding, tools)
7. Thời hạn đánh giá? Điều kiện chấm dứt?
8. Cấp bậc đối tác? (Silver / Gold / Platinum?)

#### Template gợi ý
Cấu trúc POL:
- **Điều 1-3** — Mục đích, Phạm vi, Định nghĩa các loại đối tác
- **Điều 4** — Điều kiện & Quy trình trở thành đối tác
- **Điều 5** — Cấp bậc đối tác: Bảng tier + điều kiện + quyền lợi
- **Điều 6** — Quyền lợi đối tác: Hoa hồng, hỗ trợ marketing, training, tools, co-branding
- **Điều 7** — Nghĩa vụ đối tác: Doanh số tối thiểu, báo cáo, brand compliance, chăm sóc KH
- **Điều 8** — Cơ cấu hoa hồng: Bảng chi tiết tier × sản phẩm × %
- **Điều 9** — Territory & Exclusivity: Quy định vùng, xử lý xung đột
- **Điều 10** — Đánh giá & Xếp hạng: KPIs, tần suất, thưởng/phạt
- **Điều 11** — Chấm dứt & Thanh lý: Điều kiện, quy trình, nghĩa vụ sau chấm dứt
- **Phụ lục**: Đơn đăng ký đại lý, Bảng hoa hồng chi tiết, KPI scorecard

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách đại lý/partner (Agent/Partner Policy).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Loại đối tác: [đại lý / distributor / reseller / affiliate / referral]
- Tiêu chí: [vốn / kinh nghiệm / nhân sự / vùng miền]
- Hoa hồng: [% / tiered / hybrid]
- Territory: [độc quyền / không] — Vùng: [liệt kê]
- KPIs: [doanh số min / tháng, quý]
- Cấp bậc: [Silver / Gold / Platinum hoặc custom]
- Hỗ trợ: [marketing / training / tools / co-brand]

FORMAT:
- Đánh số điều liên tục, ngôn ngữ rõ ràng
- Tier matrix: Bảng Cấp | Điều kiện | Hoa hồng % | Hỗ trợ Marketing | Training | Territory
- Commission table: SP | Cấp 1 % | Cấp 2 % | Cấp 3 % | Bonus condition
- KPI scorecard: KPI | Target | Weight | Measurement | Frequency
- Territory map: Vùng | Đại lý | Exclusive? | Population | Market size
- Evaluation timeline: Q1 Review | Mid-year | Annual | Re-certification
- Termination flowchart: Mermaid — Warning → Probation → Termination → Settlement
- Đơn đăng ký: 1 trang form

TONE: Chuyên nghiệp, rõ ràng, công bằng, hấp dẫn cho đối tác tiềm năng.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 16: Partner Agreement Template (Template hợp đồng đại lý/đối tác)

#### Mô tả
Template hợp đồng đại lý/đối tác — bao gồm điều khoản hợp tác, cam kết doanh số, cơ chế thanh toán hoa hồng, bảo mật, cạnh tranh, và chấm dứt. Phải align với Chính sách đại lý (file 15) và bảo vệ quyền lợi hợp pháp cả hai bên.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Loại hợp đồng? (đại lý / phân phối / referral / affiliate)
2. Thời hạn hợp đồng? (1 năm / 2 năm / vô thời hạn)
3. Cam kết doanh số tối thiểu?
4. Thanh toán hoa hồng: tần suất? (hàng tháng / quý) Điều kiện?
5. Điều khoản cạnh tranh? (non-compete / non-solicitation)
6. Bảo mật thông tin?
7. Điều kiện chấm dứt trước hạn?

#### Template gợi ý
Cấu trúc FRM:
- **Phần mở đầu**: Căn cứ, thông tin 2 bên (Bên A - DN, Bên B - Đối tác)
- **Điều 1** — Phạm vi hợp tác: Sản phẩm, territory, khách hàng mục tiêu
- **Điều 2** — Thời hạn hợp đồng & Gia hạn
- **Điều 3** — Cam kết doanh số & KPIs
- **Điều 4** — Giá bán & Chính sách chiết khấu
- **Điều 5** — Hoa hồng & Thanh toán: Cơ cấu, tần suất, điều kiện, phương thức
- **Điều 6** — Quyền & Nghĩa vụ Bên A
- **Điều 7** — Quyền & Nghĩa vụ Bên B
- **Điều 8** — Marketing & Thương hiệu: Co-branding rules, approval process
- **Điều 9** — Bảo mật thông tin
- **Điều 10** — Không cạnh tranh & Không lôi kéo
- **Điều 11** — Chấm dứt hợp đồng: Điều kiện, thông báo, nghĩa vụ thanh lý
- **Điều 12** — Giải quyết tranh chấp
- **Điều 13** — Điều khoản chung
- **Phụ lục**: Danh mục SP, Bảng hoa hồng, Territory map, KPI target

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Partner Agreement Template (Hợp đồng đại lý/đối tác).

CONTEXT:
- DN: [Tên] — MST: [số] — Đại diện: [tên + chức vụ]
- Loại HĐ: [đại lý / phân phối / referral / affiliate]
- Thời hạn: [năm] — Gia hạn: [tự động / thỏa thuận]
- Doanh số min: [số/tháng hoặc /quý]
- Hoa hồng: [% + cơ cấu] — Thanh toán: [tháng / quý]
- Non-compete: [Có/Không] — Phạm vi: [thời gian + territory]
- Chấm dứt: [thông báo trước X ngày]

FORMAT:
- Chia điều rõ ràng, đánh số khoản liên tục
- Thông tin 2 bên: Bảng Bên A | Bên B — đầy đủ pháp lý
- Hoa hồng: Bảng SP | Doanh số từ-đến | % Hoa hồng | Bonus
- KPI target: Bảng KPI | Q1 | Q2 | Q3 | Q4 | Annual
- Thanh toán: Bảng Kỳ | Deadline | Điều kiện | Phương thức
- Non-compete scope: Territory + Duration + Product categories
- Termination checklist: 10 mục cần hoàn thành khi chấm dứt
- Placeholder: [___] cho thông tin tùy biến

TONE: Pháp lý — chặt chẽ nhưng đối tác-friendly.
LENGTH: 6-10 trang A4 (HĐ + Phụ lục).
```

---

### PROMPT 17: Quy trình onboard đối tác (Partner Onboarding SOP)

#### Mô tả
Quy trình chuẩn hóa từ tiếp nhận đối tác mới → đánh giá → ký kết → training → go-live → review. Đảm bảo đối tác được trang bị đủ kiến thức, công cụ, và hỗ trợ để bán hàng hiệu quả từ ngày đầu.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Quy trình đánh giá đối tác hiện tại? Bao nhiêu bước?
2. Ai phụ trách onboard? (Channel Manager / Sales Manager / Team riêng)
3. Training bao gồm những gì? (sản phẩm, quy trình, CRM, marketing)
4. Thời gian onboard trung bình? (1 tuần / 2 tuần / 1 tháng)
5. Toolkit cho đối tác: những gì cần chuẩn bị? (tài liệu, tài khoản, vật phẩm)
6. Review đối tác mới: sau bao lâu? Tiêu chí đánh giá?
7. Có probation period không?

#### Template gợi ý
Cấu trúc SOP:
- **Mục đích & Phạm vi**
- **Tổng quan quy trình**: Flowchart 7 bước — Tiếp nhận → Đánh giá → Phê duyệt → Ký kết → Training → Go-live → Review
- **Bước 1 — Tiếp nhận**: Nhận đơn, sàng lọc sơ bộ, phản hồi
- **Bước 2 — Đánh giá**: Due diligence, scoring, phỏng vấn
- **Bước 3 — Phê duyệt**: Trình duyệt, điều kiện, thông báo kết quả
- **Bước 4 — Ký kết**: Chuẩn bị HĐ, ký, setup tài khoản
- **Bước 5 — Training**: Chương trình training 5-10 ngày, quiz/test
- **Bước 6 — Go-live**: First deal support, shadowing, check-in
- **Bước 7 — Review 30/60/90**: Đánh giá, feedback, điều chỉnh, graduation
- **Onboarding Toolkit**: Checklist tất cả tài liệu/công cụ cần chuẩn bị
- **Phụ lục**: Training curriculum, Partner welcome kit, Evaluation form

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Onboard đối tác (Partner Onboarding SOP).

CONTEXT:
- DN: [Tên] — Loại đối tác: [đại lý / distributor / affiliate]
- Người phụ trách: [Channel Manager / Sales Manager / Team]
- Thời gian onboard: [tuần / tháng]
- Training nội dung: [sản phẩm / quy trình / CRM / marketing]
- Toolkit: [liệt kê tài liệu + tools]
- Probation: [Có/Không] — [thời hạn]
- Review: [30 / 60 / 90 ngày]

FORMAT:
- Flowchart: Mermaid — 7 bước + timeline tổng + responsible
- Per-step detail: Bảng Bước | Actions | Owner | Duration | Output | Checklist
- Evaluation scorecard: Bảng Tiêu chí | Weight | Score 1-5 | Pass/Fail threshold
- Training curriculum: Bảng Ngày | Module | Nội dung | Duration | Trainer | Deliverable
- Onboarding checklist: 30+ mục ☐ — grouped by Trước ký | Sau ký | Trước go-live | Sau go-live
- 30/60/90 review: Bảng KPI | 30-day target | 60-day target | 90-day target | Actual | Status
- Partner welcome kit: Danh sách tất cả tài liệu + link + mô tả
- Graduation criteria: Bảng tiêu chí → Đạt = Đại lý chính thức | Không đạt = Gia hạn/Chấm dứt

TONE: SOP chuẩn — welcoming nhưng có process rõ ràng.
LENGTH: 6-8 trang A4.
```

---

## Ghi chú triển khai

### Dependencies
- `man-sales-strategy-target.md` là file gốc — tất cả file sales khác phải align với chiến lược và mục tiêu trong đây
- `man-pricing-strategy.md` là input trực tiếp cho `sop-quy-trinh-bao-gia.md` và `frm-proposal-template.md`
- `sop-sales-process.md` là quy trình chủ đạo — `frm-sales-script.md`, `frm-objection-handling.md`, `sop-quy-trinh-bao-gia.md` là công cụ hỗ trợ từng bước trong quy trình
- `man-sales-playbook.md` tổng hợp thông tin từ strategy, script, objection handling, competitive intel
- `pol-chinh-sach-dai-ly.md` là nền tảng cho `frm-partner-agreement.md` và `sop-onboard-doi-tac.md`
- `frm-sales-pipeline-tracker.md` và `frm-crm-setup-guide.md` phải sync về stages, fields, và metrics
- `frm-bao-cao-doanh-so.md` tổng hợp data từ pipeline tracker, CRM, và phản ánh KPIs trong strategy
- `rpt-unit-economics.md` cần data từ `frm-bao-cao-doanh-so.md` và input từ 03-Finance (chi phí marketing/sales)

### Lưu ý
> **QUAN TRỌNG**: Các tài liệu sales trong skill này cần được customize theo ngành nghề, mô hình kinh doanh, và quy mô DN. Sales B2B khác biệt lớn so với B2C — quy trình dài hơn, nhiều stakeholders hơn, deal size lớn hơn. DN cần xác định rõ mô hình bán hàng trước khi áp dụng templates. Các hợp đồng (file 10, 16) nên được review bởi luật sư/tư vấn pháp lý trước khi sử dụng chính thức.

### Thứ tự tạo khuyến nghị
1. Sales Strategy & Target → 2. Pricing Strategy → 3. Channel Strategy → 4. Unit Economics
5. SOP Sales Process → 6. Sales Script → 7. Objection Handling → 8. SOP Quy trình báo giá → 9. Proposal Template → 10. Hợp đồng bán hàng
11. Sales Playbook → 12. Sales Pipeline Tracker → 13. CRM Setup Guide → 14. Báo cáo doanh số
15. Chính sách đại lý/partner → 16. Partner Agreement → 17. SOP Onboard đối tác

---

### VIII.8 — BP Marketing (Marketing & Thương Hiệu)

> **Tầng 3: Tăng Trưởng** — 18 tài liệu: Chiến lược marketing (5), Digital Marketing (5), Tài liệu bán hàng (5), Đo lường (3).

---

### PROMPT 01: Marketing Plan năm (Annual Marketing Plan)

#### Mô tả
Kế hoạch marketing tổng thể cho cả năm — bao gồm mục tiêu marketing, phân tích target audience, định vị thương hiệu, chiến lược kênh, phân bổ ngân sách, KPIs, và timeline triển khai theo quý. Đây là "bản đồ tác chiến" để toàn bộ marketing team align và thực thi.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mục tiêu kinh doanh năm nay? (doanh thu, tăng trưởng %, thị phần?)
2. Target audience chính? (B2B/B2C, demographics, psychographics, pain points?)
3. Kênh marketing đang dùng? (Online: Facebook, Google, SEO, Email. Offline: event, PR, print?)
4. Ngân sách marketing năm? (% doanh thu hoặc con số cụ thể?)
5. Đối thủ chính? (3-5 đối thủ và positioning hiện tại?)
6. USP / Giá trị khác biệt cốt lõi?

#### Template gợi ý
Cấu trúc MAN:
- **Executive Summary**: Tóm tắt 1 trang — mục tiêu, chiến lược chính, ngân sách, KPIs
- **Situation Analysis**: SWOT marketing, market overview, competitive landscape
- **Target Audience**: Persona(s), customer segments, demographics + psychographics
- **Positioning & Messaging**: Brand positioning statement, key messages, tone of voice
- **Channel Strategy**: Ma trận kênh × mục tiêu × ngân sách × KPIs
- **Campaign Calendar**: Timeline Q1-Q4 — chiến dịch chính, seasonal events, launches
- **Budget Allocation**: By channel, by quarter, contingency fund
- **KPIs & Measurement**: Bảng KPI × Target × Frequency × Tool đo

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Marketing Plan năm (Annual Marketing Plan).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Doanh thu target: [số]
- Target audience: [B2B/B2C] — Persona: [mô tả]
- Kênh hiện tại: [liệt kê]
- Ngân sách marketing: [số / % doanh thu]
- Đối thủ chính: [3-5 tên]
- USP: [giá trị khác biệt]

FORMAT:
- Executive summary: 1 trang — BLUF, 5 bullet points chính
- SWOT marketing: Ma trận 2×2 + chiến lược SO/ST/WO/WT
- Persona cards: 2-3 personas — Tên | Tuổi | Nghề | Pain points | Goals | Kênh ưa thích
- Channel matrix: Bảng Kênh | Mục tiêu | Budget | KPI | Owner | Priority
- Campaign calendar: Gantt-style Q1-Q4 — Campaign | Kênh | Budget | Timeline | KPI
- Budget breakdown: Pie chart placeholder — Online [%] | Offline [%] | Content [%] | Tools [%] | Contingency [%]
- KPI dashboard: Bảng KPI | Target Q1 | Q2 | Q3 | Q4 | YTD | Tool đo

TONE: Executive, strategic, actionable.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 02: Content Strategy (Chiến lược nội dung)

#### Mô tả
Chiến lược nội dung tổng thể — xác định content pillars, content types, distribution channels, editorial calendar framework, và content performance metrics. Đảm bảo mọi nội dung tạo ra đều phục vụ mục tiêu kinh doanh và đúng brand voice.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mục tiêu content marketing? (Brand awareness / Lead gen / Thought leadership / SEO?)
2. Target audience đọc/xem content ở đâu? (Facebook, YouTube, TikTok, Blog, LinkedIn?)
3. Content hiện tại: loại nào đang hoạt động tốt? Loại nào không?
4. Nguồn lực content: mấy người? In-house hay outsource?
5. Brand voice / Tone: chuyên nghiệp, gần gũi, hài hước, thought-leader?
6. Tần suất đăng bài hiện tại? Target tần suất?

#### Template gợi ý
Cấu trúc MAN:
- **Content Mission Statement**: Tuyên bố sứ mệnh nội dung — "Chúng tôi tạo content cho [audience] để [mục đích]"
- **Content Pillars**: 3-5 trụ cột nội dung, mỗi pillar có sub-topics
- **Content Types & Formats**: Blog, Video, Infographic, Podcast, Case Study, Social Post...
- **Distribution Channels**: Owned (blog, email), Earned (PR, guest post), Paid (ads, sponsored)
- **Editorial Calendar Framework**: Cadence, workflow, approval process
- **Content Performance Metrics**: Engagement, reach, traffic, leads, conversion
- **Content Governance**: Brand voice guide, style guide, approval workflow

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Content Strategy (Chiến lược nội dung).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Mục tiêu content: [awareness / lead gen / thought leadership / SEO]
- Audience: [persona chính]
- Kênh: [Facebook / YouTube / TikTok / Blog / LinkedIn]
- Team content: [số người] — [in-house / outsource]
- Brand voice: [tone]

FORMAT:
- Content mission: 1 câu tuyên bố
- Content pillars: Bảng Pillar | Sub-topics | Mục tiêu | % tổng content | Ví dụ
- Content matrix: Bảng Type | Format | Channel | Frequency | Effort | Impact
- Distribution map: Kênh | Loại content | Tần suất | Best time | CTA
- Editorial workflow: Flowchart — Ideation → Brief → Create → Review → Approve → Publish → Measure
- Performance framework: Bảng Metric | Definition | Target | Tool | Frequency
- Content audit template: Bảng Content hiện tại | Type | Performance | Keep/Update/Archive

TONE: Creative yet strategic, data-informed.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 03: Customer Journey Map (Bản đồ hành trình khách hàng)

#### Mô tả
Bản đồ hành trình khách hàng — từ awareness → consideration → decision → purchase → retention → advocacy. Map từng touchpoint, emotion, pain point, và opportunity ở mỗi giai đoạn. Giúp marketing và sales phối hợp tối ưu trải nghiệm KH.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ chính để map? (chọn 1 sản phẩm flagship)
2. Persona chính? (ai là khách hàng điển hình?)
3. Touchpoints hiện tại? (website, MXH, email, điện thoại, gặp trực tiếp, event?)
4. Pain points lớn nhất KH đang gặp ở giai đoạn nào?
5. Thời gian trung bình từ awareness đến purchase? (ngày/tuần/tháng?)
6. Có data NPS hoặc feedback KH không?

#### Template gợi ý
Cấu trúc RPT:
- **Persona Summary**: Tóm tắt persona được map
- **Journey Stages**: 6 giai đoạn (Awareness → Consideration → Decision → Purchase → Retention → Advocacy)
- **Per Stage**: Actions | Touchpoints | Emotions | Pain Points | Opportunities | KPIs
- **Moment of Truth**: Các điểm quyết định quan trọng nhất
- **Gap Analysis**: Khoảng cách giữa trải nghiệm hiện tại và kỳ vọng
- **Action Plan**: Cải thiện ưu tiên theo từng giai đoạn

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Customer Journey Map (Bản đồ hành trình khách hàng).

CONTEXT:
- DN: [Tên] — Sản phẩm: [tên SP/DV]
- Persona: [tên persona] — [mô tả ngắn]
- Touchpoints: [liệt kê]
- Cycle time: [thời gian từ awareness → purchase]
- Pain points chính: [liệt kê]
- NPS / Feedback: [có/không — dữ liệu]

FORMAT:
- Journey map visual: Bảng Stage × (Actions | Touchpoints | Emotions 😊😐😞 | Pain Points | Opportunities)
- Emotion curve: ASCII graph — positive/negative by stage
- Touchpoint matrix: Bảng Touchpoint | Stage | Channel | Owner | Current Rating | Target
- Moment of Truth: Top 3-5 critical moments — What | Why | Current | Ideal
- Gap analysis: Bảng Stage | Customer Expectation | Current Experience | Gap | Priority
- Action plan: Bảng # | Action | Stage | Impact | Effort | Owner | Timeline
- Quick wins: 3-5 actions có thể làm ngay trong 30 ngày

TONE: Customer-centric, empathetic, insight-driven.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 04: Competitive Analysis Marketing (Phân tích đối thủ marketing)

#### Mô tả
Phân tích chi tiết hoạt động marketing của đối thủ — positioning, messaging, kênh truyền thông, nội dung, social media, paid ads, SEO, và nhận thức thị phần. Giúp DN xác định lợi thế cạnh tranh và tìm cơ hội khác biệt hóa.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Đối thủ cần phân tích? (3-5 tên + website)
2. Đối thủ trực tiếp hay gián tiếp?
3. Kênh nào cần focus phân tích? (Social, SEO, Paid Ads, Content, PR?)
4. Có data nào về đối thủ rồi? (traffic estimate, social followers, ad library?)
5. Mục đích phân tích? (tìm gap, benchmark, repositioning?)

#### Template gợi ý
Cấu trúc RPT:
- **Overview**: Ma trận tổng quan — DN vs Đối thủ A vs B vs C
- **Positioning & Messaging**: Brand promise, tagline, key messages, tone
- **Channel Analysis**: Social media, website/SEO, paid ads, email, PR, events
- **Content Analysis**: Content types, frequency, engagement, top-performing content
- **Digital Footprint**: Traffic, domain authority, keyword rankings, backlinks
- **SWOT of Each Competitor**: Điểm mạnh/yếu marketing của từng đối thủ
- **Opportunities & Recommendations**: Gaps DN có thể khai thác

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Competitive Analysis Marketing (Phân tích đối thủ marketing).

CONTEXT:
- DN: [Tên] — Website: [URL]
- Đối thủ: [A: URL] | [B: URL] | [C: URL]
- Loại: [trực tiếp / gián tiếp]
- Focus: [Social / SEO / Ads / Content / All]
- Data sẵn có: [traffic estimate / social stats / ad library]
- Mục đích: [tìm gap / benchmark / repositioning]

FORMAT:
- Comparison matrix: Bảng Tiêu chí | DN | Đối thủ A | B | C — 15+ tiêu chí
- Social media scorecard: Bảng Platform | Followers | Engagement Rate | Post Frequency | Top Content Type — per competitor
- SEO comparison: Bảng Domain Authority | Organic Traffic | Top Keywords | Content Volume | Backlinks
- Content audit: Bảng Content Type | Frequency | Avg Engagement | Best Performer — per competitor
- Messaging map: Bảng Competitor | Tagline | Key Messages | Tone | Target Audience
- Gap analysis: Bảng Kênh/Tactic | Competitor A | B | C | DN | GAP/Opportunity
- Recommendations: Top 5 actions ranked by Impact × Feasibility

TONE: Analytical, objective, competitive intelligence.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 05: Marketing Budget Allocation (Phân bổ ngân sách marketing)

#### Mô tả
Tài liệu phân bổ ngân sách marketing — chia theo kênh, theo chiến dịch, theo quý. Bao gồm ROI benchmarks cho từng kênh, triggers để tái phân bổ ngân sách, và quy trình duyệt chi tiêu marketing.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Tổng ngân sách marketing năm? (VNĐ hoặc % doanh thu?)
2. Phân bổ hiện tại? (% cho online vs offline vs tools?)
3. Kênh nào đang cho ROI tốt nhất? Kênh nào kém?
4. Có seasonal peaks không? (Tết, 11/11, Black Friday, mùa cao điểm ngành?)
5. Quy trình duyệt chi tiêu? (< X triệu: Marketing Manager | > X: CMO | > Y: CEO?)
6. Có contingency fund không? (% ngân sách dự phòng?)

#### Template gợi ý
Cấu trúc MAN:
- **Budget Overview**: Tổng ngân sách, % doanh thu, so sánh YoY
- **Channel Allocation**: Breakdown theo kênh — Paid, Organic, Content, Tools, Events, HR
- **Campaign Budget**: Breakdown theo chiến dịch lớn trong năm
- **Quarterly Breakdown**: Q1-Q4 phân bổ theo mùa vụ
- **ROI Benchmarks**: Target ROI/ROAS cho từng kênh
- **Reallocation Triggers**: Điều kiện để chuyển ngân sách giữa các kênh
- **Approval Process**: Quy trình duyệt chi tiêu theo hạn mức

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Marketing Budget Allocation (Phân bổ ngân sách marketing).

CONTEXT:
- DN: [Tên] — Tổng budget marketing: [số VNĐ / % doanh thu]
- Phân bổ hiện tại: Online [%] | Offline [%] | Tools [%]
- ROI kênh tốt nhất: [kênh] — ROI kênh kém: [kênh]
- Seasonal peaks: [liệt kê tháng/sự kiện]
- Approval: < [X] triệu (Marketing Manager) | > [X] (CMO) | > [Y] (CEO)
- Contingency: [%]

FORMAT:
- Budget summary: Bảng 1 trang — Tổng | Online | Offline | Content | Tools | Events | Contingency
- Channel breakdown: Bảng Kênh | Budget Q1 | Q2 | Q3 | Q4 | Total | % | Target ROI
- Campaign budget: Bảng Campaign | Timing | Budget | Channels | Expected ROI | Owner
- Monthly cash flow: Bảng Tháng × Kênh — dự kiến chi tiêu
- ROI benchmarks: Bảng Kênh | Industry Avg ROI | Our Target | Min Acceptable | Action if Below
- Reallocation rules: Decision tree — Performance < X% → Review → Reallocate → To where
- Approval matrix: Giá trị | Approver | Timeline | Chứng từ cần

TONE: Financial, data-driven, ROI-focused.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 06: SOP Quy trình chạy Ads (Paid Advertising SOP)

#### Mô tả
Quy trình chuẩn hóa chạy quảng cáo Facebook/Google Ads — từ planning, setup campaign, creative production, launch, optimize, đến report. Bao gồm A/B testing protocol, budget management, và escalation khi performance kém.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Platform ads chính? (Facebook/Meta Ads, Google Ads, TikTok Ads, LinkedIn Ads?)
2. Ngân sách ads tháng? Phân bổ per platform?
3. Mục tiêu ads chính? (Traffic, Leads, Conversions, Brand Awareness?)
4. Ai chạy ads? (In-house / Agency / Hybrid?)
5. Có quy trình duyệt creative trước khi chạy không?
6. Reporting frequency? (Daily / Weekly / Monthly?)

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Planning: Objective, audience, budget, timeline
- **Bước 2** — Audience Setup: Targeting, custom audiences, lookalike
- **Bước 3** — Creative Production: Ad copy, visual, video, CTA
- **Bước 4** — Campaign Setup: Campaign structure, ad sets, placements
- **Bước 5** — Launch & Monitor: Go-live checklist, daily monitoring
- **Bước 6** — Optimize: A/B testing, bid adjustment, audience refinement
- **Bước 7** — Report & Learn: Performance report, insights, next steps

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quy trình chạy Ads (Paid Advertising).

CONTEXT:
- DN: [Tên] — Platform: [Facebook / Google / TikTok / LinkedIn]
- Budget ads: [tháng] — Split: [Facebook %] [Google %] [Khác %]
- Mục tiêu: [Traffic / Leads / Conversions / Awareness]
- Team: [In-house / Agency / Hybrid]
- Duyệt creative: [Có/Không] — Approver: [ai]
- Reporting: [Daily / Weekly / Monthly]

FORMAT:
- Flowchart 7 bước: Mermaid — Planning → Setup → Creative → Launch → Monitor → Optimize → Report
- Campaign brief template: Objective | Audience | Budget | Timeline | KPIs | Creative brief
- A/B testing protocol: Bảng Variable | Version A | Version B | Duration | Sample Size | Winner Criteria
- Daily monitoring checklist: ☐ Spend | ☐ CPC/CPM | ☐ CTR | ☐ Conversions | ☐ ROAS | ☐ Anomalies
- Optimization triggers: Bảng Metric | Threshold | Action — VD: CTR < 1% → Review creative
- Budget pacing: Bảng Ngày × Planned Spend × Actual × Variance
- Report template: Executive summary | KPIs | Top campaigns | Insights | Recommendations

TONE: SOP chuẩn, performance-focused, data-driven.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 07: SOP Quy trình SEO (Search Engine Optimization SOP)

#### Mô tả
Quy trình SEO toàn diện — từ audit website, nghiên cứu từ khóa, tối ưu on-page, technical SEO, xây dựng content SEO, đến link building và monitoring. Đảm bảo website DN được tìm thấy trên Google cho các từ khóa mục tiêu.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Website hiện tại? Domain authority / traffic ước tính?
2. Đã làm SEO chưa? Kết quả hiện tại? Top keywords?
3. Target keywords / topics chính?
4. Có blog / content hub không?
5. Team SEO: mấy người? In-house hay agency?
6. Tools đang dùng? (Google Search Console, Analytics, Ahrefs, SEMrush?)

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — SEO Audit: Technical audit, on-page audit, content audit, backlink audit
- **Bước 2** — Keyword Research: Seed keywords, long-tail, search intent, difficulty/volume
- **Bước 3** — On-Page Optimization: Title, meta, headings, content, internal linking, schema
- **Bước 4** — Technical SEO: Site speed, mobile, crawlability, indexation, Core Web Vitals
- **Bước 5** — Content Creation: SEO content brief, writing guidelines, optimization checklist
- **Bước 6** — Link Building: Guest post, digital PR, broken link, resource pages
- **Bước 7** — Monitoring & Reporting: Rank tracking, traffic, conversions, monthly report

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quy trình SEO (Search Engine Optimization).

CONTEXT:
- DN: [Tên] — Website: [URL]
- Domain Authority: [DA] — Traffic: [monthly visitors]
- SEO history: [mới / đã làm X tháng]
- Target keywords: [5-10 từ khóa chính]
- Blog: [Có/Không] — Số bài: [số]
- Team: [số người] — [in-house / agency]
- Tools: [GSC / GA / Ahrefs / SEMrush / khác]

FORMAT:
- SEO audit checklist: 30+ mục — Technical | On-Page | Content | Backlinks — ☐ Check × Status × Priority
- Keyword research template: Bảng Keyword | Volume | Difficulty | Intent | Current Rank | Target | Content Needed
- On-page checklist: Per-page — Title ☐ | Meta ☐ | H1 ☐ | Content ☐ | Images ☐ | Internal Links ☐ | Schema ☐
- Content brief template: Target keyword | Search intent | Outline | Word count | Internal links | CTA
- Link building tracker: Bảng Target Site | DA | Status | Outreach Date | Response | Link URL
- Monthly SEO report: Rankings Δ | Traffic Δ | Top Pages | New Keywords | Actions
- 90-day SEO roadmap: Bảng Week × Tasks — prioritized by impact

TONE: SOP kỹ thuật, systematic, measurable.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 08: SOP Quy trình Email Marketing

#### Mô tả
Quy trình email marketing toàn diện — từ xây dựng danh sách, phân nhóm, tạo nội dung, automation sequences, A/B testing, đến analytics và optimization. Bao gồm compliance (CAN-SPAM, GDPR) và deliverability best practices.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Nền tảng email marketing? (Mailchimp, HubSpot, GetResponse, SendGrid, Ybai?)
2. Kích thước email list hiện tại? Tốc độ tăng trưởng?
3. Loại email gửi? (Newsletter, Promotion, Onboarding, Abandoned cart, Re-engagement?)
4. Tần suất gửi? (hàng tuần / 2 lần/tuần / hàng tháng?)
5. Có automation sequences chưa? (Welcome series, drip campaigns?)
6. Open rate / Click rate trung bình hiện tại?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — List Building: Lead magnets, opt-in forms, segmentation strategy
- **Bước 2** — Segmentation: Criteria, tags, dynamic segments
- **Bước 3** — Content Creation: Subject line, preview text, body, CTA, design
- **Bước 4** — Automation Setup: Welcome series, nurture sequence, triggers
- **Bước 5** — A/B Testing: Subject lines, send time, content, CTAs
- **Bước 6** — Send & Monitor: Deliverability, bounces, complaints
- **Bước 7** — Analytics & Optimization: Open rate, CTR, conversions, unsubscribes

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Quy trình Email Marketing.

CONTEXT:
- DN: [Tên] — Platform: [Mailchimp / HubSpot / GetResponse / Ybai]
- List size: [số] — Growth rate: [số/tháng]
- Email types: [Newsletter / Promo / Onboarding / Abandoned / Re-engagement]
- Frequency: [tần suất]
- Automation: [Có/Không] — Sequences: [liệt kê]
- Current metrics: Open [%] | Click [%]

FORMAT:
- Flowchart 7 bước: Mermaid — List Build → Segment → Content → Automate → Test → Send → Analyze
- List building strategies: 5-7 tactics — Lead magnet | Form placement | Incentive | Expected conversion
- Segmentation matrix: Bảng Segment | Criteria | Size | Content Type | Frequency
- Email template library: 5 templates — Welcome | Newsletter | Promo | Re-engagement | Transactional
- A/B test protocol: Bảng Element | Variant A | Variant B | Sample % | Duration | Winner = ?
- Automation workflows: 3 flows — Welcome (5 emails) | Nurture (7 emails) | Re-engage (3 emails) — timeline + content outline
- Performance benchmarks: Bảng Metric | Industry Avg | Our Target | Action if Below

TONE: SOP chuẩn, conversion-focused, data-driven.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 09: Social Media Playbook (Sổ tay mạng xã hội)

#### Mô tả
Sổ tay toàn diện cho hoạt động social media — bao gồm chiến lược từng nền tảng, lịch đăng bài, content mix, quy tắc tương tác, xử lý khủng hoảng truyền thông, và hướng dẫn làm việc với influencer/KOL.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Nền tảng MXH chính? (Facebook, Instagram, TikTok, YouTube, LinkedIn, Zalo OA?)
2. Mục tiêu MXH? (Brand awareness, Community, Lead gen, Customer service?)
3. Tần suất đăng bài hiện tại / target? Per platform?
4. Content mix hiện tại? (% giáo dục / giải trí / bán hàng / behind-the-scenes?)
5. Có làm việc với KOL/Influencer không?
6. Đã gặp khủng hoảng truyền thông MXH chưa? Quy trình xử lý?

#### Template gợi ý
Cấu trúc MAN:
- **Platform Strategy**: Mục tiêu + chiến lược cho TỪNG nền tảng
- **Content Mix**: Tỷ lệ nội dung — Educate / Entertain / Engage / Sell
- **Posting Schedule**: Tần suất, best time, calendar template
- **Engagement Protocol**: Cách reply comment, DM, mention, review
- **Crisis Management**: Phân loại tình huống, escalation, response template
- **Influencer/KOL Guidelines**: Tiêu chí chọn, brief template, đo lường hiệu quả
- **Brand Voice on Social**: Tone, do's and don'ts, ví dụ tốt/xấu

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Social Media Playbook (Sổ tay mạng xã hội).

CONTEXT:
- DN: [Tên] — Platforms: [Facebook / IG / TikTok / YouTube / LinkedIn / Zalo]
- Mục tiêu MXH: [awareness / community / leads / support]
- Posting: [tần suất per platform]
- Content mix: Educate [%] | Entertain [%] | Engage [%] | Sell [%]
- KOL: [Có/Không] — Budget KOL: [số]
- Crisis history: [Có/Không]

FORMAT:
- Platform profile cards: Per platform — Mục tiêu | Audience | Content type | Frequency | KPIs | Best time
- Content mix pie: 80/20 hoặc custom — Value vs Sell ratio
- Weekly posting schedule: Bảng Thứ × Platform — Content type + time slot
- Engagement SOP: Bảng Tình huống | Response time | Tone | Template | Escalation
- Crisis playbook: Level 1 (comment tiêu cực) → Level 2 (viral xấu) → Level 3 (khủng hoảng) — Response flow
- KOL evaluation: Bảng Tiêu chí | Trọng số | Scoring — Followers | Engagement | Relevance | Cost | Brand fit
- Do/Don't list: 10 Do's + 10 Don'ts trên MXH — có ví dụ cụ thể

TONE: Social-savvy, brand-conscious, practical.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 10: Content Calendar Template (Template lịch nội dung)

#### Mô tả
Template lịch nội dung chuẩn hóa — view daily/weekly/monthly, phân loại content type, kênh phân phối, trạng thái sản xuất, người phụ trách, và tracking hiệu quả. Giúp marketing team plan, execute, và đo lường content một cách hệ thống.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Bao nhiêu kênh content cần quản lý?
2. Bao nhiêu bài/content pieces per tuần?
3. Workflow production: mấy bước? (Idea → Brief → Create → Review → Approve → Publish)
4. Tool quản lý: Spreadsheet / Notion / Trello / chuyên dụng?
5. Cần tracking performance trên calendar không?

#### Template gợi ý
Cấu trúc FRM:
- **Monthly View**: Tháng × Tuần — themes, campaigns, holidays
- **Weekly View**: 7 ngày × kênh × content type — chi tiết
- **Production Pipeline**: Idea → Brief → Draft → Review → Approved → Scheduled → Published
- **Content Details**: Title, type, channel, copy, visual, CTA, hashtags, links
- **Performance Tracking**: Reach, engagement, clicks, conversions — per post
- **Legend**: Color codes cho content type, status, channel

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Content Calendar Template (Lịch nội dung).

CONTEXT:
- DN: [Tên] — Kênh: [liệt kê] — Số content/tuần: [số]
- Workflow: [số bước]
- Tool: [Spreadsheet / Notion / Trello]
- Track performance: [Có/Không]

FORMAT:
- Monthly overview: Bảng Tuần 1-4 × Theme | Campaign | Key dates | Content count
- Weekly detail: Bảng Thứ 2-CN × Channel | Content Type | Title | Status | Owner | Publish Time
- Content card template: Title | Type | Channel | Copy (excerpt) | Visual brief | CTA | Hashtags | Link | Status | Owner | Due | Published | Performance
- Status workflow: Idea 💡 → Briefed 📋 → Creating ✏️ → Review 👀 → Approved ✅ → Scheduled 📅 → Published 🚀 → Analyzed 📊
- Performance tracker: Bảng Post | Date | Channel | Reach | Engagement | Clicks | Conv | Notes
- Recurring content: Bảng Series/Recurring | Frequency | Day | Template

TONE: Practical, visual, easy to maintain.
LENGTH: 3-5 trang A4.
```

---

### PROMPT 11: Company Brochure (Template brochure công ty)

#### Mô tả
Template và copy guidelines cho brochure công ty — bao gồm cấu trúc trang, nội dung từng section (company story, services, case studies, team, contact), và quy tắc viết copy. Dùng cho cả digital và print.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mục đích brochure? (Sales meeting, Event, General marketing?)
2. Bao nhiêu trang? (4 / 8 / 12 / 16 trang?)
3. Sản phẩm/dịch vụ chính cần highlight? (top 3-5?)
4. Có case study / số liệu thành tựu chưa?
5. Brand guidelines: màu sắc, font, logo, tone?
6. Print hay digital? Kích thước? (A4 / A5 / custom?)

#### Template gợi ý
Cấu trúc FRM:
- **Cover**: Logo, tagline, hero image placeholder
- **About Us**: Company story, mission/vision, founding year, key numbers
- **Services/Products**: Top 3-5 offerings — problem → solution → benefit
- **Why Choose Us**: USPs, differentiators, methodology
- **Case Studies**: 2-3 mini case studies — challenge, solution, results
- **Team/Leadership**: Key team members, expertise
- **Clients/Partners**: Logo wall, notable clients
- **Contact & CTA**: Contact info, next steps, QR code

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Company Brochure Template (Template brochure công ty).

CONTEXT:
- DN: [Tên] — Ngành: [ngành] — Thành lập: [năm]
- Mục đích: [Sales / Event / General]
- Số trang: [4/8/12/16]
- Sản phẩm chính: [top 3-5]
- Thành tựu: [key numbers]
- Brand: Màu [code] | Font [tên] | Tone [mô tả]
- Format: [Print A4 / Digital / Both]

FORMAT:
- Page-by-page layout: Trang | Section | Content | Visual | Copy guidelines
- Copy templates: Mỗi section — headline formula + body copy structure + CTA
- Headline formulas: 5 options per section — pattern + ví dụ
- Word count guide: Section | Min | Max | Must include
- Visual brief: Section | Image type | Size | Mood | Reference
- Design specs: Margins, grid, typography scale, color usage rules
- Print checklist: Resolution, bleed, color mode, paper stock

TONE: Brand-aligned, professional, persuasive.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 12: Product One-Pager (Template giới thiệu sản phẩm 1 trang)

#### Mô tả
Template giới thiệu sản phẩm/dịch vụ trong 1 trang — bao gồm problem statement, solution, features, benefits, pricing/packages, và CTA. Dùng cho sales, event, email attachment.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ cần giới thiệu?
2. Đối tượng đọc? (CEO, Trưởng phòng, Technical, End-user?)
3. Top 3 pain points mà SP giải quyết?
4. Top 3-5 features nổi bật?
5. Có pricing / packages không? Hiển thị trên one-pager?
6. CTA mong muốn? (Demo, Trial, Contact, Buy?)

#### Template gợi ý
Cấu trúc FRM:
- **Header**: Product name, tagline, logo
- **Problem**: 2-3 câu mô tả vấn đề KH đang gặp
- **Solution**: Giải pháp của DN — 1 đoạn ngắn
- **Key Features**: 3-5 features + icons placeholder
- **Benefits**: 3-5 benefits — outcome-focused
- **Social Proof**: 1-2 testimonials hoặc key metrics
- **Pricing/Packages**: Tùy chọn hiển thị hoặc không
- **CTA**: Next step rõ ràng + contact info

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Product One-Pager Template (Giới thiệu sản phẩm 1 trang).

CONTEXT:
- DN: [Tên] — Sản phẩm: [tên]
- Audience: [CEO / Manager / Technical / End-user]
- Pain points: [top 3]
- Features: [top 3-5]
- Pricing: [hiển thị / ẩn]
- CTA: [Demo / Trial / Contact / Buy]

FORMAT:
- Layout 1 trang A4: Header (15%) | Problem (10%) | Solution (15%) | Features (20%) | Benefits (15%) | Proof (10%) | CTA (15%)
- Copy formulas: Per section — pattern + ví dụ
- Feature block: Icon placeholder | Feature name | 1-line description
- Benefit block: Outcome statement — "Giúp bạn [kết quả] thay vì [pain point]"
- Social proof: Metric callout (VD: "2.000+ DN đã sử dụng") hoặc Quote box
- CTA block: Button text + URL + Phone + QR code placeholder
- Variations: Version A (with pricing) | Version B (without pricing) | Version C (technical focus)

TONE: Concise, benefit-focused, persuasive.
LENGTH: 1 trang A4 (+ copy guidelines 2 trang).
```

---

### PROMPT 13: Case Study Template

#### Mô tả
Template case study chuẩn — cấu trúc Challenge → Solution → Results, kèm testimonial và key metrics. Dùng cho website, sales collateral, social proof.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có bao nhiêu case study cần viết? Ưu tiên ngành/loại KH nào?
2. Khách hàng có đồng ý cho phép sử dụng tên/logo không?
3. Có dữ liệu kết quả cụ thể không? (%, số liệu, timeline)
4. Format: dài (1-2 trang) hay ngắn (1/2 trang)?
5. Kênh phân phối: Website, PDF, Social, Sales email?

#### Template gợi ý
Cấu trúc FRM:
- **Header**: Client name/logo, industry, location
- **At a Glance**: Key metrics (3 callout boxes)
- **Challenge**: Bối cảnh, vấn đề, hậu quả nếu không giải quyết
- **Solution**: Approach, implementation, timeline
- **Results**: Metrics before/after, qualitative outcomes
- **Testimonial**: Quote từ KH + tên + chức danh
- **CTA**: "Muốn kết quả tương tự? Liên hệ..."

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Case Study Template.

CONTEXT:
- DN: [Tên] — Số case study target: [số]
- Industries ưu tiên: [liệt kê]
- Permission policy: [named / anonymous / logo only]
- Format: [long 1-2 trang / short 1/2 trang / cả hai]
- Distribution: [Website / PDF / Social / Email]

FORMAT:
- Template long-form: 1.5-2 trang — Header | At-a-Glance (3 metrics) | Challenge (150 words) | Solution (200 words) | Results (150 words + metrics table) | Testimonial | CTA
- Template short-form: 1/2 trang — Header | 1 paragraph challenge-solution-result | 3 metrics callout | Quote | CTA
- Interview guide: 10 câu hỏi để phỏng vấn KH — từ pain point đến kết quả
- Metrics framework: Bảng Metric Type | Before | After | % Change | Timeframe
- Permission form template: Tên KH | Scope cho phép | Kênh sử dụng | Thời hạn | Ký
- Social media snippets: 3 versions — LinkedIn (long) | Facebook (medium) | Twitter/X (short)

TONE: Story-driven, result-focused, credible.
LENGTH: 3-5 trang A4 (bao gồm cả template + guidelines).
```

---

### PROMPT 14: Pitch Deck Template

#### Mô tả
Template pitch deck — cấu trúc slide-by-slide cho trình bày về công ty, sản phẩm, hoặc đề xuất hợp tác. Bao gồm guidelines nội dung và copy cho từng slide: Problem, Solution, Market, Business Model, Traction, Team, Ask.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Mục đích pitch? (Investor, Partner, Client, Internal?)
2. Thời lượng trình bày? (5 / 10 / 15 / 20 phút?)
3. Audience: ai ngồi nghe? (VC, Angel, CEO đối tác, Ban giám đốc?)
4. Có traction data chưa? (revenue, users, growth rate?)
5. Ask là gì? (Investment, Partnership, Approval, Budget?)
6. Bao nhiêu slides target? (10 / 15 / 20?)

#### Template gợi ý
Cấu trúc FRM:
- **Slide 1**: Cover — Company name, tagline, presenter
- **Slide 2**: Problem — Pain point lớn, market context
- **Slide 3**: Solution — Giải pháp, demo/screenshot
- **Slide 4**: How It Works — 3-step process, user flow
- **Slide 5**: Market Opportunity — TAM/SAM/SOM, growth
- **Slide 6**: Business Model — Revenue streams, pricing
- **Slide 7**: Traction — Key metrics, milestones, growth chart
- **Slide 8**: Competition — Competitive landscape, positioning
- **Slide 9**: Team — Key members, expertise, advisors
- **Slide 10**: The Ask — What you need, what you offer, next steps

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Pitch Deck Template.

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Mục đích: [Investor / Partner / Client / Internal]
- Thời lượng: [phút] — Slides: [số]
- Audience: [mô tả]
- Traction: [revenue / users / growth rate]
- Ask: [Investment $ / Partnership / Approval]

FORMAT:
- Slide-by-slide guide: Slide # | Title | Content structure | Key message | Visual | Word count | Speaker notes
- Copy templates per slide: Headline formula + 3-5 bullet points + supporting data
- Design guidelines: Layout grid | Font sizes | Color usage | Chart style | Image guidelines
- Storytelling arc: Mermaid — Problem → Insight → Solution → Proof → Vision → Ask
- Data visualization: Bảng Data Type | Chart Type | Example — Revenue (bar) | Growth (line) | Market (pie)
- Presentation tips: Do/Don't × 10 — per slide type
- Version matrix: Investor deck vs Partner deck vs Client deck — slides khác nhau

TONE: Confident, compelling, data-backed.
LENGTH: 4-6 trang A4 (template + guidelines).
```

---

### PROMPT 15: Testimonial Collection (Quy trình & template thu thập testimonial)

#### Mô tả
Quy trình và template thu thập testimonial từ khách hàng — bao gồm timing tối ưu, câu hỏi chuẩn, format output, permission form, và hướng dẫn sử dụng testimonial trên các kênh marketing.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có bao nhiêu KH hiện tại? Bao nhiêu KH "happy" có thể xin testimonial?
2. Format ưu tiên? (Text / Video / Audio / Rating?)
3. Kênh sử dụng testimonial? (Website, Social, Brochure, Ads?)
4. Incentive cho KH khi cho testimonial? (Discount, Gift, Public recognition?)
5. Tần suất thu thập? (After project / Quarterly / Annual survey?)
6. Có template sẵn chưa?

#### Template gợi ý
Cấu trúc FRM:
- **Timing Matrix**: Khi nào nên xin testimonial — trigger events
- **Request Templates**: Email/Zalo templates cho từng tình huống
- **Interview Questions**: 5-7 câu hỏi khai thác — pain before, why chose us, results, would recommend
- **Format Guidelines**: Text (50-150 words), Video (30-90 seconds), Rating (1-5 + comment)
- **Permission Form**: Template xin phép sử dụng
- **Usage Guidelines**: Kênh nào dùng format nào, attribution rules

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Testimonial Collection (Quy trình thu thập testimonial).

CONTEXT:
- DN: [Tên] — Số KH: [số] — Happy KH estimate: [số]
- Format: [Text / Video / Audio / Rating]
- Kênh sử dụng: [Website / Social / Brochure / Ads]
- Incentive: [Discount / Gift / Recognition / None]
- Timing: [After project / Quarterly / Annual]

FORMAT:
- Timing matrix: Bảng Trigger Event | Timing | Method | Template # | Owner
- Request email templates: 3 versions — After delivery | After 3 months | Annual survey
- Zalo/SMS templates: 2 versions — Casual request | Formal request
- Interview questions: 7 câu — structured from pain → solution → result → recommendation
- Video testimonial guide: Script outline | Duration | Setting | Equipment | Questions on screen
- Permission form: Tên KH | Company | Scope (text/video/logo/name) | Channels | Duration | Signature
- Testimonial library template: Bảng KH | Industry | Quote | Rating | Date | Permission | Used on

TONE: Grateful, professional, easy-for-customer.
LENGTH: 4-5 trang A4.
```

---

### PROMPT 16: Marketing KPI Dashboard (Template dashboard marketing)

#### Mô tả
Template dashboard đo lường hiệu quả marketing — bao gồm traffic, leads, conversion, CAC (Customer Acquisition Cost), ROAS (Return on Ad Spend), engagement metrics chia theo kênh. Cung cấp cái nhìn tổng quan và chi tiết cho marketing team và BGĐ.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Kênh marketing cần track? (Website, Social, Email, Ads, SEO?)
2. KPIs quan trọng nhất? (Top 5-10?)
3. Reporting frequency? (Real-time / Daily / Weekly / Monthly?)
4. Tool dashboard? (Google Data Studio, Excel, custom, Ybai?)
5. Ai xem dashboard? (Marketing team / CMO / CEO / All?)
6. Có benchmark / target cho từng KPI chưa?

#### Template gợi ý
Cấu trúc FRM:
- **Executive Overview**: 5-7 KPIs chính — traffic, leads, conversion rate, CAC, revenue attributed, ROAS
- **Channel Performance**: Per channel — KPIs, trend, budget, ROI
- **Campaign Performance**: Active campaigns — spend, results, efficiency
- **Funnel Metrics**: TOFU → MOFU → BOFU — volume, conversion rate, velocity
- **Content Performance**: Top content, engagement trends
- **Target vs Actual**: Progress tracking by KPI

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Marketing KPI Dashboard Template.

CONTEXT:
- DN: [Tên] — Kênh: [liệt kê]
- Top KPIs: [5-10 KPIs]
- Frequency: [Real-time / Daily / Weekly / Monthly]
- Tool: [Google Data Studio / Excel / Custom / Ybai]
- Audience: [Marketing / CMO / CEO / All]
- Benchmarks: [Có/Không]

FORMAT:
- Executive scorecard: 7 KPI cards — Metric | Current | Target | Trend ↑↓→ | Status 🟢🟡🔴
- Channel dashboard: Bảng Channel | Traffic | Leads | Conv% | Spend | CPA | ROAS | Status
- Funnel visualization: TOFU [visitors] → MOFU [leads] → BOFU [opportunities] → Customers — conversion % between stages
- Campaign tracker: Bảng Campaign | Status | Budget | Spent | Leads | Conv | CPA | ROAS | Notes
- Content leaderboard: Top 10 content — Title | Channel | Views | Engagement | Leads | Conv
- Month-over-month: Bảng KPI × Tháng — 12 cột, trend line
- Alert rules: Bảng KPI | Green threshold | Yellow | Red | Action when Red

TONE: Data-driven, visual, executive-ready.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 17: SOP Đo lường ROI Marketing (Marketing ROI Measurement SOP)

#### Mô tả
Quy trình đo lường ROI marketing — từ thiết lập attribution model, cài đặt tracking, công thức tính toán, đến tần suất báo cáo và quy trình ra quyết định dựa trên data. Giúp DN biết chính xác mỗi đồng marketing chi ra mang lại bao nhiêu đồng doanh thu.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Attribution model hiện tại? (Last-click / First-click / Multi-touch / None?)
2. Tracking tools? (Google Analytics, Meta Pixel, UTM, CRM?)
3. Có thể track từ marketing đến doanh thu không? (full-funnel tracking?)
4. Reporting frequency? (Weekly / Bi-weekly / Monthly?)
5. Ai nhận report ROI? (CMO / CEO / Board?)
6. Ngưỡng ROI chấp nhận được? (VD: ROAS > 3x?)

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Attribution Model: Chọn model phù hợp, ưu/nhược điểm
- **Bước 2** — Tracking Setup: Pixels, UTMs, CRM integration, conversion events
- **Bước 3** — Data Collection: Nguồn data, frequency, automation
- **Bước 4** — Calculation: Công thức ROI, ROAS, CAC, LTV, Payback Period
- **Bước 5** — Analysis: So sánh channels, campaigns, time periods
- **Bước 6** — Reporting: Dashboard, report template, presentation
- **Bước 7** — Decision: Reallocation, scale up/down, kill campaign

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Đo lường ROI Marketing.

CONTEXT:
- DN: [Tên] — Attribution: [Last-click / Multi-touch / None]
- Tracking: [GA / Meta Pixel / UTM / CRM]
- Full-funnel tracking: [Có/Không]
- Reporting: [Weekly / Bi-weekly / Monthly]
- Report audience: [CMO / CEO / Board]
- ROI threshold: [ROAS > Xx]

FORMAT:
- Attribution model comparison: Bảng Model | Description | Best for | Pros | Cons
- Tracking checklist: Bảng Channel | Pixel/Tag | UTM convention | Conversion events | Status ☐
- UTM naming convention: Source | Medium | Campaign | Content | Term — ví dụ chuẩn
- ROI formulas: 5 công thức — ROI | ROAS | CAC | LTV | Payback — Definition | Formula | Example
- Channel ROI comparison: Bảng Channel | Investment | Revenue Attributed | ROI | ROAS | CAC | Rank
- Decision framework: Flowchart — ROAS > [X] → Scale | ROAS [Y-X] → Optimize | ROAS < [Y] → Kill/Pivot
- Report template: 1-page executive ROI report — Summary | By Channel | By Campaign | Recommendations

TONE: Analytical, ROI-obsessed, decision-enabling.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 18: Báo cáo Marketing tháng (Monthly Marketing Report)

#### Mô tả
Template báo cáo marketing hàng tháng — bao gồm executive summary, channel performance, campaign results, insights & learnings, và recommendations cho tháng tiếp theo. Giúp CMO/CEO nắm bắt hiệu quả marketing trong 5 phút đọc.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Ai đọc report? (CMO / CEO / Board / Marketing team?)
2. Kênh cần report? (tất cả hay focus channels?)
3. Có budget tracking trong report không?
4. Có so sánh MoM (month-over-month) và YoY không?
5. Deadline submit report? (ngày mấy hàng tháng?)

#### Template gợi ý
Cấu trúc FRM:
- **Executive Summary**: 3-5 bullets — highlights, lowlights, key number
- **KPI Overview**: Scorecard KPIs chính vs target
- **Channel Performance**: Per channel — traffic, leads, conversion, spend, ROI
- **Campaign Results**: Chiến dịch trong tháng — results vs goals
- **Content Performance**: Top content, engagement trends
- **Budget Status**: Planned vs Actual, variance
- **Insights & Learnings**: What worked, what didn't, why
- **Recommendations**: Actions cho tháng tiếp theo

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Báo cáo Marketing tháng (Monthly Marketing Report).

CONTEXT:
- DN: [Tên] — Report audience: [CMO / CEO / Board / Team]
- Kênh: [liệt kê channels]
- Budget tracking: [Có/Không]
- So sánh: [MoM / YoY / Both]
- Deadline: [ngày X hàng tháng]

FORMAT:
- Executive summary: 5 bullets max — 🟢 Wins | 🔴 Misses | 💡 Key insight | 📊 Key number | ➡️ Top action
- KPI scorecard: Bảng KPI | Target | Actual | % | MoM Δ | Status 🟢🟡🔴
- Channel performance: Bảng Channel | Traffic | Leads | Conv% | Spend | CPA | ROAS | MoM Δ | Notes
- Campaign deep-dive: Per campaign — Objective | Budget | Results | ROI | Learning
- Content top 10: Bảng Rank | Title | Channel | Reach | Engagement | Leads
- Budget tracker: Bảng Category | Budget | Spent | Remaining | % Used | Forecast
- Insights section: 3 "What Worked" + 3 "What Didn't" + "Why" for each
- Next month plan: Top 5 priorities | Budget allocation | Campaigns planned | Tests to run
- 3-5 trang max — designed for 5-minute executive read

TONE: Executive, insightful, action-oriented.
LENGTH: 3-5 trang A4.
```

---

## Ghi chú triển khai

### Dependencies
- `man-marketing-plan-nam.md` là file tổng quan — tham chiếu đến tất cả file khác trong folder, align với OKR từ 02-Strategy
- `man-content-strategy.md` cung cấp framework cho `frm-content-calendar.md` và `man-social-media-playbook.md`
- `rpt-customer-journey-map.md` cần input từ 08-Customer (feedback, NPS) và 06-Sales (sales cycle data)
- `man-marketing-budget.md` liên kết trực tiếp với 03-Finance (ngân sách tổng) và `sop-do-luong-roi.md` (đo lường hiệu quả chi tiêu)
- `frm-marketing-kpi-dashboard.md` và `frm-bao-cao-marketing-thang.md` cung cấp data cho 11-Reporting (Dashboard tổng)
- Các file `frm-` (Brochure, One-Pager, Pitch Deck, Case Study) cần brand guidelines từ 01-Governance

### Lưu ý
> **QUAN TRỌNG**: Marketing Plan năm phải được tạo đầu tiên vì nó set direction cho toàn bộ hoạt động marketing. Tất cả SOP, template, và dashboard đều phải align với mục tiêu và KPIs trong Marketing Plan.

> **Digital Marketing SOPs**: Các SOP Ads, SEO, Email Marketing thay đổi nhanh theo platform updates. Cần review và cập nhật ít nhất mỗi 6 tháng. AI cần hỏi version/platform hiện tại trước khi tạo SOP chi tiết.

> **Tài liệu bán hàng**: Brochure, One-Pager, Pitch Deck cần đảm bảo nhất quán về brand voice, visual, và messaging. Nên tạo sau khi có Brand Guidelines từ 01-Governance.

### Thứ tự tạo khuyến nghị
1. Marketing Plan năm (set direction tổng) → 2. Content Strategy (chiến lược nội dung)
3. Customer Journey Map (hiểu KH) → 4. Competitive Analysis (hiểu đối thủ) → 5. Marketing Budget (phân bổ ngân sách)
6. SOP chạy Ads → 7. SOP SEO → 8. SOP Email Marketing → 9. Social Media Playbook → 10. Content Calendar
11. Company Brochure → 12. Product One-Pager → 13. Case Study → 14. Pitch Deck → 15. Testimonial Collection
16. Marketing KPI Dashboard → 17. SOP Đo lường ROI → 18. Báo cáo Marketing tháng

---

### VIII.9 — BP Customer (Khách Hàng & Dịch Vụ)

> **Tầng 3: Tăng Trưởng** — 12 tài liệu: Trải nghiệm KH (4), Xử lý khiếu nại (3), Quản lý quan hệ KH (3), Cộng đồng & Referral (2).

---

### PROMPT 01: Customer Experience Standards (Tiêu chuẩn Trải nghiệm KH)

#### Mô tả
Tài liệu tổng quan định nghĩa tiêu chuẩn trải nghiệm KH của DN — service level standards, interaction guidelines, quality benchmarks, nguyên tắc CX. Đây là "hiến pháp" cho mọi tương tác với KH, đảm bảo nhất quán bất kể ai phục vụ (E-Myth: systems-dependent).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN hoạt động B2B hay B2C? Số lượng KH trung bình?
2. Các điểm chạm (touchpoints) chính với KH? (hotline, email, chat, gặp trực tiếp, app)
3. Thời gian phản hồi hiện tại? Mong muốn?
4. Có đo NPS/CSAT hiện tại không? Kết quả?
5. Điểm đau lớn nhất của KH khi tương tác với DN?
6. Có bao nhiêu nhân viên CS? Có CS Manager chuyên trách?

#### Template gợi ý
Cấu trúc MAN:
- **CX Vision & Principles**: 5-7 nguyên tắc cốt lõi (VD: "First Response < 2 giờ", "Giải quyết lần đầu > 80%")
- **Service Level Standards**: SLA cho từng kênh — thời gian phản hồi, giải quyết, escalation
- **Interaction Guidelines**: Giọng điệu, ngôn ngữ, do/don't khi giao tiếp với KH
- **Quality Benchmarks**: KPIs CX — NPS target, CSAT target, FCR, churn rate
- **Customer Journey Map**: Các giai đoạn + tiêu chuẩn tại mỗi điểm chạm
- **SERVQUAL Dimensions**: Tangibles, Reliability, Responsiveness, Assurance, Empathy — cách đo lường

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Customer Experience Standards (Tiêu chuẩn Trải nghiệm KH).

CONTEXT:
- DN: [Tên] — B2B/B2C: [loại] — Số KH: [số]
- Touchpoints: [hotline / email / chat / gặp mặt / app]
- Response time hiện tại: [giờ/phút] — Target: [giờ/phút]
- NPS hiện tại: [score / chưa đo] — CSAT: [% / chưa đo]
- CS team: [số người] — CS Manager: [Có/Không]
- Pain points KH: [mô tả]

FORMAT:
- CX Principles: 5-7 nguyên tắc — mỗi nguyên tắc có tiêu đề + mô tả 1-2 câu + metric
- SLA matrix: Kênh | Response time | Resolution time | Escalation trigger | Business hours
- Interaction playbook: Tình huống | Nên nói | Không nên nói | Ví dụ
- KPI dashboard: KPI | Target | Measurement | Frequency | Owner | Current
- Customer journey: Mermaid — Awareness → Purchase → Onboarding → Usage → Renewal → Advocacy
- SERVQUAL scorecard: 5 dimensions × 3-5 sub-criteria × rating scale

TONE: Customer-centric, inspirational nhưng actionable.
LENGTH: 8-12 trang A4.
```

---

### PROMPT 02: SOP Onboard Khách hàng (Customer Onboarding SOP)

#### Mô tả
Quy trình onboarding khách hàng mới — từ lúc ký hợp đồng/mua hàng đến khi KH đạt "first value" và ổn định sử dụng. Giai đoạn onboarding quyết định 90% khả năng giữ chân KH dài hạn.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ chính cần onboard? Độ phức tạp?
2. Thời gian onboarding trung bình? (1 ngày / 1 tuần / 1 tháng)
3. Handoff từ Sales sang CS diễn ra thế nào?
4. KH cần training không? Online hay offline?
5. "First value" — KH đạt giá trị đầu tiên khi nào? Dấu hiệu nào?
6. Tỷ lệ churn trong 90 ngày đầu?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Welcome: Email chào mừng, giới thiệu CS assigned, timeline onboarding
- **Bước 2** — Setup: Thiết lập tài khoản, cấu hình, cài đặt ban đầu
- **Bước 3** — Training: Hướng dẫn sử dụng, tài liệu, video
- **Bước 4** — First Value: Hỗ trợ KH đạt kết quả đầu tiên
- **Bước 5** — Check-in: Gọi/gặp check-in Day 7, Day 14, Day 30
- **Bước 6** — Stabilize: Chuyển sang chế độ chăm sóc thường xuyên

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Onboard Khách hàng (Customer Onboarding).

CONTEXT:
- DN: [Tên] — Sản phẩm/DV: [tên] — Độ phức tạp: [thấp/TB/cao]
- Thời gian onboard: [ngày/tuần/tháng]
- Handoff Sales → CS: [quy trình hiện tại]
- Training: [online / offline / self-serve] — Thời lượng: [giờ]
- First value milestone: [mô tả]
- Churn 90 ngày: [%]

FORMAT:
- Flowchart 6 bước: Mermaid — Welcome → Setup → Training → First Value → Check-in → Stabilize
- Timeline: Gantt-style — Day 0 → Day 7 → Day 14 → Day 30 → Day 60 → Day 90
- Welcome email template: Subject + body + CTA
- Handoff checklist: 10 items Sales phải transfer cho CS
- Check-in script: 3 scripts cho Day 7, 14, 30 — câu hỏi + action
- Success criteria: Milestone | Metric | Target | Check method
- Risk signals: 5-7 dấu hiệu KH sắp churn trong onboarding + action

TONE: Warm, supportive, proactive.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 03: SOP Chăm sóc sau bán (After-Sales Care SOP)

#### Mô tả
Quy trình chăm sóc KH sau khi mua hàng/ký hợp đồng — follow-up schedule, kiểm tra hài lòng, upsell/cross-sell, gia hạn, và re-engagement cho KH inactive. Khách hàng cũ tạo 65% doanh thu mới — chăm sóc sau bán là đầu tư sinh lời cao nhất.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Chu kỳ mua hàng trung bình? (1 lần / hàng tháng / hàng năm)
2. Có sản phẩm upsell/cross-sell không? Danh sách?
3. Hợp đồng có thời hạn? Quy trình gia hạn?
4. Sau bao lâu không mua hàng coi là KH inactive?
5. Hiện tại có follow-up sau bán không? Ai làm?

#### Template gợi ý
Cấu trúc SOP:
- **Follow-up schedule**: Day 3 (cảm ơn) → Day 7 (hài lòng?) → Day 30 (review?) → Day 60 (upsell) → Day 90 (referral)
- **Satisfaction check**: Script gọi/email kiểm tra, xử lý nếu không hài lòng
- **Upsell/Cross-sell**: Trigger events, script, offer
- **Renewal**: Timeline nhắc nhở, quy trình gia hạn, incentive
- **Re-engagement**: Phát hiện KH inactive, chuỗi email/gọi win-back
- **VIP treatment**: Chăm sóc đặc biệt cho KH tier A

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Chăm sóc sau bán (After-Sales Care).

CONTEXT:
- DN: [Tên] — Chu kỳ mua: [tần suất]
- Upsell/Cross-sell: [Có/Không] — SP: [liệt kê]
- HĐ có thời hạn: [Có/Không] — Thời hạn: [tháng/năm]
- Inactive threshold: [ngày]
- Follow-up hiện tại: [mô tả]

FORMAT:
- Follow-up calendar: Timeline — Day 3/7/30/60/90/180/365 | Action | Channel | Script | Owner
- Satisfaction check script: 3 phiên bản (gọi / email / chat) — câu hỏi + phản ứng theo kết quả
- Upsell playbook: Trigger | SP recommend | Script | Offer | Timing
- Renewal pipeline: Mermaid — 90 ngày trước HH → 60 → 30 → 7 → Hết hạn → Grace period
- Re-engagement sequence: 5 touchpoints — email 1 → email 2 → gọi → offer → final
- KPI tracking: Retention rate | Upsell rate | NPS | Churn rate | LTV

TONE: Relationship-focused, proactive, value-adding.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 04: Khảo sát NPS/CSAT (NPS & CSAT Survey Templates)

#### Mô tả
Template khảo sát đo lường sự hài lòng và trung thành KH — NPS (Net Promoter Score), CSAT (Customer Satisfaction Score), CES (Customer Effort Score). Kèm framework phân tích và lập kế hoạch hành động.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Đã từng đo NPS/CSAT chưa? Kết quả?
2. Kênh khảo sát ưu tiên? (email / in-app / SMS / gọi điện)
3. Tần suất khảo sát mong muốn? (sau mỗi giao dịch / hàng quý / hàng năm)
4. Số KH cần khảo sát? Tỷ lệ phản hồi mong đợi?
5. Ai sẽ phân tích kết quả và lập action plan?

#### Template gợi ý
Cấu trúc FRM:
- **NPS Survey**: 1 câu hỏi core (0-10) + 1 câu hỏi mở "Tại sao?" + phân loại Promoter/Passive/Detractor
- **CSAT Survey**: 3-5 câu hỏi theo dimension (sản phẩm, dịch vụ, tốc độ, nhân viên, overall)
- **CES Survey**: "Bạn dễ dàng giải quyết vấn đề đến mức nào?" (1-7)
- **Analysis Framework**: Công thức tính, benchmark ngành, trend analysis
- **Action Planning**: Score range → Action → Owner → Timeline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Template Khảo sát NPS/CSAT/CES.

CONTEXT:
- DN: [Tên] — B2B/B2C: [loại]
- Đã đo: [NPS=X / CSAT=X% / Chưa]
- Kênh: [email / in-app / SMS / gọi]
- Tần suất: [transactional / quarterly / annual]
- Số KH: [số] — Response rate target: [%]

FORMAT:
- NPS survey template: 1 câu core + 1 follow-up open + thank you page
- CSAT survey template: 5 câu rated (1-5) + 1 open + conditional logic
- CES survey template: 1 câu core (1-7) + 1 follow-up
- Scoring guide: NPS formula (% Promoter - % Detractor) | CSAT formula (satisfied/total) | CES formula
- Benchmark: Industry average NPS/CSAT + target setting
- Analysis template: Bảng Period | NPS | CSAT | CES | Trend | Top issues | Actions
- Action matrix: Score range | Urgency | Action | Owner | Timeline
- Closing the loop: Quy trình phản hồi KH sau khảo sát — Detractor (24h) | Passive (1 tuần) | Promoter (cảm ơn + referral)

TONE: Data-driven, actionable, customer-focused.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 05: SOP Xử lý khiếu nại (Complaint Management SOP)

#### Mô tả
Quy trình xử lý khiếu nại KH — từ tiếp nhận, phân loại mức độ nghiêm trọng, điều tra nguyên nhân, giải quyết, phản hồi KH, theo dõi, đến cải tiến quy trình. Theo ISO 9001 Clause 10.2 — mọi khiếu nại là cơ hội cải tiến.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Kênh tiếp nhận khiếu nại? (hotline, email, chat, social media, trực tiếp)
2. Trung bình bao nhiêu khiếu nại/tháng? Loại phổ biến nhất?
3. Thời gian giải quyết hiện tại? Target?
4. Ai có quyền quyết định bồi thường/hoàn tiền? Hạn mức?
5. Có hệ thống ticket/CRM tracking không?
6. Đã từng có khiếu nại leo thang nghiêm trọng chưa?

#### Template gợi ý
Cấu trúc SOP:
- **Bước 1** — Tiếp nhận: Ghi nhận, xác nhận với KH, tạo ticket
- **Bước 2** — Phân loại: Severity (Critical/High/Medium/Low), Category
- **Bước 3** — Điều tra: Thu thập thông tin, xác minh, root cause
- **Bước 4** — Giải quyết: Đề xuất giải pháp, duyệt, thực hiện
- **Bước 5** — Phản hồi: Thông báo KH kết quả, xin lỗi nếu cần
- **Bước 6** — Theo dõi: Follow-up sau 3-7 ngày, đảm bảo KH hài lòng
- **Bước 7** — Cải tiến: Root cause analysis, preventive action, cập nhật SOP

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Xử lý khiếu nại (Complaint Management).

CONTEXT:
- DN: [Tên] — Kênh tiếp nhận: [hotline / email / chat / social / trực tiếp]
- Khiếu nại/tháng: [số] — Loại phổ biến: [mô tả]
- Thời gian giải quyết hiện tại: [giờ/ngày] — Target: [giờ/ngày]
- Quyền bồi thường: [ai] — Hạn mức: [VNĐ]
- Ticket system: [tên / chưa có]

FORMAT:
- Flowchart 7 bước: Mermaid — Tiếp nhận → Phân loại → Điều tra → Giải quyết → Phản hồi → Theo dõi → Cải tiến
- Severity matrix: Level | Mô tả | Ví dụ | Response time | Resolution time | Escalate to
- Response scripts: 4 scripts theo severity — lời chào + xác nhận + cam kết thời gian
- Escalation path: Level 1 (Support Agent) → Level 2 (CS Team Lead) → Level 3 (CS Manager) → Level 4 (CEO)
- Root cause template: 5 Whys + Fishbone → Corrective action → Preventive action
- KPI tracking: Resolution time | FCR | Escalation rate | Repeat complaint rate | CSAT post-resolution
- Compensation matrix: Loại khiếu nại | Mức bồi thường | Approver | Điều kiện

TONE: Empathetic, solution-oriented, process-driven.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 06: Chính sách hoàn tiền/bảo hành (Refund & Warranty Policy)

#### Mô tả
Chính sách hoàn tiền và bảo hành — điều kiện, quy trình, thời hạn, trách nhiệm, ngoại lệ. Tài liệu vừa dùng nội bộ (CS team follow) vừa công bố cho KH (website, hợp đồng).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Sản phẩm/dịch vụ có bảo hành không? Thời hạn?
2. Điều kiện hoàn tiền hiện tại? (trong 7 ngày / 30 ngày / không hoàn)
3. Phương thức hoàn tiền? (tiền mặt / chuyển khoản / credit / đổi hàng)
4. Ai duyệt hoàn tiền? Hạn mức duyệt?
5. Có trường hợp ngoại lệ nào? (hàng sale, custom, digital...)
6. Luật bảo vệ người tiêu dùng áp dụng? (Luật BVQLNTD 2023)

#### Template gợi ý
Cấu trúc POL:
- **Chính sách hoàn tiền**: Điều kiện, thời hạn, quy trình, phương thức, timeline xử lý
- **Chính sách bảo hành**: Phạm vi, thời hạn, điều kiện mất bảo hành, quy trình claim
- **Đổi/trả hàng**: Điều kiện, thời hạn, chi phí vận chuyển
- **Ngoại lệ**: Các trường hợp không áp dụng
- **Trách nhiệm**: DN vs KH
- **Cơ sở pháp lý**: Tham chiếu luật BVQLNTD

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách hoàn tiền & bảo hành (Refund & Warranty Policy).

CONTEXT:
- DN: [Tên] — SP/DV: [liệt kê]
- Bảo hành: [thời hạn] — Phạm vi: [mô tả]
- Hoàn tiền: [điều kiện] — Thời hạn: [ngày]
- Phương thức hoàn: [tiền mặt / CK / credit / đổi hàng]
- Duyệt hoàn tiền: [ai] — Hạn mức: [VNĐ]
- Ngoại lệ: [liệt kê]

FORMAT:
- Refund policy: Bảng Điều kiện | Thời hạn | % hoàn | Phương thức | Timeline xử lý
- Warranty policy: Bảng SP | Thời hạn BH | Phạm vi | Điều kiện mất BH | Quy trình claim
- Refund process: Flowchart Mermaid — Yêu cầu → Kiểm tra điều kiện → Duyệt → Xử lý → Hoàn thành
- Warranty claim process: Flowchart — Báo lỗi → Kiểm tra BH → Sửa/Đổi → Giao lại
- Exception list: Trường hợp | Lý do không áp dụng | Giải pháp thay thế
- Customer-facing version: Bản rút gọn — ngôn ngữ thân thiện, có thể post lên website
- Internal version: Bản đầy đủ — bao gồm hạn mức duyệt, escalation

TONE: Rõ ràng, công bằng, bảo vệ cả KH và DN.
LENGTH: 4-6 trang A4.
```

---

### PROMPT 07: Log khiếu nại tracker (Complaint Log & Tracker)

#### Mô tả
Template tracking toàn bộ khiếu nại — ticket ID, severity, category, status, SLA compliance, resolution, root cause. Dùng để theo dõi realtime và phân tích trend hàng tháng/quý.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Phân loại khiếu nại theo category nào? (sản phẩm, giao hàng, dịch vụ, thanh toán, thái độ NV)
2. Bao nhiêu cấp severity? (3 hay 4 cấp)
3. SLA target theo severity?
4. Có cần tích hợp với CRM/helpdesk không?
5. Ai review log hàng tuần?

#### Template gợi ý
Cấu trúc FRM:
- **Complaint Log**: Ticket ID | Ngày | KH | Kênh | Category | Severity | Mô tả | Assigned to | Status | SLA deadline | Resolution | Root cause
- **Dashboard summary**: Tổng ticket | Open | In progress | Resolved | Overdue SLA | Avg resolution time
- **Trend analysis**: Monthly — Category breakdown, severity breakdown, SLA compliance rate
- **Root cause analysis**: Pareto chart — top 5 nguyên nhân, tần suất, corrective actions

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Log khiếu nại tracker (Complaint Log & Tracker).

CONTEXT:
- DN: [Tên] — Categories: [liệt kê]
- Severity levels: [3/4] — SLA: [chi tiết per level]
- CRM/Helpdesk: [tên / chưa có]
- Reviewer: [ai] — Tần suất review: [tuần/tháng]

FORMAT:
- Master log: Bảng 15+ cột — Ticket# | Date | Customer | Channel | Category | Severity | Description | Assigned | Status | SLA deadline | SLA met? | Resolution date | Resolution | Root cause | Follow-up
- Status definitions: New 🔵 | In Progress 🟡 | Escalated 🟠 | Resolved 🟢 | Closed ⚫ | Reopened 🔴
- SLA dashboard: Bảng Severity | SLA target | Avg actual | Compliance % | Trend
- Weekly summary: Template — Total | New | Resolved | Open | Overdue | Top category | Top root cause
- Monthly report: Category pie chart guide | Severity distribution | SLA trend | Action items
- Escalation alert: Trigger conditions — auto-escalate khi quá SLA hoặc severity = Critical

TONE: Tracking, analytical, data-driven.
LENGTH: 4-5 trang A4.
```

---

### PROMPT 08: SOP Phân loại khách hàng (Customer Tiering SOP)

#### Mô tả
Quy trình phân loại KH thành các tier A/B/C/D — dựa trên criteria (revenue, frequency, potential, engagement). Mỗi tier có chế độ chăm sóc khác nhau. Migration rules khi KH lên/xuống tier.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Hiện tại có phân loại KH chưa? Theo tiêu chí nào?
2. Doanh thu trung bình mỗi KH? Range min-max?
3. Tần suất mua hàng? Range?
4. Có muốn tính tiềm năng (potential) không, hay chỉ dựa trên lịch sử?
5. Bao nhiêu tier? (3: VIP/Standard/Basic hay 4: A/B/C/D)
6. Mỗi tier được chăm sóc khác nhau thế nào?

#### Template gợi ý
Cấu trúc SOP:
- **Tiêu chí phân loại**: Revenue (40%) + Frequency (25%) + Potential (20%) + Engagement (15%)
- **Tier definitions**: A (Top 10%) → B (Next 20%) → C (Next 40%) → D (Bottom 30%)
- **Benefits per tier**: Dedicated CSM, response priority, exclusive offers, events
- **Migration rules**: Đánh giá lại quarterly, điều kiện lên/xuống tier
- **Data sources**: CRM, billing, support tickets, engagement metrics

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Phân loại khách hàng (Customer Tiering).

CONTEXT:
- DN: [Tên] — Số KH: [số] — Revenue range: [min-max VNĐ/tháng]
- Phân loại hiện tại: [có/không] — Tiêu chí: [mô tả]
- Số tier: [3/4] — Tên tier: [VIP/Gold/Silver/Bronze hoặc A/B/C/D]
- Tần suất đánh giá: [quarterly / semi-annual]

FORMAT:
- Scoring model: Bảng Criteria | Weight | Scoring rule (1-10) | Data source
- Tier matrix: Tier | Score range | % KH | Revenue contribution | Mô tả | Color code
- Benefits matrix: Tier | Dedicated CSM | Response SLA | Discount | Events | Gifts | Review freq
- Migration rules: Điều kiện lên tier (2 quý liên tiếp ≥ threshold) | Xuống tier | Grace period
- Implementation: Bước 1 (data collection) → 2 (scoring) → 3 (assignment) → 4 (communication) → 5 (review)
- Dashboard: Tier distribution | Revenue by tier | Movement (up/down/stable) | At-risk customers

TONE: Strategic, data-driven, fair.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 09: Loyalty & Retention Program (Chương trình Trung thành & Giữ chân)

#### Mô tả
Thiết kế chương trình loyalty toàn diện — point system, tier benefits, retention tactics, churn prevention, win-back campaigns. Mục tiêu: tăng LTV (Lifetime Value), giảm churn rate, biến KH thành advocates.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có chương trình loyalty hiện tại không? Loại? (point / tier / paid / hybrid)
2. Churn rate hiện tại? Target?
3. LTV trung bình? Muốn tăng lên bao nhiêu?
4. Budget cho loyalty program? (% revenue)
5. Có CRM/loyalty platform không?
6. Đối thủ có chương trình loyalty gì?

#### Template gợi ý
Cấu trúc MAN:
- **Program Design**: Loại chương trình, mục tiêu, KPIs
- **Point System**: Earning rules (mua hàng, referral, review) + Redemption options (giảm giá, quà, upgrade)
- **Tier Benefits**: Bronze → Silver → Gold → Platinum — benefits tăng dần
- **Retention Tactics**: Birthday reward, anniversary, exclusive access, early launch
- **Churn Prevention**: Early warning signals, intervention playbook, save offers
- **Win-back Campaigns**: Segmentation inactive KH, chuỗi win-back, special offers, deadline

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Loyalty & Retention Program.

CONTEXT:
- DN: [Tên] — Loyalty hiện tại: [có/không] — Loại: [point/tier/paid]
- Churn rate: [%] — Target: [%]
- LTV hiện tại: [VNĐ] — Target: [VNĐ]
- Budget: [% revenue hoặc VNĐ/năm]
- Platform: [CRM/loyalty tool / chưa có]
- Đối thủ: [mô tả chương trình]

FORMAT:
- Program overview: 1-pager — Tên program | Mục tiêu | Loại | Target audience | Launch date
- Point system: Bảng Action | Points earned | Ví dụ | Cap/limit
- Redemption menu: Bảng Reward | Points needed | Value | Availability
- Tier benefits: Bảng Tier | Threshold | Benefits (8-10 items) | Upgrade path
- Churn prevention: Decision tree — Warning signal → Score check → Intervention → Result
- Win-back sequence: 5-step campaign — Email 1 (miss you) → 2 (feedback) → 3 (offer) → 4 (urgency) → 5 (final)
- ROI projection: Investment | Expected retention improvement | Revenue impact | Payback period
- KPIs: Enrollment rate | Active rate | Redemption rate | Churn rate | NPS | LTV growth

TONE: Strategic, creative, customer-centric.
LENGTH: 8-10 trang A4.
```

---

### PROMPT 10: Customer Health Score (Điểm sức khỏe KH)

#### Mô tả
Template đo lường "sức khỏe" quan hệ KH — scoring dimensions (usage, engagement, support, payment, NPS), trọng số, công thức tính, ngưỡng cảnh báo, và hành động theo từng mức score. Công cụ chủ động phát hiện KH có nguy cơ churn trước khi quá muộn.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Data nào đang có? (usage logs, login frequency, support tickets, payment history, NPS)
2. Đâu là dấu hiệu sớm nhất của KH sắp churn?
3. Có CRM/CS platform tracking được health score không?
4. Bao nhiêu KH cần monitor? Tần suất cập nhật score?
5. Ai sẽ action khi health score giảm?

#### Template gợi ý
Cấu trúc FRM:
- **Scoring Dimensions**: Usage (30%) | Engagement (20%) | Support (20%) | Payment (15%) | NPS/Feedback (15%)
- **Sub-metrics per dimension**: 3-5 metrics mỗi dimension, scoring 1-10
- **Calculation**: Weighted average → Score 0-100
- **Thresholds**: Green (≥70) — Healthy | Yellow (50-69) — At Risk | Red (<50) — Critical
- **Actions per range**: Green → nurture/upsell | Yellow → proactive outreach | Red → save team intervention

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Customer Health Score Template.

CONTEXT:
- DN: [Tên] — Data available: [usage / engagement / support / payment / NPS]
- Churn signals: [mô tả]
- Platform: [CRM / CS tool / manual]
- Số KH monitor: [số] — Update frequency: [daily / weekly / monthly]
- Action owner: [CS Manager / CSM / AI auto-alert]

FORMAT:
- Scoring model: Bảng Dimension | Weight | Sub-metrics | Scoring rule (1-10) | Data source | Update freq
- Calculation example: Walkthrough 1 KH cụ thể — input → weighted score → final score
- Threshold matrix: Score range | Status | Color | Description | Required action | Timeline | Owner
- Dashboard view: Customer | Score | Trend (↑↓→) | Status | Last contact | Next action | CSM
- Alert system: Auto-trigger khi score giảm ≥15 points/month hoặc xuống Red
- Cohort analysis: Score distribution per tier | Average score by segment | Trend over time
- Playbook per status: Green (3 actions) | Yellow (5 actions) | Red (7 actions) — scripts + offers

TONE: Analytical, proactive, early-warning focused.
LENGTH: 5-7 trang A4.
```

---

### PROMPT 11: Referral Program Design (Thiết kế Chương trình Giới thiệu)

#### Mô tả
Thiết kế chương trình referral — incentive structure (cho người giới thiệu và người được giới thiệu), mechanics, tracking, terms & conditions, promotional plan. Referral là kênh acquire KH mới chi phí thấp nhất, conversion rate cao nhất.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Có chương trình referral hiện tại không? Hiệu quả thế nào?
2. Incentive cho người giới thiệu? (tiền mặt / credit / quà / % hoa hồng)
3. Incentive cho người được giới thiệu? (giảm giá / quà / trial kéo dài)
4. Giá trị trung bình 1 KH mới? (để tính budget referral hợp lý)
5. Kênh promote referral program? (email / in-app / social / CS team)
6. Có affiliate/MGM system sẵn không? (VD: Ybai)

#### Template gợi ý
Cấu trúc MAN:
- **Program Design**: Tên, mục tiêu, double-sided incentive, budget
- **Mechanics**: Cách lấy referral link/code, share, track, validate, pay
- **Incentive Structure**: Người GT nhận gì, người được GT nhận gì, tier bonuses
- **Tracking System**: Referral link → Registration → Qualification → Reward
- **Terms & Conditions**: Eligibility, expiry, fraud prevention, caps
- **Promotional Plan**: Launch, ongoing promotion, seasonal boost

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Referral Program Design.

CONTEXT:
- DN: [Tên] — Referral hiện tại: [có/không] — Kết quả: [mô tả]
- Incentive referrer: [tiền / credit / quà / % HH]
- Incentive referee: [giảm giá / quà / trial]
- CAC trung bình: [VNĐ] — Target referral CAC: [VNĐ]
- Kênh promote: [email / in-app / social / CS]
- Affiliate system: [có/không] — Platform: [tên]

FORMAT:
- Program 1-pager: Tên | Tagline | How it works (3 steps) | Rewards | T&C summary
- Incentive matrix: Bảng Action | Referrer reward | Referee reward | Conditions | Cap
- Tier bonuses: 1-5 referrals → reward A | 6-15 → reward B | 16+ → reward C (gamification)
- Tracking flow: Mermaid — Share link → Click → Register → Qualify → Verify → Reward both
- Fraud prevention: 5-7 rules — self-referral, duplicate, abuse patterns, verification
- Promotional calendar: Month × Channel × Message × CTA
- KPIs: Referral rate | Conversion rate | CAC via referral | Viral coefficient | Revenue from referrals
- Email/message templates: 3 templates — invite, reminder, reward notification

TONE: Growth-focused, viral, win-win.
LENGTH: 6-8 trang A4.
```

---

### PROMPT 12: SOP Thu thập review (Review Collection SOP)

#### Mô tả
Quy trình thu thập review/testimonial từ KH — timing, kênh, templates, follow-up, moderation, usage rights, response protocol. Reviews là "social proof" mạnh nhất — 93% KH đọc review trước khi mua.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Kênh review quan trọng nhất? (Google, Facebook, website, Shopee, Tiki...)
2. Tỷ lệ KH để lại review hiện tại? Target?
3. Có incentive cho review không? (giảm giá, quà, point)
4. Ai quản lý review? Có quy trình trả lời review tiêu cực?
5. Review được sử dụng ở đâu? (website, ads, social, brochure)

#### Template gợi ý
Cấu trúc SOP:
- **Timing**: Khi nào xin review? (sau onboarding thành công, sau project hoàn thành, sau 30 ngày sử dụng)
- **Channels**: Google Business, Facebook Page, website, marketplace, video testimonial
- **Request Templates**: Email, SMS, in-app notification — 3 phiên bản
- **Follow-up**: Nhắc lại nếu chưa review — 1 lần sau 3 ngày
- **Moderation**: Review tiêu cực — respond within 24h, escalate nếu cần
- **Usage Rights**: Xin phép sử dụng, attribution, privacy
- **Response Protocol**: Positive → thank + share | Negative → acknowledge + resolve + follow-up

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo SOP Thu thập review (Review Collection).

CONTEXT:
- DN: [Tên] — Kênh review chính: [Google / FB / website / marketplace]
- Review rate hiện tại: [%] — Target: [%]
- Incentive: [có/không] — Loại: [giảm giá / quà / point]
- Review manager: [ai]
- Usage: [website / ads / social / brochure]

FORMAT:
- Timing matrix: Bảng Trigger event | Channel | Template | Owner | Auto/Manual
- Request templates: 3 versions — Email (subject + body) | SMS (160 chars) | In-app notification
- Follow-up sequence: Day 0 (request) → Day 3 (reminder) → Day 7 (final + incentive)
- Response playbook: Review type | Response template | Timeline | Escalation
  - 5-star → Thank + share | 4-star → Thank + note | 3-star → Thank + investigate
  - 2-star → Apologize + resolve + follow-up | 1-star → Urgent escalate + CS Manager respond
- Moderation guidelines: Fake review detection, removal request, legal considerations
- Usage rights: Permission template — email xin phép sử dụng testimonial
- KPI tracking: Review volume | Avg rating | Response rate | Response time | Review-to-referral conversion
- Video testimonial guide: Script gợi ý (5 câu hỏi) + technical requirements + release form

TONE: Proactive, appreciative, reputation-focused.
LENGTH: 5-7 trang A4.
```

---

## Ghi chú triển khai

### Dependencies
- `man-customer-experience-standards.md` là file tổng quan — tham chiếu đến tất cả file khác trong folder, đặc biệt SLA standards
- `sop-xu-ly-khieu-nai.md` phụ thuộc `pol-hoan-tien-bao-hanh.md` — cần chính sách hoàn tiền trước khi xây SOP xử lý
- `frm-log-khieu-nai.md` cần align với severity levels trong `sop-xu-ly-khieu-nai.md`
- `sop-phan-loai-kh.md` cung cấp tier data cho `man-loyalty-retention.md` và `frm-customer-health-score.md`
- `man-referral-program.md` có thể tích hợp với Ybai Marketing (MGM system) — check `Projects/Ybai/`
- `sop-onboard-khach-hang.md` cần handoff protocol từ 06-Sales (SOP bán hàng)
- `sop-cham-soc-sau-ban.md` cung cấp data cho 07-Marketing (testimonials, case studies) và 11-Reporting

### Lưu ý
> **QUAN TRỌNG**: Customer Experience là skill phụ thuộc NHIỀU vào mô hình kinh doanh. B2B (high-touch, ít KH, LTV cao) hoàn toàn khác B2C (low-touch, nhiều KH, LTV thấp) và SaaS (product-led, self-serve, usage-based). AI cần hỏi rõ mô hình trước khi tạo.

> **Tích hợp Ybai**: Nếu DN sử dụng Ybai Marketing, referral program nên tận dụng MGM (Member Get Member) system sẵn có — giảm đáng kể effort xây dựng tracking và payout.

> **NPS là leading indicator**: NPS dự báo churn trước 3-6 tháng. Detractor không xử lý trong 48h → xác suất churn tăng 4x. Setup alert system là ưu tiên.

### Thứ tự tạo khuyến nghị
1. Customer Experience Standards (định chuẩn CX cho mọi file khác)
2. SOP Onboard KH → 3. SOP Chăm sóc sau bán (customer journey flow)
4. Khảo sát NPS/CSAT (đo lường baseline)
5. SOP Xử lý khiếu nại → 6. Chính sách hoàn tiền/bảo hành → 7. Log khiếu nại tracker (complaint management cluster)
8. SOP Phân loại KH → 9. Customer Health Score (tiering + health)
10. Loyalty & Retention Program (dựa trên tiering)
11. Referral Program Design → 12. SOP Thu thập review (growth loop)

---

### VIII.10 — BP Product & Tech (Sản Phẩm & Công Nghệ)

> **Tầng 4: Tối Ưu** — 13 tài liệu: Sản phẩm & Dịch vụ (5), Công nghệ & Hạ tầng (5), Cải tiến liên tục (3).

---

### PROMPT 01: Product/Service Catalog (Danh mục Sản phẩm & Dịch vụ)
- **Mô tả:** Tài liệu master toàn bộ portfolio SP/DV — mô tả, đối tượng, pricing, lifecycle stage. Single source of truth.
- **Thu thập:** Danh sách SP/DV hiện tại, phân loại, doanh thu per SP, lifecycle stage, đối tượng KH từng SP.
- **Output:** MAN — Catalog table (SP × Mô tả × Đối tượng × Giá × Stage × Cross-ref), Mermaid lifecycle diagram.

### PROMPT 02: Product Roadmap (Lộ trình Phát triển Sản phẩm)
- **Mô tả:** Lộ trình phát triển SP theo quý/năm — milestones, tính năng mới, dependencies, resource allocation. Alignment tool.
- **Thu thập:** SP ưu tiên phát triển, tính năng planned, timeline, resource available, tech constraints.
- **Output:** MAN — Roadmap Gantt (Now/Next/Later), dependency map, resource matrix, quarterly milestones.

### PROMPT 03: SOP Phát triển Sản phẩm Mới (New Product Development)
- **Mô tả:** Quy trình chuẩn idea → research → prototype → test → launch → review. Gate/checkpoint, go/no-go criteria.
- **Thu thập:** Quy trình hiện tại, ai tham gia, timeline trung bình, tỉ lệ thành công, budget R&D.
- **Output:** SOP — Stage-Gate flowchart (Mermaid), RACI matrix, checklist per gate, timeline template.

### PROMPT 04: Product Brief Template (Mẫu Brief Sản phẩm)
- **Mô tả:** Template brief SP/tính năng mới: problem, solution, target, success metrics. Alignment giữa Product-Dev-Design-Marketing.
- **Thu thập:** Quy trình brief hiện tại, ai approve, thông tin thường thiếu, format mong muốn.
- **Output:** FRM — 1-page brief template (Problem, Solution, Target, Success Metrics, Scope, Timeline, Risks).

### PROMPT 05: SOP Kiểm soát Chất lượng (Quality Control)
- **Mô tả:** QC cho SP/DV — tiêu chuẩn, checklist, quy trình xử lý nonconformance, tracking. SP vật lý lẫn dịch vụ/phần mềm.
- **Thu thập:** Loại SP (vật lý/DV/phần mềm), tỉ lệ lỗi hiện tại, tiêu chuẩn ngành, đội QC, tools đang dùng.
- **Output:** SOP — QC checklist per SP type, nonconformance flowchart, defect tracking template, KPIs (defect rate, yield).

### PROMPT 06: Tech Stack Map (Bản đồ Công nghệ)
- **Mô tả:** Inventory toàn bộ công nghệ/phần mềm/hạ tầng IT — phân loại theo chức năng, license, chi phí, owner, tình trạng.
- **Thu thập:** Danh sách phần mềm, hosting, API, licenses, chi phí/tháng, owner, contract dates.
- **Output:** MAN — Tech stack matrix (Category × Tool × Purpose × License × Cost × Owner × Status), architecture diagram.

### PROMPT 07: Chính sách CNTT (IT Policy)
- **Mô tả:** Quy định sử dụng thiết bị, phần mềm, email, internet, BYOD, data classification. Nền tảng an ninh thông tin.
- **Thu thập:** Quy mô IT, thiết bị cấp hay BYOD, email provider, cloud hay on-premise, incident history.
- **Output:** POL — Acceptable Use Policy, BYOD rules, data classification matrix (Public/Internal/Confidential/Restricted).

### PROMPT 08: Chính sách An ninh Mạng (Cybersecurity Policy)
- **Mô tả:** Bảo mật thông tin — password, access control, encryption, incident response, compliance NĐ 13/2023.
- **Thu thập:** Incident history, hệ thống critical, data nhạy cảm, compliance requirements, budget security.
- **Output:** POL — Password policy, access control matrix, incident response flowchart, compliance checklist.

### PROMPT 09: SOP Backup Dữ liệu (Data Backup)
- **Mô tả:** Backup & recovery — lịch backup, phương pháp full/incremental, storage, test phục hồi, RPO/RTO per system.
- **Thu thập:** Hệ thống cần backup, data volume, RPO/RTO yêu cầu, backup hiện tại, budget storage.
- **Output:** SOP — Backup schedule matrix (System × Method × Frequency × Location × RPO × RTO), recovery test checklist.

### PROMPT 10: Danh sách Tài khoản Hệ thống (System Account Inventory)
- **Mô tả:** Inventory tài khoản SaaS/hệ thống — owner, quyền truy cập, review cycle. KHÔNG lưu mật khẩu. Phục vụ audit & offboarding.
- **Thu thập:** Danh sách SaaS, ai quản lý, tần suất access review, quy trình offboarding IT hiện tại.
- **Output:** MAN — Account inventory table (System × Owner × Users × Access Level × Review Date × Cost), offboarding checklist.

### PROMPT 11: Kaizen Board (Bảng Cải tiến Liên tục)
- **Mô tả:** Board quản lý ý tưởng cải tiến: đề xuất → đánh giá → ưu tiên → triển khai → đo lường. Văn hóa Kaizen.
- **Thu thập:** Cơ chế cải tiến hiện tại, số lượng đề xuất/tháng, ai đánh giá, có reward không.
- **Output:** MAN — Kaizen board template (Kanban: Idea → Evaluate → Prioritize → Implement → Measure), scoring criteria.

### PROMPT 12: Improvement Proposal Form (Mẫu Đề xuất Cải tiến)
- **Mô tả:** Form đơn giản cho mọi nhân viên đề xuất cải tiến — vấn đề, root cause, giải pháp, impact, resources.
- **Thu thập:** Level nhân viên sẽ dùng form, loại cải tiến phổ biến, quy trình phê duyệt, tracking tool.
- **Output:** FRM — 1-page form (Problem, Root Cause, Proposed Solution, Expected Impact, Resources, Priority Score).

### PROMPT 13: SOP Review & Cập nhật SOP (Meta-SOP)
- **Mô tả:** Meta-SOP quản lý, review, cập nhật toàn bộ SOP — version control, review cycle, approval flow. SOP luôn up-to-date.
- **Thu thập:** Số lượng SOP hiện tại, tần suất review, ai approve, version control method, issues gặp phải.
- **Output:** SOP — Review calendar, approval flowchart, version control template, SOP registry tracker.

### Thứ tự tạo khuyến nghị
1. Product/Service Catalog (nền tảng cho mọi file SP khác)
2. Product Roadmap → 3. SOP Phát triển SP mới → 4. Product Brief (product development cluster)
5. SOP QC (chất lượng SP)
6. Tech Stack Map (nền tảng cho mọi file IT khác)
7. Chính sách CNTT → 8. An ninh Mạng → 9. Backup → 10. Tài khoản Hệ thống (IT cluster)
11. Kaizen Board → 12. Improvement Proposal → 13. SOP Review SOP (cải tiến cluster)

---

### VIII.11 — BP Training (Đào Tạo & Phát Triển)

> **Tầng 4: Tối Ưu** — 10 tài liệu: Chính sách & Kế hoạch (3), Chương trình đào tạo (4), Hệ thống hỗ trợ (3).

---

### PROMPT 01: Training Policy (Chính sách Đào tạo)
- **Mô tả:** Chính sách đào tạo tổng thể — nguyên tắc, quyền & nghĩa vụ, ngân sách, cam kết phục vụ, cơ chế đánh giá. Nền tảng pháp lý nội bộ cho L&D.
- **Thu thập:** Ngân sách đào tạo/năm, số giờ đào tạo/người/năm, cam kết phục vụ hiện tại, ai approve đào tạo bên ngoài.
- **Output:** POL — Training principles, budget allocation formula, rights & obligations matrix, approval workflow, evaluation criteria.

### PROMPT 02: Training Needs Assessment (Khảo sát Nhu cầu Đào tạo)
- **Mô tả:** Mẫu khảo sát 3 cấp: tổ chức, phòng ban, cá nhân. Gap analysis năng lực hiện tại vs yêu cầu. Input chính cho Annual Plan.
- **Thu thập:** Competency framework (nếu có), performance review data, skill gaps đã biết, chiến lược DN năm tới.
- **Output:** FRM — TNA survey form (3 levels), gap analysis matrix (Competency × Current × Required × Gap × Priority).

### PROMPT 03: Annual Training Plan (Kế hoạch Đào tạo Hàng năm)
- **Mô tả:** Kế hoạch tổng thể từ TNA + chiến lược + compliance + ngân sách. Lịch 12 tháng, trainer, KPIs.
- **Thu thập:** Kết quả TNA, ngân sách, trainer nội bộ/ngoài, compliance training bắt buộc, facilities.
- **Output:** MAN — Training calendar 12 tháng, budget breakdown, trainer assignments, KPI targets (hours, completion, satisfaction).

### PROMPT 04: Onboarding Training Program (Đào tạo Hội nhập)
- **Mô tả:** Quy trình đào tạo nhân viên mới Day 1 → 90 ngày: orientation, văn hóa, sản phẩm, kỹ năng, buddy, checkpoint, pass probation.
- **Thu thập:** Time-to-productivity hiện tại, tỉ lệ nghỉ trong thử việc, nội dung onboarding hiện có, buddy system.
- **Output:** SOP — 90-day onboarding roadmap (Week 1/2/3/4, Month 2, Month 3), checklist per milestone, buddy guidelines.

### PROMPT 05: Leadership Development Program (Phát triển Lãnh đạo)
- **Mô tả:** Chương trình phát triển lãnh đạo các cấp — competency model, lộ trình, coaching, action learning, succession link.
- **Thu thập:** Cấp quản lý hiện tại, leadership gaps, succession needs, budget, thời gian commit được.
- **Output:** MAN — Leadership competency model per level, development roadmap, 70-20-10 activity mix, succession pipeline.

### PROMPT 06: Training Material Template (Mẫu Tài liệu Đào tạo)
- **Mô tả:** Template chuẩn cho bài giảng, slide, handout, facilitator guide. ADDIE model. Nhất quán và dễ bảo trì.
- **Thu thập:** Format đào tạo hiện tại (classroom/online/hybrid), tools dùng, brand guidelines, level học viên.
- **Output:** FRM — Slide template, facilitator guide template, handout template, lesson plan (ADDIE: Analyze-Design-Develop-Implement-Evaluate).

### PROMPT 07: Training Evaluation Form (Đánh giá Hiệu quả Đào tạo)
- **Mô tả:** Bộ form Kirkpatrick 4 cấp: Reaction, Learning, Behavior, Results. Mỗi cấp có form và timing riêng.
- **Thu thập:** Loại đào tạo phổ biến, cách đánh giá hiện tại, KPIs muốn cải thiện, ai review kết quả.
- **Output:** FRM — 4 form templates (L1: post-training survey, L2: knowledge test, L3: 30-60-90 behavior check, L4: business impact).

### PROMPT 08: Mentoring & Coaching Program (Mentoring & Coaching)
- **Mô tả:** Chương trình mentoring nội bộ — matching, session structure, goals, tracking, evaluation. Kênh "20%" trong 70-20-10.
- **Thu thập:** Pool mentor tiềm năng, mentee needs, thời gian commit, kỳ vọng outcomes, informal mentoring hiện tại.
- **Output:** SOP — Matching criteria matrix, session agenda template, development goal tracker, program evaluation form.

### PROMPT 09: Knowledge Management System Guide (Quản lý Tri thức)
- **Mô tả:** Hướng dẫn xây KMS — lưu trữ, tổ chức, chia sẻ tri thức tổ chức. Taxonomy, contribution guidelines, governance.
- **Thu thập:** Tools hiện tại (wiki, drive, Notion?), pain points tìm thông tin, ai tạo content nhiều nhất, knowledge loss incidents.
- **Output:** MAN — KMS architecture, taxonomy tree, contribution SOP, quality standards, governance roles (curator, reviewer, admin).

### PROMPT 10: Training ROI Report (Báo cáo ROI Đào tạo)
- **Mô tả:** Đo lường ROI đào tạo — chi phí, lợi ích tangible & intangible, Phillips Level 5. Chứng minh đào tạo là đầu tư.
- **Thu thập:** Chi phí đào tạo năm qua, metrics trước/sau đào tạo, business outcomes linked, CFO expectations.
- **Output:** RPT — ROI calculation template, cost-benefit matrix, intangible benefits framework, executive summary format.

### Thứ tự tạo khuyến nghị
1. Training Policy (nền tảng pháp lý cho mọi hoạt động đào tạo)
2. Training Needs Assessment → 3. Annual Training Plan (planning cluster)
4. Onboarding Training → 5. Leadership Development (program cluster)
6. Training Material Template (chuẩn hóa content)
7. Training Evaluation Form (Kirkpatrick — đo lường)
8. Mentoring & Coaching (supplementary L&D)
9. Knowledge Management Guide (tri thức tổ chức)
10. Training ROI Report (chứng minh giá trị — tạo sau cùng khi có data)

---

### VIII.12 — BP Reporting (Báo Cáo & Đo Lường)

> **Tầng 4: Tối Ưu** — 10 tài liệu: KPI & Scorecard (3), Dashboard (3), Báo cáo định kỳ (4).

---

### PROMPT 01: KPI Master — Balanced Scorecard (BSC)
- **Mô tả:** Master KPI toàn DN theo BSC 4 perspectives: Financial, Customer, Internal Process, Learning & Growth. Align với OKR chiến lược.
- **Thu thập:** Danh sách phòng ban, KPIs đang dùng, OKR hiện tại, industry benchmarks, data sources available.
- **Output:** MAN — BSC matrix (Perspective × Department × KPI × Target × Frequency × Owner × Data Source), strategy map.

### PROMPT 02: Scorecard Template (EOS-style Weekly)
- **Mô tả:** Scorecard 5-15 measurables cho L10 Meeting hàng tuần. On-track/off-track status. 1 trang, glance-able.
- **Thu thập:** Leadership team members, top priorities, leading indicators quan trọng, meeting cadence hiện tại.
- **Output:** FRM — 1-page scorecard (Measurable × Owner × Target × Actual × On/Off Track), 13-week trailing view.

### PROMPT 03: OKR Tracking Template (Theo dõi OKR)
- **Mô tả:** Template OKR từ company → department → individual. Progress tracking, confidence level, grading, review cadence.
- **Thu thập:** OKR framework đang dùng (nếu có), number of levels, grading scale, review frequency.
- **Output:** FRM — OKR cascade template (Company → Dept → Individual), progress tracker, confidence scoring (0.0-1.0), quarterly grading.

### PROMPT 04: CEO Dashboard (Bảng điều khiển CEO)
- **Mô tả:** Dashboard 1 trang cho CEO — top KPIs mọi phòng ban, traffic light, trend, alerts. Đọc 1 phút nắm toàn cảnh.
- **Thu thập:** Top 5-10 KPIs CEO quan tâm nhất, format preference (table/chart/both), frequency update, data accuracy current.
- **Output:** MAN — 1-page dashboard layout, KPI cards (metric × target × actual × trend × status), alert thresholds, update SOP.

### PROMPT 05: Department Dashboard Template (Dashboard Phòng ban)
- **Mô tả:** Template dashboard chuẩn per phòng ban — format thống nhất, KPIs khác nhau. CEO dễ đọc cross-department.
- **Thu thập:** Danh sách phòng ban, KPIs đặc thù mỗi phòng, tools báo cáo hiện tại, ai responsible cập nhật.
- **Output:** FRM — Standard dashboard template (Header × KPI Section × Trend × Actions × Notes), customization guide per dept.

### PROMPT 06: Số liệu Theo dõi Hàng tuần (Weekly Pulse Metrics)
- **Mô tả:** Pulse metrics cho weekly L10 — leading indicators, early warning signs, operational health. Khác KPI monthly.
- **Thu thập:** Meeting cadence, ai tham gia L10, leading indicators quan trọng, data available real-time.
- **Output:** MAN — Weekly metrics list per department, data collection SOP, threshold alerts, L10 review template.

### PROMPT 07: Báo cáo Tuần Template (Weekly Report)
- **Mô tả:** Template báo cáo tuần cho trưởng phòng — achievements, issues, KPI update, kế hoạch tuần tới. < 15 phút điền.
- **Thu thập:** Format hiện tại (nếu có), ai đọc, pain points khi làm báo cáo, deadline nộp.
- **Output:** FRM — 1-page weekly template (Wins × Issues × KPIs × Next Week × Help Needed), filing guide.

### PROMPT 08: Báo cáo Tháng Template (Monthly Report)
- **Mô tả:** Báo cáo tháng toàn diện — KPI vs target, variance analysis, highlights/lowlights, kế hoạch tháng tới. CEO đọc 10 phút.
- **Thu thập:** Sections cần cover, KPIs per department, variance threshold cần giải trình, ai present.
- **Output:** FRM — Monthly report template (Executive Summary × KPI Dashboard × Variance Analysis × Action Items × Next Month).

### PROMPT 09: Báo cáo Quý Template (Quarterly Report)
- **Mô tả:** Strategic review toàn diện — OKR grading, financial performance, market analysis, kế hoạch quý tới. Board/investor-ready.
- **Thu thập:** Board members/investors, strategic priorities, OKR current, financial YTD, market changes.
- **Output:** FRM — Quarterly template (OKR Scorecard × Financial Summary × Market Update × Strategic Initiatives × Next Quarter Plan).

### PROMPT 10: SOP Quarterly Business Review — QBR
- **Mô tả:** Quy trình tổ chức QBR — preparation, agenda, facilitation, follow-up. Ritual quan trọng nhất cho leadership alignment.
- **Thu thập:** QBR hiện tại (có/không), participants, duration, outcomes mong muốn, follow-up tracking.
- **Output:** SOP — QBR process flowchart, preparation checklist, agenda template (3-4 giờ), follow-up tracker, RACI.

### Thứ tự tạo khuyến nghị
1. KPI Master BSC (nền tảng metrics cho mọi file khác)
2. Scorecard EOS → 3. OKR Tracking (measurement framework cluster)
4. CEO Dashboard → 5. Department Dashboard → 6. Weekly Pulse (dashboard cluster)
7. Báo cáo Tuần → 8. Báo cáo Tháng → 9. Báo cáo Quý (reporting cadence)
10. SOP QBR (ritual tổng hợp — tạo sau cùng)

---

### VIII.13 — BP Growth (Tăng Trưởng & Đầu Tư)

> **Tầng 5: Nhân Rộng** — 12 tài liệu: Gọi vốn (5), Nhượng quyền & Mở rộng (4), Exit & Kế thừa (3).

---

### PROMPT 01: Pitch Deck (Slide Deck Gọi vốn)
- **Mô tả:** 12-15 slides story-driven, data-backed theo chuẩn VC: Problem → Solution → Market → Traction → Team → Ask.
- **Thu thập:** Problem statement, solution, market size (TAM/SAM/SOM), traction metrics, team bios, funding ask.
- **Output:** MAN — Slide-by-slide content brief, data visualization specs, speaker notes, appendix slides.

### PROMPT 02: Financial Model & Valuation (Mô hình Tài chính & Định giá)
- **Mô tả:** Mô hình tài chính 3-5 năm + định giá DN: revenue model, P&L, cashflow, DCF, comparable companies.
- **Thu thập:** Revenue model hiện tại, historical financials 2-3 năm, growth assumptions, comparable companies, cost structure.
- **Output:** RPT — Revenue model, P&L projection, cashflow projection, DCF valuation, comparable analysis, sensitivity table.

### PROMPT 03: Investment Memo (Bản ghi nhớ Đầu tư)
- **Mô tả:** Tài liệu 8-15 trang cho investor — deeper than pitch deck. Thesis, market, competitive, financials, risks, terms.
- **Thu thập:** Investment thesis, detailed market data, competitive landscape, financial model, key risks, proposed terms.
- **Output:** MAN — Structured memo (Thesis × Market × Product × Traction × Financials × Risks × Terms), executive summary 1-page.

### PROMPT 04: Cap Table (Bảng Cơ cấu Sở hữu)
- **Mô tả:** Tracking cổ phần: ai sở hữu bao nhiêu %, loại cổ phần, vesting, dilution qua các vòng. Yêu cầu bắt buộc từ investor.
- **Thu thập:** Danh sách cổ đông hiện tại, % sở hữu, loại cổ phần, ESOP pool, vesting schedules, vòng gọi vốn dự kiến.
- **Output:** RPT — Cap table (Shareholder × Shares × % × Type × Vesting), dilution waterfall per round, ESOP allocation.

### PROMPT 05: Term Sheet Template (Mẫu Điều khoản Đầu tư)
- **Mô tả:** Non-binding terms & conditions trước hợp đồng chính thức: valuation, amount, instrument, rights, governance.
- **Thu thập:** Valuation expectation, funding amount, instrument preference (equity/convertible/SAFE), governance requirements.
- **Output:** FRM — Term sheet template (Economic Terms × Control Terms × Investor Rights × Protective Provisions × Conditions).

### PROMPT 06: Franchise Model Blueprint (Thiết kế Mô hình Nhượng quyền)
- **Mô tả:** Blueprint nhượng quyền: unit economics, territory design, fee structure, support model, franchise lifecycle.
- **Thu thập:** Mô hình kinh doanh hiện tại, unit economics per location, territory strategy, support capabilities, brand standards.
- **Output:** MAN — Unit economics model, territory map, fee structure (initial + royalty + marketing), support package, franchise lifecycle.

### PROMPT 07: Franchise Operations Manual (Sổ tay Vận hành Nhượng quyền)
- **Mô tả:** "Bible" cho franchisee: setup, daily ops, staffing, local marketing, financial reporting. Clone SOP Tầng 1-4 cho franchise.
- **Thu thập:** SOP package hiện tại (Tầng 1-4), franchise-specific customizations, brand standards, reporting requirements.
- **Output:** MAN — Comprehensive ops manual (Setup → Daily Ops → Staffing → Marketing → Finance → Compliance), training curriculum.

### PROMPT 08: Market Expansion Analysis (Phân tích Mở rộng Thị trường)
- **Mô tả:** Phân tích cơ hội mở rộng: market attractiveness, entry strategy, localization, competitive landscape, financial projections.
- **Thu thập:** Target markets, entry strategy options, localization requirements, competitive intel, investment budget.
- **Output:** RPT — Market scoring matrix, entry strategy comparison, localization checklist, 3-year projections per market.

### PROMPT 09: Franchise Agreement Template (Hợp đồng Nhượng quyền)
- **Mô tả:** Hợp đồng nhượng quyền theo luật VN (NĐ 35/2006, Luật Thương mại 2005). Quyền & nghĩa vụ Franchisor-Franchisee.
- **Thu thập:** Điều khoản thương mại, territory exclusivity, term length, termination conditions, IP protection needs.
- **Output:** FRM — Contract template (Definitions × Grant × Fees × Obligations × IP × Term × Termination × Dispute), legal checklist.

### PROMPT 10: Exit Strategy Options (Các Lựa chọn Thoát vốn)
- **Mô tả:** Phân tích exit options: IPO, M&A, MBO, succession, liquidation. Feasibility, timeline, valuation impact, readiness.
- **Thu thập:** Founder goals, timeline preference, current valuation, shareholder alignment, market conditions.
- **Output:** MAN — Exit option comparison matrix (Option × Feasibility × Timeline × Valuation × Readiness), decision framework.

### PROMPT 11: Succession Plan (Kế hoạch Kế nhiệm)
- **Mô tả:** Kế nhiệm vị trí then chốt — đặc biệt CEO/Founder. Successors, development gaps, transition timeline, governance changes.
- **Thu thập:** Key positions, successor candidates, readiness assessment, development needs, transition timeline, governance structure.
- **Output:** MAN — Succession matrix (Position × Successor × Readiness × Gap × Development Plan), transition roadmap, governance changes.

### PROMPT 12: Business Valuation Report (Báo cáo Định giá DN)
- **Mô tả:** Định giá DN toàn diện 3+ phương pháp, premium/discount analysis, valuation range. Cho gọi vốn, M&A, exit, ESOP.
- **Thu thập:** Financial statements 3 năm, comparable companies, industry multiples, tangible/intangible assets, growth projections.
- **Output:** RPT — 3-method valuation (DCF × Comparable × Asset-based), premium/discount adjustments, valuation range, executive summary.

### Thứ tự tạo khuyến nghị
1. Financial Model & Valuation (nền tảng số liệu cho mọi file khác)
2. Pitch Deck → 3. Investment Memo → 4. Cap Table → 5. Term Sheet (fundraising cluster)
6. Franchise Blueprint → 7. Franchise Ops Manual → 8. Market Expansion → 9. Franchise Agreement (franchise cluster)
10. Exit Strategy → 11. Succession Plan → 12. Business Valuation (exit cluster)

---

## IX. NGUỒN THAM KHẢO

| Nguồn | Tác giả / Tổ chức | Ứng dụng trong hệ thống |
|-------|-------------------|------------------------|
| **ISO 9001:2015** | ISO | Hệ thống tài liệu 4 tầng (Policy → Manual → Procedure → Record), Process Approach |
| **EOS / Traction** | Gino Wickman | 6 thành phần: Vision, People, Data, Issues, Process, Traction — framework build order |
| **E-Myth Revisited** | Michael Gerber | Turnkey franchise model, "Work ON not IN your business" — franchise-ready mindset |
| **McKinsey 7S Framework** | McKinsey & Company | Alignment 7 yếu tố: Strategy, Structure, Systems, Skills, Staff, Style, Shared Values |
| **SYSTEMology** | David Jenyns | 100+ SOP templates theo chức năng, phương pháp hệ thống hóa |
| **Franchise Operations Manual Standards** | IFA (International Franchise Association) | Chuẩn tài liệu vận hành nhượng quyền |
| **Business-in-a-Box** | Biztree | 2,600+ business document templates — reference for document types |
| **ISO 31000:2018** | ISO | Framework quản lý rủi ro — áp dụng cho Risk Management Policy & Risk Register |
| **Luật Doanh nghiệp 2020** | Quốc hội VN (59/2020/QH14) | Cơ sở pháp lý cho Governance — điều lệ, ĐKKD, quy chế quản trị |
| **Bộ luật Lao động 2019** | Quốc hội VN (45/2019/QH14) | Cơ sở pháp lý cho hợp đồng lao động |
| **Nghị định 13/2023/NĐ-CP** | Chính phủ VN | Bảo vệ dữ liệu cá nhân — Data Protection Policy |
| **Blue Ocean Strategy** | W. Chan Kim & Renée Mauborgne | Chiến lược tạo không gian thị trường mới |
| **Business Model Generation** | Alexander Osterwalder | Business Model Canvas — 9 khối mô hình kinh doanh |
| **Measure What Matters** | John Doerr | OKR framework — Objectives & Key Results |

---

> **Document Control:**
> - Version: 2.1
> - Created: 2026-04-23
> - Last Updated: 2026-04-30
> - Author: MODORO × Claude
> - Status: ALL PHASES COMPLETE (13/13 skills) ✅
> - Completed: VIII.1 Orchestrator (8), VIII.2 Governance (19), VIII.3 Strategy (18), VIII.4 Finance (20), VIII.5 People (27), VIII.6 Operations (20), VIII.7 Sales (17), VIII.8 Marketing (18), VIII.9 Customer (12), VIII.10 Product & Tech (13), VIII.11 Training (10), VIII.12 Reporting (10), VIII.13 Growth (12)
> - Total prompts indexed: 159 (Phase 1: 37 + Phase 2: 67 + Phase 3: 47 + Phase 4: 45 — condensed format)
> - Total documents in system: 204
