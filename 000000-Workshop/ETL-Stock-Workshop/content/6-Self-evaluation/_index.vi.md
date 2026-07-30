---
title: "Tự đánh giá"
date: 2026-07-30
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

# Tự đánh giá

Trong giai đoạn từ **08/06/2026 đến 31/07/2026**, nhóm đã vận dụng kiến thức lập trình, cơ sở dữ liệu, điện toán đám mây và học máy vào một hệ thống đầu-cuối. Dự án bao gồm thu thập dữ liệu chứng khoán, kiểm duyệt và làm sạch, Feature Engineering, huấn luyện XGBoost, cung cấp kết quả qua API và trực quan hóa bằng Dashboard. Quá trình này giúp nhóm hiểu rõ hơn về kiến trúc mô-đun, xử lý lỗi, tối ưu hiệu năng và tích hợp giữa các dịch vụ AWS.

## Mức độ phát triển kỹ năng kỹ thuật

| Kỹ năng | Trước dự án | Sau dự án | Minh chứng |
|:---|:---:|:---:|:---|
| AWS Lambda | Cơ bản | Khá | Thiết kế nhiều Lambda theo từng giai đoạn của pipeline |
| Amazon S3 | Cơ bản | Khá | Tổ chức các vùng raw, cleansed, processed, quarantine và model |
| Amazon SQS | Chưa nhiều kinh nghiệm | Khá | Áp dụng Fan-Out, chia chunk ticker, retry và định hướng DLQ |
| Amazon EventBridge | Chưa nhiều kinh nghiệm | Khá | Thiết lập lịch cập nhật dữ liệu thị trường hằng ngày |
| Amazon API Gateway | Cơ bản | Khá | Tạo REST API cung cấp kết quả dự đoán |
| Amazon ECR / Docker | Cơ bản | Khá | Đóng gói thư viện dữ liệu và ML thành Lambda Container Image |
| Data Quality | Cơ bản | Khá | Thiết kế schema validation, quy tắc nghiệp vụ và quarantine |
| Feature Engineering | Cơ bản | Khá | Tính toán 16 chỉ báo kỹ thuật và kiểm soát look-ahead bias |
| XGBoost / Machine Learning | Cơ bản | Khá | Huấn luyện, đánh giá mô hình phân loại và lưu model artifact |
| Apache Parquet / Polars | Ít kinh nghiệm | Khá | Tối ưu lưu trữ và xử lý dữ liệu chuỗi thời gian quy mô lớn |
| Viết tài liệu Hugo | Ít kinh nghiệm | Khá | Tổ chức workshop song ngữ theo từng bước |

## Bảng tự đánh giá theo tiêu chí

| STT | Tiêu chí | Nhận xét | Tốt | Khá | Trung bình |
|:--:|:---|:---|:--:|:--:|:--:|
| 1 | Kiến thức và kỹ năng chuyên môn | Vận dụng kiến trúc AWS, xử lý dữ liệu và ML vào hệ thống hoàn chỉnh |  | ✓ |  |
| 2 | Khả năng học hỏi | Tiếp thu nhanh dịch vụ AWS, Polars, Parquet, XGBoost và Hugo | ✓ |  |  |
| 3 | Tính chủ động | Chủ động nghiên cứu giới hạn timeout, dữ liệu lỗi và đóng gói thư viện | ✓ |  |  |
| 4 | Tinh thần trách nhiệm | Theo dõi tiến độ, hoàn thành module và tài liệu được phân công | ✓ |  |  |
| 5 | Tính kỷ luật | Tuân thủ quy ước mã nguồn, cấu trúc dữ liệu và phân công |  | ✓ |  |
| 6 | Tinh thần cầu tiến | Tiếp nhận góp ý và cải thiện kiến trúc, tài liệu qua từng vòng review | ✓ |  |  |
| 7 | Kỹ năng giao tiếp | Trao đổi tương đối rõ ràng nhưng cần cô đọng hơn khi báo cáo lỗi kỹ thuật |  | ✓ |  |
| 8 | Khả năng làm việc nhóm | Phối hợp ingestion, ETL, ML, API, dashboard và documentation | ✓ |  |  |
| 9 | Tác phong chuyên nghiệp | Tôn trọng đóng góp và duy trì thái độ hợp tác | ✓ |  |  |
| 10 | Khả năng giải quyết vấn đề | Phân tích nguyên nhân, đề xuất giải pháp; cần tăng kiểm thử và đo lường |  | ✓ |  |
| 11 | Đóng góp cho dự án | Hoàn thiện pipeline đầu-cuối, workshop và công cụ replay/kiểm thử | ✓ |  |  |
| 12 | Đánh giá tổng thể | Đạt mục tiêu học tập và xây dựng nền tảng có thể tiếp tục mở rộng |  | ✓ |  |

