# AI-103 Practice Questions: Developing AI Apps and Agents on Azure

[← All certifications](../../README.md)

5 free, original AI-103 practice questions with an explanation for every option.

> **Want the full bank?** Practice [110+ AI-103 questions and a 50-question timed mock exam on CLOUD.VERSE](https://cloudverse.pro/microsoft/ai-103/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=ai-103). You get 15 free questions per day.

## Exam at a glance

| | |
|---|---|
| Exam code | AI-103 |
| Certification | Developing AI Apps and Agents on Azure |
| Exam duration | 100 minutes |
| Passing score | 700 (scaled 100–1000) |
| CLOUD.VERSE mock exam | 50 questions in 100 minutes |
| Official exam guide | [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-103) |

Exam details can change. Always confirm them in the official guide.

## Domains

| Domain | Weight |
|---|---|
| Plan and manage an Azure AI solution | 25–30% |
| Implement generative AI and agentic solutions | 30–35% |
| Implement computer vision solutions | 10–15% |
| Implement text analysis solutions | 10–15% |
| Implement information extraction solutions | 10–15% |

## Questions

Answer each question before you open **Show answer**.

### Question 1 · Plan and manage an Azure AI solution

An App Service web app calls a Microsoft Foundry resource. Security policy forbids storing API keys in code or configuration. How should the app authenticate?

- **A.** Store the key in appsettings.json and restrict file permissions
- **B.** Allow anonymous access to the endpoint
- **C.** Enable a managed identity on the web app and assign it an appropriate Azure RBAC role on the Foundry resource
- **D.** Send the key in each request's query string

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. Enable a managed identity on the web app and assign it an appropriate Azure RBAC role on the Foundry resource**

- ❌ **A. Store the key in appsettings.json and restrict file permissions.** This is still a stored key, which the policy forbids.
- ❌ **B. Allow anonymous access to the endpoint.** Anyone could call the endpoint, which is insecure.
- ✅ **C. Enable a managed identity on the web app and assign it an appropriate Azure RBAC role on the Foundry resource.** A managed identity gets Microsoft Entra ID tokens automatically, so no secret is stored anywhere. RBAC limits it to the permissions it needs.
- ❌ **D. Send the key in each request's query string.** Keys in URLs end up in logs and browser history. It is still a stored key, too.

</details>

### Question 2 · Implement generative AI and agentic solutions

A company wants its generative AI app to answer questions from thousands of internal PDFs and cite its sources. The documents are updated weekly. What should you implement?

- **A.** A retrieval-augmented generation (RAG) pattern that indexes the documents in Azure AI Search and passes the retrieved chunks to the model
- **B.** Fine-tune the model on the PDFs every week
- **C.** Increase the model's temperature
- **D.** Switch to a model with more parameters

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. A retrieval-augmented generation (RAG) pattern that indexes the documents in Azure AI Search and passes the retrieved chunks to the model**

- ✅ **A. A retrieval-augmented generation (RAG) pattern that indexes the documents in Azure AI Search and passes the retrieved chunks to the model.** RAG grounds each answer in retrieved passages, which makes citations possible, and weekly updates only require reindexing.
- ❌ **B. Fine-tune the model on the PDFs every week.** Fine-tuning is costly for frequent changes and does not give reliable citations.
- ❌ **C. Increase the model's temperature.** This makes answers more random and does not add knowledge.
- ❌ **D. Switch to a model with more parameters.** A bigger model still does not know your private documents.

</details>

### Question 3 · Implement generative AI and agentic solutions

You are building an agent in Foundry Agent Service. The agent must check stock levels by calling an internal REST API described by an OpenAPI 3.0 specification. What should you add to the agent?

- **A.** A higher temperature setting
- **B.** An OpenAPI tool configured with the API's specification
- **C.** A fine-tuned version of the model trained on the specification
- **D.** A content filter

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. An OpenAPI tool configured with the API's specification**

- ❌ **A. A higher temperature setting.** Sampling settings do not give the agent the ability to call APIs.
- ✅ **B. An OpenAPI tool configured with the API's specification.** The OpenAPI tool lets the agent call the operations defined in the specification, with authentication configured on the tool.
- ❌ **C. A fine-tuned version of the model trained on the specification.** Fine-tuning teaches patterns, but the model still cannot make HTTP calls without a tool.
- ❌ **D. A content filter.** Content filters moderate inputs and outputs. They do not add actions.

</details>

### Question 4 · Implement text analysis solutions

A support app must find and mask names, phone numbers, and email addresses in customer messages before storing them. Which capability should you use?

- **A.** Sentiment analysis
- **B.** Key phrase extraction
- **C.** Language detection
- **D.** PII detection in Azure Language

<details>
<summary><b>Show answer</b></summary>

**Correct answer: D. PII detection in Azure Language**

- ❌ **A. Sentiment analysis.** Sentiment analysis scores opinion (positive or negative). It does not find personal data.
- ❌ **B. Key phrase extraction.** Key phrase extraction lists the main topics of a text. It does not redact anything.
- ❌ **C. Language detection.** Language detection only identifies which language the text is in.
- ✅ **D. PII detection in Azure Language.** PII detection identifies personal information entities and returns a redacted version of the text.

</details>

### Question 5 · Implement information extraction solutions

A finance team receives thousands of supplier invoices as PDFs and scans. They need the vendor name, invoice total, and due date as structured fields, with minimal development effort. What should you use?

- **A.** Azure Document Intelligence with the prebuilt invoice model
- **B.** Azure Translator
- **C.** Azure Speech
- **D.** Image tagging in Azure Vision

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. Azure Document Intelligence with the prebuilt invoice model**

- ✅ **A. Azure Document Intelligence with the prebuilt invoice model.** The prebuilt invoice model extracts common invoice fields out of the box, with no training required.
- ❌ **B. Azure Translator.** Translator converts text between languages. It does not extract fields.
- ❌ **C. Azure Speech.** Speech works with audio, not documents.
- ❌ **D. Image tagging in Azure Vision.** Image tagging describes what appears in an image. It does not return invoice fields.

</details>

## Keep practicing

Five questions cover only a small part of the AI-103 exam guide. On CLOUD.VERSE you get:

- 110+ AI-103 practice questions with explanations
- A 50-question timed mock exam (100 minutes)
- 15 free questions per day

**[Practice AI-103 on CLOUD.VERSE →](https://cloudverse.pro/microsoft/ai-103/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=ai-103)**

---

<sub>Independent project, not affiliated with or endorsed by Microsoft. These are original practice questions, not real exam questions, and they do not guarantee a passing score.</sub>
