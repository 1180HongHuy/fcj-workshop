---
title: "Week 4 Worklog"
date: 2026-05-27
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---
{{% notice warning %}}
⚠️ **Warning:** All content below is intended for reference purposes only; strictly **do not copy verbatim** into your personal report.
{{% /notice %}}

### Internship Period

**May 25, 2026 - May 31, 2026**

### Week 4 Objectives

* Explore cloud architecture design principles that support performance, scalability, and system reliability.
* Understand how to select and organize storage resources according to application requirements.
* Practice creating, managing, and securing Amazon S3 and Amazon EBS storage services.
* Improve the ability to configure access permissions according to the principle of least privilege and protect data on AWS.

### Internship Activities

#### 1. Exploring Performance-Oriented Cloud Architecture

I explored cloud architecture design solutions that aim to improve performance, scalability, and availability. The study focused on analyzing application requirements, selecting suitable AWS services, and separating the system into components that can be scaled and managed independently.

The main design principles reviewed included:

* Selecting resource types and configurations that match the application's workload.
* Separating storage, processing, and access layers to simplify scaling, monitoring, and maintenance.
* Reducing bottlenecks by distributing resources and optimizing how applications access data.
* Using suitable storage, caching, or content delivery mechanisms to reduce latency.
* Monitoring performance, resource utilization, and costs to support architectural improvements.

This study showed me that an optimized architecture is not based on processing speed alone. It must balance performance, scalability, availability, security, and operating cost.

#### 2. Practicing with Amazon S3

I practiced using **Amazon S3** to create and manage object storage. The main activities included:

* Creating an S3 bucket with an appropriate name and configuration.
* Uploading, viewing, downloading, and deleting objects in the bucket.
* Understanding the concepts of buckets, objects, keys, and metadata in the S3 storage model.
* Reviewing access-control and data-protection options for S3 buckets.
* Testing how access can be granted to users or services through IAM policies.

During the exercise, I avoided making data publicly accessible unless it was required and reviewed access controls at the bucket and object levels. This helped reinforce the importance of protecting stored data from unauthorized access.

#### 3. Practicing with Amazon EBS

I studied **Amazon Elastic Block Store (Amazon EBS)**, which provides persistent block storage for use with Amazon EC2 instances. The practical activities included:

* Learning the concepts of volumes, snapshots, and attaching volumes to EC2 instances.
* Creating an EBS volume with a suitable type and capacity for the lab.
* Attaching the volume to an EC2 instance and checking its connection status.
* Reviewing how to manage, resize, and detach a volume when necessary.
* Studying snapshots as an option for data backup and recovery.

The exercise helped me distinguish Amazon S3 from Amazon EBS. S3 is highly scalable object storage, while EBS provides block storage that can be attached to an EC2 instance for its operating system and applications.

#### 4. Storage Service Permissions and Security

I studied how AWS IAM can be used to control access to Amazon S3 and Amazon EBS. Permissions were considered according to the principle of granting each user or service only the access required for its tasks, rather than assigning broad administrative privileges.

The topics reviewed included:

* Distinguishing identity-based policies from resource-based policies for access control.
* Identifying the required actions, such as creating, reading, writing, listing, or deleting resources.
* Restricting policies by resource and action instead of granting unnecessarily broad permissions.
* Testing permissions after configuration to confirm that users could perform only their assigned tasks.
* Combining access protection with monitoring, backup, and data lifecycle management.

### Week 4 Achievements

* Understood key principles for designing cloud architectures that support performance, scalability, availability, and cost optimization.
* Created and practiced managing buckets and objects in Amazon S3.
* Understood the characteristics of Amazon EBS and practiced creating, attaching, and managing an EBS volume for an EC2 instance.
* Distinguished the appropriate use cases for Amazon S3 and Amazon EBS in an AWS architecture.
* Applied IAM policies to control access to storage services according to the principle of least privilege.
* Built a foundation for further study of AWS storage, backup, and architecture optimization solutions.

### Reference Materials

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon S3 User Guide](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)
* [Amazon EBS User Guide](https://docs.aws.amazon.com/ebs/latest/userguide/what-is-ebs.html)

