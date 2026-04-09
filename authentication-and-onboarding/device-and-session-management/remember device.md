# Summerville Credit Union — Remember Me Feature Guide

**Platform:** Summerville nFinia Digital Banking (Mobile) **Feature:** Remember Me **Module:** Login & Authentication > Session Persistence **Prepared by:** Jeeva Krishnamurthy, Senior Product Manager — Business Banking | Tyfone **Date:** April 2026

***

## Section 1 — Product Summary

The **Remember Me** feature within Summerville Credit Union's nFinia mobile banking platform allows members to persist their username across sessions, eliminating the need to re-enter login credentials from scratch on every visit. When enabled, the Username field on the Log In screen is automatically pre-populated the next time the member opens the app—reducing login friction to a single password entry before tapping Log In.

This feature serves all registered member types: retail members checking balances daily, and business banking members managing cash flow and approving transactions on the go. For frequent users, removing the username re-entry step meaningfully reduces the cognitive load of repeated logins. For the credit union, it reduces abandoned login attempts and contributes to higher engagement with the mobile channel—without sacrificing security, since the password is never persisted and full credential validation still occurs on every session.

Remember Me lives within the Login & Authentication module at the entry point of the nFinia mobile app. It is opt-in and device-scoped: enabling it on one device does not affect login behavior on other devices. Importantly, the feature should not be recommended on shared devices, and the platform does not persist the feature state if the app is uninstalled and reinstalled. For business banking members, Remember Me pairs well with Face ID to deliver the fastest possible secure login experience when time-sensitive approvals—such as wire transfers or ACH batches—are needed.

### At a Glance

| Attribute            | Detail                                                                            |
| -------------------- | --------------------------------------------------------------------------------- |
| Feature Name         | Remember Me                                                                       |
| Module               | Login & Authentication > Session Persistence                                      |
| User Roles           | All registered members (Retail, Business Owner, Sub User, Authorized Signer)      |
| Access Level         | Opt-in; device-scoped                                                             |
| Key Actions          | Enable Remember Me (checkbox), username auto-population on return                 |
| Regulatory Relevance | Session security; username-only persistence (password never stored); device trust |

***

## Section 2 — Use Cases

| Use Case                                      | Who Uses It                                                                        | What They Do                                                                          | Business Value                                                      |
| --------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| Frequent daily login                          | Retail member checking balances or activity each morning                           | Checks Remember Me on first login; username auto-populates on all subsequent visits   | Reduces daily login time; increases mobile channel engagement       |
| Business member approving urgent transactions | Business Owner or Authorized Signer needing to quickly approve a wire or ACH batch | Remember Me pre-populates username; member enters only password to authenticate fast  | Reduces authorization latency for time-sensitive payment approvals  |
| First-time opt-in during login                | Any new or returning member who wants to enable the feature                        | Checks the Remember Me checkbox on the Log In screen before tapping Log In            | One-time setup; no additional configuration required                |
| Shared device — feature not recommended       | Member using a shared or public device                                             | Leaves Remember Me unchecked; username must be entered each session                   | Prevents credential exposure on non-personal devices                |
| App reinstall or username change              | Member who reinstalled the app or updated their username                           | Remember Me state is cleared; member re-enters username and may re-enable the feature | Ensures username persistence stays aligned with current credentials |

These use cases illustrate that Remember Me delivers the most value for members who log in frequently on a personal device—particularly business banking users who need rapid access to approve transactions. Credit unions should surface guidance to members that this feature is intended for personal devices only.

***

## Section 3 — End-to-End Workflow

### 3.1 Prerequisites

* Member must have an active, enrolled Summerville CU account on the nFinia platform
* Member must be logging in from a personal device (not shared)
* App must be installed and the member must be on the Log In screen
* Remember Me must not have been previously enabled on this device (or was cleared by app reinstall)

### 3.2 Step-by-Step Flow

