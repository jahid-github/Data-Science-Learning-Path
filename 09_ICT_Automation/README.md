# Phase 9 — AI Engineering, LLMs, and ICT Automation

Modern AI products increasingly depend on engineering **around** models — not only the models themselves. This phase covers LLM application design, retrieval systems, agentic workflows, and deploying production-grade AI automation systems.

---

## What You Will Build Toward

- Chat systems and document AI assistants
- Agent workflows that take real-world actions
- Internal knowledge bases with RAG
- Customer support automation
- Domain-specific AI applications (e.g., robotics command interfaces)
- Enterprise automation pipelines

---

## Learning Steps

### 1. LLM Application Design
- API-based AI application design (OpenAI, Anthropic, Gemini, local via Ollama)
- Prompt engineering: zero-shot, few-shot, chain-of-thought
- Structured outputs and function calling
- Context window management and chunking strategies

### 2. Retrieval and Knowledge Systems
- **Vector Databases:** Weaviate, Pinecone, ChromaDB — store and search embeddings
- **RAG (Retrieval-Augmented Generation):** ground LLM responses in your own data
- Embedding models: `text-embedding-3-small`, HuggingFace sentence-transformers
- Semantic search vs keyword search — when to use each
- Chunking, overlap, metadata filtering, reranking

### 3. Tool Use, Orchestration, and Agents
- **Tool Calling:** let LLMs invoke external functions (APIs, databases, calculators)
- **LangChain:** chains, tools, memory, agents — orchestrate complex LLM workflows
- **LlamaIndex:** document ingestion, indexing, query engines for knowledge systems
- **Agents:** ReAct, OpenAI Assistants API, Hugging Face Agents
- **Multi-Agent Systems:** task delegation between specialized agents

### 4. Automation and Applied Systems
- Workflow automation: LLM-driven pipelines for real business tasks
- Enterprise automation: connecting LLMs to CRMs, ERPs, ticketing systems
- RPA + AI integration: UiPath with AI components
- Sector-specific automation: manufacturing (Phase 8 bridge), customer support, data ops

### 5. Backend & API Development
- **FastAPI:** build production-grade REST APIs to expose ML/AI models as services
- **Django:** full-featured web framework for data-driven applications
- **Node.js:** JavaScript runtime for API services and real-time backends

### 6. Deployment, Monitoring, and Responsible AI
- Containerize AI apps with Docker + FastAPI
- CI/CD pipelines for LLM applications (GitHub Actions)
- AI system monitoring: response quality, latency, token costs
- Guardrails, safety filters, and content moderation
- Responsible AI: explainability, bias detection, audit trails

---

## Tools & Frameworks

### AI Engineering & LLM Stack

| Tool | Description |
|------|-------------|
| **[LangChain](https://python.langchain.com/docs/introduction/)** | Framework for building LLM-powered chains, agents, and tools — the most widely used LLM orchestration library |
| **[LlamaIndex](https://docs.llamaindex.ai/)** | Data framework for connecting LLMs to external knowledge sources — RAG, document ingestion, query engines |
| **[Ollama](https://ollama.com/)** | Run large language models locally (Llama, Mistral, Gemma, Phi) — no cloud dependency |
| HuggingFace Hub | Access and deploy thousands of open-source models |
| OpenAI API | GPT-4, DALL-E, Whisper, Embeddings — industry-standard AI APIs |
| Anthropic API | Claude models — strong for instruction-following and long context |

### Backend & APIs

| Tool | Description |
|------|-------------|
| **[FastAPI](https://github.com/fastapi/fastapi)** | Modern, high-performance Python web framework — ideal for exposing ML models as REST APIs with automatic docs |
| **[Django](https://www.djangoproject.com/)** | Full-featured Python web framework — batteries included: ORM, admin, auth |
| **Node.js** | JavaScript runtime for event-driven, non-blocking I/O backends and real-time services |

---

## Core Concepts Reference

| Topic | What It Covers |
|-------|---------------|
| **Vector Databases** | Store embeddings, semantic similarity search (Weaviate, Pinecone, ChromaDB) |
| **RAG** | Retrieval-Augmented Generation — ground LLM output in real documents |
| **Tool Calling** | LLMs invoking external functions (APIs, databases, calculators) |
| **Orchestration** | Chaining multiple LLM calls + tools into workflows (LangChain, LlamaIndex) |
| **Agents** | LLMs that plan and execute multi-step tasks autonomously |
| **Multi-Agent Systems** | Multiple specialized agents collaborating to complete complex tasks |
| **Guardrails** | Safety filters, output validation, PII detection for production AI |

---

## PDF Resources

* [AI Agents Cheat Sheet](./ai-agents-cheat-sheet.pdf)
* [Working with Hugging Face](./working-with-hugging-face.pdf)

---

## Learning Resources

* [OpenAI Documentation](https://platform.openai.com/docs)
* [OpenAI Function Calling Guide](https://platform.openai.com/docs/guides/function-calling)
* [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course)
* [Hugging Face Agents Course](https://huggingface.co/learn/agents-course)
* [LangChain Documentation](https://python.langchain.com/docs/introduction/)
* [LlamaIndex Documentation](https://docs.llamaindex.ai/)
* [FastAPI Documentation](https://fastapi.tiangolo.com/)

## Prjects
### Upcoming
### Develpoing
- [Building-RAG-Chatbots-for-Technical-Documentation](https://github.com/jahid-github/Building-RAG-Chatbots-for-Technical-Documentation)