# Java Microservice Setup Task

## Purpose

Initialize a new Java microservice project using Java 21, Spring Boot, Spring Cloud, Maven, and AWS cloud platform. Creates the foundation for a modern microservice with proper project structure, dependencies, and configuration.

## When to Use

- Starting a new Java microservice project
- Creating a microservice with Spring Boot and Spring Cloud
- Setting up a project for AWS EKS deployment
- Establishing a foundation for microservice development with modern Java

## Input Requirements

- Microservice name and description
- Service responsibilities and boundaries
- Inter-service communication requirements
- Service discovery preferences
- AWS deployment preferences
- Monitoring and observability requirements

## Process Steps

### 1. Project Structure Creation

- Create Maven project structure
- Set up source directories (src/main/java, src/main/resources)
- Set up test directories (src/test/java, src/test/resources)
- Create package structure following microservice conventions
- Initialize Git repository

### 2. Maven Configuration

- Create pom.xml with Java 21 configuration
- Add Spring Boot parent POM
- Add Spring Cloud dependencies
- Configure Maven compiler plugin
- Add Spring Boot Maven plugin
- Configure build profiles (dev, test, prod)
- Set up Maven wrapper

### 3. Spring Boot Configuration

- Add Spring Boot Web starter dependency
- Add Spring Boot Data JPA starter dependency
- Add Spring Boot Security starter dependency
- Add Spring Boot Test starter dependency
- Add Spring Boot Actuator starter dependency
- Add Spring Cloud dependencies
- Configure application.properties/yml

### 4. Spring Cloud Configuration

- Add Spring Cloud Netflix dependencies (Eureka, Gateway)
- Add Spring Cloud Config dependencies
- Add Spring Cloud Sleuth dependencies
- Add Resilience4j dependencies
- Configure service discovery
- Configure API Gateway
- Configure distributed tracing

### 5. Microservice Configuration

- Create main application class
- Configure Spring Boot for microservice
- Set up service discovery client
- Configure circuit breaker
- Set up health checks
- Configure metrics and monitoring
- Set up distributed tracing

### 6. Development Environment Setup

- Configure IDE for Java 21 and Spring Boot
- Set up local development database
- Configure application profiles
- Set up service discovery server locally
- Configure API Gateway locally
- Set up debugging environment

## Output Deliverables

- Complete Maven project structure
- Configured pom.xml with all dependencies
- Spring Boot microservice configuration
- Spring Cloud configuration
- Service discovery setup
- Development environment setup guide
- Basic microservice template
- Git repository with initial commit

## Success Criteria

- Maven project builds successfully
- Spring Boot application starts without errors
- Service discovery registration working
- Health checks accessible
- Metrics and monitoring working
- Development environment fully functional
- All dependencies resolved correctly
- Project ready for microservice development

## Dependencies

- Java 21 JDK installed
- Maven 3.9+ installed
- IDE configured for Java development
- Git repository access
- AWS account (for deployment)
- Service discovery server (Eureka/Consul)

## Tools and Resources

- Maven build tool
- Spring Boot framework
- Spring Cloud
- Java 21 JDK
- IDE (IntelliJ IDEA, Eclipse, VS Code)
- Git version control
- Service discovery tools
- AWS CLI (for deployment)
