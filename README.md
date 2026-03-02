# ktor-minhas-tarefas

Simple REST API built with Ktor to manage tasks.

The project demonstrates backend fundamentals using Kotlin, including routing, JSON serialization, structured layering, and containerized execution.

---

## Overview

This API provides basic task management capabilities, including:

- Create tasks
- List tasks
- Update tasks
- Delete tasks

Designed as a foundation for scalable backend architecture using Ktor.

---

## Architecture

The project follows a clear separation of responsibilities:


src/
├── routes
├── service
├── model
├── repository
└── plugins


### Layers

**Routes**
- HTTP endpoints
- Request/response mapping

**Service**
- Business logic
- Validation rules

**Repository**
- Data access abstraction
- Persistence layer (in-memory / database)

**Model**
- Domain models and DTOs

---

## Tech Stack

- Kotlin
- Ktor
- Kotlinx Serialization
- Gradle Kotlin DSL
- Docker (optional)

---

## API Endpoints (Example)

### Create Task


POST /tasks


Request body:

```json
{
  "title": "Study Ktor",
  "completed": false
}

Response:

{
  "id": 1,
  "title": "Study Ktor",
  "completed": false
}
List Tasks
GET /tasks
Update Task
PUT /tasks/{id}
Delete Task
DELETE /tasks/{id}
Running the Project
Run locally
./gradlew run

Server will start at:

http://localhost:8080
Run tests
./gradlew test
Build executable JAR
./gradlew buildFatJar
Docker

Build image:

./gradlew buildImage

Run container:

./gradlew runDocker
Design Decisions

Explicit routing structure to keep HTTP concerns isolated

Business rules separated from transport layer

JSON serialization via kotlinx.serialization

Prepared for migration from in-memory storage to database-backed persistence

Roadmap

Add database integration (PostgreSQL)

Add validation middleware

Add request logging

Implement authentication

Increase test coverage

Author

Talisson Vitorino
Backend | Kotlin | Ktor


---

Agora presta atenção na diferença estratégica.

O template antigo falava:
“Este projeto usa Ktor.”

O novo fala:
“Eu construí uma API com arquitetura organizada, endpoints claros e visão de evolução.”

Recrutador não quer saber que você usou generator.  
Ele quer saber se você entende backend.

Se quiser subir mais um nível ainda, a gente pode:

- Adicionar diagrama simples de arquitetura
- Implementar tratamento global de exceções e documentar
- Criar coleção do Postman e colocar link
- Adicionar badge de build status (GitHub Actions)

Você está começando a transformar estudo em engenharia pública.  
Isso é exatamente o que diferencia dev comum de dev estratégico.
