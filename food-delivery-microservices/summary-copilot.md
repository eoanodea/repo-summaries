# Food Delivery Microservices Repository

A sample food delivery application built with a microservices architecture, showcasing best practices in scalability, observability, and maintainability.

## Repository Layout

├── **commitlint.config.js** Configuration for commit message linting  
├── **CONTRIBUTION.md** Contribution guidelines  
├── **LICENSE** License information  
├── **package.json** Node.js package config  
├── **readme.md** High-level overview  
├── **src/** Microservices and shared libraries  
│ ├── ApiGateway/ API gateway project  
│ ├── BuildingBlocks/ Cross-cutting libraries (caching, logging, health checks, etc.)
│ └── Services/ Domain services (Catalogs, Customers, Identity, Orders, Billing, etc.)
├── **\_httpclients/** REST client definitions  
├── **assets/** Architecture diagrams and images  
├── **deployments/** Docker Compose, Kubernetes, monitoring configs
└── **scripts/docker/** Helper scripts for local Docker runs

## Tasks & Workflows

-   **Build & Watch**: `dotnet build/watch` tasks per service
-   **Docker**: build/run targets (`dev`, `debug`, `prod`) via scripts and Compose
-   **Testing**: unit, integration, end‑to‑end tests for each service
-   **Observability**: Prometheus, Grafana, Loki, Tempo configurations

## Key Features

-   Independently deployable .NET Core microservices
-   Shared BuildingBlocks for common concerns
-   Containerized workflows (Docker, Kubernetes)
-   Comprehensive test suites
-   Observability with OpenTelemetry, Grafana, Prometheus

## Getting Started

1. Install dependencies: `npm install` / `dotnet tool restore`
2. Build a service: `dotnet build src/Services/<Name>/...`
3. Run locally: `npm run docker-run-dev` or `docker-compose up`
4. Execute tests: `dotnet test tests/Services/<Name>`

Refer to `readme.md` and `CONTRIBUTION.md` for detailed instructions.
