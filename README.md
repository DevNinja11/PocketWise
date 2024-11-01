# Project Overview
This project is a fintech microservices-based web application that enables users to perform essential financial transactions, such as user registration, logging in, topping up balances, and transferring funds securely through virtual wallets. Leveraging a modular microservices architecture, this application ensures scalability, security, and a smooth user experience, offering efficient user account and wallet management. 

# Tech Stack
### Backend Technologies
- ```Java 17+```
- ```Spring Boot 3.2.0``` – Core framework for building and deploying application services.
- ```Spring Cloud 2023.0.0``` – Facilitates service communication, load balancing, and service registry.
- ```Wiremock, JUnit, Integration Tests``` – For mock testing, unit tests, and comprehensive integration testing.
- ```OpenFeign``` – Used for remote service calls, improving the flexibility of microservice interactions.

### Infrastructure & DevOps
- ```Kubernetes with Minikube``` – Deploys and manages microservices with local K8s clusters.
- ```Docker``` – Containerizes each service for smooth deployment and portability.
- ```Zipkin, Logbook, and Micrometer``` – Provides distributed tracing, logging, and metrics monitoring for tracking system health and performance.
- ```Swagger/OpenAPI``` – API documentation for streamlined development and API usage.

### Architecture Patterns
- ```Microservice Architecture``` – Modular design with clearly defined service boundaries.
- ```Domain-Driven Design (DDD)``` – Emphasizes business domain logic separation.
- ```Data-Driven Testing (DDT)``` – Ensures comprehensive testing coverage.
- ```Value Objects``` – Maintains immutability and enhances code readability.

![Screenshot 2024-08-09 104435](https://github.com/user-attachments/assets/e4ea2b0b-1089-4d2a-b416-fac7e4b8543f)

# Key Features
- **User Registration and Authentication** – Secure registration and login functionality.
- **Balance Top-Up** – Enables users to add funds to their virtual wallets.
- **Fund Transfer** – Allows secure and efficient transfer of funds between users.
- **Detailed Transaction History** – View complete transaction records for user reference.
- **Comprehensive API Documentation** – Enables seamless integration and service use.

# Service Module Structure
Each module in the application adheres to microservices principles, with distinct responsibilities and clear separation:

### Auth Module
- ```auth-sdk```: An SDK for integrating authentication features across modules.
- ```auth-api```: Contains API interfaces and definitions for authentication processes.
- ```auth-client```: Uses OpenFeign for remote authentication calls.
- ```auth-service```: The core, runnable Spring application for user authentication and authorization.

### User Module
- ```user-api```: Contains API definitions and interfaces for user operations.
- ```user-client```: Facilitates remote calls for user-related actions.
- ```user-service```: Manages core user operations, including registration and information retrieval.

### Wallet Module
- ```wallet-api```: Defines API interfaces for wallet management and transactions.
- ```wallet-client```: Feign client for seamless wallet-related interactions.
- ```wallet-service```: Handles wallet functions such as creating wallets, topping up, and fund transfers.

Each module is version-controlled as a Maven variable, allowing consistent updates across the project and reducing manual maintenance efforts.

# My Contribution
In this project, I led the DevOps and Microservices aspects, building a robust deployment pipeline and containerizing the application with **Docker**. I deployed and managed the microservices in **Kubernetes** (with Minikube for local development), ensuring each service was scalable and secure. For observability, I implemented **Zipkin** for distributed tracing, **Logbook** for centralized logging, and **Micrometer** for metrics monitoring, providing a clear view of system health and performance. My contributions helped create a flexible, production-ready application, fully integrated with CI/CD workflows for efficient deployment and maintenance.
