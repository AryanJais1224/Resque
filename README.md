# Resque

> A real-time, event-driven emergency triage and logistics orchestration platform powered by multi-agent AI, spatial computing, and streaming infrastructure.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-Async%20API-green.svg)
![LangGraph](https://img.shields.io/badge/LangGraph-Multi--Agent-orange.svg)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-PostGIS-blue.svg)
![Qdrant](https://img.shields.io/badge/Qdrant-Vector%20DB-purple.svg)
![Next.js](https://img.shields.io/badge/Next.js-Dashboard-black.svg)

---

## Table of Contents

- [Overview](#overview)
- [Application User Interface](#application-user-interface)
- [Demo Video](#demo-video)
- [Tech Stack](#tech-stack)
- [System Architecture](#system-architecture)
- [Engineering Decisions](#engineering-decisions)
- [Installation & Running the Project](#installation--running-the-project)
- [License](#-license)
- [Author](#-author)

---

# Overview

Resque is a distributed emergency triage and logistics orchestration system designed to process incoming SOS signals in real time and route them through an AI driven decision pipeline. The system ingests structured binary emergency packets, evaluates urgency using an LLM based triage agent, allocates optimal resource depots via vector similarity search, and computes safe routes using spatial queries.

The platform is built around a multi-agent workflow powered by LangGraph, where each node represents a distinct operational intelligence layer: planning, prioritization, resource allocation, and routing. These agents collaborate over a shared state object, enabling deterministic yet adaptive execution flows.

The system integrates multiple backend primitives including Kafka (Redpanda-compatible streaming), Qdrant for semantic inventory retrieval, and PostGIS for spatial route validation. The frontend dashboard built in Next.js provides real-time operational visibility with WebSocket-driven mission updates and interactive geospatial visualization.

The primary engineering goal is to build a resilient, failure-tolerant emergency dispatch pipeline capable of handling partial system failures, rerouting logistics dynamically, and ensuring safe spatial decision-making under constrained conditions.

### Core Engineering Objectives

- Design a deterministic multi-agent execution pipeline using LangGraph
- Enable real-time ingestion of structured emergency telemetry via Protobuf
- Implement semantic resource allocation using vector similarity search (Qdrant)
- Ensure spatial safety validation using PostGIS intersection queries
- Provide automatic rerouting on hazard detection and depot failure
- Maintain low-latency streaming using Kafka/Redpanda event pipeline
- Enable real-time dashboard synchronization via WebSockets
- Ensure system resilience through cyclic recovery loops in workflow graph

### Core Features

- Multi-agent orchestration pipeline (Planner → Priority → Resource → Routing)
- LLM-based emergency classification using Google Gemini structured output
- Semantic inventory matching via FastEmbed + Qdrant
- Spatial route validation using PostGIS geometry intersection
- Automatic failure recovery through conditional graph cycles
- Real-time mission broadcast via Kafka + WebSocket bridge
- Interactive geospatial dashboard with mission + drone telemetry
- Binary Protobuf-based ingestion for efficient payload transport

---

# Application User Interface

<p align="center">
  <table align="center">
    <tr>
      <td valign="top" align="center">
        <img src="https://github.com/user-attachments/assets/9dfdafd7-5f1d-44b8-8874-30998278f0ff" width="260" alt="Home Screen">
      </td>
      <td valign="top" align="center">
        <img src="https://github.com/user-attachments/assets/2e12e8e9-ece4-4282-a971-d6447ec5f2bb" width="260" alt="Chat Screen">
      </td>
      <td valign="top" align="center">
        <img src="https://github.com/user-attachments/assets/ee1d1fb9-eb8f-48d6-ad6f-7e574b7f7b2d" width="260" alt="Profile Screen">
      </td>
    </tr>
  </table>
</p>

---

# Demo Video

Demo video will be added.

---

# Tech Stack

| Layer | Technologies | Purpose |
|------|-------------|--------|
| API Layer | FastAPI | High-performance async ingestion gateway |
| Streaming | Kafka / Redpanda | Event-driven message pipeline |
| Orchestration | LangGraph | Multi-agent workflow execution |
| LLM | Google Gemini (gemini-2.5-flash) | Emergency triage classification |
| Vector DB | Qdrant | Semantic inventory retrieval |
| Embeddings | FastEmbed (MiniLM) | Lightweight embedding generation |
| Spatial DB | PostgreSQL + PostGIS | Route safety and geospatial queries |
| Backend Runtime | Python | Core system logic |
| Frontend | Next.js | Command center dashboard UI |
| Mapping | Leaflet | Real-time geospatial visualization |
| Auth | Firebase Authentication | Secure user identity verification |
| ORM | SQLAlchemy | Database abstraction layer |

---

# System Architecture

Architecture diagram will be added soon.

---

# Engineering Decisions

This system is designed around high-throughput event processing, spatial correctness, and agent-based orchestration. Each major architectural decision is driven by reliability, latency constraints, or domain-specific computation requirements.

| Design Decision | Rationale |
|----------------|----------|
| LangGraph multi-agent pipeline | Enables deterministic execution flow with modular AI agents and stateful transitions |
| Kafka / Redpanda event streaming | Provides durable, ordered, and scalable ingestion of high-frequency SOS packets |
| Protobuf binary ingestion | Reduces payload size and ensures strict schema enforcement for field transmissions |
| Qdrant vector database | Enables semantic retrieval of nearest resource depots based on emergency context |
| FastEmbed (MiniLM) | Lightweight embedding model optimized for low-latency inference without GPU dependency |
| PostGIS spatial queries | Ensures mathematically correct route validation using geometric intersection checks |
| Cyclic graph edges in LangGraph | Enables automatic rerouting when hazard blocking or depot failure occurs |
| WebSocket dashboard layer | Provides real-time mission updates without polling overhead |
| Docker-based infra assumption | Ensures consistent deployment of Kafka, Postgres, and Qdrant services |
| Async FastAPI gateway | Supports concurrent ingestion of multiple SOS streams with minimal blocking |

---

# Installation & Running the Project

Installation guidelines will be added soon.

---



# 📄 License

Distributed under the **MIT License**.

See the `LICENSE` file for more information.

---

# 👨‍💻 Author

**Aryan Jaiswal**

- GitHub: https://github.com/AryanJais1224
- LinkedIn: https://www.linkedin.com/in/aryan-jaiswal-618965256/

---
