# === Development Stage ===
FROM eclipse-temurin:21-jdk-alpine AS dev
WORKDIR /app
# We use volume mounting in local dev, so these are just for initial setup or fallback
COPY .mvn/ .mvn
COPY mvnw pom.xml ./
# Resolve dependencies to speed up subsequent runs
RUN ./mvnw dependency:go-offline
COPY src ./src
EXPOSE 8080
# Run spring boot with hot reload (devtools if added)
CMD ["./mvnw", "spring-boot:run"]

# === Build Stage ===
FROM eclipse-temurin:21-jdk-alpine AS build
WORKDIR /app
COPY .mvn/ .mvn
COPY mvnw pom.xml ./
RUN ./mvnw dependency:go-offline
COPY src ./src
# Build the application skipping tests
RUN ./mvnw clean package -DskipTests

# === Production Stage ===
FROM eclipse-temurin:21-jre-alpine AS prod
WORKDIR /app
# Copy the compiled jar from the build stage
COPY --from=build /app/target/*.jar app.jar
EXPOSE 8080
# Run the application
CMD ["java", "-jar", "app.jar"]
