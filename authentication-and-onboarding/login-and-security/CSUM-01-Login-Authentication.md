---
description: >-
  Log in securely using multi-factor authentication, recover your account, and
  manage session security.
---

# Login & Authentication

> **Module:** Banking › Login

## Summary

The Login & Authentication module is the security gateway to the Summerville Credit Union digital banking platform. Every session begins here — it is the single point of identity verification before any account data, transaction capability, or self-service function is accessible. The authentication flow employs a multi-layer design: you supply a registered username and password, then complete a one-time passcode (OTP) challenge delivered to a pre-registered email or mobile number.

Beyond standard username/password entry, the module supports forgotten credentials recovery (Forgot User ID, Forgot Password), account unlock for locked-out members, biometric login (Touch ID / Face ID) on supported devices, and a 'Save User ID' convenience feature. A 'Sneak Peek' option on supported configurations allows you to preview your account balances before completing full authentication.

Multi-factor authentication (MFA) settings — including managing OTP delivery methods — are handled in Settings after login, but the authentication framework established at login governs all session security.

**At a Glance**

| Attribute        | Detail                                                       |
| ---------------- | ------------------------------------------------------------ |
| Module           | Banking › Login                                              |
| MFA Method       | Username + Password + OTP (email or SMS)                     |
| Recovery Options | Forgot User ID, Forgot Password, Unlock Account              |
| Biometric        | Touch ID / Face ID on supported devices                      |
| Session Security | Tokens expire on inactivity; trusted device option available |

## Key Use Cases

| Use Case         | Who Uses It                                  | What They Do                                                     | Business Value                                                      |
| ---------------- | -------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------- |
| First-Time Login | You newly enrolled                           | Enter User ID and password; complete OTP challenge               | Establishes authenticated session to access all digital services    |
| Biometric Login  | You are a returning member on trusted device | Enable Touch ID / Face ID during initial login session           | Eliminates manual credential entry on subsequent sessions           |
| Forgot Password  | You who cannot remember password             | Click Forgot Password, verify identity via OTP, set new password | Self-service recovery eliminates need to call CU support            |
| Unlock Account   | You locked out after failed attempts         | Use Unlock Account flow to verify identity and restore access    | Immediate self-service unblock without branch intervention          |
| Log Off          | You ending session                           | Click Log Off to securely terminate the session                  | Prevents unauthorized access if device is shared or left unattended |

## Step-by-Step Guide

**Step 1 — Launch the Login Screen**

The Summerville Credit Union digital banking login page is displayed. A welcome modal appears over a blue background with financial service icons, showing the User ID and Password input fields along with a prominent 'Log in' button.

<figure><img src="../../.gitbook/assets/img_ba47001101d4.png" alt="" width="620"><figcaption></figcaption></figure>

**Step 2 — Enter Credentials & Click Log In**

Enter your registered User ID and password into the respective fields and click 'Log in' to begin the authentication process.

<figure><img src="../../.gitbook/assets/img_ba47001101d4.png" alt="" width="620"><figcaption></figcaption></figure>

**Step 3 — Select OTP Delivery Method**

The Verification screen appears, offering three OTP delivery options: 'Send me a text message', 'Call me', and 'Send me an email'. Select your preferred method to receive the one-time passcode.

<figure><img src="../../.gitbook/assets/img_af24a462cfc3.png" alt="" width="620"><figcaption></figcaption></figure>

**Step 4 — Select Email Address (if Email chosen)**

The email OTP option is selected. The screen displays 'Send me an email' as the chosen method with an input field for you to confirm or select the registered email address for receiving the verification code.

<figure><img src="../../.gitbook/assets/img_d002b4246e94.png" alt="" width="620"><figcaption></figcaption></figure>

**Step 5 — Enter OTP Code**

A verification code entry form is displayed with an 'Enter code' text field. A 'Didn't receive your code? Resend' link is available below the input for you if you need the OTP re-sent.

<figure><img src="../../.gitbook/assets/img_a44197ff9ff7.png" alt="" width="620"><figcaption></figcaption></figure>

**Step 6 — Arrive at Dashboard**

The Dashboard loads successfully after authentication. The screen greets you by name and displays account balances, a quick transfer widget, and promotional messaging.

<figure><img src="../../.gitbook/assets/img_76d367ae9a07.png" alt="" width="340"><figcaption></figcaption></figure>

**Step 7 — Access Self-Service Recovery Options**

The self-service recovery page is displayed with three options: 'I forgot My user ID', 'I forgot My Password', and 'Unlock My user ID'. Each option has an icon and a 'Back to login' link at the bottom to return to the main login screen.

<figure><img src="../../.gitbook/assets/img_8692cb9435f4.png" alt="" width="620"><figcaption></figcaption></figure>

**Step 8 — Forgot User ID — Enter SSN & Date of Birth**

The Forgot User ID form is displayed. You are prompted to enter your Social Security Number (SSN) in two matching fields for confirmation, and your Date of Birth. A note states the User ID will be sent to your registered email and/or mobile number. Cancel and Retrieve User ID buttons are at the bottom.

<figure><img src="../../.gitbook/assets/img_441889e049ea.png" alt="" width="620"><figcaption></figcaption></figure>

**Step 9 — Forgot Password — Enter Membership & User ID**

The Forgot Password flow begins at Step 1 (User info) of a 5-step wizard: User info, Identity verification, Authentication, Password reset, and Success. Enter your Membership Number and User ID, then click Next to proceed. Cancel is also available.

<figure><img src="../../.gitbook/assets/img_e1c29585d221.png" alt="" width="620"><figcaption></figcaption></figure>

**Step 10 — Unlock Account — Enter User ID & Membership**

The Unlock Account flow begins at Step 1 (Member verification) of a 5-step wizard: Member verification, Identity verification, One-Time Passcode (OTP), Choose password, and Success. Enter your User ID and Membership Number, then click Next. Cancel is also available.

<figure><img src="../../.gitbook/assets/img_dfa5fbc96fa9.png" alt="" width="620"><figcaption></figcaption></figure>
