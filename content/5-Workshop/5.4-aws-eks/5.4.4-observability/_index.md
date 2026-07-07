---
title : "System Observability"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4.4 </b> "
---

#### Objective

After the application is running on EKS, add an observability layer to monitor cluster status, workloads, and selected AWS infrastructure metrics. This section uses CloudWatch alarms, Prometheus, and Grafana.

#### Update CloudWatch alarms

After the ALB has been created, run Terraform again to sync alarms that depend on the ALB:

~~~powershell
cd infra/environments/aws
terraform plan -out=tfplan
terraform apply tfplan
~~~

This demonstrates that infrastructure can be updated incrementally—not all resources need to be created on the first apply.

#### Install the monitoring stack

~~~powershell
$env:GRAFANA_ADMIN_PASSWORD = "admin-password"
.\scripts\install-monitoring.ps1
~~~

The script installs kube-prometheus-stack via Helm, using configuration in <code>observability/aws/helm-values/kube-prometheus-stack.yaml</code>.

#### Run Phase 4 verification

~~~powershell
.\scripts\verify-phase4.ps1
~~~

The script checks:

+ CloudWatch alarms for RDS and ALB.
+ Prometheus and Grafana pods in the <code>observability</code> namespace.
+ Grafana accessibility via port-forward.

![verify-phase4.ps1 output (real PowerShell log)](/images/5-Workshop/5.4-aws-eks/verify-phase4-live.png)

#### Access Grafana

~~~powershell
kubectl port-forward svc/monitoring-grafana -n observability 3000:80
~~~

Open <code>http://localhost:3000</code>, sign in with user <code>admin</code> and the configured password. Use the dashboard at:

~~~text
observability/aws/dashboards/cluster-overview.json
~~~

![Cluster overview - Online Boutique dashboard on Grafana (real browser capture)](/images/5-Workshop/5.4-aws-eks/grafana-phase4-live.png)

#### CloudWatch

In the AWS Console, open CloudWatch Alarms to check RDS and ALB alarms. Immediately after creation, some alarms may be in INSUFFICIENT_DATA state because metrics data is not yet available.

#### Result

After this step, the system has a basic observability layer for both AWS infrastructure and Kubernetes workloads.
