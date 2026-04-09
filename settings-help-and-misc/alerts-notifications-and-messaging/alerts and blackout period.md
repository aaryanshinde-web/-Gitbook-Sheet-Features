# Alerts & Notifications — Feature Guide

**Summerville Credit Union | nFinia Digital Banking Platform** _Prepared by Jeeva Krishnamurthy, Senior Product Manager — Business Banking, Tyfone_

***

## Section 1 — Product Summary

The Alerts & Notifications feature in Summerville Credit Union's nFinia platform gives You real-time visibility into the activity on their accounts. You can subscribe to a range of alerts—from balance thresholds and deposit confirmations to security events like failed login attempts—and choose exactly how they receive them: push notification to a trusted device, SMS to a registered phone number, or email to a linked address. The system distinguishes between **Optional Alerts**, which You configure themselves, and **Mandatory Alerts**, which the platform automatically delivers regardless of individual preferences whenever security-critical events occur (e.g., password changes, account lockouts, new remembered device additions).

The feature is organized under **Alert Settings**, accessible via More > Alerts, and is composed of four tabs: **General Alerts**, **Account-Specific Alerts**, **Alert Settings**, and **Do-Not-Disturb**. Together these tabs give You fine-grained control over what they hear about, how they hear about it, and when they can be reached. For the credit union, this translates directly into reduced inbound support volume (You self-serve on transaction questions), stronger fraud detection outcomes (You receive and act on security alerts), and higher digital channel engagement.

The Do-Not-Disturb (DND) sub-feature extends alert control further by letting You suppress non-mandatory alert delivery during defined quiet hours—a timezone-aware window set to your local time zone. Mandatory alerts bypass DND by design, ensuring security-critical communications are never silenced.

| Attribute                | Detail                                                                                                                                        |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Feature Name**         | Alerts & Notifications                                                                                                                        |
| **Module**               | More > Alerts (General Alerts, Account-Specific Alerts, Alert Settings, Do-Not-Disturb)                                                       |
| **User Roles**           | Retail Member (all authenticated users)                                                                                                       |
| **Access Level**         | Authenticated member; OTP verification required at login                                                                                      |
| **Key Actions**          | Enable/disable alerts, configure alert channels, add account-specific alerts, set optional alert preferences, configure Do-Not-Disturb period |
| **Regulatory Relevance** | BSA/AML-adjacent fraud detection; mandatory security alerts support NCUA examination expectations for member authentication safeguards        |

***

## Section 2 — Use Cases

| Use Case                                  | Who Uses It   | What They Do                                                                                                                                                                         | Business Value                                                                                                      |
| ----------------------------------------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| **Enable alert delivery channels**        | Retail Member | Navigates to Alert Settings tab, confirms or adjusts push, SMS, and email toggles to select preferred delivery channels                                                              | Ensures alerts reach you on their preferred channel; reduces missed notifications and support calls          |
| **Add an account-specific balance alert** | Retail Member | Selects Account-Specific Alerts tab, clicks "Add a new alert" under Balance Alerts, selects account, sets condition (e.g., Less than $1,000), saves                                  | Proactively warns You of low balances, reducing overdraft events and associated fees                            |
| **Configure optional general alerts**     | Retail Member | On General Alerts tab, sets per-event preferences (Send all alerts / Send success alerts / Send failure alerts / Disable alerts) for events like Stop check request or Check reorder | Reduces noise for You who only care about outcomes, while keeping those who want full visibility fully informed |
| **Set a Do-Not-Disturb quiet period**     | Retail Member | Navigates to Do-Not-Disturb tab, sets timezone, start time, and end time; confirms                                                                                                   | Prevents late-night alert fatigue; improves member satisfaction and alert engagement rates during active hours      |
| **Edit an existing DND period**           | Retail Member | On Do-Not-Disturb tab, clicks Edit next to the active period, adjusts times, saves                                                                                                   | Gives You ongoing control without requiring them to remove and recreate preferences                             |
| **Remove a DND period**                   | Retail Member | On Do-Not-Disturb tab, clicks Remove; system confirms removal and restores full-hour alert delivery                                                                                  | Allows You to re-enable all-hours alerting when their schedule changes (e.g., new work shift)                   |

