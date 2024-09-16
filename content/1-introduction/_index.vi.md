+++
title = "Giới thiệu"
date = 2020-05-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

### Quy trình hoạt động

**1. Người dùng truy cập ứng dụng thông qua trình duyệt web**

- Khi người dùng muốn truy cập ứng dụng, họ sẽ nhập địa chỉ URL của trang web trong trình duyệt. Đây có thể là một trang web cung cấp nội dung tĩnh (HTML, CSS, JavaScript) hoặc các tính năng tương tác như đăng nhập, đăng ký, hoặc thao tác với dữ liệu. Yêu cầu truy cập này sẽ được trình duyệt gửi qua Internet đến hệ thống AWS để xử lý.

**2. Route 53 phân giải tên miền và điều hướng yêu cầu**

- Đầu tiên, yêu cầu từ trình duyệt sẽ được gửi đến Amazon Route 53, dịch vụ DNS (Domain Name System) của AWS. Nhiệm vụ của Route 53 là phân giải tên miền của ứng dụng thành địa chỉ IP cụ thể, giúp định tuyến lưu lượng truy cập đến đúng tài nguyên của hệ thống trên AWS. Route 53 có thể được cấu hình để hỗ trợ cân bằng tải giữa nhiều máy chủ hoặc vùng địa lý khác nhau nhằm tối ưu hóa tốc độ truy cập và đảm bảo khả dụng cao.

- Sau khi phân giải thành công, yêu cầu của người dùng sẽ được chuyển tiếp đến CloudFront, hệ thống phân phối nội dung (CDN) của AWS.

**3. CloudFront nhận yêu cầu và kiểm tra cache**

- Amazon CloudFront đóng vai trò là một Content Delivery Network (CDN), phân phối nội dung từ các edge location (các điểm mạng gần người dùng nhất) để giảm độ trễ và tăng hiệu suất cho trang web.

- Khi CloudFront nhận được yêu cầu từ người dùng, nó sẽ kiểm tra xem tài nguyên tĩnh (như các tệp HTML, CSS, JavaScript, hình ảnh) có sẵn trong bộ nhớ đệm (cache) của edge location gần người dùng không. Nếu tài nguyên đã có sẵn trong cache, CloudFront sẽ gửi trả lại ngay lập tức mà không cần truy cập vào máy chủ backend, giúp giảm thời gian phản hồi.

- Nếu tài nguyên không có trong cache, CloudFront sẽ lấy các tệp tĩnh từ Amazon S3, nơi lưu trữ chính cho các nội dung tĩnh của ứng dụng, và gửi về cho người dùng.

**4. Amazon S3 cung cấp nội dung tĩnh cho CloudFront**

- Amazon S3 (Simple Storage Service) được sử dụng để lưu trữ các tệp tĩnh của ứng dụng như hình ảnh, video, CSS, và JavaScript. Đây là một dịch vụ lưu trữ với khả năng mở rộng và độ bền dữ liệu cao. Khi CloudFront không tìm thấy tài nguyên trong cache, nó sẽ yêu cầu S3 để lấy tài nguyên tĩnh và lưu trữ tạm thời (cache) cho các lần truy cập sau.

**5. Web Application Firewall (WAF) bảo vệ hệ thống**

- AWS WAF (Web Application Firewall) là tường lửa ứng dụng web được tích hợp với CloudFront để bảo vệ hệ thống khỏi các cuộc tấn công phổ biến, chẳng hạn như SQL Injection, Cross-Site Scripting (XSS), và DDoS (tấn công từ chối dịch vụ).

- WAF có thể được cấu hình với các quy tắc bảo mật cụ thể để kiểm tra và chặn các yêu cầu độc hại từ người dùng trước khi chúng có thể ảnh hưởng đến ứng dụng. Điều này giúp bảo vệ hệ thống khỏi các lỗ hổng bảo mật phổ biến.

**6. Certificate Manager quản lý chứng chỉ SSL để mã hóa dữ liệu**

- Amazon Certificate Manager (ACM) quản lý chứng chỉ SSL/TLS cho hệ thống, giúp đảm bảo rằng tất cả các giao tiếp giữa người dùng và hệ thống đều được mã hóa, bảo vệ thông tin khỏi các cuộc tấn công giữa chừng (man-in-the-middle).

- Certificate Manager tự động quản lý và gia hạn chứng chỉ SSL để đảm bảo rằng các kết nối an toàn luôn hoạt động bình thường. Việc này đặc biệt quan trọng trong môi trường yêu cầu bảo mật dữ liệu cao.

**7. Người dùng xác thực qua Cognito User Pool**

- Đối với các yêu cầu cần xác thực (ví dụ: đăng nhập, đăng ký), người dùng sẽ tương tác với Amazon Cognito User Pool, một dịch vụ quản lý danh tính người dùng.

- Cognito cho phép người dùng đăng nhập hoặc đăng ký tài khoản trên ứng dụng. Khi người dùng cung cấp thông tin đăng nhập (email, mật khẩu), Cognito sẽ xác thực thông tin đó và cấp phát các JWT token để chứng thực cho các yêu cầu tiếp theo từ phía người dùng.

