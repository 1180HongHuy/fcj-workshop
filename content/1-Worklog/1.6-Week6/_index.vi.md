---
title: "Worklog Tuần 6"
date: 2026-06-08
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**08/06/2026 - 14/06/2026**

### Mục tiêu tuần 6

* Viết câu lệnh truy xuất các metrics phản ánh hiệu năng và tình trạng hoạt động của hệ thống.
* Theo dõi các chỉ số `CPUUtilization`, `NetworkIn` và `NetworkOut` trên Amazon CloudWatch.
* Thiết lập một Dashboard tập trung để quan sát các metrics quan trọng trong cùng một giao diện.
* Rèn luyện khả năng phân tích dữ liệu giám sát nhằm phát hiện dấu hiệu bất thường và hỗ trợ tối ưu hệ thống.

### Nội dung thực tập

#### 1. Tìm hiểu metrics trên Amazon CloudWatch

Em tiếp tục nghiên cứu **Amazon CloudWatch** và cách dịch vụ này lưu trữ, tổng hợp các metrics do tài nguyên AWS phát sinh. Đối với phiên bản Amazon EC2, các metrics được sử dụng trong bài thực hành gồm:

* **CPUUtilization:** phản ánh tỷ lệ phần trăm năng lực xử lý CPU đang được sử dụng.
* **NetworkIn:** thể hiện lượng dữ liệu mạng đi vào phiên bản EC2.
* **NetworkOut:** thể hiện lượng dữ liệu mạng đi ra khỏi phiên bản EC2.

Việc theo dõi đồng thời các chỉ số này giúp có cái nhìn tổng quan hơn về tải xử lý và hoạt động mạng của máy chủ. Khi một chỉ số tăng hoặc giảm bất thường, cần đối chiếu với thời gian, hoạt động của ứng dụng và các metrics liên quan để xác định nguyên nhân.

#### 2. Viết câu lệnh truy xuất dữ liệu metrics

Em thực hành sử dụng AWS CLI để truy xuất dữ liệu từ namespace `AWS/EC2`. Các tham số được xác định trong câu lệnh gồm tên metric, instance ID, khoảng thời gian, chu kỳ tổng hợp, thống kê cần lấy và Region của tài nguyên.

Một số nhóm câu lệnh được nghiên cứu và thực hành:

* Sử dụng `aws cloudwatch get-metric-statistics` để truy xuất các điểm dữ liệu của một metric trong khoảng thời gian xác định.
* Sử dụng `aws cloudwatch get-metric-data` để truy vấn nhiều metrics hoặc nhiều chuỗi dữ liệu trong một lần thực hiện.
* Lọc dữ liệu theo dimension `InstanceId` để lấy đúng metrics của phiên bản EC2 cần theo dõi.
* Chọn khoảng thời gian và `Period` phù hợp để dữ liệu trả về có ý nghĩa khi phân tích.
* So sánh các giá trị `Average`, `Maximum` hoặc `Sum` tùy theo mục đích của từng metric.

Ví dụ, khi truy xuất `CPUUtilization`, em sử dụng đơn vị phần trăm và thống kê trung bình hoặc lớn nhất. Với `NetworkIn` và `NetworkOut`, em quan sát tổng lượng byte truyền trong từng khoảng thời gian để nhận biết mức độ hoạt động của mạng.

#### 3. Phân tích kết quả truy xuất

Sau khi chạy câu lệnh, em kiểm tra dữ liệu trả về gồm timestamp, giá trị metric, đơn vị đo và thông tin dimension. Kết quả được đối chiếu với khoảng thời gian thực hành để bảo đảm truy vấn đúng tài nguyên và Region.

Em cũng tìm hiểu một số trường hợp có thể khiến dữ liệu không như mong đợi, chẳng hạn như nhập sai instance ID, chọn sai namespace, sử dụng khoảng thời gian không có dữ liệu hoặc cấu hình Region không trùng với nơi tài nguyên được tạo. Việc kiểm tra này giúp nâng cao độ chính xác khi sử dụng metrics cho giám sát và phân tích hiệu năng.

#### 4. Thiết lập CloudWatch Dashboard tập trung

Em tạo một **CloudWatch Dashboard** để tập trung các metrics quan trọng của hệ thống vào cùng một giao diện. Dashboard được tổ chức thành các widget biểu đồ phù hợp cho từng loại dữ liệu:

* Widget theo dõi xu hướng `CPUUtilization` theo thời gian.
* Widget theo dõi lưu lượng `NetworkIn` và `NetworkOut` để so sánh hoạt động mạng.
* Cấu hình khoảng thời gian hiển thị và chu kỳ cập nhật phù hợp với nhu cầu quan sát.
* Đặt tên và sắp xếp widget rõ ràng để có thể nhanh chóng nhận biết tình trạng tài nguyên.
* Kiểm tra Dashboard bằng cách tạo hoạt động trên tài nguyên và quan sát sự thay đổi của các biểu đồ.

Dashboard tập trung giúp giảm thời gian chuyển đổi giữa các màn hình dịch vụ, hỗ trợ theo dõi hệ thống một cách trực quan và tạo cơ sở cho việc thiết lập cảnh báo trong các bước tiếp theo.

### Kết quả đạt được tuần 6

* Hiểu được ý nghĩa và cách sử dụng các metrics `CPUUtilization`, `NetworkIn` và `NetworkOut` để theo dõi hiệu năng EC2.
* Viết và thực hành các câu lệnh AWS CLI để truy xuất dữ liệu metrics từ Amazon CloudWatch.
* Biết cách xác định namespace, dimension, khoảng thời gian, period và statistic phù hợp cho một truy vấn metrics.
* Phân tích được dữ liệu trả về gồm giá trị, đơn vị đo và timestamp để đánh giá hoạt động của hệ thống.
* Thiết lập thành công CloudWatch Dashboard tập trung với các widget giám sát CPU và lưu lượng mạng.
* Nâng cao khả năng phát hiện dấu hiệu bất thường và theo dõi tài nguyên AWS qua giao diện trực quan kết hợp dòng lệnh.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon CloudWatch User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)
* [AWS CLI CloudWatch Command Reference](https://docs.aws.amazon.com/cli/latest/reference/cloudwatch/)





