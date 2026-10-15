# BÀI TẬP 2

LẬP KẾ HOẠCH SPRINT CHO HỆ THỐNG ĐẶT LỊCH SẠC XE MÁY ĐIỆN

## Nhiệm vụ 1: Phân tích Velocity và Capacity

### Bảng Velocity

| Sprint | SP hoàn thành (Done) | Ghi chú |
| --- | --- | --- |
| Sprint -3 | 15 | Đủ thành viên |
| Sprint -2 | 16 | Đủ thành viên |
| Sprint -1 | 17 | Đủ thành viên |
| Velocity tham khảo | 16 SP | (15 + 16 + 17) / 3 = 16 SP; dùng làm dữ liệu tham khảo để dự báo khối lượng Sprint, không phải cam kết và không đổi SP sang giờ. |

### Bảng Capacity

| Developers | Ngày Sprint | Ngày không tham gia | Ngày khả dụng | Giờ tập trung/ngày | Capacity (giờ) |
| --- | --- | --- | --- | --- | --- |
| Dev A | 10 | 0 | 10 | 5 | 50 |
| Dev B | 10 | 0 | 10 | 5 | 50 |
| Dev C | 10 | 2 | 8 | 5 | 40 |
| Dev D | 10 | 0 | 10 | 5 | 50 |
| Tổng | | | | | 190 giờ |

**Nhận xét:** Capacity Sprint này là 190 giờ, giảm 10 giờ (5%) so với 200 giờ khi đủ người; nhóm dùng Velocity tham khảo 16 SP cùng Capacity giảm và khả năng thực hiện các Task để dự báo khối lượng phù hợp, không quy đổi SP sang giờ hay coi dự báo là cam kết.

## Nhiệm vụ 2: Viết lại Sprint Goal

**Sprint Goal đã chỉnh sửa:** Người dùng có thể tìm trạm sạc, xem các khung giờ còn trống và đặt trước một vị trí sạc với mã xác nhận để chủ động lịch sạc và giảm thời gian chờ tại trạm.

## Nhiệm vụ 3: Lập Sprint Backlog

### Bảng chọn PBI

| Mã Story | Ưu tiên | SP | Chọn/Chưa chọn | Lý do |
| --- | --- | --- | --- | --- |
| CS01 | 1 | 3 | ☑ Chọn ☐ Chưa | Ưu tiên 1; bước đầu để người dùng tìm trạm. |
| CS02 | 2 | 3 | ☑ Chọn ☐ Chưa | Ưu tiên 2; cần biết giờ còn trống trước khi đặt. |
| CS03 | 3 | 5 | ☑ Chọn ☐ Chưa | Hoàn thiện luồng đặt trước để đạt Sprint Goal; tổng 11 SP thấp hơn Velocity tham khảo 16 SP, tạo dư địa khi Capacity giảm và cần kiểm tra rủi ro đặt trùng. |
| CS04 | 4 | 5 | ☐ Chọn ☑ Chưa | Quy tắc hạn chế hủy sát giờ chưa được chốt; ưu tiên thấp hơn và chưa cần thiết để đạt Sprint Goal về tìm trạm, xem giờ trống và đặt trước. |
| Tổng SP đã chọn | | 11 SP | | Mức dự báo, không phải cam kết. |

### Task Breakdown cho CS03

| STT | Task | Đầu ra | Ước lượng (giờ) |
| --- | --- | --- | --- |
| 1 | Xây dựng và kiểm thử API đặt lịch: kiểm tra trạm, khung giờ và xe; xử lý đặt đồng thời bằng giao dịch và ràng buộc chống trùng; cấp mã xác nhận. | API tạo lịch hợp lệ có mã xác nhận; kiểm thử chứng minh một vị trí không nhận hai lịch trùng thời gian, kể cả khi hai yêu cầu đến đồng thời. | 24 |
| 2 | Xây dựng giao diện chọn trạm, giờ và xe; tích hợp API và kiểm thử luồng đặt lịch thành công, thất bại do vị trí vừa được đặt. | Người dùng đặt lịch trên giao diện và nhận mã xác nhận; nếu vị trí không còn trống, hiển thị thông báo phù hợp và cập nhật lựa chọn khả dụng. | 16 |

Ước lượng hai Task của CS03 là 40 giờ, dựa trên công việc cụ thể, không suy ra từ 5 SP; khi lập kế hoạch chi tiết, nhóm còn phải đối chiếu Task của CS01, CS02 và toàn bộ công việc cần để đạt Definition of Done với Capacity 190 giờ.

## Nhiệm vụ 4: Phân tích Burndown Chart

1. Đường thực tế nằm trên đường lý tưởng từ ngày 1 đến ngày 9; tại ngày 7 còn 8 SP trong khi lý tưởng còn 3,3 SP. Đường thực tế đi ngang từ ngày 3 đến ngày 7 ở mức 8 SP cho thấy không có thêm PBI đạt Done trong khoảng này, có thể do công việc bị tắc hoặc dồn kiểm thử, gây rủi ro không hoàn thành luồng đặt trước theo Sprint Goal. Dù ngày 8 giảm còn 5 SP và ngày 10 về 0 SP, tại ngày 7 nhóm vẫn cần xử lý rủi ro sớm.

2. Tại Daily Scrum ngày 7, khi còn 8 SP so với mức lý tưởng 3,3 SP, nhóm thống nhất tập trung phối hợp để tháo vướng và hoàn tất PBI đang gần Done nhất trong luồng xem giờ trống và đặt lịch, bao gồm kiểm thử và sửa lỗi cần thiết. Hành động này giúp giảm công việc dở dang và bảo vệ Sprint Goal trong ba ngày còn lại; chỉ trừ SP khi PBI đạt Definition of Done.
