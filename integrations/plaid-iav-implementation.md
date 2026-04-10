<div align="center">
![](/.gitbook/assets/plaid-001.png)
</div>

---

# Instant Account Verification (IAV) — Plaid Integration Guide

**nFinia Digital Banking Platform | Business Banking Module**
*Prepared by: Jeeva Krishnamurthy, Senior Product Manager — Commercial & SMB Digital Banking, Tyfone*
*Document Version: 1.0.1 | Last Updated: August 27, 2025*

---

## Table of Contents

1. [Product Summary](#1-product-summary)
2. [Use Cases](#2-use-cases)
3. [End-to-End Workflow](#3-end-to-end-workflow)
4. [Feature Overview — UI Walkthrough](#4-feature-overview--ui-walkthrough)
5. [Quick Reference](#5-quick-reference)

---

## . Product Summary

Instant Account Verification (IAV) via Plaid is a feature within the nFinia digital banking platform that allows you to verify your own external bank accounts — accounts you hold at other financial institutions — in real time, without waiting for micro-deposit confirmation. The integration leverages Plaid's Link API, enabling you to authenticate directly with their external institution through a secure, embedded OAuth flow launched from within the nFinia interface.

By eliminating the traditional micro-deposit wait period (typically 1–3 business days), IAV dramatically reduces friction in the external account onboarding journey. Once an external account is verified, you can immediately initiate ACH transfers to and from that account. This is a significant improvement for both you experience and the credit union's competitive position against digital-native challengers like Mercury and Relay, which offer instant account linking as table stakes.

**Scope & Eligibility:** In the current Plaid integration configuration, IAV is enabled for **personal/retail accounts only** (`applicableForPersonal: true`, `applicableForBusiness: false`). Business members use the micro-deposit flow. The feature does not permit you to verify an account owned by someone else — only your own accounts qualify. This constraint is enforced at both the configuration and UI levels.

### At a Glance

| Attribute | Detail |
|-----------|--------|
| **Feature Name** | Instant Account Verification (IAV) — Plaid |
| **Module** | nFinia > External Transfers > Account Verification |
| **User Roles** | Retail Member (Personal Account Holder) |
| **Access Level** | Enabled per system config; personal accounts only |
| **Key Actions** | Initiate IAV, Authenticate with external institution, Select & verify accounts, Complete ACH-ready linkage |
| **Vendor** | Plaid (via Plaid Link Web SDK) |
| **Regulatory Relevance** | Account ownership verification, BSA/AML — confirms account belongs to the authenticated member |
| **Fix Version** | nFinia 10.45 (OLB Branch: NFIN-41731) |

---

## . Use Cases

| Use Case | Who Uses It | What They Do | Business Value |
|----------|-------------|--------------|----------------|
| **Instant External Account Link** | Retail member onboarding a new external account | Initiates IAV, authenticates with their external bank via Plaid, selects the account to link — verified in under 2 minutes | Eliminates 1–3 day micro-deposit wait; you can initiate ACH transfers immediately |
| **ACH Transfer Setup — Personal** | Member who wants to transfer funds to/from a personal account at another FI | Completes IAV flow to verify their external checking/savings account, then proceeds to schedule ACH transfer | Increases ACH origination volume for the credit union; reduces call center contacts about pending verification |
| **Guest / Unlinked Authentication Path** | Member who prefers not to share full banking credentials | Selects "Continue as Guest" during Plaid flow and proceeds through alternative credential path | Preserves member choice; reduces abandonment for credential-sensitive you |
| **Multi-Factor Verification** | Member whose external bank requires MFA during Plaid authentication | Receives OTP/verification code from external bank, enters it within the Plaid Link interface | Supports institutions with enhanced security; does not require additional nFinia configuration |
| **Identity Category Selection** | Member whose external bank offers multiple verification methods | Selects the appropriate identity verification category (e.g., SSN, email, phone) to authenticate | Accommodates diverse institution requirements within a single standardized flow |
| **Business Account — Micro-Deposit Fallback** | Business member attempting external account verification | IAV is not presented; system routes to micro-deposit flow (`applicableForBusiness: false`) | Maintains compliance separation between personal and business account verification pathways |

These use cases reflect the reality that credit union members hold accounts across multiple institutions and need frictionless pathways to consolidate their financial activity within nFinia. IAV via Plaid positions the credit union to retain primary financial institution (PFI) status by making it easier to aggregate external funds.

---

## . End-to-End Workflow

### Prerequisites

- Member must be enrolled in nFinia and logged in
- The `IAV_DETAILS` system configuration must have `"enabled": "Y"` and `"isPersonalApplicable": true`
- `IAV_VENDOR_NAME` must be set to `'PLAID'`
- Member must be on a **personal/retail account** (business accounts are excluded in current config)
- Member must hold an account at an external financial institution supported by Plaid's network

### Step-by-Step Flow

**Step 1 — Navigate to External Account Verification**
Navigate to the External Transfers section of nFinia and selects the option to add or verify an external account. The system detects that IAV is enabled and the account is personal-eligible, then launches the IAV entry point.

**Step 2 — IAV Prompt: "Yes" or "Continue as Guest"**
You is presented with a prompt asking whether they want to proceed with instant verification. Two options are available:
- **"Yes"** — Proceeds to the Plaid Link flow for full instant verification
- **"Continue as Guest"** — Proceeds through an alternative path (limited or deferred verification)

**Step 3 — Institution Search & Selection**
You is presented with the Plaid Link interface, which displays a searchable list of financial institutions. You searches for and selects their external institution (e.g., Bank of America, Chase, Wells Fargo).

**Step 4 — Click "Continue to Login"**
After selecting the institution, you clicks "Continue to Login." Plaid loads the institution-specific login interface within the embedded frame.

**Step 5 — Enter External Bank Credentials**
A new secure window opens displaying the external institution's login form (served by Plaid). You enters their online banking username and password, then clicks "Sign In."

**Step 6 — Identity Verification Category Selection** *(conditional)*
If the external institution requires identity verification, you are prompted to select a verification category — for example, Social Security Number, email address, or phone number. This step varies by institution.

**Step 7 — Multi-Factor Authentication / Get Code** *(conditional)*
If MFA is required, you clicks "Get Code." An OTP is sent to your registered contact method at the external institution. Enter the code to complete authentication.

**Step 8 — Account Selection**
After successful authentication, Plaid returns a list of your eligible accounts at the external institution. Select the specific account(s) you want to verify and link.

**Step 9 — Submit & Confirm**
Click "Continue" or "Submit." Plaid completes the verification handshake with nFinia. The external account is added as a verified, ACH-ready linked account.

### Decision Points & Branching

| Decision Point | Branch A | Branch B |
|----------------|----------|----------|
| Member clicks "Yes" at IAV prompt | Full Plaid Link flow launches | — |
| Member clicks "Continue as Guest" | Alternative limited verification path | — |
| External institution requires MFA | OTP/Code entry step is presented | Skipped if no MFA required |
| Identity category selection required | Member selects category (SSN/email/phone) | Skipped if not required by institution |
| Member is on business account | Routed to micro-deposit flow | IAV not available |

### Completion & Confirmation

Upon successful completion of the Plaid flow:
- The external account is added to your verified accounts list in nFinia
- The account is immediately available for ACH transfer origination
- An audit log entry is created capturing the IAV event, timestamp, and linked account details
- You may proceed directly to initiate an ACH transfer without any further verification delay

### Error Handling

| Scenario | Member Experience | Resolution |
|----------|-------------------|------------|
| Incorrect external bank credentials | Plaid displays an error within the Link frame; you can retry | Re-enter correct credentials |
| External institution not supported by Plaid | Institution not found in Plaid search | Member is directed to micro-deposit flow |
| MFA code expired or incorrect | Plaid prompts to re-request a new code | Click "Get Code" again |
| Member attempts IAV on business account | IAV option not shown; routed to micro-deposit flow | No action required — by design |
| Plaid service unavailable | Error state displayed; IAV option may be suppressed | Contact FI support; retry later |

---

## . Feature Overview — UI Walkthrough

### Screen 1 — IAV Entry Prompt ("Yes" / "Continue as Guest")

This is the initial prompt presented to you when external account verification is initiated. It offers two paths: instant verification via Plaid or a guest/alternative path.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Prompt message | Label | Explains the instant verification option | Displayed when IAV config is enabled |
| **"Yes"** button | Button | Launches the full Plaid Link flow | Primary CTA for instant verification |
| **"Continue as Guest"** button | Button | Proceeds with alternative verification | Available for members who do not want to share credentials |

**On click of "Yes":**

![](/.gitbook/assets/plaid-002.png)

---

### Screen 2 — Institution Search & Selection

The Plaid Link interface displays a searchable directory of supported financial institutions. You types the name of their external bank to locate it.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Institution search bar | Text Input | Free-text search for external FI | Plaid-hosted; searches Plaid's supported institution network |
| Institution list | List | Scrollable/filtered list of matching institutions | Dynamically filtered as member types |
| Institution tile | Selectable Item | Tap/click to select the target institution | Triggers transition to login screen |

**Select any institution:**

![](/.gitbook/assets/plaid-004.png)

---

### Screen 3 — Continue to Login

After institution selection, you are shown a confirmation screen for the chosen institution before being directed to the institution's login interface.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Selected institution name | Label | Displays the chosen external institution | Read-only; confirms member's selection |
| **"Continue to Login"** button | Button | Proceeds to external institution login | Initiates Plaid's secure OAuth/credential flow |
| Back/Cancel option | Link/Button | Returns to institution search | Allows member to change institution |

**Click on Continue to Login:**

![](/.gitbook/assets/plaid-005.png)

---

### Screen 4 — External Institution Credential Entry

A new secure window opens displaying the external institution's login form, served through the Plaid Link frame. You authenticates using their credentials for the external bank.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Username / User ID | Text Input | Member's online banking username at the external FI | Plaid-hosted; credentials not stored by nFinia |
| Password | Password Input | Member's online banking password | Transmitted securely through Plaid's encrypted channel |
| **"Sign In"** button | Button | Submits credentials to external institution | Triggers Plaid authentication |

**New window opens — enter credentials, click Sign In:**

![](/.gitbook/assets/plaid-016.png)

---

### Screen 5 — Identity Verification Category Selection *(conditional)*

Some external institutions require identity verification as an additional authentication step. Select the appropriate category based on the options presented by the institution.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Verification category list | Radio / Selectable List | Options such as SSN, email, phone number | Institution-dependent; not all banks require this step |
| **"Continue"** / **"Next"** button | Button | Proceeds with selected verification method | Triggers delivery of OTP or further identity check |

**Select category for verify your identity:**

![](/.gitbook/assets/plaid-017.png)

---

### Screen 6 — Enter Verification Code

After selecting a verification method, you receive a one-time security code at your registered contact (e.g., phone number ending in 1111). Enter the code in the field provided and click **Submit** to authenticate. This step confirms your identity before proceeding to account selection.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Verification header | Label | Confirms the destination of the security code (masked phone/email) | Displayed by Plaid; varies by institution MFA config |
| **Code** field | Text Input | Field to enter the one-time security code received | Time-limited; must be entered before expiry |
| **"Submit"** button | Button | Submits the code for validation | Proceeds to account selection on successful verification |

**Enter the verification code received:**

![](/.gitbook/assets/plaid-018.png)

---

### Screen 7 — Account Selection & Data Sharing Consent

After successful authentication, Plaid presents a list of your eligible accounts at the external institution. Select the account(s) you want to link. Below the account list, you will see a summary of the standard account data that will be shared (e.g., Account Name, Balance, Transactions) as well as optional additional data fields you may choose to share. Review the data sharing details and click **Continue** to proceed.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Account list | Checkbox List | Lists all available accounts (checking, savings, loans, etc.) with masked account numbers | Select one or more accounts to link; checked accounts will be verified |
| Standard data access summary | Label | Lists the standard information that will be shared: Account Name, Description, Balance, Transactions, Statement Date, Payment Details | Pre-determined by the institution and Plaid; cannot be deselected |
| Additional information checkboxes | Checkbox | Optional fields: Account holder name(s) & Role(s); Account number and routing number | Member can choose whether to share these additional data points |
| **"Continue"** button | Button | Confirms account selection and data sharing consent; advances to the confirmation screen | Triggers Plaid's account verification handshake |

**Select accounts and review data sharing:**

![](/.gitbook/assets/plaid-009.png)

![](/.gitbook/assets/plaid-019.png)

---

### Screen 8 — Connect Account Information — Confirm

This screen provides a full summary of the account information that will be shared with your institution before finalizing the connection. It includes the selected cash accounts, a statement about what financial statements will be shared, and a profile information disclosure. You must accept the Terms and Conditions and click **Connect account information** to complete the Plaid verification. Once confirmed, the external account is linked and ACH-ready.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Cash accounts summary | Label | Displays the selected accounts to be linked | Read-only confirmation of member's account selection |
| Statements disclosure | Label | States that checking, savings, mortgage, home equity, HELOC, and credit card statements will be shared as they become available | Informational; member must review before accepting |
| Profile information disclosure | Label | States that account ownership, name, primary address, email, and phone number will be shared with the authorized third party | Informational; ensures transparency about PII sharing |
| **Terms and Conditions** checkbox | Checkbox | "I have read and accept the Terms and Conditions" | Must be checked to enable the Connect button |
| **"Connect account information"** button | Button | Finalizes the Plaid link; returns member to nFinia with account verified | Triggers Plaid verification handshake; account becomes ACH-ready |

**Review and confirm account connection:**

![](/.gitbook/assets/plaid-020.png)

---

### Screen 9 — Multi-Factor Authentication — Get Code *(conditional)*

If the external institution requires an additional MFA step, you are prompted to request and enter a one-time passcode via phone. This step is served through the Plaid Link interface and varies by institution.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Verification method indicator | Label | Shows how the OTP will be delivered (SMS, email, etc.) | Determined by external institution's MFA configuration |
| **"Get Code"** button | Button | Requests OTP from external institution | Triggers delivery to member's registered contact |

**On clicking "Get Code":**

![](/.gitbook/assets/plaid-008.png)

---

### Screen 10 — Save Credentials & Success

After account selection is confirmed, Plaid may prompt you to save your credentials for faster re-linking in the future. Once saved, a success screen confirms that the external account has been successfully verified and linked within nFinia. The account is now available for ACH transfers immediately.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Account list overview | Display | Shows all linked accounts at a glance | Confirmation that the correct accounts were selected |
| Save credentials prompt | Modal | Asks if you want to save your login with Plaid for future use | Optional; improves re-linking experience |
| Success confirmation | Screen | Confirms the external account is verified and ACH-ready | Returned to nFinia with linked account available |

**Account confirmed — save credentials and completion:**

![](/.gitbook/assets/plaid-010.png)

![](/.gitbook/assets/plaid-015.png)

---

## . Quick Reference

| Task | Navigation Path | Who Can Do It | Notes |
|------|----------------|---------------|-------|
| Initiate Instant Account Verification | nFinia > External Transfers > Add External Account > Verify Instantly | Retail member (personal account) | IAV must be enabled in system config; business accounts use micro-deposit |
| Search and select external institution | Plaid Link modal > Institution Search | Retail member | Powered by Plaid's institution directory |
| Authenticate with external bank | Plaid Link > Sign In | Retail member | Credentials handled entirely by Plaid — not stored in nFinia |
| Complete MFA for external bank | Plaid Link > Get Code | Retail member | Institution-dependent; triggered automatically if MFA is required |
| Select accounts to link | Plaid Link > Account Selection | Retail member | Multiple accounts may be selected if available |
| Verify business external account | nFinia > External Transfers > Add External Account > Micro-Deposit | Business member | IAV not available for business accounts in current config |
| Enable/disable IAV | System Configuration > `IAV_DETAILS` > `enabled` | FI Administrator / Tyfone Support | Set `"enabled": "Y"` or `"N"` to toggle feature |
| Switch personal IAV eligibility | System Configuration > `IAV_DETAILS` > `isPersonalApplicable` | FI Administrator / Tyfone Support | Set `true`/`false` to control retail member access |

---

*For implementation questions or to request changes to IAV configuration, contact your Tyfone Platform Support representative.*
*Plaid integration reference: [https://plaid.com/docs/link/web/](https://plaid.com/docs/link/web/)*

---
<div align="center"><sub>Tyfone nFinia Platform | IAV-Plaid Guide v1.0.1 | Confidential</sub></div>
