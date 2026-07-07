---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Ôn tập nội dung tuần 6 về chiến lược migration, AWS VM Import/Export, AWS DMS và AWS SCT.
* Tìm hiểu tổng quan tối ưu hệ thống trên AWS sau khi dịch chuyển workload.
* Thực hành tự động hóa vận hành với AWS Lambda, giám sát với CloudWatch/Grafana, quản lý tài nguyên bằng Tag và Resource Groups.
* Nắm IAM Resource Tag, AWS Systems Manager, Session Manager và AWS CloudFormation.

### Khung thời gian tuần: **01/06/2026 – 07/06/2026**

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ôn tập nội dung tuần 6 về chiến lược migration, AWS VM Import/Export, AWS DMS và AWS SCT. <br> **Tổng quan tối ưu hệ thống trên AWS:** <br>&emsp; + Nắm mục tiêu tối ưu theo các khía cạnh vận hành, bảo mật, độ tin cậy, hiệu năng và chi phí. <br>&emsp; + Liên hệ kiến thức migration với giai đoạn vận hành sau khi hệ thống đã được đưa lên AWS. | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/3-optimize/> |
| 3 | **Tự động hóa vận hành và tối ưu chi phí EC2 với AWS Lambda:** <br>&emsp; + Nắm cách dùng Lambda để tự động bật/tắt EC2 instance theo tag hoặc lịch chạy, kết hợp thông báo Slack webhook. <br>&emsp; + Thực hành mô phỏng tạo EC2, gán tag, tạo IAM Role cho Lambda, viết hàm start/stop instance và kiểm tra kết quả. | 02/06/2026 | 03/06/2026 | <https://000022.awsstudygroup.com/> |
| 4 | **Giám sát hệ thống với Amazon CloudWatch và Grafana:** <br>&emsp; + Củng cố kiến thức CloudWatch metrics, log, alarm và dashboard trong quá trình vận hành hệ thống. <br>&emsp; + Tìm hiểu cách cài Grafana trên EC2 Linux, kết nối CloudWatch làm data source và tạo dashboard theo dõi EC2. <br> **Quản lý tài nguyên bằng Tag và Resource Groups:** <br>&emsp; + Nắm vai trò của tag trong việc phân loại tài nguyên theo môi trường, mục đích sử dụng, người phụ trách và chi phí. <br>&emsp; + Thực hành gán tag cho EC2/EBS, lọc tài nguyên theo tag và tạo Resource Group để quản lý tài nguyên tập trung. | 03/06/2026 | 04/06/2026 | <https://000029.awsstudygroup.com/><br><https://000027.awsstudygroup.com/> |
| 5 | **Kiểm soát truy cập EC2 bằng Resource Tag thông qua AWS IAM:** <br>&emsp; + Nắm cách xây dựng IAM Policy có điều kiện dựa trên tag để áp dụng nguyên tắc phân quyền tối thiểu. <br>&emsp; + Tìm hiểu IAM User, IAM Role, assume role và kiểm tra quyền tạo/chỉnh sửa EC2 khi tag đáp ứng điều kiện. <br> **AWS Systems Manager, Session Manager và CloudFormation:** <br>&emsp; + Nắm vai trò Systems Manager trong quản lý tập trung, Patch Manager và Run Command trên nhiều máy chủ. <br>&emsp; + Tìm hiểu Session Manager để kết nối EC2 public/private an toàn hơn, hạn chế mở SSH/RDP trực tiếp và có thể lưu session log. | 04/06/2026 | 05/06/2026 | <https://000028.awsstudygroup.com/><br><https://000031.awsstudygroup.com/><br><https://000058.awsstudygroup.com/> |
| 6 | **AWS CloudFormation:** <br>&emsp; + Nắm khái niệm CloudFormation, Infrastructure as Code, template, stack, rollback và drift detection. <br>&emsp; + Thực hành mô phỏng triển khai tài nguyên cơ bản bằng template và quan sát trạng thái stack. <br> **Dọn dẹp:** Dọn dẹp các tài nguyên đã tạo như EC2, Security Group, IAM Role, Lambda Function, CloudWatch alarm, Grafana instance, Resource Group, Systems Manager cấu hình thử nghiệm và CloudFormation stack để hạn chế phát sinh chi phí. | 05/06/2026 | 07/06/2026 | <https://000037.awsstudygroup.com/> |

### Kết quả đạt được tuần 7:

* Hiểu định hướng tối ưu hệ thống sau khi triển khai hoặc migration lên AWS.

* Biết dùng Lambda, tag, Resource Groups, IAM Resource Tag, CloudWatch/Grafana, Systems Manager, Session Manager và CloudFormation ở mức cơ bản.

* Củng cố kỹ năng tự động hóa vận hành, giám sát, kiểm soát truy cập, quản lý tài nguyên và tối ưu chi phí trên AWS.
