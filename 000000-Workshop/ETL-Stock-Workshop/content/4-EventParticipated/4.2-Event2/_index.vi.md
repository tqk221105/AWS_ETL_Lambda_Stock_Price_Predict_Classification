---
title: "Agentic AI Build Week - 25/07/2026"
date: 2026-07-25
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Agentic AI Build Week - Project Sharing & Hackathon Journey

## Thông tin chung

| Nội dung | Thông tin |
|:---|:---|
| Tên sự kiện | Agentic AI Build Week - Project Sharing & Hackathon Journey |
| Đơn vị tổ chức | First Cloud AI Journey / Agentic AI Build Week |
| Ngày tham dự | 25/07/2026 |
| Vai trò | Người tham dự |

Sự kiện trình bày ba hành trình khác nhau khi xây dựng sản phẩm Agentic AI trong điều kiện thực tế. SignalScout và Plan V giới thiệu các prototype đã hoàn thiện, còn đội 3KA chia sẻ thẳng thắn về 24 giờ hackathon, từ quyết định phạm vi, lỗi kỹ thuật, phối hợp nhóm đến chuẩn bị demo.

## Mục tiêu tham gia

- Tìm hiểu cách các nhóm biến ý tưởng Agentic AI thành sản phẩm có thể demo.
- Tham khảo kiến trúc AWS phối hợp nhiều agent và nhiều nguồn dữ liệu.
- Hiểu vai trò của bằng chứng, khả năng giải thích và sự kiểm soát của con người trong quyết định có AI hỗ trợ.
- Học cách giới hạn phạm vi, phân chia công việc và chuẩn bị demo đáng tin cậy khi thời gian ngắn.
- Rút ra bài học có thể áp dụng vào dự án ETL và phân loại xu hướng giá cổ phiếu.

## Các nhóm và giải pháp

### SignalScout

SignalScout phát hiện sớm các tín hiệu thay đổi chiến lược của doanh nghiệp. Hệ thống thu thập thông tin từ nhiều nguồn, kiểm tra bằng chứng, phân tích chỉ số và sắp xếp kết quả thành câu chuyện có thể truy vết cho các nhóm chiến lược, quản trị rủi ro, competitive intelligence và khách hàng B2B. Kết quả hỗ trợ con người cân nhắc các hướng **Maintain**, **Adapt** hoặc **Accelerate**, không tự thay người dùng đưa ra quyết định cuối cùng.

Kiến trúc kết hợp Route 53, Amplify, WAF, Cognito, API Gateway, Lambda, AgentCore Runtime, AgentCore Memory, Strands Agent, Amazon Bedrock Guardrails, S3, DynamoDB, CloudWatch, CloudTrail, IAM và Secrets Manager. Crawler subagent và analysis subagent minh họa cách tách trách nhiệm. Nhóm còn trình bày phương án tiết kiệm chi phí hơn với AgentCore Gateway, công cụ web search và browser, cho thấy kiến trúc cần được điều chỉnh sau khi xem xét chi phí, dependency và khả năng quan sát.

### Plan V - Solution Architect Professional AI Native App

Plan V giải quyết khối lượng công việc của Solution Architect khi phải đọc yêu cầu, tìm thông tin còn thiếu, phác thảo kiến trúc, vẽ sơ đồ và ước tính chi phí AWS. Ứng dụng nhận tài liệu có cấu trúc hoặc yêu cầu bằng ngôn ngữ tự nhiên, tạo Requirements Catalogue, đề xuất nhiều phương án kiến trúc cấp cao, sinh sơ đồ Draw.io có thể chỉnh sửa và đưa ra ước tính định hướng cho khu vực `ap-southeast-1`.

Workflow sử dụng knowledge base nội bộ, Amazon Bedrock, Draw.io MCP và AWS Pricing MCP. Kiến trúc triển khai tách frontend, backend, agent, dữ liệu dự án và dịch vụ AI bằng S3, CloudFront, Cognito, Application Load Balancer, ECS Fargate, PostgreSQL, EFS, ECR, CloudWatch và Terraform. Điểm quan trọng nhất là kết quả chỉ được gọi là **bản nháp**: AI giảm công việc lặp lại và tạo điểm bắt đầu, còn Solution Architect vẫn phải xác minh giả định, yêu cầu bảo mật và chịu trách nhiệm với thiết kế cuối cùng.

### Đội 3KA - S.H.E.P.H.E.R.D.

S.H.E.P.H.E.R.D. là viết tắt của *Smart Human-flow Evaluation, Prediction, Hazard Detection, Response, and Dispatch*. Hệ thống xử lý camera để theo dõi người, đo mật độ đám đông, ước tính tình trạng hàng chờ, phát hiện nguy cơ ùn tắc, tạo cảnh báo và đề xuất hành động vận hành.

