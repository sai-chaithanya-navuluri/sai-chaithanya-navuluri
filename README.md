# Hi, I'm Sai Chaithanya Navuluri 👋

**Senior Full Stack Java Engineer** · 9+ years · **AWS Certified Developer – Associate**

I build scalable enterprise applications across financial, healthcare, and retail domains — and lately, production-grade AI platforms. My core is backend engineering (Java, Spring Boot, microservices, AWS), and I bring that same rigor — testing, observability, clean architecture, documented decisions — to LLM systems.

📍 Atlanta, GA · 📫 chaithanyasc208@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/chaithanya-n-775a96174/)

---

### 🛠️ What I work with

**Backend:** Java (8/11/21), Spring Boot, Spring Cloud, Microservices, REST, GraphQL, Kafka, RabbitMQ
**Cloud & DevOps:** AWS (Lambda, ECS, API Gateway, S3, DynamoDB, Step Functions), Terraform, Docker, Kubernetes, GitHub Actions, Jenkins
**Data:** PostgreSQL, Oracle, Snowflake, MongoDB, DynamoDB, SQLAlchemy
**Frontend:** React, TypeScript, Angular, Tailwind
**AI Platform:** LLM abstractions (Claude/OpenAI/Gemini), RAG, MCP, FastAPI, prompt evaluation & benchmarking, LLM-as-a-judge, observability

---

### 🚀 Featured project — AI Content Platform

A production-grade, six-repository AI platform that applies backend engineering discipline to LLM systems. Not a script — a real platform with a versioned core, a service layer, persistence, evaluation, and observability.

- **[content-core](https://github.com/moneymadeclear52-design/content-core)** — the platform kernel: provider-agnostic **LLM abstraction** (Claude/OpenAI/Gemini), a step-based **workflow engine**, **RAG** retrieval, a multi-agent orchestrator, an **MCP server**, a **FastAPI** REST layer, **SQLAlchemy/Alembic** persistence, **LLM cost/latency telemetry**, an **evaluation framework** (rule-based + LLM-as-a-judge, benchmarking, A/B experiments), and a **closed-loop feedback** system. 53 tests · 10 ADRs.
- **[platform-dashboard](https://github.com/moneymadeclear52-design/platform-dashboard)** — a React + TypeScript + Tailwind operations console (run history, cost/latency trends, model benchmarks, approval queue).
- Four content-automation **pipelines** (Python + Node.js) built on the shared core.

Highlights: zero secrets in source (with CI secret-scanning gates), Docker Compose deployment, and every significant architecture choice — including the deliberate *declines* (no Celery, no LangGraph, no LiteLLM) — documented as ADRs.

---

### 📌 Start here
[content-core](https://github.com/moneymadeclear52-design/content-core) → the flagship · [platform-dashboard](https://github.com/moneymadeclear52-design/platform-dashboard) → the UI

<sub>Open to Senior Software Engineer / Full Stack / AI Platform Engineering roles.</sub>
