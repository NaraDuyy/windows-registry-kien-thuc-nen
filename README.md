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

## Hình trích từ bộ slide

Thư mục [`images/slide/`](images/slide) chứa các hình được cắt ra từ bộ slide thuyết trình của nhóm (độ phân giải theo trang slide 1920 × 1080). Tên tệp có dạng `SlideNN_tên-hình.png`, trong đó `NN` là số slide.

| Slide | Tệp | Nội dung |
|---|---|---|
| 3 | `Slide03_type-registry.png` | Sơ đồ truy vấn "Type Registry" (minh họa khái niệm chung, không phải thành phần của Windows) |
| 4 | `Slide04_vai-tro-registry.png` | Bảy vai trò của Registry |
| 5 | `Slide05_cay-registry.png` | Cấu trúc Registry dạng cây |
| 6 | `Slide06_khoa-goc.png` | Cấu trúc phân cấp của các khóa gốc |
| 7 | `Slide07_kieu-du-lieu.png` | Bảng các kiểu dữ liệu giá trị |
| 8 | `Slide08_regedit-hive.png`, `Slide08_bang-hive.png` | Registry Editor minh họa hive, khóa, khóa con; bảng hive và tệp vật lý |
| 9 | `Slide09_kien-truc-truy-cap.png` | Kiến trúc truy cập Registry trong Windows |
| 10 | `Slide10_khoi-dong.png` | Registry trong quá trình khởi động |
| 11 | `Slide11_quan-ly-quyen.png` | Quản lý quyền truy cập (DACL, ACE, token) |
| 12 | `Slide12_bao-ve-he-thong.png` | Các lớp bảo vệ Registry ở mức hệ thống |
| 13 | `Slide13_sao-luu.png` | Sao lưu và khôi phục Registry |
| 14 | `Slide14_cong-cu.png` | Các công cụ quản trị Registry |
| 15 | `Slide15_phan-loai-ma-doc.png` | Phân loại mã độc theo chức năng |
| 16 | `Slide16_muc-dich-lam-dung.png` | Các mục đích lạm dụng Registry của mã độc |
| 17 | `Slide17_ma-doc-duy-tri.png` | Cơ chế hoạt động của RAT và tác động lên Registry |
| 18 | `Slide18_ma-doc-khong-tep.png` | Quy trình tấn công của mã độc không tệp |
| 21 | `Slide21_ma-doc-stealer.png` | Sơ đồ hoạt động của một stealer (RedLine) |

**Về bản quyền hình.** Các hình trong `images/slide/` được trích nguyên từ slide của nhóm. Một số hình có nguồn từ bên thứ ba (ví dụ ảnh có hình mờ của trang nguồn, sơ đồ trong tài liệu của nhà cung cấp, sơ đồ mô hình kiểm soát truy cập của Microsoft). Bản quyền các hình đó thuộc về chủ sở hữu tương ứng. Nếu chủ sở hữu yêu cầu gỡ, chúng tôi sẽ xóa hình khỏi repo. Các sơ đồ trong `images/` (ngoài thư mục `slide/`) là do nhóm tự vẽ.
