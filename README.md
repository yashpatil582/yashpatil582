<div align="center">

# Yash Patil

**AI/ML engineer building agentic copilots, production RAG — and the evals that keep them honest.**

<p>
  <a href="https://yashpatil582githubio.vercel.app"><img src="https://img.shields.io/badge/Portfolio-live_AI_demos-6366F1?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/yashpatil23/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:yashpatil582@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

</div>

I work on LLM systems end to end — from rebuilding transformer architectures in raw PyTorch to shipping agents with deterministic safety rails. The through-line: **I don't publish an AI claim I can't verify in code.** Every project below ships its own evaluation harness.

Currently AI/ML Engineer at **TipTop Technologies** (LLM + RAG agents for healthcare workflows on LangGraph/EKS). M.S. Computer Science, Santa Clara University '25.

## Spotlight

| Project | What it is | Proof |
|---|---|---|
| **[llm-anatomy](https://github.com/yashpatil582/llm-anatomy)** | Qwen2.5, Llama-3.2, Gemma-2 & Mistral rebuilt from scratch in pure PyTorch — one readable file per model, no `transformers` in the model path | Logit parity vs HF verified by a falsifiable harness with a negative control (bit-identical for Qwen & Llama); 10.5 GB fp32 models verify on an 8 GB laptop via mmap |
| **[clineval](https://github.com/yashpatil582/clineval)** | Claim-level hallucination, failure-mode & demographic-equity evaluation for LLM-generated medical notes | Hand-validated LLM judge, bootstrap confidence intervals, [live dashboard](https://dashboard-three-kappa-58.vercel.app) |
| **[llm-efficiency-bench](https://github.com/yashpatil582/llm-efficiency-bench)** | Token-efficiency benchmark that pairs cost with reliability — a cheap-but-flaky model can't top it — plus TokenLint, a static linter for prompt-cache waste | Sourced provider pricing with cache-write surcharge & break-even math; [live leaderboard](https://llm-efficiency-bench.vercel.app); 79 offline tests |
| **[open-scribe](https://github.com/yashpatil582/open-scribe)** | FHIR-native medical scribe baseline: encounter audio → SOAP note → ICD-10/CPT → FHIR R4B Bundle | Token-F1 evals on PriMock57 with per-example scores committed |
| **[voice-triage](https://github.com/yashpatil582/voice-triage)** | Voice-first clinical intake agent (Whisper + Llama 3.3) with red-flag triage | Deterministic regex failsafe that escalates even if the LLM call fails; persona-based eval suite; [live demo](https://voice-triage.vercel.app) |
| **[autolabel](https://github.com/yashpatil582/autolabel)** | Self-improving weak supervision: an LLM writes labeling functions, an AST sandbox validates them, a ratchet keeps only what improves held-out F1 | Snorkel-style label model over auto-generated LFs, built to run on free-tier 8B models |

More: [circuit-extract](https://github.com/yashpatil582/circuit-extract) (circuit diagrams → component graphs), [court-notice-gateway](https://github.com/yashpatil582/court-notice-gateway) (court-notice ingestion with a deterministic phishing gate before any LLM call), [matterpilot](https://github.com/yashpatil582/matterpilot) (legal AI matter platform), [agent-skills](https://github.com/yashpatil582/agent-skills) (eval methods packaged as reusable Claude Agent Skills), [healthcare-fde](https://github.com/yashpatil582/healthcare-fde) (dbt + DuckDB data-quality pipeline).

## How I build

- **Evals as an engineering discipline.** Parity harnesses with negative controls, hand-audited judges, committed per-example scores — if it can't be falsified, it doesn't ship.
- **Internals, not just APIs.** From-scratch reimplementations with KV-cache streaming and low-memory tricks prove depth below the API layer.
- **Agents with deterministic safety rails.** Every agent has a non-LLM failsafe: regex escalation gates, AST sandboxes for model-written code, phishing checks before extraction.
- **One coherent healthcare vertical.** Scribe → note evaluation → patient intake → the messy-data layer underneath.

## Stack

`PyTorch` `Python` `TypeScript` `Next.js` `FastAPI` `LangGraph / LangChain` `pgvector / FAISS` `MCP` `dbt` `DuckDB` `PostgreSQL` `Redis` `Docker` `Kubernetes / EKS` `AWS Bedrock` `GCP` `Airflow` `Groq` `Whisper`

<div align="center">

<img width="60%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=yashpatil582&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=6366F1&text_color=FFFFFF&langs_count=8" />

*Open to conversations about LLM evaluation, agent infrastructure, and healthcare AI.*

</div>
