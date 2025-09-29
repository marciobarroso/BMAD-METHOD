# 🚀 BMAD Java Development Studio

Um framework abrangente de desenvolvimento Java alimentado por IA para criar aplicações Java modernas e modernizar sistemas legados. Focado em Java 21, Spring Boot ecosystem, Maven, e plataforma AWS cloud.

## 📋 Visão Geral

Este expansion pack fornece tudo que é necessário para desenvolvimento Java moderno, tanto para criação de novos projetos quanto para modernização de sistemas legados. Construído especificamente para desenvolvimento Java enterprise com tecnologias modernas, inclui agentes especializados em IA, workflows de desenvolvimento e modernização, padrões de arquitetura moderna e desenvolvimento orientado a testes.

## ✨ Funcionalidades

### 🤖 Agentes Especializados em IA

- **Java Architect** 🏗️ - Especialista em arquitetura Java 21, Spring Boot e AWS
- **Spring Boot Developer** 🌱 - Desenvolvedor especializado em Spring Boot ecosystem
- **AWS Cloud Engineer** ☁️ - Engenheiro especializado em AWS cloud platform

### 🔄 Workflows de Desenvolvimento

#### 🆕 Workflows Greenfield (Novos Projetos)

- **Java Web Project** - Criação de aplicações web Java com Spring Boot MVC
- **Java API Project** - Desenvolvimento de APIs REST com Spring Boot Web
- **Java Microservice** - Arquitetura de microserviços com Spring Cloud

#### 📈 Workflows Brownfield (Modernização)

- **Java Version Modernization** - Migração entre versões Java (ex: Java 8 → Java 21)
- **Build System Modernization** - Migração para Maven como gestor de pacotes
- **Application Server to Container** - Migração de WebLogic para containers
- **Cloud Migration** - Migração para ambiente AWS distribuído

## 🛠️ Tech Stack Recomendado

### Tecnologias Centrais

- **Java 21** - Versão LTS mais recente
- **Spring Boot 3.x** - Framework moderno para aplicações Java
- **Spring Ecosystem** - MVC, Security, Data JPA, Cloud
- **Maven** - Gestor de pacotes e build automation
- **AWS** - Plataforma cloud para deploy e infraestrutura

### Stack Completo

```
Java 21
├── Spring Boot 3.x
│   ├── Spring MVC (Web)
│   ├── Spring Security (Auth)
│   ├── Spring Data JPA (Persistence)
│   └── Spring Cloud (Microservices)
├── Maven (Build)
├── AWS Cloud Platform
│   ├── EKS/ECS (Containers)
│   ├── RDS/Aurora (Database)
│   ├── API Gateway (APIs)
│   └── CloudWatch (Monitoring)
└── Docker (Containerization)
```

## 🚀 Início Rápido

### Para Novos Projetos (Greenfield)

#### Aplicação Web Java

```bash
# Criar projeto web com Spring Boot MVC
bmad-java java-web-project-greenfield
```

#### API REST Java

```bash
# Desenvolver API REST com Spring Boot Web
bmad-java java-api-project-greenfield
```

#### Microserviços Java

```bash
# Criar arquitetura de microserviços
bmad-java java-microservice-greenfield
```

### Para Modernização (Brownfield)

#### Migração de Versão Java

```bash
# Migrar de Java 8 para Java 21
bmad-java java-version-modernization
```

#### Migração para Maven

```bash
# Migrar build system para Maven
bmad-java build-system-modernization
```

#### Migração de WebLogic para Containers

```bash
# Migrar de WebLogic para containers AWS
bmad-java application-server-to-container
```

#### Migração para AWS Cloud

```bash
# Migrar aplicação para AWS cloud
bmad-java cloud-migration
```

## 🏗️ Arquiteturas Suportadas

### 🆕 Projetos Greenfield

#### Aplicação Web Tradicional

