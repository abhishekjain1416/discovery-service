# Service Discovery with Netflix Eureka
## Introduction

Welcome to the Service Discovery with Netflix Eureka project! This service discovery solution is designed to simplify the process of locating and communicating with microservices within distributed application architecture. By utilizing Netflix Eureka, we can effectively manage and coordinate services, making it easier to scale microservices-based applications.

In a microservices architecture, services are distributed across multiple instances and can dynamically scale up or down based on demand. Keeping track of these services and their availability becomes a complex task. Netflix Eureka simplifies this challenge by providing a centralized service registry that allows services to register themselves and query the registry for information about other services.

## Architecture
Overall Architecture of the E-Commerce Platform

![architecture-E-Commerce Application drawio](https://github.com/abhishekjain1416/discovery-service/assets/142833334/11165903-8564-43ea-9839-ee4b13adc9b8)


Here's a brief explanation of the architecture of a service discovery system using Netflix Eureka:

### Service Registry (Eureka Server)
1. At the core of the architecture is the Eureka server, which acts as the service registry.
2. The Eureka server maintains a registry of all the services in your microservices ecosystem.
3. Service instances periodically send heartbeat signals to the server to update their status.
4. The registry contains information such as service names, network locations (host and port), health status, and metadata about each service instance.

*Working of Discovery Server*

![Working of Discovery Server](https://github.com/abhishekjain1416/discovery-service/assets/142833334/a6a513a5-653d-42cf-83d5-aa254650e6a4)

### Service Instances (Eureka Clients)
1. Each service that wants to participate in service discovery is considered an Eureka client.
2. Eureka clients are typically microservices or applications that need to discover and communicate with other services.
3. They register themselves with the Eureka server during startup and send regular heartbeats to maintain their registration.
4. Eureka clients can query the Eureka server to discover other services. They use the Eureka client library to do this, making it easy to locate and communicate with other services.

*Client's Local Copy of Service Registry*

![Client Local Copy of Service Registry](https://github.com/abhishekjain1416/discovery-service/assets/142833334/dc71f6cf-4826-466a-bd30-d0db3ed17da5)

### Service Discovery
1. When a service instance needs to communicate with another service, it queries the Eureka server for the location of that service.
2. The Eureka client library abstracts the complexities of making low-level network requests, making service discovery a seamless process.
3. Service instances can access the registry to find the network location (IP address and port) of the desired service, allowing for dynamic and efficient inter-service communication.

*Communication with Service Discovery*

![Communication with Service Discovery](https://github.com/abhishekjain1416/discovery-service/assets/142833334/3f75be41-566e-45fd-a1cb-9423ced7dc34)
