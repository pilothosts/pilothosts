# Security Policy

PilotHosts is deployed inside customer infrastructure and holds credentials for vCenter, Veeam, LDAP/Active Directory, and Kubernetes environments. We take security reports seriously and appreciate responsible disclosure.

## Supported Versions

Only the latest released version of PilotHosts receives security fixes. Customers on an older version should upgrade to the latest release before reporting an issue, if possible.

| Version | Supported |
|---|---|
| v1.1.x | ✅ |
| v1.0.x | ⚠️ Critical fixes only |
| < v1.0 | ❌ |

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Instead, email us directly at **[support@pilothosts.com](mailto:support@pilothosts.com)** (subject line: `Security Report`) with:

- A description of the vulnerability and its potential impact
- Steps to reproduce, or a proof of concept if available
- The PilotHosts version and deployment context (if relevant)

We aim to:

- Acknowledge your report within **2 business days**
- Provide an initial assessment within **5 business days**
- Keep you updated as we investigate and remediate

If confirmed, we will coordinate a disclosure timeline with you before any public details are shared. We're happy to credit reporters who wish to be acknowledged once a fix ships.

## Scope

This policy covers the PilotHosts appliance itself (application code, OVA packaging, update mechanism). It does not cover vulnerabilities in third-party components we bundle (VMware SDKs, PostgreSQL, Redis, etc.) — please report those directly to the upstream project, though we're glad to hear about them too so we can track and patch our bundled versions.

## Data Handling

PilotHosts is designed so that infrastructure data never leaves your network: there is no SaaS backend, no telemetry of infrastructure contents, and no agents installed on managed platforms. Credentials are encrypted at rest. See [pilothosts.com/docs](https://www.pilothosts.com/docs/) for architecture details.
