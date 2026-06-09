# Modernization Plan: Acme Catalog Azure Modernization

**Project**: acme-catalog

---

## Technical Framework

- **Language**: Java 17
- **Framework**: Spring Boot 3.0.0
- **Build Tool**: Gradle 7.5.1 wrapper
- **Database**: H2 (in-memory default), PostgreSQL runtime dependency
- **Key Dependencies**: Spring Data JPA, Eureka client, Azure Spring starters

---

## Overview

> This modernization updates the acme-catalog application to align with the
> project rulebook for Java modernization to Azure. The application currently
> runs on Java 17 and does not yet have an explicit rulebook-scoped migration
> plan for Azure storage/authentication guardrails.
>
> The new architecture will:
>
> - Upgrade the runtime baseline to Java 21 LTS for target-state consistency
> - Standardize Azure authentication and secret handling guardrails
> - Define Azure Blob storage modernization scope with private-access controls
>
> The migration follows a phased approach: runtime upgrade, Azure service
> modernization tasks, infrastructure policy alignment, and security validation.

---

## Migration Impact Summary

| Application | Original Service | New Azure Service | Authentication | Comments |
|-------------|------------------|-------------------|----------------|----------|
| acme-catalog | Java 17 runtime baseline | Java 21 LTS baseline | N/A | Align to target framework policy |
| acme-catalog | AWS/S3-style object storage patterns | Azure Blob Storage | DefaultAzureCredential + Managed Identity | Remove AWS dependency paths |
| acme-catalog | Ad-hoc secret/config handling | Azure Key Vault + env vars | Managed Identity in prod | No hardcoded credentials |

---

## Open Questions & Questionnaire

- [x] Q: What is the modernization goal? → A: Modernize the app
- [x] Q: What language scope applies? → A: Java
- [x] Q: Which plan folder/name should be used? → A: `.github/modernize/planii`
- [x] Q: Should rulebook compliance validation be included? → A: Yes
- [ ] Which Azure region and subscription should infrastructure target?
- [ ] Should deployment automation be included in this plan iteration?
