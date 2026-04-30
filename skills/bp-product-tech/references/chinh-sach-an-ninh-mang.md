### PROMPT 08: Chính sách An ninh Mạng (Cybersecurity Policy)

#### Mô tả
Chính sách bảo mật thông tin và an ninh mạng — quy định về password, access control, encryption, incident response, và compliance. Bảo vệ DN khỏi rủi ro mất dữ liệu, tấn công mạng, và vi phạm pháp luật về dữ liệu cá nhân.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN lưu trữ dữ liệu khách hàng? Loại gì? (PII, payment, health...)
2. Có MFA (xác thực 2 lớp) chưa? Cho hệ thống nào?
3. Đã từng bị tấn công/data breach chưa?
4. Có nhân sự IT security chuyên trách không?
5. Compliance requirements? (PDPA VN / GDPR / PCI-DSS / ISO 27001)
6. Có sử dụng cloud services không? (AWS / GCP / Azure)

#### Template gợi ý
Cấu trúc POL:
- **Phần 1** — Mục đích, Phạm vi, Thuật ngữ, Tham chiếu (ISO 27001, NĐ 13/2023)
- **Phần 2** — Password Policy: Độ phức tạp, thay đổi, quản lý password manager
- **Phần 3** — Access Control: Least privilege, role-based access, review cycle
- **Phần 4** — Data Protection: Encryption at rest/in transit, data retention, deletion
- **Phần 5** — Network Security: Firewall, VPN, Wi-Fi, segmentation
- **Phần 6** — Endpoint Security: Antivirus, patching, device encryption
- **Phần 7** — Incident Response Plan: Detection → Containment → Eradication → Recovery → Lessons learned
- **Phần 8** — Awareness & Training: Phishing test, security training frequency
- **Phần 9** — Compliance: Luật An ninh mạng VN 2018, NĐ 13/2023 về bảo vệ DLCN
- **Phụ lục**: Incident response checklist, Security awareness quiz, Vendor security assessment

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Chính sách An ninh Mạng (Cybersecurity Policy).

CONTEXT:
- DN: [Tên] — Dữ liệu KH: [loại] — Cloud: [provider]
- MFA: [Có/Không] — Hệ thống: [liệt kê]
- IT Security: [chuyên trách / kiêm nhiệm / outsource]
- Compliance: [PDPA VN / GDPR / PCI-DSS / ISO 27001]
- Incident history: [Có/Không]

FORMAT:
- Password matrix: System | Min length | Complexity | Rotation | MFA
- Access control matrix: Role | System A | System B | System C → CRUD permissions
- Incident response flowchart: Mermaid — 5 phases + timeline
- Data classification × Handling: Matrix 4 levels × encryption/storage/sharing/disposal
- Security checklist: Monthly ☐ + Quarterly ☐ + Annual ☐ review items
- Compliance mapping: Requirement | Luật/Tiêu chuẩn | Current status | Gap | Action
- Training calendar: Topic | Audience | Frequency | Format | Owner

TONE: Chuyên nghiệp, bảo mật, reference cụ thể luật VN + tiêu chuẩn quốc tế.
LENGTH: 8-12 trang A4.

CROSS-REFERENCE: Đây là chính sách an ninh mạng kỹ thuật. Chính sách bảo vệ dữ liệu pháp lý xem bp-governance/Chính sách bảo vệ dữ liệu. Quy chế bảo mật nhân sự xem bp-people/Quy chế bảo mật thông tin.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
