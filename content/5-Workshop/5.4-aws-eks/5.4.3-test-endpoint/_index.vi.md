---
title : "Xác minh GitOps và ALB"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.4.3 </b> "
---

#### Mục tiêu

Bước này xác minh ứng dụng đã được Argo CD đồng bộ thành công lên EKS và có thể truy cập từ bên ngoài thông qua Application Load Balancer.

#### Chạy kiểm tra Phase 3

~~~powershell
.\scripts\verify-phase3.ps1
~~~

Script kiểm tra trạng thái Argo CD Application, pod trong namespace <code>boutique</code>, Ingress ALB và HTTP smoke test.

#### Lấy ALB hostname

~~~powershell
kubectl get ingress frontend-ingress -n boutique -o jsonpath='{.status.loadBalancer.ingress[0].hostname}'
~~~

Nếu hostname chưa xuất hiện, cần chờ AWS Load Balancer Controller reconcile Ingress hoặc kiểm tra log controller.

#### Smoke test qua ALB

~~~powershell
$alb = kubectl get ingress frontend-ingress -n boutique -o jsonpath='{.status.loadBalancer.ingress[0].hostname}'
.\scripts\smoke-aws.ps1 $alb
~~~

Kết quả mong đợi là HTTP 200 từ frontend.

![Kết quả .\scripts\verify-phase3.ps1 (log PowerShell thật)](/images/5-Workshop/5.4-aws-eks/verify-phase3-live.png)

#### Kiểm tra trình duyệt

1. Truy cập URL ALB.
2. Xác nhận trang chủ hiển thị sản phẩm.
3. Thêm sản phẩm vào giỏ hàng để kiểm tra frontend, cartservice và Redis.

![Trang chủ Online Boutique qua ALB (chụp trình duyệt thật)](/images/5-Workshop/5.4-aws-eks/alb-browser-real.png)

{{% notice note %}}
Phase 1 trên EKS tập trung vào service cốt lõi. Luồng checkout đầy đủ vẫn được kiểm thử ở Docker Compose vì cần thêm các service phụ trợ.
{{% /notice %}}

#### Kiểm tra Argo CD UI

~~~powershell
kubectl port-forward svc/argocd-server -n argocd 8081:443
~~~

Truy cập <code>https://localhost:8081</code> và xác nhận application <code>online-boutique</code> ở trạng thái Synced và Healthy.

#### Kết quả

Sau bước này, có thể kết luận ứng dụng đã được triển khai lên EKS bằng GitOps và truy cập được qua ALB.
