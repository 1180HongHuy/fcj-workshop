---
title: "Các bài blogs đã đăng"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{% notice warning %}}  
⚠️ **Lưu ý:** Các thông tin dưới đây chỉ nhằm mục đích tham khảo, vui lòng **không sao chép nguyên văn** cho bài báo cáo của bạn kể cả warning này.
{{% /notice %}}

Tại đây sẽ là phần liệt kê, giới thiệu các blogs mà các bạn đã đăng trên [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj).

### [Blog 1: Xây dựng Hệ thống Đặt Tour Du Lịch Ứng dụng Kiến trúc Serverless trên AWS](3.1-Blog1/)
Bài viết này trình bày giải pháp xây dựng hệ thống đặt tour du lịch trực tuyến áp dụng hoàn toàn mô hình Cloud-Native Serverless trên nền tảng AWS nhằm tối ưu hóa chi phí và khả năng tự động mở rộng. Hệ thống được phân tách rõ ràng thành các tầng độc lập bao gồm tầng mạng và bảo mật (Route 53, WAF), tầng frontend (CloudFront, S3), tầng xác thực và API (Cognito, API Gateway), cùng tầng xử lý và dữ liệu (Lambda, DynamoDB, CloudWatch). Bài viết cũng làm nổi bật luồng hoạt động khép kín từ giao diện người dùng, quy trình xác thực token đến khâu xử lý nghiệp vụ và lưu trữ dữ liệu thời gian thực.


### [note-bài Blog 2 đã đăng mà chưa được duyệt]
###  [Blog 2: AWS Lambda (Serverless) – Khi nào nên dùng và làm sao để tối ưu hiệu năng tối đa?](3.2-Blog2/)
Bài viết này chia sẻ các trường hợp sử dụng chuẩn bài cho AWS Lambda như xử lý sự kiện thời gian thực, xây dựng RESTful API hay tự động hóa tác vụ hệ thống. Đồng thời, bài viết cung cấp các bí quyết thiết thực để tối ưu hiệu năng, giảm độ trễ và tiết kiệm chi phí, bao gồm kỹ thuật tái sử dụng kết nối database ở phạm vi global scope, tối ưu dung lượng package, cấu hình RAM linh hoạt để tăng vCPU và kết hợp Amazon RDS Proxy để quản lý connection pooling hiệu quả.

### [note-bài Blog 3 đã đăng mà chưa được duyệt]
###  [Blog 3: Khám phá và Tối ưu Quản lý Dữ liệu Quy mô Lớn với Amazon S3 Metadata](3.3-Blog3/)
Bài viết này chia sẻ bài toán thực tế về việc tìm kiếm và quản lý hàng tỷ object trên Amazon S3 khi các phương pháp truyền thống như dùng API ListObjectsV2 hay tự xây dựng pipeline đồng bộ sang DynamoDB/Elasticsearch tỏ ra phức tạp và tốn kém chi phí. Đồng thời, bài viết làm nổi bật cách Amazon S3 Metadata giải quyết triệt để bài toán này, giúp doanh nghiệp dễ dàng truy vấn các thuộc tính của object (như kích thước, thời gian truy cập, tags, storage class) một cách nhanh chóng, qua đó tiết kiệm thời gian phát triển và tập trung tối đa vào giá trị phân tích dữ liệu.