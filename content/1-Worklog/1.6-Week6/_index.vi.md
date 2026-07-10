---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Ôn tập nội dung tuần 5 về AWS Support, AWS CLI trên EC2 và mô hình Highly Available Web Application.
* Tìm hiểu tổng quan chiến lược dịch chuyển hệ thống lên AWS.
* Nắm quy trình dịch chuyển máy chủ ảo với AWS VM Import/Export và cơ sở dữ liệu với AWS DMS, AWS SCT.
* Củng cố bảo mật, mạng, giám sát khi migration và dọn dẹp tài nguyên sau thực hành.

### Khung thời gian tuần: **25/05/2026 – 31/05/2026**

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Ôn tập nội dung tuần 5 về AWS Support, AWS CLI trên EC2, mô hình Highly Available Web Application và workshop triển khai ứng dụng web có tính sẵn sàng cao. | 25/05/2026 | 25/05/2026 | [Cloud Journey – Dịch chuyển](https://cloudjourney.awsstudygroup.com/2-migrate/) |
| 3 | **Chiến lược dịch chuyển hệ thống lên AWS:** <br>&emsp; + Nắm khái niệm migration và vai trò của việc đánh giá workload trước khi dịch chuyển. <br>&emsp; + Tìm hiểu các bước cơ bản: đánh giá hệ thống, lập kế hoạch, thực hiện dịch chuyển, kiểm thử và tối ưu sau dịch chuyển. <br>&emsp; + Nhận biết các rủi ro thường gặp như downtime, sai cấu hình mạng, lỗi phân quyền, mất dữ liệu và phát sinh chi phí. | 26/05/2026 | 26/05/2026 | [Cloud Journey – Dịch chuyển](https://cloudjourney.awsstudygroup.com/2-migrate/) |
| 4–5 | **Dịch chuyển máy chủ ảo với AWS VM Import/Export:** <br>&emsp; + Nắm mục đích sử dụng VM Import/Export để đưa máy ảo từ môi trường local/on-premises lên AWS. <br>&emsp; + Tìm hiểu quy trình chuẩn bị image máy ảo, upload lên Amazon S3 và import thành Amazon Machine Image hoặc EC2 instance. <br>&emsp; + Tìm hiểu các thành phần liên quan như S3 bucket, IAM Role, EC2, AMI, định dạng image, bảo mật dữ liệu và chi phí. | 27/05/2026 | 28/05/2026 | [Bài lab 14](https://000014.awsstudygroup.com/) |
| 6–7 | **Dịch chuyển cơ sở dữ liệu với AWS DMS và AWS SCT:** <br>&emsp; + Nắm vai trò của AWS DMS trong việc dịch chuyển dữ liệu giữa database nguồn và database đích. <br>&emsp; + Tìm hiểu replication instance, source endpoint, target endpoint, migration task và các kiểu migration như full load, CDC. <br>&emsp; + Tìm hiểu AWS SCT dùng để hỗ trợ chuyển đổi schema khi database nguồn và database đích khác engine. <br>&emsp; + Thực hành mô phỏng tạo database nguồn/đích, cấu hình endpoint, tạo migration task và kiểm tra dữ liệu sau khi migrate. | 29/05/2026 | 30/05/2026 | [Bài lab 43](https://000043.awsstudygroup.com/) |
| CN | **Củng cố bảo mật, mạng và giám sát khi migration:** <br>&emsp; + Kiểm tra Security Group, subnet, route table, quyền IAM, snapshot/backup và phương án rollback khi cần thiết. <br>&emsp; + Theo dõi log, metric và trạng thái migration task bằng CloudWatch hoặc giao diện quản trị AWS. <br> **Dọn dẹp:** Dọn dẹp các tài nguyên đã tạo như EC2, AMI, S3 object, RDS instance, replication instance, endpoint, migration task và snapshot để hạn chế phát sinh chi phí. | 31/05/2026 | 31/05/2026 | [Bài lab 43](https://000043.awsstudygroup.com/)<br>[Bài lab 14](https://000014.awsstudygroup.com/) |

### Kết quả đạt được tuần 6:

* Hiểu tổng quan quy trình dịch chuyển workload từ môi trường truyền thống lên AWS.

* Nắm được vai trò của AWS VM Import/Export trong việc dịch chuyển máy chủ ảo.

* Hiểu cách AWS DMS và SCT hỗ trợ dịch chuyển cơ sở dữ liệu và chuyển đổi schema.

* Biết các yếu tố cần kiểm tra sau migration như dữ liệu, kết nối ứng dụng, bảo mật, log và chi phí.

* Củng cố kỹ năng lập kế hoạch, kiểm thử, giám sát và dọn dẹp tài nguyên sau khi thực hành trên AWS.
