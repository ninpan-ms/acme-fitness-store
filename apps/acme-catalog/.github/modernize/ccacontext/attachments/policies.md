# Policies

Enforceable standards and hard boundaries for Java modernization. Every policy here is validatable against generated artifacts.

## Security Requirements

### Authentication & Authorization

- Use `DefaultAzureCredential` for all Azure service authentication.
- Use managed identity in production environments.

### Secrets Management

- Connection strings must come from environment variables.
- No hardcoded keys or credentials in code.

### Encryption

- Enable Azure Storage encryption at rest for all blob storage.

## Guardrails (Hard Boundaries)

### Prohibited Technologies

| Technology | Reason | Approved Alternative |
|-----------|--------|---------------------|
| AWS S3 SDK | Migration target is Azure | com.azure:azure-storage-blob |
| AWS credentials in code | Post-migration prohibition | DefaultAzureCredential / managed identity |

### Prohibited Patterns

| Pattern | Reason | Approved Alternative |
|---------|--------|---------------------|
| Hardcoded connection strings | Security risk | Environment variables |
| Direct S3 API calls | AWS dependency | Azure Blob Storage SDK equivalents |

### Required Elements

Every modernized application must include:

#### Cloud Resources

- All blob containers must be configured with **private** access level.

#### Authentication

- `DefaultAzureCredential` for Azure service authentication.
- Managed identity enabled in production.

## Validation & Quality Gates

### Pipeline Gates

- Unit tests required for all migrated storage operations.
- Minimum 80% code coverage on new/migrated code.

## Coding Style Guidelines

### Java

- Follow Azure SDK best practices for retry and error handling.
- Use async APIs where available.
