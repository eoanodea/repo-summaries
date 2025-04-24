# Food Delivery Microservices Repository Summary

**Food Delivery Microservices** is a sample .NET-based microservices architecture demonstrating modern cloud-native design patterns, vertical slice architecture, and various integration techniques.

## Overview
- Purpose: Showcase a fictional food delivery platform built using microservices, Domain-Driven Design (DDD), CQRS, Event-Driven Architecture, and other best practices.
- Technologies: .NET 9, ASP.NET Core, MassTransit, RabbitMQ, MediatR, Entity Framework Core, EventStoreDB, PostgreSQL, MongoDB, Elasticsearch, Serilog, OpenTelemetry, YARP, and more.
- Architecture: API Gateway → microservices → databases/message broker; supports synchronous (REST/gRPC) and asynchronous (MassTransit/RabbitMQ) communication.

## Key Components
- **ApiGateway**: YARP-based reverse proxy (`src/ApiGateway/FoodDelivery.ApiGateway`).
- **BuildingBlocks**: Shared infrastructure abstractions (caching, email, health checks, open API, persistence, messaging, observability, validation, security, resiliency).
- **Services** (`src/Services/*`): Individual microservices such as Catalogs, Customers, Identity, Orders, Billing, Carts, etc., each with its own domain, API, and persistence.
- **_httpclients**: REST definitions for generating strongly-typed HTTP clients for inter-service calls.
- **Assets**: Architecture diagrams and images illustrating high-level structure and vertical slice flow.
- **Deployments**:
  - `deployments/docker-compose`: Compose files for local and production deployments.
  - `deployments/k8s`: Kubernetes manifests and Kustomize overlays.
  - `deployments/configs`: Monitoring (Prometheus, Grafana), logging (Loki), tracing (Tempo).
- **Scripts** (`scripts/docker`): Shell scripts to run services in various environments using Docker.

## Testing
- **Unit Tests**: xUnit, NSubstitute in `tests` folder.
- **Integration & E2E Tests**: Using `testcontainers-dotnet` for isolated Docker-based test environments.

## Features & Patterns
- Microservices & Vertical Slice Architecture
- DDD & Bounded Contexts
- CQRS with MediatR
- Event Sourcing & EventStoreDB
- Outbox & Inbox patterns for reliable messaging
- Structured logging (Serilog → Elasticsearch & Kibana)
- OpenTelemetry metrics and distributed tracing
- Resiliency via Polly
- API documentation with Swagger / OpenAPI
- Authentication & Authorization with Duende IdentityServer
- Containerized deployments (Docker Compose, Kubernetes, Helm, Kustomize)
- Developer productivity: PM2, Microsoft Tye, GitHub Codespaces support

## Getting Started
Refer to `readme.md` for prerequisites and setup instructions:
- Local development: PM2, Docker Compose, Tye.
- Kubernetes: `deployments/k8s` with Kustomize overlays.
- Monitoring: Prometheus, Grafana dashboards in `deployments/configs/grafana`.

----
This repository is continuously evolving. For detailed information, visit the [README](readme.md) or the project author’s GitHub.
----