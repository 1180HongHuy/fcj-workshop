---
title: "Worklog Tuần 10"
date: 2026-07-06
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**06/07/2026 - 12/07/2026**

### Mục tiêu tuần 10

* Thực hành xây dựng một bài lab bảo mật nâng cao với nhiều dịch vụ bảo vệ và phát hiện mối đe dọa trên AWS.
* Hiểu cách kết hợp AWS Security Hub, Amazon GuardDuty, Amazon Macie và AWS Network Firewall trong một quy trình bảo mật tổng thể.
* Rèn luyện khả năng thu thập, tổng hợp và xử lý các phát hiện bảo mật từ nhiều nguồn.
* Lên ý tưởng và xây dựng đề cương chi tiết cho một Workshop công nghệ có nội dung rõ ràng, phù hợp với người tham dự.

### Nội dung thực tập

#### 1. Xây dựng bài lab bảo mật nâng cao

Em xây dựng kịch bản bài lab nhằm mô phỏng quy trình bảo vệ tài nguyên và dữ liệu trong môi trường AWS. Bài lab được thiết kế theo hướng kết hợp nhiều lớp kiểm soát: phát hiện mối đe dọa, kiểm tra dữ liệu nhạy cảm, tổng hợp phát hiện và kiểm soát lưu lượng mạng.

Các thành phần chính trong bài lab gồm:

* **Amazon GuardDuty:** phát hiện hoạt động đáng ngờ và các dấu hiệu mối đe dọa trong tài khoản AWS.
* **Amazon Macie:** hỗ trợ phát hiện, phân loại và bảo vệ dữ liệu nhạy cảm được lưu trữ trên Amazon S3.
* **AWS Network Firewall:** kiểm soát và lọc lưu lượng mạng theo các rule được cấu hình.
* **AWS Security Hub:** tổng hợp các phát hiện bảo mật từ nhiều dịch vụ và cung cấp góc nhìn tập trung về trạng thái bảo mật.

#### 2. Tìm hiểu Amazon GuardDuty và Amazon Macie

Em thực hành tìm hiểu cách **Amazon GuardDuty** phân tích các nguồn dữ liệu và tạo security findings khi phát hiện hành vi bất thường. Các findings được xem xét theo mức độ nghiêm trọng, loại mối đe dọa và tài nguyên liên quan để xác định hướng xử lý.

Đối với **Amazon Macie**, em nghiên cứu cách dịch vụ sử dụng cơ chế phát hiện dữ liệu nhạy cảm để hỗ trợ kiểm tra các object trong S3. Nội dung tập trung vào việc xác định loại dữ liệu cần bảo vệ, xem kết quả phát hiện và đánh giá rủi ro khi dữ liệu được chia sẻ hoặc cấu hình quyền truy cập không phù hợp.

Qua hai dịch vụ, em hiểu thêm sự khác nhau giữa phát hiện mối đe dọa hoạt động và phát hiện rủi ro liên quan đến dữ liệu. GuardDuty tập trung vào hành vi, sự kiện và mối đe dọa; Macie tập trung vào dữ liệu nhạy cảm và cấu hình bảo vệ dữ liệu.

#### 3. Cấu hình AWS Network Firewall

Em tìm hiểu **AWS Network Firewall** trong vai trò kiểm soát lưu lượng giữa các vùng mạng và bảo vệ tài nguyên khỏi các kết nối không được phép. Bài lab tập trung vào việc xác định luồng lưu lượng cần cho phép, luồng cần chặn và cách áp dụng rule theo nhu cầu bảo mật.

Các nội dung thực hành gồm:

* Xác định vị trí của Network Firewall trong kiến trúc VPC.
* Tìm hiểu stateful và stateless rule trong quá trình xử lý lưu lượng.
* Xây dựng rule theo giao thức, địa chỉ, port và hướng kết nối.
* Kiểm tra luồng truy cập hợp lệ và luồng bị chặn sau khi áp dụng chính sách.
* Đối chiếu kết quả với log hoặc finding để hỗ trợ phân tích sự cố.

