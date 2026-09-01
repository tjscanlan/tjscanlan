# Hi, I'm TJ Scanlan 👋

Senior AI/ML Engineer building and evaluating LLM-powered agents in production. I live at the intersection of **AI/ML Ops** and **platform engineering** — shipping agentic features and then building the evaluation infrastructure that proves they actually work.

- 🔭 Currently building **agent & model evaluation frameworks (EvalOps)** at Entegris — versioned test suites, offline/online eval pipelines, and quality metrics for tool invocation, structured outputs, and multi-step reasoning
- 🤖 Deep in the **MCP / LLM API / ML systems** world — model training & fine-tuning, tool calling, cross-platform ML/agent builders, vector search
- ⚙️ Background in **cybersecurity data engineering** — ETL pipelines, SQL data models, and containerized services that fed ML pipelines long before I was building and evaluating the models themselves
- 🎓 B.S. in Mathematics, Minor in Data Science — Merrimack College
- 📍 Based in the Boston area (Medford, MA)
- 📫 Reach me at tjpscanlan.44@gmail.com or [LinkedIn](https://linkedin.com/in/tj-scanlan)

---

## 🧠 What I care about

I think the hard part of agentic AI isn't getting a demo to work once — it's **knowing whether it's still working** after the 50th change to a prompt, tool, or model version. That's what pulls me toward AI evaluation frameworks, observability for agent systems, and the "boring" platform work (Docker, Kubernetes, Terraform, CI/CD) that makes agentic features reliable enough to trust in production.

## 🛠️ Tech Stack

- **Languages:** TypeScript, Python, Go, SQL
- **AI & Agents:** LLM API integration, MCP, tool invocation, structured outputs, multi-step reasoning, agent evaluation (EvalOps), vector search, cross-platform agent builders
- **Cloud & Infra:** GCP, AWS, Docker, Kubernetes, Terraform, Kafka, BigQuery
- **Practices:** CI/CD, observability, microservice architecture, API design (REST/gRPC), unit & integration testing, Agile

## 📌 Pinned Projects

### [mimic3-db-demo](https://github.com/tjscanlan/mimic3-db-demo)
A healthcare ML portfolio project predicting 30-day hospital readmission on the MIMIC-III Clinical Database Demo — running two parallel approaches on the same patients (gradient-boosted model on structured features vs. a fine-tuned small language model on clinical text) into a shared evaluation harness. The eval-harness-first mindset here is the same one I use at work.

### [half-staff](https://github.com/tjscanlan/half-staff)
A feature-flag / experimentation service: Go API (REST + gRPC), Postgres for flag definitions and audit logging, Redis for evaluation caching with pub/sub invalidation, plus a TypeScript SDK. The kind of platform primitive that makes it safe to roll out risky changes — including agentic ones — gradually.

### [beer-reccommender](https://github.com/tjscanlan/beer-reccommender)
A recommendation-system side project in Python — smaller in scope, but scratches the same "build a model, see if it's actually useful" itch.

### [conduit](https://github.com/tjscanlan/conduit)
A secure, runtime-safe **observability platform for AI agents** — mTLS-secured ingestion, NATS JetStream buffering, and dedicated storage for traces, metrics, and LLM payloads (ClickHouse). Built in Go with SDKs for Go and Python agents. This is basically EvalOps infrastructure applied to production agent traffic: schema-validated ingestion, per-agent rate limiting, and a query layer for digging into what an agent actually did.

---

*Currently exploring how agent evaluation practices from EvalOps translate into general MLOps discipline — always happy to talk shop about making AI systems observable, testable, and boring in the best way.*
