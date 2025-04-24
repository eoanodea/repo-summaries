# Repository Summary

## Overview

The `food-delivery-modular-monolith` repository is a sample .NET-based modular monolith application demonstrating key architectural patterns and best practices:
- Modular Monolith Architecture
- Vertical Slice Architecture
- Domain-Driven Design (DDD)
- Command Query Responsibility Segregation (CQRS)
- Event-Driven Architecture (using an in-memory broker)

It shows how to build a self-contained, maintainable, and testable monolith with independent modules and a clear path to transition toward microservices.

## Key Components
- **src/**: Main Food Delivery solution
  - **Api/FoodDelivery.Api**: Public API hosting all modules via HTTP (minimal APIs and MVC controllers)
  - **BuildingBlocks**: Shared libraries for messaging, persistence, monitoring, security, web abstractions, and more
  - **Modules**: Domain modules (Catalogs, Customers, Identity, Orders), each as a vertical slice with its own composition root and persistence
- **_httpclients/**: REST client definitions for synchronous inter-module calls
- **deployments/**: Docker Compose configuration for infrastructure
- **assets/**: Architecture and module diagrams
- **tests/**: Unit and integration tests for building blocks, modules, and shared components
- **my-monolith/**: Alternative non-modular monolith implementation for comparison

## Technologies & Libraries
- .NET 8, ASP.NET Core
- Entity Framework Core (PostgreSQL)
- FluentValidation, AutoMapper
- Serilog, OpenTelemetry, Health Checks
- Duende IdentityServer, JWT Authentication
- Polly, Scrutor
- StyleCop Analyzers
- IdGen (Snowflake-like IDs), Hellang ProblemDetails middleware
- Testing: xUnit, NSubstitute

## Architecture Highlights
- **Composition Roots**: Each module has its own dependency injection container for autonomy
- **In-Memory Messaging**: Asynchronous communication between modules
- **GatewayProcessor**: Routes commands and queries to the appropriate module's service provider
- **CQRS**: Separation of read/write models; prepares for future event sourcing and projections

## Getting Started
1. Install .NET 8 SDK
2. Restore dependencies: `dotnet restore`
3. Build solution: `dotnet build`
4. Run API: `dotnet run --project src/Api/FoodDelivery.Api`
5. Run tests: `dotnet test`

Refer to [README.md](README.md) for detailed instructions and design discussion.