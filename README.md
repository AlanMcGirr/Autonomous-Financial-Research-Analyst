# Autonomous-Financial-Research-Analyst
This project implements a production-style autonomous AI agent designed to perform end-to-end financial research and investment analysis.

It was built as part of the Johns Hopkins Agentic AI course and received a perfect score (20/20).

Unlike traditional chatbots, this system is designed as a goal-oriented, tool-driven agent with constrained autonomy, traceability, and error handling.

⸻

🔍 What This Agent Does

Given a natural language query (e.g. “Analyze NVIDIA’s AI strategy”), the agent autonomously:
	•	Retrieves real-time stock data (price, volume, market cap)
	•	Analyzes 3-year historical performance
	•	Searches recent financial news and evaluates market sentiment
	•	Queries a private knowledge base using RAG (analyst reports on AI initiatives)
	•	Identifies risks, opportunities, and data gaps
	•	Produces a Buy / Hold / Sell recommendation with confidence level
	•	Cites sources for every factual claim

⸻

🧩 Core Architecture

Agent Design
	•	Goal-oriented agent charter (not prompt-based Q&A)
	•	Explicit behavioral constraints (proactive, reactive, autonomous)
	•	Error handling and graceful degradation when tools fail
	•	Source-grounded outputs with auditability

Tool Orchestration
	•	get_stock_price() – real-time financial metrics
	•	get_stock_history() – 3-year performance analysis
	•	search_financial_news() – real-time news retrieval
	•	analyze_sentiment() – sentiment scoring
	•	query_private_database() – RAG-powered access to private analyst reports

RAG Pipeline
	•	PDF document loading (analyst reports)
	•	Chunking with overlap for context preservation
	•	Embedding generation (OpenAI embeddings)
	•	Vector storage using ChromaDB
	•	Semantic retrieval (top-k similarity search)
	•	Grounded response generation with citations

Agent Orchestration
	•	Built using LangGraph StateGraph
	•	Explicit routing logic: Agent → Tools → Agent → Final Response
	•	Optional conversation memory for multi-turn analysis

⸻

📊 Advanced Capabilities
	•	Multi-company investment ranking (financial + AI innovation weighted scoring)
	•	Synergistic tool usage (news → sentiment → RAG → synthesis)
	•	Healthcare & education transferability analysis
	•	Demonstrated robustness under tool failures and missing data

⸻

🎓 Key Learnings

Smarter-looking answers are not better agents.
Better agents are traceable, constrained, robust under failure, and designed as systems.

This project significantly clarified:
	•	When to use RAG vs fine-tuning
	•	How to design agents as systems, not prompts
	•	How to validate RAG outputs before trusting generation
	•	How to scale analysis from single queries to portfolio-level intelligence

⸻

🚀 What’s Next
	•	Live deployment (FastAPI backend + real APIs)
	•	Frontend interface for interactive querying
	•	Extending agentic layers to:
	•	Education (guided learning agents for game development)
	•	Healthcare / medical tourism
	•	Enterprise analytics & decision support
