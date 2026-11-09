# GenAI Vocabulary

Key terms I need to know and use as a specialist in Generative AI application development. Explanations are written in my own words based on my current understanding; I plan to expand this file during the course.

| # | Term | Explanation |
|---|---|---|
| 1 | **Generative AI (GenAI)** | AI that creates new content — text, code, images, audio — instead of only classifying or predicting from existing data. |
| 2 | **Large Language Model (LLM)** | A very large neural network trained on huge amounts of text to predict the next token; this simple task lets it answer questions, write and reason. Examples: GPT, Claude, Gemini, Llama. |
| 3 | **Token** | The small piece of text a model actually works with — a word, part of a word or a symbol. Prices and limits of LLMs are counted in tokens. |
| 4 | **Context window** | The maximum number of tokens the model can "see" at once: the prompt, documents, chat history and the answer together. |
| 5 | **Prompt** | The input instruction or question we give to the model. The quality of the prompt strongly affects the quality of the answer. |
| 6 | **Prompt engineering** | The practice of designing prompts (role, context, examples, output format) to get reliable and useful results from a model. |
| 7 | **System prompt** | Hidden instructions set by the developer that define how the assistant should behave in every conversation. |
| 8 | **Few-shot prompting** | Giving the model a few examples of input and expected output inside the prompt so it follows the same pattern. |
| 9 | **Hallucination** | When the model generates information that sounds confident and correct but is actually false or invented. |
| 10 | **Grounding** | Connecting the model's answer to real, verifiable data (documents, databases) to reduce hallucinations. |
| 11 | **Embedding** | A list of numbers (a vector) that represents the meaning of a text, so that texts with similar meaning have similar vectors. |
| 12 | **Vector database** | A database that stores embeddings and quickly finds the ones most similar to a query. Examples: Pinecone, Weaviate, pgvector. |
| 13 | **Retrieval-Augmented Generation (RAG)** | An approach where relevant documents are first retrieved from a knowledge base and then added to the prompt, so the model answers based on that data. |
| 14 | **Chunking** | Splitting long documents into smaller pieces before creating embeddings, so retrieval can find the exact relevant part. |
| 15 | **Fine-tuning** | Additional training of an existing model on a specific dataset to adapt its style or knowledge for a particular task. |
| 16 | **Temperature** | A setting that controls randomness: low temperature gives more predictable answers, high temperature gives more creative and varied ones. |
| 17 | **AI agent** | A system where an LLM plans steps, uses tools (APIs, code execution, search) and acts in a loop to complete a goal, not just to answer once. |
| 18 | **Tool calling (function calling)** | The model's ability to request a specific function or API with structured arguments, which the application then executes. |
| 19 | **Copilot** | An AI assistant that works alongside a human inside their tool (IDE, office apps) and suggests actions, while the human stays in control. |
| 20 | **Multimodal model** | A model that can understand or generate more than one type of data, for example text and images together. |
| 21 | **Guardrails** | Rules and filters around a model that block unsafe, off-topic or policy-violating inputs and outputs. |
| 22 | **Prompt injection** | An attack where malicious text in user input or retrieved documents tries to override the model's original instructions. |
| 23 | **Human-in-the-loop** | A design where a person reviews or approves AI output before it is used, especially in high-risk decisions. |
| 24 | **Evaluation (evals)** | Systematic testing of an AI system's answers against expected results to measure quality and catch regressions. |
