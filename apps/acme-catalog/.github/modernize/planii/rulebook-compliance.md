## Rulebook Compliance

| Rulebook | Rule | Status | Task |
|----------|------|--------|------|
| charter.md | Java applications are in scope | ✅ COVERED | 001-upgrade-java-21-lts |
| charter.md | Java apps on AWS requiring Azure migration are included | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| charter.md | All Java applications must migrate from AWS to Azure | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| charter.md | Supported strategy includes Refactor modernization | ✅ COVERED | 001-upgrade-java-21-lts, 002-transform-azure-storage-auth-patterns |
| charter.md | Replace AWS SDK calls with Azure SDK equivalents | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| charter.md | Upgrade Java to 21 LTS | ✅ COVERED | 001-upgrade-java-21-lts |
| policies.md | Use DefaultAzureCredential for Azure authentication | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| policies.md | Use managed identity in production | ✅ COVERED | 002-transform-azure-storage-auth-patterns, 003-infrastructure-blob-private-baseline |
| policies.md | Connection strings must come from environment variables | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| policies.md | No hardcoded keys/credentials in code | ✅ COVERED | 002-transform-azure-storage-auth-patterns, 004-security-rulebook-validation |
| policies.md | Enable Azure Storage encryption at rest | ✅ COVERED | 003-infrastructure-blob-private-baseline |
| policies.md | Prohibit AWS S3 SDK usage | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| policies.md | Prohibit AWS credentials in code | ✅ COVERED | 002-transform-azure-storage-auth-patterns, 004-security-rulebook-validation |
| policies.md | Prohibit hardcoded connection strings | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| policies.md | Prohibit direct S3 API calls | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| policies.md | Blob containers must use private access level | ✅ COVERED | 003-infrastructure-blob-private-baseline |
| policies.md | Unit tests required for migrated storage operations | ✅ COVERED | 004-security-rulebook-validation |
| policies.md | Minimum 80% code coverage on new/migrated code | ✅ COVERED | 004-security-rulebook-validation |
| policies.md | Follow Azure SDK retry/error handling best practices | ✅ COVERED | 004-security-rulebook-validation |
| policies.md | Use async APIs where available | ✅ COVERED | 004-security-rulebook-validation |
| targets.md | Target Java framework version is 21 LTS | ✅ COVERED | 001-upgrade-java-21-lts |
| targets.md | Use Azure Blob Storage when replacing AWS S3 | ✅ COVERED | 002-transform-azure-storage-auth-patterns |
| targets.md | Replace AWS S3 SDK with azure-storage-blob | ✅ COVERED | 002-transform-azure-storage-auth-patterns |

**COVERED: 23/23  ·  NOT COVERED: 0/23**
