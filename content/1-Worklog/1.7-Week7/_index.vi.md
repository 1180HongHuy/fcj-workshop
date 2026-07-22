---
title: "Worklog Tuần 7"
date: 2026-06-15
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**15/06/2026 - 21/06/2026**

### Mục tiêu tuần 7

* Triển khai một ứng dụng web tĩnh viết bằng ReactJS theo mô hình Single Page Application (SPA) lên Amazon S3.
* Tìm hiểu cách cấu hình S3 để lưu trữ và phân phối các tệp frontend đã được build.
* Sử dụng Amazon CloudFront (CDN) để phân phối nội dung nhanh hơn đến người dùng ở nhiều khu vực.
* Cấu hình HTTPS/SSL và các thiết lập bảo mật cần thiết cho website.

### Nội dung thực tập

#### 1. Chuẩn bị và build ReactJS Single Page Application

Em chuẩn bị mã nguồn frontend của ứng dụng ReactJS và kiểm tra cấu hình trước khi triển khai. Ứng dụng được xây dựng theo mô hình **Single Page Application (SPA)**, trong đó phần lớn nội dung được tải và điều hướng ở phía trình duyệt.

Các bước chuẩn bị gồm:

* Kiểm tra cấu hình môi trường và các biến dùng trong quá trình build.
* Cấu hình đúng địa chỉ endpoint API để frontend có thể giao tiếp với backend sau khi triển khai.
* Chạy lệnh build để tạo các tệp tĩnh gồm HTML, JavaScript, CSS và tài nguyên hình ảnh.
* Kiểm tra thư mục build và xác nhận ứng dụng có thể tải đúng các tài nguyên cần thiết.

Việc build trước khi tải lên S3 giúp tối ưu kích thước mã nguồn, giảm tài nguyên không cần thiết và tạo ra phiên bản sẵn sàng để phân phối trên môi trường production.

#### 2. Triển khai website tĩnh lên Amazon S3

Em tạo và cấu hình một **Amazon S3 bucket** để lưu trữ các tệp tĩnh của ReactJS SPA. Các nội dung thực hành bao gồm:

* Tạo bucket với tên và Region phù hợp.
* Tải các tệp trong thư mục build lên bucket, đồng thời giữ nguyên cấu trúc thư mục của ứng dụng.
* Thiết lập tài liệu index để S3 biết tệp được phục vụ khi người dùng truy cập website.
* Kiểm tra việc tải các tệp HTML, CSS, JavaScript và hình ảnh từ bucket.
* Tìm hiểu cách cấu hình quyền truy cập để hạn chế việc công khai dữ liệu ngoài phạm vi cần thiết.

Đối với ứng dụng SPA, em cũng lưu ý vấn đề điều hướng bằng client-side routing. Khi người dùng truy cập trực tiếp một đường dẫn con, máy chủ cần được cấu hình để trả về tệp entry point của ứng dụng thay vì báo lỗi không tìm thấy tài nguyên.

#### 3. Cấu hình Amazon CloudFront để phân phối nội dung

Em tạo một **Amazon CloudFront distribution** với S3 làm origin để phân phối nội dung website qua mạng CDN. CloudFront giúp đưa nội dung đến các edge location gần người dùng hơn, từ đó giảm độ trễ và cải thiện tốc độ tải trang.

Các nội dung thực hành gồm:

* Chọn S3 bucket làm origin cho CloudFront distribution.
* Tìm hiểu cơ chế cache và thời gian lưu nội dung tại edge location.
* Cấu hình các tùy chọn truy cập, phương thức HTTP và hành vi cache phù hợp với website tĩnh.
* Thiết lập trang mặc định và xử lý phản hồi lỗi để hỗ trợ hoạt động điều hướng của SPA.
* Tạo invalidation khi cần làm mới nội dung đã được cache sau mỗi lần cập nhật phiên bản frontend.

Em hiểu rằng cần cân bằng giữa hiệu năng cache và tốc độ cập nhật nội dung. Thời gian cache dài giúp giảm số request về origin, nhưng khi phát hành bản build mới có thể cần invalidation để người dùng nhận được tệp mới.

#### 4. Cấu hình SSL và bảo mật website

Em tìm hiểu và thực hành cấu hình bảo mật cho website thông qua CloudFront. Nội dung chính gồm:

* Sử dụng chứng chỉ SSL/TLS phù hợp để cho phép người dùng truy cập website qua HTTPS.
* Cấu hình viewer protocol policy để chuyển hướng hoặc yêu cầu các request sử dụng HTTPS.
* Tìm hiểu cách giới hạn quyền truy cập origin S3, ưu tiên cho người dùng truy cập nội dung thông qua CloudFront thay vì truy cập trực tiếp bucket.
* Kiểm tra domain, chứng chỉ và trạng thái distribution sau khi cấu hình.
* Xác nhận website tải được tài nguyên an toàn và không phát sinh lỗi do nội dung hỗn hợp HTTP/HTTPS.

Các thiết lập này giúp bảo vệ dữ liệu truyền giữa trình duyệt và hệ thống, đồng thời hạn chế việc truy cập trực tiếp vào nguồn lưu trữ gốc.

#### 5. Kiểm tra hiệu năng và tính liên thông

Sau khi triển khai, em truy cập website thông qua domain của CloudFront và kiểm tra các chức năng chính của ứng dụng. Em đối chiếu thời gian tải trang, trạng thái phản hồi, việc tải tài nguyên tĩnh và khả năng gọi API từ frontend.

Em cũng kiểm tra lại website sau khi cập nhật một phiên bản build mới để xác nhận quy trình upload, cache invalidation và phân phối nội dung hoạt động đúng.

### Kết quả đạt được tuần 7

* Hoàn thành quy trình build và triển khai ứng dụng ReactJS Single Page Application lên Amazon S3.
* Hiểu cách cấu hình S3 bucket để lưu trữ và phục vụ các tài nguyên website tĩnh.
* Tạo và cấu hình CloudFront distribution sử dụng S3 làm origin để phân phối nội dung qua CDN.
* Nắm được vai trò của cache, edge location và invalidation trong việc tối ưu tốc độ tải website.
* Cấu hình truy cập HTTPS/SSL và tìm hiểu cách bảo vệ S3 origin khỏi truy cập không cần thiết.
* Kiểm tra thành công việc tải website, tải tài nguyên tĩnh và kết nối frontend với backend sau khi triển khai.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon S3 Static Website Hosting](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)
* [Amazon CloudFront Developer Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)





