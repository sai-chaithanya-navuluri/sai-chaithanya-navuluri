# Sai Chaithanya Navuluri

Senior Java Backend Engineer with 9+ years building enterprise backend systems.

This GitHub contains my recent independent work in AI platform engineering, applying the same software architecture and engineering principles used throughout my professional Java career.

[LinkedIn](https://www.linkedin.com/in/chaithanya-n-775a96174/) · chaithanyasc208@gmail.com

---

## About Sentinel — Incident Intelligence Platform

A production-grade incident-management system, built end to end: Java 21, Spring Boot, PostgreSQL with pgvector, Kafka (KRaft mode), local ONNX embeddings via Deep Java Library, and a React/TypeScript operations dashboard. 34 automated tests (Testcontainers-backed), CI with a secret-scanning gate, and full Docker Compose deployment.

Sentinel recognizes recurring production incidents — even when the wording differs — using text similarity backed by measured evidence for exactly where and why semantic embeddings were added on top of it. It surfaces what resolved a problem last time, automatically flags chronic issues that need a permanent fix rather than another patch, and optionally grounds an LLM suggestion strictly in retrieved historical data — refusing to speculate when the evidence doesn't support a conclusion, and fully functional at zero cost with that feature disabled.

sentinel → — start with the README for the full architecture and the documented design decisions, including the ones where a popular tool (ZooKeeper, a @ManyToOne relationship, an unrestricted lifecycle transition) was deliberately not used, and why.

---

## About AI Content Platform

The repositories in this profile together form an AI automation platform built independently over the past year to explore modern AI platform engineering while applying the same architectural principles used throughout my enterprise Java career.

The platform emphasizes modular architecture, provider abstraction, workflow orchestration, versioned persistence, typed retry policies, observability, and long-term maintainability. It currently includes 53 automated tests and 11 Architecture Decision Records (ADRs).

Python was chosen deliberately because the modern LLM ecosystem (frameworks, SDKs, and tooling) is significantly more mature than the JVM ecosystem. The architecture, engineering patterns, and system design intentionally mirror the enterprise Java systems I build professionally. The rationale is [documented in ADR-0011](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/adr/0011-python-over-java.md).

### [Content-Core](https://github.com/sai-chaithanya-navuluri/content-core):

The platform is organized around a shared core consumed by multiple independent pipelines, allowing reusable engineering capabilities to evolve independently of individual automation workflows.

- Provider-neutral generation across Anthropic, OpenAI, and Google, with typed retry and per-call cost telemetry
- Step-sequenced workflow engine with per-stage retry policy and graceful degradation
- Retrieval-Augmented Generation (RAG) using semantic retrieval with a reusable content-addressed index cache
- Role-specialised agent orchestration with a bounded revision loop
- Evaluation framework: rule-based scorers, model-as-judge, versioned prompt registry, cross-provider benchmarking, A/B prompt experiments
- Closed-loop feedback correlating content performance with features
- FastAPI service layer, SQLAlchemy/Alembic persistence, MCP server

### [Platform-Dashboard](https://github.com/sai-chaithanya-navuluri/platform-dashboard):

React and TypeScript operations console: run history, cost and latency trends, benchmark comparison, review queue.

The shared platform is consumed by four independent automation pipelines (three Python, one Node.js), demonstrating reusable platform architecture instead of duplicated implementations.

---

## Key Platform Capabilities

- Multi-provider LLM architecture (Anthropic, OpenAI, Google)
- Retrieval-Augmented Generation (RAG) with Semantic Search
- Workflow Engine & Agent Orchestration
- MCP Server
- Prompt Registry & Evaluation Framework
- Human-in-the-loop approval workflow
- Cost & latency observability
- FastAPI + SQLAlchemy backend
- React + TypeScript operations dashboard
- Docker Compose
- GitHub Actions CI

---

## Documentation

The platform includes detailed engineering documentation covering its architecture, design decisions, scalability, testing strategy, and operational characteristics.

- 🏗️ [**Architecture**](https://github.com/sai-chaithanya-navuluri/content-core/blob/master/docs/ARCHITECTURE.md) — Overall platform architecture, request flow, and component interactions.
- ⚙️ [**Engineering Principles**](https://github.com/sai-chaithanya-navuluri/content-core/blob/master/docs/ENGINEERING_PRINCIPLES.md) — Enterprise engineering patterns and their application throughout the platform.
- 📈 [**Scalability**](https://github.com/sai-chaithanya-navuluri/content-core/blob/master/docs/SCALABILITY.md) — Scaling strategy, bottlenecks, worker model, and future evolution.
- 🚀 [**Performance**](https://github.com/sai-chaithanya-navuluri/content-core/blob/master/docs/PERFORMANCE.md) — Performance characteristics, optimization techniques, and engineering tradeoffs.
- ✅ [**Testing**](https://github.com/sai-chaithanya-navuluri/content-core/blob/master/docs/TESTING.md) — Testing philosophy, workflow validation, and CI strategy.
- 📖 [**Architecture Decision Records (ADRs)**](https://github.com/sai-chaithanya-navuluri/content-core/tree/master/docs/adr) — Major technical decisions, alternatives considered, tradeoffs, and architectural evolution.

---
