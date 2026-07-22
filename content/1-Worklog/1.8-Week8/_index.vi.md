---
title: "Worklog Tuần 8"
date: 2026-06-22
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**22/06/2026 - 28/06/2026**

### Mục tiêu tuần 8

* Cấu hình hệ thống thu thập, lưu trữ và phân tích nhật ký nâng cao bằng Amazon CloudWatch Logs.
* Thiết lập CloudWatch Alarms để phát hiện các điều kiện bất thường và hỗ trợ cảnh báo vận hành.
* Tìm hiểu AWS Systems Manager (SSM) trong việc quản lý máy chủ ảo tập trung.
* Thực hành quản lý cấu hình và triển khai bản vá bảo mật cho máy chủ theo cách có kiểm soát.

### Nội dung thực tập

#### 1. Quản lý nhật ký với CloudWatch Logs

Em tìm hiểu **Amazon CloudWatch Logs** và cách dịch vụ này tập trung nhật ký từ các nguồn khác nhau để phục vụ giám sát, phân tích và xử lý sự cố. Nội dung thực hành tập trung vào việc tổ chức log theo log group và log stream, đồng thời xác định thời gian lưu trữ phù hợp.

Các hoạt động chính gồm:

* Tìm hiểu log group, log stream, log event và timestamp trong CloudWatch Logs.
* Kiểm tra cách thu thập log từ tài nguyên hoặc ứng dụng về một nơi tập trung.
* Tìm kiếm các chuỗi lỗi, cảnh báo và thông tin quan trọng trong log.
* Lọc và phân tích log để xác định thời điểm cũng như nguyên nhân của sự cố.
* Nghiên cứu thời gian lưu trữ log nhằm cân bằng nhu cầu điều tra với chi phí lưu trữ.

Việc tập trung nhật ký giúp giảm thời gian truy cập từng máy chủ riêng lẻ, tạo điều kiện so sánh sự kiện giữa các thành phần và hỗ trợ theo dõi lịch sử hoạt động của hệ thống.

#### 2. Thiết lập CloudWatch Alarms

Em thực hành thiết lập **CloudWatch Alarms** dựa trên các metrics hoặc điều kiện được xác định trước. Alarm có thể theo dõi một metric trong một khoảng thời gian và chuyển trạng thái khi giá trị vượt qua ngưỡng cấu hình.

Các nội dung đã thực hiện gồm:

* Lựa chọn metric và xác định điều kiện cần giám sát.
* Cấu hình ngưỡng, khoảng thời gian đánh giá và số lần vi phạm liên tiếp.
* Tìm hiểu các trạng thái `OK`, `ALARM` và `INSUFFICIENT_DATA`.
* Kiểm tra lịch sử thay đổi trạng thái để xác định thời điểm điều kiện cảnh báo xảy ra.
* Liên kết alarm với cơ chế thông báo hoặc hành động xử lý phù hợp.

Em kiểm tra alarm bằng cách quan sát dữ liệu metric và đối chiếu trạng thái cảnh báo. Qua đó, em hiểu được cách xây dựng một cơ chế phát hiện sớm khi tài nguyên có dấu hiệu quá tải hoặc hoạt động khác thường.

#### 3. Làm quen với AWS Systems Manager

Em nghiên cứu **AWS Systems Manager (SSM)**, dịch vụ hỗ trợ quản lý tập trung các máy chủ và tài nguyên trong môi trường AWS. SSM giúp thực hiện các tác vụ quản trị mà không nhất thiết phải kết nối thủ công đến từng máy chủ thông qua giao thức SSH hoặc RDP.

Các nội dung tìm hiểu gồm:

* Kiểm tra điều kiện để máy chủ được SSM quản lý, bao gồm SSM Agent, IAM instance profile và khả năng kết nối cần thiết.
* Tìm hiểu Fleet Manager hoặc thông tin managed nodes để theo dõi các máy chủ đã đăng ký.
* Sử dụng Run Command để thực thi lệnh quản trị trên một hoặc nhiều máy chủ.
* Tìm hiểu Parameter Store để lưu trữ và quản lý tham số cấu hình tập trung.
* Xem lịch sử lệnh, kết quả thực thi và thông báo lỗi để kiểm tra quá trình quản trị.

Việc quản lý tập trung giúp chuẩn hóa thao tác trên nhiều máy chủ, giảm sai sót do thực hiện thủ công và hỗ trợ kiểm tra lại lịch sử thay đổi.

#### 4. Quản lý cấu hình và vá lỗi bảo mật tập trung

Em thực hành tìm hiểu quy trình quản lý cấu hình và cập nhật bản vá bảo mật cho máy chủ bằng SSM. Nội dung tập trung vào việc kiểm tra trạng thái bản vá, xác định các bản cập nhật còn thiếu và lập kế hoạch áp dụng theo phạm vi được kiểm soát.

Các bước chính gồm:

* Kiểm tra thông tin hệ điều hành, cấu hình và trạng thái quản lý của máy chủ.
* Sử dụng Patch Manager để xem các bản vá bảo mật còn thiếu theo baseline hoặc tiêu chí được chọn.
* Đánh giá ảnh hưởng trước khi cài đặt bản vá và chọn nhóm máy chủ phù hợp.
* Thực hiện cập nhật theo lịch hoặc theo nhóm để hạn chế ảnh hưởng đến hệ thống đang hoạt động.
* Kiểm tra lại trạng thái sau khi vá và xác nhận kết quả trên từng máy chủ.
* Theo dõi log và lịch sử thực thi để phục vụ kiểm tra, truy vết và báo cáo.

Em nhận thấy việc vá lỗi tập trung cần đi kèm với việc kiểm thử, sao lưu và kế hoạch khôi phục phù hợp. Không nên áp dụng thay đổi trên diện rộng mà không kiểm tra trước tác động đến ứng dụng và dịch vụ liên quan.

### Kết quả đạt được tuần 8

* Hiểu được cách tổ chức và quản lý nhật ký tập trung bằng CloudWatch Logs.
* Thực hành tìm kiếm, lọc và phân tích log để hỗ trợ phát hiện và điều tra sự cố.
* Thiết lập và kiểm tra CloudWatch Alarms với ngưỡng, khoảng thời gian và trạng thái phù hợp.
* Nắm được vai trò của AWS Systems Manager trong việc quản lý máy chủ ảo tập trung.
* Hiểu quy trình kiểm tra cấu hình, xác định bản vá thiếu và quản lý cập nhật bảo mật bằng SSM Patch Manager.
* Thực hành theo dõi kết quả lệnh, lịch sử thay đổi và trạng thái sau khi cập nhật.
* Nhận thức rõ tầm quan trọng của kiểm thử, phân quyền IAM, sao lưu và kế hoạch khôi phục trước khi thay đổi cấu hình hoặc vá lỗi trên máy chủ.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon CloudWatch Logs User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html)
* [AWS Systems Manager User Guide](https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html)
* [AWS Systems Manager Patch Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/patch-manager.html)




