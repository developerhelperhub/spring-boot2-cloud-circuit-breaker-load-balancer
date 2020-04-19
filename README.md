# Spring Boot 2.2.5 Cloud Circuit Breaker and Load Balancer

This repository contains the spring boot cloud Circuit breaker and load balancer implementation. This example is continuation of the [Cloud Zuul API Gateway](https://github.com/developerhelperhub/spring-boot2-cloud-netflix-api-gateway) example. I would suggest, please look previous implementation before looking this source code.

In this example, I am using the use case is pull the data from ```inventory-service``` to ```sales-service``` through rest API. In this case, we face the cascade failures if the ```inventory-service``` failed. As per my understanding, in this use case, we can handle to kind of approach when we call the rest API from once service to another service, one is retry mechanism and another one is circuit breaker. In this example, I am using circuit breaker implementation because, I am assuming that, if the ```inventory-service``` service is failing more than one minute, my client should not face communication failures and ```sales-serivce``` should handle this issue and send the correct response back to the client. 

In this cases ```inventory-service``` failied, the circuit breaker will open, if the failure is reached the partiular threshold, and redirect the API call into callback method in the ```seales-service```. Once ```inventory-service``` is working fine, then circuit breaker will close and the API communication will start work.

We need to implement the API communication from ```inventory-service``` to ```sales-service``` before jumping into the cuircute breaker code implementation. 

### Code changes in the inventory-service.



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
