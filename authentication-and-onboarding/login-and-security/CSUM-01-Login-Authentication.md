---
description: Log in securely using multi-factor authentication with OTP verification
---

# Login & Authentication

## Summary

Login & Authentication is the secured entry point to nFinia Digital Banking — every session, payment instruction, and account action begins with identity verification here. The platform uses a two-factor model: members authenticate with a registered User ID and password, then confirm identity via a one-time passcode (OTP) delivered to a pre-registered phone number or email. This design satisfies NCUA member authentication expectations and provides the credit union with a defensible, auditable access control posture that scales from individual retail members to multi-user business accounts.

For business members managing cash flow, approving transfers, or reviewing commercial activity throughout the day, the "Remember this device" option and biometric login (Face ID / Touch ID) reduce session friction without weakening the authentication chain. Self-service recovery links for forgotten credentials and locked accounts are available directly on the login screen, eliminating branch or call-center dependency for common access issues.

## Key Use Cases

| Use Case | Who Uses It | What They Do | Business Value |
| --- | --- | --- | --- |
| Standard login with MFA | All members — retail and business | Enter User ID and password, select OTP channel, submit passcode | Confirms identity before any account data or transaction capability is accessible |
| Trusted device registration | Frequent users — business members monitoring cash flow daily | Check "Remember this device" during OTP step | Subsequent logins require only credentials — OTP step is skipped on that device |
| Biometric login | Mobile users on supported devices | Enable Face ID or Touch ID at the credential step | One-tap authentication for repeat sessions without entering a password |
| First-time login | New members completing onboarding | Complete credential entry and full MFA flow for the first session | Establishes authenticated session and binds device trust if elected |
| Account recovery | Members with forgotten credentials or locked accounts | Use Forgot User ID, Forgot Password, or Unlock Account links on login screen | Full self-service recovery without contacting the credit union |

For credit unions with business banking members, reliable and low-friction authentication directly affects how often those members engage with cash management, transfer approvals, and account monitoring — making this the most critical UX touchpoint on the platform.

## End-to-End Workflow

### Prerequisites

* Active nFinia digital banking enrollment with a registered User ID and password
* At least one verified contact on file (mobile number or email) for OTP delivery
* For biometric login: a supported mobile device with Face ID or Touch ID configured at the OS level

### Step-by-Step Flow

**Step 1: Open the Login Screen**

Navigate to the Summerville CU digital banking URL to load the login page, which presents the User ID and Password input fields along with self-service recovery links for Forgot User ID, Forgot Password, and Unlock Account. This screen is the sole authenticated entry point — no account balances, transaction history, or payment features are accessible before credentials are validated.

<figure><img src="../../.gitbook/assets/img_ba47001101d4.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 2: Enter Credentials and Submit**

Enter your registered User ID and password, then click **Log In** to submit for validation against the nFinia authentication layer. A successful credential match advances the session to the OTP verification step; an incorrect entry returns an inline error and increments the failed-attempt counter, which will lock the account after the configured threshold is reached.

<figure><img src="../../.gitbook/assets/img_ba47001101d4.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 3: Select OTP Delivery Method**

The Verification screen presents three delivery options for the one-time passcode: **Send me a text message**, **Call me**, or **Send me an email** — all routed to contact details registered on the account. Select the channel most accessible at the moment; this selection applies only to the current session and does not modify the registered contact information on the account.

<figure><img src="../../.gitbook/assets/img_af24a462cfc3.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 4: Confirm Email Address (if Email is Selected)**

If email delivery is chosen, the platform prompts confirmation of the destination email address before dispatching the OTP. Verify the displayed address is current and correct, then proceed — the passcode will not be sent until this confirmation is submitted.

<figure><img src="../../.gitbook/assets/img_d002b4246e94.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 5: Enter the OTP and Decide on Device Trust**

Enter the one-time passcode in the **Enter code** field; use the **Resend** link if the code was not received within the expected window. Before submitting, evaluate the **Remember this device** checkbox — checking it registers this browser or device as trusted, eliminating the OTP requirement on all future logins from this device, while unchecking it enforces full MFA on every session. Trusted devices can be reviewed and individually revoked at any time from Device Management under the More menu.

<figure><img src="../../.gitbook/assets/img_a44197ff9ff7.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 6: Access the Authenticated Dashboard**

Successful OTP entry completes the authentication session and loads the Dashboard, displaying account balances, a quick transfer panel, upcoming scheduled payments, and the full navigation menu. All digital banking capabilities — fund transfers, bill pay, card controls, account management, and third-party integrations — are now accessible within this session.

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

### Decision Points & Branching

* **Correct credentials + OTP:** Session authenticated; member lands on Dashboard
* **Incorrect credentials:** Error displayed; failed-attempt counter incremented; account locks after configured threshold
* **Trusted device (Remember this device checked):** Future logins on this device skip OTP and require only User ID and password
* **Biometric enabled:** Subsequent mobile sessions launch Face ID / Touch ID prompt instead of the credential entry screen
* **Forgotten credentials / locked account:** Member uses self-service recovery links on the login screen

### Error Handling

| Scenario | Member Experience | Recovery |
| --- | --- | --- |
| Incorrect User ID or password | Inline error; attempt counter incremented | Re-enter correct credentials; use Forgot User ID or Forgot Password if needed |
| Account locked after failed attempts | Lock message displayed on login screen | Use Unlock Account self-service link or contact the credit union |
| OTP not received | Use "Resend" link to request a new code | Switch delivery method if the primary contact is unavailable |
| OTP expired | Re-entry prompt or session restart required | Request a new OTP via Resend or restart the login flow |
| Biometric failure | Device falls back to credential entry screen | Complete standard User ID and password login |
