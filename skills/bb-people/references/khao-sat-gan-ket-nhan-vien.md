### PROMPT 27: Employee Engagement Survey (Khảo sát gắn kết nhân viên)

#### Mô tả
Bộ khảo sát gắn kết nhân viên định kỳ (annual + pulse survey) — đo lường mức độ engagement, satisfaction, eNPS (Employee Net Promoter Score), và identify drivers của attrition. Bao gồm câu hỏi chuẩn (Gallup Q12, Engagement Index), quy trình triển khai ẩn danh, phân tích kết quả, và action plan post-survey. Là input chính cho việc cải thiện văn hóa và giảm turnover.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Quy mô DN: bao nhiêu nhân viên? Chia mấy phòng ban?
2. Đã từng làm engagement survey chưa? Kết quả cuối cùng (eNPS, score)?
3. Tần suất mong muốn: Annual (1 lần đầy đủ) + Pulse (mini hàng quý)?
4. Tool dùng để chạy khảo sát: Google Form / Typeform / SurveyMonkey / Officevibe / 15Five / Lattice?
5. Có cam kết của lãnh đạo công bố kết quả + action plan minh bạch không?
6. Các topic ưu tiên muốn đo: Leadership / Manager / Career / Compensation / Wellbeing / Diversity / Culture?
7. Ngân sách (tool + analysis + intervention sau survey)?

#### Template gợi ý
Cấu trúc FRM:
- **Mục đích Khảo sát**: Tại sao đo engagement, dùng để làm gì
- **Phương pháp luận**: Gallup Q12 / Engagement Index / eNPS — chọn framework
- **Cấu trúc Câu hỏi** (40-50 câu chia 8-10 dimension):
  - Engagement Index (5 câu — đo overall engagement)
  - eNPS (1 câu — Khả năng giới thiệu DN cho bạn bè)
  - Leadership & Vision (5 câu)
  - Direct Manager (5 câu)
  - Career Development (5 câu)
  - Recognition & Reward (4 câu)
  - Work-Life Balance & Wellbeing (4 câu)
  - Team & Collaboration (4 câu)
  - Compensation & Benefits (3 câu)
  - Culture & Values (4 câu)
  - Diversity & Inclusion (3 câu)
  - Open-ended (3 câu — most loved, biggest concern, suggestion)
- **Thang đo**: Likert 5 hoặc 7 điểm (Strongly Disagree → Strongly Agree)
- **Quy trình Triển khai**:
  - Pre-survey: Communication, manager briefing, reassure anonymity
  - During: Gửi link, reminder, monitor response rate (target ≥80%)
  - Post: Phân tích, present results, action planning
- **Phân tích & Báo cáo**:
  - Overall score + dimension score
  - eNPS calculation (Promoters - Detractors)
  - Cut by department / tenure / level / generation
  - Heat map dimension × department
  - Top 5 strengths + Top 5 areas of concern
  - Open-text theme analysis
- **Action Planning Framework**: Mỗi pain point → Owner → Action → Deadline → Re-measure
- **Communication Plan**: How & when to share results with employees
- **Ethics & Anonymity**: Cam kết về anonymity, data security, no retaliation

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
```
Tạo Employee Engagement Survey (Khảo sát gắn kết nhân viên).

CONTEXT:
- DN: [Tên] — Quy mô: [n nhân viên] — Phòng ban: [list]
- Đã làm survey trước: [có/không] — Kết quả: [eNPS/score]
- Tần suất: [Annual + Pulse / chỉ Annual]
- Tool: [Google Form / Typeform / Officevibe / khác]
- Topic ưu tiên: [list]
- Ngân sách: [VNĐ]

FORMAT:
- Methodology section: 1 trang giải thích framework (Gallup Q12 hoặc tự xây)
- Question bank: 40-50 câu chia 10 dimension — định dạng dễ copy vào tool
  • Mỗi câu: ID | Dimension | Question | Scale | Required (Y/N)
- Demographics (anonymous): Phòng ban / Tenure / Level / Generation (KHÔNG hỏi tên, giới, tuổi cụ thể)
- Communication template: 3 emails — Pre-launch, Launch, Reminder, Thank you
- Manager briefing deck: 5 slide cho manager
- Analysis template (Excel): Sheet Raw data | Sheet Dimension scores | Sheet eNPS | Sheet Cuts | Sheet Heat map
- Report template (PPT): 12-15 slide — Executive summary, Methodology, Results, Drivers, Action plan
- Action planning workshop guide: 90 phút workshop với leadership
- Communication plan post-survey: Bảng Audience | Message | Channel | Timeline
- Anonymity & Ethics statement: 1 trang cam kết với nhân viên

TONE: Khoa học, đáng tin cậy, đề cao anonymity và transparency.
LENGTH: Survey 40-50 câu (5 trang) + Methodology guide 10-15 trang + Excel template + PPT template.
LƯU Ý: Response rate ≥80% mới đáng tin. Dưới 60% phải re-evaluate triển khai.
```


---
📋 Tài liệu được tạo bởi MODORO
✍️ Tác giả: Quốc MODORO
🔗 Liên hệ hỗ trợ: https://bio.ybai.me/777777
