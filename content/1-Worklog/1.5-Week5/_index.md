---
title: "Week 5 Worklog"
date: 2026-06-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---
{{% notice warning %}}
⚠️ **Warning:** All content below is intended for reference purposes only; strictly **do not copy verbatim** into your personal report.
{{% /notice %}}
### Internship Period

**June 01, 2026 - June 07, 2026**

### Week 5 Objectives

* Establish system-monitoring metrics using AWS automated monitoring tools.
* Learn how to collect, view, and interpret operational metrics for cloud resources and services.
* Practice using the AWS Command Line Interface (AWS CLI) to configure, manage, and modify cloud services.
* Develop a consistent command-line workflow that can support repeatable operations and future automation.

### Internship Activities

#### 1. Establishing System Monitoring Metrics

I explored **Amazon CloudWatch**, AWS's monitoring and observability service. CloudWatch can collect metrics, logs, and events from AWS resources and services, allowing system health and operational behavior to be monitored continuously.

The main activities included:

* Identifying important metrics such as CPU utilization, network traffic, request counts, and resource status.
* Viewing metric data through CloudWatch dashboards to assess system conditions.
* Reviewing logs and events to support troubleshooting when a service does not behave as expected.
* Defining suitable thresholds for metrics that require monitoring.
* Learning how CloudWatch alarms transition between `OK`, `ALARM`, and `INSUFFICIENT_DATA` states based on incoming metric data.

This work demonstrated the value of proactive monitoring. Regular observation of system metrics can help identify abnormal behavior early, support incident response, and provide evidence for performance improvements.

#### 2. Using the AWS CLI

I configured and used the **AWS Command Line Interface (AWS CLI)** to manage AWS resources from the command line. Before performing the exercises, I reviewed the authentication configuration, default Region, active profile, and permissions of the IAM user or role being used.

The AWS CLI makes repeated operations faster and can be incorporated into scripts and automated workflows. I also verified the profile, Region, and access permissions before each operation to avoid modifying unrelated resources.

#### 3. Configuring and Managing Cloud Services

I practiced the basic lifecycle of cloud-service management through AWS CLI commands:

* **Create:** provision a resource or add a new configuration using the appropriate service command.
* **Update:** modify the properties, configuration, or settings of an existing resource.
* **Delete:** remove test resources after completing the exercise to avoid unnecessary charges.
* **Inspect:** use query or describe commands to confirm that a resource was created and configured correctly.

For each operation, I reviewed the command syntax, identified required parameters, and checked the returned output. This helped reduce errors caused by an incorrect resource name, Region, parameter, or IAM permission.

#### 4. Checking Service Status

I used AWS CLI commands to check the status of resources and services after they were created or modified. The returned information was compared with the expected state to determine whether an operation had completed or was still in progress.

The validation process included:

* Querying resource details with `describe`, `get`, or service-specific commands.
* Comparing the resource state before and after a configuration change.
* Reviewing error messages when a command failed because of missing permissions, invalid parameters, or a resource that could not be found.
* Monitoring related changes in CloudWatch when an operation affected system behavior.
* Confirming and cleaning up temporary resources after completing the practice tasks.

### Week 5 Achievements

* Understood the role of Amazon CloudWatch in collecting metrics, monitoring logs and events, and issuing alerts about system conditions.
* Established and reviewed basic monitoring metrics and learned the meaning of CloudWatch alarm states.
* Used the AWS CLI to query and manage AWS resources from the command line.
* Practiced creating, updating, deleting, and inspecting resources as part of a basic management lifecycle.
* Learned how to check service status, interpret command output, and troubleshoot common configuration errors.
* Improved awareness of IAM permissions, Region selection, and resource cleanup for security and cost control.

### Reference Materials

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon CloudWatch User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html)
* [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/reference/)

