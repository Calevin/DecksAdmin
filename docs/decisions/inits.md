# Project Initialization Decisions

This document records the initial setup and configuration decisions for the DecksAdmin project.

## 1. Backend Initialization (Java/Spring Boot)

The backend was scaffolded as a modern Spring Boot application to handle business logic, deck-building rules, and collection management.

- **Build Tool:** Maven
- **Java Version:** 25 (LTS)
- **Spring Boot Version:** 4.0.3
- **Core Dependencies:**
    - `spring-boot-starter-webmvc`: For RESTful API development.
    - `spring-boot-starter-data-jpa`: For persistence via Hibernate.
    - `postgresql`: Runtime driver for PostgreSQL connectivity.
    - `spring-boot-starter-validation`: For robust input data integrity.
    - `lombok`: To minimize boilerplate code (getters, setters, etc.).
- **Rationale:** Choosing Java 25 ensures access to the latest JVM features (like advanced Pattern Matching and Records) while Spring Boot 4 provides a cutting-edge foundation for the application lifecycle.

## 2. Frontend Initialization (React/Vite)

The frontend was initialized using Vite for a fast, modern development experience with strict type safety.

- **Scaffolding Tool:** `create-vite`
- **Library:** React 19
- **Language:** TypeScript (Strict)
- **Initialization Command:**
  ```bash
  npm create vite@latest frontend -- --template react-ts
  ```
- **Key Dev Tools:**
    - `vite`: Fast HMR and build optimization.
    - `eslint`: Configured for React Hooks and TypeScript best practices.
- **Rationale:** Vite's performance significantly outperforms traditional tools like Create React App. React 19 was selected to leverage the latest UI patterns and performance improvements.

## 3. Infrastructure & Environment

- **Database:** PostgreSQL 16 (Containerized via Docker).
- **Orchestration:** Docker Compose is used to manage the database and administrative tools (pgAdmin) to ensure environment consistency across different development machines.
- **Project Structure:** A monorepo-style approach with clear separation between `backend/` and `frontend/` directories.

---
*Last Updated: March 6, 2026*
