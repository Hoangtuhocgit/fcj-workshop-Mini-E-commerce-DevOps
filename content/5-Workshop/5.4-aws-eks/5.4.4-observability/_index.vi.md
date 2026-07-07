---
title : "Quan sát hệ thống"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4.4 </b> "
---

#### Mục tiêu

Sau khi ứng dụng chạy trên EKS, cần bổ sung lớp quan sát hệ thống để theo dõi trạng thái cluster, workload và một số chỉ số hạ tầng AWS. Phần này sử dụng CloudWatch alarms, Prometheus và Grafana.

#### Cập nhật CloudWatch alarms

Sau khi ALB đã được tạo, chạy lại Terraform để đồng bộ các alarm phụ thuộc vào ALB:

~~~powershell
cd infra/environments/aws
terraform plan -out=tfplan
terraform apply tfplan
~~~

Điều này cho thấy hạ tầng có thể được cập nhật theo từng giai đoạn, không nhất thiết tạo tất cả tài nguyên ngay từ lần apply đầu tiên.

#### Cài monitoring stack

~~~powershell
$env:GRAFANA_ADMIN_PASSWORD = "mat-khau-quan-tri"
.\scripts\install-monitoring.ps1
~~~

Script cài kube-prometheus-stack bằng Helm, sử dụng cấu hình trong <code>observability/aws/helm-values/kube-prometheus-stack.yaml</code>.

#### Kiểm tra Phase 4

~~~powershell
.\scripts\verify-phase4.ps1
~~~

Script kiểm tra:

+ CloudWatch alarms cho RDS và ALB.
+ Pod Prometheus và Grafana trong namespace <code>observability</code>.
+ Khả năng truy cập Grafana qua port-forward.

![Kết quả .\scripts\verify-phase4.ps1 (log PowerShell thật)](/images/5-Workshop/5.4-aws-eks/verify-phase4-live.png)

#### Truy cập Grafana

~~~powershell
kubectl port-forward svc/monitoring-grafana -n observability 3000:80
~~~

Mở <code>http://localhost:3000</code>, đăng nhập bằng user <code>admin</code> và mật khẩu đã cấu hình. Dashboard sử dụng:

~~~text
observability/aws/dashboards/cluster-overview.json
~~~

![Dashboard Cluster overview - Online Boutique trên Grafana (chụp trình duyệt thật)](/images/5-Workshop/5.4-aws-eks/grafana-phase4-live.png)

#### CloudWatch

Trên AWS Console, mở CloudWatch Alarms để kiểm tra alarm của RDS và ALB. Ngay sau khi tạo, một số alarm có thể ở trạng thái INSUFFICIENT_DATA do chưa có đủ dữ liệu metrics.

#### Kết quả

Hoàn tất bước này, hệ thống đã có lớp quan sát cơ bản cho cả hạ tầng AWS và workload Kubernetes.
