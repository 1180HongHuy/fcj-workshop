---
title: "Week 10 Worklog"
date: 2026-07-06
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---
{{% notice warning %}}
⚠️ **Warning:** All content below is intended for reference purposes only; strictly **do not copy verbatim** into your personal report.
{{% /notice %}}

### Internship Period

**July 06, 2026 - July 12, 2026**

### Week 10 Objectives

* Practice building an advanced security lab that combines multiple AWS security and protection services.
* Understand how AWS Security Hub, Amazon GuardDuty, Amazon Macie, and AWS Network Firewall contribute to a layered security architecture.
* Learn how to collect, consolidate, and respond to security findings from different sources.
* Brainstorm and prepare a detailed outline for a technology Workshop with clear learning outcomes and hands-on activities.

### Internship Activities

#### 1. Building an Advanced AWS Security Lab

I designed a lab scenario that simulated the protection of AWS resources and data. The lab combined multiple security layers: threat detection, sensitive-data discovery, centralized findings management, and network traffic control.

The main components included:

* **Amazon GuardDuty:** detecting suspicious activity and potential threats in the AWS account.
* **Amazon Macie:** discovering, classifying, and helping protect sensitive data stored in Amazon S3.
* **AWS Network Firewall:** inspecting and controlling network traffic according to configured rules.
* **AWS Security Hub:** aggregating security findings from multiple services and providing a centralized view of the security posture.

#### 2. Exploring Amazon GuardDuty and Amazon Macie

I explored how **Amazon GuardDuty** analyzes data sources and generates security findings when it detects suspicious behavior. I reviewed findings by severity, threat type, and affected resource to understand how they could be prioritized for investigation and response.

For **Amazon Macie**, I studied how the service helps discover sensitive data in S3 objects. The work focused on identifying data that required protection, reviewing discovery results, and assessing the risks of inappropriate sharing or overly permissive access settings.

These services demonstrated two different security perspectives. GuardDuty focuses on activity, events, and potential threats, while Macie focuses on sensitive data and data-protection risks.

#### 3. Configuring AWS Network Firewall

I studied **AWS Network Firewall** and its role in controlling traffic between network segments and protecting resources from unauthorized connections. The lab focused on identifying traffic that should be allowed, traffic that should be blocked, and rules required to enforce the intended security policy.

The practical activities included:

* Identifying the position of Network Firewall within a VPC architecture.
* Reviewing stateful and stateless rules and how they process traffic.
* Building rules based on protocols, addresses, ports, and connection direction.
* Testing permitted and blocked traffic after applying the firewall policy.
* Comparing test results with logs or security findings to support incident analysis.

I learned that firewall rules must be clearly scoped and thoroughly tested before wider deployment. This helps avoid blocking legitimate traffic or leaving unintended gaps in the security policy.

#### 4. Consolidating Findings with AWS Security Hub

I configured and explored **AWS Security Hub** as a central location for security findings from GuardDuty, Macie, and other security sources. Security Hub helps normalize, organize, and display findings so that administrators can prioritize remediation according to potential impact.

The main steps included:

* Enabling Security Hub and checking its status in the practice environment.
* Reviewing findings received from the configured security services.
* Categorizing findings by severity, control type, and affected resource.
* Learning how a finding can be connected to an investigation and remediation workflow.
* Checking the finding status after a response action and recording the result.

Centralized findings reduce the need to inspect each security service separately and support a more consistent incident-response process.

#### 5. Brainstorming and Outlining the Technology Workshop

Alongside the security lab, I brainstormed and prepared a detailed outline for a **technology Workshop**. The Workshop was planned around practical learner needs, combining concise theory with hands-on activities that produce verifiable results.

The outline included:

* Defining the topic, learning objectives, and target audience.
* Describing the prerequisites and foundational knowledge required before the Workshop.
* Dividing the content into introduction, demonstration, hands-on practice, and review sections.
* Allocating time for each activity, including support and troubleshooting time.
* Preparing a list of required resources, accounts, IAM permissions, and practice environments.
* Defining expected outcomes that participants could verify after completing the exercises.
* Anticipating common issues and preparing support procedures for the hands-on portion.

Creating the outline strengthened my ability to present technical knowledge in a logical sequence, anticipate learner difficulties, and prepare practical content that is easier to follow.

### Week 10 Achievements

* Completed the core scenario for an advanced AWS security lab combining Security Hub, GuardDuty, Macie, and Network Firewall.
* Understood the role of each service in threat detection, data protection, network control, and centralized findings management.
* Practiced reviewing finding severity, affected resources, and remediation status.
* Learned how to design traffic-control rules and validate their results with Network Firewall.
* Developed the topic, objectives, content, timing, and support process for a technology Workshop.
* Prepared a detailed outline containing theory, demonstrations, hands-on practice, result verification, and troubleshooting activities.

### Reference Materials

* [AWS Documentation](https://docs.aws.amazon.com/)
* [AWS Security Hub User Guide](https://docs.aws.amazon.com/securityhub/latest/userguide/what-is-securityhub.html)
* [Amazon GuardDuty User Guide](https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html)
* [Amazon Macie User Guide](https://docs.aws.amazon.com/macie/latest/user/what-is-macie.html)
* [AWS Network Firewall Developer Guide](https://docs.aws.amazon.com/network-firewall/latest/developerguide/what-is-aws-network-firewall.html)

