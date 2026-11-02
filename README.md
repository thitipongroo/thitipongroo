<div align="center">
  <h1>THITIPONG ROONGPRASERT</h1>
  <h3>Senior Systems & Distributed Backend Engineer</h3>
  <p>
    Specializing in <b>fault-tolerant telemetry ingestion, event-driven distributed systems, and high-performance developer tooling</b>.<br/>
    Core engineering in <b>Rust · Go · Java</b>, with production-grade discipline in deterministic state, observability, and system resilience.
  </p>

  <p>
    <a href="https://crates.io/crates/mqtt-sniper"><img src="https://img.shields.io/crates/v/mqtt-sniper?style=for-the-badge&logo=rust&logoColor=white&label=mqtt-sniper&color=DEA584" alt="Crates.io mqtt-sniper" /></a>
    <a href="https://www.npmjs.com/package/mqtt-mock-sensor"><img src="https://img.shields.io/npm/v/mqtt-mock-sensor?style=for-the-badge&logo=npm&logoColor=white&label=mqtt-mock-sensor&color=CB3837" alt="NPM mqtt-mock-sensor" /></a>
    <a href="https://www.pulseiot-cloud.com/"><img src="https://img.shields.io/badge/Live_SaaS-pulseiot--cloud.com-06b6d4?style=for-the-badge&logo=googlechrome&logoColor=white" alt="PulseIoT Cloud" /></a>
    <a href="https://linkedin.com/in/thitipongroo"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
    <a href="mailto:thitipong.roo@gmail.com"><img src="https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  </p>
</div>

---

## 📦 Published Open-Source Developer Tooling

Production-ready, published CLI utilities designed for high-concurrency broker stress-testing, synthetic telemetry generation, and CI/CD quality gates:

