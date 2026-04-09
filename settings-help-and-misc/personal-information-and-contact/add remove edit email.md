# Manage Email — Product Feature Guide

**Summerville Credit Union | nFinia Digital Banking Platform** _Prepared by Jeeva Krishnamurthy, Senior Product Manager — Commercial & SMB Digital Banking, Tyfone_

***

## 1. Product Summary

The **Manage Email** feature within nFinia's Personal Information module gives Summerville Credit Union You full self-service control over the email addresses associated with their online banking profile. You can add new email IDs, update existing ones, and remove addresses they no longer use — all from within the Contact Information section of the platform, without requiring branch intervention or a call to member services.

This feature serves retail You (Personal Memberships) as well as business users operating under a personal profile at Summerville CU. Because email addresses function as both a communication channel and an OTP delivery method, maintaining accurate email data is critical to account security and member-facing notifications. For the credit union, this self-service capability reduces inbound contact center volume and accelerates the accuracy of member contact records without manual staff effort.

From a compliance and security standpoint, every change to contact information — add, edit, or remove — is gated behind an OTP (One-Time Passcode) step. This ensures that unauthorized actors cannot silently redirect communications. The feature lives at **Banking > More > Contact Information** within the nFinia Summerville deployment.

### At a Glance

| Attribute            | Detail                                                      |
| -------------------- | ----------------------------------------------------------- |
| Feature Name         | Manage Email                                                |
| Module               | Banking > More > Contact Information                        |
| User Roles           | Personal Member, Business Member (personal profile)         |
| Access Level         | Authenticated session, OTP-verified                         |
| Key Actions          | Add Email, Edit Email, Remove Email                         |
| Regulatory Relevance | OTP-gated contact changes; audit trail on all modifications |

***

## 2. Use Cases

| Use Case                                | Who Uses It              | What They Do                                                                          | Business Value                                                                                   |
| --------------------------------------- | ------------------------ | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| Add a new personal or business email    | Personal/Business Member | Navigates to Contact Information, enters a new email address, saves                   | you can receive notifications to an additional address; reduces missed communications         |
| Update an outdated email address        | Personal/Business Member | Selects Edit next to an existing email, types the new address, saves changes          | Keeps contact records current without branch visit; reduces returned mail and missed OTPs        |
| Remove a deactivated or unwanted email  | Personal/Business Member | Selects Remove next to an email, confirms deletion in the confirmation modal          | Cleans up stale addresses; reduces security surface area for phishing misdirection               |
| Verify identity before any email change | Personal/Business Member | Completes OTP verification (SMS, call, or email) before accessing Contact Information | Prevents unauthorized contact changes; satisfies security best practice for sensitive data edits |
| Recover from an incorrect email entry   | Personal/Business Member | Cancels an in-progress add or edit, or removes an incorrectly added address           | Self-service error recovery without staff involvement                                            |

All three sub-workflows — Add, Edit, and Remove — share the same OTP authentication gate. This design ensures that no email modification can occur unless you have proven possession of a registered phone number or existing email address, aligning with the credit union's obligation to maintain data integrity and prevent social engineering attacks on member contact records.

***

## 3. End-to-End Workflow

### 3.1 Prerequisites

* Member must have an active Summerville CU online banking enrollment.
* you must have at least one OTP-capable contact method already on file (phone number or email).
* To **remove** an email, at least one other email must remain on the account (the system does not permit removal of the last/primary email).
* Session must be active (not timed out).

***

### 3.2 Step-by-Step Flow — Add Email

**Step 1 — Login**

you navigate to the Summerville CU online banking portal and enters their User ID and password on the Login screen, then clicks **Log in**.

<figure><img src="/.gitbook/assets/image_1.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 1 — Login screen: Member enters credentials_

***

**Step 2 — OTP Method Selection**

The system presents the Verification screen, prompting you to select how they would like to receive their One-Time Passcode: **Send me a message** (SMS), **Call me**, or **Send me an email**.

<figure><img src="/.gitbook/assets/image_2.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 2 — OTP method selection: Choose SMS, call, or email_

