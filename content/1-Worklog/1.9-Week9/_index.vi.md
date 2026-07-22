---
title: "Worklog Tuần 9"
date: 2026-06-29
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**29/06/2026 - 05/07/2026**

### Mục tiêu tuần 9

* Tìm hiểu chuyên sâu cách giới hạn quyền IAM bằng IAM Permission Boundaries.
* Giám sát và phân tích lưu lượng mạng thông qua VPC Flow Logs.
* Xây dựng kế hoạch sao lưu tự động cho Amazon EBS bằng AWS Backup.
* Tham gia hỗ trợ kỹ thuật cho sự kiện **First Cloud Security Journey**.

### Nội dung thực tập

#### 1. Quản lý giới hạn quyền với IAM Permission Boundaries

Em nghiên cứu **IAM Permission Boundaries**, một cơ chế dùng để đặt giới hạn tối đa cho các quyền mà IAM user hoặc IAM role có thể nhận được. Permission boundary không tự động cấp quyền, mà xác định phạm vi quyền tối đa được phép sử dụng khi kết hợp với identity-based policy.

Các nội dung tìm hiểu và thực hành gồm:

* Phân biệt permission boundary với identity-based policy và resource-based policy.
* Tạo policy làm permission boundary cho IAM user hoặc role.
* Giới hạn các thao tác và tài nguyên mà danh tính IAM có thể truy cập.
* Kiểm tra trường hợp policy cấp quyền rộng nhưng permission boundary vẫn ngăn không cho thực hiện thao tác vượt quá phạm vi.
* Tìm hiểu cách sử dụng boundary để kiểm soát việc tự cấp thêm quyền hoặc tạo role mới trong môi trường AWS.

Qua hoạt động này, em hiểu rằng permission boundary hỗ trợ triển khai mô hình phân quyền nhiều lớp. Ngay cả khi một policy cấp quyền rộng hơn dự kiến, danh tính IAM vẫn bị giới hạn bởi phạm vi tối đa được định nghĩa trong boundary.

#### 2. Giám sát lưu lượng mạng bằng VPC Flow Logs

Em tìm hiểu **VPC Flow Logs**, tính năng ghi lại thông tin về lưu lượng IP đi qua các network interface trong VPC. Dữ liệu flow log có thể hỗ trợ phân tích kết nối, kiểm tra truy cập và điều tra các vấn đề liên quan đến mạng.

Các bước thực hiện gồm:

* Xác định phạm vi cần ghi log ở cấp độ VPC, Subnet hoặc network interface.
* Cấu hình đích lưu trữ log phù hợp, chẳng hạn như CloudWatch Logs.
* Tìm hiểu các trường thông tin trong flow log như source, destination, protocol, port, action và trạng thái chấp nhận hoặc từ chối.
* Lọc các bản ghi `ACCEPT` và `REJECT` để kiểm tra lưu lượng hợp lệ hoặc bị chặn.
* Đối chiếu flow log với Security Group, Network ACL và cấu hình route để tìm nguyên nhân khi kết nối không thành công.

VPC Flow Logs không ghi lại nội dung gói tin, nhưng cung cấp thông tin cần thiết để nhận biết nguồn, đích, hướng lưu lượng và kết quả xử lý. Đây là dữ liệu hữu ích cho việc giám sát và phân tích bảo mật mạng.

#### 3. Xây dựng kế hoạch sao lưu Amazon EBS với AWS Backup

Em nghiên cứu **AWS Backup** và thực hành xây dựng kế hoạch sao lưu tự động cho các EBS volume. Kế hoạch sao lưu giúp chuẩn hóa lịch chạy, thời gian lưu giữ và phạm vi tài nguyên được bảo vệ.

Các nội dung chính gồm:

* Tạo backup vault để lưu trữ các recovery point.
* Tạo backup plan với lịch sao lưu định kỳ phù hợp.
* Cấu hình lifecycle và thời gian retention cho bản sao lưu.
* Gán tài nguyên EBS vào kế hoạch bằng tag hoặc lựa chọn tài nguyên phù hợp.
* Kiểm tra job sao lưu, trạng thái hoàn thành và recovery point được tạo ra.
* Tìm hiểu quy trình khôi phục từ bản sao lưu để tạo lại volume khi cần thiết.

Trong quá trình thực hành, em chú ý lựa chọn lịch và thời gian lưu giữ phù hợp với nhu cầu khôi phục cũng như chi phí. Việc kiểm tra định kỳ backup job và thực hành khôi phục là cần thiết để bảo đảm bản sao lưu có thể sử dụng khi xảy ra sự cố.

#### 4. Hỗ trợ kỹ thuật sự kiện First Cloud Security Journey

Em tham gia hỗ trợ kỹ thuật cho sự kiện **First Cloud Security Journey**. Công việc tập trung vào việc hỗ trợ người tham dự trong quá trình truy cập tài liệu, chuẩn bị môi trường thực hành và xử lý các vấn đề cơ bản liên quan đến tài khoản hoặc dịch vụ AWS.

Các hoạt động hỗ trợ gồm:

* Hướng dẫn người tham dự kiểm tra điều kiện cần thiết trước khi bắt đầu bài thực hành.
* Hỗ trợ xác định các lỗi thường gặp về quyền IAM, Region, cấu hình mạng hoặc tài nguyên chưa sẵn sàng.
* Ghi nhận câu hỏi, phân loại vấn đề và phối hợp với các thành viên phụ trách để xử lý.
* Hướng dẫn kiểm tra kết quả sau mỗi bước và nhắc nhở người tham dự dọn dẹp tài nguyên sau khi hoàn thành.
* Theo dõi tiến độ chung và hỗ trợ duy trì trải nghiệm thực hành ổn định cho người tham dự.

Hoạt động này giúp em rèn luyện kỹ năng giao tiếp kỹ thuật, phân tích sự cố theo trình tự và trình bày giải pháp rõ ràng cho người có mức độ kinh nghiệm khác nhau.

### Kết quả đạt được tuần 9

* Hiểu được vai trò của IAM Permission Boundaries trong việc đặt giới hạn quyền tối đa cho IAM user và role.
* Thực hành phân quyền nhiều lớp và kiểm tra hiệu lực của boundary khi policy cấp quyền rộng hơn phạm vi cho phép.
* Nắm được cách cấu hình VPC Flow Logs để ghi nhận và phân tích lưu lượng mạng.
* Biết cách sử dụng các trường thông tin trong flow log để kiểm tra kết nối và các request bị chấp nhận hoặc từ chối.
* Xây dựng được backup plan tự động cho EBS bằng AWS Backup, bao gồm lịch chạy, retention và recovery point.
* Hiểu quy trình kiểm tra backup job và khôi phục tài nguyên từ bản sao lưu.
* Hoàn thành vai trò hỗ trợ kỹ thuật cho sự kiện First Cloud Security Journey và cải thiện kỹ năng xử lý sự cố, hướng dẫn người dùng.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [IAM Permissions Boundaries](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html)
* [VPC Flow Logs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html)
* [AWS Backup User Guide](https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html)




