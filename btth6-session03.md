# Bài tập thực hành 6

## Mô hình DIKW cho ứng dụng MoMo-Lite:

Data : ghi nhận các giao dịch thô đơn lẻ, vd: lịch sử thanh toán vé xe khách từ Duyên Hải lên TP.HCM.

Information : tổng hợp dữ liệu thành báo cáo, vd:  biểu đồ tổng chi tiêu tháng phân theo danh mục đi lại, ăn uống.

Knowledge : nhận diện xu hướng và phát cảnh báo, vd: thông báo tiền tiêu tháng này đã vượt ngân sách 20%.

Wisdom : đưa ra hành động cụ thể, vd: gợi ý người dùng tự động trích 500k vào heo đất MoMo mỗi lần nhận tiền vào ví để tránh tiêu lố.

## Các module IPO :

Input: nhận thông tin các giao dịch, số tiền, thời gian, tên dịch vụ từ hệ thống.

Process: phân loại danh mục, tính toán chi tiêu, so sánh dữ liệu với tháng trước để đưa ra các phân tích.

Output: hiển thị biểu đồ ra màn hình và thông báo nhắc nhở hoặc gợi ý tiết kiệm cho người dùng.

## Giải quyết các bẫy dữ liệu:

Bẫy 1 (File ẩn): Để hiện file .env, mở File Explorer, nhấn vào tab View --> Show và đánh dấu tích vào Hidden items.

Bẫy 2 (Tính dung lượng): 1 triệu giao dịch = 1.000.000 KB. Đổi sang MB : 1.000.000 / 1024 = 976,56 MB mỗi ngày.