- Ngoài ra, Cognito hỗ trợ xác thực đa yếu tố (MFA) và tích hợp với các dịch vụ bên ngoài như Facebook, Google để giúp người dùng đăng nhập một cách thuận tiện.

**8. API Gateway xử lý các yêu cầu động từ người dùng**

- Đối với các yêu cầu phức tạp như lấy dữ liệu từ cơ sở dữ liệu hoặc xử lý các tác vụ backend, yêu cầu của người dùng sẽ được gửi từ trình duyệt qua API Gateway.

- Amazon API Gateway hoạt động như một cổng kết nối giữa người dùng và các dịch vụ backend. Nó tiếp nhận các yêu cầu HTTP(S) và chuyển tiếp chúng đến AWS Lambda để xử lý. API Gateway có thể tích hợp với Cognito để kiểm tra token xác thực từ người dùng trước khi cho phép truy cập vào các tài nguyên nhạy cảm.

- Ngoài ra, API Gateway hỗ trợ việc quản lý phiên bản API, áp dụng giới hạn lưu lượng (throttling), và giám sát các yêu cầu để đảm bảo hiệu suất và bảo mật.

**9. Lambda thực thi logic nghiệp vụ**

- AWS Lambda là dịch vụ tính toán serverless, chỉ hoạt động khi có sự kiện. Khi API Gateway chuyển tiếp yêu cầu từ người dùng, Lambda sẽ thực thi logic nghiệp vụ của ứng dụng mà không cần quản lý máy chủ.

- Lambda có thể thực hiện nhiều tác vụ khác nhau, chẳng hạn như xử lý thông tin đăng nhập, truy xuất dữ liệu từ cơ sở dữ liệu, hoặc gọi các dịch vụ khác để xử lý công việc phức tạp. Lambda tự động mở rộng quy mô để đáp ứng lượng yêu cầu lớn và chỉ tính phí dựa trên thời gian thực thi, giúp tiết kiệm chi phí cho hệ thống.

**10. DynamoDB lưu trữ và truy xuất dữ liệu động**

- Amazon DynamoDB là cơ sở dữ liệu NoSQL có khả năng mở rộng linh hoạt. Khi Lambda cần truy xuất hoặc ghi dữ liệu, nó sẽ tương tác với DynamoDB.

- DynamoDB lưu trữ dữ liệu động của ứng dụng, ví dụ như thông tin người dùng, trạng thái giao dịch, hay dữ liệu liên quan đến ứng dụng. DynamoDB hỗ trợ tốc độ đọc/ghi rất nhanh và có khả năng xử lý lượng dữ liệu lớn, giúp hệ thống luôn hoạt động mượt mà ngay cả khi có nhiều người dùng truy cập đồng thời.

**11. SNS gửi thông báo**

- Khi có sự kiện quan trọng hoặc thay đổi trạng thái trong ứng dụng (ví dụ: một người dùng mới đăng ký hoặc có đơn hàng mới), Lambda có thể kích hoạt Amazon SNS (Simple Notification Service) để gửi thông báo.

- SNS có thể gửi thông báo qua nhiều kênh khác nhau như email, tin nhắn SMS, hoặc các hệ thống khác sử dụng cơ chế pub/sub. Điều này giúp ứng dụng cung cấp thông tin nhanh chóng và chính xác tới người dùng hoặc quản trị viên.

**12. Người dùng nhận phản hồi**

- Sau khi các yêu cầu được xử lý bởi Lambda và dữ liệu đã được lấy từ DynamoDB hoặc các nguồn khác, API Gateway sẽ nhận phản hồi từ Lambda và chuyển tiếp kết quả đó về cho trình duyệt của người dùng.

- Người dùng cuối cùng sẽ nhận được dữ liệu mà họ yêu cầu, hoặc các thông báo liên quan (như xác nhận đăng ký tài khoản, thông báo đơn hàng, v.v.).

![Serverless-FCJ](/images/1/Serverles.png?width=90pc)

### Tổng kết

Mỗi bước trong hệ thống đều đảm nhận một phần quan trọng để xử lý yêu cầu của người dùng từ khi truy cập trang web, gửi yêu cầu, đến khi nhận phản hồi. Hệ thống **Serverless** sử dụng các dịch vụ như **CloudFront**, **Lambda**, và **API Gateway** giúp giảm tải quản lý hạ tầng, đồng thời đảm bảo hiệu suất và bảo mật cho ứng dụng. Các thành phần như **Cognito**, **DynamoDB**, và **SNS** mang đến các chức năng quản lý người dùng, lưu trữ và gửi thông báo một cách dễ dàng, giúp xây dựng ứng dụng phân tán mạnh mẽ và có khả năng mở rộng lớn.

### Nội dung

1. [Định tuyến, Phân phối Nội dung và Bảo mật](1-introduction/1-frontend)
2. [Xử lý Logic, Quản lý Người dùng và Tương tác Hệ thống](1-introduction/2-system)
