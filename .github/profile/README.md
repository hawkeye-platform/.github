# Hawkeye

> High-performance cloud platform for algorithmic cryptocurrency trading.

## Overview

Hawkeye is a distributed, event-driven trading platform designed for low latency,
high throughput, and horizontal scalability.

The platform provides infrastructure for:

- 📈 Market data collection
- ⚡ Strategy execution
- 💹 Order management
- 📊 Portfolio tracking
- 📉 Risk management
- 🔔 Real-time notifications
- 📜 Historical analytics

---

# Architecture

The platform follows a microservice architecture.

```
                API Gateway
                     │
        ┌────────────┴────────────┐
        │                         │
      REST                     gRPC
        │                         │
 ┌──────▼─────────────────────────▼──────┐
 │              RabbitMQ                  │
 └────────────────────────────────────────┘
        │
 ┌──────┼─────────────────────────────────────────────┐
 │      │      │      │      │      │      │          │
 ▼      ▼      ▼      ▼      ▼      ▼      ▼          ▼

 Auth  Users Market Orders Trading Portfolio Risk Notifications
               │
               ▼
          Exchange Connectors
               │
      Binance • Bybit • OKX • etc.
```

---

# Technology Stack

| Layer | Technology |
|--------|------------|
| Language | C# (.NET) |
| Database | PostgreSQL |
| Cache | Redis |
| Messaging | RabbitMQ |
| RPC | gRPC |
| API | REST |
| Authentication | JWT |
| Containerization | Docker |
| Orchestration | Kubernetes |
| CI/CD | GitHub Actions |

---

# Core Principles

- Event-driven architecture
- Domain-driven design (DDD)
- CQRS
- Clean Architecture
- SOLID principles
- High availability
- Horizontal scalability
- Fault tolerance
- Observability-first

---

# Services

- API Gateway
- Authentication
- User Service
- Market Data
- Exchange Gateway
- Order Service
- Portfolio Service
- Trading Engine
- Strategy Engine
- Risk Engine
- Notification Service
- Reporting Service

---

# Repository Structure

```
hawkeye-platform/
│
├── api-gateway/
├── auth-service/
├── user-service/
├── market-service/
├── exchange-service/
├── trading-service/
├── order-service/
├── portfolio-service/
├── risk-service/
├── notification-service/
├── reporting-service/
├── shared/
├── infrastructure/
└── docs/
```

---

# Development

Requirements

- .NET 10
- PostgreSQL
- Redis
- RabbitMQ
- Docker
- Docker Compose

---

# Vision

Build a modern, cloud-native trading infrastructure capable of running automated
cryptocurrency trading strategies across multiple exchanges with reliability,
speed, and scalability.

---

## License

Private repository.
