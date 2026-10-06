# Bài tập thực hành 4

## Phân tích 
- Mở 20 tab Chrome và VS Code cùng lúc làm %RAM quá tải. 
- RAM đầy kích hoạt Swap file, máy tính lấy SSD làm bộ nhớ tạm.
- %CPU tăng vọt do phải hoán đổi dữ liệu liên tục giữa RAM và SSD gây treo máy.
RAM: Dung lượng nhỏ (8GB), tốc độ cực nhanh, chứa công việc đang xử lý.
Storage : Dung lượng lớn (256GB SSD), tốc độ chậm, lưu trữ lâu dài. Bàn làm việc đầy phải cất tạm xuống ngăn tủ, khi cần lại moi lên làm hệ thống chậm đi.

## Thiết kế
Không lưu data vào C:\Windows\System32 vì đây là thư mục lõi hệ thống. Lưu ở đây dễ lỗi quyền truy cập và mất sạch dữ liệu khi cài lại Windows.
Cây thư mục ổ D (3 cấp, 4 trụ cột, kebab-case):

D:
/
hoc-tap-ptit

lap-trinh-python

bai-tap.py

du-an-ca-nhan

ung-dung-python

main-app.py

tai-lieu-tham-khao

sach-lap-trinh

python-basic.pdf

ho-so-ca-nhan

cv-xin-viec

cv-it-tester.pdf
