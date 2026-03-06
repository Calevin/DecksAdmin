# Skills: DecksAdmin Workflow

## 🏗 Project Scaffolding
- **init-backend**: Use Spring Initializr CLI or curl to create the `backend/` folder.
  - Config: Java 25, Maven, Spring Boot 4.0.3.
  - Dependencies: web, data-jpa, postgresql, validation, lombok, security.
- **init-frontend**: Use Vite to create the `frontend/` folder.
  - Config: React, TypeScript, SWC.
  - Setup: Install Tailwind CSS and Shadcn/ui.

## 🗄 Database Management
- **db-status**: Check Docker container status for `deck_admin_db`.
- **db-shell**: Access `psql` inside the container.

## 🧪 Development
- **run-back**: Command: `./mvnw spring-boot:run`
- **run-front**: Command: `npm run dev`
- **test-back**: Command: `./mvnw test`
- **test-front**: Command: `npm run test`

## 📝 Use Cases
- **features**: Write use cases in `.feature` files using Gherkin format located in `docs/features/`.

## 🚀 Deployment / Operations
- **run-docker-dev**: Command: `docker-compose -f docker-compose.yml -f docker-compose.dev.yml up -d` (Para desarrollo local con hot-reload e interfaz DB expuesta).
- **run-docker-prod**: Command: `docker-compose up -d` (Para levantar producción completo en Ubuntu Server).