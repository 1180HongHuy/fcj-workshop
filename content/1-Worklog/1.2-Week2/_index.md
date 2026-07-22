---
title: "Week 2 Worklog"
date: 2026-05-11
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}}
⚠️ **Warning:** All content below is intended for reference purposes only; strictly **do not copy verbatim** into your personal report.
{{% /notice %}}

### Internship Period

**May 11, 2026 - May 17, 2026**

### Week 2 Objectives

* Practice the basic steps for launching and configuring a virtual server with Amazon EC2.
* Understand how AWS networking resources are organized through a VPC, Subnet, and Security Group.
* Study the fundamental concepts of Cloud Computing and the AWS Shared Responsibility Model.
* Build the foundation required to deploy AWS resources securely and manage them effectively.

### Internship Activities

#### 1. Cloud Computing Theory

I studied the fundamental concepts of **Cloud Computing**, including the on-demand delivery of information technology resources over the Internet. The study focused on key characteristics such as elasticity, scalability, self-service resource provisioning, and usage-based billing.

I also reviewed the main cloud service models: **Infrastructure as a Service (IaaS)**, **Platform as a Service (PaaS)**, and **Software as a Service (SaaS)**. This helped me understand the position of Amazon EC2 as an IaaS offering and the responsibilities of the provider and customer in each service model.

#### 2. AWS Shared Responsibility Model

I researched the **AWS Shared Responsibility Model**, which divides security responsibilities between AWS and the customer:

* AWS is responsible for security **of** the cloud, including the physical infrastructure, hardware, core networking, and foundational services operated by AWS.
* The customer is responsible for security **in** the cloud, including data, operating systems, applications, network configuration, access permissions, and service-specific security settings.
* The customer's responsibilities vary depending on the service used. With Amazon EC2, the customer is responsible for managing the guest operating system, patches, installed software, data, and network access rules.

Understanding this model clarified that using AWS does not eliminate the customer's security responsibilities. AWS secures the underlying cloud infrastructure, while customers must configure and operate their resources correctly.

#### 3. Amazon EC2 Virtual Server Lab

I practiced launching a virtual server using **Amazon EC2** through the AWS Management Console. The main activities included:

* Selecting a suitable Amazon Machine Image (AMI) for the server's operating system.
* Choosing an EC2 instance type and basic resource configuration for the lab requirements.
* Creating or selecting a key pair for secure server authentication.
* Reviewing the network settings and configuration options before launching the instance.
* Checking the instance status after launch and reviewing information such as its IP address, state, and associated Security Group.

#### 4. VPC, Subnet, and Security Group Configuration

As part of the lab, I studied the relationship between the core AWS networking components:

* **Amazon VPC:** an isolated virtual network in which AWS resources can be deployed and managed.
* **Subnet:** a segment of a VPC associated with a specific Availability Zone, used to organize resources within the network.
* **Security Group:** a virtual firewall at the EC2 instance level that controls inbound and outbound traffic through configured rules.

I practiced selecting a VPC and Subnet when launching an EC2 instance and configuring a Security Group with the access rules required for the lab. This exercise demonstrated the importance of opening only the necessary ports, protocols, and source addresses instead of allowing broader network access than required.

### Week 2 Achievements

* Developed a foundational understanding of Cloud Computing and the IaaS, PaaS, and SaaS service models.
* Understood how security responsibilities are divided between AWS and the customer under the Shared Responsibility Model.
* Completed the basic steps for launching a virtual server with Amazon EC2.
* Understood the roles and relationship of a VPC, Subnet, and Security Group in an AWS network architecture.
* Practiced configuring Security Group rules according to the lab's access requirements and recognized the importance of least-privilege network access.
* Established the foundation for further study of AWS networking, security, and application deployment.

### Reference Materials

* [AWS Documentation](https://docs.aws.amazon.com/)
* [AWS Cloud Journey](https://cloudjourney.awsstudygroup.com/)


