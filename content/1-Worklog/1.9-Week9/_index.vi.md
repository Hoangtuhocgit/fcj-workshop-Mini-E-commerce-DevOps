---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Ôn tập nội dung tuần 8 về bảo mật, độ tin cậy, hiệu năng và tối ưu chi phí trên AWS.
* Tìm hiểu lộ trình hiện đại hóa ứng dụng từ monolith sang microservices và serverless.
* Nắm CI/CD, tách microservice, database-per-service, messaging/eventing và các dịch vụ container trên AWS.

### Khung thời gian tuần: **15/06/2026 – 21/06/2026**

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ôn tập nội dung tuần 8 về bảo mật, độ tin cậy, hiệu năng và tối ưu chi phí trên AWS. <br> **Tổng quan lộ trình Hiện đại hóa ứng dụng:** <br>&emsp; + Nắm mục tiêu chuyển ứng dụng monolith sang microservices, tách bounded context và giảm phụ thuộc. <br>&emsp; + Tìm hiểu cách host (triển khai) ứng dụng trên AWS và chuẩn bị quy trình phát hành tự động. | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/4-modernize/> |
| 3–4 | **Dịch chuyển ứng dụng Monolith:** <br>&emsp; + Phân tích ứng dụng Java Spring Boot/RDBMS, xác định frontend, backend, database và các điểm phụ thuộc. <br>&emsp; + Tìm hiểu các bước đưa ứng dụng lên AWS, cấu hình môi trường chạy và kiểm tra kết nối sau migration. | 16/06/2026 | 17/06/2026 | <https://000050.awsstudygroup.com/> |
| 5–6 | **Tự động phát hành ứng dụng và tạo Microservice:** <br>&emsp; + Nắm CI/CD pipeline, source/build/deploy stage và kiểm thử sau triển khai. <br>&emsp; + Tìm hiểu cách tách chức năng trong monolith thành microservice độc lập, có API và dữ liệu riêng. <br> **Cơ cấu lại dữ liệu, workflow, messaging và eventing:** <br>&emsp; + Nhận biết vấn đề shared database, hướng xử lý database-per-service và trao đổi bất đồng bộ bằng SQS/SNS hoặc event-driven. | 18/06/2026 | 19/06/2026 | <https://000051.awsstudygroup.com/><br><https://000052.awsstudygroup.com/><br><https://000053.awsstudygroup.com/><br><https://000054.awsstudygroup.com/> |
| 7 | **Xác thực ứng dụng và serverless:** <br>&emsp; + Tìm hiểu SPA, Amazon Cognito, API Gateway, Lambda, Step Functions, S3, DynamoDB, SAM, CloudWatch và X-Ray. | 20/06/2026 | 20/06/2026 | <https://000055.awsstudygroup.com/><br><https://000081.awsstudygroup.com/> |
| CN | **Mở đầu phần Container services và tổng hợp:** <br>&emsp; + Tìm hiểu Lightsail Container, Amazon EKS, AWS Fargate và CI/CD trên EKS với CodePipeline/GitHub ở mức tổng quan. <br>&emsp; + Tổng hợp kiến thức hiện đại hóa ứng dụng: CI/CD, microservice, database tách riêng, messaging/eventing, SPA, Cognito, API Gateway, Lambda và container services. <br> **Dọn dẹp:** Dọn dẹp tài nguyên thực hành như app demo, database thử nghiệm, API Gateway, Lambda, Cognito, S3, SQS/SNS, EKS/Lightsail Container demo và pipeline để hạn chế phát sinh chi phí. | 21/06/2026 | 21/06/2026 | <https://000046.awsstudygroup.com/><br><https://000126.awsstudygroup.com/><br><https://cloudjourney.awsstudygroup.com/4-modernize/> |

### Kết quả đạt được tuần 9:

* Hiểu định hướng hiện đại hóa ứng dụng từ monolith sang microservices và serverless trên AWS.

* Nắm các thành phần chính: CI/CD, microservice, database tách riêng, messaging/eventing, SPA, Cognito, API Gateway, Lambda và container services.

* Có cái nhìn tổng quan về ECS/EKS/Fargate và cách kết hợp container với pipeline triển khai.
