<div align="center">
  <h1>THITIPONG ROONGPRASERT</h1>
  <h3>Senior Software Engineer · Distributed Backend & Systems Architect · IoT & Data Pipelines</h3>
  <p>
    Designing fault-tolerant, high-concurrency backend systems, event-driven data pipelines, and developer tooling with <b>Java, Go, Rust, TypeScript, and Python</b>.<br/>
    Focused on resilient ingestion, deterministic state, observability, and production-grade operational discipline.
  </p>

  <p>
    <a href="https://www.npmjs.com/package/mqtt-mock-sensor"><img src="https://img.shields.io/npm/v/mqtt-mock-sensor?style=for-the-badge&logo=npm&logoColor=white&label=mqtt-mock-sensor&color=CB3837" alt="NPM mqtt-mock-sensor" /></a>
    <a href="https://crates.io/crates/mqtt-sniper"><img src="https://img.shields.io/crates/v/mqtt-sniper?style=for-the-badge&logo=rust&logoColor=white&label=mqtt-sniper&color=DEA584" alt="Crates.io mqtt-sniper" /></a>
    <a href="https://linkedin.com/in/thitipongroo"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
    <a href="mailto:thitipong.roo@gmail.com"><img src="https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  </p>
</div>

---

## 📦 Published Open-Source CLI Tools

I build and maintain open-source developer tools published on **NPM**, **Crates.io**, and **GitHub Container Registry (GHCR)** to accelerate IoT data pipeline development, chaos testing, and high-concurrency broker benchmarking.

