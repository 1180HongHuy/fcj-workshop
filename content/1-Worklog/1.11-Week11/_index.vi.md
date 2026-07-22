---
title: "Worklog Tuần 11"
date: 2026-07-13
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}}
⚠️ **Cảnh báo:** Toàn bộ nội dung bên dưới chỉ dùng làm tài liệu định hướng tham khảo; tuyệt đối **không được sao chép y nguyên** vào bài báo cáo cá nhân của bạn.
{{% /notice %}}

### Thời gian thực tập

**13/07/2026 - 19/07/2026**

### Mục tiêu tuần 11

* Hoàn thiện kịch bản demo cho đề tài Workshop tổng kết theo trình tự rõ ràng và dễ thực hiện.
* Hoàn chỉnh tài liệu kỹ thuật mô tả kiến trúc, các bước triển khai và cách kiểm tra hệ thống.
* Deploy phiên bản website hoàn chỉnh lên môi trường production bằng quy trình tự động hóa.
* Kiểm tra tính ổn định của phiên bản production và bảo đảm quy trình phát hành có thể lặp lại.

### Nội dung thực tập

#### 1. Hoàn thiện kịch bản demo Workshop tổng kết

Em rà soát lại toàn bộ nội dung của đề tài và xây dựng kịch bản demo cho Workshop tổng kết. Kịch bản được sắp xếp theo trình tự từ giới thiệu mục tiêu, trình bày kiến trúc, minh họa luồng hoạt động đến kiểm tra kết quả.

Các nội dung được hoàn thiện gồm:

* Giới thiệu bối cảnh, mục tiêu và các chức năng chính của ứng dụng.
* Trình bày kiến trúc tổng thể và vai trò của các dịch vụ AWS được sử dụng.
* Chuẩn bị dữ liệu, tài khoản và môi trường cần thiết trước khi bắt đầu demo.
* Xây dựng các bước thao tác theo thứ tự để người trình bày có thể thực hiện ổn định.
* Bổ sung các điểm kiểm tra để xác nhận kết quả sau mỗi phần trình diễn.
* Chuẩn bị phương án xử lý một số lỗi có thể xảy ra trong lúc demo.

Việc chuẩn hóa kịch bản giúp thời lượng trình bày được kiểm soát tốt hơn, hạn chế thao tác thừa và giúp người tham dự dễ theo dõi mối liên hệ giữa các thành phần của hệ thống.

#### 2. Hoàn thiện tài liệu kỹ thuật

Em xây dựng và cập nhật bộ tài liệu kỹ thuật đi kèm với đề tài Workshop. Tài liệu được trình bày theo hướng có thể sử dụng để chuẩn bị môi trường, triển khai, kiểm thử và xử lý các vấn đề cơ bản.

Các phần chính của tài liệu gồm:

* Mô tả kiến trúc hệ thống, các thành phần chính và luồng dữ liệu.
* Danh sách điều kiện tiên quyết, công cụ, tài khoản và quyền IAM cần thiết.
* Hướng dẫn cấu hình môi trường và các biến cấu hình của ứng dụng.
* Các bước build, deploy và kiểm tra phiên bản sau khi phát hành.
* Mô tả quy trình giám sát, kiểm tra log và xác định lỗi.
* Danh sách lỗi thường gặp cùng hướng xử lý hoặc bước kiểm tra tương ứng.
* Hướng dẫn dọn dẹp tài nguyên và lưu ý về bảo mật, chi phí.

Em rà soát lại nội dung để bảo đảm các câu lệnh, đường dẫn, tên tài nguyên và thứ tự thao tác trong tài liệu thống nhất với môi trường thực tế.

#### 3. Xây dựng quy trình deploy tự động

Em hoàn thiện quy trình tự động hóa cho việc đưa phiên bản website lên môi trường production. Quy trình được tổ chức thành các bước có thể lặp lại, giúp giảm thao tác thủ công và hạn chế sai sót khi phát hành.

Luồng triển khai gồm:

* Kiểm tra mã nguồn và các cấu hình cần thiết trước khi build.
* Cài đặt dependency và tạo production build của ứng dụng.
* Kiểm tra kết quả build để phát hiện lỗi trước khi triển khai.
* Đưa các tệp build lên môi trường lưu trữ production bằng bước deploy tự động.
* Làm mới cache hoặc thực hiện bước cập nhật phân phối khi cần thiết.
* Kiểm tra trạng thái sau deploy và ghi nhận kết quả của từng bước trong quy trình.

Việc tự động hóa giúp quy trình phát hành nhất quán hơn giữa các lần triển khai. Khi có phiên bản mới, chỉ cần thực hiện đúng các bước đã định nghĩa thay vì thao tác thủ công trên từng tài nguyên.

#### 4. Kiểm tra phiên bản production

Sau khi deploy thành công, em thực hiện kiểm tra website trên môi trường production. Nội dung kiểm tra bao gồm khả năng truy cập trang, tải tài nguyên tĩnh, điều hướng các màn hình và kết nối đến backend/API.

Em cũng kiểm tra các phản hồi lỗi, thời gian tải cơ bản và log liên quan để xác nhận hệ thống hoạt động ổn định. Nếu phát hiện vấn đề, em đối chiếu với bước build, cấu hình môi trường hoặc kết quả deploy để xác định nguyên nhân và cập nhật lại quy trình khi cần.

### Kết quả đạt được tuần 11

* Hoàn thiện kịch bản demo Workshop tổng kết với trình tự trình bày, điểm kiểm tra và phương án xử lý lỗi rõ ràng.
* Hoàn chỉnh tài liệu kỹ thuật về kiến trúc, cấu hình, triển khai, kiểm thử và xử lý sự cố.
* Xây dựng được quy trình build và deploy tự động cho phiên bản website hoàn chỉnh.
* Deploy thành công website lên môi trường production ổn định.
* Kiểm tra được khả năng truy cập, tải tài nguyên, điều hướng và kết nối backend của phiên bản production.
* Giảm các thao tác thủ công và tăng tính nhất quán, khả năng lặp lại của quy trình phát hành.

### Tài liệu tham khảo

* [AWS Documentation](https://docs.aws.amazon.com/)
* [AWS Cloud Journey](https://cloudjourney.awsstudygroup.com/)






