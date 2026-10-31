# Windows Registry và mã độc: tài liệu kiến thức nền dễ hiểu

Tài liệu học tập (tiếng Việt) giải thích **Windows Registry** và **cách mã độc lạm dụng Registry**, viết ở mức khái niệm, dễ đọc cho sinh viên chưa chuyên về bảo mật.

Tài liệu được soạn trong khuôn khổ bài tập lớn môn *Hệ điều hành Windows và Linux/Unix* (Nhóm 03).

## Nội dung

- **Phần A.** Windows Registry: khái niệm, cấu trúc cây, khóa gốc, kiểu dữ liệu, hive, Configuration Manager, khởi động, DACL/SACL/ACE, bảo vệ, sao lưu, công cụ.
- **Phần B.** Phân loại mã độc và sáu mục đích lạm dụng Registry.
- **Phần C.** Sáu kiểu lạm dụng Registry: Persistence, Fileless Storage, Defense Evasion, Privilege Escalation, Credential Access, Discovery và Impact.
- **Phần D–G.** Phát hiện và phòng chống, câu hỏi thường gặp, bảng thuật ngữ Anh – Việt, các lỗi cần lưu ý.

Đọc tại: [KienThucNen_DeHieu.md](KienThucNen_DeHieu.md).

## Hình minh họa

Thư mục [`images/`](images) chứa các sơ đồ do nhóm tự vẽ để minh họa tài liệu. Tài liệu không chứa ảnh chụp từ nguồn thứ ba.

## Lưu ý

- Đây là tài liệu **kiến thức tổng quát và phòng thủ**. Không có hướng dẫn tạo hay chạy mã độc.
- Mã MITRE ATT&CK, tên khóa Registry và mốc lịch sử đã được tra cứu theo tài liệu của Microsoft và MITRE. Một số chi tiết (như thay đổi của ATT&CK v19 năm 2026) dựa trên nguồn thứ cấp, nên đối chiếu lại trên trang chính thức trước khi trích dẫn.
- Một số ví dụ lấy từ báo cáo sandbox công khai (Joe Sandbox). Đó là quan sát của một báo cáo cụ thể, không phải kết luận chung về cả họ mã độc.
