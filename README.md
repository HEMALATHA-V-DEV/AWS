# AWS?

```
- AWS (Amazon Web Services) is a Cloud Provider
- They provide you with servers and services that you can use on demand and scale easily
```

# AWS Global Infrastructure
```
• AWS Regions
• AWS Availability Zones
• AWS Data Centers
• AWS Edge Locations / Points of Presence
```

```
- AWS Regions : A region is a cluster of data centers, Most AWS services are region-scoped
How to choose an AWS Region?
• Compliance with data governance and legal requirements: data never leaves a region without your explicit permission
• Proximity to customers: reduced latency
• Available services within a Region: new services and new features aren’t available in every Region
• Pricing: pricing varies region to region and is transparent in the service pricing page

- AWS Availability Zones
• Each region has many availability zones (usually 3, min is 3, max is 6).
• AZ with redundant power, networking, and connectivity
• They’re separate from each other, so that they’re isolated from disasters
• They’re connected with high bandwidth, ultra-low latency networking

- Edge Locations
Content is delivered to end users with lower latency
```

```
- Global Services
These AWS services are designed to operate across all AWS regions: 

Amazon Route 53 - Scalable DNS and domain name registration.
Amazon CloudFront - Content delivery network (CDN).
AWS Identity and Access Management (IAM) - User and permissions management.
AWS CloudTrail - API activity logging.
AWS Key Management Service (KMS) - Key management and encryption.
AWS Organizations - Multi-account management and governance.
AWS Systems Manager - Unified interface for managing resources.
AWS Backup - Centralized backup management.
Amazon CloudWatch - Monitoring and observability.
Amazon CloudFormation - Infrastructure as code (stack management).
Amazon S3 - Object storage (though S3 buckets are region-scoped, the S3 service itself is global).

- Region-Scoped Services
These AWS services operate within specific AWS regions: 

Amazon EC2 (Elastic Compute Cloud) - Scalable virtual servers.
Amazon RDS (Relational Database Service) - Managed relational databases.
Amazon DynamoDB - Managed NoSQL database service.
Amazon S3 (Simple Storage Service) - Object storage service (buckets are region-specific).
Amazon EBS (Elastic Block Store) - Persistent block storage for EC2.
Amazon EKS (Elastic Kubernetes Service) - Managed Kubernetes service.
Amazon ECS (Elastic Container Service) - Container orchestration.
Amazon ECR (Elastic Container Registry) - is a fully managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images.
```

# AWS Services Overview

## 1. Amazon EC2 (Elastic Compute Cloud)

### What is EC2?
Amazon EC2 provides scalable virtual servers in the cloud, allowing users to run applications with configurable capacity.

### Why Use EC2?
- **Scalability**: Adjust resources based on demand.
- **Flexibility**: Choose from various instance types optimized for different workloads.
- **Pay-as-you-go**: Only pay for what you use.

---

## 2. Amazon S3 (Simple Storage Service)

### What is S3?
Amazon S3 is an object storage service designed for storing and retrieving any amount of data at any time.

### Why Use S3?
- **Durability**: Offers 99.999999999% durability for stored data.
- **Scalability**: Easily handles vast amounts of data.
- **Cost-effective**: Pay only for the storage you use.

---

## 3. Amazon EBS (Elastic Block Store)

### What is EBS?
EBS provides block-level storage volumes for use with EC2 instances.

### Why Use EBS?
- **Persistence**: Data remains available after instance termination.
- **Performance**: Low-latency access to data.
- **Backup Capabilities**: Snapshot capabilities for data protection.

---

## 4. Amazon VPC (Virtual Private Cloud)

### What is VPC?
A VPC allows you to launch AWS resources in a logically isolated virtual network.

### Why Use VPC?
- **Control**: Customize your networking environment.
- **Security**: Enhanced security through subnets and security groups.

---

## 5. Amazon ELB (Elastic Load Balancer)

### What is ELB?
ELB automatically distributes incoming application traffic across multiple targets, such as EC2 instances.

### Why Use ELB?
- **High Availability**: Ensures fault tolerance by distributing traffic.
- **Scalability**: Automatically scales based on traffic demands.

---

## 6. Amazon AMI (Amazon Machine Image)

### What is AMI?
An AMI is a pre-configured template for launching EC2 instances.

### Why Use AMI?
- **Consistency**: Uniform instances launched from the same image.
- **Speed**: Quickly launch new instances.

---

## 7. Amazon SNS (Simple Notification Service)

### What is SNS?
SNS is a fully managed messaging service for sending notifications.

### Why Use SNS?
- **Decoupled Systems**: Facilitates communication between application components.
- **Scalability**: Handles high-throughput messaging effortlessly.

---

## 8. Amazon RDS (Relational Database Service)

