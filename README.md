# API Gateway

This is a Gateway for safely routing to APIs in ResourceServer, Photos and Albums microservices with authentication using oauth2.


This project has basic APIs which can only be accessed after proving authorized access token in the headers of the request URI.

**Keycloak** authorization server is used to first generate a token from the credentials, then that code is exchanged with
an access token which can further be used for APIs.


## Ports
- API Gateway: 8084
- keycloak server: 8081
- Spring Boot Resource Server: 8082
- Spring Boot Photos Server: 8090
- Spring Boot Albums Server: 8091


Note: To start the keycloak server type the following commands:
- kc.bat (./kc.sh in Linux or macOS) start-dev (simpl start for prod anvironment)--http-port=8820 (optional)
