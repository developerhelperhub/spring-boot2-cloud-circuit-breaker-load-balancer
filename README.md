# Spring Boot 2.2.5 Cloud Circuit Breaker and Load Balancer

This repository contains the spring boot cloud Circuit breaker and load balancer implementation. This example is continuation of the [Cloud Zuul API Gateway](https://github.com/developerhelperhub/spring-boot2-cloud-netflix-api-gateway) example. I would suggest, please look previous implementation before looking this source code.

#### Note : Implementation not completed, only implemented done in the sales-service for the rest API communciation call from inventory-service.

#### Below implementation coming soon...
* Circuit breaker
* Documentation


This repository contains seven maven project. 
* my-cloud-service: Its main module, it contains the dependecy management of our application.
* my-cloud-discovery-service: This is the server for the discovery service.
* identity-service: This authentication server service. 
* client-application-service: This client application for authentication server.
* inventory-service: This is one of the microservice which is called inventory service to manage the inventory in the project.
* sales-service: This is one of the microservice which is called sales service to manage the point of sales in the project.

### Reference
* [Spring boot circuit breaker](https://cloud.spring.io/spring-cloud-netflix/2.2.x/reference/html/#circuit-breaker-spring-cloud-circuit-breaker-with-hystrix)
* [Rest template implementation](https://spring.io/blog/2015/01/20/microservice-registration-and-discovery-with-spring-cloud-and-netflix-s-eureka)
* [Oauth Scope Security](https://docs.spring.io/spring-security-oauth2-boot/docs/current/reference/htmlsingle/)
