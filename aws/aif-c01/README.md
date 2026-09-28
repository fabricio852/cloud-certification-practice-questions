# AIF-C01 Practice Questions: AWS Certified AI Practitioner

[← All certifications](../../README.md)

5 free, original AIF-C01 practice questions with an explanation for every option.

> **Want the full bank?** Practice [440+ AIF-C01 questions and a 65-question timed mock exam on CLOUD.VERSE](https://cloudverse.pro/aws/aif-c01/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=aif-c01). You get 15 free questions per day.

## Exam at a glance

| | |
|---|---|
| Exam code | AIF-C01 |
| Certification | AWS Certified AI Practitioner |
| Exam duration | 90 minutes |
| Passing score | 700 (scaled 100–1000) |
| CLOUD.VERSE mock exam | 65 questions in 90 minutes |
| Official exam guide | [AWS](https://docs.aws.amazon.com/aws-certification/latest/ai-practitioner-01/ai-practitioner-01.html) |

Exam details can change. Always confirm them in the official guide.

## Domains

| Domain | Weight |
|---|---|
| Fundamentals of AI and ML | 20% |
| Fundamentals of Generative AI | 24% |
| Applications of Foundation Models | 28% |
| Guidelines for Responsible AI | 14% |
| Security, Compliance, and Governance for AI Solutions | 14% |

## Questions

Answer each question before you open **Show answer**.

### Question 1 · Fundamentals of AI and ML

A real estate company has 10 years of labeled sales data and wants a model that predicts the sale price of a house. Which type of machine learning problem is this?

- **A.** Classification
- **B.** Regression
- **C.** Clustering
- **D.** Dimensionality reduction

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. Regression**

- ❌ **A. Classification.** Classification predicts a category, such as "sold" or "not sold".
- ✅ **B. Regression.** Predicting a continuous numeric value (a price) from labeled examples is supervised regression.
- ❌ **C. Clustering.** Clustering is unsupervised. It groups data without labels and does not predict a value.
- ❌ **D. Dimensionality reduction.** This technique reduces the number of input features. It is not a prediction task on its own.

</details>

### Question 2 · Fundamentals of Generative AI

A company uses a foundation model to write product descriptions. The outputs vary too much between runs, and the team wants more consistent, focused text. Which inference parameter change helps MOST?

- **A.** Increase the temperature
- **B.** Decrease the temperature
- **C.** Increase the maximum number of output tokens
- **D.** Add more stop sequences

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. Decrease the temperature**

- ❌ **A. Increase the temperature.** Higher temperature adds randomness, which increases the variation.
- ✅ **B. Decrease the temperature.** Lower temperature makes the model pick high-probability tokens more often, so the output becomes more deterministic and focused.
- ❌ **C. Increase the maximum number of output tokens.** This allows longer answers. It does not reduce variation.
- ❌ **D. Add more stop sequences.** Stop sequences end generation early when certain text appears. They do not make the content more consistent.

</details>

### Question 3 · Applications of Foundation Models

A company wants a chatbot that answers employee questions using internal policy documents. The documents change every week, and the company does not want to retrain a model each time. Which approach fits BEST?

- **A.** Pre-train a new foundation model on the documents
- **B.** Fine-tune a model every week
- **C.** Use Retrieval Augmented Generation (RAG) with Amazon Bedrock Knowledge Bases
- **D.** Raise the model's temperature so it improvises answers

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. Use Retrieval Augmented Generation (RAG) with Amazon Bedrock Knowledge Bases**

- ❌ **A. Pre-train a new foundation model on the documents.** Pre-training is extremely expensive and slow, and the model would be outdated after the next weekly change.
- ❌ **B. Fine-tune a model every week.** Fine-tuning costs time and money on every change, and it is a weak way to teach a model facts that change often.
- ✅ **C. Use Retrieval Augmented Generation (RAG) with Amazon Bedrock Knowledge Bases.** RAG retrieves the relevant passages at question time and passes them to the model. When the documents change, you sync the knowledge base, with no retraining.
- ❌ **D. Raise the model's temperature so it improvises answers.** More randomness increases hallucinations. It adds no knowledge of the documents.

</details>

### Question 4 · Guidelines for Responsible AI

A bank must check its training data for bias and explain which features influenced each loan decision made by its model. Which AWS service helps with both tasks?

- **A.** Amazon SageMaker Clarify
- **B.** Amazon Macie
- **C.** AWS Artifact
- **D.** Amazon Comprehend

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. Amazon SageMaker Clarify**

- ✅ **A. Amazon SageMaker Clarify.** SageMaker Clarify detects bias in data and models, and it explains predictions with feature attributions.
- ❌ **B. Amazon Macie.** Macie discovers sensitive data such as PII in Amazon S3. It does not measure model bias.
- ❌ **C. AWS Artifact.** Artifact provides AWS compliance reports.
- ❌ **D. Amazon Comprehend.** Comprehend is a natural language processing service (entities, sentiment). It does not explain another model's decisions.

</details>

### Question 5 · Security, Compliance, and Governance for AI Solutions

A company's generative AI assistant runs on Amazon Bedrock. The company must block harmful topics and mask personally identifiable information (PII) in responses. What should it use?

- **A.** AWS CloudTrail
- **B.** An IAM policy that denies bedrock:InvokeModel
- **C.** Amazon Bedrock model evaluation
- **D.** Amazon Bedrock Guardrails

<details>
<summary><b>Show answer</b></summary>

**Correct answer: D. Amazon Bedrock Guardrails**

- ❌ **A. AWS CloudTrail.** CloudTrail logs API activity for auditing. It does not filter what the model says.
- ❌ **B. An IAM policy that denies bedrock:InvokeModel.** This blocks the assistant completely instead of filtering its content.
- ❌ **C. Amazon Bedrock model evaluation.** Model evaluation compares model quality before you choose one. It does not filter live traffic.
- ✅ **D. Amazon Bedrock Guardrails.** Guardrails provide denied topics, content filters, and sensitive information filters that can block or mask PII in prompts and responses.

</details>

## Keep practicing

Five questions cover only a small part of the AIF-C01 exam guide. On CLOUD.VERSE you get:

- 440+ AIF-C01 practice questions with explanations
- A 65-question timed mock exam (90 minutes)
- 15 free questions per day

**[Practice AIF-C01 on CLOUD.VERSE →](https://cloudverse.pro/aws/aif-c01/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=aif-c01)**

---

<sub>Independent project, not affiliated with or endorsed by AWS. These are original practice questions, not real exam questions, and they do not guarantee a passing score.</sub>
