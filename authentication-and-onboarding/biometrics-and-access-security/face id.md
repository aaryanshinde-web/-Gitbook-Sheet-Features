# Face ID — Feature Guide

### Summerville Credit Union | nFinia Digital Banking Platform

**Prepared by:** Jeeva Krishnamurthy, Senior Product Manager — Commercial & SMB Digital Banking, Tyfone **Platform:** nFinia | **Module:** Authentication & Security Settings **Version:** 1.0 | **Date:** April 2026

***

## Section 1 — Product Summary

Face ID is a biometric authentication feature within the nFinia mobile banking platform that enables members of Summerville Credit Union to log into their digital banking account using facial recognition instead of (or in addition to) a traditional username and password. The feature is surfaced as an opt-in checkbox—**Enable Face ID**—directly on the standard Log In screen, making activation frictionless and contextual at the moment of first credential entry.

The feature leverages the native biometric framework of the member's mobile device (iOS Face ID / Android BiometricPrompt), meaning that no facial data is transmitted to or stored on Tyfone's or Summerville's servers. The device itself performs the biometric match and passes an authenticated signal to the nFinia app. This architecture separates credential security from biometric data entirely, reducing PII exposure risk and simplifying compliance posture.

Face ID serves all authenticated nFinia users—both retail members and business banking users—who access the platform via a compatible mobile device. Once enrolled, the member can authenticate subsequent sessions with a glance, eliminating password entry friction while maintaining a strong second-factor assurance level. This is particularly valuable for business members who log in frequently to monitor cash flow, approve transactions, or review commercial activity throughout the workday.

For Summerville Credit Union, Face ID represents a tangible differentiator in member experience: it signals that the credit union is keeping pace with the biometric authentication standards that large national banks and neobanks have normalized. Reduced login abandonment and higher session engagement are the expected downstream effects.

### At a Glance

| Attribute                | Detail                                                                                             |
| ------------------------ | -------------------------------------------------------------------------------------------------- |
| **Feature Name**         | Face ID (Biometric Authentication)                                                                 |
| **Module**               | Authentication > Log In                                                                            |
| **User Roles**           | All authenticated members (Retail & Business Banking)                                              |
| **Access Level**         | Self-service; member opt-in at login                                                               |
| **Key Actions**          | Enable Face ID, authenticate via biometric, fall back to password                                  |
| **Regulatory Relevance** | Strong customer authentication (SCA); device-bound credential; no biometric PII stored server-side |

***

## Section 2 — Use Cases

| Use Case                                     | Who Uses It                                                                | What They Do                                                                                                    | Business Value                                                                                 |
| -------------------------------------------- | -------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **First-Time Face ID Enrollment**            | Retail or Business member logging in from a new or reset device            | Checks the "Enable Face ID" box during credential-based login; completes device biometric prompt on next launch | Eliminates repeated password entry; reduces login friction from day one on new devices         |
| **Biometric Login — Returning Member**       | Any enrolled member opening the app for a subsequent session               | App launches biometric prompt automatically; member authenticates with a glance                                 | Faster session start; reduces abandonment from forgotten passwords; improves daily engagement  |
| **Shared Device — Intentional Opt-Out**      | Member who shares a device with a family member or colleague               | Leaves "Enable Face ID" unchecked; uses password-only login                                                     | Preserves account security on shared hardware; no unwanted biometric binding                   |
| **Biometric Failure — Fallback to Password** | Member whose Face ID fails (poor lighting, appearance change, etc.)        | Device declines biometric match; member is presented with standard username/password login                      | Maintains access continuity; prevents lockout; ensures 100% accessibility                      |
| **Device Change or Re-Enrollment**           | Member who upgrades their phone or resets biometrics                       | Re-enables Face ID by checking the option at next credential login                                              | Seamless re-onboarding to biometric auth without contacting the FI                             |
| **Business Member — High-Frequency Access**  | CFO or business owner checking balances and approvals multiple times daily | Uses Face ID to authenticate quickly between commercial tasks                                                   | Reduces session startup cost; supports real-time cash flow monitoring without password fatigue |

Face ID directly addresses one of the most common friction points in digital banking: the repetitive credential entry required for frequent session logins. For credit unions like Summerville CU that serve business members with high daily transaction volumes, reducing this friction translates directly into more frequent platform engagement and fewer password-related support calls.

***

## Section 3 — End-to-End Workflow

### 3.1 Prerequisites

* Member must have an active nFinia account (retail or business) with valid credentials.
* The mobile device must support Face ID (iOS) or Biometric Authentication (Android).
* The device's native biometric (Face ID / fingerprint) must be enrolled at the OS level before the feature can be activated in nFinia.
* The member must be on the Log In screen and have entered a valid Username (the "Enable Face ID" checkbox only becomes actionable in the context of a credential-based login session).

