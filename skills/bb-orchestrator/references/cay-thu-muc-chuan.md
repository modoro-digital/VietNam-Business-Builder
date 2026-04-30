# PROMPT 03: Directory Scaffold (Cây thư mục chuẩn)

#### Mô tả
SOP hướng dẫn tạo cây thư mục hoàn chỉnh cho DN — bao gồm naming convention, numbering system, và template README cho mỗi folder. Đảm bảo 200+ file được tổ chức logic, dễ tìm, dễ maintain.

#### Thông tin cần thu thập (hỏi người dùng trước khi tạo)
1. DN muốn lưu trữ ở đâu? (Google Drive / SharePoint / Notion / Local folder / Git repo)
2. Có naming convention riêng không? (VD: [Dept]-[Type]-[Name]-v[Version])
3. Ngôn ngữ file name: tiếng Việt, tiếng Anh, hay mã số?
4. Cần version control không? (v1, v2... hay date-based?)
5. Có cần phân quyền truy cập theo folder không?

#### Template gợi ý
Cấu trúc SOP:
- **Naming Convention** — Quy tắc đặt tên: `[##]-[Category]-[Type]-[Name].[ext]`
- **Numbering System** — 00-12 cho skill, 00.1-00.x cho sub-groups
- **Folder Structure** — Tree view đầy đủ 5 tầng
- **README Template** — Mỗi folder có README mô tả contents
- **File Types** — POL/MAN/SOP/FRM/RPT + extension mapping
- **Auto-generation Script** — Pseudocode/script tạo toàn bộ cây thư mục

Confirm cấu trúc trước khi tạo.

#### Prompt tạo file
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
