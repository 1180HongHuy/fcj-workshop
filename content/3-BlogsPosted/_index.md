---
title: "Blogs Posted"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}

This section lists and introduces the blog posts that have been published on the [AWS Study Group](https://www.facebook.com/groups/awsstudygroupfcj).

### [Blog 1: Building a Serverless Travel Booking System on AWS](3.1-Blog1/)
This article presents a complete solution for building an online travel booking system using a Cloud-Native Serverless architecture on Amazon Web Services (AWS). The architecture is designed to optimize operational costs while providing automatic scalability. The system is divided into multiple independent layers, including the networking and security layer (Route 53, AWS WAF), frontend layer (Amazon CloudFront and Amazon S3), authentication and API layer (Amazon Cognito and API Gateway), and the application logic and data layer (AWS Lambda, Amazon DynamoDB, and Amazon CloudWatch). The article also explains the complete request flow, from the user interface and JWT authentication to backend processing and real-time data storage.

### *Note: Blog 2 has been submitted but is still awaiting approval.*

### [Blog 2: AWS Lambda (Serverless) – When Should You Use It and How Can You Maximize Performance?](3.2-Blog2/)
This article discusses the most common use cases for AWS Lambda, including real-time event processing, building RESTful APIs, and automating system operations. It also provides practical techniques for improving performance while reducing latency and operational costs, such as reusing database connections through the global scope, minimizing deployment package size, allocating memory strategically to increase available vCPUs, and integrating Amazon RDS Proxy for efficient connection pooling.

### *Note: Blog 3 has been submitted but is still awaiting approval.*

### [Blog 3: Exploring and Optimizing Large-Scale Data Management with Amazon S3 Metadata](3.3-Blog3/)
This article examines the challenges of searching and managing billions of objects stored in Amazon S3, where traditional approaches such as the ListObjectsV2 API or custom synchronization pipelines to DynamoDB or Elasticsearch become increasingly complex and expensive. It introduces Amazon S3 Metadata as a more efficient solution, enabling organizations to query object attributes—including size, last access time, tags, and storage class—quickly and efficiently. By eliminating unnecessary infrastructure complexity, developers can spend less time managing metadata and more time focusing on data analysis and business value.