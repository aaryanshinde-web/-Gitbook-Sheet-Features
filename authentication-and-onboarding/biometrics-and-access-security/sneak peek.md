# Sneak Peek

## Summary

Sneak Peek is a convenience feature in Summerville Credit Union's nFinia mobile banking platform that allows you to view your account balance on the pre-login Welcome screen — without requiring a full username/password/OTP authentication session. You opt in per account through Account Settings, and once enabled, a **Balance** widget on the Welcome screen surfaces your configured account's current balance with a single tap or swipe.

The feature serves enrolled retail members who frequently check their balance without needing to conduct a transaction — a common behavior pattern among mobile banking users. Rather than requiring a full multi-factor authentication session for a read-only balance inquiry, Sneak Peek delivers just enough information to answer "How much do I have?" while keeping your full account access securely behind the login wall. The feature is per-account and opt-in only, meaning no account balance is ever exposed without your explicit decision.

Sneak Peek reduces unnecessary authentication events, lowers the risk of credential fatigue, and improves the mobile experience for everyday banking.

**At a Glance**

| Attribute          | Detail                                                                       |
| ------------------ | ---------------------------------------------------------------------------- |
| Feature Name       | Sneak Peek                                                                   |
| Module             | Banking › Welcome Screen (pre-login) · Account Settings (configuration)      |
| User Roles         | Enrolled Retail Member                                                       |
| Access Level       | Pre-login (balance view only); Account Settings requires full authentication |
| Key Actions        | Enable Sneak Peek per account (toggle), View balance on Welcome screen       |
| Configuration Path | Dashboard › Menu › Settings › Account Settings › Sneak Peek toggle           |

## Use Cases

| Use Case                                                 | Who Uses It                               | What They Do                                                                                                    | Business Value                                                                                      |
| -------------------------------------------------------- | ----------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Quick pre-login balance check                            | You on the go                             | Open the app and tap Balance on the Welcome screen — no login required                                          | Eliminates a full authentication session for a read-only inquiry; reduces session load and friction |
| Enabling Sneak Peek for the first time                   | You new to the feature or existing member | Authenticate, navigate to Account Settings, and turn on the Sneak Peek toggle for your primary checking account | One-time setup that permanently improves the day-to-day mobile experience                           |
| Enabling Sneak Peek for a secondary account              | You with multiple accounts                | Repeat the Account Settings flow for a savings or secondary checking account                                    | Allows you to monitor multiple balances at a glance pre-login                                       |
| Disabling Sneak Peek (privacy preference)                | You sharing a device                      | Turn off the Sneak Peek toggle in Account Settings                                                              | Ensures no balance information is visible to anyone who picks up the phone before login             |
| Using Balance widget alongside other pre-login shortcuts | You performing a quick task               | Tap Balance on Welcome screen, review balance, then proceed to Move Money or Check Deposit                      | Increases pre-login feature engagement; reduces steps to action                                     |

## Step-by-Step Guide: Enabling Sneak Peek

**Step 1 — Open the App (Welcome Screen)**

You open the Summerville mobile app. The Welcome screen is displayed. Note the **Balance** widget at the bottom — it exists for all users but only shows data once Sneak Peek is configured. Tap **Log In** to begin the authentication session needed to configure the feature.

<figure><img src="../../.gitbook/assets/Welcome_Screen_showing_Balance_widget_and_pre-login_shortcut_1.jpeg" alt="Welcome Screen" width="340"><figcaption></figcaption></figure>

**Step 2 — Log In**

On the Log In screen, enter your **Username** and **Password**. Optional checkboxes are available for **Remember me** (saves username) and **Enable Face ID** (registers biometrics for future logins). Tap the **Log In** button to proceed.

<figure><img src="../../.gitbook/assets/Log_In_screen_with_username__password__Remember_Me_and_Face__2.jpeg" alt="Log In screen" width="340"><figcaption></figcaption></figure>

**Step 3 — Select MFA Verification Method**

The platform validates your credentials and prompts for step-up authentication. The **Verification** screen lists available OTP delivery methods — SMS text or voice call — tied to your registered phone numbers (displayed in masked format for security). Select your preferred method.

<figure><img src="../../.gitbook/assets/Verification_screen_showing_Text_and_Call_OTP_delivery_optio_3.jpeg" alt="OTP delivery method selection screen" width="340"><figcaption></figcaption></figure>

**Step 4 — Enter One-Time Passcode**

The **User Verification** screen confirms where the OTP was sent and provides an input field for the passcode. A 60-second countdown is shown before a resend is available. Enter the OTP and tap **Submit**.

<figure><img src="../../.gitbook/assets/OTP_entry_screen_showing_masked_destination_number__passcode_4.jpeg" alt="OTP entry screen" width="340"><figcaption></figcaption></figure>

**Step 5 — Authenticated Dashboard**

On successful OTP validation, you land on the **Dashboard**. The personalized greeting, account summary, and navigation bar confirm full authenticated access. Now open the side menu to reach Settings.

