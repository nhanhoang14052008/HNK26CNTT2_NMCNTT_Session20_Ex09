## Phần 1: Thiết kế Prompt

**1.** Câu hỏi thiếu ngữ cảnh và thông báo lỗi cụ thể nên AI dễ đoán sai nguyên nhân, dẫn đến hiện tượng AI Hallucination.

**2. Prompt 3 thành phần:**

[Context]: Trạm sạc VoltCharge #04 chạy Windows 11 bị lỗi khi khởi động.

[Raw Error]: `UnauthorizedAccessException: Access to the path 'C:\Program Files\VoltCharge\data\session.log' is denied. Exit code 5.`

[Instruction]: Giải thích lỗi bằng tiếng Việt và đưa ra 3 bước khắc phục an toàn.

## Phần 2: Giải mã lỗi và khắc phục

**3.** Lỗi có nghĩa là phần mềm không có quyền ghi vào file `session.log` trong thư mục `Program Files`.

**4. Ba bước xử lý:**
- Bước 1: Chọn Run as Administrator để chạy phần mềm.
- Bước 2: Vào Properties → Security của thư mục `data`.
- Bước 3: Cấp quyền Write và Modify cho đúng tài khoản chạy phần mềm, sau đó khởi động lại.

**5.** Xóa hoặc thay API Key bằng `[REDACTED]` trước khi gửi AI để tránh lộ thông tin bí mật và bị truy cập trái phép.
