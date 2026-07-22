---
title: "Worklog Tuần 5"
date: 2026-06-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**01/06/2026 - 07/06/2026**

### Mục tiêu tuần 5

* Thiết lập các chỉ số và cơ chế giám sát để theo dõi tình trạng hoạt động của hệ thống trên AWS.
* Tìm hiểu cách dịch vụ theo dõi tự động của AWS thu thập, hiển thị và cảnh báo dựa trên các chỉ số vận hành.
* Thực hành sử dụng AWS CLI để thêm, chỉnh sửa, xóa và kiểm tra trạng thái tài nguyên hoặc dịch vụ.
* Làm quen với quy trình quản lý tài nguyên bằng dòng lệnh nhằm tăng tính nhất quán và khả năng tự động hóa.

### Nội dung thực tập

#### 1. Thiết lập giám sát hệ thống trên AWS

Em tìm hiểu **Amazon CloudWatch**, dịch vụ giám sát và quan sát tự động của AWS. CloudWatch hỗ trợ thu thập các chỉ số, nhật ký và sự kiện từ tài nguyên cũng như dịch vụ AWS, giúp người dùng theo dõi tình trạng hoạt động của hệ thống.

Các nội dung đã tìm hiểu gồm:

* Xác định những chỉ số quan trọng cần theo dõi, chẳng hạn như mức sử dụng CPU, lưu lượng mạng, số lượng request và trạng thái tài nguyên.
* Quan sát dữ liệu chỉ số trên CloudWatch Dashboard để đánh giá tình trạng hệ thống.
* Tìm hiểu log và event nhằm hỗ trợ việc phát hiện nguyên nhân khi dịch vụ hoạt động không đúng như mong đợi.
* Thiết lập ngưỡng cảnh báo phù hợp cho các chỉ số cần giám sát.
* Nghiên cứu cách CloudWatch Alarm chuyển sang các trạng thái `OK`, `ALARM` hoặc `INSUFFICIENT_DATA` dựa trên dữ liệu nhận được.

Qua hoạt động này, em hiểu được vai trò của việc giám sát chủ động. Việc theo dõi chỉ số thường xuyên giúp phát hiện sớm dấu hiệu bất thường, hỗ trợ xử lý sự cố và cung cấp dữ liệu để tối ưu hiệu năng hệ thống.

#### 2. Làm quen với AWS CLI

Em cài đặt và sử dụng **AWS Command Line Interface (AWS CLI)** để thực hiện các thao tác quản lý tài nguyên AWS từ dòng lệnh. Trước khi thực hành, em kiểm tra cấu hình thông tin xác thực, region mặc định và quyền của IAM user hoặc role được sử dụng.

AWS CLI giúp thực hiện các thao tác lặp lại nhanh chóng và có thể tích hợp vào script hoặc quy trình tự động hóa. Em cũng chú ý sử dụng đúng profile, region và quyền truy cập để tránh thao tác nhầm trên tài nguyên không liên quan.

#### 3. Thực hành thêm, sửa và xóa tài nguyên

Em thực hành các nhóm thao tác quản lý tài nguyên bằng AWS CLI theo vòng đời cơ bản:

* **Thêm:** tạo tài nguyên hoặc cấu hình mới bằng câu lệnh tương ứng của dịch vụ.
* **Sửa:** cập nhật thuộc tính, cấu hình hoặc thông tin cần thiết của tài nguyên đang tồn tại.
* **Xóa:** loại bỏ tài nguyên thử nghiệm sau khi hoàn thành để tránh phát sinh chi phí không cần thiết.
* **Kiểm tra:** sử dụng các lệnh truy vấn hoặc mô tả để xác nhận tài nguyên đã được tạo và cấu hình đúng.

Trong quá trình thực hành, em đọc cú pháp lệnh, xác định các tham số bắt buộc và kiểm tra kết quả trả về sau mỗi thao tác. Việc này giúp hạn chế lỗi do sai tên tài nguyên, sai region hoặc thiếu quyền IAM.

#### 4. Quản lý và kiểm tra trạng thái dịch vụ

Em sử dụng AWS CLI để kiểm tra trạng thái hoạt động của các tài nguyên và dịch vụ sau khi tạo hoặc cập nhật. Kết quả trả về được đối chiếu với trạng thái mong đợi để xác định thao tác đã hoàn tất hay vẫn đang được xử lý.

Các bước kiểm tra bao gồm:

* Truy vấn thông tin chi tiết của tài nguyên bằng lệnh `describe`, `get` hoặc lệnh tương ứng của từng dịch vụ.
* Kiểm tra trạng thái trước và sau khi thực hiện thao tác thay đổi.
* Đọc thông báo lỗi khi câu lệnh thất bại để xác định nguyên nhân như thiếu quyền, sai tham số hoặc tài nguyên không tồn tại.
* Theo dõi các thay đổi trên CloudWatch khi thao tác có ảnh hưởng đến hoạt động của hệ thống.
* Xác nhận và dọn dẹp tài nguyên thử nghiệm sau khi hoàn thành bài thực hành.

### Kết quả đạt được tuần 5

* Hiểu được vai trò của Amazon CloudWatch trong việc thu thập chỉ số, theo dõi log, sự kiện và cảnh báo tình trạng hệ thống.
* Thiết lập và quan sát các chỉ số giám sát cơ bản, đồng thời hiểu ý nghĩa các trạng thái của CloudWatch Alarm.
* Sử dụng được AWS CLI để truy vấn và quản lý tài nguyên AWS từ dòng lệnh.
* Thực hành các thao tác thêm, chỉnh sửa, xóa và kiểm tra tài nguyên theo vòng đời quản lý cơ bản.
* Biết cách kiểm tra trạng thái dịch vụ, đọc phản hồi và xử lý một số lỗi cấu hình thường gặp.
* Nhận thức rõ hơn về việc sử dụng IAM permission, đúng region và dọn dẹp tài nguyên để bảo đảm an toàn và kiểm soát chi phí.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon CloudWatch User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)
* [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/reference/)


