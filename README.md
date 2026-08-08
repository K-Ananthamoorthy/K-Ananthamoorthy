<h1 align="center">K Ananthamoorthi Holla</h1>
<p align="center">AI Engineer &nbsp;|&nbsp; LLM systems, RAG, and multi-agent workflows</p>

<p align="center">
  <a href="https://ananthamoorthi.dev"><img src="https://img.shields.io/badge/Portfolio-ananthamoorthi.dev-F06038?style=flat-square"></a>
  <a href="https://www.linkedin.com/in/ananthamoorthi/"><img src="https://img.shields.io/badge/LinkedIn-ananthamoorthi-0A66C2?style=flat-square&logo=linkedin&logoColor=white"></a>
  <a href="mailto:ananthamoorthi04@gmail.com"><img src="https://img.shields.io/badge/Email-ananthamoorthi04-D14836?style=flat-square&logo=gmail&logoColor=white"></a>
</p>

## About

I am an AI engineer based in Bengaluru with over a year of production experience building LLM systems end to end.

Most of that came from being the founding engineer at SutraAI Solutions, where I built the AI backend for [mysutra.ai](https://mysutra.ai), a health intelligence platform that is live on the Google Play Store. Working on health content taught me to care less about clever prompts and more about whether the output can be trusted.

That is what I optimise for now: retrieval that is grounded in real sources, responses that are validated before they reach a user, and deterministic code making the decisions that have to be reproducible. An LLM is good at language. It should not be the thing that commits an irreversible action.

Lately I have been spending my time on agentic systems, LLM evaluation, and getting models to run offline on device.

## Experience

### AI Engineer, Founding Team
**SutraAI Solutions LLP** &nbsp;·&nbsp; Manipal, Karnataka &nbsp;·&nbsp; Jun 2025 to Jul 2026

- Built the production AI backend for mysutra.ai end to end, covering LLM integration, prompt engineering, and multi-step LangGraph workflows with tool calling and conditional routing.
- Powered meal analysis, personalised health insights, and an AI coach on top of that pipeline.
- Designed and indexed a RAG pipeline over a nutrition knowledge base normalised from open sources such as Open Food Facts and government food composition data, which improved accuracy and cut per query search cost.
- Ran domain adaptation fine tuning experiments with Unsloth on open weight Llama and GPT-OSS models, and curated a labelled food dataset of roughly 13,000 images for custom vision training.
- Implemented health content guardrails covering medical advice boundaries, disclaimers, and refusal handling, then validated output with retrieval quality evaluation against reference data.
- Built the supporting REST APIs and PostgreSQL data models, and shipped the companion Flutter app to the Play Store.

### Project Intern
**IoTracX** &nbsp;·&nbsp; Manipal, Karnataka &nbsp;·&nbsp; Jan 2025 to May 2025

- Worked on on-device LLM inference for offline use, tuning latency and memory footprint for constrained mobile hardware.
- Ran vision language model and fine tuning experiments, and refined datasets to improve training data quality.

### Intern, IT Department
**Wipro Consumer Care & Lighting** &nbsp;·&nbsp; Bengaluru, Karnataka &nbsp;·&nbsp; Nov 2023

- Contributed to internal IT prototypes for a market survey application and a vendor portal, working on Node.js backend services and React frontend components.
- First hands-on exposure to enterprise practices: requirement discussions, version control workflows, and iterative delivery inside an IT team.

## Projects

### [Project Sentinel](https://github.com/K-Ananthamoorthy/Sentinel)
Autonomous multi-agent cold-chain monitoring

An event-driven backend that watches refrigerated pharmaceutical shipments in real time and reroutes them on its own when the temperature drifts out of range.

- A five-stage LangGraph pipeline handles the decision: assess risk, select a cold storage warehouse, score the options on safety, time and cost, then apply the reroute.
- Redis pub/sub separates the simulation from LLM inference, so model calls that take several seconds never stall the real-time loop. Four concurrent asyncio workers handle simulation, breach detection, and WebSocket fan-out.
- The committing decision is deterministic weighted scoring, not the model, so every reroute can be reproduced and audited. Output is validated with Pydantic and IDs are cross-checked against the database to contain hallucination.

`Python` `FastAPI` `LangGraph` `Groq (Llama 3.3 70B)` `PostgreSQL` `SQLAlchemy` `Redis` `Docker` `WebSockets` `JWT`

### [Doc Companion](https://github.com/K-Ananthamoorthy/student-assistant-rag)
Agentic RAG for PDFs, fully offline

A LangGraph agent that decides how to answer each question instead of retrieving blindly, and cites the page it got the answer from.

- A few-shot classifier routes every question, scoring 8 out of 8 on a routing testset. The agent decides when to retrieve, grades its own chunks, and rewrites the query once when retrieval misses.
- Corpus level questions skip top-k entirely and are answered from per-document cards built at ingestion, because no set of k chunks can represent a whole document collection.
- Guardrails are graduated into verified, caution, and refuse, pairing a deterministic citation guard with an LLM grounding judge. I moved to plain text verdicts after measuring that JSON constrained output was silently defaulting to false on a 3B model.
- Runs fully offline on Ollama over persistent ChromaDB, with a golden set eval harness that scores faithfulness and correctness.

`Python` `LangGraph` `LangChain` `Ollama` `ChromaDB` `Streamlit`

### [LocalGPT](https://github.com/K-Ananthamoorthy/localgpt-llama.rn)
Offline on-device AI chat &nbsp;·&nbsp; [Download APK](https://github.com/K-Ananthamoorthy/localgpt-llama.rn/releases)

A privacy-first mobile chat app that runs quantized LLMs entirely on the phone.

- Everything happens on device through llama.cpp, so the app works with no network and no user data ever leaves the phone.
- Inference is accelerated by offloading computation to the phone GPU where one is available, which noticeably improves latency on mid-range hardware.

`React Native` `llama.cpp` `Quantized open-source LLMs`

## Skills

| | |
|---|---|
| **Languages** | Python, TypeScript, SQL |
| **AI and LLM** | LLM integration and orchestration, RAG, prompt engineering, embeddings and vector search, multi-agent workflows, LLM evaluation, guardrails and hallucination control, fine tuning with Unsloth, on-device inference |
| **Frameworks** | LangGraph, LangChain, FastAPI, Ollama, llama.cpp, NumPy, pandas, scikit-learn, pytest, Flutter, React Native |
| **Databases** | PostgreSQL, pgvector, ChromaDB, Supabase, Firebase |
| **Backend and Tools** | REST API design, Docker, Git, Linux |

## Education

**B.E. in Artificial Intelligence and Machine Learning**, 2021 to 2025
Visvesvaraya Technological University (VTU), Belagavi &nbsp;·&nbsp; CGPA 8.4

## Contact

Open to conversations about AI engineering roles, or about anything above.

- Email: [ananthamoorthi04@gmail.com](mailto:ananthamoorthi04@gmail.com)
- Portfolio: [ananthamoorthi.dev](https://ananthamoorthi.dev)
- LinkedIn: [in/ananthamoorthi](https://www.linkedin.com/in/ananthamoorthi/)
