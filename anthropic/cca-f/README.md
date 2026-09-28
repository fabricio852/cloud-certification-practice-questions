# CCA-F Practice Questions: Claude Certified Architect – Foundations

[← All certifications](../../README.md)

5 free, original CCA-F practice questions with an explanation for every option.

> **Want the full bank?** Practice [240+ CCA-F questions and a 60-question timed mock exam on CLOUD.VERSE](https://cloudverse.pro/ai/claude/ccar-f?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=cca-f). You get 15 free questions per day.

## Exam at a glance

| | |
|---|---|
| Exam code | CCA-F |
| Certification | Claude Certified Architect – Foundations |
| Exam duration | 120 minutes |
| Passing score | 720 (scaled 100–1000) |
| CLOUD.VERSE mock exam | 60 questions in 120 minutes |
| Official exam guide | [Anthropic](https://www.anthropic.com/news/claude-partner-network) |

Exam details can change. Always confirm them in the official guide.

## Domains

| Domain | Weight |
|---|---|
| Agentic Architecture & Orchestration | 27% |
| Tool Design & MCP Integration | 18% |
| Claude Code Configuration & Workflows | 20% |
| Prompt Engineering & Structured Output | 20% |
| Context Management & Reliability | 15% |

## Questions

Answer each question before you open **Show answer**.

### Question 1 · Claude Code Configuration & Workflows

A team wants every developer's Claude Code session in a repository to follow the same build commands, coding conventions, and testing rules. Where should these instructions live?

- **A.** In a CLAUDE.md file at the repository root, committed to version control
- **B.** In each developer's ~/.claude/CLAUDE.md file
- **C.** In an environment variable on each machine
- **D.** In the repository's .gitignore file

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. In a CLAUDE.md file at the repository root, committed to version control**

- ✅ **A. In a CLAUDE.md file at the repository root, committed to version control.** Claude Code loads the project CLAUDE.md automatically at the start of a session, and committing it shares the same instructions with the whole team.
- ❌ **B. In each developer's ~/.claude/CLAUDE.md file.** The user-level file holds personal preferences across all projects. It is not shared with the team.
- ❌ **C. In an environment variable on each machine.** Environment variables are not read as project instructions.
- ❌ **D. In the repository's .gitignore file.** .gitignore only lists files Git should ignore.

</details>

### Question 2 · Tool Design & MCP Integration

A company wants Claude Desktop, Claude Code, and its own internal agent to use the same ticketing system through the same set of tools. What is the MOST maintainable approach?

- **A.** Paste the ticketing API documentation into every prompt
- **B.** Fine-tune a model on the ticketing API
- **C.** Build one MCP server that exposes the ticketing operations as tools and connect each client to it
- **D.** Write a separate custom integration for each client

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. Build one MCP server that exposes the ticketing operations as tools and connect each client to it**

- ❌ **A. Paste the ticketing API documentation into every prompt.** Documentation does not let Claude call the API, and it wastes context on every request.
- ❌ **B. Fine-tune a model on the ticketing API.** Fine-tuning cannot give a model the ability to make live API calls.
- ✅ **C. Build one MCP server that exposes the ticketing operations as tools and connect each client to it.** MCP is a standard protocol: one server works with every compatible client, so the integration is written and maintained once.
- ❌ **D. Write a separate custom integration for each client.** This triples the code to maintain and lets the behavior drift between clients.

</details>

### Question 3 · Tool Design & MCP Integration

An agent has two tools, search_orders and search_customers. Claude often calls the wrong one. What should you fix FIRST?

- **A.** Increase the temperature
- **B.** Rewrite the tool names and descriptions to say what each tool returns, when to use it, and what each parameter means
- **C.** Remove the tool descriptions to save tokens
- **D.** Add a third, similar tool as a fallback

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. Rewrite the tool names and descriptions to say what each tool returns, when to use it, and what each parameter means**

- ❌ **A. Increase the temperature.** More randomness makes tool choice less reliable, not more.
- ✅ **B. Rewrite the tool names and descriptions to say what each tool returns, when to use it, and what each parameter means.** Claude chooses tools based on their names, descriptions, and input schemas. Clear, detailed descriptions are the most effective fix.
- ❌ **C. Remove the tool descriptions to save tokens.** Descriptions are exactly what Claude uses to choose. Removing them makes the problem worse.
- ❌ **D. Add a third, similar tool as a fallback.** Another overlapping tool adds more ambiguity.

</details>

### Question 4 · Prompt Engineering & Structured Output

A pipeline needs Claude to return data that always matches a fixed JSON schema so downstream code can parse it. Which approach is MOST reliable?

- **A.** Ask for "JSON please" and extract it with a regular expression
- **B.** Increase max_tokens
- **C.** Ask Claude to return a Markdown table instead
- **D.** Define the schema explicitly (for example, as a tool input_schema or with structured outputs) and validate the result in code before using it

<details>
<summary><b>Show answer</b></summary>

**Correct answer: D. Define the schema explicitly (for example, as a tool input_schema or with structured outputs) and validate the result in code before using it**

- ❌ **A. Ask for "JSON please" and extract it with a regular expression.** A loose instruction plus regex parsing breaks on the first unexpected format.
- ❌ **B. Increase max_tokens.** This only raises the output length limit. It does not enforce a structure.
- ❌ **C. Ask Claude to return a Markdown table instead.** A table is harder to parse reliably than schema-constrained JSON.
- ✅ **D. Define the schema explicitly (for example, as a tool input_schema or with structured outputs) and validate the result in code before using it.** An explicit schema constrains the format, and validation in code catches anything unexpected before it reaches downstream systems.

</details>

### Question 5 · Agentic Architecture & Orchestration

A research agent must read dozens of long web pages. Its context window fills with raw page text, and answer quality drops late in the task. Which design change helps MOST?

- **A.** Put all pages into one prompt and raise max_tokens
- **B.** Remove the system prompt to free space
- **C.** Delegate each source to a subagent that reads it in its own context and returns a short, structured summary to the orchestrator
- **D.** Restart the conversation from zero after every tool call

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. Delegate each source to a subagent that reads it in its own context and returns a short, structured summary to the orchestrator**

- ❌ **A. Put all pages into one prompt and raise max_tokens.** max_tokens limits output length. It does not enlarge the context window or reduce input.
- ❌ **B. Remove the system prompt to free space.** This saves little space and removes the instructions that guide the agent.
- ✅ **C. Delegate each source to a subagent that reads it in its own context and returns a short, structured summary to the orchestrator.** The orchestrator-worker pattern keeps raw text out of the main context, so the orchestrator reasons over condensed findings.
- ❌ **D. Restart the conversation from zero after every tool call.** The agent would lose its progress and the facts it already found.

</details>

## Keep practicing

Five questions cover only a small part of the CCA-F exam guide. On CLOUD.VERSE you get:

- 240+ CCA-F practice questions with explanations
- A 60-question timed mock exam (120 minutes)
- 15 free questions per day

**[Practice CCA-F on CLOUD.VERSE →](https://cloudverse.pro/ai/claude/ccar-f?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=cca-f)**

---

<sub>Independent project, not affiliated with or endorsed by Anthropic. These are original practice questions, not real exam questions, and they do not guarantee a passing score.</sub>
