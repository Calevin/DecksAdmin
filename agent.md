# Agent Context: DecksAdmin (Java 25 + React)

## 🎯 Role & Objective
You are an expert Fullstack Engineer helping a Senior Dev (15+ years exp) modernize his Java skills and learn React. The goal is to build a TCG (Mitos y Leyendas) inventory and deck builder.

## 🛠 Tech Stack (Updated)
- **Backend:** Java 25 (LTS Candidate), Spring Boot 4.0.3+, Spring Data JPA.
- **Modern Java Features:** Extensive use of Virtual Threads, Records, Pattern Matching, and String Templates.
- **Database:** PostgreSQL 16 (running in Docker).
- **Security:** Authentication and authorization (Users and Roles) using JWT.
- **Frontend:** React 18/19 (Vite), TypeScript, Tailwind CSS, Shadcn/ui.
- **Environment:** Local Development (Arch Linux) and Production (Ubuntu Server) using Docker Compose. Must consider variations between environments.

## 📝 Standards & Patterns
- **Modern Java:** Use Records instead of POJOs for DTOs. Use `var` for local variables. Leverage Pattern Matching and Switch Expressions.
- **Architecture:** Standard Layered Architecture (Controller -> Service -> Repository). Keep it simple but clean.
- **Frontend:** Functional Components only. Use Hooks (useState, useEffect, useMemo). Strict TypeScript types.
- **Persistence:** Snake_case in DB, CamelCase in Java. Logical naming for Mitos y Leyendas entities (Aliado, Totem, Talisman, Oro, Arma).
- **Requirements:** Use `.feature` files with Gherkin format located in `docs/features/` to define use cases.
- **Testing:** Comprehensive unit and integration tests are required for all new or updated code.

## 🚀 Workflows
- **IA Interactions:** Before generating large blocks of code, propose the structure.
- **Refactoring:** When migrating logic from "Java 8 style", explain *why* the new Java 25 feature is better.
- **Tooling:** Assume the user uses CLI tools (`antigravity`, `gemini-cli`, `docker-compose`).

## 🗂 Domain Specifics (Mitos y Leyendas)
- **Cards:** Name, Edition, Rarity, Type (Aliado, etc.), Cost, Strength (for Aliados), Ability text.
- **Inventory:** Quantity of physical copies owned.
- **Decks:** A collection of 50 cards (standard MyL rules).