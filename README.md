<div align="center">
  <h1>Hi there 👋, I'm Thitipong Roongprasert</h1>
  <h3>Software Engineer | Backend Architect | Data Pipelines | IoT</h3>
  <p>I build resilient, high-concurrency backend systems and data pipelines, primarily working with <b>Java, Go, Python, and Node.js</b>. My focus is on fault-tolerant architecture, event-driven design, and strict operational discipline.</p>
  
  <!-- GitHub Stats -->
  <p>
    <img src="https://github-readme-stats.vercel.app/api?username=thitipongroo&show_icons=true&theme=transparent&hide_border=true&title_color=00ADD8&text_color=777777" alt="GitHub Stats" width="45%"/>
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=thitipongroo&layout=compact&theme=transparent&hide_border=true&title_color=00ADD8&text_color=777777" alt="Top Languages" width="45%"/>
  </p>
</div>

---

## 🛠️ Tech Stack

**Backend & Architecture**<br>
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)

**Data & Event Streaming**<br>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![InfluxDB](https://img.shields.io/badge/InfluxDB-22ADF6?style=flat&logo=influxdb&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)

**DevOps & Infrastructure**<br>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)

**Observability & Testing**<br>
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat&logo=opentelemetry&logoColor=white)
![Cypress](https://img.shields.io/badge/Cypress-17202C?style=flat&logo=cypress&logoColor=white)

---

## 💼 Production Work

The systems below were built under commercial engagements, so the source is proprietary. Happy to walk through the architecture and trade-offs in conversation.

- **Real-time analytics platform:** Sustains 10M+ requests/day. Redis caching layer brought API responses under 100ms; Kafka-based ingestion decoupled the write path from reporting reads so traffic spikes stopped degrading dashboard performance. 
- **Distributed chat service:** WebSocket & Pub/Sub fan-out keeps message delivery consistent across nodes instead of pinning users to a single server.
- **High-throughput notification pipeline:** Event-driven delivery with Kafka retry/backoff, dead-letter handling, and idempotent sends.

---

## 🚀 Projects

### [Construction OS](https://github.com/thitipongroo/cos) · `NestJS, React Native, Python, Go`
AI-native construction management platform built for enterprise scale. 
- **Modular monolith over microservices:** One deployable holding all domain modules, with separate services only where throughput boundary justifies it (e.g., Python/FastAPI for LLM gateway, Go for analytics/IoT).
- **Offline-first clients:** Drizzle over expo-sqlite with a sync queue on React Native, reconciling through Kafka; built for sites with no signal.
- **Monetary correctness:** Strict database enforcement (`DECIMAL(19,4)`) and float banning via lint rules.

### [Omni-Tracker](https://github.com/thitipongroo/omni-tracker) · `Go, InfluxDB, Playwright, Docker` 🌟
A distributed, high-concurrency market intelligence platform. 
- Treats web scrapers as "IoT sensors" to ingest massive e-commerce data into a Golang Fiber API.
- Stores time-series trends in InfluxDB with real-time LINE Bot alerts.
- Fully containerized via Docker Compose with GitHub Actions CI/CD pipeline.

### [Sentinel IoT Platform](https://github.com/thitipongroo/sentinel-iot) · `Java 21, Spring Boot 3.2, Kafka, Kubernetes`
Industrial IoT monitoring platform - MQTT sensor ingestion, threshold alerting, and a full observability stack.
- **Ingestion & Resilience:** Mosquitto MQTT via Spring Integration, with DLQ routing. Resilience4j circuit breaker and fallback to Redis queue during database downtime.
- **Performance:** Sustains 1,000 req/s (60k+ ops/min) at p95 112 ms under k6 load test.

### [MQTT Mock Sensor](https://github.com/thitipongroo/mqtt-mock-sensor) · `Node.js, MQTT` 📦
A zero-config CLI tool published on NPM to generate and publish mock IoT sensor data. Built to help frontend and backend engineers test their IoT dashboards without physical hardware.
[![NPM Version](https://img.shields.io/npm/v/mqtt-mock-sensor?style=flat&color=CB3837&logo=npm)](https://www.npmjs.com/package/mqtt-mock-sensor)

### [Cypress Cinema Automation](https://github.com/thitipongroo/cypress-cinema-test) · `Cypress 13`
E2E suite for a cinema booking platform using Page Object Model, JSON Fixture-driven test data, and Mochawesome HTML reports generated in CI.

### [Embedded & Automation]
- **[LINE Bot API](https://github.com/thitipongroo/line-bot-api):** RESTful service integrated with LINE Messaging API (Java/Spring Boot).
- **[Remote Vote](https://github.com/thitipongroo/remote-vote-firebase):** Secure remote voting system with live result updates (Firebase/C).
- **[Smart Window](https://github.com/thitipongroo/smart-window):** IoT automation that reads environmental sensor data (C++).

---

## 🏆 Certifications
Google Cybersecurity • Prompt Engineering & Agentic AI • Secure Coding: OWASP Top 10 • Secure Coding on Frontend
