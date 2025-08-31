# Microservices Asynchronous Communication using RabbitMQ

A **production-grade blog platform** built with **Spring Boot**, **Spring Cloud**, and **RabbitMQ** for **event-driven architecture**.

---

## Features
- **Async communication** via RabbitMQ
- **Service discovery** with Eureka
- **API Gateway** with Spring Cloud Gateway
- **Declarative clients** with Feign
- **Dockerized** with PostgreSQL, Zipkin, and RabbitMQ
- **CRUD operations** on articles and comments

---

## Services
| Service | Role |
|--------|------|
| `article` | Create & manage blog posts |
| `comment` | Add comments to articles |
| `notification` | Send async notifications |
| `gatewayApi` | Route all HTTP requests |
| `eureka-server` | Register and discover services |

---

## Run Locally

```bash
# Start infrastructure
docker-compose up -d

# Run a service
./mvnw spring-boot:run -pl article

--

## Run Locally 

bashcurl -X POST http://localhost:8080/article/api/articles \
  -H "Content-Type: application/json" \
  -d '{"title":"My Journey with Microservices","body":"Today I built..."}'




## Tech Stack

Java 17
Spring Boot 3
Spring Cloud (Eureka, Gateway, Feign)
RabbitMQ
PostgreSQL
Zipkin (distributed tracing)
Maven



