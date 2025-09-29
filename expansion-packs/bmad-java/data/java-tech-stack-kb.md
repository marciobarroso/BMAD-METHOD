# Java Tech Stack Knowledge Base

## Java 21 Features

### Language Features

- **Pattern Matching**: Enhanced switch expressions and pattern matching
- **Records**: Immutable data carriers
- **Sealed Classes**: Restricted class hierarchies
- **Text Blocks**: Multi-line string literals
- **Local Variable Type Inference**: `var` keyword
- **Virtual Threads**: Lightweight concurrency
- **Foreign Function & Memory API**: Interop with native code

### Performance Improvements

- **ZGC**: Low-latency garbage collector
- **Shenandoah**: Concurrent garbage collector
- **JIT Compiler**: Enhanced optimization
- **Memory Management**: Improved heap management

## Spring Boot Ecosystem

### Core Modules

- **Spring Boot Starter Web**: Web applications and REST APIs
- **Spring Boot Starter Security**: Authentication and authorization
- **Spring Boot Starter Data JPA**: Data persistence with JPA
- **Spring Boot Starter Test**: Testing framework integration
- **Spring Boot Starter Actuator**: Production-ready features

### Spring Cloud Modules

- **Spring Cloud Gateway**: API Gateway
- **Spring Cloud Netflix**: Service discovery and load balancing
- **Spring Cloud Config**: Configuration management
- **Spring Cloud Sleuth**: Distributed tracing
- **Spring Cloud Stream**: Event-driven microservices

## Maven Configuration

### Project Structure

```
project/
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   └── test/
│       ├── java/
│       └── resources/
├── pom.xml
└── README.md
```

### Essential Plugins

- **maven-compiler-plugin**: Java compilation
- **maven-surefire-plugin**: Unit testing
- **maven-failsafe-plugin**: Integration testing
- **spring-boot-maven-plugin**: Spring Boot packaging
- **dockerfile-maven-plugin**: Docker image building

## AWS Services

### Compute Services

- **Amazon EC2**: Virtual machines
- **AWS Lambda**: Serverless compute
- **Amazon ECS**: Container service
- **Amazon EKS**: Kubernetes service
- **AWS Fargate**: Serverless containers

### Database Services

- **Amazon RDS**: Relational databases
- **Amazon Aurora**: MySQL/PostgreSQL compatible
- **Amazon DynamoDB**: NoSQL database
- **Amazon DocumentDB**: MongoDB compatible

### Networking & Security

- **Amazon VPC**: Virtual private cloud
- **AWS API Gateway**: API management
- **AWS Load Balancer**: Traffic distribution
- **AWS IAM**: Identity and access management
- **AWS Secrets Manager**: Secrets management

### Monitoring & Logging

- **Amazon CloudWatch**: Monitoring and logging
- **AWS X-Ray**: Distributed tracing
- **Amazon CloudTrail**: API logging
- **AWS Config**: Resource configuration

## Best Practices

### Java 21 Development

- Use modern Java features (records, pattern matching)
- Implement proper exception handling
- Follow naming conventions
- Use immutable objects when possible
- Optimize for performance

### Spring Boot Development

- Use Spring Boot starters for dependencies
- Implement proper configuration management
- Use Spring profiles for environment-specific config
- Implement proper error handling
- Use Spring Boot Actuator for monitoring

### Maven Best Practices

- Use dependency management for version control
- Implement proper plugin configuration
- Use profiles for different environments
- Implement proper testing configuration
- Use Maven wrapper for consistent builds

### AWS Best Practices

- Design for failure and scalability
- Implement proper security practices
- Use AWS managed services when possible
- Implement proper monitoring and logging
- Optimize for cost and performance