***

**Step 3 — Select OTP Delivery Number**

If you select **Send me a message**, they are shown a list of registered phone numbers (masked for security, e.g. (+1) 2\*\*-\*\*\*-\*\*01). you select the number where the OTP should be sent.

<figure><img src="/.gitbook/assets/image_3.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 3 — Select the phone number to receive the OTP_

***

**Step 4 — Enter OTP Code**

The system confirms the OTP has been dispatched ("A One-Time Passcode (OTP) has been sent to (+1) 2\*\*-\*\*\*-\*\*01"). you enter the 5-digit code in the **Enter code** fields. A retry countdown timer is displayed. you may optionally select **Remember Device/Browser** before clicking **Submit**.

<figure><img src="/.gitbook/assets/image_4.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 4 — Enter the OTP code and optionally remember the device_

***

**Step 5 — Dashboard**

After successful OTP verification, you land on the main Dashboard ("Good Morning, DONALD BLAKE"). From here, they navigate to **More** in the top navigation bar.

<figure><img src="/.gitbook/assets/image_5.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 5 — Dashboard: Navigate to More_

***

**Step 6 — Select View Personal Information**

you open the account profile switcher and selects **View Personal Information**. This brings up the Contact Information section.

<figure><img src="/.gitbook/assets/image_6.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 6 — Profile selector: Choose View Personal Information_

***

**Step 7 — Contact Information: Add Email**

The system displays the Contact Information page. Under the **Personal email** section, the current email addresses are shown. you click **Add a new email address**, which reveals an inline text input field. you types the new email address and clicks **Add a new email address** (submit button) or **Cancel** to abandon.

<figure><img src="/.gitbook/assets/image_7.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 7 — Contact Information: Enter new email address in the inline input field_

***

**Step 8 — Success Confirmation**

Upon saving, the Personal Information page reloads and displays a green success banner: **"New email ID has been added successfully."** The new email now appears in the Personal email list.

<figure><img src="/.gitbook/assets/image_8.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 8 — Success: New email ID has been added successfully_

***

### 3.3 Step-by-Step Flow — Edit Email

Steps 1–6 are identical to the Add Email flow (Login → OTP method → Phone selection → OTP entry → Dashboard → Profile selection).

**Step 7 — Contact Information: Edit Email**

On the Contact Information screen, you locates the email entry they want to update under **Personal email** and clicks **Edit**. The email field becomes an editable text input pre-populated with the current value. you modifies the address and clicks **Save changes**, or clicks **Cancel** to discard.

<figure><img src="/.gitbook/assets/image_9.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 7 (Edit) — Contact Information: Edit the email address inline_

***

**Step 8 — Success Confirmation**

After saving, a green success banner appears: **"Email ID has been updated successfully."** The updated address is reflected immediately in the contact list.

<figure><img src="/.gitbook/assets/image_10.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 8 (Edit) — Success: Email ID has been updated successfully_

***

### 3.4 Step-by-Step Flow — Remove Email

Steps 1–6 are identical to the Add Email flow.

**Step 7 — Contact Information: Initiate Remove**

On the Contact Information screen, you locates the email entry they wish to delete and clicks **Remove**. The page shows the full contact info list with multiple email addresses visible, each with Edit and Remove links.

<figure><img src="/.gitbook/assets/image_11.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 7 (Remove) — Contact Information: Multiple emails shown with Remove option_

***

**Step 8 — Removal Confirmation Modal**

A confirmation modal dialog appears overlaying the page: **"Do you want to remove this email ID?"** with two options — **Cancel** and **Confirm**. you must explicitly click **Confirm** to proceed; clicking **Cancel** or closing the modal aborts the action.

<figure><img src="/.gitbook/assets/image_12.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 8 (Remove) — Confirmation modal: Do you want to remove this email ID?_

***

**Step 9 — Success Confirmation**

After confirming, the page reloads and displays a green success banner: **"Email ID has been removed successfully."** The removed address no longer appears in the contact list.

