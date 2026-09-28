# DVA-C02 Practice Questions: AWS Certified Developer – Associate

[← All certifications](../../README.md)

5 free, original DVA-C02 practice questions with an explanation for every option.

> **Want the full bank?** Practice [590+ DVA-C02 questions and a 65-question timed mock exam on CLOUD.VERSE](https://cloudverse.pro/aws/dva-c02/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=dva-c02). You get 15 free questions per day.

## Exam at a glance

| | |
|---|---|
| Exam code | DVA-C02 |
| Certification | AWS Certified Developer – Associate |
| Exam duration | 130 minutes |
| Passing score | 720 (scaled 100–1000) |
| CLOUD.VERSE mock exam | 65 questions in 130 minutes |
| Official exam guide | [AWS](https://docs.aws.amazon.com/aws-certification/latest/developer-associate-02/developer-associate-02.html) |

Exam details can change. Always confirm them in the official guide.

## Domains

| Domain | Weight |
|---|---|
| Development with AWS Services | 32% |
| Security | 26% |
| Deployment | 24% |
| Troubleshooting and Optimization | 18% |

## Questions

Answer each question before you open **Show answer**.

### Question 1 · Development with AWS Services

An application writes an order to an Amazon DynamoDB table and must immediately read the same item back with the latest data. Which approach guarantees this?

- **A.** Use a Scan operation instead of GetItem
- **B.** Enable DynamoDB Streams on the table
- **C.** Query a global secondary index that contains the item
- **D.** Call GetItem with ConsistentRead set to true

<details>
<summary><b>Show answer</b></summary>

**Correct answer: D. Call GetItem with ConsistentRead set to true**

- ❌ **A. Use a Scan operation instead of GetItem.** Scan is eventually consistent by default and reads the whole table, which is slow and expensive.
- ❌ **B. Enable DynamoDB Streams on the table.** Streams capture changes so other consumers can process them. They do not change read consistency.
- ❌ **C. Query a global secondary index that contains the item.** Global secondary indexes support only eventually consistent reads.
- ✅ **D. Call GetItem with ConsistentRead set to true.** A strongly consistent read returns the result of every write that succeeded before the read.

</details>

### Question 2 · Security

An AWS Lambda function needs to read objects from one Amazon S3 bucket. What is the MOST secure way to give it access?

- **A.** Create an IAM user and store its access keys in the function's environment variables
- **B.** Attach an execution role to the function with a policy that allows s3:GetObject on that bucket only
- **C.** Make the bucket public
- **D.** Store the root user's access keys in AWS Secrets Manager and load them at runtime

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. Attach an execution role to the function with a policy that allows s3:GetObject on that bucket only**

- ❌ **A. Create an IAM user and store its access keys in the function's environment variables.** Long-lived access keys can leak and must be rotated by hand. Roles are the recommended way to grant access to Lambda.
- ✅ **B. Attach an execution role to the function with a policy that allows s3:GetObject on that bucket only.** The execution role gives the function temporary credentials that rotate automatically, scoped to the least privilege it needs.
- ❌ **C. Make the bucket public.** This exposes the data to everyone on the internet.
- ❌ **D. Store the root user's access keys in AWS Secrets Manager and load them at runtime.** Applications should never use root credentials. Root has unrestricted access to the whole account.

</details>

### Question 3 · Deployment

A team deploys a new version of a Lambda function. They want to send 10% of traffic to the new version for 10 minutes, then shift the rest, and roll back automatically if an Amazon CloudWatch alarm fires. What should they use?

- **A.** AWS CodeDeploy with the CodeDeployDefault.LambdaCanary10Percent10Minutes configuration and CloudWatch alarms on the deployment
- **B.** Update the $LATEST version directly
- **C.** A CloudFormation stack policy
- **D.** S3 Versioning on the deployment bucket

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. AWS CodeDeploy with the CodeDeployDefault.LambdaCanary10Percent10Minutes configuration and CloudWatch alarms on the deployment**

- ✅ **A. AWS CodeDeploy with the CodeDeployDefault.LambdaCanary10Percent10Minutes configuration and CloudWatch alarms on the deployment.** CodeDeploy shifts traffic between Lambda versions through an alias. The canary configuration sends 10% first, and the attached alarms trigger an automatic rollback. AWS SAM can set this up with DeploymentPreference.
- ❌ **B. Update the $LATEST version directly.** All traffic moves at once, with no gradual shift and no automatic rollback.
- ❌ **C. A CloudFormation stack policy.** A stack policy protects stack resources from unintended updates. It does not shift traffic.
- ❌ **D. S3 Versioning on the deployment bucket.** Versioning keeps old object versions. It does not control how traffic reaches the function.

</details>

### Question 4 · Troubleshooting and Optimization

Users report slow responses from an API built with Amazon API Gateway, AWS Lambda, and Amazon DynamoDB. A developer needs to see how long each service takes for individual requests. Which service should they enable?

- **A.** AWS CloudTrail
- **B.** AWS Config
- **C.** AWS X-Ray
- **D.** VPC Flow Logs

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. AWS X-Ray**

- ❌ **A. AWS CloudTrail.** CloudTrail records API calls for auditing (who did what, and when). It does not measure per-request latency across services.
- ❌ **B. AWS Config.** Config tracks changes to resource configurations.
- ✅ **C. AWS X-Ray.** X-Ray traces each request end to end and shows the latency of every segment (API Gateway, Lambda, DynamoDB calls) on a service map.
- ❌ **D. VPC Flow Logs.** Flow Logs capture IP traffic metadata for network interfaces. They cannot break down application latency.

</details>

### Question 5 · Development with AWS Services

A worker polls an Amazon SQS standard queue. Processing each message takes about 90 seconds, and the queue's visibility timeout is 30 seconds. Many messages are processed twice. What should the developer do FIRST?

- **A.** Increase the visibility timeout to more than the processing time
- **B.** Reduce the message retention period
- **C.** Enable long polling
- **D.** Replace the queue with an Amazon SNS topic

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. Increase the visibility timeout to more than the processing time**

- ✅ **A. Increase the visibility timeout to more than the processing time.** After 30 seconds the message becomes visible again while it is still being processed, so another consumer picks it up. Set the timeout above 90 seconds (or extend it with ChangeMessageVisibility). Keep processing idempotent anyway, because standard queues deliver at least once.
- ❌ **B. Reduce the message retention period.** Retention controls how long unprocessed messages stay in the queue. It does not prevent duplicates.
- ❌ **C. Enable long polling.** Long polling reduces empty responses and cost. It does not stop a message from reappearing mid-processing.
- ❌ **D. Replace the queue with an Amazon SNS topic.** SNS pushes messages to subscribers. It does not solve the timeout problem and removes the buffering the worker relies on.

</details>

## Keep practicing

Five questions cover only a small part of the DVA-C02 exam guide. On CLOUD.VERSE you get:

- 590+ DVA-C02 practice questions with explanations
- A 65-question timed mock exam (130 minutes)
- 15 free questions per day

**[Practice DVA-C02 on CLOUD.VERSE →](https://cloudverse.pro/aws/dva-c02/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=dva-c02)**

---

<sub>Independent project, not affiliated with or endorsed by AWS. These are original practice questions, not real exam questions, and they do not guarantee a passing score.</sub>