<figure><img src="../../.gitbook/assets/Dashboard_showing_personalized_greeting__Credit_Score___Offe_5.jpeg" alt="Dashboard after successful login" width="340"><figcaption></figcaption></figure>

**Step 6 — Open the Side Menu**

Tap the hamburger icon (≡) at the top-right of the Dashboard. The **side menu / profile drawer** slides in, displaying your name, last login time, membership context, and a list of navigation items. Tap **Settings**.

<figure><img src="../../.gitbook/assets/Side_menu_showing_member_profile__All_Personal_Memberships___6.jpeg" alt="Side menu" width="340"><figcaption></figcaption></figure>

**Step 7 — Settings Hub**

The **Settings** screen presents three options: Account Settings, Personal Information, and User ID and Password. Tap **Account Settings**.

<figure><img src="../../.gitbook/assets/Settings_screen_with_Account_Settings__Personal_Information__7.jpeg" alt="Settings hub screen" width="340"><figcaption></figcaption></figure>

**Step 8 — Account Settings: Enable Sneak Peek**

The **Account Settings** screen loads with your target account pre-selected (e.g. Retail Checking Account #0001). You see the **Sneak Peek** toggle in the Settings panel — by default it is **off**. Tap the toggle to turn it **on**. The toggle turns green/active.

<figure><img src="../../.gitbook/assets/Account_Settings_showing_Retail_Checking_Account_selected__A_8.jpeg" alt="Account Settings — Sneak Peek toggle" width="340"><figcaption></figcaption></figure>

**Step 9 — Confirmation & Pre-Login Use**

A toast notification confirms: _"Your account settings have been updated."_ From this point forward, when you open the app without logging in, tapping **Balance** on the Welcome screen reveals your configured account's current balance — no authentication required.

<figure><img src="../../.gitbook/assets/Account_Settings_with_Sneak_Peek_toggle_enabled__green___Act_9.jpeg" alt="Sneak Peek enabled" width="340"><figcaption></figcaption></figure>

## Decision Points

* **Sneak Peek off (default):** Balance widget on the Welcome screen shows no data or prompts you to enable the feature
* **Sneak Peek on for one account:** Only that account's balance is surfaced pre-login; other accounts remain hidden
* **Multiple accounts with Sneak Peek on:** The Balance widget may display a summary or allow you to cycle between configured accounts
* **Disabling Sneak Peek:** Turn off the toggle in Account Settings; balance immediately stops appearing pre-login on next app open
* **Show/Hide toggle also off:** If an account is hidden (Show/Hide = off), Sneak Peek for that account will not function regardless of toggle state

## Error Handling

| Scenario                             | Your Experience                                                                           | Recovery                                                                               |
| ------------------------------------ | ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Authentication failure during setup  | You cannot reach Account Settings if login fails                                          | Resolve credentials first                                                              |
| OTP not received                     | Use the Retry option after the 60-second countdown, or select a different delivery method | Try again after countdown expires                                                      |
| Balance not appearing after enabling | Sneak Peek is on but balance is not visible                                               | Check that the Show/Hide toggle for the same account is also in the "shown" (on) state |

## Welcome Screen Reference

| Field / Element | Type                               | Description                                                                            |
| --------------- | ---------------------------------- | -------------------------------------------------------------------------------------- |
| Balance         | Slide-up widget (bottom of screen) | Sneak Peek surface. Displays your configured account's balance without requiring login |
| Accounts        | Shortcut icon                      | Pre-login access to account views                                                      |
| Move Money      | Shortcut icon                      | Pre-login shortcut to Move Money hub                                                   |
| Check Deposit   | Shortcut icon                      | Pre-login shortcut to mobile deposit                                                   |
| Manage Devices  | Shortcut icon                      | Pre-login device management shortcut                                                   |
| Log In          | Button (Primary)                   | Full authenticated login entry point                                                   |
| Enroll          | Button (Secondary)                 | New member enrollment flow                                                             |

## Quick Reference

| Task                                        | Navigation Path                                                                | Who Can Do It                      | Notes                                                   |
| ------------------------------------------- | ------------------------------------------------------------------------------ | ---------------------------------- | ------------------------------------------------------- |
| Enable Sneak Peek for an account            | Log In › Dashboard › Menu › Settings › Account Settings › Sneak Peek toggle ON | You (authenticated)                | Per-account setting; must be done once per account      |
| View balance without logging in             | Open app › Welcome Screen › Tap **Balance** widget                             | Any member with Sneak Peek enabled | No authentication required; balance is read-only        |
| Disable Sneak Peek                          | Dashboard › Menu › Settings › Account Settings › Sneak Peek toggle OFF         | You (authenticated)                | Balance immediately stops appearing pre-login           |
| Enable Sneak Peek for a second account      | Repeat Account Settings flow, select second account                            | You (authenticated)                | Each account is configured independently                |
| Rename an account shown via Sneak Peek      | Account Settings › Rename                                                      | You (authenticated)                | The friendly name appears in the Balance widget         |
| Ensure Sneak Peek is working (troubleshoot) | Check Account Settings: Show/Hide must be ON, Sneak Peek must be ON            | You (authenticated)                | Both toggles must be active for the feature to function |