<figure><img src="/.gitbook/assets/image_13.png" alt="" width="620"><figcaption></figcaption></figure>

_Step 9 (Remove) — Success: Email ID has been removed successfully_

***

### 3.5 Decision Points & Branching

| Condition                                 | Behavior                                                                                 |
| ----------------------------------------- | ---------------------------------------------------------------------------------------- |
| Member selects "Call me" for OTP          | System initiates a voice call to the selected registered number with the passcode        |
| Member selects "Send me an email" for OTP | OTP is sent to the primary email already on file                                         |
| Member clicks "Select another method"     | Returns to OTP method selection screen                                                   |
| Member clicks "Cancel" during Add or Edit | Input field collapses; no change is saved                                                |
| Member clicks "Cancel" on removal modal   | Modal closes; email remains unchanged                                                    |
| "Remember Device/Browser" is checked      | Device is flagged as trusted; OTP gate may be bypassed on future logins from same device |

### 3.6 Error Handling

| Scenario                                    | System Response                                                                                   |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| OTP not received within countdown window    | "Didn't receive your code? Retry in 52s" message with retry countdown                             |
| Invalid OTP entered                         | Submit button remains inactive until valid code length entered; incorrect code shows inline error |
| Attempting to save an invalid email format  | Form validation prevents submission; you are prompted to correct the entry                      |
| Attempting to remove the only email on file | Remove action is not available; only emails beyond the minimum required can be deleted            |

***

## 4. Feature Overview — UI Walkthrough

### Login Screen

The entry point to the platform. you provide their **User ID** and **Password** to initiate authentication. A "I need help logging in" link provides self-service recovery options for forgotten credentials.

| Field / Element        | Type           | Description                                 | Notes                                                   |
| ---------------------- | -------------- | ------------------------------------------- | ------------------------------------------------------- |
| User ID                | Text Input     | your registered online banking username | Pre-populated if "Save User ID" was previously selected |
| Password               | Password Input | your account password                   | Masked by default; show/hide toggle available           |
| Log in                 | Button         | Submits credentials and triggers OTP flow   | Disabled until both fields are populated                |
| I need help logging in | Link           | Navigates to credential recovery options    | Available without authentication                        |
| Enroll                 | Button         | New member registration entry point         | Top-right corner                                        |

<figure><img src="/.gitbook/assets/image_14.png" alt="" width="620"><figcaption></figcaption></figure>

_Login Screen — Summerville CU nFinia portal_

***

### OTP Method Selection Screen

Presented immediately after credential validation. you select their preferred OTP delivery channel. This screen is shared across all three email management workflows (Add, Edit, Remove).

| Field / Element   | Type          | Description                                | Notes                                      |
| ----------------- | ------------- | ------------------------------------------ | ------------------------------------------ |
| Send me a message | Option Button | Delivers OTP via SMS to a registered phone | Selecting opens phone number sub-selection |
| Call me           | Option Button | Delivers OTP via automated voice call      | Selecting opens phone number sub-selection |
| Send me an email  | Option Button | Delivers OTP to the primary email on file  | Used when phone access is unavailable      |

<figure><img src="/.gitbook/assets/image_15.png" alt="" width="620"><figcaption></figcaption></figure>

_OTP Method Selection Screen_

***

### OTP Phone Number Selection Screen

Shown when SMS or Call is chosen. Lists all registered phone numbers (masked) so you can route the OTP to the correct device.

| Field / Element                                        | Type            | Description                                               | Notes                                            |
| ------------------------------------------------------ | --------------- | --------------------------------------------------------- | ------------------------------------------------ |
| Select another method                                  | Link            | Returns to OTP method selection                           | Visible at top of screen                         |
| Phone number options                                   | Selectable Rows | Masked registered numbers (e.g. (+1) 2\*\*-\*\*\*-\*\*01) | Each row navigates to OTP entry on selection     |
| Don't see your updated contact information? Click here | Link            | Retrieves latest contact data from core                   | Useful if contact was recently updated at branch |

