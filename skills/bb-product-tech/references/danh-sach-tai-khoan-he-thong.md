### PROMPT 10: Danh sách Tài khoản Hệ thống (System Account Inventory)

#### Mô tả
Inventory toàn bộ tài khoản hệ thống, phần mềm, SaaS mà DN đang sử dụng — bao gồm owner, quyền truy cập, review cycle. **KHÔNG LƯU MẬT KHẨU** — chỉ tracking ai có quyền gì, ở đâu. Phục vụ audit, offboarding, và access review.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Bao nhiêu hệ thống/SaaS đang dùng?
2. Có quản lý tập trung (SSO/IAM) không?
3. Quy trình cấp/thu hồi quyền khi onboard/offboard?
4. Tần suất review access? (hàng tháng / quý / khi có thay đổi)
5. Có shared accounts / service accounts không?
6. Password manager đang dùng? (1Password, Bitwarden, LastPass...)

#### Template gợi ý
Cấu trúc MAN:
- **Phần 1** — Tổng quan: Số lượng systems, tổng users, SSO coverage
- **Phần 2** — Account Inventory: Bảng master — System | URL | Owner | Admin | Users | Auth method | SSO | MFA | Review date
- **Phần 3** — Access Matrix: User × System → Role/Permission level
- **Phần 4** — Service Accounts: Accounts không thuộc cá nhân — purpose, owner, rotation schedule
- **Phần 5** — Onboarding Checklist: Hệ thống cần cấp quyền per role
- **Phần 6** — Offboarding Checklist: Hệ thống cần thu hồi quyền
- **Phần 7** — Access Review Process: Tần suất, quy trình, sign-off
- **Phụ lục**: Access request form, Access review report template

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Danh sách Tài khoản Hệ thống (System Account Inventory).

CONTEXT:
- DN: [Tên] — Số hệ thống: [số] — Nhân sự: [số]
- SSO: [Có/Không] — Provider: [tên]
- Password Manager: [tên]
- Access review: [tần suất]

FORMAT:
- Summary dashboard: Total systems | SSO-enabled | MFA-enabled | Shared accounts | Last full review
- Master inventory: System | URL | Category | Owner | # Users | Auth | SSO ☐ | MFA ☐ | License type | Cost | Renewal
- Access matrix: Bảng User × System → Role (Admin/Editor/Viewer/None)
- Service accounts: Account | System | Purpose | Owner | Rotation | Last rotated
- Onboarding per role: Role | Systems to provision | Access level | Provisioned by
- Offboarding checklist: System | Action | Verified by | Date ☐
- Review log: System | Review date | Reviewer | Changes made | Next review

⚠️ SECURITY: KHÔNG bao gồm passwords, API keys, hoặc secrets trong file này.

TONE: Inventory, compliance-ready, structured.
LENGTH: 4-6 trang A4.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
