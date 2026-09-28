# GH-300 Practice Questions: GitHub Copilot Certification

[← All certifications](../../README.md)

5 free, original GH-300 practice questions with an explanation for every option.

> **Want the full bank?** Practice [100+ GH-300 questions and a 60-question timed mock exam on CLOUD.VERSE](https://cloudverse.pro/github/gh-300/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=gh-300). You get 15 free questions per day.

## Exam at a glance

| | |
|---|---|
| Exam code | GH-300 |
| Certification | GitHub Copilot Certification |
| Exam duration | 100 minutes |
| Passing score | 700 (scaled 100–1000) |
| CLOUD.VERSE mock exam | 60 questions in 100 minutes |
| Official exam guide | [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/github-copilot/) |

Exam details can change. Always confirm them in the official guide.

## Domains

| Domain | Weight |
|---|---|
| Responsible AI | 7% |
| GitHub Copilot Plans & Features | 31% |
| How GitHub Copilot Works & Handles Data | 15% |
| Prompt Crafting & Prompt Engineering | 9% |
| Developer Use Cases for AI | 14% |
| Testing with GitHub Copilot | 9% |
| Privacy Fundamentals & Context Exclusions | 15% |

## Questions

Answer each question before you open **Show answer**.

### Question 1 · Privacy Fundamentals & Context Exclusions

An organization must stop GitHub Copilot from using files in the secrets/ folder and all .env files as context. What should an administrator configure?

- **A.** Add the paths to .gitignore
- **B.** Content exclusion for those paths in the repository or organization Copilot settings
- **C.** Change the policy for suggestions matching public code
- **D.** A branch protection rule

<details>
<summary><b>Show answer</b></summary>

**Correct answer: B. Content exclusion for those paths in the repository or organization Copilot settings**

- ❌ **A. Add the paths to .gitignore.** .gitignore controls what Git tracks. It is not the mechanism for excluding content from Copilot.
- ✅ **B. Content exclusion for those paths in the repository or organization Copilot settings.** Content exclusion prevents Copilot from using the specified files as context and disables suggestions inside them.
- ❌ **C. Change the policy for suggestions matching public code.** That policy filters suggestions that match public code. It does not exclude your files.
- ❌ **D. A branch protection rule.** Branch protection controls pushes and merges, not Copilot context.

</details>

### Question 2 · GitHub Copilot Plans & Features

A company wants to reduce the risk of accepting code suggestions that match public code on GitHub. What should the organization owner do?

- **A.** Set the "Suggestions matching public code" policy to Blocked
- **B.** Make all repositories private
- **C.** Turn off Copilot Chat
- **D.** Enable Dependabot alerts

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. Set the "Suggestions matching public code" policy to Blocked**

- ✅ **A. Set the "Suggestions matching public code" policy to Blocked.** When blocked, Copilot checks suggestions against public code on GitHub and does not show matches.
- ❌ **B. Make all repositories private.** Repository visibility does not change what Copilot suggests.
- ❌ **C. Turn off Copilot Chat.** This removes a feature but does not filter code completions.
- ❌ **D. Enable Dependabot alerts.** Dependabot flags vulnerable dependencies. It is unrelated to suggestion matching.

</details>

### Question 3 · Prompt Crafting & Prompt Engineering

Copilot keeps suggesting generic code for a date-parsing function. Which change is MOST likely to improve the suggestions?

- **A.** Close every other open file so Copilot can focus
- **B.** Give the function a short, generic name like fn1
- **C.** Write a comment that states the input format, the output type, and an example, and keep related files open
- **D.** Turn off inline suggestions and try again later

<details>
<summary><b>Show answer</b></summary>

**Correct answer: C. Write a comment that states the input format, the output type, and an example, and keep related files open**

- ❌ **A. Close every other open file so Copilot can focus.** Open related files are useful context. Closing them usually makes suggestions worse.
- ❌ **B. Give the function a short, generic name like fn1.** Descriptive names are part of the context. Generic names remove intent.
- ✅ **C. Write a comment that states the input format, the output type, and an example, and keep related files open.** Copilot builds its prompt from the current file and open tabs. Specific intent plus an example gives it the context it needs.
- ❌ **D. Turn off inline suggestions and try again later.** This does not change the quality of the next suggestion.

</details>

### Question 4 · Testing with GitHub Copilot

In Copilot Chat in VS Code, a developer selects a function and wants unit tests generated for it. Which slash command is designed for this?

- **A.** /tests
- **B.** /fix
- **C.** /explain
- **D.** /new

<details>
<summary><b>Show answer</b></summary>

**Correct answer: A. /tests**

- ✅ **A. /tests.** /tests generates unit tests for the selected code.
- ❌ **B. /fix.** /fix proposes fixes for problems in the selected code.
- ❌ **C. /explain.** /explain describes how the selected code works.
- ❌ **D. /new.** /new scaffolds a new project or file structure.

</details>

### Question 5 · Responsible AI

Which practice follows responsible use of GitHub Copilot?

- **A.** Accept suggestions without review because Copilot was trained on high-quality code
- **B.** Skip code review for pull requests created with Copilot
- **C.** Assume suggestions never resemble existing public code
- **D.** Review, test, and security-scan Copilot suggestions the same way you would review code written by a teammate

<details>
<summary><b>Show answer</b></summary>

**Correct answer: D. Review, test, and security-scan Copilot suggestions the same way you would review code written by a teammate**

- ❌ **A. Accept suggestions without review because Copilot was trained on high-quality code.** Training data does not guarantee that a suggestion is correct or secure.
- ❌ **B. Skip code review for pull requests created with Copilot.** AI-assisted code needs the same review as any other code.
- ❌ **C. Assume suggestions never resemble existing public code.** Suggestions can match public code, which is why a filter policy exists.
- ✅ **D. Review, test, and security-scan Copilot suggestions the same way you would review code written by a teammate.** Suggestions can contain bugs, insecure patterns, or outdated APIs. The developer stays responsible for the code that ships.

</details>

## Keep practicing

Five questions cover only a small part of the GH-300 exam guide. On CLOUD.VERSE you get:

- 100+ GH-300 practice questions with explanations
- A 60-question timed mock exam (100 minutes)
- 15 free questions per day

**[Practice GH-300 on CLOUD.VERSE →](https://cloudverse.pro/github/gh-300/practice-exam?utm_source=github&utm_medium=readme&utm_campaign=free-practice-questions&utm_content=gh-300)**

---

<sub>Independent project, not affiliated with or endorsed by GitHub. These are original practice questions, not real exam questions, and they do not guarantee a passing score.</sub>
