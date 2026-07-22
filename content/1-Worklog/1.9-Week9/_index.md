---
title: "Week 9 Worklog"
date: 2026-06-29
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}}
⚠️ **Warning:** All content below is intended for reference purposes only; strictly **do not copy verbatim** into your personal report.
{{% /notice %}}

### Internship Period

**June 29, 2026 - July 05, 2026**

### Week 9 Objectives

* Manage advanced IAM permissions using IAM Permission Boundaries.
* Monitor network traffic with VPC Flow Logs.
* Build automated backup and recovery plans for EBS volumes using AWS Backup.
* Provide technical support for the **First Cloud Security Journey** event.

### Internship Activities

#### 1. Managing Permission Boundaries for IAM

I studied **IAM Permission Boundaries**, a mechanism used to define the maximum permissions that an IAM user or role can receive. A permission boundary does not grant permissions by itself; instead, it limits the maximum permissions available when combined with identity-based policies.

The activities included:

* Distinguishing permission boundaries from identity-based and resource-based policies.
* Creating a policy to use as a permission boundary for an IAM user or role.
* Restricting the actions and resources available to an IAM identity.
* Testing a case in which a broad identity policy was still limited by the permission boundary.
* Reviewing how boundaries can help prevent users from granting themselves additional permissions or creating roles with excessive access.

This exercise demonstrated how permission boundaries support layered access control. Even when an identity policy grants broader permissions, the IAM identity cannot exceed the maximum scope defined by its boundary.

#### 2. Monitoring Network Traffic with VPC Flow Logs

I studied **VPC Flow Logs**, which record information about IP traffic passing through network interfaces in a VPC. Flow-log data can support connection analysis, access verification, and investigation of network-related security issues.

The main activities included:

* Selecting the required logging scope at the VPC, Subnet, or network-interface level.
* Configuring an appropriate destination, such as CloudWatch Logs, for the flow-log records.
* Reviewing fields such as source, destination, protocol, port, action, and accept or reject status.
* Filtering `ACCEPT` and `REJECT` records to distinguish permitted and blocked traffic.
* Comparing flow logs with Security Group, Network ACL, and route configuration when a connection failed.

VPC Flow Logs do not capture packet contents, but they provide useful information about traffic sources, destinations, direction, and processing results. This makes them valuable for network monitoring and security analysis.

#### 3. Building an Automated EBS Backup and Recovery Plan

I studied **AWS Backup** and practiced creating an automated backup plan for Amazon EBS volumes. A backup plan standardizes the schedule, retention period, and scope of the resources that need protection.

The activities included:

* Creating a backup vault to store recovery points.
* Creating a backup plan with an appropriate recurring schedule.
* Configuring the lifecycle and retention period for backups.
* Assigning EBS resources to the plan through tags or explicit resource selection.
* Checking backup jobs, completion status, and the recovery points that were created.
* Reviewing the recovery process for restoring a volume from a backup.

During the exercise, I considered the relationship between backup frequency, retention requirements, recovery needs, and cost. Regularly checking backup jobs and testing recovery are necessary to verify that backups can be used when an incident occurs.

#### 4. Providing Technical Support for the First Cloud Security Journey

I provided technical support for the **First Cloud Security Journey** event. The support focused on helping participants access learning materials, prepare their practice environments, and resolve basic issues involving AWS accounts or services.

The support activities included:

* Guiding participants through the prerequisites before they started the hands-on exercises.
* Helping identify common issues related to IAM permissions, AWS Regions, network configuration, or unavailable resources.
* Recording questions, categorizing issues, and coordinating with the responsible team members.
* Guiding participants through result verification after each step and reminding them to clean up resources after completing the exercises.
* Monitoring overall progress and helping maintain a stable hands-on learning experience.

This activity improved my technical communication, structured troubleshooting, and ability to explain solutions clearly to participants with different levels of experience.

### Week 9 Achievements

* Understood the role of IAM Permission Boundaries in defining maximum permissions for IAM users and roles.
* Practiced layered permission control and tested the effect of a boundary when an identity policy granted broader access.
* Learned how to configure VPC Flow Logs to record and analyze network traffic.
* Used flow-log fields to investigate connections and distinguish accepted from rejected requests.
* Built an automated EBS backup plan with AWS Backup, including scheduling, retention, and recovery points.
* Understood how to verify backup jobs and restore resources from backups.
* Provided technical support for the First Cloud Security Journey event and strengthened troubleshooting and user-guidance skills.

### Reference Materials

* [AWS Documentation](https://docs.aws.amazon.com/)
* [IAM Permissions Boundaries](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_boundaries.html)
* [VPC Flow Logs](https://docs.aws.amazon.com/vpc/latest/userguide/flow-logs.html)
* [AWS Backup User Guide](https://docs.aws.amazon.com/aws-backup/latest/devguide/whatisbackup.html)

