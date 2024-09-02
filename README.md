# What’s AWS?


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
AWS Regions : A region is a cluster of data centers, Most AWS services are region-scoped

How to choose an AWS Region?

• Compliance with data governance and legal requirements: data never leaves a region without your explicit permission
• Proximity to customers: reduced latency
• Available services within a Region: new services and new features aren’t available in every Region
• Pricing: pricing varies region to region and is transparent in the service pricing page


AWS Availability Zones

• Each region has many availability zones (usually 3, min is 3, max is 6).
• AZ with redundant power, networking, and connectivity
• They’re separate from each other, so that they’re isolated from disasters
• They’re connected with high bandwidth, ultra-low latency networking

Edge Locations

Content is delivered to end users with lower latency
```


```
AWS has Global Services:

• Identity and Access Management (IAM)
• Route 53 (DNS service)
• CloudFront (Content Delivery Network)
• WAF (Web Application Firewall)

Most AWS services are Region-scoped:

• Amazon EC2 (Infrastructure as a Service)
• Elastic Beanstalk (Platform as a Service)
• Lambda (Function as a Service)
• Rekognition (Software as a Service)

```