| Package & Distribution | Ecosystem & Architecture | Key Capabilities | Quick Run |
| :--- | :--- | :--- | :--- |
| **[mqtt-sniper](https://github.com/thitipongroo/mqtt-sniper)**<br/>[![Crates.io](https://img.shields.io/crates/v/mqtt-sniper?style=flat-square&logo=rust&color=DEA584)](https://crates.io/crates/mqtt-sniper) [![CI](https://img.shields.io/github/actions/workflow/status/thitipongroo/mqtt-sniper/ci.yml?style=flat-square&logo=githubactions)](https://github.com/thitipongroo/mqtt-sniper) | **Rust · Tokio Async Runtime**<br/>Engineered for bounded $O(1)$ memory per socket (~1.5–2.5 KB RAM/conn) | • High-concurrency MQTT load injector spawning thousands of asynchronous clients with near-zero overhead.<br/>• Microsecond-resolution **HDR Latency Histograms** (`p50`, `p90`, `p99`, `p99.9`).<br/>• Automated JSON regression reporting designed for CI/CD performance gates and soak tests.<br/>• Enterprise TLS/mTLS and pub/sub fan-out validation. | `cargo install mqtt-sniper`<br/>*or*<br/>`docker run --rm ghcr.io/thitipongroo/mqtt-sniper:latest` |
| **[mqtt-mock-sensor](https://github.com/thitipongroo/mqtt-mock-sensor)**<br/>[![NPM](https://img.shields.io/npm/v/mqtt-mock-sensor?style=flat-square&logo=npm&color=CB3837)](https://www.npmjs.com/package/mqtt-mock-sensor) [![CI](https://img.shields.io/github/actions/workflow/status/thitipongroo/mqtt-mock-sensor/ci.yml?style=flat-square&logo=githubactions)](https://github.com/thitipongroo/mqtt-mock-sensor) | **Node.js · TypeScript**<br/>Stream-based telemetry generator with SLSA OIDC provenance | • Zero-config synthetic IoT telemetry generator supporting **Multi-Tenant Schema v2** and dynamic waveform simulation.<br/>• **Chaos Engineering capabilities**: Injects network jitter, abnormal disconnects, payload schema anomalies, and DLQ triggers.<br/>• Bidirectional digital twin state simulation and device shadow synchronizer. | `npx mqtt-mock-sensor --preset sentinel-industrial --anomaly-rate 5` |

---

## 💼 Commercial Engineering Impact & Production Outcomes

*Representative distributed systems architectures delivered for commercial platforms (focusing on architectural patterns, reliability, and measurable outcomes under strict IP confidentiality):*

- **Low-Latency Telemetry Serving Layer (Sub-15ms p99):** Architected a write-through Redis caching cluster paired with asynchronous Kafka ingestion, decoupling write-heavy telemetry streams from analytical query loads. Slashed downstream database query pressure by over **80%** and stabilized p99 read latencies below 15ms during high-volume ingest bursts.
- **Stateless Real-Time Gateway & Pub/Sub Fan-Out:** Designed horizontally scalable WebSocket connection gateways backed by a Redis Pub/Sub messaging fabric. Eliminated sticky-session dependencies, allowing seamless rolling deployments and deterministic sub-second event broadcasts across distributed client pods.
- **Resilient Multi-Channel Notification Dispatcher:** Engineered an event-driven alert dispatcher featuring exponential backoff retries, circuit breakers, and Dead-Letter Queues (DLQ). Guaranteed idempotent delivery and exactly-once processing semantics across external webhook providers (Slack, Telegram, LINE Messaging API).

---

## 🏢 Enterprise SaaS & Production Systems

*Architecture case studies of commercial production platforms. Proprietary source code is protected under commercial licenses; system designs and architectural trade-offs are available for technical walkthrough.*

### ⚡ [PulseIoT Cloud Platform](https://www.pulseiot-cloud.com/) · `Commercial SaaS`
**Unified Industrial Telemetry Reliability, Ingestion & Device Shadow Platform**  
*Live Platform:* [www.pulseiot-cloud.com](https://www.pulseiot-cloud.com/)

- **High-Throughput Resilient Ingestion:** Ingests live industrial sensor streams via MQTT and HTTP gateways. Backed by automated schema verification, Dead-Letter Queue (DLQ) isolation, and automated circuit breakers to protect downstream ingestion pipelines from toxic payload anomalies.
- **Fail-Safe Persistence & Replay Architecture:** Employs an automated buffer replay queue that safely stages incoming telemetry streams during database maintenance windows or failover events, draining sequentially upon health recovery with zero data loss.
- **Time-Series Storage & Data Lifecycle:** Utilizes monthly range-partitioned database tables for time-series telemetry, coupled with automated rollup roll-ups and WAL archiving for point-in-time recovery.
- **Production Observability:** Instrumented end-to-end with **OpenTelemetry**, exporting distributed traces and metrics to Prometheus and Jaeger for microsecond-level latency diagnosis.

### 🏗️ [CONSTRUCTION OS](https://www.construction-os.io/) · `Enterprise Platform`
**Enterprise Operating System for Construction Supply Chain, Site Operations & Financial Workflows**  
*Live Platform:* [www.construction-os.io](https://www.construction-os.io/)

- **Modular Monolith with Language-Boundary Microservices:** Engineered a domain-isolated Modular Monolith core behind an API Gateway, strictly segregating CPU-intensive pipelines into dedicated background workers (Go ingestion workers, Python FastAPI ML/OCR pipelines) orchestrated via workflow engines.
- **Multi-Tenant Security & Isolation:** Enforces strict tenant data boundaries at the database layer via **PostgreSQL Row-Level Security (RLS)**, coupled with Keycloak OIDC (RS256 JWT validation) and enterprise role-based access control (RBAC).
- **Deterministic Offline-First Synchronization:** Engineered an offline mutation queue for field applications, reconciling asynchronous site updates, conflict resolutions, and audit trails across Kafka event streams once mobile network connectivity is restored.
- **Financial-Grade Ledger Precision:** Enforces exact currency computations using fixed-point arithmetic (`DECIMAL(19,4)` and language-level Decimal wrappers) with strict automated linting rules banning IEEE-754 floating-point operations in billing modules.

---

## 🧪 Open-Source Foundations & Quality Engineering

- **[Omni-Tracker](https://github.com/thitipongroo/omni-tracker):** Distributed market intelligence scraping framework pairing stealth Playwright workers with Go Fiber ingestion and time-series metrics storage.
- **[Cypress Cinema E2E Suite](https://github.com/thitipongroo/cypress-cinema-test):** Automated end-to-end testing framework with Page Object Model (POM) patterns, fixture-driven data sets, and CI HTML reporting.
- **[Embedded Hardware Firmware](https://github.com/thitipongroo/remote-vote-firebase):** C/C++ microcontroller firmware integrating low-power hardware sensors with cloud services via event webhooks.

---

## 🛠️ Core Technical Competencies

```
High-Concurrency Systems  │  Rust (Tokio), Go, Java 21 (Virtual Threads)
Distributed Architecture  │  Apache Kafka, MQTT (Mosquitto), Event-Driven Architecture, CQRS
Storage & In-Memory Data  │  PostgreSQL (Partitioning, RLS), Redis, TimescaleDB, ClickHouse
Infrastructure & DevOps   │  Docker, Kubernetes, GitHub Actions, OpenTelemetry, Prometheus, Grafana
Quality & Chaos Testing   │  k6, HDR Histogram Benchmarking, Jest, Playwright, Cypress
```

---

## 🏆 Certifications & Continuing Education

- **Cybersecurity & AppSec:** Google Cybersecurity Professional • Secure Coding: OWASP Top 10 • Secure Coding on Frontend
- **System Design & AI:** Prompt Engineering & Agentic Workflow Systems
