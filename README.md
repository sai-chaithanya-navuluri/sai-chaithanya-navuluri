# Sai Chaithanya Navuluri

Senior Java Backend Engineer with 9+ years building enterprise backend systems.

This GitHub showcases my recent independent work in AI platform engineering, applying the same software architecture and engineering principles used throughout my professional Java career.

[LinkedIn](https://www.linkedin.com/in/chaithanya-n-775a96174/) · chaithanyasc208@gmail.com

---

My professional experience is centered on enterprise Java Full Stack development.

The repositories here focus on independent engineering work completed over the past year, where I explored modern AI platform engineering while applying the same architectural principles I use in enterprise systems—modularity, abstraction, reliability, observability, workflow orchestration, and maintainability.

---

## The platform in these repositories

Built independently outside of work to explore modern AI platform engineering 
while applying enterprise backend engineering principles developed through 
9+ years of Java experience: layered architecture, provider abstraction 
behind a stable interface, versioned persistence, typed retry at integration
boundaries, instrumentation at a single choke point, 53 tests, 
and 11 documented architecture decisions.

The implementation language is Python because the LLM tooling ecosystem lives
there — [documented as ADR-0011](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/adr/0011-python-over-java.md).
The architectural patterns are the ones I apply in enterprise Java, and the
mapping is set out explicitly in
[Engineering Principles](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ENGINEERING_PRINCIPLES.md).

**[content-core](https://github.com/sai-chaithanya-navuluri/content-core)** — the platform kernel:

- Provider-neutral generation across Anthropic, OpenAI, and Google, with typed retry and per-call cost telemetry
- Step-sequenced workflow engine with per-stage retry policy and graceful degradation
- Retrieval-Augmented Generation (RAG) using semantic retrieval with a reusable content-addressed index cache
- Role-specialised agent orchestration with a bounded revision loop
- Evaluation framework: rule-based scorers, model-as-judge, versioned prompt registry, cross-provider benchmarking, A/B prompt experiments
- Closed-loop feedback correlating content performance with features
- FastAPI service layer, SQLAlchemy/Alembic persistence, MCP server

**[platform-dashboard](https://github.com/sai-chaithanya-navuluri/platform-dashboard)** — React and TypeScript operations console: run history, cost and latency trends, benchmark comparison, review queue.

Four consuming pipelines (three Python, one Node.js) build on the shared kernel.

### Platform Highlights

- Multi-provider LLM architecture (Anthropic, OpenAI, Google)
- Retrieval-Augmented Generation (RAG)
- Semantic Search
- Workflow Engine
- Agent Orchestration
- MCP Server
- Prompt Registry
- Evaluation Framework
- Human-in-the-loop Approval
- Cost & Latency Observability
- FastAPI
- SQLAlchemy
- React + TypeScript Dashboard
- Docker Compose
- GitHub Actions


**Documentation:**
[Architecture](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ARCHITECTURE.md) ·
[Engineering Principles](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ENGINEERING_PRINCIPLES.md) ·
[Scalability](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/SCALABILITY.md) ·
[Performance](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/PERFORMANCE.md) ·
[Testing](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/TESTING.md) ·
[Decision records](https://github.com/sai-chaithanya-navuluri/content-core/tree/main/docs/adr)

Architecture Decision Records (ADRs) document the reasoning behind major technical decisions, 
alternatives considered, and the tradeoffs accepted during the platform's evolution. Several
document technologies deliberately **not** adopted — distributed task queues,
graph-based agent frameworks, multi-provider routing libraries, hosted vector
stores, container orchestration — each with the conditions under which that
decision would reverse.

---

<sub>Architecture

Engineering Principles

Scalability

Performance

Testing

ADRs</sub>