## Những điều nhóm đã làm tốt

- Phân rã bài toán thành các pipeline ingestion, quality gate, ETL, ML, serving và dashboard.
- Áp dụng Lambda và SQS Fan-Out để xử lý hàng nghìn ticker mà không phụ thuộc một hàm chạy kéo dài.
- Bảo vệ dữ liệu phía sau bằng quy tắc kiểm tra và vùng quarantine.
- Sử dụng Parquet và Polars để tối ưu dung lượng lưu trữ và tốc độ xử lý chuỗi thời gian.
- Duy trì README, workshop Hugo song ngữ và worklog để người khác có thể theo dõi, tái hiện hệ thống.
- Phối hợp các module độc lập thành một luồng đầu-cuối.

## Những điểm cần cải thiện

- **Accuracy 53,12%** và **AUC-ROC 0,5487** hiện chỉ cho thấy tín hiệu yếu. Phiên bản tiếp theo cần baseline rõ ràng, chọn lọc feature, walk-forward validation và thử nghiệm thêm mô hình.
- Bổ sung backtesting có chi phí giao dịch, slippage, giới hạn thanh khoản và so sánh với Buy-and-Hold.
- Tăng độ phủ unit test, integration test và kiểm thử dữ liệu đầu-cuối.
- Chuẩn hóa triển khai hạ tầng bằng AWS SAM, CDK hoặc Terraform.
- Hoàn thiện CloudWatch Dashboard, Alarm, DLQ metrics và cảnh báo khi pipeline thiếu dữ liệu hoặc chạy lỗi.
- Trình bày rõ giả định, số liệu, giới hạn và phân biệt kết quả thử nghiệm với khuyến nghị đầu tư.

## Bài học rút ra

- Thiết kế kiến trúc phải bắt đầu từ giới hạn dịch vụ, khối lượng dữ liệu và yêu cầu phục hồi khi có lỗi.
- Validation, logging và khả năng replay quan trọng không kém logic biến đổi chính.
- Với dữ liệu chuỗi thời gian, cách chia tập và kiểm soát rò rỉ tương lai quyết định độ tin cậy của kết quả.
- Accuracy cao hơn 50% một chút chưa đồng nghĩa với chiến lược sinh lợi và không đủ để đưa ra quyết định đầu tư.
- Tài liệu rõ ràng, quy ước thống nhất và giao tiếp thường xuyên giúp giảm lỗi tích hợp, tiết kiệm thời gian.

## Kết luận tự đánh giá

Dự án đạt mục tiêu học tập và tạo được một nền tảng hoạt động, nhưng chưa phải hệ thống giao dịch production. Bước tiếp theo quan trọng nhất là tăng độ tin cậy và kỷ luật đánh giá trước khi mở rộng tính năng: ưu tiên kiểm thử tự động, hạ tầng có khả năng quan sát, triển khai tái lập và backtesting thực tế hơn thay vì chỉ tăng độ phức tạp của mô hình.
