# Hackathon Mission and Use-Case

Mission: Demonstrate a rapid, repeatable modernization pipeline for a Java monolith that reduces operational overhead and migrates dependencies to managed cloud services while preserving application functionality.

A small-to-medium enterprise wants to move a self-hosted asset management application to cloud-managed services to improve reliability, reduce maintenance, and enable scalable deployments. The modernization path includes:

- Upgrading to a supported Java runtime and modern Spring Boot.

- Moving relational data to a managed PostgreSQL service (Azure Database for PostgreSQL Flexible Server).

- Replacing object storage with Azure Blob Storage.

- Moving messaging to Azure Service Bus for durable, managed messaging.

- Containerizing and deploying to AKS for scalable orchestration.

- Adding observability via Spring Boot Actuator.

Participants will adopt best practices for incremental modernization: run and test locally, apply automated refactor suggestions, and validate each migration step before proceeding to the next.
