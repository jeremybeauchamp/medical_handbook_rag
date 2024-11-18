# Medical Question Answering with Retrieval-Augmented Generation (RAG)

This project explores medical question answering using Retrieval-Augmented Generation (RAG). RAG optimizes large language models (LLMs) by referencing an external knowledge base before generating responses, improving accuracy and relevance.

## Why RAG for Medical Question Answering?

Large Language Models (LLMs) face challenges in medical domains:

* **Hallucinations:** Presenting false information.
* **Outdated Information:**  LLM training data is static.
* **Lack of Source Attribution:**  Difficult to verify responses.
* **Terminology Confusion:** Inconsistent use of medical terms.

RAG addresses these challenges by grounding LLM responses in a trusted knowledge base.

## Benefits of RAG

* **Cost-Effective:** Avoids expensive LLM retraining.
* **Current Information:** Integrates the latest research and data.
* **Enhanced User Trust:** Provides source attribution and citations.
* **Developer Control:**  Fine-grained control over information sources.

## How RAG Works

1. **External Knowledge Base:** Create a knowledge base from sources like medical texts, research papers, and clinical guidelines. This data is often converted into vector embeddings for efficient searching.

2. **Retrieval:**  User queries are embedded and used to retrieve relevant information from the knowledge base.

3. **Augmented Prompt:** The retrieved information is added to the LLM prompt, providing context for generating accurate and informed responses.

4. **Knowledge Base Updates:**  Implement mechanisms to keep the knowledge base up-to-date.

## Project Specifics

This project utilizes the Oxford Handbook of Clinical Medicine as its initial knowledge base. The PDF has been parsed and processed into individual pages using `llama_parse`. The current focus is on exploring different document processing methods and libraries for RAG.

## Current Progress

* Parsed the Oxford Handbook of Clinical Medicine into 911 individual text files using `llama_parse`.
* Saved the parsed pages in the `medical_pages` directory.
* Explored basic file saving and text manipulation using Python.

## Next Steps

* Investigate alternative document processing libraries (e.g., `PyPDF2`, `unstructured`).
* Experiment with different vector databases (e.g., `Faiss`, `Pinecone`).
* Implement a RAG pipeline using `LlamaIndex` or `LangChain`.

## Dependencies

* `llama_index`
* `llama_parse`
* `langchain`
* `openai`
* `tavily`