### What is RDS?
RDS makes it easy to set up, operate, and scale a relational database in the cloud.

### Why Use RDS?
- **Managed Service**: Simplifies database management.
- **Scalability**: Adjust storage and compute resources easily.

---

## 9. AWS IAM (Identity and Access Management)

### What is IAM?
IAM enables you to manage access to AWS services and resources securely.

### Why Use IAM?
- **Fine-Grained Control**: Define permissions at a granular level.
- **Secure Access**: Multi-factor authentication enhances security.

---

## 10. Amazon ALB (Application Load Balancer)

### What is ALB?
ALB routes HTTP/HTTPS traffic based on request attributes, providing advanced routing capabilities.

### Why Use ALB?
- **Advanced Routing**: Efficiently routes traffic based on content type.
- **HTTP/2 Support**: Enhances performance for web applications.

---

## 11. Auto Scaling

### What is Auto Scaling?
Auto Scaling ensures that the number of Amazon EC2 instances adjusts automatically based on demand.

### Why Use Auto Scaling?
- **Availability**: Automatically adjusts instances to maintain performance.
- **Cost-Effective**: Reduces costs by scaling down resources during low-demand periods.

---

## 12. Amazon CloudFront

### What is CloudFront?
CloudFront is a fast content delivery network (CDN) service.

### Why Use CloudFront?
- **Low Latency**: Delivers content with low latency and high transfer speeds.
- **Security**: Integrated with AWS Shield for enhanced security.

---

## 13. Amazon Security Groups

### What are Security Groups?
Security groups act as virtual firewalls for your EC2 instances to control inbound and outbound traffic.

### Why Use Security Groups?
- **Network Access Control**: Define rules to allow or deny traffic.
- **Stateful**: Automatically allows responses to allowed inbound traffic.

---

## 14. Amazon CloudWatch

### What is CloudWatch?
CloudWatch is a monitoring service for AWS cloud resources and applications.

### Why Use CloudWatch?
- **Resource Monitoring**: Track metrics and logs for insights into resource utilization.
- **Automated Actions**: Set alarms to react to changes automatically.

---

## 15. AWS CloudTrail

### What is CloudTrail?
CloudTrail enables governance, compliance, and auditing of your AWS account by logging API calls.

### Why Use CloudTrail?
- **Compliance**: Maintains compliance by recording account activity.
- **Security Analysis**: Useful for security audits and troubleshooting.

---

## 16. Amazon ECR (Elastic Container Registry)

### What is ECR?
ECR is a fully managed Docker container registry.

### Why Use ECR?
- **Integration**: Seamlessly integrates with ECS and EKS.
- **Security**: Provides built-in encryption for data at rest and in transit.

---

## 17. Amazon EKS (Elastic Kubernetes Service)

### What is EKS?
EKS is a managed Kubernetes service for running Kubernetes on AWS without needing to install and operate your own control plane.

### Why Use EKS?
- **Managed Control Plane**: Automatically manages the Kubernetes control plane.
- **Integration**: Integrates with other AWS services for enhanced functionality.

---

## 18. Amazon Route 53

### What is Route 53?
Route 53 is a scalable Domain Name System (DNS) and domain name registration service.

### Why Use Route 53?
- **High Availability**: Provides reliable and cost-effective DNS routing.
- **Traffic Management**: Advanced traffic routing capabilities, including latency-based routing.

---

## 19. AWS Key Management Service (KMS)

### What is KMS?
KMS is a managed service that makes it easy to create and control cryptographic keys.

### Why Use KMS?
- **Centralized Control**: Control over the cryptographic keys used to encrypt data.
- **Integration**: Easily integrates with other AWS services for security.

---

## 20. AWS Organizations

### What is Organizations?
AWS Organizations helps you centrally manage multiple AWS accounts.

### Why Use Organizations?
- **Account Management**: Simplifies billing and resource management across multiple accounts.
- **Governance**: Apply policies for compliance across accounts.

---

## 21. AWS Systems Manager

### What is Systems Manager?
Systems Manager provides a unified interface for managing AWS resources.

### Why Use Systems Manager?
- **Resource Management**: Centralized management for operational tasks across AWS resources.
- **Automation**: Automate tasks to improve operational efficiency.

---

## 22. AWS Backup

### What is AWS Backup?
AWS Backup is a centralized backup management service.

### Why Use AWS Backup?
- **Centralized Management**: Simplifies the backup process across multiple AWS services.
- **Compliance**: Helps ensure compliance with backup requirements.

---

## 23. Amazon DynamoDB

### What is DynamoDB?
DynamoDB is a fully managed NoSQL database service.

### Why Use DynamoDB?
- **Performance**: Single-digit millisecond response times.
- **Scalability**: Seamlessly scales to handle large amounts of traffic.

---