### 3.2 Step-by-Step Flow

**Step 1 — Navigate to the Log In Screen** The member opens the Summerville CU nFinia app. The Welcome screen presents two primary actions: **Enroll** and **Log In**. The member taps **Log In**.

<figure><img src="/.gitbook/assets/Summerville_CU_Welcome_Screen___nFinia_Mobile_App_1.jpeg" alt="Welcome Screen — tap Log In to proceed" width="340"><figcaption></figcaption></figure>


**Step 2 — Enter Credentials** The Log In screen loads with fields for **Username** and **Password**. The member enters their username (e.g., `dblake`) and their password.

<figure><img src="/.gitbook/assets/Summerville_CU_Log_In_Screen___Enable_Face_ID_Checkbox_2.jpeg" alt="Log In screen — enter Username and Password" width="340"><figcaption></figcaption></figure>


**Step 3 — Enable Face ID Checkbox** Below the credential fields, two checkboxes are visible:

<figure><img src="/.gitbook/assets/Summerville_CU_Log_In_Screen___Enable_Face_ID_Checkbox_2.jpeg" alt="Log In screen — check Enable Face ID checkbox" width="340"><figcaption></figcaption></figure>


* **Remember me** — pre-checked (grayed, indicating it is already active or dependent on the Face ID opt-in)
* **Enable Face ID** — unchecked by default on first access; the member checks this box to enroll

Checking **Enable Face ID** signals to the app that the member consents to biometric authentication for future sessions on this device.

**Step 4 — Complete Login** The member taps the **Log In** button. The platform authenticates the credential pair against the member record. On success, the app requests the device's biometric framework to register this session as Face ID–enabled.

<figure><img src="/.gitbook/assets/Summerville_CU_Log_In_Screen___Enable_Face_ID_Checkbox_2.jpeg" alt="Log In screen — tap Log In button to complete enrollment" width="340"><figcaption></figcaption></figure>


**Step 5 — Biometric Binding (OS-Level)** The device OS presents a native biometric confirmation prompt. The member confirms using Face ID. The nFinia app stores a device-bound token (not facial data) associated with the member's session.

**Step 6 — Subsequent Sessions** On the next app launch, instead of the credential entry screen, the app triggers the Face ID prompt directly. The member authenticates with a glance. Session begins immediately upon successful biometric match.

### 3.3 Decision Points & Branching

* **Face ID not available on device:** The "Enable Face ID" checkbox does not appear, or is disabled/hidden. The member proceeds with standard credential login only.
* **Biometric not enrolled at OS level:** The app may display a system message directing the member to configure Face ID in device Settings before proceeding.
* **Member does not check "Enable Face ID":** Login proceeds normally with credentials only; Face ID is not activated for future sessions.
* **"Remember me" interaction:** The "Remember me" checkbox appears pre-checked and grayed when "Enable Face ID" is selected, suggesting it is a dependency — device is remembered as part of the biometric trust chain.

### 3.4 Completion & Confirmation

Upon successful Face ID enrollment and login:

* The member is routed to the nFinia Dashboard (or Business Banking home, depending on account type).
* No explicit confirmation banner is shown for Face ID enrollment — success is implicit in the next biometric-authenticated session.
* The device is added to the member's trusted device list, visible under **Manage Devices** from the Welcome screen or account settings.

### 3.5 Error Handling

| Scenario                                                           | Member Experience                            | Recovery Path                                                             |
| ------------------------------------------------------------------ | -------------------------------------------- | ------------------------------------------------------------------------- |
| Face ID match fails (lighting, angle)                              | Device presents retry or fallback prompt     | Member falls back to username/password login                              |
| Device biometric not set up                                        | OS-level alert or feature unavailable in app | Member configures Face ID in device Settings, then re-attempts enrollment |
| Account lockout (too many failed password attempts before Face ID) | Standard lockout message with help link      | Member taps "I need help logging in" for self-service recovery            |
| Token expiry / session invalidated                                 | App falls back to full credential entry      | Member re-enters credentials and re-checks "Enable Face ID" to re-bind    |

***

## Section 4 — Feature Overview (UI Walkthrough)

### Welcome Screen

The Welcome screen is the app's pre-authentication landing page. It presents quick-access options for unauthenticated actions alongside the primary Login and Enrollment calls to action. Face ID itself is not surfaced here — this screen is the gateway to it.

![Summerville CU Welcome Screen — nFinia Mobile App](../../../.gitbook/assets/Summerville_CU_Welcome_Screen___nFinia_Mobile_App_1.jpeg) _Figure 1: Summerville CU Welcome Screen — nFinia Mobile App_

