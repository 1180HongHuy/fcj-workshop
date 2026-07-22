---
title: "Worklog Tuần 2"
date: 2026-05-11
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**11/05/2026 - 17/05/2026**

### Mục tiêu tuần 2

* Thực hành các bước cơ bản để khởi tạo và cấu hình một máy chủ ảo trên Amazon EC2.
* Hiểu cách tổ chức tài nguyên mạng trên AWS thông qua VPC, Subnet và Security Group.
* Nắm được các khái niệm nền tảng của Cloud Computing và mô hình trách nhiệm chia sẻ trong AWS.
* Hình thành kiến thức cần thiết để triển khai các tài nguyên AWS theo hướng an toàn và có kiểm soát.

### Nội dung thực tập

#### 1. Nghiên cứu lý thuyết Cloud Computing

Em tìm hiểu các khái niệm cơ bản của **Cloud Computing**, trong đó có việc cung cấp tài nguyên công nghệ thông tin theo nhu cầu thông qua Internet. Nội dung học tập tập trung vào các đặc điểm chính của điện toán đám mây như khả năng mở rộng linh hoạt, sử dụng tài nguyên theo nhu cầu, tự động cung cấp tài nguyên và thanh toán dựa trên mức sử dụng.

Bên cạnh đó, em tìm hiểu các mô hình dịch vụ phổ biến gồm **Infrastructure as a Service (IaaS)**, **Platform as a Service (PaaS)** và **Software as a Service (SaaS)**. Qua đó, em hiểu rõ hơn vị trí của Amazon EC2 trong nhóm dịch vụ IaaS và vai trò của nhà cung cấp cũng như người sử dụng trong từng mô hình.

#### 2. Tìm hiểu mô hình Shared Responsibility

Em nghiên cứu mô hình **Shared Responsibility Model** của AWS, trong đó trách nhiệm bảo mật được phân chia giữa AWS và khách hàng:

* AWS chịu trách nhiệm bảo mật **của** đám mây, bao gồm cơ sở hạ tầng vật lý, phần cứng, mạng lõi và các dịch vụ nền tảng do AWS cung cấp.
* Khách hàng chịu trách nhiệm bảo mật **trong** đám mây, bao gồm dữ liệu, hệ điều hành, ứng dụng, cấu hình mạng, quyền truy cập và các thiết lập bảo mật phù hợp với dịch vụ đang sử dụng.
* Mức độ trách nhiệm của khách hàng có thể thay đổi tùy theo loại dịch vụ. Với Amazon EC2, khách hàng cần chủ động quản lý hệ điều hành khách, bản vá, phần mềm, dữ liệu và quy tắc truy cập mạng.

Việc nắm rõ mô hình này giúp em hiểu rằng sử dụng dịch vụ AWS không đồng nghĩa với việc toàn bộ vấn đề bảo mật đã được nhà cung cấp xử lý. Người dùng vẫn cần cấu hình và vận hành tài nguyên đúng cách.

#### 3. Thực hành khởi tạo máy chủ ảo Amazon EC2

Em thực hành khởi tạo một máy chủ ảo bằng dịch vụ **Amazon EC2** trên AWS Management Console. Các bước chính bao gồm:

* Lựa chọn Amazon Machine Image (AMI) phù hợp làm hệ điều hành cho máy chủ.
* Chọn loại phiên bản EC2 và cấu hình tài nguyên cơ bản theo nhu cầu của bài lab.
* Thiết lập cặp khóa để xác thực khi kết nối đến máy chủ.
* Cấu hình thông tin mạng và kiểm tra các tùy chọn trước khi khởi chạy phiên bản.
* Kiểm tra trạng thái hoạt động của phiên bản sau khi khởi tạo và tìm hiểu các thông tin như địa chỉ IP, trạng thái và nhóm bảo mật.

#### 4. Cấu hình VPC, Subnet và Security Group

Trong quá trình thực hành, em tìm hiểu mối quan hệ giữa các thành phần mạng cơ bản trên AWS:

* **Amazon VPC:** mạng ảo riêng biệt dùng để triển khai và kiểm soát các tài nguyên AWS.
* **Subnet:** phân vùng mạng nằm trong một VPC, được tạo trong một Availability Zone cụ thể để tổ chức tài nguyên.
* **Security Group:** tường lửa ảo ở cấp độ phiên bản EC2, dùng để kiểm soát lưu lượng truy cập vào và ra thông qua các quy tắc được cấu hình.

Em thực hành lựa chọn VPC và Subnet khi khởi tạo EC2, đồng thời cấu hình Security Group với các quy tắc truy cập cần thiết cho bài lab. Qua đó, em hiểu được tầm quan trọng của việc chỉ mở đúng cổng, giao thức và nguồn truy cập cần thiết, tránh cấp quyền mạng rộng hơn yêu cầu.

### Kết quả đạt được tuần 2

* Hiểu các khái niệm cơ bản của Cloud Computing, các mô hình dịch vụ IaaS, PaaS và SaaS.
* Nắm được nguyên tắc phân chia trách nhiệm bảo mật giữa AWS và khách hàng theo mô hình Shared Responsibility.
* Hoàn thành các bước cơ bản để khởi tạo một máy chủ ảo Amazon EC2.
* Hiểu vai trò và mối quan hệ giữa VPC, Subnet và Security Group trong kiến trúc mạng AWS.
* Thực hành cấu hình quy tắc Security Group theo nhu cầu truy cập của bài lab và nhận thức được tầm quan trọng của nguyên tắc cấp quyền tối thiểu.
* Có nền tảng để tiếp tục học về thiết kế mạng, bảo mật và triển khai ứng dụng trên AWS trong các tuần tiếp theo.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [AWS Cloud Journey](https://cloudjourney.awsstudygroup.com/)


