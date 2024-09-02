# Amazon EC2

```
• EC2 is one of the most popular of AWS’ offering
• EC2 = Elastic Compute Cloud = Infrastructure as a Service


• It mainly consists in the capability of :
• Renting virtual machines (EC2)
• Storing data on virtual drives (EBS)
• Distributing load across machines (ELB)
• Scaling the services using an auto-scaling group (ASG)
```
# EC2 sizing & configuration options

```
 • Operating System (OS): Linux, Windows or Mac OS
 • How much compute power & cores (CPU)
 • How much random-access memory (RAM)

• How much storage space:
  • Network-attached (EBS & EFS)
  • hardware (EC2 Instance Store)
  • Network card: speed of the card, Public IP address
  • Firewall rules: security group
  • Bootstrap script (configure at first launch): EC2 User Data
```

# EC2 User Data

```
• It is possible to bootstrap our instances using an EC2 User data script.
• bootstrapping means launching commands when a machine starts
• That script is only run once at the instance first start
• EC2 user data is used to automate boot tasks such as:
• Installing updates
• Installing software
• Downloading common file
```


EC2 Instance Types

General purpose
```
General Purpose instances are designed to deliver a balance of compute, memory, and network resources.
They are suitable for a wide range of applications, including web servers, small databases, development and test environments, and more.
```

Compute optimized
```
Compute Optimized instances provide a higher ratio of compute power to memory.
They excel in workloads that require high-performance processing such as batch processing, 
scientific modeling, gaming servers, and high-performance web servers.
```

Memory optimized

```
Memory Optimized instances are designed to handle memory-intensive workloads.
They are suitable for applications that require large amounts of memory, such as in-memory databases, real-time big data analytics, and high-performance computing.
```

Storage optimized

```
Storage Optimized instances are optimized for applications that require high, sequential read and write access to large datasets. 
They are ideal for tasks like data warehousing, log processing, and distributed file systems.
```

Accelerated computing

```
Accelerated Computing Instances typically come with one or more types of accelerators, such as Graphics Processing Units (GPUs),
Field Programmable Gate Arrays (FPGAs), or custom Application Specific Integrated Circuits (ASICs). 
These accelerators offload computationally intensive tasks from the main CPU, enabling faster and more efficient processing for specific workloads.
```
```
m5.2xlarge
• m: instance class
• 5: generation (AWS improves them over time)
• 2xlarge: size within the instance class
```

#Security Groups

```
• Security Groups are the fundamental of network security in AWS
• They control how traffic is allowed into or out of our EC2 Instances
• Security groups only contain rules
• Security groups rules can reference by IP or by security group
```

# Good to know

```
• Can be attached to multiple instances
• Locked down to a region / VPC combination
• If your application is not accessible (time out), then it’s a security group issue
• If your application gives a “connection refused“ error, then it’s an application error or it’s not launched
• All inbound traffic is blocked by default
• All outbound traffic is authorised by default


# Classic Ports to know

• 22 = SSH (Secure Shell) - log into a Linux instance
• 21 = FTP (File Transfer Protocol) – upload files into a file share
• 22 = SFTP (Secure File Transfer Protocol) – upload files using SSH
• 80 = HTTP – access unsecured websites
• 443 = HTTPS – access secured websites
• 3389 = RDP (Remote Desktop Protocol) – log into a Windows instance

• Mac / Linux:
• SSH on Mac/Linux lecture
• Windows:
• Putty Lecture
• If Windows 10: SSH on Windows 10 lecture

```


# EC2 Instances Purchasing Options

```
• On-Demand Instances – short workload, predictable pricing, pay by second
• Reserved (1 & 3 years)
• Reserved Instances – long workloads
• Convertible Reserved Instances – long workloads with flexible instances
• Savings Plans (1 & 3 years) –commitment to an amount of usage, long workload
• Spot Instances – short workloads, cheap, can lose instances (less reliable)
• Dedicated Hosts – book an entire physical server, control instance placement
• Dedicated Instances – no other customers will share your hardware
• Capacity Reservations – reserve capacity in a specific AZ for any duration



Which purchasing option is right for me?
• On demand: coming and staying in resort whenever we like, we pay the full price
• Reserved: like planning ahead and if we plan to stay for a long time, we may get a good discount.
• Savings Plans: pay a certain amount per hour for certain period and stay in any room type (e.g., King, Suite, Sea View, …)
• Spot instances: the hotel allows people to bid for the empty rooms and the highest bidder keeps the rooms. You can get kicked out at any time
• Dedicated Hosts: We book an entire building of the resort
• Capacity Reservations: you book a room for a period with full price even you don’t stay in it
```


Private vs Public IP (IPv4)

```

• Networking has two sorts of IPs. IPv4 and IPv6

• IPv4 is still the most common format used online.
• IPv4: [0-255].[0-255].[0-255].[0-255].

Fundamental Differences

• Public IP:
  • Public IP means the machine can be identified on the internet (WWW)
  • Must be unique across the whole web (not two machines can have the same public IP).
  • Can be geo-located easily

• Private IP:
  • Private IP means the machine can only be identified on a private network only
  • The IP must be unique across the private network
  • BUT two different private networks (two companies) can have the same IPs.
  • Machines connect to WWW using a NAT + internet gateway (a proxy)
  • Only a specified range of IPs can be used as private IP

• Elastic IPs
  • When you stop and then start an EC2 instance, it can change its public IP.
  • If you need to have a fixed public IP for your instance, you need an Elastic IP
  • An Elastic IP is a public IPv4 IP you own as long as you don’t delete it
  • You can attach it to one instance at a time

```

# In AWS EC2 – Hands On

```
 • By default, your EC2 machine comes with:
   • A private IP for the internal AWS Network
   • A public IP, for the WWW.
 • When we are doing SSH into our EC2 machines:
   • We can’t use a private IP, because we are not in the same network
   • We can only use the public IP.
  
 • If your machine is stopped and then started, the public IP can change
```