Account-specific and general alerts together give Summerville CU You a layered notification model that mirrors what business-class banking platforms offer—a meaningful differentiator for credit unions competing with larger FIs for financially engaged You.

***

## Section 3 — End-to-End Workflow

### 3.1 Prerequisites

* Member holds an active Summerville CU account enrolled in online banking.
* you have at least one registered contact (phone number or email) on file for OTP and alert delivery.
* your device is enrolled as trusted, or you are prepared to complete OTP verification at login.

***

### 3.2 Step-by-Step Flow — Alert Preferences (Channel Setup)

**Step 1 — Log in to Online Banking**

you navigate to the Summerville CU Online Banking portal and enters their User ID and password, then clicks **Log in**.

<figure><img src="/.gitbook/assets/Screenshot_1_1.png" alt="Screenshot 1" width="620"><figcaption></figcaption></figure>

***

**Step 2 — Complete OTP Verification (Select Method)**

The system prompts for a One-Time Passcode. you select how to receive it: Send me a message, Call me, or Send me an email.

<figure><img src="/.gitbook/assets/Screenshot_2_2.png" alt="Screenshot 2" width="620"><figcaption></figcaption></figure>

***

**Step 3 — Select Contact Number**

After choosing "Send me a message," you select the registered phone number to receive the OTP.

<figure><img src="/.gitbook/assets/Screenshot_3_3.png" alt="Screenshot 3" width="620"><figcaption></figcaption></figure>

***

**Step 4 — Enter OTP**

you enter the 6-digit code sent to their selected contact. The **Remember Device/Browser** option is available to skip OTP on future logins from this device.

<figure><img src="/.gitbook/assets/Screenshot_4_4.png" alt="Screenshot 4" width="620"><figcaption></figcaption></figure>

***

**Step 5 — Dashboard Loads**

After successful authentication, you land on the main Dashboard showing account balances and the Quick Transfer panel.

<figure><img src="/.gitbook/assets/Screenshot_5_5.png" alt="Screenshot 5" width="620"><figcaption></figcaption></figure>

***

**Step 6 — Open More > Alert Settings**

you click **More** in the navigation bar. A panel expands showing Alerts options: Account Alerts, General Alerts, Do-Not-Disturb, and Alert Settings. you click **Alert Settings**.

<figure><img src="/.gitbook/assets/Screenshot_6_6.png" alt="Screenshot 6" width="620"><figcaption></figcaption></figure>

***

**Step 7 — Alert Settings Tab: Configure Channels**

The **Alert Settings** tab loads. you can:

* Toggle **Enable alerts** on or off (disabling suspends delivery without deleting configured alerts)
* Toggle each delivery channel independently: **Push notifications**, **SMS alerts**, **Email alerts**

The screen displays the registered phone number and email address that alerts will be sent to.

<figure><img src="/.gitbook/assets/Screenshot_7_7.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

***

### 3.3 Step-by-Step Flow — Add an Account-Specific Alert

Steps 1–6 are identical to the Alert Preferences flow above (login → OTP → Dashboard → More → Alert Settings). At Step 6, you instead navigates to the **Account-Specific Alerts** tab.

**Step 7 — Account-Specific Alerts Tab**

The tab displays four alert categories, each with an "Add a new alert" link:

* Balance alerts
* Periodic balance alerts
* Deposit alerts
* Withdrawal alerts

<figure><img src="/.gitbook/assets/Screenshot_7_8.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

***

**Step 8 — Open Add Alert Modal**

you click **+ Add a new alert** under Balance Alerts. A modal titled **"Add new 'Available balance alert'"** appears. you:

