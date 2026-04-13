# Direct & Web Connect - Quicken / QuickBooks

## Quicken / QuickBooks Integration Guide

***

## Summary

The nFinia In-House OFX Server enables credit unions and community banks to facilitate direct financial data exchange between their members and Intuit products — specifically **QuickBooks** and **Quicken.** This feature hosts a fully compliant OFX 2.3 / FDX-standard endpoint within the Tyfone platform itself.

There are two connectivity modes this integration supports: **Direct Connect** and **Web Connect**. Direct Connect is the primary migration focus, as it involves real-time, credential-based communication between Intuit's software and the financial institution's OFX server. Web Connect, by contrast, is a file-export workflow (QBO, QFX, OFX, CSV) managed directly by Tyfone, where you manually download and import transaction files into your accounting software.

For the credit union, this migration delivers meaningful operational benefits: reduced third-party vendor dependency, improved platform stability, greater control over endpoint configuration, and the ability to serve members who rely on Intuit products for personal and small business financial management. For you, the integration means your transaction data — checking, savings, credit card, and more — stays in sync with your accounting or personal finance tools with minimal friction once the initial reconnection is completed.

### At a Glance

| Attribute            | Detail                                                                                             |
| -------------------- | -------------------------------------------------------------------------------------------------- |
| Feature Name         | Intuit Direct Connect & Web Connect (In-House OFX Server)                                          |
| Module               | nFinia Platform > Account Detail Page > Financial Data Export                                      |
| User Roles           | Member (end user), FI Operations, Tyfone Support, Tyfone CSM                                       |
| Access Level         | Member-initiated (Direct Connect); Member-initiated file download (Web Connect)                    |
| Key Actions          | Connect account, authenticate, fetch transaction history, export file formats (QBO, QFX, OFX, CSV) |
| Regulatory Relevance | FDX compliance, OFX 2.3 standard, multi-factor authentication, credential security                 |

***

## Use Cases

| Use Case                                       | Who Uses It                      | What They Do                                                                                                                                                               | Business Value                                                                                             |
| ---------------------------------------------- | -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Initial Direct Connect Setup**               | Member (QuickBooks/Quicken user) | Adds the credit union as a connected account in Quicken or QuickBooks using credentials; the OFX endpoint resolves to the new in-house server via Intuit's branding portal | Enables real-time transaction sync for members managing business or personal finances in Intuit software   |
| **Web Connect File Export**                    | Member                           | Logs into nFinia, navigates to account transaction history, and exports in QBO, QFX, OFX, or CSV format for manual import into QuickBooks or Quicken                       | Provides an alternative to Direct Connect for members who prefer or require manual import workflows        |
| **Post-Conversion Support & Issue Escalation** | FI Operations / Tyfone Support   | During the 48-hour post-launch window,  contact Tyfone CSM for issues; after that window, submit tickets via the Intuit partner portal                                     | Ensures rapid resolution of connectivity issues with a defined escalation path; maintains SLA expectations |
| **Transaction History Verification**           | Member                           | After reconnecting, verifies that 90 days of transaction history (default) has synced correctly across linked accounts                                                     | Confirms data integrity post-migration and builds member confidence in the new integration                 |

The use cases above reflect the reality of a migration-heavy integration: the majority of member impact is concentrated in the reconnection workflow. Credit unions that proactively communicate with their Quicken and QuickBooks members before the conversion date will see significantly fewer support escalations in the days immediately following go-live.

***

## End-to-End Workflow

### Prerequisites

Before Direct Connect can be established with the in-house OFX server:

* The credit union must have completed the OFX server conversion with Tyfone and confirmed the new endpoint URL is registered in **Intuit's branding portal**
* The conversion date must have been communicated to Intuit at least **8 weeks in advance**
* You must have an active nFinia account with valid credentials
* You must have QuickBooks Online, QuickBooks Desktop, or Quicken installed and configured

***

### Direct Connect — Member Workflow

**Step 1 — Intuit Resolves the OFX Endpoint**

Open QuickBooks or Quicken and initiate "Add Account" or "Update Account." The Intuit application queries the **Intuit FI Directory** to retrieve the financial institution's current OFX server URL. Intuit returns the **new in-house OFX endpoint**.

**Step 2 — Profile Request**

Quicken/QuickBooks sends an OFX Profile Request to the in-house server. The server responds with:

* Supported OFX version (OFX 2.3)
* Authentication method (username/password, with MFA if configured)
* Available services (banking, savings, credit card, etc.)

**Step 3 — Sign-On Request**

Enter your credit union credentials (username and password) within the Intuit application. Quicken/QuickBooks sends a **Sign-On Request** to the in-house OFX server. The server validates the credentials against the nFinia member authentication layer and returns a success token — or an error response if credentials are invalid.

**Step 4 — Account Enumeration**

