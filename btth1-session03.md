# Bài Tập Thực Hành 1: Quản lý lưu trữ và đường dẫn tệp trong Windows
## Phần 1: Phân tích các sai lầm của Nam

- Vị trí lưu trữ sai: mục System32, đây là mục cốt lỗi của hệ điều hành nếu dùng đây là nơi chưa file thì dễ gây ra xung đột hệ thống.
- Cách đặt tên file sai quy tắc: Các thư mục và file Bai Tap Cua Nam, Session 01, bai tap 1.py chứa khoảng trắng và viết hoa lộn xộn. 
- Hiểu lầm đơn vị: Nam nhầm lẫn giữa Megabits và Megabytes.
*Theo chuẩn, 1 Byte = 8 bits. Do đó, gói mạng 100 Mbps sẽ có tốc độ tải xuống là: 100 / 8 = 12.5 MB/s. Chính xác.*

- Nguyên nhân SSD 256 GB hiển thị dung lượng thấp hơn: Do sự khác biệt trong hệ cơ số tính toán giữa các hệ điều hành:
- Nhà sản xuất: 1 KB = 1,000 Bytes, 1 GB = 1,000^3 Bytes. Ổ 256 GB có đúng 256,000,000,000 Bytes.
- Windows: T1 KiB = 1,024 Bytes, 1 GiB = 1,024^3 Bytes. 
- Khi Windows đọc 256,000,000,000 Bytes, nó chia cho 1024^3, kết quả hiển thị khoảng 238.4 GB. Phần dung lượng hao hụt nhỏ còn lại là do bị chiếm bởi định dạng hệ thống.

---

## Phần 2: Thiết kế lại cây thư mục học tập

Toàn bộ tên file và thư mục sử dụng chuẩn kebab-case (viết thường, không dấu, ngăn cách bằng dấu gạch ngang).

1. **projects:** Các dự án, bài tập ngắn hạn đang thực hiện.
2. **areas:** Các môn học, lĩnh vực kiến thức dài hạn.
3. **resources:** Tài liệu tham khảo, phần mềm, lms.
4. **archives:** Lưu trữ các môn học, dữ liệu cũ đã hoàn thành.

**Cây thư mục minh họa (Chuẩn 3 cấp trên ổ D):**

```text
D:\
└── hoc-tap\
    ├── projects\
    │   ├── it108-nhap-mon-cntt\
    │   │   ├── session-01\
    │   │   │   └── bai-tap-1.py
    │   │   └── session-02\
    │   └── dsa-cau-truc-du-lieu\
    │
    ├── areas\
    │   ├── lap-trinh-python\
    │   │   └── ly-thuyet-co-ban\
    │   └── tieng-anh-chuyen-nganh\
    │
    ├── resources\
    │   ├── softwares\
    │   │   └── python-installer\
    │   └── e-books\
    │
    └── archives\
        └── hoc-ky-1-2025\
            └── tin-hoc-van-phong\
