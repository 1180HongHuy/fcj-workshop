---
title: "Week 3 Worklog"
date: 2026-05-18
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---
{{% notice warning %}}
⚠️ **Warning:** All content below is intended for reference purposes only; strictly **do not copy verbatim** into your personal report.
{{% /notice %}}

### Internship Period

**May 18, 2026 - May 24, 2026**

### Week 3 Objectives

* Explore the role and operating principles of AWS Lambda in a serverless architecture.
* Learn how to use Amazon API Gateway to create and manage APIs that integrate with Lambda.
* Deploy a sample web application to AWS and verify data connectivity between the user interface and backend services.
* Practice validating requests, responses, and basic configuration errors during service integration.

### Internship Activities

#### 1. Exploring AWS Lambda

I studied **AWS Lambda** as a serverless compute service that runs code in response to events without requiring direct server management. The study covered fundamental concepts such as functions, runtimes, handlers, events, and execution roles.

I created a sample Lambda function, configured the appropriate runtime, and tested it with sample events. This exercise helped me understand how Lambda receives input data, processes application logic, and returns output data to the calling service.

#### 2. Exploring Amazon API Gateway

I studied **Amazon API Gateway** and its role in providing endpoints that allow a frontend application to communicate with a backend service. The main activities included:

* Creating an API and configuring the required resources, routes, or endpoints.
* Setting up HTTP methods such as `GET` and `POST`.
* Integrating API Gateway with a Lambda function to receive and process requests.
* Learning how request data is passed to Lambda and how responses are returned to the client.
* Testing the endpoint through the AWS Console and reviewing the returned results.

Through this exercise, I understood that API Gateway acts as an intermediary layer: it receives requests from the application, routes them to Lambda, and sends the processed results back to the client.

#### 3. Deploying a Demo Web App to AWS

I deployed a **Demo Web App** to AWS to verify connectivity between the frontend, API Gateway, and Lambda. The main steps included:

* Preparing the source code and configuring the API endpoint for the sample web application.
* Deploying the web interface to a suitable AWS hosting environment.
* Configuring the frontend to call the endpoint provided by API Gateway.
* Connecting API Gateway to a Lambda function that handled the backend logic.
* Sending requests from the web interface and checking the data returned by the backend.

#### 4. Validating Data Connectivity

I tested the data flow in the following sequence: the user interacted with the frontend, the frontend sent a request to API Gateway, API Gateway forwarded the request to Lambda, and the result was returned to the interface.

During testing, I compared request and response contents, confirmed that the correct endpoint was being called, checked HTTP status codes, and reviewed the result displayed in the Demo Web App. I also reviewed basic configuration issues, such as an incorrect endpoint, an invalid HTTP method, or an incompatible data format, to ensure that the components communicated correctly.

### Week 3 Achievements

* Understood the operating model and fundamental components of AWS Lambda.
* Created and successfully tested a sample Lambda function with defined input and output data.
* Gained an understanding of the role of Amazon API Gateway in exposing endpoints and connecting a frontend to a serverless backend.
* Deployed a Demo Web App to AWS and configured the application to call an API endpoint.
* Verified data exchange between the frontend, API Gateway, and Lambda through real request and response flows.
* Gained practical experience identifying and resolving basic configuration issues during AWS service integration.

### Reference Materials

* [AWS Documentation](https://docs.aws.amazon.com/)
* [AWS Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
* [Amazon API Gateway Developer Guide](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html)