Upon successful sign-on, Quicken/QuickBooks requests a list of all accounts linked to your authenticated profile. The OFX server returns account identifiers, types (checking, savings, credit card, etc.), and balances.

**Step 5 — Transaction Download**

Quicken/QuickBooks requests transaction history for each linked account. By default, the in-house OFX server returns **90 days of transaction history** (this is a configurable setting managed by Tyfone). Transactions are delivered in the OFX standard format and parsed natively by the Intuit application.

**Step 6 — Sync Confirmation**

Quicken/QuickBooks displays the imported transactions. Review and categorize them within your application. Subsequent syncs occur on-demand or on a scheduled basis, always resolving through the same in-house OFX endpoint.

***

### Web Connect — Member Workflow

**Step 1 — Log in to nFinia**

Log in to the nFinia digital banking platform via browser or mobile app.

**Step 2 — Navigate to Account Transaction History**

Select the relevant account (checking, savings, etc.) and open the transaction history view.

**Step 3 — Export Transactions**

Click the export/download option and select the desired format:

* **QBO** — for QuickBooks
* **QFX** — for Quicken
* **OFX** — open standard, compatible with multiple tools
* **CSV** — for spreadsheet or custom import workflows

**Step 4 — Import into Intuit Application**

Open QuickBooks or Quicken, navigate to File > Import, and select the downloaded file. The application imports the transactions and presents them for review and categorization.

***

### Decision Points & Branching

| Condition                                             | Outcome                                                                                             |
| ----------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Member does not disconnect & reconnect post-migration | Authentication failures, missing transactions, and sync errors will occur                           |
| Credentials are invalid at Sign-On                    | OFX server returns error; Quicken/QuickBooks displays login failure message                         |
| MFA is enabled for the FI                             | Additional authentication step required during Sign-On; Intuit application prompts for OTP or token |
| Member prefers no credential sharing                  | Use Web Connect (file export) as alternative — no live credential exchange required                 |

***

### Completion & Confirmation

For **Direct Connect**, a successful connection is confirmed when:

* Quicken/QuickBooks displays your accounts and transaction history without errors
* Subsequent scheduled sync operations complete without authentication failures
* Your transaction data matches what is visible in nFinia

For **Web Connect**, a successful import is confirmed when:

* The downloaded file opens without error in QuickBooks or Quicken
* Transactions displayed in the application match the exported date range from nFinia
* No duplicate transactions appear (Quicken/QuickBooks deduplication is handled by the FITID — which does not change in this migration)

***

### Error Handling

| Scenario                                    | What You See                      | Resolution                                                            |
| ------------------------------------------- | --------------------------------- | --------------------------------------------------------------------- |
| Incorrect credentials at Sign-On            | Login error in Quicken/QuickBooks | Verify credentials in nFinia; reset password if needed                |
| OFX server temporarily unavailable          | Connection timeout in Intuit app  | Retry after a few minutes; contact FI support if issue persists       |
| Transactions not syncing after reconnection | Incomplete transaction history    | Verify 90-day default window; contact FI if history appears truncated |
| MFA prompt not received                     | Sign-On stalls or times out       | Check phone/email for OTP; ensure contact info is current in nFinia   |

***

## Feature Overview (UI Walkthrough)

### Direct Connect — Quicken/QuickBooks (Member Side)

This screen flow occurs within the **Intuit application** (not in nFinia). Navigate to the account connection workflow — the OFX server interaction is handled in the background.

| Field / Element         | Type           | Description                                             | Notes                                                                 |
| ----------------------- | -------------- | ------------------------------------------------------- | --------------------------------------------------------------------- |
| Add Account / Search FI | Input          | Search for your credit union by name                    | Intuit resolves OFX URL from its branding portal based on the FI name |
| Username                | Input          | Your nFinia login username                              | Transmitted securely via OFX Sign-On Request                          |
| Password                | Input (masked) | Your nFinia password                                    | Validated against nFinia authentication layer                         |
| MFA / OTP Prompt        | Input          | One-time passcode if MFA is enabled                     | Displayed only if the FI has configured MFA                           |
| Account List            | Display        | Lists all accounts returned by the OFX server           | Includes account type, partial account number, and balance            |
| Transaction History     | Display        | Transactions returned for the selected date range       | Defaults to 90 days; FITID ensures no duplicate imports               |
| Sync / Update           | Button         | Triggers a new OFX session to fetch latest transactions | Member-initiated; Intuit handles the full OFX handshake automatically |

***

### Web Connect — nFinia Export (Member Side)

This screen is accessed within the **nFinia digital banking platform** under your account transaction history.

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

