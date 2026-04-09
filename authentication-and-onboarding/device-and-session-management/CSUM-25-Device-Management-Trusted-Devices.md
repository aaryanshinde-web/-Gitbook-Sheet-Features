---
description: nFinia Digital Banking · CSUM-28 · Device Management & Trusted Devices
---

# Device Management & Trusted Devices

> **Module:** nFinia Digital Banking → More → Personal Information → Devices  |  **Reference:** CSUM-28


## 01 · Product Summary


Device Management allows Diamond Credit Union The member to view and manage all devices registered as trusted for their digital banking account. A device becomes trusted when a member completes a full login (username + password + OTP) and selects 'Remember this device' during the OTP step, allowing future logins from that device to bypass the OTP verification.

The Devices tab shows all trusted devices with their device name, OS, last login date, and trust status. The member can remove any device from the trusted list — which immediately requires full OTP authentication on the next login from that device. This is essential for decommissioning old phones and for security response after a suspected compromise.

Trusted Device Approval Required is an enhanced security mode available for some account types, where any new device login requires explicit approval from an already-trusted device before the session is established.

**At a Glance**

| Attribute | Detail |
| --- | --- |
| Module | More > Personal Information > Devices |
| Trusted Device | Device where OTP step is bypassed after initial trust |
| Trust Action | Set during login by checking 'Remember this device' |
| Revoke Trust | Removing a device from the list re-requires OTP on next login |
| Enhanced Mode | Trusted Device Approval Required — new logins require existing device approval |
| Related Reports | CSUM-22 (Personal Information), CSUM-01 (Login & Auth), CSUM-25 (Password & MFA) |


## 02 · Key Use Cases



| Use Case                     | Who Uses It                                                          | What They Do                                                | Business Value                                                                                                                                                                                                    |
| ---------------------------- | -------------------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Review Trusted Devices       | The member auditing account security                                    | Open Devices tab to see all registered trusted devices      | Confirms which devices can log in without OTP, enabling security audit                                                                                                                                            |
| Remove Old Phone             | The member replacing their device                                       | Click remove on the old device entry                        | Immediately revokes OTP bypass for the decommissioned device                                                                                                                                                      |
| Revoke After Security Event  | The member who suspect account compromise                               | Remove ALL trusted devices to force OTP on every login      | Nuclear option that resets all trusted sessions, securing the account                                                                                                                                             |
| Approve New Device Login     | The member with Trusted Device Approval mode                            | Approve a new login attempt from an existing trusted device | Enhanced security requiring confirmation from a known good device                                                                                                                                                 |
| 
## 03 · Step-by-Step Guide
 | *Navigation: Dashboard > More > Personal Information > Devices tab.* | **Step 1 — Start from Dashboard**                           | you begins at the Dashboard after logging in. The Dashboard displays all account balances, upcoming payments, quick-action tiles, and the top navigation bar with links to Accounts, Move Money, and More. |


<figure><img src="/.gitbook/assets/img_eb0a7d21423c.png" alt="" width="480"><figcaption></figcaption></figure>

*Step 1: Start from Dashboard*

**Step 2 — Open the More Menu**

you click ‘More' in the top navigation bar. The More options panel expands to show additional features: Check Deposit, User ID and Password, eDocuments, Account Alerts, General Alerts, Password, Forms, One-Time Passcode, Skip A Pay, Do-Not-Disturb, Manage Devices, My Insights, Alert Settings, Recent Activities, and Card Services.

<figure><img src="/.gitbook/assets/img_ba578ecd81d3.png" alt="" width="620"><figcaption></figcaption></figure>

*Step 2: More Menu*

**Step 3 — Navigate from Dashboard to Devices**

The Account Overview page shows a detailed list of registered devices with columns for device type, date registered, and action buttons for managing each device.

<figure><img src="/.gitbook/assets/Device_Management_img3.png" alt="" width="340"><figcaption></figcaption></figure>

*Step 3: Navigate from Dashboard to Devices*

**Step 4 — Review Device Details**

The Personal Information page displays a comprehensive list of registered devices, each with a 'Forget Device' button for removing the device from your trusted device list.

<figure><img src="/.gitbook/assets/Device_Management_img3.png" alt="" width="340"><figcaption></figcaption></figure>

*Step 4: Review Device Details*

**Step 5 — Remove a Trusted Device**

A confirmation modal asks 'Are you sure you want to forget this device?' with Cancel and Proceed buttons for you to confirm or cancel the device removal.

<figure><img src="/.gitbook/assets/img_02399f4ee5dd.png" alt="" width="620"><figcaption></figcaption></figure>

*Step 5: Remove a Trusted Device*

