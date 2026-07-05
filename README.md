# Hi, I'm Berkay

📍 **London ↔ Bristol** | ☁️ **Software Engineer** | 🧠 **AI Researcher** | 🚀 **Founder @ [TensorSphere](https://tensorsphere.com)**

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Go](https://img.shields.io/badge/-Go-00ADD8?style=flat&logo=go&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/-Azure-0078D4?style=flat&logo=microsoft-azure&logoColor=white)
![Terraform](https://img.shields.io/badge/-Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![Bicep](https://img.shields.io/badge/-Bicep-0078D4?style=flat&logo=microsoft-azure&logoColor=white)

I build secure cloud infrastructure and AI tooling, with a research focus on Trustworthy Digital Infrastructure — the intersection of Sovereign AI, Explainable AI, and secure cloud architecture.

## Open Source

- 🧪 **[mcp-llm-eval](https://github.com/berkayildi/mcp-llm-eval)** — LLM evaluation engine powering CI/CD quality gates and benchmark runs. Run datasets against multiple models, score with LLM-as-judge, enforce quality thresholds. Used by [LLMShot](https://llmshot.vercel.app) for cross-provider benchmarking.
  <br>[![PyPI](https://img.shields.io/pypi/v/mcp-llm-eval)](https://pypi.org/project/mcp-llm-eval/) [![Downloads](https://img.shields.io/pypi/dm/mcp-llm-eval)](https://pypi.org/project/mcp-llm-eval/)

- 🎬 **[mcp-content-pipeline](https://github.com/berkayildi/mcp-content-pipeline)** — YouTube and X feed analysis pipeline with AI-generated infographics. 6 tools, 72 tests.
  <br>[![PyPI](https://img.shields.io/pypi/v/mcp-content-pipeline)](https://pypi.org/project/mcp-content-pipeline/) [![Downloads](https://img.shields.io/pypi/dm/mcp-content-pipeline)](https://pypi.org/project/mcp-content-pipeline/)

- ☁️ **[rag-on-azure](https://github.com/berkayildi/rag-on-azure)** — Production-shaped RAG application on Microsoft Azure. Bicep IaC + FastAPI + LangGraph over UK regulatory corpus (FCA Handbook + HMRC). Multi-tenant via JWT-driven OData filters, OIDC-federated CI, mcp-llm-eval gate runs on every push to main, p95 retrieval 8.3ms, citation faithfulness 0.99. Live results render on [LLMShot](https://llmshot.vercel.app/retrieval).
  <br>[![GitHub](https://img.shields.io/github/v/release/berkayildi/rag-on-azure)](https://github.com/berkayildi/rag-on-azure/releases)

- 📊 **[LLMShot](https://github.com/berkayildi/llmshot)** — Multi-domain LLM benchmark dashboard. Real-time inference, text generation, and retrieval/RAG across 8 generation models, 4 retrievers, ~790 runs.
  <br>[![Live](https://img.shields.io/badge/live-llmshot.vercel.app-7c3aed)](https://llmshot.vercel.app) [![GitHub](https://img.shields.io/github/v/release/berkayildi/llmshot)](https://github.com/berkayildi/llmshot/releases)

- 📈 **[llm-benchmarks](https://github.com/berkayildi/llm-benchmarks)** — Benchmark datasets and results evaluating LLMs across providers on quality, latency, and cost. Served via GitHub Pages; rendered live in [LLMShot](https://llmshot.vercel.app).

- 🖼️ **[FeedShot](https://github.com/berkayildi/feedshot)** — YouTube and X feed content analysis + comic-book infographic. React/FastAPI web app wrapping mcp-content-pipeline. BYO API keys, zero sign-up.
  <br>[![Live](https://img.shields.io/badge/live-feedshot.vercel.app-7c3aed)](https://feedshot.vercel.app) [![GitHub](https://img.shields.io/github/v/release/berkayildi/feedshot)](https://github.com/berkayildi/feedshot/releases)

- 💸 **[mcp-aws-cost-explorer](https://github.com/berkayildi/mcp-aws-cost-explorer)** — AWS cost analysis for AI agents. 7 tools: forecasting, anomaly detection, rightsizing.
  <br>[![NPM](https://img.shields.io/npm/v/mcp-aws-cost-explorer)](https://www.npmjs.com/package/mcp-aws-cost-explorer) [![Downloads](https://img.shields.io/npm/dm/mcp-aws-cost-explorer)](https://www.npmjs.com/package/mcp-aws-cost-explorer)

- 🔍 **[mcp-tfstate-reader](https://github.com/berkayildi/mcp-tfstate-reader)** — Terraform state security auditor. 16 AWS rules, 5 tools, 55 tests.
  <br>[![PyPI](https://img.shields.io/pypi/v/mcp-tfstate-reader)](https://pypi.org/project/mcp-tfstate-reader/) [![Downloads](https://img.shields.io/pypi/dm/mcp-tfstate-reader)](https://pypi.org/project/mcp-tfstate-reader/)

- 📰 **[daily-news](https://github.com/berkayildi/daily-news)** — Daily Bloomberg Technology analyses with comic-book infographics. Auto-synced.
  <br>[![Last Commit](https://img.shields.io/github/last-commit/berkayildi/daily-news)](https://github.com/berkayildi/daily-news)

## How these connect

The five LLM repos form a small ecosystem:

- **[mcp-llm-eval](https://github.com/berkayildi/mcp-llm-eval)** is the evaluation engine. It ships as a PyPI package with an MCP server, a CLI, and pluggable retrieval adapters (BM25 plus three embedding-based).
- **[mcp-content-pipeline](https://github.com/berkayildi/mcp-content-pipeline)** consumes mcp-llm-eval as a CI quality gate, with its own golden dataset for video and X feed analysis.
- **[rag-on-azure](https://github.com/berkayildi/rag-on-azure)** consumes mcp-llm-eval against a deployed Azure AI Search index, snapshotting the corpus on every CI run and gating merges to main on retrieval and faithfulness thresholds.
- **[llm-benchmarks](https://github.com/berkayildi/llm-benchmarks)** is the data layer. Every benchmark run from any producer writes its JSON results here. Served via GitHub Pages.
- **[LLMShot](https://github.com/berkayildi/llmshot)** is the visualization layer. It fetches the benchmark JSON and renders three domain dashboards live.

One engine, multiple consumers, one public artifact. Each producer defines its own quality bar without forking the engine.

## Industry

- 🏦 **[Quantios](https://www.quantios.com/)** — LLM evaluation framework, WAF security, LangSmith observability (Fintech)
- ☁️ **[MindWalk](https://www.biostrand.be/)** — Lead frontend, Auth@Edge, AI agents (Biotech)
- 📡 **[Turkcell](https://www.turkcell.com.tr/)** — 5M+ user messaging platform (Telecom)
- 🔬 **[Huawei](https://www.huawei.com/)** — AI Database Query Platform, Sparkling Star Award (5G and R&D)
- 🏗️ **[Ronesans](https://ronesans.com/)** — Enterprise project management platform (Construction)

## Publications

- 📄 **[Architecting for Autonomy: A Federated and Explainable AI Blueprint for UK Public Services](https://doi.org/10.1049/icp.2026.1123)**
  _IET Conference Proceedings, Vol. 2025, Issue 50, pp. 13–31_
  Presented at the International Conference on Trustworthy Digital Infrastructure 2025 (Alan Turing Institute / Royal Institution of Great Britain)
  → [IET Digital Library](https://digital-library.theiet.org/doi/10.1049/icp.2026.1123) · [IEEE Xplore](https://ieeexplore.ieee.org/document/11514733) · [DOI: 10.1049/icp.2026.1123](https://doi.org/10.1049/icp.2026.1123)

## Recognition

- 🎙️ **[Alan Turing Institute](https://youtu.be/H0jlpiNTdo8?si=tZRLqk5IW5g-bZos)** — Invited speaker at the International Conference on Trustworthy Digital Infrastructure 2025 (Royal Institution of Great Britain).
- 🏛️ **[IET](https://theiet.org)** — Member (MIET). Selected as a foundational Career Mentor.
- 📜 **UK Government (DSIT)** — Submitted expert feedback on the Code of Practice for Enterprise Connected Device Security.
- 🏅 **AWS Certified Solutions Architect — Associate**

## Research

- **MSc Artificial Intelligence** (UWE Bristol) — Thesis on Medical XAI achieving 92.42% accuracy using ResNet34, Grad-CAM, SHAP, and GPT-4.
- **Multi-Agent Systems** — UK Economic Strategy paper using LangGraph and Llama 3 for zombie company detection.
- **Sovereign AI** — Federated AI blueprint for UK public services, presented at the Alan Turing Institute.

## Connect

[![X](https://img.shields.io/badge/@berkayildi-000000?style=flat&logo=x&logoColor=white)](https://twitter.com/berkayildi)
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/berkayildi)
