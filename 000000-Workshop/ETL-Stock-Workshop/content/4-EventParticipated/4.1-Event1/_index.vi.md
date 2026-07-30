---
title: "FCAJ Meetup - 13/06/2026"
date: 2026-06-13
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# FCAJ Meetup - 13/06/2026

## Thông tin chung

| Nội dung | Thông tin |
|:---|:---|
| Tên sự kiện | FCAJ Meetup |
| Đơn vị tổ chức | First Cloud AI Journey (FCAJ) |
| Ngày tham dự | 13/06/2026 |
| Vai trò | Người tham dự |

Buổi meetup gồm bốn góc nhìn bổ trợ cho nhau: công việc và văn hóa của Data Analytics trong tập đoàn đa quốc gia, kiến trúc dịch vụ URL Shortener có khả năng mở rộng trên AWS, trách nhiệm thực tế của một DevOps Engineer và hành trình phát triển từ FCAJ đến các cộng đồng sinh viên cùng môi trường AWS Partner.

## Mục tiêu tham gia

- Hiểu thêm công việc thực tế của Data Analytics Engineer và DevOps Engineer.
- Tham khảo cách phân rã một hệ thống AWS có khả năng mở rộng qua bài toán URL Shortener.
- Tìm hiểu quy trình tuyển dụng, văn hóa làm việc và định hướng phát triển trong môi trường quốc tế.
- Biết thêm các cơ hội dành cho sinh viên như AWS Student Builder Group và AWS Community Builder.
- Rút ra những thực hành có thể cải thiện dự án ETL và Machine Learning của nhóm.

## Diễn giả và chủ đề

1. **Đạt Phạm và Cường Nguyễn** - công việc Data Analytics thực tế, tuyển dụng, phát triển nghề nghiệp và văn hóa tại tập đoàn đa quốc gia.
2. **Đinh Trung Kiên và Nguyễn Minh Thọ** - *A Scalable URL Shortening Service on AWS*.
3. **Trong H. Truong** - *What Does a DevOps Engineer Really Do?*
4. **Danh Hoàng Hiếu Nghị** - hành trình từ First Cloud AI Journey đến cộng đồng sinh viên AWS và môi trường AWS Partner.

## Nội dung nổi bật

### Data Analytics không chỉ là làm báo cáo

Data Analytics Engineer không chỉ tính chỉ số rồi đưa lên dashboard. Công việc còn yêu cầu hiểu bối cảnh kinh doanh, theo dõi hiệu suất vận hành, phát hiện bất thường, tìm nguyên nhân gốc rễ và kể một câu chuyện dữ liệu rõ ràng. Khi một chỉ số như GMV biến động, việc báo tăng hay giảm mới chỉ là bước đầu; câu hỏi hữu ích hơn là vì sao chỉ số thay đổi và hành động nào nên được cân nhắc.

Phần chia sẻ cũng nhấn mạnh tư duy phản biện, giao tiếp, giải quyết vấn đề và data storytelling. Điều này liên quan trực tiếp tới dashboard cổ phiếu của nhóm: nhiều biểu đồ chưa chắc có giá trị nếu người dùng không nhận ra tín hiệu quan trọng hoặc không hiểu giới hạn của kết quả.

### URL Shortener có khả năng mở rộng trên AWS

Kiến trúc tách trách nhiệm giữa CloudFront, AWS WAF, AWS Amplify, các dịch vụ container trên Amazon ECS, Amazon ElastiCache for Redis và Amazon DynamoDB. Key Generation Service được tách riêng để tạo trước các mã ngắn; Redis áp dụng cache-aside nhằm giảm số lượt đọc trực tiếp từ cơ sở dữ liệu.

Bài học quan trọng không nằm ở số lượng dịch vụ AWS, mà ở lý do phân tách: mỗi thành phần có trách nhiệm rõ ràng, cache đặt tại luồng đọc nhiều, điểm truy cập công khai được bảo vệ và không gom toàn bộ chức năng vào một ứng dụng duy nhất.

### DevOps rộng hơn một danh sách công cụ

Docker, Kubernetes, CI/CD và cloud chỉ là một phần của DevOps. Nền tảng Linux, networking, lập trình, Git, container, deployment, logging, configuration và environment variables vẫn cần thiết dù công cụ thay đổi. Thông điệp **“Tools change. Fundamentals stay.”** phản ánh đúng trải nghiệm của nhóm khi phải thay đổi thư viện và cách triển khai trong quá trình làm dự án.

Phần này cũng nhấn mạnh việc hỏi “tại sao” trước “làm như thế nào”, xác định đúng người hoặc thành phần sở hữu vấn đề, giao tiếp rõ ràng và sử dụng AI để tăng năng lực làm việc thay vì tắt tư duy.

### Từ FCAJ đến cộng đồng AWS

Công việc hoặc chương trình đầu tiên chỉ là điểm bắt đầu. FCAJ, AWS Student Builder Group, AWS Community Builder và môi trường AWS Partner tạo cơ hội làm dự án, chia sẻ kiến thức, gặp gỡ những người cùng quan tâm và xây dựng dần lịch sử nghề nghiệp. Giá trị cuối cùng phụ thuộc vào việc duy trì học tập và đóng góp, không chỉ ở việc đã tham gia chương trình.

## Áp dụng vào dự án

- Giữ riêng trách nhiệm của ingestion, kiểm tra chất lượng, biến đổi, huấn luyện và cung cấp kết quả dự đoán.
- Cải thiện log để mỗi lỗi thể hiện rõ ticker, bước xử lý, nguyên nhân và vị trí dữ liệu quarantine.
- Giúp dashboard giải thích độ mới, chất lượng dữ liệu và các tín hiệu quan trọng thay vì chỉ hiển thị con số.
- Kiểm thử luồng thất bại bằng schema sai, Lambda lỗi và message SQS không hợp lệ.
- Viết rõ cách triển khai, quyền IAM, biến môi trường và quy trình kiểm thử để thành viên khác có thể tái hiện hệ thống.

## Trải nghiệm và bài học

Buổi meetup giúp nhóm kết nối công nghệ, thực hành nghề nghiệp và hoạt động cộng đồng. Ba ưu tiên gần nhất là làm rõ ranh giới giữa các module, cải thiện khả năng quan sát lỗi và trình bày dashboard thành một câu chuyện có ý nghĩa từ dữ liệu. Bài học xuyên suốt là phải hiểu vấn đề trước, sau đó mới chọn tập công cụ nhỏ nhất có thể giải quyết vấn đề một cách đáng tin cậy.
