# Summerville Credit Union — Sneak Peek Feature Guide

**Platform:** Summerville CU nFinia Digital Banking (Mobile) **Feature:** Sneak Peek — Pre-Login Balance Visibility **Feature Coverage:** CSUM-01 · CSUM-23 **Prepared by:** Jeeva Krishnamurthy, Senior Product Manager, Business Banking — Tyfone **Date:** April 7, 2026

***

## Section 1 — Product Summary

Sneak Peek is a convenience feature in Summerville Credit Union's nFinia mobile banking platform that allows members to view their account balance on the pre-login Welcome screen — without requiring a full username/password/OTP authentication session. Members opt in per account through Account Settings, and once enabled, a **Balance** widget on the Welcome screen surfaces the configured account's current balance with a single tap or swipe.

The feature serves enrolled retail members who frequently check their balance without needing to conduct a transaction — a common behavior pattern among mobile banking users. Rather than requiring a full multi-factor authentication session for a read-only balance inquiry, Sneak Peek delivers just enough information to answer "How much do I have?" while keeping the member's full account access securely behind the login wall. The feature is per-account and opt-in only, meaning no account balance is ever exposed without an explicit member decision.

Why it matters for Summerville CU: balance checking is one of the highest-frequency, lowest-complexity digital banking interactions. By deflecting these low-value authentication events, Sneak Peek reduces unnecessary session load, lowers the risk of credential fatigue, and measurably improves the mobile experience for everyday members. It is also a meaningful differentiator in the credit union's digital channel — a feature that communicates member-centric design and competes directly with neobank UX patterns from Mercury, Relay, and similar challengers that have made frictionless balance visibility a baseline expectation.

### At a Glance

| Attribute            | Detail                                                                                                                   |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Feature Name         | Sneak Peek                                                                                                               |
| Module               | Welcome Screen (pre-login) · Account Settings (configuration)                                                            |
| User Roles           | Enrolled Retail Member                                                                                                   |
| Access Level         | Pre-login (balance view only); Account Settings requires full authentication                                             |
| Key Actions          | Enable Sneak Peek per account (toggle), View balance on Welcome screen                                                   |
| Configuration Path   | Dashboard → ≡ Menu → Settings → Account Settings → Sneak Peek toggle                                                     |
| Regulatory Relevance | No financial transaction exposure; member opt-in required; consistent with FFIEC guidance on low-risk read-only features |

***

## Section 2 — Use Cases

| Use Case                                                 | Who Uses It                    | What They Do                                                                                                                        | Business Value                                                                                      |
| -------------------------------------------------------- | ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Quick pre-login balance check                            | Enrolled member on the go      | Opens the app and taps Balance on the Welcome screen — no login required                                                            | Eliminates a full authentication session for a read-only inquiry; reduces session load and friction |
| Enabling Sneak Peek for the first time                   | New or existing member         | Authenticates, navigates to Account Settings, and turns on the Sneak Peek toggle for their primary checking account                 | One-time setup that permanently improves the day-to-day mobile experience                           |
| Enabling Sneak Peek for a secondary account              | Member with multiple accounts  | Repeats the Account Settings flow for a savings or secondary checking account                                                       | Allows members to monitor multiple balances at a glance pre-login                                   |
| Disabling Sneak Peek (privacy preference)                | Member sharing a device        | Turns off the Sneak Peek toggle in Account Settings                                                                                 | Ensures no balance information is visible to anyone who picks up the phone before login             |
| Using Balance widget alongside other pre-login shortcuts | Member performing a quick task | Taps Balance on Welcome screen, reviews balance, then proceeds to Move Money or Check Deposit without a separate login interruption | Increases pre-login feature engagement; reduces steps to action                                     |

Sneak Peek is a genuinely member-centric feature that credit unions can highlight in digital channel marketing and onboarding communications. For Summerville CU, positioning it as a transparency and convenience benefit — rather than a technical capability — resonates strongly with members who value the credit union's personal-service ethos.

***

## Section 3 — End-to-End Workflow

### 3.1 Prerequisites

* Member must be enrolled in Summerville CU nFinia digital banking
* Sneak Peek must be explicitly enabled per account in Account Settings (it is **off by default**)
* Full authentication (username + password + OTP) is required the first time to access Account Settings

### 3.2 Step-by-Step Flow: Enabling Sneak Peek

