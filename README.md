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
AWS Config - Configuration and compliance monitoring.
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
Amazon ElastiCache - In-memory caching (Redis and Memcached).
Amazon Aurora - High-performance relational database.
Amazon Redshift - Data warehousing service.
Amazon EKS (Elastic Kubernetes Service) - Managed Kubernetes service.
Amazon ECS (Elastic Container Service) - Container orchestration.

```
