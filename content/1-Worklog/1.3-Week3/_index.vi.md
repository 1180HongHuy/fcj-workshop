---
title: "Worklog Tuần 3"
date: 2026-05-18
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}
### Thời gian thực tập

**18/05/2026 - 24/05/2026**

### Mục tiêu tuần 3

* Khám phá vai trò và cách hoạt động của AWS Lambda trong kiến trúc serverless.
* Tìm hiểu cách sử dụng Amazon API Gateway để tạo và quản lý các API kết nối với Lambda.
* Triển khai một ứng dụng web mẫu lên AWS và kiểm tra khả năng trao đổi dữ liệu giữa giao diện người dùng và backend.
* Thực hành kiểm tra request, response và xử lý các lỗi cơ bản trong quá trình tích hợp dịch vụ.

### Nội dung thực tập

#### 1. Khám phá AWS Lambda

Em tìm hiểu **AWS Lambda** là dịch vụ điện toán không máy chủ, cho phép thực thi mã theo sự kiện mà không cần tự quản lý máy chủ. Nội dung nghiên cứu tập trung vào các khái niệm như function, runtime, handler, event và execution role.

Em thực hành tạo một Lambda function mẫu, cấu hình runtime phù hợp và kiểm tra kết quả bằng các sự kiện thử nghiệm. Qua đó, em hiểu được cách Lambda nhận dữ liệu đầu vào, xử lý logic nghiệp vụ và trả về dữ liệu đầu ra cho thành phần gọi hàm.

#### 2. Khám phá Amazon API Gateway

Em tìm hiểu **Amazon API Gateway** và vai trò của dịch vụ này trong việc cung cấp endpoint để ứng dụng frontend có thể giao tiếp với backend. Các nội dung đã thực hành gồm:

* Tạo một API và cấu hình tài nguyên, route hoặc endpoint tương ứng.
* Thiết lập phương thức HTTP cần thiết, chẳng hạn như `GET` và `POST`.
* Kết nối API Gateway với Lambda function để tiếp nhận và xử lý request.
* Tìm hiểu cách truyền dữ liệu từ request đến Lambda và trả response về cho client.
* Kiểm tra endpoint bằng công cụ test trên AWS Console và theo dõi kết quả phản hồi.

Qua bài thực hành, em hiểu được API Gateway đóng vai trò là lớp trung gian tiếp nhận request từ ứng dụng, định tuyến request đến Lambda và chuyển kết quả xử lý trở lại cho client.

#### 3. Triển khai Demo Web App lên AWS

Em triển khai một **Demo Web App** lên môi trường AWS để kiểm tra tính liên thông giữa frontend, API Gateway và Lambda. Các bước thực hiện chính gồm:

* Chuẩn bị mã nguồn và cấu hình endpoint API cho ứng dụng web mẫu.
* Triển khai phần giao diện web lên môi trường lưu trữ phù hợp trên AWS.
* Cấu hình frontend gọi đến endpoint do API Gateway cung cấp.
* Kết nối API Gateway với Lambda function xử lý logic backend.
* Gửi các request từ giao diện web và kiểm tra dữ liệu trả về từ backend.

#### 4. Kiểm tra tính liên thông dữ liệu

Em thực hiện kiểm thử luồng dữ liệu theo trình tự: người dùng thao tác trên frontend, frontend gửi request đến API Gateway, API Gateway chuyển request đến Lambda, sau đó kết quả được trả ngược về giao diện.

Trong quá trình kiểm tra, em đối chiếu nội dung request và response, xác nhận endpoint được gọi đúng, kiểm tra mã trạng thái HTTP và quan sát kết quả hiển thị trên Demo Web App. Một số lỗi cấu hình cơ bản như sai endpoint, sai phương thức HTTP hoặc định dạng dữ liệu không phù hợp cũng được rà soát để đảm bảo các thành phần hoạt động liên thông.

### Kết quả đạt được tuần 3

* Hiểu được mô hình hoạt động và các thành phần cơ bản của AWS Lambda.
* Tạo và kiểm tra thành công Lambda function mẫu với dữ liệu đầu vào và đầu ra xác định.
* Nắm được vai trò của Amazon API Gateway trong việc cung cấp endpoint và kết nối frontend với backend serverless.
* Hoàn thành triển khai Demo Web App lên AWS và cấu hình ứng dụng gọi API.
* Kiểm tra được luồng trao đổi dữ liệu giữa frontend, API Gateway và Lambda thông qua request và response thực tế.
* Có thêm kinh nghiệm phát hiện và xử lý các lỗi cấu hình cơ bản trong quá trình tích hợp các dịch vụ AWS.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [AWS Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
* [Amazon API Gateway Developer Guide](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html)



