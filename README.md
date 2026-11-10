<h1>George Bonovas</h1>

<p>
Software engineer working on LLM inference and backend systems, based in Athens. Final-year CS at NKUA, writing my thesis on KV cache quantization.<br>
I work mostly on backend systems and AI tooling, and I like owning the whole thing: data layer, API, and the ops around it.
</p>

<p>
<a href="https://personal-website-g3co.vercel.app"><img src="https://img.shields.io/badge/Website-000000?style=flat-square&logo=vercel&logoColor=white" alt="Website"></a>
<a href="https://www.linkedin.com/in/george-bonovas"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:georgebonovas315@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
</p>

Open to internships and junior roles in AI engineering or backend. Remote or hybrid.

## Projects

### [minillm.cpp](https://github.com/georgebon5/minillm-cpp)
LLM inference engine written from scratch in C++20. No PyTorch, no ggml, no BLAS.

- Full transformer stack (GQA, RoPE, SwiGLU, KV cache) on hand-written NEON SIMD kernels
- Runs SmolLM2 135M to 1.7B on Apple Silicon / ARM CPUs at **10–61 tok/s**
- Loads BF16 weights straight into INT8, so the 1.7B model fits in **under 2 GB of RAM**
- Web UI with live token streaming, a per-token top-5 probability panel, and FP32 / INT8 / INT4 side by side

`C++20` `NEON` `SafeTensors` `POSIX sockets` `CMake`

### [Multi-Tenant AI RAG System](https://github.com/georgebon5/Multi-Tenant-AI-RAG-System) · [demo](https://multi-tenant-rag-api.onrender.com/app/#login)
Backend where organisations upload documents and chat with them over RAG. Each tenant's data is fully isolated, and new tenants are onboarded without touching existing ones.

- **~13k LOC, 55 endpoints, 330 tests**
- Celery + Redis for ingestion jobs, WebSocket streaming for LLM responses
- JWT auth, RBAC, Kubernetes manifests and CI/CD (clone to running in one command)

`FastAPI` `ChromaDB` `PostgreSQL` `Celery` `Redis` `Docker` `Kubernetes`

### [Political Response Clarity (SemEval 2026 Task 6)](https://github.com/georgebon5/political-response-clarity)
Three-way clarity classification of politicians' answers on the QEvasion dataset. I ran four approaches on the same split: TF-IDF / Word2Vec baselines, fine-tuned BERT / DistilBERT / DeBERTa-v3 (plain PyTorch, no Trainer), Qwen2.5-3B/7B prompting (zero-shot, few-shot, CoT), and a four-agent pipeline on a 0.5B model.

The final submission, a 6-encoder ensemble with one round of pseudo-labelling, placed **2nd on the private Kaggle leaderboard** (macro F1 0.67).

`PyTorch` `HuggingFace` `Qwen2.5` `scikit-learn`

### [MLOps Pipeline](https://github.com/georgebon5/MLOps-project)
Churn prediction on 10k bank customers, built as a full pipeline rather than a notebook. DVC for data, MLflow for experiments (gradient boosting won, ROC-AUC 0.730), FastAPI serving, Evidently AI for drift detection, GitHub Actions for CI/CD.

`MLflow` `DVC` `FastAPI` `Docker` `Evidently AI`

### [Next Jr by NBG](https://github.com/georgebon5/nbgtechbliz) · TechBiz Hackathon
🏆 **1st in the National Bank of Greece track, 3rd overall.** A youth banking app with AI features, built and pitched to NBG in under 24 hours: two codebases, GDPR compliance, Claude API integration. I did the frontend, the API design, and the pitch.

`Next.js` `TypeScript` `FastAPI` `Claude API`

<details>
<summary><b>Coursework</b></summary>
<br>

| Project | |
|---|---|
| Database Systems | C, B+ trees, file organisation, indexing |
| Operating Systems | C, processes, memory, scheduling |
| RSA | C, encryption from scratch |
| OpenGL shadow renderer | C++, shadow mapping, Phong lighting |
| Pacman | Python, search and adversarial agents |

All in [programming-projects](https://github.com/georgebon5/programming-projects).
</details>

## Stack

**Languages** &nbsp; Python, C++, C, SQL, TypeScript<br>
**ML** &nbsp; PyTorch, HuggingFace, scikit-learn, ChromaDB, Anthropic SDK, MLflow, DVC, Evidently AI<br>
**Backend** &nbsp; FastAPI, Flask, PostgreSQL, Redis, Celery, WebSockets<br>
**Frontend** &nbsp; Next.js, React<br>
**Infra** &nbsp; Docker, Kubernetes, GitHub Actions
