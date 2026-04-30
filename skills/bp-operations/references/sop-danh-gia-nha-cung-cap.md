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
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
