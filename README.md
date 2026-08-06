# Sai Chaithanya Navuluri

Senior Java Backend Engineer with 9+ years building enterprise backend systems.

This GitHub showcases my recent independent work in AI platform engineering, applying the same software architecture and engineering principles used throughout my professional Java career.

[LinkedIn](https://www.linkedin.com/in/chaithanya-n-775a96174/) · chaithanyasc208@gmail.com

---

## About the Platform

The repositories in this organization represent an AI automation platform built independently over the past year to explore modern AI platform engineering while applying the same architectural principles used throughout my enterprise Java career.

The platform emphasizes modular architecture, provider abstraction, workflow orchestration, versioned persistence, typed retry policies, observability, and long-term maintainability. It currently includes 53 automated tests and 11 Architecture Decision Records (ADRs).

---

## The platform in these repositories

Built independently outside of work to explore modern AI platform engineering 
while applying enterprise backend engineering principles developed through 
9+ years of Java experience: layered architecture, provider abstraction 
behind a stable interface, versioned persistence, typed retry at integration
boundaries, instrumentation at a single choke point, 53 tests, 
and 11 documented architecture decisions.

Python was chosen deliberately because the modern LLM ecosystem (frameworks, SDKs, and tooling) is significantly more mature than the JVM ecosystem. The architecture, engineering patterns, and system design intentionally mirror the enterprise Java systems I build professionally. The rationale is documented in ADR-0011.[documented as ADR-0011](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/adr/0011-python-over-java.md).
[Engineering Principles](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ENGINEERING_PRINCIPLES.md).

**[content-core](https://github.com/sai-chaithanya-navuluri/content-core)** — the platform kernel:
The platform is organized around a shared core consumed by multiple independent pipelines, allowing reusable engineering capabilities to evolve independently of individual automation workflows.

- Provider-neutral generation across Anthropic, OpenAI, and Google, with typed retry and per-call cost telemetry
- Step-sequenced workflow engine with per-stage retry policy and graceful degradation
- Retrieval-Augmented Generation (RAG) using semantic retrieval with a reusable content-addressed index cache
- Role-specialised agent orchestration with a bounded revision loop
- Evaluation framework: rule-based scorers, model-as-judge, versioned prompt registry, cross-provider benchmarking, A/B prompt experiments
- Closed-loop feedback correlating content performance with features
- FastAPI service layer, SQLAlchemy/Alembic persistence, MCP server

**[platform-dashboard](https://github.com/sai-chaithanya-navuluri/platform-dashboard)** — React and TypeScript operations console: run history, cost and latency trends, benchmark comparison, review queue.

Four consuming pipelines (three Python, one Node.js) build on the shared kernel.

---

## Platform Highlights

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
[Architecture](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ARCHITECTURE.md) ·
[Engineering Principles](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ENGINEERING_PRINCIPLES.md) ·
[Scalability](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/SCALABILITY.md) ·
[Performance](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/PERFORMANCE.md) ·
[Testing](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/TESTING.md) ·
[Decision records](https://github.com/sai-chaithanya-navuluri/content-core/tree/main/docs/adr)

The platform is accompanied by Architecture Decision Records (ADRs) documenting major technical decisions, tradeoffs, rejected alternatives, and the conditions under which those decisions would be revisited.

---

<sub>
Architecture

Engineering Principles

Scalability

Performance

Testing

ADRs
</sub>