**Step 1 — App Launch: Welcome Screen** The member opens the Summerville app and is presented with the **Welcome Screen**. The screen shows Enroll and Log In CTAs along with pre-login quick-action icons. The member taps **Log In** to proceed.

<figure><img src="/.gitbook/assets/Welcome_Screen___Summerville_nFinia_1.jpeg" alt="Welcome Screen — tap Log In to access Remember Me" width="340"><figcaption></figcaption></figure>


**Step 2 — Log In Screen Presented** The member lands on the **Log In screen**, which displays Username and Password input fields, the **Remember Me** checkbox, the **Enable Face ID** checkbox, and the Log In button.

<figure><img src="/.gitbook/assets/Log_In_Screen___Summerville_nFinia_2.jpeg" alt="Log In screen with Remember Me checkbox" width="340"><figcaption></figcaption></figure>


**Step 3 — Enter Credentials** The member types their **Username** and **Password** in the respective fields.

<figure><img src="/.gitbook/assets/Log_In_Screen___Summerville_nFinia_2.jpeg" alt="Log In screen — enter Username and Password" width="340"><figcaption></figcaption></figure>


**Step 4 — Enable Remember Me** The member checks the **Remember Me** checkbox. A checkmark appears in the checkbox to confirm the selection. This action signals the platform to persist the username locally on the device after a successful login.

<figure><img src="/.gitbook/assets/Log_In_Screen___Summerville_nFinia_2.jpeg" alt="Remember Me checkbox — check to enable username persistence" width="340"><figcaption></figcaption></figure>


**Step 5 — Submit Login** The member taps the **Log In** button. The platform validates the credentials. On success, the member is routed to the Dashboard.

**Step 6 — Return Visit: Username Auto-Populated** On the next app launch, the Log In screen loads with the **Username field pre-populated** with the member's saved username. The member only needs to enter their password and tap Log In to authenticate.

<figure><img src="/.gitbook/assets/Log_In_Screen___Summerville_nFinia_2.jpeg" alt="Log In screen on return visit — Username field pre-populated" width="340"><figcaption></figcaption></figure>


### 3.3 Decision Points & Branching

* **Remember Me checked + login successful → Username persisted**: On next visit, the username field is pre-filled
* **Remember Me not checked → No persistence**: Username must be entered manually on every visit
* **App uninstalled and reinstalled → Remember Me cleared**: Member must re-enable on next login
* **Username changed → Stale username displayed**: Member must clear the pre-populated field, enter the new username, and re-check Remember Me

### 3.4 Completion & Confirmation

There is no explicit confirmation message when Remember Me is enabled. The visual checkmark in the checkbox serves as the in-context confirmation. The feature's effect becomes apparent on the next app launch when the username field is pre-populated. No audit log entry is generated for enabling Remember Me, as it is a client-side UX preference rather than a transactional event.

### 3.5 Error Handling

| Scenario                                             | What the Member Sees                                      | Recovery Path                                                               |
| ---------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------------------------- |
| Login fails after Remember Me is checked             | Login error message; Remember Me checkbox remains checked | Re-enter password; username stays pre-populated                             |
| Wrong username pre-populated (after username change) | Pre-filled username that no longer matches the account    | Clear the field, type the correct username, re-check Remember Me and log in |
| Feature unavailable after app update or reinstall    | Username field is blank on next launch                    | Re-enter username, re-check Remember Me to re-enable                        |

***

## Section 4 — Feature Overview (UI Walkthrough)

### Screen 1: Welcome Screen

The Welcome Screen is the unauthenticated landing page that every member encounters on app launch. It provides entry points to both Log In and Enroll. From here, the member taps **Log In** to reach the screen where Remember Me can be enabled.

![Welcome Screen — Summerville nFinia](../../../.gitbook/assets/Welcome_Screen___Summerville_nFinia_1.jpeg)

_Screenshot 1: Summerville CU Welcome Screen — the starting point before reaching the Log In screen where Remember Me is available._