1. Selects the account from the dropdown (e.g., Retail Checking Account #0001)
2. Sets the condition: "Alert me if my available balance is [Less than] [$1,000]"

<figure><img src="/.gitbook/assets/Screenshot_8_9.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

***

**Step 9 — Confirmation: Alert Added Successfully**

After clicking **Save**, the modal closes and the Account-Specific Alerts tab refreshes. A green success banner reads "Available balance alert successfully added." The new alert appears listed under Balance Alerts (1) with the account name, condition, and **Edit** / **Remove** actions.

<figure><img src="/.gitbook/assets/Screenshot_9_10.png" alt="Screenshot 9" width="620"><figcaption></figcaption></figure>

***

### 3.4 Step-by-Step Flow — Configure General (Optional) Alerts

Steps 1–6 are identical. At Step 6, you navigate to **General Alerts** tab.

**Step 7 — General Alerts Tab**

The tab is divided into two sections:

* **Optional Alerts**: Events you can configure (e.g., Stop check request, Check reorder). Each row has a dropdown with four options: Send all alerts / Send success alerts / Send failure alerts / Disable alerts.
* **Mandatory Alerts**: Events that always trigger regardless of preferences (failed login attempt, password change, account lock, contact info update, new device remembered, A2A transfer micro-deposit).

<figure><img src="/.gitbook/assets/Screenshot_7_11.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

***

**Step 8 — Set Optional Alert Preference**

you click the dropdown on an optional alert row and selects the desired delivery option. The system saves the selection and displays a green success banner: "Alert has been updated successfully."

<figure><img src="/.gitbook/assets/Screenshot_8_12.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

***

### 3.5 Step-by-Step Flow — Set Do-Not-Disturb Period

Steps 1–6 are identical. At Step 6, you click **Do-Not-Disturb**.

**Step 7 — Do-Not-Disturb Landing (No Period Set)**

The Do-Not-Disturb screen loads. A message states "You have not set a Do-Not-Disturb period." A **Set Do-Not-Disturb period** button is prominently displayed. A disclaimer in red text clarifies that mandatory alerts bypass DND and will always be delivered.

<figure><img src="/.gitbook/assets/Screenshot_7_13.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

***

**Step 8 — Set DND Form**

After clicking **Set Do-Not-Disturb period**, a form appears inline with three fields:

* **Timezone** (dropdown, e.g., PST)
* **Start time** (time picker, e.g., 10:00 PM)
* **End time** (time picker, e.g., 7:00 AM)

A preview message in red reads: "You will not receive alerts between [Start time] & [End time] the next day." you click **Set Do-Not-Disturb**.

<figure><img src="/.gitbook/assets/Screenshot_8_14.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

***

**Step 9 — DND Confirmation**

A green banner reads "Your Do-Not-Disturb period has been set." The page reflects the active DND window and shows a "Processing…" indicator as the system saves the preference.

<figure><img src="/.gitbook/assets/Screenshot_9_15.png" alt="Screenshot 9" width="620"><figcaption></figcaption></figure>

***

### 3.6 Step-by-Step Flow — Edit Do-Not-Disturb Period

After a DND period is active, the Do-Not-Disturb tab displays the current period with **Edit** and **Remove** inline actions.

**Existing Period Display**

The current DND window is shown (e.g., "10:00 PM PST to 07:00 AM PST") with Edit and Remove links. The red disclaimer about mandatory alerts remains visible.

<figure><img src="/.gitbook/assets/Screenshot_7_16.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

***

**Edit Form**

Clicking **Edit** expands the form with the current values pre-populated. you adjusts Timezone, Start time, or End time and clicks **Set Do-Not-Disturb** to save.

<figure><img src="/.gitbook/assets/Screenshot_8_17.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

***

**Edit Confirmation**

A green banner confirms "Your Do-Not-Disturb period has been set." The updated values are reflected immediately.

<figure><img src="/.gitbook/assets/Screenshot_9_18.png" alt="Screenshot 9" width="620"><figcaption></figcaption></figure>

***

### 3.7 Step-by-Step Flow — Remove Do-Not-Disturb Period

**Remove Action**

On the Do-Not-Disturb tab, you click **Remove** next to the active period.

<figure><img src="/.gitbook/assets/Screenshot_7_19.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

***

**Removal Confirmation**

The system processes the request and displays a green banner: "Do-Not-Disturb-Period has been removed successfully." The page returns to the "no period set" state, restoring full-hour alert delivery.

<figure><img src="/.gitbook/assets/Screenshot_8_20.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

***

### 3.8 Decision Points & Branching

* **Enable alerts toggle OFF**: All optional and mandatory alert delivery is suspended. Disabling does not delete configured alert rules—they resume when toggled back on.
* **DND period active + mandatory alert triggered**: System bypasses DND and delivers the mandatory alert immediately on all active channels.
* **No registered phone**: The SMS channel option will not be available; member must add a contact number via Personal Information before enabling SMS alerts.
* **OTP not received**: you can click "Retry in [N] seconds" or select "Select another method" to switch OTP delivery channel.

### 3.9 Error Handling

* If you save an alert with no account selected, the modal displays an inline validation error requiring account selection before saving.
* If the DND start time and end time are identical, the system will not allow submission.
* If contact information is missing or outdated, a notice on the Alert Settings page states "Have you not been receiving your alerts? Check your contact information on record" with a direct link to Personal Information settings.

***

## Section 4 — Feature Overview (UI Walkthrough)

### Login Screen

The entry point for all Summerville CU Online Banking sessions. You authenticate with User ID and password before reaching any alert configuration screens.

<figure><img src="/.gitbook/assets/Screenshot_1_21.png" alt="Screenshot 1" width="620"><figcaption></figcaption></figure>

| Field / Element        | Type               | Description                        | Notes                                            |
| ---------------------- | ------------------ | ---------------------------------- | ------------------------------------------------ |
| User ID                | Text input         | your enrolled username         | Pre-filled if "Save User ID" was used previously |
| Password               | Password input     | your account password          | Masked by default; eye icon to reveal            |
| I need help logging in | Link               | Navigates to account recovery flow | For forgotten User ID or password                |
| Log in                 | Button             | Submits credentials                | Disabled until both fields are populated         |
| Enroll                 | Button (top right) | Opens new member enrollment        | For prospective You only                     |

***

### OTP Verification — Select Method

Displayed after successful credential entry. Enforces step-up authentication before any account access.

<figure><img src="/.gitbook/assets/Screenshot_2_22.png" alt="Screenshot 2" width="620"><figcaption></figcaption></figure>

| Field / Element   | Type              | Description                 | Notes                                |
| ----------------- | ----------------- | --------------------------- | ------------------------------------ |
| Send me a message | Selectable option | Delivers OTP via SMS        | Proceeds to contact number selection |
| Call me           | Selectable option | Delivers OTP via phone call | Direct delivery to registered phone  |
| Send me an email  | Selectable option | Delivers OTP via email      | Sent to registered email address     |

***

### OTP Verification — Select Contact

Shown after selecting "Send me a message." Displays masked registered phone numbers for you to choose from.

<figure><img src="/.gitbook/assets/Screenshot_3_23.png" alt="Screenshot 3" width="620"><figcaption></figcaption></figure>

| Field / Element                   | Type            | Description                          | Notes                                               |
| --------------------------------- | --------------- | ------------------------------------ | --------------------------------------------------- |
| Select another method             | Link            | Returns to method selection screen   | Allows switching delivery method                    |
| Contact number rows               | Selectable list | Masked phone numbers on record       | Member taps the desired number                      |
| "Don't see your updated contact?" | Informational   | Link to retrieve latest contact info | Supports You who recently updated their profile |

***

### OTP Verification — Enter Code

<figure><img src="/.gitbook/assets/Screenshot_4_24.png" alt="Screenshot 4" width="620"><figcaption></figcaption></figure>

| Field / Element                        | Type             | Description                          | Notes                                       |
| -------------------------------------- | ---------------- | ------------------------------------ | ------------------------------------------- |
| Enter code                             | 6-cell OTP input | Member enters the one-time passcode  | Each digit in a separate cell               |
| Didn't receive your code? Retry in N s | Countdown + link | Allows resend after cooldown expires | Timer resets on each send                   |
| Remember Device/Browser                | Checkbox         | Marks device as trusted              | Skips OTP on future logins from same device |
| Submit                                 | Button           | Submits the OTP                      | Disabled until all 6 digits entered         |

***

### Dashboard

Post-login landing screen. Starting point for navigation to all alert management features.

<figure><img src="/.gitbook/assets/Screenshot_5_25.png" alt="Screenshot 5" width="620"><figcaption></figcaption></figure>

| Field / Element | Type          | Description                                        | Notes                          |
| --------------- | ------------- | -------------------------------------------------- | ------------------------------ |
| Dashboard       | Nav tab       | Active view; shows account balances and promotions |                                |
| Accounts        | Nav tab       | Account list and detail views                      |                                |
| Move Money      | Nav tab       | Transfer and payment hub                           |                                |
| More            | Nav tab       | Expands to Alerts, Settings, Security, Utilities   | Entry point for Alert Settings |
| Quick Transfer  | Panel (right) | Fast fund transfer without navigating away         |                                |

***

### More Options Panel

Expanded view of the More navigation menu. The Alerts section surfaces four alert-related destinations.

<figure><img src="/.gitbook/assets/Screenshot_6_26.png" alt="Screenshot 6" width="620"><figcaption></figcaption></figure>

| Field / Element | Type      | Description                              | Notes                                         |
| --------------- | --------- | ---------------------------------------- | --------------------------------------------- |
| Account Alerts  | Menu item | Navigates to Account-Specific Alerts tab | For balance, deposit, withdrawal thresholds   |
| General Alerts  | Menu item | Navigates to General Alerts tab          | Optional and mandatory event alerts           |
| Do-Not-Disturb  | Menu item | Navigates to DND tab directly            | For setting/editing quiet hours               |
| Alert Settings  | Menu item | Navigates to Alert Settings tab          | For channel toggles and master enable/disable |

***

### Alert Settings Tab

Controls master alert delivery and individual channel preferences.

<figure><img src="/.gitbook/assets/Screenshot_7_27.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

| Field / Element             | Type         | Description                                          | Notes                                         |
| --------------------------- | ------------ | ---------------------------------------------------- | --------------------------------------------- |
| General alerts tab          | Tab          | Shows optional and mandatory general alerts          |                                               |
| Account-specific alerts tab | Tab          | Shows account threshold alerts                       |                                               |
| Alert Settings tab          | Tab (active) | Current view — channel configuration                 |                                               |
| Do-Not-Disturb tab          | Tab          | DND period management                                |                                               |
| Enable alerts               | Toggle       | Master on/off for all alert delivery                 | Disabling suspends but does not delete alerts |
| Push notifications          | Toggle       | Enables push to trusted mobile devices               | Requires app installed and device trusted     |
| SMS alerts                  | Toggle       | Enables text delivery                                | Displays registered phone number              |
| Email alerts                | Toggle       | Enables email delivery                               | Displays registered email address             |
| Contact information link    | Inline link  | Opens Personal Information to update contact details | Shown in advisory message at top              |

***

### Account-Specific Alerts Tab

Allows You to configure threshold-based alerts tied to specific accounts.

<figure><img src="/.gitbook/assets/Screenshot_7_28.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

| Field / Element             | Type           | Description                             | Notes                  |
| --------------------------- | -------------- | --------------------------------------- | ---------------------- |
| Balance alerts (N)          | Section header | Count of active balance alerts          |                        |
| Periodic balance alerts (N) | Section header | Count of active periodic alerts         |                        |
| Deposit alerts (N)          | Section header | Count of active deposit alerts          |                        |
| Withdrawal alerts (N)       | Section header | Count of active withdrawal alerts       |                        |
| + Add a new alert           | Link           | Opens add-alert modal for that category | One click per category |

***

### Add New Alert Modal

Modal dialog for creating a threshold alert on a specific account.

<figure><img src="/.gitbook/assets/Screenshot_8_29.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

| Field / Element    | Type           | Description                          | Notes                                    |
| ------------------ | -------------- | ------------------------------------ | ---------------------------------------- |
| Select account     | Dropdown       | Lists all eligible member accounts   | Required field                           |
| Condition operator | Dropdown       | "Less than" / "Greater than" / etc.  | Context-dependent on alert type          |
| Threshold amount   | Currency input | Dollar value that triggers the alert | Required; numeric only                   |
| Cancel             | Button         | Dismisses modal without saving       |                                          |
| Save               | Button         | Creates the alert and closes modal   | Triggers success banner on parent screen |

***

### Account-Specific Alerts — Post-Save Confirmation

<figure><img src="/.gitbook/assets/Screenshot_9_30.png" alt="Screenshot 9" width="620"><figcaption></figcaption></figure>

| Field / Element | Type                | Description                                   | Notes                                     |
| --------------- | ------------------- | --------------------------------------------- | ----------------------------------------- |
| Success banner  | Green inline banner | "Available balance alert successfully added." | Dismisses automatically                   |
| Alert row       | Listed item         | Shows account name, condition, and threshold  | Appears under the relevant alert category |
| Edit            | Inline link         | Opens modal to modify the alert               |                                           |
| Remove          | Inline link         | Deletes the alert                             | Immediate; no confirmation prompt         |

***

### General Alerts Tab — Optional & Mandatory

<figure><img src="/.gitbook/assets/Screenshot_7_31.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

| Field / Element          | Type           | Description                           | Notes                                                     |
| ------------------------ | -------------- | ------------------------------------- | --------------------------------------------------------- |
| Optional Alerts section  | Section        | Per-event alert preference dropdowns  | Member-configurable                                       |
| Stop check request       | Row + dropdown | Alert when a stop check is placed     | Options: Send all / Send success / Send failure / Disable |
| Check reorder attempted  | Row + dropdown | Alert when check reorder is triggered | Same four options                                         |
| Alert Preferences link   | Inline link    | Jumps to Alert Settings tab           | Contextual shortcut                                       |
| Mandatory Alerts section | Section        | Always-on alerts; not configurable    | Listed for member awareness only                          |

***

### General Alerts — Post-Update Confirmation

<figure><img src="/.gitbook/assets/Screenshot_8_32.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

| Field / Element   | Type                | Description                                        | Notes                                     |
| ----------------- | ------------------- | -------------------------------------------------- | ----------------------------------------- |
| Success banner    | Green inline banner | "Alert has been updated successfully."             | Confirms the dropdown selection was saved |
| Updated alert row | Row                 | Reflects new setting (e.g., "Send success alerts") | Live update without page reload           |

***

### Do-Not-Disturb — No Period Set

<figure><img src="/.gitbook/assets/Screenshot_7_33.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

| Field / Element            | Type               | Description                                 | Notes                                |
| -------------------------- | ------------------ | ------------------------------------------- | ------------------------------------ |
| Status message             | Informational text | "You have not set a Do-Not-Disturb period." | Shown when no DND is configured      |
| Set Do-Not-Disturb period  | Button             | Expands inline DND configuration form       | Primary call to action               |
| Mandatory alert disclaimer | Red text           | States mandatory alerts bypass DND          | Permanent reminder; non-configurable |

***

### Do-Not-Disturb — Set Period Form

<figure><img src="/.gitbook/assets/Screenshot_8_34.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

| Field / Element    | Type            | Description                                                          | Notes                                      |
| ------------------ | --------------- | -------------------------------------------------------------------- | ------------------------------------------ |
| Timezone           | Dropdown        | your local timezone (e.g., PST)                                  | Required; affects alert suppression window |
| Start time         | Time picker     | Beginning of quiet period (e.g., 10:00 PM)                           | Required                                   |
| End time           | Time picker     | End of quiet period (e.g., 7:00 AM)                                  | Required; can cross midnight               |
| Preview message    | Red inline text | "You will not receive alerts between [start] & [end] the next day" | Dynamically updates as times change        |
| Cancel             | Button          | Dismisses form without saving                                        |                                            |
| Set Do-Not-Disturb | Button          | Saves DND period                                                     | Triggers success banner                    |

***

### Do-Not-Disturb — Period Active (Edit / Remove)

<figure><img src="/.gitbook/assets/Screenshot_7_35.png" alt="Screenshot 7" width="620"><figcaption></figcaption></figure>

| Field / Element       | Type        | Description                                                 | Notes                        |
| --------------------- | ----------- | ----------------------------------------------------------- | ---------------------------- |
| Active period display | Text        | Shows current window (e.g., "10:00 PM PST to 07:00 AM PST") |                              |
| Edit                  | Inline link | Expands edit form with current values pre-filled            |                              |
| Remove                | Inline link | Deletes the DND period                                      | Confirms with success banner |

***

### Do-Not-Disturb — Period Removed Confirmation

<figure><img src="/.gitbook/assets/Screenshot_8_36.png" alt="Screenshot 8" width="620"><figcaption></figcaption></figure>

| Field / Element | Type                | Description                                            | Notes                            |
| --------------- | ------------------- | ------------------------------------------------------ | -------------------------------- |
| Success banner  | Green inline banner | "Do-Not-Disturb-Period has been removed successfully." | Confirms removal                 |
| Period display  | Text                | Still shows old period during "Processing…" indicator  | Clears once processing completes |

***

## Section 5 — Quick Reference

| Task                                         | Navigation Path                                                                        | Who Can Do It            | Notes                                                     |
| -------------------------------------------- | -------------------------------------------------------------------------------------- | ------------------------ | --------------------------------------------------------- |
| Enable or disable all alerts                 | More > Alert Settings > Alert Settings tab > Enable alerts toggle                      | Any authenticated member | Disabling suspends, does not delete, alert rules          |
| Change delivery channel (Push / SMS / Email) | More > Alert Settings > Alert Settings tab                                             | Any authenticated member | Registered contact required for SMS and Email             |
| Add a balance alert                          | More > Alert Settings > Account-Specific Alerts tab > Balance Alerts > Add a new alert | Any authenticated member | Select account and set threshold amount                   |
| Add a deposit or withdrawal alert            | More > Alert Settings > Account-Specific Alerts tab > Deposit/Withdrawal alerts        | Any authenticated member | Same modal flow as balance alert                          |
| Edit or remove an account alert              | More > Alert Settings > Account-Specific Alerts tab > [Alert row] > Edit / Remove     | Any authenticated member | Edit opens same modal; Remove is immediate                |
| Set optional general alert preference        | More > Alert Settings > General Alerts tab > [Event row] dropdown                     | Any authenticated member | Options: Send all / Send success / Send failure / Disable |
| Set Do-Not-Disturb period                    | More > Alert Settings > Do-Not-Disturb tab > Set Do-Not-Disturb period                 | Any authenticated member | Mandatory alerts always bypass DND                        |
| Edit Do-Not-Disturb period                   | More > Alert Settings > Do-Not-Disturb tab > Edit                                      | Any authenticated member | Pre-fills current values                                  |
| Remove Do-Not-Disturb period                 | More > Alert Settings > Do-Not-Disturb tab > Remove                                    | Any authenticated member | Restores full-hour alert delivery immediately             |
| Update contact info for alerts               | More > Alert Settings > Alert Settings tab > contact information link                  | Any authenticated member | Redirects to Personal Information                         |