- **Frontend**: Thymeleaf, React, Vue.js, Angular
- **Backend**: Spring Boot MVC, Spring Security
- **Database**: PostgreSQL, MySQL, Amazon RDS
- **Deploy**: AWS ECS/EKS, Docker

#### API REST

- **Framework**: Spring Boot Web
- **Documentação**: OpenAPI/Swagger
- **Security**: JWT, OAuth2, AWS Cognito
- **Database**: Spring Data JPA, Amazon RDS
- **Deploy**: AWS API Gateway, Lambda, ECS

#### Microserviços

- **Framework**: Spring Boot + Spring Cloud
- **Discovery**: Eureka, Consul, AWS Service Discovery
- **Gateway**: Spring Cloud Gateway, AWS API Gateway
- **Communication**: REST, Message Queues, Event-Driven
- **Deploy**: AWS EKS, Service Mesh

### 📈 Modernização Brownfield

#### Migração de Versão Java

- **De**: Java 8, 11, 17
- **Para**: Java 21 LTS
- **Estratégias**: Big Bang, Incremental, Blue-Green
- **Validação**: Testes, Performance, Segurança

#### Migração para Maven

- **De**: Ant, Gradle, Ivy
- **Para**: Maven 3.9+
- **Features**: Dependency Management, Build Automation
- **CI/CD**: GitHub Actions, AWS CodePipeline

#### Migração de Application Server

- **De**: WebLogic, JBoss, Tomcat
- **Para**: Spring Boot Embedded Server
- **Containerização**: Docker, Kubernetes
- **Cloud**: AWS EKS, ECS, Fargate

#### Migração para Cloud

- **De**: On-premise, Data Center
- **Para**: AWS Cloud Platform
- **Estratégias**: Lift & Shift, Replatform, Refactor
- **Services**: EC2, Lambda, RDS, S3, CloudWatch

## 📚 Documentação

### Conceitos Centrais

- [Java 21 Features](docs/java-21-features.md)
- [Spring Boot Best Practices](docs/spring-boot-practices.md)
- [Maven Configuration](docs/maven-configuration.md)
- [AWS Architecture Patterns](docs/aws-patterns.md)

### Guias de Desenvolvimento

- [Getting Started](docs/getting-started.md)
- [Development Workflow](docs/development-workflow.md)
- [Testing Strategy](docs/testing-strategy.md)
- [Deployment Guide](docs/deployment-guide.md)

## 🎯 Casos de Uso

### 🆕 Cenários Greenfield

#### Startup Tech

- **Problema**: Criar MVP rápido com Java moderno
- **Solução**: `java-web-project-greenfield` + AWS
- **Resultado**: Aplicação web moderna em produção

#### Enterprise API

- **Problema**: Desenvolver API para integração
- **Solução**: `java-api-project-greenfield` + AWS API Gateway
- **Resultado**: API REST documentada e escalável

#### Microserviços Platform

- **Problema**: Arquitetura distribuída escalável
- **Solução**: `java-microservice-greenfield` + AWS EKS
- **Resultado**: Plataforma de microserviços cloud-native

### 📈 Cenários Brownfield

#### Legacy Java Upgrade

- **Problema**: Java 8 → Java 21
- **Solução**: `java-version-modernization`
- **Resultado**: Aplicação moderna com performance melhorada

#### Build System Migration

- **Problema**: Ant → Maven
- **Solução**: `build-system-modernization`
- **Resultado**: Build automation e dependency management

#### WebLogic to Cloud

- **Problema**: WebLogic → Containers AWS
- **Solução**: `application-server-to-container`
- **Resultado**: Aplicação containerizada e cloud-native

#### On-premise to Cloud

- **Problema**: Data Center → AWS Cloud
- **Solução**: `cloud-migration`
- **Resultado**: Infraestrutura cloud escalável e otimizada

## 🏷️ Versão

**Versão Atual:** 1.0.0

**Compatibilidade:**

- Java 21 LTS
- Spring Boot 3.x
- Maven 3.9+
- AWS Cloud Platform

---

Construído com ❤️ usando o framework BMAD Method.
