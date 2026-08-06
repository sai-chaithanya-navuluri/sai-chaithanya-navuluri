# Sai Chaithanya Navuluri

**Senior Java Backend Engineer** · 9+ years · AWS Certified Developer – Associate · Atlanta, GA

I build and operate enterprise backend systems in financial services — distributed
services on Java and Spring Boot, event-driven architectures on Kafka, and
cloud-native deployment on AWS. Over the past year I've extended that work into
LLM systems, designing and operating a production-grade AI platform end to end.

[LinkedIn](https://www.linkedin.com/in/chaithanya-n-775a96174/) · chaithanyasc208@gmail.com

---

## Professional background

| | |
|---|---|
| **Languages** | Java 8 / 11 / 21, SQL, PL/SQL, Python, TypeScript |
| **Backend** | Spring Boot, Spring Cloud, Spring Security, Spring Batch, Hibernate, JPA, Microservices |
| **Messaging** | Apache Kafka, RabbitMQ, JMS, ActiveMQ |
| **Data** | Oracle, PostgreSQL, MSSQL, MongoDB, DynamoDB, Snowflake |
| **Cloud & Infra** | AWS (Lambda, ECS, API Gateway, S3, SQS/SNS, Step Functions, IAM), Terraform, Docker, Kubernetes |
| **AI / LLM** | Provider abstraction (Anthropic, OpenAI, Google), RAG, agent orchestration, MCP, prompt evaluation, LLM cost telemetry |
| **Delivery** | Jenkins, GitHub Actions, Bitbucket, SonarQube, Checkmarx, JUnit, Selenium |
| **Frontend** | React, TypeScript, Angular |

**Northern Trust — Global Entitlements Hub** (asset servicing): Spring Boot
microservices and REST APIs on Java 21, migrated from Java 8. Role-based access
control integrated with enterprise IAM. Replaced nightly batch reconciliation with
event-driven synchronization on Kafka. Led a point-in-time-recovery database
migration that reduced primary database load by ~30% and cut entitlement-validation
response times by ~35% at peak.

Earlier: **Express Scripts** — decomposed monolithic claims and invoicing services
into 15+ Spring Boot microservices with Kafka event processing on Kubernetes.
**Wells Fargo** — ACH, EFT, and wire payment processing. **Macy's** — high-volume
order management.

---

## The platform in these repositories

A production-grade AI content platform, designed and built end to end. It began as
a side project and is engineered as I would a production backend service: layered
architecture, provider abstraction behind a stable interface, versioned
persistence, typed retry at integration boundaries, instrumentation at a single
choke point, 53 tests, and 11 documented architecture decisions.

The implementation language is Python because the LLM tooling ecosystem lives
there — [documented as ADR-0011](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/adr/0011-python-over-java.md).
The architectural patterns are the ones I apply in enterprise Java, and the
mapping is set out explicitly in
[Engineering Principles](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ENGINEERING_PRINCIPLES.md).

**[content-core](https://github.com/sai-chaithanya-navuluri/content-core)** — the platform kernel:

- Provider-neutral generation across Anthropic, OpenAI, and Google, with typed retry and per-call cost telemetry
- Step-sequenced workflow engine with per-stage retry policy and graceful degradation
- Semantic retrieval (RAG) with a content-addressed index cache
- Role-specialised agent orchestration with a bounded revision loop
- Evaluation framework: rule-based scorers, model-as-judge, versioned prompt registry, cross-provider benchmarking, A/B prompt experiments
- Closed-loop feedback correlating content performance with features
- FastAPI service layer, SQLAlchemy/Alembic persistence, MCP server

**[platform-dashboard](https://github.com/sai-chaithanya-navuluri/platform-dashboard)** — React and TypeScript operations console: run history, cost and latency trends, benchmark comparison, review queue.

Four consuming pipelines (three Python, one Node.js) build on the shared kernel.

**Documentation:**
[Architecture](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ARCHITECTURE.md) ·
[Engineering Principles](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/ENGINEERING_PRINCIPLES.md) ·
[Scalability](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/SCALABILITY.md) ·
[Performance](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/PERFORMANCE.md) ·
[Testing](https://github.com/sai-chaithanya-navuluri/content-core/blob/main/docs/TESTING.md) ·
[Decision records](https://github.com/sai-chaithanya-navuluri/content-core/tree/main/docs/adr)

The decision records are the most useful artifact for assessing judgment. Several
document technologies deliberately **not** adopted — distributed task queues,
graph-based agent frameworks, multi-provider routing libraries, hosted vector
stores, container orchestration — each with the conditions under which that
decision would reverse.

---

<sub>Open to Senior / Lead roles in Java backend, platform, and AI engineering.</sub>
