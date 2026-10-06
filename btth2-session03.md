# BÁO CÁO BÀI TẬP 2: PHÂN TÍCH HIỆU NĂNG HỆ THỐNG VÀ QUẢN LÝ ĐƯỜNG DẪN TỆP

## PHÂN TÍCH

Nguyên nhân lỗi FileNotFoundError:
Đường dẫn tuyệt đối cố định địa chỉ theo cấu trúc ổ đĩa máy cũ. Khi chuyển sang máy khác, tên người dùng thay đổi làm đường dẫn bị đứt gãy, dẫn đến hệ điều hành không tìm thấy tệp dù file vẫn nằm trong dự án.

Luồng IPO khi nạp file từ Storage vào RAM:

Input: CPU phát lệnh đọc file ảnh từ bộ nhớ trong nạp vào RAM.

Process: CPU thực hiện giải mã dữ liệu ảnh từ dạng nén thành ma trận pixel thô và tính toán hiển thị.

Output: Dữ liệu pixel được xuất ra màn hình giao diện.

Giải thích RAM 98%: Ảnh lưu ở bộ nhớ trong đã được nén, khi CPU giải nén nạp vào RAM sẽ phình to gấp nhiều lần. Việc tải toàn bộ ảnh cùng lúc làm RAM quá tải gây treo máy.

GIẢI PHÁP KỸ THUẬT

Viết lại đường dẫn tương đối (dùng . và ..):

Ký hiệu . đại diện cho thư mục hiện hành.

Ký hiệu .. đại diện cho thư mục cha (lùi 1 cấp).

Cùng thư mục chạy code: ./assets/logo.png

File code nằm trong thư mục con (ví dụ src/): ../assets/logo.png

3 bước giảm lag dựa trên Task Manager:

Bước 1: Vào Task Manager, kiểm tra tab Processes -> Memory để tắt bớt các ứng dụng chạy ngầm chiếm nhiều RAM (như Chrome, Discord) để giải phóng bộ nhớ.

Bước 2: Tối ưu code theo cơ chế Lazy Loading (chỉ nạp ảnh vào RAM khi cần hiển thị trên giao diện, không nạp toàn bộ thư mục assets lúc khởi động).

Bước 3: Nén và giảm độ phân giải của các file ảnh logo trong thư mục assets về kích thước vừa đủ dùng để giảm dung lượng chiếm dụng trên RAM khi giải mã.
