Overview
The system is a comprehensive cloud-based ticketing and remote maintenance solution leveraging Azure services, containerization, time-series data recording, and a marketplace for extension installation. It's designed to offer scalable, secure, and high-availability IoT management with reduced operational costs.
Core Components
Cloud Platform
Azure : Primary hosting environment for all services.
Compute Services
Azure Functions : Serverless compute for processing tasks (e.g., ADB2C invitation function).
Kubernetes : Orchestration for containerized application management.
IoT Management
Azure IoT Hub : Central communication service for IoT devices.
OPC UA : Protocol for collecting machine data.
Data Storage
Azure SQL Database : Relational database for main application data.
Azure Blob Storage : Temporary storage for time-series data before ingestion.
Azure Data Explorer (ADX) : Time-series database for measurement data.
Cosmos DB : Stores data model definitions and marketplace applications.
Continuous Delivery and Deployment
Argo CD : GitOps tool for continuous deployment integrated with Kubernetes.
Networking and API Management
IoT Hub : Communication hub for IoT devices.
Tyk : API management platform, segregating public APIs from internal graph.
Apollo GraphQL : GraphQL implementation for efficient data querying.
Security Measures
API Key Authentication : For Azure Functions.
Azure DDoS Protection : To prevent denial-of-service attacks.
IP Whitelisting : For Azure SQL Database.
MSAL Library : Ensures secure authentication against Azure Identity Provider.
Runtime Environments and Frameworks
Spring Boot : Microservices framework.
Node.js : Server-side JavaScript runtime.
React : Frontend framework.
Logging
Elasticsearch : Centralized logging platform.
Third-party Integrations
Marketplace : For customer to install extensions.
Specific Functions
Remote Tunnel Connection : Facilitates remote maintenance of shop floor devices.
Marketplaces : Allows users to install various extensions.
ADB2C Invitation Function : Manages user invitations and access control.
Scalability and High Availability
Azure and Kubernetes enhance scalability and high availability.
Argo CD supports consistent and reliable deployments.