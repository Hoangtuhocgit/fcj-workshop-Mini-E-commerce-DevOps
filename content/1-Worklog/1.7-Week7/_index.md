---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 objectives:

* Review Week 6 topics: migration strategy, AWS VM Import/Export, AWS DMS, and AWS SCT.
* Learn the overall approach to optimizing systems on AWS after workload migration.
* Practice operational automation with AWS Lambda, monitoring with CloudWatch/Grafana, and resource management with tags and Resource Groups.
* Understand IAM Resource Tag policies, AWS Systems Manager, Session Manager, and AWS CloudFormation.

### Week timeframe: **June 1–7, 2026**

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference material |
| --- | --- | --- | --- | --- |
| 2 | Review Week 6 content on migration strategy, AWS VM Import/Export, AWS DMS, and AWS SCT. <br> **System optimization overview on AWS:** <br>&emsp; + Understand optimization goals across operations, security, reliability, performance, and cost. <br>&emsp; + Connect migration knowledge with post-migration operations on AWS. | June 1, 2026 | June 1, 2026 | <https://cloudjourney.awsstudygroup.com/3-optimize/> |
| 3 | **Operational automation and EC2 cost optimization with AWS Lambda:** <br>&emsp; + Learn how to use Lambda to automatically start/stop EC2 instances by tag or schedule, with optional Slack webhook notifications. <br>&emsp; + Practice simulating EC2 creation, tagging, Lambda IAM Roles, start/stop functions, and verifying results. | June 2, 2026 | June 3, 2026 | <https://000022.awsstudygroup.com/> |
| 4 | **System monitoring with Amazon CloudWatch and Grafana:** <br>&emsp; + Reinforce CloudWatch metrics, logs, alarms, and dashboards for day-to-day operations. <br>&emsp; + Learn how to install Grafana on a Linux EC2 instance, connect CloudWatch as a data source, and build EC2 monitoring dashboards. <br> **Resource management with tags and Resource Groups:** <br>&emsp; + Understand how tags classify resources by environment, purpose, owner, and cost. <br>&emsp; + Practice tagging EC2/EBS resources, filtering by tag, and creating Resource Groups for centralized management. | June 3, 2026 | June 4, 2026 | <https://000029.awsstudygroup.com/><br><https://000027.awsstudygroup.com/> |
| 5 | **EC2 access control with IAM Resource Tag policies:** <br>&emsp; + Learn how to build IAM policies with tag-based conditions to enforce least privilege. <br>&emsp; + Explore IAM Users, IAM Roles, assume role, and verify create/modify EC2 permissions when tags meet conditions. <br> **AWS Systems Manager, Session Manager, and CloudFormation:** <br>&emsp; + Understand Systems Manager for centralized management, Patch Manager, and Run Command across servers. <br>&emsp; + Learn Session Manager for safer public/private EC2 access, reducing direct SSH/RDP exposure and enabling session logging. | June 4, 2026 | June 5, 2026 | <https://000028.awsstudygroup.com/><br><https://000031.awsstudygroup.com/><br><https://000058.awsstudygroup.com/> |
| 6 | **AWS CloudFormation:** <br>&emsp; + Understand CloudFormation, Infrastructure as Code, templates, stacks, rollback, and drift detection. <br>&emsp; + Practice simulating basic resource deployment with a template and observing stack status. <br> **Cleanup:** Remove lab resources—EC2 instances, security groups, IAM Roles, Lambda functions, CloudWatch alarms, Grafana instances, Resource Groups, Systems Manager test configurations, and CloudFormation stacks—to limit unexpected charges. | June 5, 2026 | June 7, 2026 | <https://000037.awsstudygroup.com/> |

### Week 7 achievements:

* Understands the direction for optimizing systems after deployment or migration to AWS.

* Can use Lambda, tags, Resource Groups, IAM Resource Tag policies, CloudWatch/Grafana, Systems Manager, Session Manager, and CloudFormation at a basic level.

* Strengthens skills in operational automation, monitoring, access control, resource management, and cost optimization on AWS.
