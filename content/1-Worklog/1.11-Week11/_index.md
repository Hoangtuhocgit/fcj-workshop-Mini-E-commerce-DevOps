---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 objectives:

* Review Week 10 topics on Docker, ECR, and foundational AWS container services.
* Practice packaging multi-service applications with Docker Compose and deploy containers on Lightsail Container Service.
* Learn CI/CD for containers, the Monolith to Microservices model, and deploy workloads on EKS/Fargate at a more advanced level.

### Week timeframe: **June 29–July 5, 2026**

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference material |
| --- | --- | --- | --- | --- |
| 2 | Review Week 10 content on Docker, ECR, ECS, Fargate, and EKS. <br> **Docker Compose and multi-container applications:** <br>&emsp; + Write a <code>docker-compose.yml</code> for an app with frontend, API, and database. <br>&emsp; + Understand service dependencies, internal networking, volumes, and health checks locally. | June 29, 2026 | June 29, 2026 | [Cloud Journey – Modernize](https://cloudjourney.awsstudygroup.com/4-modernize/)<br>[Lab 15](https://000015.awsstudygroup.com/) |
| 3 | **Amazon Lightsail Container Service:** <br>&emsp; + Create a Lightsail container service, push an image, and deploy a simple container on AWS. <br>&emsp; + Compare Lightsail Container with ECS/Fargate for operational complexity and cost on small workloads. | June 30, 2026 | June 30, 2026 | [Lab 67](https://000067.awsstudygroup.com/) |
| 4–5 | **Monolith to Microservices:** <br>&emsp; + Analyze how to split a monolith into microservices by bounded context. <br>&emsp; + Package each service as its own image and prepare registry and independent deploy configuration. | July 1, 2026 | July 2, 2026 | [Cloud Journey – Modernize](https://cloudjourney.awsstudygroup.com/4-modernize/) |
| 6 | **CI/CD for containers:** <br>&emsp; + Learn pipelines to build images, push to ECR, and update deployment manifests. <br>&emsp; + Get familiar with GitHub Actions (or CodePipeline) for a basic build — scan — deploy flow. | July 3, 2026 | July 3, 2026 | [Lab 126](https://000126.awsstudygroup.com/) |
| 7–Sun | **Advanced deployment on EKS/Fargate:** <br>&emsp; + Deploy core services with Deployment and Service on EKS; verify pods, replicas, and self-healing. <br>&emsp; + Monitor status with kubectl and CloudWatch; prepare groundwork for the project workshop. <br> **Post-lab cleanup:** <br>&emsp; + Remove Lightsail services, trial EKS/Fargate workloads, unused images, and review ECR to limit charges. | July 4, 2026 | July 5, 2026 | [Lab 126](https://000126.awsstudygroup.com/)<br>[Lab 67](https://000067.awsstudygroup.com/) |

### Week 11 achievements:

* Can use Docker Compose to run multi-service applications locally.

* Have hands-on experience deploying containers on Lightsail Container Service and comparing with ECS/Fargate.

* Understand the direction of splitting monoliths into microservices and packaging services independently.

* Grasp basic CI/CD for containers and deploy workloads on EKS/Fargate at a deeper level than Week 10.
