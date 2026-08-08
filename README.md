<h1 align="center">Hi, I'm K Ananthamoorthi Holla</h1>
<h3 align="center">AI Engineer — LLM systems, RAG, and multi-agent workflows</h3>

<p align="center">
  <a href="https://ananthamoorthi.dev"><img src="https://img.shields.io/badge/Portfolio-ananthamoorthi.dev-F06038"></a>
  <a href="https://www.linkedin.com/in/ananthamoorthi/"><img src="https://img.shields.io/badge/LinkedIn-ananthamoorthi-0A66C2?logo=linkedin"></a>
  <a href="mailto:ananthamoorthi04@gmail.com"><img src="https://img.shields.io/badge/Email-ananthamoorthi04-D14836?logo=gmail&logoColor=white"></a>
</p>

---

### About Me

AI Engineer with 1+ year of production experience building LLM systems end to end — RAG, multi-agent LangGraph workflows, evaluation, and safety guardrails.

I was the founding engineer at **SutraAI Solutions**, where I designed and shipped the AI backend for **[mysutra.ai](https://mysutra.ai)**, a health intelligence platform live on the Google Play Store.

What I care about is reliable model output: grounded retrieval, validated responses, and deterministic control where correctness actually matters. If a decision has to be reproducible and auditable, it shouldn't be the LLM making it.

- B.E. in Artificial Intelligence & Machine Learning, SMVITM (2021–2025), CGPA 8.4
- Based in Bengaluru, Karnataka
- Currently interested in agentic systems, LLM evaluation, and on-device inference

---

### Projects

**[Project Sentinel](https://github.com/K-Ananthamoorthy/Sentinel)** — Autonomous multi-agent cold-chain monitoring
`Python` `FastAPI` `LangGraph` `Groq (Llama 3.3 70B)` `PostgreSQL` `Redis` `Docker` `WebSockets`

Event-driven backend that monitors refrigerated pharmaceutical shipments in real time and autonomously reroutes them on temperature excursion, through a five-stage LangGraph pipeline: assess risk → select cold-storage warehouse → score safety/time/cost → apply reroute. Redis pub/sub decouples simulation from LLM inference so multi-second model calls never stall the real-time loop. The committing decision stays deterministic via weighted scoring rather than the LLM, so every reroute is reproducible and auditable.

**[Doc Companion](https://github.com/K-Ananthamoorthy/student-assistant-rag)** — Agentic RAG for PDFs, fully offline
`Python` `LangGraph` `LangChain` `Ollama` `ChromaDB` `Streamlit`

A LangGraph agent that routes each question with a few-shot classifier (8/8 on a routing testset), decides when to retrieve, grades its own chunks, and rewrites the query once when retrieval misses — answering with per-page citations. Corpus-level questions bypass top-k entirely and are answered from per-document cards built at ingestion, since no k chunks can represent a whole document set. Graduated guardrails (verified / caution / refuse) pair a deterministic citation guard with an LLM grounding judge. Runs fully offline on Ollama with a golden-set eval harness scoring faithfulness and correctness.

**[LocalGPT](https://github.com/K-Ananthamoorthy/localgpt-llama.rn)** — Offline on-device AI chat &nbsp;·&nbsp; [Download APK](https://github.com/K-Ananthamoorthy/localgpt-llama.rn/releases)
`React Native` `llama.cpp` `Quantized open-source LLMs`

Privacy-first mobile chat app running quantized LLMs entirely on-device via llama.cpp — fully offline, with no user data leaving the phone. Inference is accelerated by offloading computation to the phone's GPU when available.

---

### Experience

**AI Engineer (Founding Team)** · SutraAI Solutions LLP &nbsp;·&nbsp; Jun 2025 – Jul 2026
Built the production AI backend for mysutra.ai end to end — LLM integration, prompt engineering, and multi-step LangGraph workflows with tool calling and conditional routing, powering meal analysis, personalized health insights, and an AI coach. Designed a RAG pipeline over a nutrition knowledge base normalized from open sources (Open Food Facts, government food-composition data), ran domain-adaptation fine-tuning experiments with Unsloth on Llama and GPT-OSS models, curated a ~13,000-image labelled food dataset, and implemented health-content guardrails with retrieval-quality evaluation. Also shipped the companion Flutter app to the Play Store.

**Project Intern** · IoTracX &nbsp;·&nbsp; Jan 2025 – May 2025
On-device LLM inference for offline use — optimizing latency and memory footprint on constrained mobile hardware, plus VLM and fine-tuning experiments and dataset refinement.

**Intern, IT Department** · Wipro Consumer Care & Lighting &nbsp;·&nbsp; Nov 2023
Internal IT prototypes for a Market Survey application and a Vendor Portal — Node.js backend services and React frontend components.

---

### Tech I Actually Work With

**Languages:** Python, TypeScript, SQL

**AI & LLM:** LLM integration and orchestration, RAG, prompt engineering, embeddings and vector search, multi-agent workflows, LLM evaluation, guardrails and hallucination control, fine-tuning (Unsloth), on-device inference

**Frameworks & Libraries:** LangGraph, LangChain, FastAPI, Ollama, llama.cpp, NumPy, pandas, scikit-learn, pytest, Flutter, React Native

**Databases:** PostgreSQL, pgvector, ChromaDB, Supabase, Firebase

**Backend & Tools:** REST API design, Docker, Git, Linux

---

### Reach Me

- Email: **ananthamoorthi04@gmail.com**
- Portfolio: **[ananthamoorthi.dev](https://ananthamoorthi.dev)**
- LinkedIn: **[in/ananthamoorthi](https://www.linkedin.com/in/ananthamoorthi/)**

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=K-Ananthamoorthy&label=Profile%20views&color=28C8C0&style=flat" alt="profile views" />
</p>