| Field / Element                                        | Type              | Description                     | Notes                                            |
| ------------------------------------------------------ | ----------------- | ------------------------------- | ------------------------------------------------ |
| Summerville Logo                                       | Image/Label       | Branded header                  | Non-interactive                                  |
| Welcome Heading                                        | Label             | Entry-point title               | Non-interactive                                  |
| Enroll                                                 | Button (outlined) | Routes to new member enrollment | For members not yet registered                   |
| Log In                                                 | Button (filled)   | Navigates to the Log In screen  | Primary path to access Remember Me               |
| Accounts / Move Money / Check Deposit / Manage Devices | Icon Buttons      | Pre-login quick access          | Authentication required to complete most actions |
| Balance                                                | Pill Button       | Pre-login balance inquiry       | No credentials required                          |

***

### Screen 2: Log In Screen — Remember Me Checkbox

The Log In screen is where the **Remember Me** feature is accessed and enabled. The checkbox sits below the Password field, and when checked, instructs the platform to persist the username locally on the device for future sessions. The Password field is never persisted regardless of this setting.

![Log In Screen — Summerville nFinia](../../../.gitbook/assets/Log_In_Screen___Summerville_nFinia_2.jpeg)

_Screenshot 2: Summerville CU Log In Screen — the Remember Me checkbox (checked) is visible below the Password field, alongside the Enable Face ID option._

| Field / Element         | Type                | Description                                          | Notes                                                                               |
| ----------------------- | ------------------- | ---------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Back Arrow              | Icon Button         | Returns to Welcome Screen                            | Top-left                                                                            |
| Hamburger Menu          | Icon Button         | Opens navigation drawer                              | Top-right                                                                           |
| Username                | Text Input          | Member's registered username                         | Required; pre-populated on return visits when Remember Me is active                 |
| Password                | Text Input (masked) | Member's account password                            | Required; never persisted regardless of Remember Me setting                         |
| **Remember Me**         | **Checkbox**        | **Persists username across sessions on this device** | **Key feature; opt-in; device-scoped; shown checked in screenshot**                 |
| Enable Face ID          | Checkbox            | Registers biometric auth for future logins           | Optional; complements Remember Me for fastest login experience                      |
| Log In                  | Button (filled)     | Submits credentials                                  | Primary CTA; triggers authentication and, if Remember Me is checked, saves username |
| Enroll                  | Button (outlined)   | Routes to member enrollment                          | Secondary CTA                                                                       |
| I need help logging in  | Hyperlink           | Opens credential recovery flow                       | For members who have forgotten their username or password                           |
| Tap to see your balance | Pill (bottom)       | Pre-login balance inquiry                            | Persists on the login screen                                                        |

***

## Section 5 — Quick Reference

| Task                                  | Navigation Path                                                        | Who Can Do It                     | Notes                                                       |
| ------------------------------------- | ---------------------------------------------------------------------- | --------------------------------- | ----------------------------------------------------------- |
| Enable Remember Me                    | App launch → Log In → check Remember Me → Log In                       | All registered members            | One-time setup per device; re-enable after app reinstall    |
| Experience Remember Me (return visit) | App launch → Log In (username pre-populated) → enter password → Log In | Members who previously enabled it | Username field is auto-filled; only password entry required |
| Disable Remember Me                   | App launch → Log In → uncheck Remember Me → Log In                     | All registered members            | Username will no longer be persisted after next login       |
| Clear saved username (app reinstall)  | Uninstall and reinstall app                                            | Any member                        | Clears all local preferences including Remember Me          |
| Pair with Face ID for fastest login   | Log In → check Remember Me + Enable Face ID → Log In                   | Members with compatible devices   | Subsequent logins require only Face ID confirmation         |

***

_This guide was prepared by Jeeva Krishnamurthy, Senior Product Manager — Commercial & SMB Digital Banking, Tyfone. It reflects the Summerville Credit Union deployment of the nFinia platform as documented in the CSUM-01 report series._
