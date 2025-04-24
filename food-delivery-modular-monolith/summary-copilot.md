# Food Delivery Modular Monolith Repository

This repository contains the source code for a modular monolith application designed for a food delivery service. The project is structured to emphasize modularity, scalability, and maintainability, leveraging modern software engineering practices.

## Repository Structure

### Solution and Configuration Files

- **food-delivery-modular-monolith.sln**: The main solution file for the project.
- **global.json**: Specifies the .NET SDK version.
- **nuget.config**: Configuration for NuGet package sources.
- **stylecop.json**: StyleCop configuration for code style enforcement.

### HTTP Clients

Located in the `_httpclients/` directory, this folder contains REST client definitions for various modules:

- **catalogs.rest**: REST client for the Catalogs module.
- **customers.rest**: REST client for the Customers module.
- **identity.rest**: REST client for the Identity module.

### Assets

The `assets/` directory contains visual assets such as architecture diagrams and module structure illustrations.

### Deployments

The `deployments/` directory includes deployment configurations:

- **docker-compose.infrastructure.yaml**: Docker Compose file for infrastructure setup.

### Source Code

The `src/` directory contains the main application code, organized into the following subdirectories:

#### Api

- **FoodDelivery.Api/**: Contains the API layer of the application, including configuration files, constants, and the main `Program.cs` file.

#### Building Blocks

Reusable components and abstractions shared across modules:

- **BuildingBlocks.Abstractions/**: Core abstractions for caching, CQRS, domain logic, messaging, persistence, and more.
- **BuildingBlocks.Caching.InMemory/**: In-memory caching implementation.
- **BuildingBlocks.Core/**: Core utilities and services, such as `ServiceActivator` and `ExclusiveLock`.
- Additional building blocks for email, logging, monitoring, security, and more.

#### Modules

Feature-specific modules, each encapsulating its own domain logic:

- **Catalogs/**: Handles catalog-related functionality.
- **Customers/**: Manages customer-related operations.
- **Identity/**: Responsible for authentication and identity management.
- **Orders/**: Manages order processing and tracking.

### Tests

The `tests/` directory contains unit and integration tests, organized into:

- **building-blocks/**: Tests for shared building blocks.
- **modules/**: Tests for individual modules like Customers and Identity.
- **shared/Tests.Shared/**: Shared testing utilities.

## Key Features

- **Modular Monolith Architecture**: Promotes separation of concerns and scalability.
- **Building Blocks**: Reusable components for common functionalities.
- **REST Clients**: Predefined clients for inter-module communication.
- **Docker Support**: Infrastructure setup using Docker Compose.
- **Comprehensive Testing**: Well-structured test suites for reliability.

## Visual Assets

The `assets/` directory includes diagrams illustrating the architecture and module structure, such as:

- Vertical Slice Architecture
- Module Composition Roots

## Getting Started

1. Clone the repository.
2. Open the solution file `food-delivery-modular-monolith.sln` in your IDE.
3. Restore NuGet packages using `nuget restore`.
4. Build and run the application.

## License

Refer to the `LICENSE` file for licensing information.