**Step 1 — Open the app (Welcome Screen)** The member opens the Summerville mobile app. The Welcome screen is displayed. Note the **Balance** widget at the bottom — it exists for all users but only shows data once Sneak Peek is configured. The member taps **Log In** to begin the authentication session needed to configure the feature.

<figure><img src="/.gitbook/assets/Welcome_Screen_showing_Balance_widget_and_pre-login_shortcut_1.jpeg" alt="Welcome Screen — open the app" width="340"><figcaption></figcaption></figure>


**Step 2 — Log In** On the Log In screen, the member enters their **Username** and **Password**. Optional checkboxes are available for **Remember me** (saves username) and **Enable Face ID** (registers biometrics for future logins). The member taps the **Log In** button to proceed.

<figure><img src="/.gitbook/assets/Log_In_screen_with_username__password__Remember_Me_and_Face__2.jpeg" alt="Log In screen — enter credentials" width="340"><figcaption></figcaption></figure>


**Step 3 — Select MFA Verification Method** The platform validates credentials and prompts for step-up authentication. The **Verification** screen lists available OTP delivery methods — SMS text or voice call — tied to the member's registered phone numbers (displayed in masked format for security). The member selects their preferred method.

<figure><img src="/.gitbook/assets/Verification_screen_showing_Text_and_Call_OTP_delivery_optio_3.jpeg" alt="OTP delivery method selection screen" width="340"><figcaption></figcaption></figure>


**Step 4 — Enter One-Time Passcode** The **User Verification** screen confirms where the OTP was sent and provides an input field for the passcode. A 60-second countdown is shown before a resend is available. The member enters the OTP and taps **Submit**.

<figure><img src="/.gitbook/assets/OTP_entry_screen_showing_masked_destination_number__passcode_4.jpeg" alt="OTP entry screen" width="340"><figcaption></figcaption></figure>


**Step 5 — Authenticated Dashboard** On successful OTP validation, the member lands on the **Dashboard**. The personalized greeting, account summary, and navigation bar confirm full authenticated access. The member now opens the side menu to reach Settings.

<figure><img src="/.gitbook/assets/Dashboard_showing_personalized_greeting__Credit_Score___Offe_5.jpeg" alt="Dashboard after successful login" width="340"><figcaption></figcaption></figure>


**Step 6 — Open the Side Menu** The member taps the hamburger icon (≡) at the top-right of the Dashboard. The **side menu / profile drawer** slides in, displaying the member's name (DONALD BLAKE), last login time, membership context, and a list of navigation items. The member taps **Settings**.

<figure><img src="/.gitbook/assets/Side_menu_showing_member_profile__All_Personal_Memberships___6.jpeg" alt="Side menu — hamburger icon" width="340"><figcaption></figcaption></figure>


**Step 7 — Settings Hub** The **Settings** screen presents three options: Account Settings, Personal Information, and User ID and Password. The member taps **Account Settings**.

<figure><img src="/.gitbook/assets/Settings_screen_with_Account_Settings__Personal_Information__7.jpeg" alt="Settings hub screen" width="340"><figcaption></figcaption></figure>