<figure><img src="/.gitbook/assets/image_16.png" alt="" width="620"><figcaption></figcaption></figure>

_Phone Number Selection Screen for OTP delivery_

***

### OTP Entry Screen

you enter the 5-digit code dispatched to their chosen contact method. A retry timer enforces a cooldown period before a new code can be requested.

| Field / Element                       | Type         | Description                                      | Notes                                           |
| ------------------------------------- | ------------ | ------------------------------------------------ | ----------------------------------------------- |
| Enter code                            | 5-cell Input | One digit per cell; auto-advances on entry       | Code expires after the countdown period         |
| Didn't receive your code? Retry in Xs | Timer/Link   | Countdown before retry is available              | Prevents OTP brute-force attempts               |
| Remember Device/Browser               | Checkbox     | Marks this device as trusted for future sessions | Optional; reduces OTP friction on repeat logins |
| Submit                                | Button       | Validates entered OTP and proceeds               | Inactive until all 5 digits are entered         |

<figure><img src="/.gitbook/assets/image_17.png" alt="" width="620"><figcaption></figcaption></figure>

_OTP Entry Screen — Enter the 5-digit code_

***

### Dashboard

The authenticated home screen for you. Accessed after successful OTP validation. You navigate to **More** from the top navigation to reach Personal Information and Contact settings.

| Field / Element                  | Type             | Description                                     | Notes                                        |
| -------------------------------- | ---------------- | ----------------------------------------------- | -------------------------------------------- |
| More (nav)                       | Navigation Link  | Opens secondary navigation menu                 | Houses Personal Information, Settings, etc.  |
| Quick Transfer widget            | Panel            | Right-side transfer initiation shortcut         | Not relevant to email management workflow    |
| Personal Memberships (top right) | Profile Switcher | Switches between personal and business profiles | Business You must select correct profile |

<figure><img src="/.gitbook/assets/image_18.png" alt="" width="620"><figcaption></figcaption></figure>

_Dashboard — Navigate via More to reach Contact Information_

***

### Profile Selector

Appears when you click their profile/membership indicator. Lists all memberships (personal and business) the user has access to, enabling context switching between accounts.

| Field / Element                                                 | Type             | Description                        | Notes                                        |
| --------------------------------------------------------------- | ---------------- | ---------------------------------- | -------------------------------------------- |
| Personal Memberships                                            | Selectable Card  | Routes to personal banking context | Highlighted when active                      |
| Business entries (e.g. Perfect Pitch Music, Green Thumb Lands…) | Selectable Cards | Routes to business banking context | Shows role (e.g. Basic Role, Business Admin) |

<figure><img src="/.gitbook/assets/image_19.png" alt="" width="620"><figcaption></figcaption></figure>

_Profile Selector — Choose Personal Memberships or a Business profile_

***

### Contact Information Screen — Add Email

Displays all contact data on file: phone numbers and email addresses for Home, Business, Business cell, Personal, and Business categories. The **Add a new email address** option expands to reveal an inline text input.

| Field / Element                     | Type               | Description                                   | Notes                                        |
| ----------------------------------- | ------------------ | --------------------------------------------- | -------------------------------------------- |
| Personal email (existing entries)   | Read-only Labels   | Shows masked current email addresses          | Each entry has Edit \| Remove action links   |
| Add a new email address (link)      | Expandable Trigger | Reveals inline text input for new email entry | Clicking collapses the input if already open |
| Email input field                   | Text Input         | Accepts the new email address value           | Standard email format validation applies     |
| Add a new email address (button)    | Submit Button      | Saves the new email to you profile     | Disabled until valid email is entered        |
| Cancel                              | Button             | Collapses the input without saving            | No change is persisted                       |
| Business email / Add a new email ID | Section + Link     | Adds an email to the Business email category  | Separate from Personal email                 |

<figure><img src="/.gitbook/assets/image_20.png" alt="" width="620"><figcaption></figcaption></figure>

_Contact Information — Add a new email address inline_

***

### Contact Information Screen — Edit Email

The existing email entry transforms into an editable text field pre-filled with the current value. you make their changes directly inline.

