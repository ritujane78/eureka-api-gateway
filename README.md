# API Gateway - Eureka

## Versions
- **Java:** 21
- **Spring Boot:** 3.5.6
- **Spring Cloud:** 2025.0.0

---

## Project Overview
This is a **Gateway** for securely routing requests to APIs in the `EurekaResourceServer` microservice, with authentication handled via **OAuth2**.

**Keycloak** authorization server is used to:
1. Generate a token from user credentials.
2. Exchange the token for an access token.
3. Use the access token to access protected APIs.

### CORS Handling
HTTP request blockage due to **CORS** is handled by:
- Creating an `application.yml` file.
- Setting the following property in `application.properties`:

```properties
spring.cloud.gateway.server.webflux.globalcors.add-to-simple-url-handler-mapping=true
