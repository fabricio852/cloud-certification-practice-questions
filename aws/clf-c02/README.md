# CLF-C02 Practice Questions: AWS Certified Cloud Practitioner

[← All certifications](../../README.md)

5 free, original CLF-C02 practice questions with an explanation for every option.

> **Want the full bank?** Practice [700+ CLF-C02 questions and a 65-question timed mock exam on CLOUD.VERSE](https://cloudverse.pro/aws/clf-c02/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=clf-c02). You get 15 free questions per day.

## Exam at a glance

| | |
|---|---|
| Exam code | CLF-C02 |
| Certification | AWS Certified Cloud Practitioner |
| Exam duration | 90 minutes |
| Passing score | 700 (scaled 100–1000) |
| CLOUD.VERSE mock exam | 65 questions in 90 minutes |
| Official exam guide | [AWS](https://docs.aws.amazon.com/aws-certification/latest/cloud-practitioner-02/cloud-practitioner-02.html) |

Exam details can change. Always confirm them in the official guide.

## Domains

| Domain | Weight |
|---|---|
| Cloud Concepts | 24% |
| Security and Compliance | 30% |
| Cloud Technology and Services | 34% |
| Billing, Pricing, and Support | 12% |

## Questions

Answer each question before you open **Show answer**.

### Question 1 · Cloud Concepts

A retailer buys enough on-premises servers to handle its busiest week of the year. For the other 51 weeks, most of that capacity sits idle. Which benefit of the AWS Cloud most directly solves this problem?

- **A.** Go global in minutes
- **B.** Stop guessing capacity
- **C.** Benefit from massive economies of scale
- **D.** Increase speed and agility

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. Stop guessing capacity**

- ❌ **A. Go global in minutes.** This is about deploying in multiple AWS Regions quickly. It does not address idle capacity.
- ✅ **B. Stop guessing capacity.** In the cloud you provision for the demand you have today and scale up or down as it changes (for example, with Auto Scaling). You no longer buy hardware for the peak and leave it idle the rest of the year.
- ❌ **C. Benefit from massive economies of scale.** This explains why AWS prices are low (aggregate usage across many customers). It does not stop you from over-provisioning.
- ❌ **D. Increase speed and agility.** This is about getting resources in minutes so teams can experiment faster. It is not about matching capacity to demand.

</details>

### Question 2 · Security and Compliance

A company runs its database on Amazon RDS for PostgreSQL. Under the AWS shared responsibility model, which task belongs to the company?

- **A.** Managing database users and the security group rules that allow access to the DB instance
- **B.** Replacing failed disks in the underlying hosts
- **C.** Patching the host operating system of the database servers
- **D.** Physically securing the data center

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. Managing database users and the security group rules that allow access to the DB instance**

- ✅ **A. Managing database users and the security group rules that allow access to the DB instance.** RDS is a managed service. AWS runs the hardware, the host operating system, and the data center. The customer still controls who can reach and log in to the database: security groups, database users, IAM access, and encryption settings.
- ❌ **B. Replacing failed disks in the underlying hosts.** Physical hardware is always an AWS responsibility.
- ❌ **C. Patching the host operating system of the database servers.** With RDS, AWS patches the underlying operating system. You only choose the maintenance window.
- ❌ **D. Physically securing the data center.** Physical security of AWS facilities is part of the security OF the cloud, which AWS owns.

</details>

### Question 3 · Security and Compliance

An auditor asks for the AWS SOC 2 report and the PCI DSS Attestation of Compliance. Where can the company download these documents?

- **A.** AWS Config
- **B.** Amazon Inspector
- **C.** AWS Trusted Advisor
- **D.** AWS Artifact

<details>
<summary><b>Show answer</b></summary>

**Correct answer: D. AWS Artifact**

- ❌ **A. AWS Config.** Config records and evaluates the configuration of your own resources. It does not host AWS audit reports.
- ❌ **B. Amazon Inspector.** Inspector scans your workloads for software vulnerabilities and unintended network exposure.
- ❌ **C. AWS Trusted Advisor.** Trusted Advisor gives best-practice recommendations for your account (cost, security, limits).
- ✅ **D. AWS Artifact.** AWS Artifact is the self-service portal for AWS compliance reports (SOC, PCI, ISO) and agreements such as the BAA.

</details>

### Question 4 · Cloud Technology and Services

A company wants to resize every image uploaded to an Amazon S3 bucket. The team does not want to provision or manage servers, and uploads happen only a few times per hour. Which service should run the resize code?

- **A.** Amazon EC2
- **B.** Amazon Lightsail
- **C.** AWS Lambda
- **D.** AWS Elastic Beanstalk

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. AWS Lambda**

- ❌ **A. Amazon EC2.** EC2 instances are servers you manage and pay for while they run, even when no uploads arrive.
- ❌ **B. Amazon Lightsail.** Lightsail offers simple virtual servers. You still manage a server that runs all the time.
- ✅ **C. AWS Lambda.** Lambda runs code in response to events such as an S3 upload. There are no servers to manage, and you pay per request and execution time, so a few uploads per hour cost very little.
- ❌ **D. AWS Elastic Beanstalk.** Beanstalk automates deployment, but your app still runs on EC2 instances that you pay for continuously.

</details>

### Question 5 · Billing, Pricing, and Support

Before migrating, a company wants to estimate the monthly cost of an architecture that does not exist on AWS yet. Which tool should it use?

- **A.** AWS Cost Explorer
- **B.** AWS Pricing Calculator
- **C.** AWS Budgets
- **D.** AWS Cost and Usage Report

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. AWS Pricing Calculator**

- ❌ **A. AWS Cost Explorer.** Cost Explorer analyzes and forecasts costs based on usage that already exists in your account.
- ✅ **B. AWS Pricing Calculator.** The Pricing Calculator estimates the cost of workloads you are planning, before anything is deployed.
- ❌ **C. AWS Budgets.** Budgets alerts you when actual or forecasted spend crosses a threshold you set.
- ❌ **D. AWS Cost and Usage Report.** The CUR delivers detailed line items of past usage. It cannot price an architecture that does not exist.

</details>

## Keep practicing

Five questions cover only a small part of the CLF-C02 exam guide. On CLOUD.VERSE you get:

- 700+ CLF-C02 practice questions with explanations
- A 65-question timed mock exam (90 minutes)
- 15 free questions per day

**[Practice CLF-C02 on CLOUD.VERSE →](https://cloudverse.pro/aws/clf-c02/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=clf-c02)**

---

<sub>Independent project, not affiliated with or endorsed by AWS. These are original practice questions, not real exam questions, and they do not guarantee a passing score.</sub>