Em nhận thấy rule firewall cần được thiết kế rõ ràng, giới hạn đúng phạm vi và kiểm thử trước khi áp dụng rộng rãi để tránh chặn nhầm lưu lượng hợp lệ hoặc tạo ra điểm yếu bảo mật.

#### 4. Tổng hợp phát hiện với AWS Security Hub

Em cấu hình và tìm hiểu **AWS Security Hub** như một nơi tổng hợp security findings từ GuardDuty, Macie và các nguồn bảo mật khác. Security Hub giúp chuẩn hóa, sắp xếp và hiển thị findings để người quản trị có thể ưu tiên xử lý theo mức độ ảnh hưởng.

Các bước chính gồm:

* Kích hoạt và kiểm tra trạng thái của Security Hub trong môi trường thực hành.
* Xem các findings được gửi từ những dịch vụ bảo mật đã cấu hình.
* Phân loại findings theo mức độ nghiêm trọng, loại kiểm soát và tài nguyên bị ảnh hưởng.
* Tìm hiểu cách liên kết finding với quy trình điều tra và khắc phục.
* Kiểm tra trạng thái finding sau khi xử lý và ghi nhận kết quả.

Việc tập trung findings giúp giảm việc kiểm tra rời rạc từng dịch vụ, đồng thời hỗ trợ xây dựng quy trình phản ứng sự cố có thứ tự ưu tiên rõ ràng.

#### 5. Lên ý tưởng và xây dựng đề cương Workshop công nghệ

Song song với bài lab, em lên ý tưởng và xây dựng đề cương chi tiết cho một **Workshop công nghệ**. Chủ đề được định hướng theo nhu cầu thực tế của người học, có sự kết hợp giữa phần lý thuyết ngắn gọn và các bước thực hành có thể kiểm chứng.

Đề cương Workshop được xây dựng với các phần chính:

* Xác định chủ đề, mục tiêu và đối tượng tham dự.
* Mô tả kiến thức nền tảng cần chuẩn bị trước Workshop.
* Phân chia nội dung thành các phần: giới thiệu, trình diễn, thực hành và tổng kết.
* Sắp xếp thời lượng cho từng hoạt động, bao gồm thời gian hỗ trợ và xử lý lỗi.
* Chuẩn bị danh sách tài nguyên, tài khoản, quyền IAM và môi trường cần thiết.
* Xây dựng kết quả đầu ra để người tham dự có thể tự kiểm tra sau khi hoàn thành.
* Dự kiến các lỗi thường gặp và phương án hỗ trợ trong quá trình thực hành.

Việc xây dựng đề cương giúp em rèn luyện khả năng trình bày kiến thức theo trình tự, dự đoán khó khăn của người học và chuẩn bị nội dung kỹ thuật dễ theo dõi hơn.

### Kết quả đạt được tuần 10

* Hoàn thành kịch bản cơ bản cho bài lab bảo mật nâng cao kết hợp Security Hub, GuardDuty, Macie và Network Firewall.
* Hiểu vai trò của từng dịch vụ trong quy trình phát hiện mối đe dọa, bảo vệ dữ liệu, kiểm soát mạng và tổng hợp findings.
* Thực hành xem xét mức độ nghiêm trọng, tài nguyên ảnh hưởng và trạng thái xử lý của các security findings.
* Nắm được cách thiết kế rule kiểm soát lưu lượng và kiểm tra kết quả sau khi cấu hình Network Firewall.
* Xây dựng được ý tưởng, mục tiêu, nội dung, thời lượng và quy trình hỗ trợ cho Workshop công nghệ.
* Chuẩn bị được đề cương chi tiết có phần lý thuyết, demo, thực hành, kiểm tra kết quả và xử lý sự cố.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [AWS Security Hub User Guide](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html)
* [Amazon GuardDuty User Guide](https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html)
* [Amazon Macie User Guide](https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html)
* [AWS Network Firewall Developer Guide](https://docs.aws.amazon.com/network-firewall/latest/developerguide/what-is-aws-network-firewall.html)




