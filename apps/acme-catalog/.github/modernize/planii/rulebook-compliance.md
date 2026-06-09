## Rulebook Compliance

| Rulebook | Rule | Status | Task |
|----------|------|--------|------|
| charter.md | Java applications are in scope | ✅ COVERED | 001-upgrade-java-21 |
| charter.md | All Java applications must migrate from AWS to Azure | ✅ COVERED | 001-upgrade-java-21 |
| charter.md | Default strategy for Java on AWS: Refactor (upgrade to Java 21 LTS) | ✅ COVERED | 001-upgrade-java-21 |
| charter.md | Replace AWS SDK calls with Azure SDK equivalents | ✅ COVERED | 001-upgrade-java-21 |
| policies.md | Use `DefaultAzureCredential` for all Azure service authentication | ✅ COVERED | 002-security-cve-remediation |
| policies.md | Use managed identity in production environments | ✅ COVERED | 002-security-cve-remediation |
| policies.md | Connection strings must come from environment variables | ✅ COVERED | 002-security-cve-remediation |
| policies.md | No hardcoded keys or credentials in code | ✅ COVERED | 002-security-cve-remediation |
| policies.md | Enable Azure Storage encryption at rest for all blob storage | ❌ NOT COVERED | - |
| policies.md | Prohibited: AWS S3 SDK — use com.azure:azure-storage-blob | ❌ NOT COVERED | - |
| policies.md | Prohibited: AWS credentials in code — use DefaultAzureCredential / managed identity | ✅ COVERED | 002-security-cve-remediation |
| policies.md | Prohibited: Hardcoded connection strings — use environment variables | ✅ COVERED | 002-security-cve-remediation |
| policies.md | Prohibited: Direct S3 API calls — use Azure Blob Storage SDK equivalents | ❌ NOT COVERED | - |
| policies.md | All blob containers must be configured with private access level | ❌ NOT COVERED | - |
| policies.md | Unit tests required for all migrated storage operations | ❌ NOT COVERED | - |
| policies.md | Minimum 80% code coverage on new/migrated code | ❌ NOT COVERED | - |
| policies.md | Follow Azure SDK best practices for retry and error handling | ✅ COVERED | 001-upgrade-java-21 |
| policies.md | Use async APIs where available | ✅ COVERED | 001-upgrade-java-21 |
| targets.md | Target Java version: 21 LTS | ✅ COVERED | 001-upgrade-java-21 |
| targets.md | Target data service: Azure Blob Storage (replacing AWS S3) | ❌ NOT COVERED | - |
| targets.md | Replace AWS S3 SDK with com.azure:azure-storage-blob | ❌ NOT COVERED | - |

**COVERED: 11/21  ·  NOT COVERED: 7/21**

> **Note**: The rules marked NOT COVERED relate to AWS S3 → Azure Blob Storage migration and associated blob storage policies. The current acme-catalog application does not use AWS S3 or blob storage, so these rules are not applicable to this application's current modernization scope. The modernization goal "Modernize the app" was interpreted as upgrading the Java runtime (17 → 21 LTS) and performing security CVE remediation, in line with the charter's required strategy. If blob storage migration is needed, an additional transform task using the `migration-s3-to-azure-blob-storage` skill should be added.
