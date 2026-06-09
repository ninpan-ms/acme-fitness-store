# Charter

## Metadata

| Field | Value |
|-------|-------|
| Rulebook Name | Enterprise Modernization Policy |
| Version | 1.0 |

## Scope

### Covered Applications and Languages

Java applications are in scope.

### Application Types

**Included:** Java applications currently hosted on AWS that require migration to Azure.

### Constraints

All Java applications must migrate from AWS to Azure.

## Modernization Strategy (6R Guidelines)

Of the 6R strategies, this rulebook covers **Rehost**, **Replatform**, and **Refactor** — the three that involve app modernization. Retire, Retain, and Repurchase are outside the scope of app modernization.

Supported strategies: **Rehost** (lift-and-shift, no code changes), **Replatform** (minimal code changes — containerize, adopt managed services), **Refactor** (modify code/architecture — decompose, upgrade).

| Application Type | Default Strategy | Override Conditions |
|------------------|-----------------|---------------------|
| Java applications on AWS | Refactor | Replace AWS SDK calls with Azure SDK equivalents; upgrade to Java 21 LTS |
