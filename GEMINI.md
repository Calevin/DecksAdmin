# DecksAdmin - GEMINI Context

## 🎯 Project Overview
DecksAdmin is a specialized TCG (Trading Card Game) inventory and deck builder application focused on the "Mitos y Leyendas" card game. It aims to provide a modern interface for managing physical card collections and building competitive decks according to standard game rules.

The project is designed as a full-stack application with a clear separation between a Java-based backend and a React-based frontend.

## 🛠 Tech Stack
- **Backend:** Java 25 (LTS), Spring Boot 3.4+, Spring Data JPA, Hibernate.
- **Security:** JWT-based Authentication and Authorization (Users and Roles).
- **Frontend:** React 18/19 (Vite), TypeScript, Tailwind CSS, Shadcn/ui.
- **Database:** PostgreSQL 16 (running in Docker).
- **Architecture:** Standard Layered Architecture (Controller -> Service -> Repository).
- **Environment:** Local Development (Arch Linux) and Production (Ubuntu Server) utilizing Docker and Docker Compose.

## 🚀 Building and Running

### Prerequisites
- Docker & Docker Compose
- Java 25 JDK
- Node.js (Latest LTS)
- Maven (or use provided wrapper after scaffolding)

### Infrastructure
The application is intended to run seamlessly in both Local (Development on Arch Linux) and Production (personal Ubuntu Server) environments via Docker and Docker Compose. Environment configurations must be decoupled and handled carefully.

Start the PostgreSQL database and pgAdmin (Local):
```bash
docker-compose up -d
```

### Backend (Planned)
Navigate to `backend/` and run:
```bash
./mvnw spring-boot:run
```
*Note: Scaffolding is pending. Dependencies include: Web, Data JPA, PostgreSQL, Validation, Lombok, Security (JWT).*

### Frontend (Planned)
Navigate to `frontend/` and run:
```bash
npm install
npm run dev
```
*Note: Scaffolding is pending. Use Vite with React and TypeScript.*

## 📝 Development Conventions

### Testing
- **Coverage Requirement:** All new features or updates must be accompanied by their respective unit and integration tests.

### Backend (Java 25+)
- **Modern Features:** Use `Records` for DTOs. Use `var` for local variables. Leverage Pattern Matching and Switch Expressions.
- **Persistence:** Use `Snake_case` for database names and `CamelCase` for Java entities/properties.
- **Naming:** Follow "Mitos y Leyendas" domain logic for entity names (e.g., `Aliado`, `Totem`, `Talisman`, `Oro`, `Arma`).

### Frontend (React + TypeScript)
- **Component Style:** Use Functional Components only.
- **State Management:** Prioritize React Hooks (`useState`, `useEffect`, `useMemo`).
- **Typing:** Strict TypeScript types are mandatory for all components and data structures.
- **UI:** Use Tailwind CSS for styling and Shadcn/ui for consistent components.

### Documentation & Use Cases
- **BDD / Features:** Project use cases will be defined using `.feature` files conforming to the Gherkin format, located in the `docs/features/` directory.

## 🗂 Domain Specifics (Mitos y Leyendas)
- **Cards:** Name, Edition, Rarity, Type (Aliado, etc.), Cost, Strength (for Aliados), Ability text.
- **Inventory:** Tracking of physical copies owned.
- **Decks:** Standard collection of 50 cards following MyL deck-building rules.
