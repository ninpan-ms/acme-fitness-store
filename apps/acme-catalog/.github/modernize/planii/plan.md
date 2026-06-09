# Modernization Plan: planii

**Project**: acme-catalog

---

## Technical Framework

- **Language**: Java 17 (target: Java 21 LTS)
- **Framework**: Spring Boot (with Spring Data JPA, Spring Cloud Azure)
- **Build Tool**: Gradle
- **Database**: PostgreSQL (via Azure JDBC with managed identity)
- **Key Dependencies**: Spring Boot Actuator, Spring Data JPA, Spring Cloud Azure Key Vault Secrets, Spring Cloud Azure JDBC PostgreSQL, Flyway, Eureka Client

---

## Overview

> This migration modernizes the acme-catalog Java application to align with enterprise Azure modernization policy. The application currently runs on Java 17 with Spring Boot and uses Azure services (Key Vault, PostgreSQL). The new architecture will:
>
> - Upgrade the Java runtime from 17 to 21 LTS as mandated by the enterprise modernization charter
> - Remediate known security vulnerabilities (CVEs) in project dependencies to ensure the application is secure
>
> The migration follows a Refactor strategy: upgrading the Java runtime to the required LTS version and performing security hardening before deployment.

---

## Migration Impact Summary

| Application   | Original Service | New Azure Service | Authentication    | Comments                                  |
|---------------|-----------------|-------------------|-------------------|-------------------------------------------|
| acme-catalog  | Java 17          | Java 21 LTS       | Managed Identity  | Upgrade Java runtime to enterprise LTS    |
| acme-catalog  | Existing deps    | Patched deps      | Managed Identity  | CVE remediation for all project dependencies |

---

## Task List

| # | Task ID                        | Type    | Description                                              |
|---|-------------------------------|---------|----------------------------------------------------------|
| 1 | 001-upgrade-java-21           | upgrade | Upgrade Java runtime from 17 to 21 LTS                   |
| 2 | 002-security-cve-remediation  | security| Scan and remediate CVEs in all project dependencies      |
