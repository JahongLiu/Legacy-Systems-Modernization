# Legacy-Systems-Modernization
Modernized legacy enterprise applications into cloud-native microservices

## Part 1: Spring MVC App to Spring Boot
The company, known for running successful fantasy football leagues, is modernizing its intranet, transitioning from outdated web applications running on Tomcat servlet engines to a modern, cloud-based, microservices architecture. This modernization effort includes both hardware and software updates, starting with adopting Spring Boot. The goal is to leverage Spring Boot's benefits, such as bundled dependencies, reduced boilerplate code, and integration with modern frameworks, while decommissioning the old application servers.

The initial task is to migrate a report-generating application, which provides an overview of interesting statistics from previous league seasons, to Spring Boot. This application currently uses Thymeleaf and can be tested with sample data and an internal H2 database. The migration will involve rearchitecting the application to use Spring Boot, facilitating easier and more effective building, testing, and deployment.

## Part 2: Convert an App to RESTful API
The company has successfully migrated its web applications from war-based deployments to self-contained Spring Boot executables. Although Spring Boot provides an embedded application server, the company's applications remain monolithic, causing slow velocity and inflexibility in scaling and resiliency. To modernize, the company is transitioning to a cloud-based microservices architecture, breaking apart monoliths into smaller services using RESTful APIs with JSON.

This modernization now involves converting the report-generating application into a REST-based service. This allows the retention of business logic while enabling a separate team to develop a modern frontend. The application, testable with sample data and an internal H2 database, is ready for this migration. The focus now shifts to building the service layer as an independent microservice, with reliable deployment being addressed in future steps.

## Part 3: Containerize with Docker
The company has migrated all of its web applications away from war-based deployments onto servlet and application servers and into self-contained Spring Boot executables. Spring Boot is architected so that instead of having an application server run the application, the application runs an application server (by default, for Spring Boot, that embedded application server is Apache Tomcat). You have further started splitting up the application into microservices, with the frontend being developed by a separate team. You and your colleagues are working on modernizing the service layer, in which all the business logic and data are maintained. So far, you have exposed these via a REST API, running locally on a test server. Now it’s time to start putting the project into containers.

“Why?”

Containers make it easy to scale: Containers, because they are not entire machines (physical or virtual), can be started (and stopped) quickly. They also provide isolation from other containers.

Because of this, containers are a step toward cloud-based deployment. And docker-compose is a great tool for seeing how your containerized applications and services interact.

## Part 4: Deploy in Kubernetes
“Why?” 

Kubernetes is the most popular orchestration framework for cloud-based applications and microservices. It runs on all public infrastructures, like Alibaba and Azure.

Kubernetes runs containers. Containers make it easy to scale; because they are not entire machines (physical or virtual), they can be started (and stopped) quickly. They also provide isolation from other containers. And Kubernetes doesn’t just start and stop containers; it manages their entire lifecycle.


