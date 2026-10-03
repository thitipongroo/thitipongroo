<div align="center">
  <h1>Hi there 👋, I'm THITIPONG ROONGPRASERT</h1>
  <h3>Software Engineer | Backend Architect | Data Pipelines | IoT</h3>
  <p>I build resilient, high-concurrency backend systems and data pipelines, primarily working with <b>Java, Go, Python, and Node.js</b>. My focus is on fault-tolerant architecture, event-driven design, and strict operational discipline.</p>
  
  <!-- GitHub Stats -->
  <p>
    <img src="https://github-readme-stats.vercel.app/api?username=thitipongroo&show_icons=true&theme=transparent&hide_border=true&title_color=00ADD8&text_color=777777" alt="GitHub Stats" width="45%"/>
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=thitipongroo&layout=compact&theme=transparent&hide_border=true&title_color=00ADD8&text_color=777777" alt="Top Languages" width="45%"/>
  </p>
</div>

---

## 🌟 Open-Source Project

<div align="center">
  <a href="https://github.com/thitipongroo/mqtt-mock-sensor">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=thitipongroo&repo=mqtt-mock-sensor&theme=transparent&hide_border=true&title_color=CB3837&icon_color=CB3837" alt="MQTT Mock Sensor Repo Card" width="400"/>
  </a>
  <br>
  <a href="https://www.npmjs.com/package/mqtt-mock-sensor"><img src="https://img.shields.io/npm/v/mqtt-mock-sensor?style=for-the-badge&color=CB3837&logo=npm" alt="NPM Version" /></a>
  <a href="https://www.npmjs.com/package/mqtt-mock-sensor"><img src="https://img.shields.io/npm/dt/mqtt-mock-sensor?style=for-the-badge&color=28a745" alt="NPM Downloads" /></a>
  <a href="https://github.com/thitipongroo/mqtt-mock-sensor"><img src="https://img.shields.io/github/actions/workflow/status/thitipongroo/mqtt-mock-sensor/ci.yml?style=for-the-badge&logo=githubactions" alt="CI Status" /></a>
  <br><br>
</div>

**[MQTT MOCK SENSOR](https://github.com/thitipongroo/mqtt-mock-sensor)** is a zero-config, production-grade CLI tool published on NPM to generate and stream mock IoT sensor telemetry (Env, GPS, Power) to any MQTT broker. Built to accelerate data pipeline development and E2E testing for frontend and backend engineers without needing physical hardware.

Run it globally without installation:
```bash
npx mqtt-mock-sensor --broker mqtt://test.mosquitto.org --type power
```

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

**DevOps & Infrastructure**<br>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)

---

## 💼 Production Work

The systems below were built under commercial engagements, so the source is proprietary. Happy to walk through the architecture and trade-offs in conversation.

- **Real-time analytics platform:** Sustains 10M+ requests/day. Redis caching layer brought API responses under 100ms; Kafka-based ingestion decoupled the write path from reporting reads so traffic spikes stopped degrading dashboard performance. 
- **Distributed chat service:** WebSocket & Pub/Sub fan-out keeps message delivery consistent across nodes instead of pinning users to a single server.
- **High-throughput notification pipeline:** Event-driven delivery with Kafka retry/backoff, dead-letter handling, and idempotent sends.

---

## 🚀 Enterprise Projects

### [Sentinel IoT Platform](https://github.com/thitipongroo/sentinel-iot) · `Java, Spring Boot, Kafka, Kubernetes` `🚧 In development`
Industrial IoT monitoring platform - MQTT sensor ingestion, threshold alerting, and a full observability stack.
- **Ingestion & Resilience:** Mosquitto MQTT via Spring Integration, with DLQ routing. Resilience4j circuit breaker and fallback to Redis queue during database downtime.

### [Construction OS](https://github.com/thitipongroo/cos) · `NestJS, React Native, Python, Go` `🚧 In development`
AI-native construction management platform built for enterprise scale. 
- **Modular monolith over microservices:** One deployable holding all domain modules, with separate services only where throughput boundary justifies it.
- **Offline-first clients:** Drizzle over expo-sqlite with a sync queue on React Native, reconciling through Kafka; built for sites with no signal.
- **Monetary correctness:** Strict database enforcement (`DECIMAL(19,4)`) and float banning via lint rules.

### [Omni-Tracker](https://github.com/thitipongroo/omni-tracker) · `Go, InfluxDB, Playwright, Docker` `🚧 In development`
A distributed, high-concurrency market intelligence platform. 
- Treats web scrapers as "IoT sensors" to ingest massive e-commerce data into a Golang Fiber API.
- Stores time-series trends in InfluxDB with real-time LINE Bot alerts.
- Fully containerized via Docker Compose with GitHub Actions CI/CD pipeline.

### [Cypress Cinema Automation](https://github.com/thitipongroo/cypress-cinema-test) · `Cypress` `📚 Portfolio project`
E2E suite for a cinema booking platform using Page Object Model, JSON Fixture-driven test data, and Mochawesome HTML reports generated in CI.

### [Embedded & Automation]
- **[LINE Bot API](https://github.com/thitipongroo/line-bot-api):** RESTful service integrated with LINE Messaging API (Java/Spring Boot).
- **[Remote Vote](https://github.com/thitipongroo/remote-vote-firebase):** Secure remote voting system with live result updates (Firebase/C).
- **[Smart Window](https://github.com/thitipongroo/smart-window):** IoT automation that reads environmental sensor data (C++).

---

## 🏆 Certifications
Google Cybersecurity • Prompt Engineering & Agentic AI • Secure Coding: OWASP Top 10 • Secure Coding on Frontend
