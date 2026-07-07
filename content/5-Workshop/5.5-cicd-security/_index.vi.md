---
title : "CI/CD và bảo mật"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

#### Mục tiêu

Mục này trình bày pipeline CI/CD và các lớp bảo mật được tích hợp trong dự án. Trọng tâm là xây dựng quy trình phát hành image an toàn, không dùng AWS access key tĩnh và có kiểm soát trước khi triển khai lên EKS.

#### Luồng CI/CD ứng dụng

Khi có thay đổi trong <code>src/**</code> trên nhánh <code>main</code>, GitHub Actions thực hiện:

1. Xác thực với AWS bằng GitHub OIDC.
2. Build image cho các service chính.
3. Push image lên Amazon ECR.
4. Quét lỗ hổng bằng Trivy.
5. Ký image bằng cosign và tạo SBOM.
6. Cập nhật image tag trong repository GitOps.
7. Argo CD đồng bộ thay đổi lên EKS.

![Minh chứng workflow CI build và push ECR — chụp trình duyệt thật từ GitHub Actions](/images/5-Workshop/5.5-cicd-security/github-actions-ci-live.png)

Job <code>build-push</code> thể hiện đầy đủ các bước Trivy gate, cosign sign và SBOM attestation:

![Minh chứng Trivy + cosign trong job build-push — chụp trình duyệt thật](/images/5-Workshop/5.5-cicd-security/ci-trivy-cosign-live.png)

#### Luồng hạ tầng

Khi pull request thay đổi <code>infra/**</code>, workflow Terraform chạy:

+ <code>terraform fmt -check</code>
+ <code>terraform validate</code>
+ <code>terraform plan</code>
+ Checkov scan
+ Comment kết quả lên pull request

![Minh chứng workflow terraform plan trên PR — chụp trình duyệt thật](/images/5-Workshop/5.5-cicd-security/terraform-plan-pr-live.png)

{{% notice warning %}}
Terraform apply không chạy trong CI. Việc apply hạ tầng luôn được thực hiện thủ công sau khi đã xem xét plan.
{{% /notice %}}

#### Quét bảo mật định kỳ

Workflow <code>security-scan.yml</code> chạy trên pull request và theo lịch hàng tuần, gồm Checkov (Terraform) và Trivy filesystem scan:

![Minh chứng Security Scan — Checkov + Trivy FS — chụp trình duyệt thật](/images/5-Workshop/5.5-cicd-security/security-scan-live.png)

#### Các lớp bảo mật

| Lớp | Công nghệ | Mục đích |
|-----|-----------|----------|
| Xác thực CI | GitHub OIDC | Không lưu access key dài hạn trong GitHub Secrets |
| Image scanning | Trivy | Phát hiện lỗ hổng nghiêm trọng |
| Image signing | cosign | Chứng minh nguồn gốc image |
| IaC scanning | Checkov | Kiểm tra cấu hình Terraform |
| Secret runtime | Secrets Manager + ESO + IRSA | Đồng bộ secret an toàn vào cluster |
| Policy runtime | Kyverno | Kiểm soát image được phép chạy |

#### Quản lý secret

Luồng secret trên AWS:

~~~text
RDS credentials
  -> AWS Secrets Manager
  -> External Secrets Operator
  -> Kubernetes Secret trong namespace boutique
~~~

Thiết kế này giúp tránh việc commit secret vào Git hoặc hard-code trong manifest.

![Minh chứng ExternalSecret SecretSynced — log PowerShell thật](/images/5-Workshop/5.5-cicd-security/externalsecret-live.png)

#### Kyverno verify image

Sau khi image được ký bằng cosign, Kyverno có thể kiểm tra chữ ký trước khi cho phép workload chạy:

~~~powershell
.\scripts\install-kyverno.ps1 -AuditOnly
.\scripts\install-kyverno.ps1
~~~

Chế độ AuditOnly dùng để quan sát trước khi chuyển sang enforce. Điều này giúp giảm rủi ro làm gián đoạn workload khi policy chưa được kiểm tra đủ.

![Minh chứng cài Kyverno và ClusterPolicy verify-boutique-images — log PowerShell thật](/images/5-Workshop/5.5-cicd-security/kyverno-policy-live.png)

#### Kết luận

Pipeline của đề tài không chỉ tự động hóa build và deploy, mà còn bổ sung các lớp kiểm soát cần thiết cho DevSecOps: không dùng khóa tĩnh, quét lỗ hổng, ký image, kiểm tra IaC và quản lý secret an toàn.
