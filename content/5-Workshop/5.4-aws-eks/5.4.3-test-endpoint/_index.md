---
title : "Verify GitOps and ALB"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.4.3 </b> "
---

#### Objective

This step verifies that the application has been successfully synced to EKS by Argo CD and is accessible externally through the Application Load Balancer.

#### Run Phase 3 verification

~~~powershell
.\scripts\verify-phase3.ps1
~~~

The script checks Argo CD Application status, pods in the <code>boutique</code> namespace, ALB Ingress, and HTTP smoke test.

#### Get ALB hostname

~~~powershell
kubectl get ingress frontend-ingress -n boutique -o jsonpath='{.status.loadBalancer.ingress[0].hostname}'
~~~

If the hostname is not yet available, wait for the AWS Load Balancer Controller to reconcile the Ingress or check controller logs.

#### Smoke test via ALB

~~~powershell
$alb = kubectl get ingress frontend-ingress -n boutique -o jsonpath='{.status.loadBalancer.ingress[0].hostname}'
.\scripts\smoke-aws.ps1 $alb
~~~

The expected result is HTTP 200 from the frontend.

![verify-phase3.ps1 output (real PowerShell log)](/images/5-Workshop/5.4-aws-eks/verify-phase3-live.png)

#### Browser verification

1. Open the ALB URL.
2. Confirm the home page displays products.
3. Add a product to the cart to verify frontend, cartservice, and Redis.

![Online Boutique home page via ALB (real browser capture)](/images/5-Workshop/5.4-aws-eks/alb-browser-real.png)

{{% notice note %}}
Phase 1 on EKS focuses on core services. The full checkout flow is still tested on Docker Compose because additional supporting services are required.
{{% /notice %}}

#### Check Argo CD UI

~~~powershell
kubectl port-forward svc/argocd-server -n argocd 8081:443
~~~

Open <code>https://localhost:8081</code> and confirm the <code>online-boutique</code> application is Synced and Healthy.

#### Result

After this step, you can conclude that the application has been deployed to EKS via GitOps and is accessible through the ALB.
