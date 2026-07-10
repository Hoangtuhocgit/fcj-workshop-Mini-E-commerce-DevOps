---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Ôn tập nội dung tuần 10 về Docker, ECR và các dịch vụ container cơ bản trên AWS.
* Thực hành đóng gói ứng dụng nhiều service bằng Docker Compose và triển khai container trên Lightsail Container Service.
* Tìm hiểu CI/CD cho container, mô hình Monolith to Microservices và triển khai workload trên EKS/Fargate ở mức nâng cao hơn.

### Khung thời gian tuần: **29/06/2026 – 05/07/2026**

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ôn tập nội dung tuần 10 về Docker, ECR, ECS, Fargate và EKS. <br> **Docker Compose và ứng dụng nhiều container:** <br>&emsp; + Viết file <code>docker-compose.yml</code> cho ứng dụng gồm frontend, API và database. <br>&emsp; + Hiểu service dependency, network nội bộ, volume và health check trong môi trường local. | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/4-modernize/><br><https://000015.awsstudygroup.com/> |
| 3 | **Amazon Lightsail Container Service:** <br>&emsp; + Tạo Lightsail container service, đẩy image và triển khai container đơn giản trên AWS. <br>&emsp; + So sánh Lightsail Container với ECS/Fargate về độ phức tạp vận hành và chi phí cho workload nhỏ. | 30/06/2026 | 30/06/2026 | <https://000067.awsstudygroup.com/> |
| 4–5 | **Monolith to Microservices:** <br>&emsp; + Phân tích cách tách monolith thành microservices theo bounded context. <br>&emsp; + Đóng gói từng service thành image riêng, chuẩn bị registry và cấu hình deploy độc lập. | 01/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/4-modernize/> |
| 6 | **CI/CD cho container:** <br>&emsp; + Tìm hiểu pipeline build image, push ECR và cập nhật manifest triển khai. <br>&emsp; + Làm quen GitHub Actions (hoặc CodePipeline) cho luồng build — scan — deploy cơ bản. | 03/07/2026 | 03/07/2026 | <https://000126.awsstudygroup.com/> |
| 7–CN | **Triển khai nâng cao trên EKS/Fargate:** <br>&emsp; + Triển khai nhóm service cốt lõi bằng Deployment và Service trên EKS; kiểm tra Pod, Replica và khả năng tự khôi phục. <br>&emsp; + Theo dõi trạng thái bằng kubectl và CloudWatch; chuẩn bị nền tảng cho workshop đề tài. <br> **Dọn dẹp tài nguyên:** <br>&emsp; + Xóa Lightsail service, workload EKS/Fargate thử nghiệm, image không dùng và rà soát ECR để hạn chế chi phí. | 04/07/2026 | 05/07/2026 | <https://000126.awsstudygroup.com/><br><https://000067.awsstudygroup.com/> |

### Kết quả đạt được tuần 11:

* Biết dùng Docker Compose để chạy ứng dụng nhiều service trên môi trường local.

* Có kinh nghiệm triển khai container trên Lightsail Container Service và so sánh với ECS/Fargate.

* Hiểu hướng tách monolith sang microservices và đóng gói từng service độc lập.

* Nắm luồng CI/CD cơ bản cho container và triển khai workload trên EKS/Fargate ở mức thực hành sâu hơn tuần 10.
