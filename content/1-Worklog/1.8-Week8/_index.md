---
title: "Week 8 Worklog"
date: 2026-06-22
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}}
⚠️ **Warning:** All content below is intended for reference purposes only; strictly **do not copy verbatim** into your personal report.
{{% /notice %}}

### Internship Period

**June 22, 2026 - June 28, 2026**

### Week 8 Objectives

* Configure an advanced system for collecting, storing, and analyzing logs with Amazon CloudWatch Logs.
* Set up CloudWatch Alarms to detect abnormal conditions and support operational alerts.
* Learn how to use AWS Systems Manager (SSM) for centralized virtual-server management.
* Practice managing server configuration and deploying security patches in a controlled manner.

### Internship Activities

#### 1. Log Management with CloudWatch Logs

I studied **Amazon CloudWatch Logs** and how it centralizes logs from different sources for monitoring, analysis, and incident investigation. The practical work focused on organizing logs into log groups and log streams and selecting an appropriate retention period.

The main activities included:

* Reviewing log groups, log streams, log events, and timestamps in CloudWatch Logs.
* Learning how logs from resources or applications can be collected in a centralized location.
* Searching for errors, warnings, and important information in log data.
* Filtering and analyzing logs to identify when an incident occurred and investigate its cause.
* Reviewing log-retention settings to balance investigation requirements with storage costs.

Centralized logging reduces the need to access each server individually, makes it easier to compare events across components, and supports review of the system's operational history.

#### 2. Configuring CloudWatch Alarms

I practiced configuring **CloudWatch Alarms** based on predefined metrics and conditions. An alarm monitors a metric over a specified period and changes state when the configured threshold is met or exceeded.

The activities included:

* Selecting a metric and defining the condition to be monitored.
* Configuring thresholds, evaluation periods, and the number of consecutive breaches.
* Reviewing the `OK`, `ALARM`, and `INSUFFICIENT_DATA` states.
* Examining state-change history to identify when an alarm condition occurred.
* Connecting alarms to an appropriate notification or response action.

I validated the alarm by observing metric data and comparing it with the alarm state. This exercise demonstrated how early detection can be used when a resource shows signs of overload or unexpected behavior.

#### 3. Exploring AWS Systems Manager

I studied **AWS Systems Manager (SSM)**, a service that supports centralized management of servers and resources in an AWS environment. SSM can perform administration tasks without requiring a manual SSH or RDP connection to each server.

The topics reviewed included:

* Checking the requirements for a server to be managed by SSM, including the SSM Agent, an IAM instance profile, and the required connectivity.
* Reviewing managed nodes through Fleet Manager or related Systems Manager views.
* Using Run Command to execute administrative commands on one or more servers.
* Exploring Parameter Store for centralized storage and management of configuration parameters.
* Reviewing command history, execution results, and error messages to verify administrative operations.

Centralized management helps standardize operations across multiple servers, reduces errors caused by manual work, and provides a record of configuration changes.

#### 4. Centralized Configuration Management and Security Patching

I explored the process of managing server configuration and applying security updates through SSM. The work focused on checking patch status, identifying missing updates, and planning deployments within a controlled scope.

The main steps included:

* Reviewing the operating system, configuration details, and management status of each server.
* Using Patch Manager to identify missing security patches according to a selected baseline or criteria.
* Assessing the potential impact before installing patches and selecting an appropriate group of servers.
* Applying updates according to a schedule or in groups to limit the effect on running systems.
* Verifying the status after patching and confirming the result for each server.
* Reviewing logs and execution history for auditing, troubleshooting, and reporting.

I learned that centralized patching should be combined with testing, backups, and an appropriate recovery plan. Changes should not be deployed broadly without first evaluating their possible effects on applications and related services.

### Week 8 Achievements

* Understood how to organize and manage centralized logs using CloudWatch Logs.
* Practiced searching, filtering, and analyzing logs to support incident detection and investigation.
* Configured and tested CloudWatch Alarms with appropriate thresholds, evaluation periods, and states.
* Understood the role of AWS Systems Manager in centralized virtual-server management.
* Learned the process of reviewing server configuration, identifying missing patches, and managing security updates through SSM Patch Manager.
* Practiced monitoring command results, execution history, and server status after updates.
* Improved awareness of the importance of testing, IAM permissions, backups, and recovery plans before changing server configurations or applying patches.

### Reference Materials

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon CloudWatch Logs User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html)
* [AWS Systems Manager User Guide](https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html)
* [AWS Systems Manager Patch Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/patch-manager.html)

