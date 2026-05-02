### PROMPT 24: Competency Framework (Khung năng lực)

#### Mô tả
Khung năng lực toàn DN — định nghĩa các năng lực cốt lõi (Core), năng lực lãnh đạo (Leadership), năng lực chuyên môn (Functional/Technical) cho mỗi vị trí. Là nền tảng cho tuyển dụng, đánh giá hiệu suất, kế hoạch phát triển, và lương thưởng. Mỗi năng lực được mô tả theo 4-5 cấp độ (Level 1: Awareness → Level 5: Expert/Master).

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Quy mô DN: bao nhiêu vị trí công việc cần có khung năng lực?
2. Đã có giá trị cốt lõi (Core values) chưa? List ra
3. Mô hình tổ chức: phòng ban nào, function nào chính?
4. Cấp bậc tổ chức: bao nhiêu level (Junior → Senior → Lead → Manager → Director)?
5. Có muốn tích hợp với JD và đánh giá hiệu suất không?
6. Tham chiếu chuẩn nào: Lominger / SHL / ESCO / tự xây?
7. Ai duyệt khung: HR Director / CEO / cả hai?

#### Template gợi ý
Cấu trúc FRM:
- **Mục đích**: Tại sao cần competency framework + use case
- **Cấu trúc khung 3 lớp**: Core (cho tất cả) + Leadership (cho manager+) + Functional (cho từng phòng ban)
- **Định nghĩa Cấp độ**: Level 1 (Awareness) → 2 (Basic) → 3 (Proficient) → 4 (Advanced) → 5 (Expert)
- **Core Competencies**: 5-7 năng lực bắt buộc với mọi nhân viên (Customer focus, Communication, Teamwork, Integrity, Learning agility...)
- **Leadership Competencies**: 5-7 năng lực cho cấp manager+ (Vision, People development, Decision making, Strategic thinking, Change management...)
- **Functional Competencies**: Theo phòng ban (Sales, Marketing, Tech, Finance, HR, Ops) — mỗi phòng 5-10 năng lực
- **Behavioral Indicators**: Mỗi năng lực × cấp độ có 3-5 hành vi quan sát được
- **Mapping với Vị trí**: Bảng Position × Required Competencies × Required Level
- **Sử dụng Khung**: Cho Recruitment / Performance Review / Development Plan / Succession
- **Quy trình cập nhật**: Review định kỳ 2 năm/lần

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Competency Framework (Khung năng lực).

CONTEXT:
- DN: [Tên] — Ngành: [ngành]
- Số vị trí công việc: [n positions]
- Số phòng ban / function: [list]
- Cấp bậc: [Junior / Mid / Senior / Lead / Manager / Director / VP / C-level]
- Core values: [list]
- Tham chiếu: [Lominger / SHL / ESCO / tự xây]

FORMAT:
- Sơ đồ kiến trúc 3 lớp Core/Leadership/Functional
- Cấp độ chuẩn: Bảng Level 1-5 với định nghĩa chung
- Core competencies: 5-7 năng lực — mỗi năng lực 1 trang
  • Tên + Định nghĩa
  • Bảng Level 1-5 × Behavioral Indicator (3-5 hành vi/level)
- Leadership competencies: 5-7 năng lực, format tương tự
- Functional competencies: Mỗi phòng ban 1 section, 5-10 năng lực
- Position mapping: Bảng Position | Core Lv | Leadership Lv | Functional Lv (cho 10-15 vị trí key)
- Use case map: Recruitment | Performance | Development | Succession — cách dùng khung
- Update cycle: Quy trình review 2 năm/lần

TONE: Hệ thống, có cấu trúc, dễ áp dụng.
LENGTH: 25-30 trang A4 hoặc Excel với multiple sheets (preferred).
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
