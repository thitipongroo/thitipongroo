# THITIPONG ROONGPRASERT

**Backend Engineer — Java/Spring Boot & Node.js** · Bangkok, Thailand

I build backend services for production traffic. Most recently a real-time analytics platform sustaining 10M+ requests/day at sub-100ms response times, built on Kafka and Redis. Two platforms I'm building at **One Inspector and Consultant**, my own consultancy: **[Sentinel IoT Platform](https://github.com/thitipongroo/sentinel-iot)**, an industrial monitoring system in Java 21 / Spring Boot with MQTT ingestion, circuit-breaker resilience and GitOps deployment to EKS; and **[Construction OS](https://github.com/thitipongroo/cos)**, an AI-native construction management platform currently in development.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thitipongroo/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:thitipong.roo@gmail.com)

---

## Tech Stack

**Languages**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat&logo=cplusplus&logoColor=white)

**Backend**

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring-boot&logoColor=white)
![Spring](https://img.shields.io/badge/Spring_MVC-6DB33F?style=flat&logo=spring&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)

**Data & Messaging**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=flat&logo=clickhouse&logoColor=black)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat&logo=neo4j&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)

**Infrastructure & CI**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat&logo=helm&logoColor=white)
![ArgoCD](https://img.shields.io/badge/Argo_CD-EF7B4D?style=flat&logo=argo&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)

**Observability**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat&logo=opentelemetry&logoColor=white)
![Jaeger](https://img.shields.io/badge/Jaeger-60D0E4?style=flat&logo=jaeger&logoColor=black)

**Frontend & Testing**

![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![JUnit](https://img.shields.io/badge/JUnit5-25A162?style=flat&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-291A3F?style=flat&logo=testcontainers&logoColor=white)
![Cypress](https://img.shields.io/badge/Cypress-17202C?style=flat&logo=cypress&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat&logo=k6&logoColor=white)

---

## Production Work

The systems below were built under commercial engagements, so the source is proprietary and not published here. Happy to walk through the architecture and trade-offs in conversation.

**Real-time analytics platform** — Kafka, Redis, Docker
Sustains 10M+ requests/day. Redis caching layer brought API responses under 100ms; Kafka-based ingestion decoupled the write path from reporting reads so traffic spikes stopped degrading dashboard performance. Collapsed client reporting from a multi-hour batch job into on-demand results.

**Distributed chat service** — WebSocket, Pub/Sub
Pub/sub fan-out keeps message delivery consistent across nodes instead of pinning users to a single server.

**High-throughput notification pipeline** — Kafka
Event-driven delivery with retry/backoff, dead-letter handling, and idempotent sends.

---

## Projects

### [Construction OS](https://github.com/thitipongroo/cos) · NestJS, Next.js, React Native, Python, Go `🚧 In development`

AI-native construction management platform built for enterprise scale. Currently at Stage 1 (BUILD) — architecture and specs are settled, implementation is underway.

- **Modular monolith over microservices** — one NestJS deployable holding all domain modules (identity, tenant, project, BoQ, procurement, site-ops, finance, equipment, workforce), with separate services only where a language or throughput boundary justifies it: Python/FastAPI for LLM gateway, embedding, OCR and transcription; Go for analytics, knowledge-graph and MQTT IoT ingestion
- **Multi-tenancy** — shared database with `tenant_id` and PostgreSQL row-level security, chosen over schema-per-tenant and documented as an ADR
- **Offline-first clients** — Serwist PWA with IndexedDB on web, Drizzle over expo-sqlite with a sync queue on React Native, reconciling through Kafka; built for sites with no signal
- **Monetary correctness** — `DECIMAL(19,4)` in PostgreSQL, `decimal.js` and Python `decimal` in application code, floats banned by lint rule
- **Event bus** — Kafka with Avro and Schema Registry under `BACKWARD_TRANSITIVE` compatibility; Temporal for long-running workflows
- **Auth split by user reality** — phone + SMS OTP via AWS SNS for site workers, Keycloak OIDC with RS256 JWT for office staff
- **Polyglot persistence** — PostgreSQL + TimescaleDB, ClickHouse (analytics), Neo4j (knowledge graph), pgvector + OpenSearch (retrieval), MinIO (objects), Redis
- **Operational discipline** — PgBouncer in transaction mode with direct PostgreSQL connections prohibited, OpenTelemetry → Grafana/Loki/Prometheus, secrets via Vault and AWS Secrets Manager, ~60 ADRs and a 100% line/branch coverage mandate

### [Sentinel IoT Platform](https://github.com/thitipongroo/sentinel-iot) · Java 21, Spring Boot 3.2, Kafka, Kubernetes

Industrial IoT monitoring platform — MQTT sensor ingestion, threshold alerting, multi-channel notifications, live WebSocket dashboard, and a full observability stack.

**Measured:** cache read path sustains 1,000 req/s (60k+ ops/min) at p95 112 ms / p99 187 ms under k6 load test, against SLO targets of p95 < 200 ms and p99 < 500 ms.

- **Ingestion** — Mosquitto MQTT via Spring Integration, with DLQ routing for invalid payloads and unknown devices; Kafka event streaming with Avro schemas and Confluent Schema Registry
- **Resilience** — Resilience4j circuit breaker and retry; when Postgres is unavailable the dashboard stays live off Redis while writes queue to a Redis replay list, drained every 30s once the breaker recovers
- **Data** — PostgreSQL 16 with monthly range partitioning, hourly aggregates, row-level security for multi-tenancy, Flyway migrations; CloudNativePG + Barman for HA replication and WAL archiving
- **Realtime** — Spring WebSocket with Redis pub/sub fan-out across nodes
- **Observability** — Prometheus, Grafana, OpenTelemetry/Micrometer, Jaeger tracing, structured JSON logging with MDC request correlation, multi-window burn-rate SLO alerting
- **Testing** — JUnit, Mockito, Testcontainers, Pact contract tests, JMH benchmarks, Pitest mutation testing, ArchUnit, schemathesis fuzzing, k6 load tests
- **Deploy** — Docker Compose locally; EKS via Terraform and Helm, GitOps with ArgoCD, blue/green and canary rollouts with Argo Rollouts, event-driven autoscaling with KEDA, Velero backup/DR
- **Frontend** — Next.js 14 App Router, Tailwind, Recharts, react-query, Zustand, list virtualization

### [LINE Bot API](https://github.com/thitipongroo/line-bot-api) · Java, Spring Boot

RESTful service integrated with the LINE Messaging API, handling webhook events and message delivery.

### [Codebox Platform](https://github.com/thitipongroo/codebox-platform) · Node.js, Express, MongoDB `✅ Completed`

Full-stack platform for user and content management. Currently migrating the frontend from server-rendered EJS to React + Tailwind CSS.

### [Cypress Cinema Automation](https://github.com/thitipongroo/cypress-cinema-test) · Cypress 13 `📚 Portfolio project`

E2E suite for a cinema booking platform, covering language switching → cinema selection → movie selection → showtime verification → seat selection.

- Page Object Model — selectors and interactions encapsulated per page class
- Fixture-driven test data, decoupled from test logic via JSON
- Mochawesome HTML reports, generated in CI on every push and pull request
- Retry strategy for flaky network-dependent tests

### [Remote Vote](https://github.com/thitipongroo/remote-vote-firebase) · Firebase, embedded C `✅ Completed`

Secure remote voting system with live result updates, backed by a microcontroller client. Firebase Authentication, Cloud Functions, and Realtime Database.

### [Smart Window](https://github.com/thitipongroo/smart-window) · Embedded C++ `✅ Completed`

IoT automation that reads environmental sensor data and drives microcontroller-based window control logic.

---

## Certifications

Google Cybersecurity · Prompt Engineering & Agentic AI (AIS Academy) · Secure Coding: OWASP Top 10 · Secure Coding on Frontend
