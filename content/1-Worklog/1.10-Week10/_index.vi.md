---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Ôn tập nội dung tuần 9 về hiện đại hóa ứng dụng, microservices, serverless và mở đầu container services.
* Tìm hiểu Docker, Amazon ECR và các dịch vụ chạy container trên AWS: ECS, Fargate, Kubernetes/EKS.
* Thực hành đóng gói, triển khai ứng dụng container và dọn dẹp tài nguyên sau lab.

### Khung thời gian tuần: **22/06/2026 – 28/06/2026**

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ôn tập nội dung tuần 9 về hiện đại hóa ứng dụng, microservices, serverless và mở đầu container services. <br> **Tổng quan Docker và Container:** <br>&emsp; + Nắm khái niệm Container, Image, Dockerfile, Docker Engine và Container Registry. <br>&emsp; + Phân biệt Virtual Machine và Container, hiểu lợi ích đóng gói ứng dụng và triển khai nhất quán. | 22/06/2026 | 22/06/2026 | [Cloud Journey – Container](https://cloudjourney.awsstudygroup.com/5-container/)<br>[Bài lab 15](https://000015.awsstudygroup.com/) |
| 3–4 | **Thực hành Docker cơ bản:** <br>&emsp; + Viết Dockerfile cho ứng dụng mẫu, build Docker Image và chạy Container trên môi trường local. <br>&emsp; + Sử dụng các lệnh Docker cơ bản để kiểm tra container, image, log, port mapping và dọn dẹp tài nguyên. | 23/06/2026 | 24/06/2026 | [Bài lab 15](https://000015.awsstudygroup.com/) |
| 5 | **Amazon Elastic Container Registry (Amazon ECR):** <br>&emsp; + Tạo Private Repository, đăng nhập ECR bằng AWS CLI và push Docker Image lên repository. <br>&emsp; + Kiểm tra image tag, version và quyền truy cập repository để chuẩn bị cho triển khai ứng dụng. | 25/06/2026 | 25/06/2026 | [Bài lab 67](https://000067.awsstudygroup.com/) |
| 6 | **Amazon ECS và AWS Fargate:** <br>&emsp; + Nắm vai trò của ECS Cluster, Task Definition, Service, Fargate và cách chạy container không cần quản lý server. | 26/06/2026 | 26/06/2026 | [Bài lab 67](https://000067.awsstudygroup.com/) |
| 7–CN | **Amazon EKS và thực hành triển khai container:** <br>&emsp; + Tìm hiểu kiến trúc Kubernetes/EKS gồm Cluster, Node, Pod, Deployment, Service, Namespace và kubectl. <br>&emsp; + Triển khai ứng dụng mẫu bằng Deployment và Service, kiểm tra Pod, Replica và khả năng tự khôi phục. <br>&emsp; + Theo dõi trạng thái tài nguyên bằng kubectl và CloudWatch ở mức cơ bản. <br> **Dọn dẹp tài nguyên sau thực hành:** <br>&emsp; + Xóa Deployment, Service, Pod, Docker Image không sử dụng và kiểm tra lại Amazon ECR Repository. <br>&emsp; + Rà soát các tài nguyên liên quan đến ECS/EKS/Fargate để hạn chế phát sinh chi phí ngoài dự kiến. | 27/06/2026 | 28/06/2026 | [Bài lab 126](https://000126.awsstudygroup.com/)<br>[Bài lab 67](https://000067.awsstudygroup.com/) |

### Kết quả đạt được tuần 10:

* Hiểu sự khác biệt giữa Container và Virtual Machine, cũng như quy trình build, run, push và pull Docker Image.

* Biết sử dụng Docker để đóng gói ứng dụng và lưu trữ image trên Amazon ECR.

* Nắm kiến thức cơ bản về ECS, Fargate, Kubernetes và Amazon EKS trong triển khai ứng dụng container.

* Có khả năng triển khai ứng dụng container mẫu, kiểm tra trạng thái tài nguyên và dọn dẹp sau thực hành.
