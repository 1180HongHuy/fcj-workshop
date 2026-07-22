---
title: "Week 7 Worklog"
date: 2026-06-15
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
{{% notice warning %}}
⚠️ **Warning:** All content below is intended for reference purposes only; strictly **do not copy verbatim** into your personal report.
{{% /notice %}}

### Internship Period

**June 15, 2026 - June 21, 2026**

### Week 7 Objectives

* Deploy a static ReactJS Single Page Application (SPA) to Amazon S3.
* Learn how to configure S3 for storing and serving the frontend build artifacts.
* Use Amazon CloudFront as a CDN to distribute website content efficiently to users in different locations.
* Configure HTTPS/SSL and security settings for the website's CloudFront delivery.

### Internship Activities

#### 1. Preparing and Building the ReactJS SPA

I prepared the ReactJS frontend source code and reviewed its configuration before deployment. The application followed the **Single Page Application (SPA)** model, in which most content loading and navigation are handled in the browser.

The preparation steps included:

* Reviewing the environment configuration and variables used during the build process.
* Configuring the correct API endpoint so that the frontend could communicate with the backend after deployment.
* Running the build command to generate static HTML, JavaScript, CSS, and image assets.
* Inspecting the build directory and confirming that the application could load its required resources.

Building the application before uploading it to S3 reduced unnecessary source files and produced a deployment-ready version of the frontend.

#### 2. Deploying the Static Website to Amazon S3

I created and configured an **Amazon S3 bucket** to store the static assets of the ReactJS SPA. The main activities included:

* Creating a bucket with an appropriate name and AWS Region.
* Uploading the files in the build directory while preserving the application's folder structure.
* Configuring the index document used when users access the website.
* Checking that HTML, CSS, JavaScript, and image assets could be loaded from the bucket.
* Reviewing access settings to avoid exposing data beyond what was required.

For the SPA, I also considered client-side routing. When a user directly accesses a nested route, the hosting configuration must return the application's entry point instead of responding with a missing-resource error.

#### 3. Configuring Amazon CloudFront for Content Delivery

I created an **Amazon CloudFront distribution** with the S3 bucket as its origin. CloudFront distributes content through edge locations closer to users, which can reduce latency and improve page-loading performance.

The configuration activities included:

* Selecting the S3 bucket as the CloudFront origin.
* Reviewing caching behavior and the amount of time content remains at edge locations.
* Configuring access options, allowed HTTP methods, and cache behavior for the static website.
* Setting the default root object and custom error responses to support SPA navigation.
* Creating an invalidation when cached content needed to be refreshed after a frontend update.

I learned that cache duration requires a balance between performance and content freshness. Longer cache periods reduce requests to the origin, but a new invalidation may be required after publishing an updated frontend build.

#### 4. Configuring SSL and Website Security

I reviewed and practiced the security configuration for CloudFront website delivery. The main topics included:

* Using an appropriate SSL/TLS certificate to allow users to access the website over HTTPS.
* Configuring the viewer protocol policy to redirect or require HTTPS requests.
* Reviewing how to restrict access to the S3 origin and prefer CloudFront access over direct bucket access.
* Checking the domain, certificate, and distribution status after configuration.
* Confirming that the website loaded securely without mixed HTTP/HTTPS content errors.

These settings help protect data transmitted between the browser and the system while reducing unnecessary direct access to the origin storage.

#### 5. Testing Performance and Connectivity

After deployment, I accessed the website through the CloudFront distribution domain and checked the application's main functions. I reviewed page-loading behavior, response status, static asset delivery, and the frontend's ability to call the backend API.

I also tested the website after publishing an updated build to verify that the upload, cache invalidation, and content distribution workflow worked as expected.

### Week 7 Achievements

* Completed the build and deployment process for a ReactJS Single Page Application on Amazon S3.
* Understood how to configure an S3 bucket to store and serve static website assets.
* Created and configured a CloudFront distribution using S3 as its origin for CDN delivery.
* Understood the role of caching, edge locations, and invalidation in improving page-loading performance.
* Configured HTTPS/SSL access and reviewed methods for protecting the S3 origin from unnecessary direct access.
* Successfully checked website loading, static asset delivery, and frontend-to-backend connectivity after deployment.

### Reference Materials

* [AWS Documentation](https://docs.aws.amazon.com/)
* [Amazon S3 Static Website Hosting](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html)
* [Amazon CloudFront Developer Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html)



