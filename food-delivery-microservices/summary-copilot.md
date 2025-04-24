# Food Delivery Microservices Repository

This repository contains a food delivery application built using a microservices architecture. It is designed to demonstrate best practices in building scalable, maintainable, and observable distributed systems.

## Repository Structure

### Root Files

-   **commitlint.config.js**: Configuration for commit message linting.
-   **CONTRIBUTION.md**: Guidelines for contributing to the repository.
-   **food-delivery-microservices.slnx**: Solution file for managing the project.
-   **global.json**: Configuration for .NET SDK version.
-   **LICENSE**: Licensing information.
-   **nuget.config**: Configuration for NuGet package management.
-   **package.json**: Node.js package configuration.
-   **pipeline-behaviors.md**: Documentation on pipeline behaviors.
-   **pm2.json / pm2.yaml**: PM2 process manager configuration files.
-   **readme.md**: General overview of the repository.
-   **stylecop.json**: StyleCop configuration for code style enforcement.
-   **summary-codex.md**: Existing summary of the repository.

### HTTP Clients

Located in the `_httpclients/` directory, this contains REST client configurations for various services:

-   **catalogs.rest**: Catalog service API.
-   **customers.rest**: Customer service API.
-   **identity.rest**: Identity service API.
-   **rabbitmq.rest**: RabbitMQ API.

### Assets

The `assets/` directory contains images and diagrams, such as architecture diagrams and service illustrations.

### Deployments

The `deployments/` directory includes configurations for deploying the application:

-   **configs/**: Configuration files for monitoring and observability tools like Grafana, Prometheus, and Loki.
-   **docker-compose/**: Docker Compose files for different environments (infrastructure, development, production).
-   **k8s/**: Kubernetes deployment configurations.

### Scripts

The `scripts/` directory contains shell scripts for managing Docker containers:

-   **docker/**: Scripts for running services in different environments (base, debug, dev, prod).

### Source Code

The `src/` directory contains the main application code:

-   **ApiGateway/**: API Gateway for routing requests to services.
-   **BuildingBlocks/**: Shared libraries and utilities for cross-cutting concerns (e.g., caching, health checks, observability).
-   **Services/**: Microservices for different domains (e.g., Catalogs, Customers, Identity, Orders).

### Tests

The `tests/` directory contains unit, integration, and end-to-end tests for the application:

-   **ApiGateway/**: Tests for the API Gateway.
-   **BuildingBlocks/**: Tests for shared libraries.
-   **Services/**: Tests for individual microservices.
-   **Shared/**: Shared test utilities.

## Tasks

The repository includes a variety of tasks for building, testing, and deploying the application. These tasks are defined in the VS Code workspace and include:

### Build and Watch

-   Build and watch tasks for each service (e.g., `build: catalogs`, `watch: catalogs`).

### Docker

-   Docker build and run tasks for different environments (e.g., `docker-build-dev: catalogs`, `docker-run-dev: catalogs`).
-   Docker Compose tasks for managing infrastructure and services.

### Testing

-   Unit, integration, and end-to-end test tasks for each service (e.g., `unit test: catalogs`, `integrtion test: catalogs`).

### Miscellaneous

-   NPM tasks for preparing the environment and installing dependencies.
-   Script for installing the VS Debugger on Ubuntu.

## Key Features

-   **Microservices Architecture**: Each service is independently deployable and scalable.
-   **Observability**: Configurations for monitoring and logging using tools like Grafana, Prometheus, and Loki.
-   **Docker and Kubernetes**: Support for containerized deployments and orchestration.
-   **Extensive Testing**: Unit, integration, and end-to-end tests for ensuring code quality.
-   **Shared Libraries**: Reusable components for common functionality.

## Getting Started

1. Install dependencies using the `npm: install dependencies` task.
2. Build the desired service using the corresponding `build` task.
3. Run the service locally using Docker or Docker Compose.
4. Execute tests using the `unit test`, `integrtion test`, or `end-to-end test` tasks.

For more details, refer to the `readme.md` and `CONTRIBUTION.md` files.
