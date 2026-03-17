# auth-server

Spring Boot-based OAuth2 Authorization Server for issuing tokens and handling authorization flows.

## Stack
- Java 25
- Spring Boot 4.0.3
- Spring Security + OAuth2 Authorization Server
- Maven

## Project Structure
- `src/main/java/org/kiroff/auth_server/oauth/AuthServerApplication.java` - application entry point
- `src/main/resources/application.yaml` - application configuration

## Running Locally
```bash
./mvnw spring-boot:run
```

## Tests
```bash
./mvnw test
```

## Configuration
Minimal configuration is in `application.yaml`:

```yaml
spring:
  application:
    name: auth-server
```

Additional authorization server configuration (clients, keys, endpoints) should be added under `src/main/resources` or Java configuration as needed.

## Build
```bash
./mvnw clean package
```

## Notes
The POM pins Spring Boot 4.0.3 and Spring Cloud 2025.1.1, and sets Java 25 as the target. It also enables additional JVM arguments for native access and ByteBuddy.