| Field / Element          | Type                | Description                                        | Notes                                    |
| ------------------------ | ------------------- | -------------------------------------------------- | ---------------------------------------- |
| Email input (pre-filled) | Editable Text Input | Current email value, editable                      | Validation enforces correct email format |
| Save changes             | Button              | Persists the updated email to you record    | Triggers success confirmation on save    |
| Cancel                   | Button              | Discards edits; field reverts to read-only display | No changes saved                         |

<figure><img src="/.gitbook/assets/image_21.png" alt="" width="620"><figcaption></figcaption></figure>

_Contact Information — Edit email address inline with Save changes / Cancel_

***

### Contact Information Screen — Remove Email (with Confirmation Modal)

When Remove is clicked, a modal overlay appears requiring explicit confirmation before deletion occurs. This two-step pattern prevents accidental removal.

| Field / Element                               | Type           | Description                         | Notes                                              |
| --------------------------------------------- | -------------- | ----------------------------------- | -------------------------------------------------- |
| Remove (action link)                          | Inline Link    | Initiates the removal process       | Available on each removable email entry            |
| Modal: "Do you want to remove this email ID?" | Overlay Dialog | Confirmation prompt before deletion | Blocks interaction with background until dismissed |
| Cancel (modal)                                | Button         | Dismisses modal; no change made     | Safe exit path                                     |
| Confirm (modal)                               | Button         | Executes the email removal          | Action is immediate upon click                     |

<figure><img src="/.gitbook/assets/image_22.png" alt="" width="620"><figcaption></figcaption></figure>

_Removal Confirmation Modal — Confirm or Cancel_

***

### Success Confirmation (All Flows)

After Add, Edit, or Remove, the Personal Information page reloads and displays a green success notification banner at the top of the Contact Information tab. Related links (Change Password, Download E-Statements, View Scheduled Transfers) are visible in the right panel for convenient post-action navigation.

| Outcome       | Banner Message                              |
| ------------- | ------------------------------------------- |
| Email added   | "New email ID has been added successfully." |
| Email updated | "Email ID has been updated successfully."   |
| Email removed | "Email ID has been removed successfully."   |

<figure><img src="/.gitbook/assets/image_23.png" alt="" width="620"><figcaption></figcaption></figure>

_Success — New email ID has been added successfully_

<figure><img src="/.gitbook/assets/image_24.png" alt="" width="620"><figcaption></figcaption></figure>

_Success — Email ID has been updated successfully_

<figure><img src="/.gitbook/assets/image_25.png" alt="" width="620"><figcaption></figcaption></figure>

_Success — Email ID has been removed successfully_

***

## 5. Quick Reference

| Task                           | Navigation Path                                                                 | Who Can Do It                              | Notes                                                                  |
| ------------------------------ | ------------------------------------------------------------------------------- | ------------------------------------------ | ---------------------------------------------------------------------- |
| Add a new email address        | Banking > More > Contact Information > Personal email > Add a new email address | Authenticated member                       | OTP verification required on each session; inline input                |
| Edit an existing email address | Banking > More > Contact Information > Personal email > Edit                    | Authenticated member                       | OTP required; changes take effect immediately                          |
| Remove an email address        | Banking > More > Contact Information > Personal email > Remove                  | Authenticated member                       | OTP required; two-step confirmation modal prevents accidental deletion |
| Switch OTP delivery method     | Verification screen > Select another method                                     | Authenticated member during OTP step       | Available for SMS, voice call, or existing email                       |
| Trust a device to skip OTP     | OTP Entry screen > Remember Device/Browser checkbox                             | Authenticated member                       | Reduces friction on subsequent logins from same device                 |
| Add a business email address   | Banking > More > Contact Information > Business email > Add a new email ID      | Authenticated member with business profile | Separate from Personal email section                                   |

***

_This guide was produced using the nFinia platform as deployed at Summerville Credit Union. Navigation paths, field names, and screen layouts reflect the Summerville CU instance. Feature behavior may vary based on credit union configuration settings._
