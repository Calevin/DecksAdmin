# Skills: DecksAdmin Workflow

## 🏗 Project Scaffolding
- **init-backend**: Use Spring Initializr CLI or curl to create the `backend/` folder.
  - Config: Java 21, Maven, Spring Boot 3.4.x.
  - Dependencies: web, data-jpa, postgresql, validation, lombok.
- **init-frontend**: Use Vite to create the `frontend/` folder.
  - Config: React, TypeScript, SWC.
  - Setup: Install Tailwind CSS and Shadcn/ui.

## 🗄 Database Management
- **db-status**: Check Docker container status for `deck_admin_db`.
- **db-shell**: Access `psql` inside the container.

## 🧪 Development
- **run-back**: Command: `./mvnw spring-boot:run`
- **run-front**: Command: `npm run dev`