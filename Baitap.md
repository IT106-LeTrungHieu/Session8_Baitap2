# BÀI TẬP 2

ƯỚC LƯỢNG PRODUCT BACKLOG CHO NỀN TẢNG BÁN HÀNG QUA LIVESTREAM

## Nhiệm vụ 1: Kiểm tra dữ liệu

| Mã Story | Đủ rõ | Cần làm rõ | Thông tin/câu hỏi còn thiếu |
| --- | --- | --- | --- |
| LS01 | ☐ | ☒ | Khi đến giờ bắt đầu, hệ thống có phải tự chuyển phiên sang trạng thái khác hay chỉ cần hiển thị “Sắp diễn ra”? |
| LS03 | ☐ | ☒ | Nếu hai khách cùng đặt sản phẩm cuối, hệ thống giữ số lượng và quyết định đơn nào thành công như thế nào để không bán vượt tồn kho? |

## Nhiệm vụ 2: Product Backlog đã ước lượng

| Mã Story | Mức ưu tiên | Kết quả phiếu | SP cuối cùng | Lý do ngắn |
| --- | --- | --- | --- | --- |
| LS01 | 1 | 3 - 3 - 5 - 3 | 3 | Phiếu chênh lệch do cách hiểu phạm vi xử lý thời gian và trạng thái; PO đã xác nhận tự chuyển trạng thái thuộc Story khác. Chọn 3 SP vì việc tạo phiên, kiểm tra tiêu đề và hiển thị “Sắp diễn ra” có khối lượng và độ phức tạp tương đương LS02. |
| LS02 | 2 | 3 - 3 - 3 - 3 | 3 | Reference Story; các phiếu đã trùng nhau. |
| LS03 | 3 | 5 - 8 - 8 - 5 | 8 | Phiếu chênh lệch do đánh giá khác nhau về độ phức tạp, rủi ro đặt đồng thời và quy tắc giảm/hoàn tồn; PO xác nhận chỉ đơn giữ được số lượng mới thành công. Chọn 8 SP, lớn hơn LS02, vì cần bảo đảm giữ số lượng an toàn khi đặt đồng thời, xử lý tạo/xác nhận/hủy đơn và kiểm thử tính nhất quán tồn kho. |

## Nhiệm vụ 3: Phát hiện cách hiểu sai

Cố định “1 Story Point = 4 giờ” là sai vì Story Point ước lượng tương đối quy mô công việc, độ phức tạp và rủi ro hoặc mức độ chưa chắc chắn, không đo số giờ cố định. Velocity là tổng Story Point của các Story đạt Definition of Done trong một Sprint; nhóm dùng kết quả của các Sprint gần đây để dự báo khối lượng SP có thể hoàn thành trong Sprint tiếp theo. Dự báo cần xét năng lực thực tế và bối cảnh Sprint, không quy đổi SP sang giờ và không xem Velocity là cam kết chắc chắn.