**Step 8 — Account Settings: Enable Sneak Peek** The **Account Settings** screen loads with the target account pre-selected (e.g. Retail Checking Account #0001). The member sees the **Sneak Peek** toggle in the Settings panel — by default it is **off**. The member taps the toggle to turn it **on**. The toggle turns green/active.

<figure><img src="/.gitbook/assets/Account_Settings_with_Sneak_Peek_toggle_enabled__green___Act_9.jpeg" alt="Account Settings — Sneak Peek toggle enabled" width="340"><figcaption></figcaption></figure>


**Step 9 — Confirmation & Pre-Login Use** A toast notification confirms: _"Your account settings have been updated."_ From this point forward, when the member opens the app without logging in, tapping **Balance** on the Welcome screen reveals the configured account's current balance — no authentication required.

<figure><img src="/.gitbook/assets/Account_Settings_with_Sneak_Peek_toggle_enabled__green___Act_9.jpeg" alt="Sneak Peek enabled — accessible from Welcome Screen" width="340"><figcaption></figcaption></figure>


### 3.3 Decision Points & Branching

* **Sneak Peek off (default):** Balance widget on the Welcome screen shows no data or prompts the member to enable the feature
* **Sneak Peek on for one account:** Only that account's balance is surfaced pre-login; other accounts remain hidden
* **Multiple accounts with Sneak Peek on:** The Balance widget may display a summary or allow the member to cycle between configured accounts (per FI configuration)
* **Member disables Sneak Peek:** The toggle is turned off in Account Settings; balance immediately stops appearing pre-login on next app open
* **Show/Hide toggle also off:** If an account is hidden (Show/Hide = off), Sneak Peek for that account will not function regardless of toggle state

### 3.4 Completion & Confirmation

* The toast _"Your account settings have been updated."_ confirms the Sneak Peek toggle state was saved
* On next app open, the Balance widget on the Welcome screen displays the configured account's balance
* No audit-triggering transaction occurs; this is a read-only display preference change

### 3.5 Error Handling

* **Authentication failure during setup:** Member cannot reach Account Settings if login fails; must resolve credentials first
* **OTP not received:** Use the Retry option after the 60-second countdown, or select a different delivery method
* **Balance not appearing after enabling:** Check that the Show/Hide toggle for the same account is also in the "shown" (on) state; hidden accounts suppress all display including Sneak Peek

***

## Section 4 — Feature Overview (UI Walkthrough)

### Screen 1 — Welcome Screen: Sneak Peek Entry Point

The Welcome screen is where the Sneak Peek feature delivers its value. The **Balance** widget at the bottom of the screen — available before any login — is the pre-login balance display surface. When Sneak Peek is not yet configured, this widget either shows a prompt or is inactive. Once enabled for one or more accounts, it reveals the current balance on tap.

![Welcome Screen showing Balance widget and pre-login shortcuts](../../../.gitbook/assets/Welcome_Screen_showing_Balance_widget_and_pre-login_shortcut_1.jpeg)

| Field / Element | Type                               | Description                                                                               | Notes                                                      |
| --------------- | ---------------------------------- | ----------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| Balance         | Slide-up widget (bottom of screen) | **Sneak Peek surface.** Displays the configured account's balance without requiring login | Only active once Sneak Peek is enabled in Account Settings |
| Accounts        | Shortcut icon                      | Pre-login access to account views                                                         | Limited functionality without full auth                    |
| Move Money      | Shortcut icon                      | Pre-login shortcut to Move Money hub                                                      | Transaction actions require login                          |
| Check Deposit   | Shortcut icon                      | Pre-login shortcut to mobile deposit                                                      | Requires full authentication                               |
| Manage Devices  | Shortcut icon                      | Pre-login device management shortcut                                                      | Requires authentication                                    |
| Log In          | Button (Primary)                   | Full authenticated login entry point                                                      | Required to configure Sneak Peek in Account Settings       |
| Enroll          | Button (Secondary)                 | New member enrollment flow                                                                | For first-time digital banking users                       |

***

### Screen 2 — Log In: Authentication to Reach Account Settings

Full authentication is required once to enable Sneak Peek. The Log In screen collects credentials before routing the member through OTP verification to the authenticated session where Account Settings is accessible.

![Log In screen with username, password, Remember Me and Face ID options](../../../.gitbook/assets/Log_In_screen_with_username__password__Remember_Me_and_Face__2.jpeg)

| Field / Element        | Type                    | Description                               | Notes                                            |
| ---------------------- | ----------------------- | ----------------------------------------- | ------------------------------------------------ |
| Username               | Text input              | Member's registered username              | Required                                         |
| Password               | Password input (masked) | Member's account password                 | Show/hide toggle available                       |
| Remember me            | Checkbox                | Pre-populates username on future visits   | Optional convenience                             |
| Enable Face ID         | Checkbox                | Registers biometric login for this device | Speeds up future logins                          |
| Log In                 | Button (Primary CTA)    | Submits credentials; triggers OTP step-up | Entry point to the Sneak Peek configuration path |
| I need help logging in | Link                    | Account recovery / forgot credentials     | Out-of-scope for Sneak Peek setup                |

***

### Screen 3 — Verification: Select OTP Delivery Method

After credentials are validated, MFA is triggered. The member selects how to receive their one-time passcode. This step is part of the one-time setup path to reach Account Settings and configure Sneak Peek.

![Verification screen showing Text and Call OTP delivery options with masked phone numbers](../../../.gitbook/assets/Verification_screen_showing_Text_and_Call_OTP_delivery_optio_3.jpeg)

| Field / Element               | Type           | Description                                        | Notes                                                    |
| ----------------------------- | -------------- | -------------------------------------------------- | -------------------------------------------------------- |
| Text (+1 X\*\*-\*\*\*-\*\*XX) | Selectable row | Sends OTP via SMS to a masked registered number    | Multiple numbers displayed if member has several on file |
| Call (+1 X\*\*-\*\*\*-\*\*XX) | Selectable row | Delivers OTP via automated voice call              | Fallback for members who cannot receive SMS              |
| Refresh                       | Inline link    | Reloads contact info if recently updated at branch | Useful after a phone number change                       |

***

### Screen 4 — User Verification: OTP Entry

The passcode entry step completes MFA. Once the OTP is submitted and validated, the member gains full authenticated access and can navigate to Account Settings to enable Sneak Peek.

![OTP entry screen showing masked destination number, passcode field, retry countdown and Submit button](../../../.gitbook/assets/OTP_entry_screen_showing_masked_destination_number__passcode_4.jpeg)

| Field / Element       | Type             | Description                                    | Notes                              |
| --------------------- | ---------------- | ---------------------------------------------- | ---------------------------------- |
| OTP destination label | Display label    | Confirms the masked number the OTP was sent to | Read-only                          |
| Enter passcode        | Text input       | Field for the received one-time passcode       | Required; typically 6 digits       |
| Retry countdown       | Timer label      | Shows seconds until resend is available        | Prevents OTP flooding              |
| Submit                | Button (Primary) | Validates the OTP and completes authentication | Unlocks access to Account Settings |

***

### Screen 5 — Authenticated Dashboard: Post-Login State

After successful authentication, the member lands on the Dashboard. This is the starting point for navigating to Account Settings to configure Sneak Peek. The hamburger menu (≡) in the top-right opens the side menu.

![Dashboard showing personalized greeting, Credit Score & Offers, All Accounts summary and Retail Checking account card](../../../.gitbook/assets/Dashboard_showing_personalized_greeting__Credit_Score___Offe_5.jpeg)

| Field / Element      | Type            | Description                                         | Notes                                                              |
| -------------------- | --------------- | --------------------------------------------------- | ------------------------------------------------------------------ |
| Greeting             | Display label   | Personalized salutation confirming successful login | Time-of-day aware                                                  |
| ≡ (Menu icon)        | Navigation icon | Opens the side menu / profile drawer                | **Path to Settings → Account Settings → Sneak Peek**               |
| All Accounts summary | Summary card    | Aggregate balance view across all accounts          | Background context for which account to enable Sneak Peek on       |
| Account card         | Account tile    | Individual account with balance and activity        | The account shown here can be the one Sneak Peek is configured for |

***

### Screen 6 — Side Menu: Navigation to Settings

The side menu provides the navigation path to Account Settings where Sneak Peek is configured. The member taps **Settings** from this menu to proceed.

![Side menu showing member profile, All Personal Memberships, Enable Alerts toggle, Settings, Alert Settings, Trust this Device, Apply for Loans, Statements and eNotices, Digital Wallet and Log Out](../../../.gitbook/assets/Side_menu_showing_member_profile__All_Personal_Memberships___6.jpeg)

| Field / Element          | Type              | Description                                                      | Notes                                                                   |
| ------------------------ | ----------------- | ---------------------------------------------------------------- | ----------------------------------------------------------------------- |
| Settings                 | Navigation row    | **Direct path to Account Settings and Sneak Peek configuration** | Sub-options: Account Settings, Personal Information, User ID & Password |
| Member name & last login | Display label     | Confirms authenticated session identity                          | Shows name and timestamp                                                |
| All Personal Memberships | Membership chip   | Active membership context                                        | Switch Profile link for multi-membership members                        |
| Enable Alerts            | Toggle            | Master alert on/off switch                                       | Not related to Sneak Peek                                               |
| Log out                  | Bottom bar button | Terminates session                                               | After Sneak Peek is saved, member can log out; feature persists         |

***

### Screen 7 — Settings Hub

The Settings hub offers three sub-sections. **Account Settings** is the destination for Sneak Peek configuration.

![Settings screen with Account Settings, Personal Information and User ID and Password options](../../../.gitbook/assets/Settings_screen_with_Account_Settings__Personal_Information__7.jpeg)

| Field / Element      | Type           | Description                                                              | Notes                             |
| -------------------- | -------------- | ------------------------------------------------------------------------ | --------------------------------- |
| Account Settings     | Navigation row | **Opens Sneak Peek configuration (and other account-level preferences)** | Icon: bank/institution symbol     |
| Personal Information | Navigation row | Contact details and device management                                    | Not required for Sneak Peek setup |
| User ID and Password | Navigation row | Credential and OTP preference changes                                    | Not required for Sneak Peek setup |

***

### Screen 8 — Account Settings: Sneak Peek Toggle (Default Off State)

The Account Settings screen is where Sneak Peek is enabled. By default, the Sneak Peek toggle is **off**. The member selects the target account from the dropdown and taps the Sneak Peek toggle to turn it on.

![Account Settings showing Retail Checking Account selected, Account title Rename option, Show/Hide toggle on, Sneak Peek toggle off, Activities since last login toggle on](../../../.gitbook/assets/Account_Settings_showing_Retail_Checking_Account_selected__A_8.jpeg)

| Field / Element                    | Type                  | Description                                                                                  | Notes                                                          |
| ---------------------------------- | --------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| Account selector                   | Dropdown              | Selects the account to configure                                                             | Required; configure one account at a time                      |
| Account title / Rename             | Label + link          | Displays and allows renaming the account's display label                                     | Optional; unrelated to Sneak Peek                              |
| Show / Hide toggle                 | Toggle                | Controls whether the account appears in digital banking at all                               | **Must be ON (shown) for Sneak Peek to function**              |
| **Sneak Peek toggle**              | **Toggle (off → on)** | **When turned on, enables pre-login balance display for this account on the Welcome screen** | **Default: off. This is the primary action for this feature.** |
| Activities since last login toggle | Toggle                | Shows a since-last-login badge on the account's Dashboard card                               | Independent of Sneak Peek                                      |

***

### Screen 9 — Account Settings: Sneak Peek Enabled + Confirmation Toast

After the member taps the Sneak Peek toggle to the on position and saves, the confirmation toast _"Your account settings have been updated."_ is displayed. The Sneak Peek toggle is now shown in its active (green) state. From this point forward, the account's balance is visible on the Welcome screen without logging in.

![Account Settings with Sneak Peek toggle enabled (green), Activities since last login on, and Your account settings have been updated toast at the bottom](../../../.gitbook/assets/Account_Settings_with_Sneak_Peek_toggle_enabled__green___Act_9.jpeg)

| Field / Element                                | Type                    | Description                                                                    | Notes                                               |
| ---------------------------------------------- | ----------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------- |
| **Sneak Peek toggle (enabled)**                | **Toggle (on / green)** | **Sneak Peek is now active for this account**                                  | **Balance will appear on Welcome screen pre-login** |
| Activities since last login toggle (on)        | Toggle (on / green)     | Activity badge remains enabled on Dashboard                                    | Independent setting                                 |
| Set this account as a default for              | Section label           | Default payment/transfer account preferences                                   | Visible on scroll; unrelated to Sneak Peek          |
| **"Your account settings have been updated."** | **Toast notification**  | **Confirms Sneak Peek (and any other toggle changes) were saved successfully** | **Auto-dismisses after a few seconds**              |

***

## Section 5 — Quick Reference

| Task                                        | Navigation Path                                                                  | Who Can Do It                      | Notes                                                   |
| ------------------------------------------- | -------------------------------------------------------------------------------- | ---------------------------------- | ------------------------------------------------------- |
| Enable Sneak Peek for an account            | Log In → Dashboard → ≡ Menu → Settings → Account Settings → Sneak Peek toggle ON | Enrolled member (authenticated)    | Per-account setting; must be done once per account      |
| View balance without logging in             | Open app → Welcome Screen → Tap **Balance** widget                               | Any member with Sneak Peek enabled | No authentication required; balance is read-only        |
| Disable Sneak Peek                          | Dashboard → ≡ Menu → Settings → Account Settings → Sneak Peek toggle OFF         | Enrolled member (authenticated)    | Balance immediately stops appearing pre-login           |
| Enable Sneak Peek for a second account      | Repeat Account Settings flow, select second account                              | Enrolled member (authenticated)    | Each account is configured independently                |
| Rename an account shown via Sneak Peek      | Account Settings → Rename                                                        | Enrolled member (authenticated)    | The friendly name appears in the Balance widget         |
| Ensure Sneak Peek is working (troubleshoot) | Check Account Settings: Show/Hide must be ON, Sneak Peek must be ON              | Enrolled member (authenticated)    | Both toggles must be active for the feature to function |

***

_This guide was prepared by Jeeva Krishnamurthy, Senior Product Manager — Tyfone, as part of the Summerville Credit Union nFinia Feature Documentation Series. All screenshots reflect the live Summerville CU deployment captured April 7, 2026. Feature: Sneak Peek (CSUM-01, CSUM-23)._
