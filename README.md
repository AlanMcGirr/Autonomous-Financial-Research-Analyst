# 🧠 Autonomous Financial Research Analyst  
### Agentic AI • Tool Orchestration • Retrieval-Augmented Generation (RAG)

This project implements a **production-style autonomous AI agent** designed to perform end-to-end financial research and investment analysis.  
It was built as part of the **Johns Hopkins Agentic AI course**

Unlike traditional chatbots, this system is designed as a **goal-oriented, tool-driven agent** with constrained autonomy, traceability, and robust error handling.

## 📊 Autonomous Financial Research Analyst – 


**[Open the full rendered project by downloading the HTML file here](./Autonomous_financial_analyst_project.html)**
---
[![Autonomous Financial Research Agent – Walkthrough](https://img.youtube.com/vi/BOFLue-HUks/0.jpg)](https://youtu.be/BOFLue-HUks)
## 🔍 What This Agent Does

Given a natural language query (e.g. *“Analyze NVIDIA’s AI strategy”*), the agent autonomously:

- Retrieves real-time stock data (price, volume, market cap)
- Analyzes **3-year historical performance**
- Searches recent financial news and evaluates **market sentiment**
- Queries a **private knowledge base using RAG** (analyst reports on AI initiatives)
- Identifies risks, opportunities, and data gaps
- Produces a **Buy / Hold / Sell recommendation** with confidence level
- Cites sources for every factual claim

---

## 🧩 Core Architecture

### Agent Design
- Goal-oriented agent charter (not prompt-based Q&A)
- Explicit behavioral constraints (proactive, reactive, autonomous)
- Error handling and graceful degradation when tools fail
- Source-grounded outputs with auditability

### Tool Orchestration
- `get_stock_price()` – real-time financial metrics  
- `get_stock_history()` – 3-year performance analysis  
- `search_financial_news()` – real-time news retrieval  
- `analyze_sentiment()` – sentiment scoring  
- `query_private_database()` – RAG-powered access to private analyst reports  

### RAG Pipeline
- PDF document loading (analyst reports)
- Chunking with overlap for context preservation
- Embedding generation (OpenAI embeddings)
- Vector storage using **ChromaDB**
- Semantic retrieval (top-k similarity search)
- Grounded response generation with citations

### Agent Orchestration
- Built using **LangGraph StateGraph**
- Explicit routing logic:  
  `Agent → Tools → Agent → Final Response`
- Optional conversation memory for multi-turn analysis

---

## 📊 Advanced Capabilities

- **Multi-company investment ranking**  
  (financial performance + AI innovation weighted scoring)
- **Synergistic tool usage**  
  (news → sentiment → RAG → synthesis)
- **Healthcare & education transferability analysis**
- Demonstrated robustness under tool failures and missing data

---

## 🎓 Key Learnings

> **Smarter-looking answers are not better agents.**  
> Better agents are **traceable, constrained, robust under failure, and designed as systems**.

This project clarified:
- When to use **RAG vs fine-tuning**
- How to design agents as **systems**, not prompts
- How to validate retrieval *before* generation
- How to scale from single-query analysis to portfolio-level intelligence

---

## 🚀 Future Scope

- Live deployment (FastAPI backend + real APIs)
- Frontend interface for interactive querying
- Extending agentic layers to:
  - **Education** (guided learning agents for game development)
  - **Healthcare / medical tourism**
  - **Enterprise analytics & decision support**

---

## 📓 Project Artifacts

This project includes both a **fully implemented autonomous agent** and an **interactive educational demo** explaining the architecture.

### 1️⃣ Jupyter Notebook – Full Implementation

The complete implementation of the autonomous Financial Research Analyst Agent, including:
- Tool definitions and orchestration
- LangGraph state management
- RAG pipeline (ChromaDB + embeddings)
- Error handling and routing logic
- Multi-company investment ranking
- End-to-end testing and validation

📄 **Notebook:**  
👉 **[Autonomous Financial Analyst – Full Notebook](./Autonomous_financial_analyst_project2%20(1).ipynb)**

> Recommended: View directly in Jupyter, Colab, or VS Code for full interactivity.

---

### 2️⃣ Interactive Demo – Agent Architecture Visualization

An interactive visual demo built using Claude Artifacts to explain:
- Agent evolution (LLM → Autonomous → RAG-enhanced)
- Tool orchestration flow
- RAG pipeline
- Error handling behavior
- Multi-company ranking logic

🎨 **Claude Artifact Demo:**  
https://claude.ai/public/artifacts/60938a4d-ae0a-4e58-8bc0-e2e39e9bfa16

> This demo is for **education and communication** only.  
> The production logic lives in the notebook above.

---
## 🎥 Project Walkthrough Video

This short walkthrough video explains the design and implementation of the **Autonomous Financial Research Analyst Agent**, including:

- Evolution from reactive LLMs → autonomous agents
- Tool orchestration and routing logic
- Retrieval-Augmented Generation (RAG) with ChromaDB
- Investment analysis workflow and recommendations
- Key learnings and design trade-offs

▶️ **Watch the full walkthrough:**  
https://youtu.be/BOFLue-HUks

## 👤 Author

**Alan McGirr**  
AI Product / Solutions Architecture • Agentic Systems • Applied AI  

---
