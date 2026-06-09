# Targets

Approved target technologies for Java modernization. Defines *what is approved* — not implementation steps.

## Target Frameworks

| Language | Target Version | Notes |
|----------|---------------|-------|
| Java | 21 LTS | Target for all Java application migrations |

## Target Data Services

| Service | Use When |
|---------|----------|
| Azure Blob Storage | Replacing AWS S3 for object/blob storage |

## Target Libraries

Source → target mappings for Java.

| Category | Source | Target | Notes |
|----------|--------|--------|-------|
| Object Storage SDK | AWS S3 SDK | com.azure:azure-storage-blob (Azure SDK for Java) | All S3 API calls must be replaced with Azure Blob Storage SDK equivalents |