| Package | Ecosystem | Key Capabilities | Quick Run |
| :--- | :--- | :--- | :--- |
| **[mqtt-mock-sensor](https://github.com/thitipongroo/mqtt-mock-sensor)** | ![NPM](https://img.shields.io/npm/v/mqtt-mock-sensor?style=flat-square&logo=npm&color=CB3837) ![Downloads](https://img.shields.io/npm/dt/mqtt-mock-sensor?style=flat-square&color=28a745) ![CI](https://img.shields.io/github/actions/workflow/status/thitipongroo/mqtt-mock-sensor/ci.yml?style=flat-square&logo=githubactions) | Zero-config IoT telemetry simulator supporting **Multi-Tenant Schema v2**, **Bi-directional Device Shadow sync**, **Chaos Engineering** (`--chaos-jitter`, `--chaos-disconnect`), **Anomaly/DLQ injection**, and **Enterprise mTLS**. Published with SLSA OIDC provenance. | `npx mqtt-mock-sensor --preset sentinel-industrial --anomaly-rate 10` |
| **[mqtt-sniper](https://github.com/thitipongroo/mqtt-sniper)** | ![Crates.io](https://img.shields.io/crates/v/mqtt-sniper?style=flat-square&logo=rust&color=DEA584) ![Downloads](https://img.shields.io/crates/d/mqtt-sniper?style=flat-square&color=28a745) ![CI](https://img.shields.io/github/actions/workflow/status/thitipongroo/mqtt-sniper/ci.yml?style=flat-square&logo=githubactions) | High-concurrency MQTT load-testing CLI built with **Rust & Tokio**. Spawns thousands of async clients with near-zero memory overhead, **HDR Latency Histograms** (`p50`/`p95`/`p99`), Pub/Sub fan-out & soak testing, **mTLS**, and JSON CI reporting. | `cargo install mqtt-sniper` or `docker run --rm ghcr.io/thitipongroo/mqtt-sniper:latest` |

---

## 💼 Commercial Production Impact

*Selected architectures delivered under commercial engagements (proprietary source code — happy to walk through system design and trade-offs in detail):*

- **High-Throughput Real-Time Analytics Platform (`10M+ req/day`):** Engineered a Redis caching layer that reduced API response latencies to **sub-100ms**, paired with **Apache Kafka** event ingestion to decouple write-heavy telemetry streams from analytical read queries during traffic spikes.
- **Distributed Real-Time Chat Infrastructure:** Designed horizontal WebSocket gateways backed by **Redis Pub/Sub fan-out**, ensuring deterministic message delivery across stateless nodes without sticky-session bottlenecks.
- **Fault-Tolerant Notification Pipeline:** Built an event-driven multi-channel delivery engine utilizing **Kafka retry/exponential backoff**, Dead-Letter Queues (DLQ), and idempotent consumer guarantees.

---

## 🏗️ Featured Systems & Reference Architectures

### ⚡ [SENTINEL-IoT-PLATFORM](https://github.com/thitipongroo/sentinel-iot-platform) · `Java` `Spring Boot` `Kafka` `PostgreSQL` `Redis` `Next.js`

**Production-grade Industrial IoT Monitoring, Alerting & Device Twin Platform**

- **Verified Load Performance:** Cache read path sustains **1,000 req/s (60,000+ ops/min)** at **p95 112ms / p99 187ms** under k6 load testing.
- **Resilience & Self-Healing:** Mosquitto MQTT ingestion via Spring Integration with automated schema validation, **DLQ routing** (`factory/telemetry/dlq`), **Resilience4j circuit breakers**, and an automated **Redis replay queue** that buffers writes during DB outages and drains upon recovery.
- **Enterprise Data & Observability:** Monthly range-partitioned PostgreSQL tables, **CloudNativePG HA + Barman WAL archiving**, **Confluent Schema Registry (Avro)**, distributed rate limiting (**Bucket4j Redis**), and full **OpenTelemetry + Jaeger + Prometheus/Grafana** tracing.

### 🏢 [CONSTRUCTION-OS](https://github.com/thitipongroo/construction-os) · `NestJS` `Go` `Python` `Next.js` `React Native` `Kafka`

**AI-Native Enterprise Construction Operating System (Polyglot Modular Monolith)**

- **Pragmatic Architecture (68+ ADRs):** Structured as a **NestJS Modular Monolith** behind Kong API Gateway, extracting separate microservices strictly at language/throughput boundaries (**Go** high-throughput ingestion workers, **Python FastAPI** AI/OCR/BIM pipelines, and **Temporal** workflow orchestration).
- **Multi-Tenant Security & Financial Precision:** Enforces tenant isolation via **PostgreSQL Row-Level Security (RLS)**, Keycloak OIDC (`RS256` JWT), W3C DID/VC verifiable credentials, and strict monetary arithmetic (`DECIMAL(19,4)` with custom lint rules banning floating-point types).
- **Offline-First Field Operations:** React Native mobile client built on **Drizzle ORM + expo-sqlite** with a deterministic sync queue reconciling field mutations through Kafka when connectivity is restored.

### 📊 [OMNI-TRACKER](https://github.com/thitipongroo/omni-tracker) · `Go (Fiber)` `FastAPI` `Playwright` `InfluxDB` `Redis`

**Distributed E-Commerce Market Intelligence & AI Analysis Platform**

- **Polyglot Microservices:** Treats stealth **Playwright** scraper workers as distributed sensors consuming jobs from Redis queues (with queue-poisoning protection) and ingesting price time-series into **Go Fiber** and **InfluxDB**.
- **Agentic Market Insights:** Combines historical volatility metrics from InfluxDB with live news aggregation in a **Python + Google Gemini AI** service to push interactive `BUY/WAIT/SELL` Flex Message alerts via LINE Messaging API.

### 🧪 Quality Engineering & Embedded Foundations

- **[Cypress Cinema E2E Suite](https://github.com/thitipongroo/cypress-cinema-test):** Automated E2E testing framework built on Page Object Model (POM), fixture-driven test data, and CI-generated Mochawesome HTML reports.
- **[LINE Bot REST API](https://github.com/thitipongroo/line-bot-api):** Java Spring Boot webhook & messaging service integrated with LINE Messaging API.
- **[Embedded & IoT Hardware](https://github.com/thitipongroo/remote-vote-firebase):** Low-level microcontroller firmware in **C/C++** ([Remote Vote Firebase](https://github.com/thitipongroo/remote-vote-firebase), [Smart Window Automation](https://github.com/thitipongroo/smart-window)) bridging hardware sensors with cloud functions.

---

## 🛠️ Technical Skills & Ecosystem

**Languages & Core Runtimes**<br/>
![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C%2FC%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)

**Backend Frameworks & APIs**<br/>
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Go Fiber](https://img.shields.io/badge/Go_Fiber-00ADD8?style=flat-square&logo=go&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Tokio](https://img.shields.io/badge/Tokio_Async-000000?style=flat-square&logo=rust&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**Data Stores, Messaging & Event Streaming**<br/>
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT_/_Mosquitto-3C5280?style=flat-square&logo=eclipsemosquitto&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_16-316192?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis_7-DC382D?style=flat-square&logo=redis&logoColor=white)
![InfluxDB](https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white)
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=flat-square&logo=clickhouse&logoColor=black)

**DevOps, Observability & Quality Engineering**<br/>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry_/_Jaeger-000000?style=flat-square&logo=opentelemetry&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus_/_Grafana-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Cypress](https://img.shields.io/badge/Cypress-17202C?style=flat-square&logo=cypress&logoColor=white)
![k6](https://img.shields.io/badge/k6_Load_Testing-7D64FF?style=flat-square&logo=k6&logoColor=white)

---

## 🏆 Certifications & Security Training

- **Cybersecurity & AppSec:** Google Cybersecurity Professional • Secure Coding: OWASP Top 10 • Secure Coding on Frontend
- **AI Engineering:** Prompt Engineering & Agentic AI
