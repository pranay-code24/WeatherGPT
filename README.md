<h1 align="center">WeatherGPT</h1>

<p align="center">
   An AI-powered conversational platform for real-time weather intelligence, extreme event alerts, and climate analysis. <br>
</p>

<p align="center">
  <a href="#introduction"><strong>Introduction</strong></a> ·
  <a href="#features"><strong>Features</strong></a> ·
  <a href="#architecture--tech-stack"><strong>Architecture & Tech Stack</strong></a> ·
  <a href="#getting-started"><strong>Getting Started</strong></a>
</p>
<br/>

## Introduction

Weather information is often fragmented across multiple portals, bulletins, and forecast systems, making it difficult for common users, farmers, and disaster managers to quickly obtain actionable insights.

**WeatherGPT** bridges this gap. It is an intelligent conversational platform that seamlessly integrates official meteorological datasets, numerical forecasting models (GFS/WRF), and disaster warning systems to provide accurate, location-based weather intelligence through a native, multilingual interface.

## Features

- **Unified Data Ingestion:** Real-time data pipeline utilizing MQTT and WMO WIS 2.0 protocols for zero-latency updates.
- **Multilingual Voice AI:** Voice-enabled interactions powered by Whisper ASR and Indic LLM models to ensure rural accessibility and bypass language barriers.
- **Geospatial Micro-Forecasting:** Pinpoint location-based agricultural and civic advisories powered by PostGIS spatial routing.
- **Instant Disaster Alerts:** Low-latency push notifications for extreme weather events (floods, cyclones) distributed via WebSockets.
- **Sector-Specific RAG:** Dynamic LLM prompt templates tailored for precise use cases like farming crop cycles, aviation briefings, and smart city planning.
- **Scalable Infrastructure:** Auto-scaling containerized deployment designed to handle massive traffic spikes during critical weather emergencies.

## Architecture & Tech Stack

WeatherGPT relies on a high-availability microservices architecture combining robust backend data processing with responsive conversational AI:

- **Frontend Interfaces:** Next.js (Web Dashboard), TailwindCSS, Flutter (Mobile App)
- **Backend Services:** FastAPI (Python for NWP processing & AI endpoints), Node.js (WebSocket management)
- **AI & NLP Engine:** Gemini / Llama 3 API, Whisper ASR
- **Databases:** PostgreSQL with PostGIS (Relational user & geospatial data), MongoDB (Conversational logging & caching)
- **Real-Time Networking:** MQTT, WebSockets
- **Infrastructure:** Docker, Kubernetes