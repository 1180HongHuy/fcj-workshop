---
title: "Worklog Tuần 4"
date: 2026-05-27
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**25/05/2026 - 31/05/2026**

### Mục tiêu tuần 4

* Khám phá chuyên sâu các nguyên tắc thiết kế kiến trúc đám mây nhằm tối ưu hiệu năng, khả năng mở rộng và tính ổn định của hệ thống.
* Hiểu cách lựa chọn và tổ chức tài nguyên lưu trữ phù hợp với yêu cầu của ứng dụng.
* Thực hành tạo, quản lý và phân quyền đối với Amazon S3 và Amazon EBS.
* Nâng cao khả năng cấu hình quyền truy cập theo nguyên tắc cấp quyền tối thiểu và bảo vệ dữ liệu trên AWS.

### Nội dung thực tập

#### 1. Nghiên cứu thiết kế kiến trúc đám mây tối ưu hiệu năng

Em tìm hiểu các giải pháp thiết kế kiến trúc đám mây hướng đến hiệu năng cao, khả năng mở rộng và tính sẵn sàng. Nội dung nghiên cứu tập trung vào việc phân tích yêu cầu của ứng dụng, lựa chọn dịch vụ phù hợp và phân chia hệ thống thành các thành phần có thể mở rộng độc lập.

Một số nguyên tắc được nghiên cứu gồm:

* Lựa chọn loại tài nguyên và cấu hình phù hợp với đặc điểm tải của ứng dụng.
* Tách biệt các lớp lưu trữ, xử lý và truy cập để dễ dàng mở rộng, giám sát và bảo trì.
* Hạn chế các điểm nghẽn bằng cách phân phối tài nguyên và tối ưu cách ứng dụng truy cập dữ liệu.
* Sử dụng cơ chế lưu trữ, bộ nhớ đệm hoặc phân phối nội dung phù hợp để giảm độ trễ.
* Theo dõi hiệu năng, mức sử dụng tài nguyên và chi phí để có cơ sở điều chỉnh kiến trúc.

Qua nội dung này, em hiểu rằng một kiến trúc tối ưu không chỉ phụ thuộc vào tốc độ xử lý mà còn cần cân bằng giữa hiệu năng, khả năng mở rộng, tính sẵn sàng, bảo mật và chi phí vận hành.

#### 2. Thực hành với Amazon S3

Em thực hành sử dụng **Amazon S3** để tạo và quản lý kho lưu trữ đối tượng. Các nội dung chính gồm:

* Tạo một S3 bucket với tên và cấu hình phù hợp.
* Tìm hiểu cách tải lên, xem, tải xuống và xóa các đối tượng trong bucket.
* Phân biệt bucket, object, key và metadata trong mô hình lưu trữ của S3.
* Nghiên cứu các tùy chọn kiểm soát quyền truy cập và bảo vệ dữ liệu trong bucket.
* Kiểm tra cách cấp quyền truy cập cho người dùng hoặc dịch vụ thông qua IAM policy.

Trong quá trình thực hành, em chú ý không công khai dữ liệu ngoài nhu cầu sử dụng và tìm hiểu cách kiểm soát quyền ở cấp độ bucket hoặc object. Điều này giúp hạn chế nguy cơ truy cập trái phép đối với dữ liệu được lưu trữ.

#### 3. Thực hành với Amazon EBS

Em tìm hiểu **Amazon Elastic Block Store (Amazon EBS)**, dịch vụ cung cấp bộ nhớ khối bền vững để sử dụng cùng các phiên bản Amazon EC2. Các hoạt động thực hành gồm:

* Tìm hiểu các khái niệm volume, snapshot và khả năng gắn volume vào EC2.
* Tạo một EBS volume với loại và dung lượng phù hợp cho bài lab.
* Gắn volume vào phiên bản EC2 và kiểm tra trạng thái kết nối.
* Tìm hiểu cách quản lý, mở rộng và tháo gắn volume khi cần thiết.
* Nghiên cứu snapshot như một phương án sao lưu và khôi phục dữ liệu.

Qua bài thực hành, em phân biệt được Amazon S3 với Amazon EBS: S3 là dịch vụ lưu trữ đối tượng có khả năng mở rộng cao, còn EBS cung cấp bộ nhớ khối gắn trực tiếp với EC2 để phục vụ hệ điều hành và ứng dụng.

#### 4. Phân quyền và bảo mật dịch vụ lưu trữ

Em nghiên cứu cách sử dụng AWS IAM để phân quyền truy cập đối với Amazon S3 và Amazon EBS. Việc cấu hình được thực hiện theo nguyên tắc cấp đúng quyền cần thiết cho đúng người dùng hoặc dịch vụ, tránh sử dụng quyền quản trị toàn bộ khi không cần thiết.

Các nội dung tìm hiểu gồm:

* Phân biệt identity-based policy và resource-based policy trong việc kiểm soát truy cập.
* Xác định các thao tác cần thiết như tạo, đọc, ghi, liệt kê hoặc xóa tài nguyên.
* Hạn chế phạm vi tài nguyên và thao tác trong policy thay vì cấp quyền rộng.
* Kiểm tra quyền sau khi cấu hình để bảo đảm người dùng có thể thực hiện đúng nhiệm vụ được giao.
* Kết hợp bảo mật quyền truy cập với việc theo dõi, sao lưu và quản lý vòng đời dữ liệu.

### Kết quả đạt được tuần 4

* Hiểu được các nguyên tắc cơ bản khi thiết kế kiến trúc đám mây hướng đến hiệu năng, khả năng mở rộng, tính sẵn sàng và tối ưu chi phí.
* Tạo và thực hành quản lý bucket, object trên Amazon S3.
* Hiểu được đặc điểm của Amazon EBS và thực hành tạo, gắn, quản lý volume với phiên bản EC2.
* Phân biệt được trường hợp sử dụng của Amazon S3 và Amazon EBS trong kiến trúc AWS.
* Nắm được cách áp dụng IAM policy để phân quyền truy cập dịch vụ lưu trữ theo nguyên tắc cấp quyền tối thiểu.
* Có nền tảng để tiếp tục nghiên cứu các giải pháp lưu trữ, sao lưu và tối ưu kiến trúc AWS trong các tuần tiếp theo.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon S3 User Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)
* [Amazon EBS User Guide](https://docs.aws.amazon.com/ebs/latest/userguide/what-is-ebs.html)