| Field / Element      | Type                   | Description                                | Notes                                  |
| -------------------- | ---------------------- | ------------------------------------------ | -------------------------------------- |
| **Summerville Logo** | Label / Branding       | Credit union brand mark at top center      | Static display                         |
| **Welcome**          | Heading                | Page title                                 | Static display                         |
| **Enroll**           | Button (outlined)      | Navigates to new member enrollment flow    | Available to unauthenticated users     |
| **Log In**           | Button (filled, dark)  | Navigates to the Log In screen             | Primary CTA; dark navy fill            |
| **Accounts**         | Quick-access icon      | Pre-login account summary shortcut         | Available without full authentication  |
| **Move Money**       | Quick-access icon      | Pre-login money movement shortcut          | Scope limited until authenticated      |
| **Check deposit**    | Quick-access icon      | Pre-login check deposit shortcut           | Scope limited until authenticated      |
| **Manage Devices**   | Quick-access icon      | Device management shortcut                 | Links to trusted device management     |
| **Balance**          | Slide-to-reveal button | Reveals account balance without full login | Touch/slide interaction; privacy-aware |

***

### Log In Screen

The Log In screen is where Face ID enrollment is triggered. The member enters their credentials and, if they wish to enable biometric login for future sessions, checks the **Enable Face ID** checkbox before submitting.

![Summerville CU Log In Screen — Enable Face ID Checkbox](../../../.gitbook/assets/Summerville_CU_Log_In_Screen___Enable_Face_ID_Checkbox_2.jpeg) _Figure 2: Summerville CU Log In Screen — Enable Face ID Option_

| Field / Element             | Type                       | Description                                                                      | Notes                                                                                                    |
| --------------------------- | -------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Back arrow**              | Navigation button          | Returns to Welcome screen                                                        | Top-left corner                                                                                          |
| **Summerville Logo**        | Label / Branding           | Credit union brand mark                                                          | Static display                                                                                           |
| **Log in**                  | Heading                    | Page title                                                                       | Static display                                                                                           |
| **Username**                | Text input                 | Member's digital banking username                                                | Required; plain text                                                                                     |
| **Password**                | Password input             | Member's account password                                                        | Required; masked by default; reveal toggle (eye icon) available                                          |
| **Remember me**             | Checkbox                   | Persists device recognition across sessions                                      | Appears pre-checked/grayed when "Enable Face ID" is active; dependent state                              |
| **Enable Face ID**          | Checkbox                   | Opts the member into biometric authentication for future sessions on this device | Unchecked by default; member must actively check to enroll; triggers OS biometric binding on next launch |
| **Log In**                  | Button (filled, dark navy) | Submits credentials and initiates authentication                                 | Primary action; active only when Username + Password are populated                                       |
| **Enroll**                  | Button (outlined)          | Navigates to new member enrollment                                               | Secondary CTA for non-members                                                                            |
| **I need help logging in**  | Hyperlink                  | Self-service help for forgotten credentials, lockouts                            | Routes to password reset / help flow                                                                     |
| **Tap to see your balance** | Persistent bottom bar      | Reveals balance without full authentication                                      | Slide/tap interaction; always visible on Login screen                                                    |

***

## Section 5 — Quick Reference

| Task                                     | Navigation Path                                                        | Who Can Do It                                   | Notes                                                     |
| ---------------------------------------- | ---------------------------------------------------------------------- | ----------------------------------------------- | --------------------------------------------------------- |
| Enable Face ID for the first time        | Welcome → Log In → Enter credentials → Check "Enable Face ID" → Log In | Any authenticated member on a compatible device | Device biometric must be configured at OS level first     |
| Disable / skip Face ID                   | Welcome → Log In → Leave "Enable Face ID" unchecked                    | Any member                                      | Face ID will not activate; standard credential login only |
| Re-enroll Face ID after device change    | Welcome → Log In → Enter credentials → Check "Enable Face ID" → Log In | Any member on a new or reset device             | Re-binds biometric token to new device                    |
| Manage trusted devices                   | Welcome → Manage Devices                                               | Any authenticated member                        | View and remove devices with saved biometric trust        |
| Fall back to password when Face ID fails | Face ID prompt → Use Password / Cancel                                 | Any enrolled member                             | App returns to standard Log In screen                     |
| Get help with login                      | Welcome → Log In → "I need help logging in"                            | Any member                                      | Routes to self-service credential recovery                |

***

_Guide prepared by Jeeva Krishnamurthy, Senior Product Manager — Commercial & SMB Digital Banking, Tyfone. All platform behavior documented as observed in the Summerville Credit Union deployment of nFinia. April 2026._