Lớp computer vision sử dụng YOLO và ByteTrack với Kinesis Video Streams, ECS, SageMaker Endpoint, DynamoDB và S3. Lớp web sử dụng CloudFront, API Gateway, Lambda và Cognito. AgentCore Runtime, Strands Agent, Amazon Bedrock và AgentCore Memory tạo hai vai trò: **Autonomous Monitor** chủ động quan sát và **Operator Copilot** trả lời câu hỏi bằng ngôn ngữ tự nhiên.

Hành trình 24 giờ cũng cho thấy các rủi ro thực tế: code không ổn định, độ trễ inference, phân công chưa rõ, thiếu ngủ, quên commit và vô tình đẩy file môi trường lên GitHub. Đội đề xuất xác định rõ thế nào là “done”, chuẩn bị tài khoản và starter template, phân vai cụ thể, thu nhỏ phạm vi và tập trước câu chuyện demo ngắn.

## Bài học nhóm rút ra

### Bắt đầu từ quyết định hoặc vấn đề cần hỗ trợ

Mỗi sản phẩm bắt đầu bằng một nhu cầu cụ thể: phát hiện thay đổi chiến lược, rút ngắn thời gian phác thảo kiến trúc hoặc hỗ trợ vận hành khu vực đông người. Dự án cổ phiếu cũng cần giải thích người dùng nhận được gì từ pipeline, Quality Gate, mô hình phân loại và dashboard, thay vì chỉ mô tả một tập hợp dịch vụ AWS.

### AI cần bằng chứng và điểm kiểm tra của con người

SignalScout gắn kết luận với bằng chứng, còn Plan V coi kiến trúc là bản nháp để chuyên gia phản biện. Mô hình phân loại xu hướng giá cũng chỉ nên là thông tin hỗ trợ, không phải lời khuyên đầu tư chắc chắn. Người dùng cần biết dữ liệu đầu vào, thời gian cập nhật, trạng thái kiểm tra chất lượng, feature quan trọng và giới hạn của mô hình.

### Giới hạn phạm vi trước khi thêm tính năng

Một luồng đầu-cuối nhỏ nhưng chạy ổn định có giá trị hơn nhiều tính năng chưa hoàn thành. Nhóm cần ổn định ingestion, validation, transformation, inference và visualization cho một tập ticker rõ ràng trước khi thêm model mới hoặc lớp Agentic AI.

### Nghĩ đến chi phí, bảo mật và quan sát lỗi từ sớm

Các phần trình bày đều đề cập authentication, secret management, monitoring hoặc chi phí. Dự án hiện tại cần theo dõi số lần Lambda chạy, dung lượng S3, message lỗi trong SQS, lưu lượng API và chi phí bất thường; thông tin nhạy cảm không được đưa lên Git và nên được quản lý bằng biến môi trường hoặc Secrets Manager khi phù hợp.

### Cách làm việc ảnh hưởng trực tiếp tới demo

Quy ước branch, trách nhiệm rõ ràng, deadline nội bộ và phương án demo dự phòng quan trọng không kém mô hình. Nhóm nên chuẩn bị bộ dữ liệu đã xác minh, kết quả inference mẫu và ảnh dashboard để vẫn trình bày được khi API hoặc mạng gặp lỗi.

## Áp dụng vào dự án cổ phiếu

- Viết lại giá trị dự án theo hướng dữ liệu đáng tin cậy, tín hiệu có thể giải thích và hỗ trợ quyết định.
- Hiển thị bằng chứng cùng dự đoán: ngày dữ liệu, trạng thái kiểm tra chất lượng và các feature quan trọng.
- Giữ bước kiểm tra của con người và ghi rõ kết quả chỉ mang tính tham khảo.
- Ưu tiên MVP đầu-cuối ổn định trước khi mở rộng phạm vi.
- Tách collection, validation, feature transformation, training, inference và visualization.
- Theo dõi chi phí, lỗi; tăng cường quản lý secret và thực hành Git.
- Phân vai demo rõ ràng và chuẩn bị một kịch bản dự phòng đã được kiểm thử.

## Trải nghiệm và kết luận

Sự kiện cho thấy sản phẩm AI không được tạo nên chỉ bằng việc chọn model hoặc gọi API. Cách đặt bài toán, tổ chức dữ liệu, kiểm tra bằng chứng, kiểm soát chi phí, bảo mật và phối hợp nhóm quyết định sản phẩm có thực sự hữu ích hay không. Trước mắt, nhóm sẽ ưu tiên độ tin cậy và khả năng giải thích của pipeline hiện tại; trợ lý hoặc agent chỉ được cân nhắc khi nền tảng đã ổn định.
