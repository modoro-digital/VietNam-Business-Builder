# PROMPT 04: Execution Flow (Luồng thực thi)

#### Mô tả
SOP mô tả chi tiết luồng thực thi: thứ tự gọi 12 skill con, điều kiện trigger mỗi skill, dependencies giữa các skill, cách xử lý khi 1 skill fail hoặc bị skip.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. Muốn chạy tuần tự (sequential) hay song song (parallel) khi có thể?
2. Có checkpoint review giữa các tầng không? (VD: dừng sau Tầng 1 để chủ DN duyệt)
3. Khi 1 skill fail, hành xử thế nào? (retry / skip / halt all)
4. Ai approve kết quả mỗi skill trước khi chuyển sang skill tiếp?
5. Có time-box cho mỗi skill không? (VD: mỗi skill tối đa 2 giờ)

#### Template gợi ý
Cấu trúc SOP:
- **Execution Modes** — Full run / Selective run / Single skill
- **Dependency Map** — Skill nào phụ thuộc skill nào (DAG diagram)
- **Trigger Conditions** — Khi nào skill được activate
- **Checkpoint Gates** — Điểm dừng để review & approve
- **Error Handling** — Retry logic, fallback, escalation
- **Progress Tracking** — Status dashboard (% complete per skill)
- **Flowchart** — Mermaid diagram toàn bộ luồng

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
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
