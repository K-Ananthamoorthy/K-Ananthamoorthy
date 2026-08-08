<h1 align="center">K Ananthamoorthi Holla</h1>
<p align="center">AI Engineer &nbsp;|&nbsp; LLM systems, RAG, and multi-agent workflows</p>

<p align="center">
  <a href="https://ananthamoorthi.dev"><img src="https://img.shields.io/badge/Portfolio-ananthamoorthi.dev-F06038?style=flat-square"></a>
  <a href="https://www.linkedin.com/in/ananthamoorthi/"><img src="https://img.shields.io/badge/LinkedIn-ananthamoorthi-0A66C2?style=flat-square&logo=linkedin&logoColor=white"></a>
  <a href="mailto:ananthamoorthi04@gmail.com"><img src="https://img.shields.io/badge/Email-ananthamoorthi04-D14836?style=flat-square&logo=gmail&logoColor=white"></a>
</p>

I build LLM systems that hold up in production. Retrieval that is grounded in real sources, output that is validated before a user sees it, and deterministic code making the calls that have to be reproducible.

A model is good at language. It should not be the thing that decides whether a number is dangerous, or commits an action you cannot undo. Most of what I build is some version of that split.

**Right now** I am building agentic systems and pushing small models to run useful workloads fully offline, on device.

## mySutra.ai

I was the founding engineer at SutraAI Solutions, where I built the AI behind [mysutra.ai](https://mysutra.ai), a health app that is live on the Google Play Store.

You photograph a meal, the app works out what you ate, and turns that into insight you can act on, with an AI coach to make sense of the trend rather than just the number.

I owned the AI side of it from first prototype to launch, built the backend it runs on, and shipped the mobile app to the Play Store. Being the founding engineer meant deciding what the product should do as much as building it.

Health is also where a confident wrong answer does real damage, so a lot of the work was not about making the AI smarter. It was about deciding what it was allowed to say, and proving it stayed inside that line.

## Featured project

### [Project Sentinel](https://github.com/K-Ananthamoorthy/Sentinel)
**Autonomous multi-agent cold-chain monitoring**

Vaccines and other refrigerated medicine spoil quietly. By the time someone notices the temperature slipped, the shipment is already lost. Sentinel watches those shipments in real time and reroutes them to the nearest cold storage on its own, before the cargo is gone.

- A five-stage LangGraph pipeline runs the decision: assess the risk, find candidate cold storage warehouses, score them on safety, time and cost, then commit the reroute.
- Redis pub/sub separates the simulation from model inference, so calls that take several seconds never stall the real-time loop. Four asyncio workers handle simulation, breach detection, and WebSocket fan-out.
- The final commit is deterministic weighted scoring, not the model. Every reroute can be reproduced and audited afterwards, which is the whole point when the cargo is pharmaceutical. Pydantic validates output and IDs are checked against the database.

`Python` `FastAPI` `LangGraph` `Groq (Llama 3.3 70B)` `PostgreSQL` `Redis` `Docker` `WebSockets`

## More projects

### [PlainLabs](https://github.com/K-Ananthamoorthy/plainlabs)
**Offline lab-report explainer on a small on-device model**

Upload a blood report, get every value explained in plain language and flagged normal, borderline, abnormal, or urgent, with questions worth asking a doctor.

- Runs fully offline on MedGemma 4B via Ollama. A blood report is health data, and it should not need a cloud chatbot to become readable.
- The model only does language. Every severity flag is a deterministic comparison against curated reference ranges, never model output, which is what makes a 4B model safe to put in front of a health tool.
- Built as a LangGraph StateGraph, alternating between code and model on purpose so each step stays isolated and testable.

`Python` `LangGraph` `Ollama (MedGemma 4B)` `100% offline`

### [Doc Companion](https://github.com/K-Ananthamoorthy/student-assistant-rag)
**Agentic RAG for PDFs, fully offline**

A LangGraph agent that decides how to answer each question instead of retrieving blindly, and cites the page it came from.

- A few-shot classifier routes every question, 8 out of 8 on a routing testset. The agent chooses when to retrieve, grades its own chunks, and rewrites the query once when retrieval misses.
- Corpus level questions skip top-k entirely and are answered from per-document cards built at ingestion, because no set of k chunks can represent a whole collection.
- Guardrails are graduated into verified, caution, and refuse. I switched to plain text verdicts after measuring that JSON constrained output silently defaulted to false on a 3B model.

`Python` `LangGraph` `LangChain` `Ollama` `ChromaDB` `Streamlit`

### [LocalGPT](https://github.com/K-Ananthamoorthy/localgpt-llama.rn)
**On-device AI chat** &nbsp;·&nbsp; [Download APK](https://github.com/K-Ananthamoorthy/localgpt-llama.rn/releases)

Quantized LLMs running entirely on the phone through llama.cpp. No network, no data leaving the device, with GPU offload where available to keep latency usable on mid-range hardware.

`React Native` `llama.cpp` `Quantized open-source LLMs`

## Skills

| | |
|---|---|
| **Languages** | Python, TypeScript, SQL |
| **AI and LLM** | LLM integration and orchestration, RAG, prompt engineering, embeddings and vector search, multi-agent workflows, LLM evaluation, guardrails and hallucination control, fine tuning with Unsloth, on-device inference |
| **Frameworks** | LangGraph, LangChain, FastAPI, Ollama, llama.cpp, NumPy, pandas, scikit-learn, pytest, Flutter, React Native |
| **Databases** | PostgreSQL, pgvector, ChromaDB, Supabase, Firebase |
| **Backend and Tools** | REST API design, Docker, Git, Linux |

## Reach me

Happy to talk about AI engineering work, or anything above.

[ananthamoorthi04@gmail.com](mailto:ananthamoorthi04@gmail.com) &nbsp;·&nbsp; [ananthamoorthi.dev](https://ananthamoorthi.dev) &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/ananthamoorthi/)

<sub>B.E. in Artificial Intelligence and Machine Learning, Visvesvaraya Technological University (VTU), Belagavi, 2025.</sub>
