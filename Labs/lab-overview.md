# GitHub CoPilot Java App Modernization - Hackathon

### Introduction

Welcome to the Java App Modernization Hackathon. In this hands-on challenge, teams will modernize a legacy Java web application ("Asset Manager") using AI-assisted tooling (GitHub Copilot App Modernization) and Azure platform services. The application currently uses local PostgreSQL, AWS S3, and RabbitMQ. During the hackathon you'll assess the app, apply upgrades and refactors, migrate services to Azure, containerize the app, and deploy it to Azure Kubernetes Service (AKS).

### Learning Objectives
By participating in this hackathon, you will learn how to:

  - Run and assess a legacy Spring Boot Java application locally and identify modernization blockers.
  - Upgrade Java runtime and Spring framework versions safely.
  - Migrate relational data to Azure Database for PostgreSQL (Flexible Server).
  - Migrate object storage from AWS S3 to Azure Blob Storage.
  - Migrate messaging from RabbitMQ (AMQP) to Azure Service Bus.
  - Expose and validate health and monitoring endpoints using Spring Boot Actuator.
  - Containerize the application with Docker and produce working Dockerfiles.
  - Provision infrastructure and deploy the application to AKS, validating pods and ingress.

###  Hackathon Format: Challenge-Based

  - Structure: Challenge-based, hands-on lab with incremental tasks. Teams complete a sequence of challenges that build on each other.
  - Timebox: The event is timeboxed to 4 hours. Each challenge includes a recommended time allocation.
  - Tools: GitHub Copilot App Modernization extension (VS Code), Docker, Azure CLI / Azure Portal, and Kubernetes tools (kubectl/AKS).
  - Collaboration: Teams should use source control (Git) and coordinate code changes. Use the Copilot agent to generate suggested modifications, then review and apply them.
  - Scoring (optional): Points awarded for completing challenges, successful migrations, running containers, and successful AKS deployment. Bonus points for documenting decisions and producing a short demo.

### Challenges

The hackathon is organized into discrete challenges. Complete them in order for a smooth experience:

1. Assess the Application
   - Run the app locally with provided scripts.
   - Use Copilot App Modernization to generate an assessment report and identify blockers.

2. Upgrade Java & Frameworks  
   - Run the Java Version Upgrade task to update JDK and Spring Boot versions.
   - Resolve compilation or dependency issues.

3. Migrate Database to Azure
   - Use Copilot tasks to migrate data/configuration to Azure Database for PostgreSQL Flexible Server.
   - Validate DB connectivity and migrations.

4. Migrate Storage to Azure Blob Storage 
   - Convert S3 usage to Azure Blob Storage.
   - Update configuration and test file operations.

5. Migrate Messaging to Azure Service Bus 
   - Refactor RabbitMQ AMQP code paths to use Azure Service Bus (or use adapter patterns).
   - Validate message flow end-to-end.

6. Add Health & Monitoring 
   - Create a custom Copilot task to enable Spring Boot Actuator health endpoints.
   - Verify readiness and liveness endpoints.

7. Containerize the Application
   - Generate Dockerfile(s) via Copilot, build images, and fix build errors.
   - Run containers locally to ensure parity.

8. Deploy to Azure
   - Provision infrastructure and deploy to AKS using Copilot-generated deployment plan.
   - Validate pods, external access, and Azure resources.

Success criteria: application runs locally after modernization tasks, all three migrations completed (DB, storage, messaging), health endpoints active, Docker images built, and application accessible on AKS.

## Support Contact

The CloudLabs support team is available 24/7, 365 days a year, via email and live chat to ensure seamless assistance at any time. We offer dedicated support channels tailored specifically for both learners and instructors, ensuring that all your needs are promptly and efficiently addressed.

Learner Support Contacts:
- Email Support: cloudlabs-support@spektrasystems.com
- Live Chat Support: https://cloudlabs.ai/labs-support

### Happy hacking!
