---
title : "CI/CD and Security"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

#### Objective

This section presents the CI/CD pipeline and security layers integrated into the project. The focus is building a secure image release process without static AWS access keys and with controls before deployment to EKS.

#### Application CI/CD flow

When changes occur in <code>src/**</code> on the <code>main</code> branch, GitHub Actions performs:

1. Authenticate to AWS using GitHub OIDC.
2. Build images for core services.
3. Push images to Amazon ECR.
4. Scan for vulnerabilities with Trivy.
5. Sign images with cosign and generate an SBOM.
6. Update image tags in the GitOps repository.
7. Argo CD syncs changes to EKS.

![CI workflow evidence — build and push to ECR (real browser capture from GitHub Actions)](/images/5-Workshop/5.5-cicd-security/github-actions-ci-live.png)

The <code>build-push</code> job shows the full Trivy gate, cosign sign, and SBOM attestation steps:

![Trivy + cosign evidence in build-push job (real browser capture)](/images/5-Workshop/5.5-cicd-security/ci-trivy-cosign-live.png)

#### Infrastructure flow

When a pull request changes <code>infra/**</code>, the Terraform workflow runs:

+ <code>terraform fmt -check</code>
+ <code>terraform validate</code>
+ <code>terraform plan</code>
+ Checkov scan
+ Comment results on the pull request

![Terraform plan workflow evidence on PR (real browser capture)](/images/5-Workshop/5.5-cicd-security/terraform-plan-pr-live.png)

{{% notice warning %}}
Terraform apply does not run in CI. Infrastructure apply is always performed manually after reviewing the plan.
{{% /notice %}}

#### Scheduled security scanning

The <code>security-scan.yml</code> workflow runs on pull requests and weekly on a schedule, covering Checkov (Terraform) and Trivy filesystem scans:

![Security Scan evidence — Checkov + Trivy FS (real browser capture)](/images/5-Workshop/5.5-cicd-security/security-scan-live.png)

#### Security layers

| Layer | Technology | Purpose |
|-------|------------|---------|
| CI authentication | GitHub OIDC | Avoid storing long-lived access keys in GitHub Secrets |
| Image scanning | Trivy | Detect critical vulnerabilities |
| Image signing | cosign | Prove image provenance |
| IaC scanning | Checkov | Validate Terraform configuration |
| Runtime secrets | Secrets Manager + ESO + IRSA | Sync secrets securely into the cluster |
| Runtime policy | Kyverno | Control which images are allowed to run |

#### Secret management

Secret flow on AWS:

~~~text
RDS credentials
  -> AWS Secrets Manager
  -> External Secrets Operator
  -> Kubernetes Secret in boutique namespace
~~~

This design avoids committing secrets to Git or hard-coding them in manifests.

![ExternalSecret SecretSynced evidence (real PowerShell log)](/images/5-Workshop/5.5-cicd-security/externalsecret-live.png)

#### Kyverno image verification

After images are signed with cosign, Kyverno can verify signatures before allowing workloads to run:

~~~powershell
.\scripts\install-kyverno.ps1 -AuditOnly
.\scripts\install-kyverno.ps1
~~~

AuditOnly mode is used to observe behavior before switching to enforce mode. This reduces the risk of disrupting workloads when policies have not been fully validated.

![Kyverno install and verify-boutique-images ClusterPolicy (real PowerShell log)](/images/5-Workshop/5.5-cicd-security/kyverno-policy-live.png)

#### Conclusion

The project pipeline does not only automate build and deploy—it adds the control layers required for DevSecOps: no static keys, vulnerability scanning, image signing, IaC checks, and secure secret management.
