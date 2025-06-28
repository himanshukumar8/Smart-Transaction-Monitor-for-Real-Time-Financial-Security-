# 💳 Smart Transaction Monitor for Real-Time Financial Security 

A high-performance, real-time fraud detection engine built with **Kafka Streams** and **Spring Boot** to analyze a live stream of financial transactions, identify fraudulent patterns using stateful stream processing, and flag suspicious activity in milliseconds.

## 🚀 Key Features

- **Real-Time Processing**: Ingests and analyzes a high-throughput stream of Kafka events with millisecond latency.
- **Stateful Analysis**: Uses Kafka Streams' **custom processor topology** to aggregate and monitor transaction activity.
- **Complex Pattern Detection**: Flags behaviors like multi-location ATM usage and burst transaction activity within session windows.
- **Event-Driven & Scalable**: Fully decoupled, Kafka-powered architecture containerized with Docker for smooth deployment.

## 🛠️ Technology Stack

- **Backend**: Java 11+, Spring Boot  
- **Stream Processing**: Kafka Streams (Processor API)  
- **Messaging**: Apache Kafka  
- **Containerization**: Docker, Docker Compose

---

## 🧠 How It Works

1. **Transaction Ingestion**: Transactions (movements) are continuously streamed into a Kafka topic.
2. **Stream Analysis**: The `fraud-checker` service consumes and processes these events in real time.
3. **Topology Logic**: Stream processing pipeline detects fraud conditions based on temporal and behavioral criteria.
4. **Alerting**: Suspicious activities are flagged and routed to a separate `fraud-cases` Kafka topic.

---

## ▶️ How to Run the Demo

### 🔧 Prerequisites

- Docker & Docker Compose  
- JDK 11+  
- Maven

### 📝 Instructions

1. **Clone the repository and navigate to the project directory:**
   ```bash
   git clone https://github.com/jaruizes-paradigma/fraud-checker-kstreams-springboot.git
   cd fraud-checker-kstreams-springboot
