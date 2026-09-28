# SAA-C03 Practice Questions: AWS Certified Solutions Architect – Associate

[← All certifications](../../README.md)

5 free, original SAA-C03 practice questions with an explanation for every option.

> **Want the full bank?** Practice [800+ SAA-C03 questions and a 65-question timed mock exam on CLOUD.VERSE](https://cloudverse.pro/aws/saa-c03/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=saa-c03). You get 15 free questions per day.

## Exam at a glance

| | |
|---|---|
| Exam code | SAA-C03 |
| Certification | AWS Certified Solutions Architect – Associate |
| Exam duration | 130 minutes |
| Passing score | 720 (scaled 100–1000) |
| CLOUD.VERSE mock exam | 65 questions in 130 minutes |
| Official exam guide | [AWS](https://docs.aws.amazon.com/aws-certification/latest/solutions-architect-associate-03/solutions-architect-associate-03.html) |

Exam details can change. Always confirm them in the official guide.

## Domains

| Domain | Weight |
|---|---|
| Design Secure Architectures | 30% |
| Design Resilient Architectures | 26% |
| Design High-Performing Architectures | 24% |
| Design Cost-Optimized Architectures | 20% |

## Questions

Answer each question before you open **Show answer**.

### Question 1 · Design Resilient Architectures

A web application runs on a single Amazon EC2 instance in one Availability Zone behind an Application Load Balancer (ALB). The application must keep serving traffic if an entire Availability Zone fails. Which solution meets this requirement?

- **A.** Change to a larger instance type
- **B.** Take hourly Amazon EBS snapshots of the instance
- **C.** Create an Auto Scaling group that launches instances in at least two Availability Zones and register it with the ALB
- **D.** Move the instance into a cluster placement group

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. Create an Auto Scaling group that launches instances in at least two Availability Zones and register it with the ALB**

- ❌ **A. Change to a larger instance type.** A bigger instance is still one instance in one AZ. If the AZ fails, the application goes down.
- ❌ **B. Take hourly Amazon EBS snapshots of the instance.** Snapshots help you recover data, but restoring takes manual work and downtime. They do not keep the application serving traffic.
- ✅ **C. Create an Auto Scaling group that launches instances in at least two Availability Zones and register it with the ALB.** The ALB spans Availability Zones and sends traffic only to healthy targets. An Auto Scaling group across two or more AZs keeps capacity running in the surviving AZ and replaces failed instances automatically.
- ❌ **D. Move the instance into a cluster placement group.** A cluster placement group packs instances close together in a single AZ for low latency. That is the opposite of AZ resilience.

</details>

### Question 2 · Design Secure Architectures

Amazon EC2 instances in private subnets must download software updates from the internet. The instances must not be reachable from the internet. What should a solutions architect do?

- **A.** Attach an internet gateway and assign public IP addresses to the instances
- **B.** Create a NAT gateway in a public subnet and add a 0.0.0.0/0 route to it in the private subnets' route table
- **C.** Create a gateway VPC endpoint for Amazon S3
- **D.** Move the instances to a public subnet and restrict inbound traffic with security groups

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. Create a NAT gateway in a public subnet and add a 0.0.0.0/0 route to it in the private subnets' route table**

- ❌ **A. Attach an internet gateway and assign public IP addresses to the instances.** Public IPs plus an internet gateway make the instances directly reachable from the internet.
- ✅ **B. Create a NAT gateway in a public subnet and add a 0.0.0.0/0 route to it in the private subnets' route table.** A NAT gateway lets instances start outbound connections to the internet while blocking connections that start from the internet.
- ❌ **C. Create a gateway VPC endpoint for Amazon S3.** A gateway endpoint only reaches Amazon S3 (and DynamoDB). It does not provide general internet access for updates.
- ❌ **D. Move the instances to a public subnet and restrict inbound traffic with security groups.** The instances would have public addresses and depend only on security group rules. The requirement is that they stay private.

</details>

### Question 3 · Design High-Performing Architectures

An Amazon RDS for MySQL database serves an online store. Analysts run heavy reporting queries during business hours, and checkout becomes slow. The reports can tolerate data that is a few seconds old. What is the MOST effective solution?

- **A.** Convert to a Multi-AZ DB instance deployment and point the reports at the standby
- **B.** Increase the allocated storage
- **C.** Place a Network Load Balancer in front of the database
- **D.** Create a read replica and point the reporting queries to it

<details>
<summary><b>Show answer</b></summary>

**Correct answer: D. Create a read replica and point the reporting queries to it**

- ❌ **A. Convert to a Multi-AZ DB instance deployment and point the reports at the standby.** In a Multi-AZ DB instance deployment, the standby exists for failover and does not serve read traffic.
- ❌ **B. Increase the allocated storage.** More storage does not separate the reporting workload from checkout traffic.
- ❌ **C. Place a Network Load Balancer in front of the database.** A load balancer does not split reads from writes, and it is not how you scale RDS reads.
- ✅ **D. Create a read replica and point the reporting queries to it.** A read replica takes the reporting load off the primary. Replication is asynchronous, which is fine because the reports accept data a few seconds old.

</details>

### Question 4 · Design Cost-Optimized Architectures

A company runs a nightly batch job for about 3 hours. The job saves checkpoints, so it can stop and resume without losing work, and the finish time is flexible. Which EC2 purchasing option is MOST cost-effective?

- **A.** On-Demand Instances
- **B.** 3-year Standard Reserved Instances
- **C.** Spot Instances
- **D.** Dedicated Hosts

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. Spot Instances**

- ❌ **A. On-Demand Instances.** On-Demand works, but you pay full price for a workload that can tolerate interruptions.
- ❌ **B. 3-year Standard Reserved Instances.** Reserved Instances pay off for steady 24/7 usage. Here you would pay for about 21 idle hours every day.
- ✅ **C. Spot Instances.** Spot Instances use spare capacity at a steep discount and can be interrupted with a two-minute warning. Checkpointing makes the job tolerant to interruptions, which makes Spot the cheapest fit.
- ❌ **D. Dedicated Hosts.** Dedicated Hosts are the most expensive option. They exist for licensing and compliance needs, not cost savings.

</details>

### Question 5 · Design Secure Architectures

A company serves a static website from an Amazon S3 bucket to users worldwide. Pages must load with low latency, and the bucket must not be publicly accessible. Which solution meets these requirements?

- **A.** Create an Amazon CloudFront distribution with origin access control (OAC) and a bucket policy that allows only that distribution
- **B.** Enable S3 static website hosting and add a bucket policy that allows public read access
- **C.** Enable S3 Transfer Acceleration
- **D.** Put AWS Global Accelerator in front of the bucket

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. Create an Amazon CloudFront distribution with origin access control (OAC) and a bucket policy that allows only that distribution**

- ✅ **A. Create an Amazon CloudFront distribution with origin access control (OAC) and a bucket policy that allows only that distribution.** CloudFront caches content at edge locations close to users. With OAC, only the distribution can read from the bucket, so the bucket stays private.
- ❌ **B. Enable S3 static website hosting and add a bucket policy that allows public read access.** This makes the bucket public, which the requirement forbids, and it adds no edge caching.
- ❌ **C. Enable S3 Transfer Acceleration.** Transfer Acceleration speeds up long-distance transfers to the bucket. It does not cache content, and anonymous readers would still need a public bucket.
- ❌ **D. Put AWS Global Accelerator in front of the bucket.** Global Accelerator endpoints are load balancers, EC2 instances, and Elastic IPs. S3 buckets are not supported endpoints.

</details>

## Keep practicing

Five questions cover only a small part of the SAA-C03 exam guide. On CLOUD.VERSE you get:

- 800+ SAA-C03 practice questions with explanations
- A 65-question timed mock exam (130 minutes)
- 15 free questions per day

**[Practice SAA-C03 on CLOUD.VERSE →](https://cloudverse.pro/aws/saa-c03/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=saa-c03)**

---

<sub>Independent project, not affiliated with or endorsed by AWS. These are original practice questions, not real exam questions, and they do not guarantee a passing score.</sub>
