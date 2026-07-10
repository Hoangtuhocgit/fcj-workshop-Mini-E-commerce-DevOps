---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 objectives:

* Review Week 5 topics: AWS Support, AWS CLI on EC2, and the Highly Available Web Application model.
* Learn the overall strategy for migrating systems to AWS.
* Understand virtual server migration with AWS VM Import/Export and database migration with AWS DMS and AWS SCT.
* Reinforce security, networking, and monitoring during migration, and clean up lab resources afterward.

### Week timeframe: **May 25–31, 2026**

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference material |
| --- | --- | --- | --- | --- |
| 2 | Review Week 5 content on AWS Support, AWS CLI on EC2, the highly available web application model, and the related deployment workshop. | May 25, 2026 | May 25, 2026 | <https://cloudjourney.awsstudygroup.com/2-migrate/> |
| 3 | **Migration strategy to AWS:** <br>&emsp; + Understand migration concepts and the role of workload assessment before moving to the cloud. <br>&emsp; + Learn the basic steps: assess the system, plan, migrate, test, and optimize after migration. <br>&emsp; + Recognize common risks such as downtime, network misconfiguration, permission errors, data loss, and unexpected costs. | May 26, 2026 | May 26, 2026 | <https://cloudjourney.awsstudygroup.com/2-migrate/> |
| 4–5 | **Virtual server migration with AWS VM Import/Export:** <br>&emsp; + Understand how VM Import/Export moves virtual machines from local/on-premises environments to AWS. <br>&emsp; + Learn the workflow: prepare the VM image, upload to Amazon S3, and import as an Amazon Machine Image or EC2 instance. <br>&emsp; + Review related components such as S3 buckets, IAM Roles, EC2, AMIs, image formats, data security, and cost. | May 27, 2026 | May 28, 2026 | <https://000014.awsstudygroup.com/> |
| 6–7 | **Database migration with AWS DMS and AWS SCT:** <br>&emsp; + Understand the role of AWS DMS in moving data between source and target databases. <br>&emsp; + Learn about replication instances, source/target endpoints, migration tasks, and migration types such as full load and CDC. <br>&emsp; + Explore AWS SCT for schema conversion when source and target engines differ. <br>&emsp; + Practice simulating source/target databases, configuring endpoints, creating migration tasks, and validating data after migration. | May 29, 2026 | May 30, 2026 | <https://000043.awsstudygroup.com/> |
| Sun | **Security, networking, and monitoring during migration:** <br>&emsp; + Review security groups, subnets, route tables, IAM permissions, snapshots/backups, and rollback options when needed. <br>&emsp; + Monitor logs, metrics, and migration task status with CloudWatch or the AWS management console. <br> **Cleanup:** Remove lab resources—EC2 instances, AMIs, S3 objects, RDS instances, replication instances, endpoints, migration tasks, and snapshots—to limit unexpected charges. | May 31, 2026 | May 31, 2026 | <https://000043.awsstudygroup.com/><br><https://000014.awsstudygroup.com/> |

### Week 6 achievements:

* Understands the overall process of migrating workloads from traditional environments to AWS.

* Knows the role of AWS VM Import/Export in virtual server migration.

* Understands how AWS DMS and SCT support database migration and schema conversion.

* Knows what to verify after migration: data integrity, application connectivity, security, logs, and cost.

* Strengthens skills in planning, testing, monitoring, and cleaning up resources after AWS lab work.