| Field / Element  | Type        | Description                              | Notes                                                       |
| ---------------- | ----------- | ---------------------------------------- | ----------------------------------------------------------- |
| Account Selector | Dropdown    | Select the account to export             | Checking, savings, credit card, etc.                        |
| Date Range       | Date Picker | Defines the transaction period to export | Default range is configurable; up to 90 days standard       |
| Export Format    | Dropdown    | Select file format                       | QBO (QuickBooks), QFX (Quicken), OFX (open standard), CSV   |
| Download Button  | Button      | Initiates file generation and download   | File is generated server-side and downloaded to your device |

***

### FI Operations — Intuit Partner Portal

For post-conversion issue escalation (beyond the first 48 hours), the FI uses the Intuit partner-only support portal.

| Field / Element  | Type      | Description                              | Notes                                                                          |
| ---------------- | --------- | ---------------------------------------- | ------------------------------------------------------------------------------ |
| Issue Category   | Dropdown  | Type of connectivity issue               | Direct Connect, Web Connect, authentication, transaction sync                  |
| Affected Product | Dropdown  | Intuit product impacted                  | QuickBooks, Quicken, Mint                                                      |
| Description      | Text Area | Detailed description of the issue        | More detail = faster resolution; include error codes and affected member count |
| Submission       | Button    | Submits ticket to Intuit partner support | 24–48 hour SLA applies; for urgent issues, escalate directly to Tyfone CSM     |

> **Note:** The Intuit partner portal (`https://ofx-partner.intuit.com/app/fi/ContactUs`) is for FI use only. Members should never be directed to this portal — they must be referred back to the FI.

***

***

## Post-Conversion Support

### First 48 Hours Post-Launch

The 48-hour window immediately following go-live is the highest-risk period for connectivity issues.

* Both Web Connect and Direct Connect should be **tested internally by the FI** before member-reported issues arrive
* Any issues during this period should be escalated directly to the **Tyfone CSM or Tyfone Support** — not to Intuit's partner portal
* Tyfone and the FI should maintain heightened monitoring of sync errors and authentication failures during this window

### Remaining Post-Conversion Support Period

* All issues beyond the first 48 hours are submitted via the **Intuit partner portal**: `https://ofx-partner.intuit.com/app/fi/ContactUs`
* A **24–48 hour SLA** applies to inquiries submitted through this channel
* Provide maximum detail in submissions: product affected, error messages, number of impacted members, and steps to reproduce
* For urgent escalations, contact the Tyfone CSM directly as the primary point of contact

***

## Frequently Asked Questions

**Will the OFX Profile URL change?**\
Yes. The OFX endpoint URL will change from NinthWave's server to the new in-house server. Members using Direct Connect will need to disconnect and reconnect your accounts to pick up the new endpoint automatically via Intuit's directory lookup.

**Will FITIDs (transaction IDs) change?**\
No. FITIDs remain unchanged — they continue to be sourced from the core system's transaction ID. This ensures Quicken and QuickBooks will not create duplicate transaction entries during or after the migration.

**How much transaction history will be available after migration?**\
By default, **90 days of transaction history** will be available through the OFX server. This is a configurable setting managed by Tyfone — contact your CSM if a different history window is needed for your members.

**What happens if I do not reconnect after migration?**\
If you do not disconnect and reconnect, you will experience authentication failures (credentials won't resolve against the old endpoint), failed transaction syncs (requests still routing to NinthWave's deprecated URL), and missing transactions in your Quicken or QuickBooks application. The only resolution is to manually disconnect and reconnect your account.

***

## Quick Reference

| Task                                         | Navigation Path / Action                                              | Who Can Do It  | Notes                                                                      |
| -------------------------------------------- | --------------------------------------------------------------------- | -------------- | -------------------------------------------------------------------------- |
| Connect account via Direct Connect           | Quicken/QuickBooks > Add Account > Search FI > Enter credentials      | Member         | OFX endpoint resolved automatically via Intuit directory                   |
| Disconnect existing account (post-migration) | Quicken/QuickBooks > Connected Accounts > Select Account > Disconnect | Member         | Required before reconnecting to new OFX endpoint                           |
| Export transactions (Web Connect)            | nFinia > Account > Transaction History > Export > Select Format       | Member         | Formats: QBO, QFX, OFX, CSV                                                |
| Update OFX URL in Intuit branding portal     | Intuit FI Branding Portal                                             | Tyfone Support | Done as part of conversion milestone; not member-facing action             |
| Submit post-conversion support ticket        | https://ofx-partner.intuit.com/app/fi/ContactUs                       | FI Operations  | Partner-only portal; do not direct members here                            |
| Escalate urgent issue during 48-hour window  | Contact Tyfone CSM directly                                           | FI Operations  | Use Tyfone Support channel; Intuit portal not applicable in first 48 hours |
| Verify transaction history depth             | Contact Tyfone CSM                                                    | FI Operations  | Default: 90 days; configurable per FI                                      |
| Confirm FITID continuity                     | No action required                                                    | —              | FITIDs do not change; deduplication handled natively by Intuit apps        |
