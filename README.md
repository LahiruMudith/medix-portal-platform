# CMS Platform Services

## Student Information
- **Name:** Lahiru Mudith
- **Student Number:** CMS-ST-2026
- **GCP Project ID:** cms-cloud-architecture

## Description
This repository contains the core platform and infrastructure microservices for the Clinic Management System. It includes the Spring Cloud Config Server for centralized external configuration, Netflix Eureka Service Registry for service discovery, and Spring Cloud API Gateway for intelligent routing and global CORS handling.

## Technology Stack
- Java 25 / Spring Boot 3.4.3
- Spring Cloud 2024.0.0
- Spring Cloud Config Server
- Spring Cloud Netflix Eureka Server
- Spring Cloud Gateway (Reactive WebFlux)
- PM2 (process management)

## Setup / Getting Started
1. Build all platform services:
   ```bash
   cd config-server && mvn clean package -DskipTests && cd ..
   cd service-registry && mvn clean package -DskipTests && cd ..
   cd api-gateway && mvn clean package -DskipTests && cd ..
   ```
2. Start all platform components using PM2:
   ```bash
   pm2 start ecosystem.config.js
   ```

## Platform Components
| Component | Port | Description |
|-----------|------|-------------|
| config-server | 8888 | Centralized configuration management |
| service-registry | 8761 | Eureka service registration & discovery |
| api-gateway | 7000 | Reverse proxy, routing, and CORS handling |
