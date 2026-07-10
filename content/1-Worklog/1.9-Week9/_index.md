---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 objectives:

* Review Week 8 topics: security, reliability, performance, and cost optimization on AWS.
* Learn the application modernization path from monolith to microservices and serverless.
* Understand CI/CD, microservice decomposition, database-per-service, messaging/eventing, and container services on AWS.

### Week timeframe: **June 15–21, 2026**

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference material |
| --- | --- | --- | --- | --- |
| 2 | Review Week 8 content on security, reliability, performance, and cost optimization on AWS. <br> **Application modernization overview:** <br>&emsp; + Understand goals for moving from monolith to microservices, separating bounded contexts, and reducing dependencies. <br>&emsp; + Learn how to host applications on AWS and prepare automated release workflows. | June 15, 2026 | June 15, 2026 | <https://cloudjourney.awsstudygroup.com/4-modernize/> |
| 3–4 | **Monolith application migration:** <br>&emsp; + Analyze a Java Spring Boot/RDBMS application, identifying frontend, backend, database, and dependency points. <br>&emsp; + Learn the steps to move the application to AWS, configure the runtime environment, and verify connectivity after migration. | June 16, 2026 | June 17, 2026 | <https://000050.awsstudygroup.com/> |
| 5–6 | **Automated application release and microservice creation:** <br>&emsp; + Understand CI/CD pipelines, source/build/deploy stages, and post-deployment testing. <br>&emsp; + Learn how to split monolith functionality into independent microservices with separate APIs and data stores. <br> **Data restructuring, workflow, messaging, and eventing:** <br>&emsp; + Recognize shared-database issues, database-per-service approaches, and asynchronous communication with SQS/SNS or event-driven patterns. | June 18, 2026 | June 19, 2026 | <https://000051.awsstudygroup.com/><br><https://000052.awsstudygroup.com/><br><https://000053.awsstudygroup.com/><br><https://000054.awsstudygroup.com/> |
| 7 | **Application authentication and serverless:** <br>&emsp; + Explore SPAs, Amazon Cognito, API Gateway, Lambda, Step Functions, S3, DynamoDB, SAM, CloudWatch, and X-Ray. | June 20, 2026 | June 20, 2026 | <https://000055.awsstudygroup.com/><br><https://000081.awsstudygroup.com/> |
| Sun | **Introduction to container services and summary:** <br>&emsp; + Get an overview of Lightsail Container, Amazon EKS, AWS Fargate, and CI/CD on EKS with CodePipeline/GitHub. <br>&emsp; + Consolidate application modernization knowledge: CI/CD, microservices, separate databases, messaging/eventing, SPAs, Cognito, API Gateway, Lambda, and container services. <br> **Cleanup:** Remove lab resources—demo apps, test databases, API Gateway, Lambda, Cognito, S3, SQS/SNS, EKS/Lightsail Container demos, and pipelines—to limit unexpected charges. | June 21, 2026 | June 21, 2026 | <https://000046.awsstudygroup.com/><br><https://000126.awsstudygroup.com/><br><https://cloudjourney.awsstudygroup.com/4-modernize/> |

### Week 9 achievements:

* Understands the direction for modernizing applications from monolith to microservices and serverless on AWS.

* Knows the main components: CI/CD, microservices, separate databases, messaging/eventing, SPAs, Cognito, API Gateway, Lambda, and container services.

* Has an overview of ECS/EKS/Fargate and how containers combine with deployment pipelines.
