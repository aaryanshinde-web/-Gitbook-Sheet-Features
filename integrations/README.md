---
description: Third-party vendor and API integrations within the nFinia Digital Banking platform — configuration, architecture, and member-facing flows.
---

# Vendor Integrations

This section documents all third-party vendor and API integrations that extend the nFinia platform's capabilities for Diamond Credit Union members.

---

## Integration Inventory

| Integration | Vendor | Category | Status |
| --- | --- | --- | --- |
| [Prisma — Full Edition](prisma-integration.md) | Prisma | Security & Compliance | ✅ Documented |
| [Direct & Web Connect](direct-and-web-connect-quicken-quickbooks.md) | Intuit / Tyfone OFX | Account Export | ✅ Documented |
| [End User Support Portal](zendesk-end-user-support.md) | ZenDesk | Member Support | ✅ Documented |
| [Mortgage Balances](mortgage-balances-fics-api.md) | FICS API | Loan Data | ✅ Documented |
| [eDocuments](edocuments-bdi-sso.md) | BDI SSO | Statements & Docs | ✅ Documented |
| [Velera API](velera-api-integration.md) | Velera | Card Services | ✅ Documented |
| [Loan Origination SSO](meridianlink-loan-origination-sso.md) | MeridianLink | Loan Origination | ✅ Documented |
| [Plaid IAV](plaid-iav-implementation.md) | Plaid | Account Verification | ✅ Documented |

---

## Integration Architecture

All vendor integrations operate through one of three connection patterns:

| Pattern | Description | Examples |
| --- | --- | --- |
| **SSO / OAuth Redirect** | Member is redirected to a vendor-hosted portal and returned to nFinia after authentication | BDI SSO, MeridianLink |
| **Embedded API** | nFinia calls a vendor REST or SOAP API server-side; member sees a native UI | FICS API, Plaid IAV, Velera |
| **Data Export / OFX** | Member downloads a file or initiates a direct connect session from within nFinia | Direct Connect, Web Connect |

{% hint style="info" %}
All integrations are subject to the credential and API key management processes defined in the Tyfone implementation runbook. Contact the Tyfone implementation team for provisioning details.
{% endhint %}
