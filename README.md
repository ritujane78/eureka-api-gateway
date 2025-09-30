# API Gateway - Eureka

## Versions
- Java: 21
- Spring Boot: 3.5.6
- Spring Cloud: 2025.0.0
- 

This is a Gateway for safely routing to APIs in EurekaResourceServer microservice with authentication using oauth2.

**Keycloak** authorization server is used to first generate a token from the credentials, then that code is exchanged with
an access token which can further be used for APIs.

Blockage of http requests through CORS is also handled.


## Ports
- API Gateway: 8084
- keycloak server: 8081
- Spring Boot Resource Server: Random port number

Note: To start the keycloak server type the following commands:
- kc.bat (./kc.sh in Linux or macOS) start-dev (simpl start for prod anvironment)--http-port=8820 (optional)
