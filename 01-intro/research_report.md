# Research Report: Generative AI Applications

**Author:** Sezim Satlyk-klych
**Course:** Generative AI for Software Development 2026–2027 (TechOrda, EPAM School of Digital Engineering)
**Module:** Course Introduction — Practical Task

---

## Contents

1. [AI-Assisted Software Development (Coding Assistants)](#1-ai-assisted-software-development-coding-assistants)
2. [Customer Support Chatbots and Virtual Agents](#2-customer-support-chatbots-and-virtual-agents)
3. [Enterprise Knowledge Search (RAG over Company Data)](#3-enterprise-knowledge-search-rag-over-company-data)
4. [Marketing and Content Generation](#4-marketing-and-content-generation)
5. [Healthcare Clinical Documentation](#5-healthcare-clinical-documentation)
6. [Education and Personalized Tutoring](#6-education-and-personalized-tutoring)
7. [Legal Document Analysis](#7-legal-document-analysis)
8. [Summary Table](#summary-table)

---

## 1. AI-Assisted Software Development (Coding Assistants)

AI coding assistants use large language models (LLMs) trained on source code to suggest completions, generate functions from natural-language prompts, explain unfamiliar code, write unit tests, and, in their newer "agentic" form, plan and carry out multi-step changes across a repository. **Business value:** faster delivery, less time on boilerplate and routine tasks, quicker onboarding of new developers into large codebases, and higher test coverage. They are now one of the most widely adopted GenAI use cases in companies.

**Technical challenges:** the assistant needs the right context (other files, project conventions, dependencies), which is limited by the model's context window; integration into IDEs, CI/CD and code review must be fast and secure. **Weak points:** generated code can look correct but contain subtle bugs or security vulnerabilities, may use outdated or non-existent APIs (hallucinations), may raise licensing concerns, and can lead to over-reliance by junior developers who stop understanding the code they commit. Human review and automated tests remain mandatory.

**Existing implementations:**
- **GitHub Copilot** — https://github.com/features/copilot — AI pair programmer integrated into VS Code, JetBrains IDEs and GitHub, with chat and agent modes.
- **Cursor** — https://cursor.com — an AI-first code editor (VS Code fork) that can edit multiple files based on natural-language instructions.
- **Claude Code** — https://www.anthropic.com/claude-code — an agentic command-line coding tool that can read a codebase, run commands and make changes.
- **Amazon Q Developer** — https://aws.amazon.com/q/developer/ — AWS coding assistant focused on code generation, transformation and cloud development.

---

## 2. Customer Support Chatbots and Virtual Agents

LLM-based support agents answer customer questions in natural language 24/7, resolve common requests (order status, password reset, refunds) and hand complex cases over to human operators with a summary of the conversation. **Business value:** lower support costs, shorter response times, consistent answers in many languages, and human agents freed up for difficult cases.

**Technical challenges:** the bot must be grounded in up-to-date company policies and product data (usually through RAG), integrated with CRM and ticketing systems, and able to take safe actions through APIs. **Weak points:** the bot can confidently give wrong or invented answers (for example, promising a refund policy that does not exist), it can be manipulated through prompt injection, and customers get frustrated when it cannot escalate to a human. The company is legally responsible for what its chatbot says.

**Existing implementations:**
- **Intercom Fin** — https://www.intercom.com/fin — an AI customer service agent that answers questions using a company's help-center content.
- **Zendesk AI Agents** — https://www.zendesk.com/service/ai/ — AI agents and agent-assist features built into the Zendesk support platform.
- **Salesforce Agentforce** — https://www.salesforce.com/agentforce/ — a platform for building autonomous AI agents for service, sales and other functions.

---

## 3. Enterprise Knowledge Search (RAG over Company Data)

Employees ask questions in plain language and get answers built from internal documents, wikis, tickets, emails and chats, with links to the original sources. This is usually implemented with **Retrieval-Augmented Generation (RAG)**: documents are split into chunks, converted into embeddings, stored in a vector database, and the most relevant chunks are added to the LLM prompt. **Business value:** less time spent searching for information, faster onboarding, and preserved knowledge when experienced employees leave.

**Technical challenges:** connecting many data sources, keeping the index fresh, choosing a good chunking and ranking strategy, and — most importantly — respecting access permissions so that a user never sees documents they are not allowed to read. **Weak points:** answer quality depends entirely on data quality (outdated or contradictory documents produce wrong answers), retrieval can miss the relevant passage, and costs grow with the amount of data and number of queries.

**Existing implementations:**
- **Glean** — https://www.glean.com — enterprise AI search and assistant that connects to many workplace apps while respecting permissions.
- **Microsoft 365 Copilot** — https://www.microsoft.com/microsoft-365/copilot — AI assistant in Word, Outlook, Teams and other apps that uses the user's work data.
- **Notion AI** — https://www.notion.com/product/ai — answers questions and summarizes content stored in a team's Notion workspace.

---

## 4. Marketing and Content Generation

Generative models create marketing copy, product descriptions, social media posts, emails, images and short videos, and adapt them for different audiences and languages. **Business value:** much faster content production, cheap A/B testing of many variants, personalization at scale, and localization without large translation teams.

**Technical challenges:** keeping a consistent brand voice and visual style (often solved with brand guidelines in prompts, templates or fine-tuning), integrating with marketing tools, and checking facts and claims before publishing. **Weak points:** content can become generic and repetitive, copyright and ownership of generated images are still legally unclear in many countries, factual errors in product claims can cause legal risk, and audiences may react negatively to obviously AI-generated content.

**Existing implementations:**
- **Jasper** — https://www.jasper.ai — an AI content platform for marketing teams with brand-voice features.
- **Adobe Firefly** — https://www.adobe.com/products/firefly.html — generative image and design models integrated into Photoshop, Illustrator and Adobe Express.
- **Canva Magic Studio** — https://www.canva.com/magic/ — AI tools in Canva for generating text, images and designs.

---

## 5. Healthcare Clinical Documentation

"Ambient" AI scribes listen to the conversation between a doctor and a patient (with consent), transcribe it, and generate a structured clinical note that the doctor reviews and signs. **Business value:** doctors spend significantly less time on paperwork and more time with patients, burnout is reduced, and documentation becomes more complete and consistent.

**Technical challenges:** accurate speech recognition with medical terminology and accents, integration with electronic health record (EHR) systems, and strict privacy and regulatory requirements for patient data. **Weak points:** any error or hallucination in a medical note can directly harm a patient, so a clinician must always review the output; there are also concerns about data storage, consent, and liability when something goes wrong.

**Existing implementations:**
- **Microsoft Dragon Copilot (Nuance DAX)** — https://www.microsoft.com/en-us/health-solutions/clinical-workflow/dragon-copilot — ambient clinical documentation and assistant for healthcare providers.
- **Abridge** — https://www.abridge.com — generates clinical notes from recorded patient-clinician conversations.

---

## 6. Education and Personalized Tutoring

AI tutors explain topics, answer students' questions, generate practice exercises and give feedback on answers or essays, adapting to each student's level and pace. **Business value:** personalized learning at scale, 24/7 availability, and teachers saving time on preparing materials and checking routine work.

**Technical challenges:** the tutor should guide students to the answer instead of simply giving it, must be factually correct and age-appropriate, and needs to track each learner's progress over time. **Weak points:** students may use it to cheat rather than learn, explanations can contain errors that a beginner cannot notice, and there are privacy concerns when working with minors' data.

**Existing implementations:**
- **Khanmigo (Khan Academy)** — https://www.khanmigo.ai — an AI tutor and teaching assistant that uses guiding questions rather than giving direct answers.
- **Duolingo Max** — https://blog.duolingo.com/duolingo-max/ — a subscription tier with AI features such as "Explain My Answer" and role-play conversations.

---

## 7. Legal Document Analysis

LLMs help lawyers review contracts, extract key clauses, compare documents, summarize case materials and draft first versions of legal documents. **Business value:** large reductions in time spent on routine document review and due diligence, which lowers costs for clients and lets lawyers focus on strategy.

**Technical challenges:** very long documents, precise legal language, the need for citations to exact sources, and strict confidentiality of client data. **Weak points:** hallucinated case law or incorrect citations are a serious risk (there have been real court cases where lawyers submitted AI-invented precedents), and responsibility always stays with the human lawyer.

**Existing implementations:**
- **Harvey** — https://www.harvey.ai — a generative AI platform built for law firms and legal teams.
- **Thomson Reuters CoCounsel** — https://www.thomsonreuters.com/en/cocounsel — an AI legal assistant for research, document review and drafting.

---

## Summary Table

| Use case | Main business value | Main technical challenge | Main weak point |
|---|---|---|---|
| Coding assistants | Faster development | Repository context | Subtle bugs and vulnerabilities |
| Customer support | Lower support costs | Grounding in company data | Wrong answers, prompt injection |
| Enterprise search (RAG) | Faster access to knowledge | Permissions and data freshness | Depends on data quality |
| Content generation | Scalable content | Brand consistency | Copyright and generic content |
| Clinical documentation | Less paperwork for doctors | Medical accuracy and privacy | High cost of errors |
| Education | Personalized learning | Teaching, not just answering | Cheating, unnoticed errors |
| Legal analysis | Faster document review | Long documents and citations | Hallucinated case law |

## Common Patterns Across Use Cases

- **Human in the loop:** in every high-stakes domain (medicine, law, code) the AI produces a draft and a human expert reviews it.
- **Grounding with RAG:** most business applications connect the model to company or domain data instead of relying only on what the model learned during training.
- **Hallucinations are the main shared risk,** so citations, verification and evaluation are essential parts of any GenAI product.
- **Security and privacy** (prompt injection, data leakage, access control) must be designed in from the start.
