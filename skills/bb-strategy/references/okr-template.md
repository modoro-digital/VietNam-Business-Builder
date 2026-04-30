# PROMPT 12: OKR Template (Objectives & Key Results)

#### Mô tả
Hệ thống OKR theo quý — cascade từ Company → Department → Individual. Mỗi Objective có 3-5 Key Results đo lường được. Kèm scoring guide và review template.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. OKR cho cấp nào? (Company / Department / Individual / tất cả)
2. Quý nào? (Q1/Q2/Q3/Q4 năm nào)
3. Company-level objectives? (liệt kê 3-5)
4. Phòng ban nào cần OKR? (liệt kê)
5. Đã từng dùng OKR chưa? (cần training materials kèm theo?)
6. Scoring system: 0-1.0 (Google style) / % / RAG?

#### Template gợi ý
Cấu trúc FRM:
- **OKR Primer** — 1 trang hướng dẫn nhanh: OKR là gì, rules, common mistakes
- **Company OKRs** — 3-5 Objectives, mỗi O có 3-5 KRs
- **Department OKRs** — Per dept, aligned lên Company OKRs
- **Individual OKRs** — Template trống cho cá nhân
- **Scoring Guide** — 0.0-0.3 (Red), 0.4-0.6 (Yellow), 0.7-1.0 (Green)
- **Weekly Check-in Template** — KR | Target | Current | Confidence (🟢🟡🔴) | Blockers
- **Quarterly Review Template** — Score + Learnings + Next Quarter Adjustments
- **OKR Calendar** — Timeline: Set (tuần 1) → Check-in (weekly) → Score (tuần 12) → Reflect (tuần 13)

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
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
LENGTH: 5-8 trang A4 (bao gồm templates).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
