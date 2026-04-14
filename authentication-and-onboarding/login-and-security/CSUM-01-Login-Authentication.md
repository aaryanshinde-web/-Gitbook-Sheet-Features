---
description: Log in securely using multi-factor authentication with OTP verification
---

# Login & Authentication

## Summary

Login & Authentication is the security entry point to nFinia Digital Banking — every session, every transaction, and every self-service action begins here. The flow is designed around a two-layer identity check: members present a registered username and password, then complete a one-time passcode (OTP) challenge delivered to a pre-registered phone or email address. This dual-factor approach aligns with NCUA examination expectations for member authentication and provides the credit union with a defensible access control posture.

Once authenticated, the member lands on the Dashboard with full access to account data, transfers, payments, and all self-service features. Returning members on trusted devices can bypass the OTP step entirely through the "Remember this device" option, reducing session friction without compromising security. Biometric login via Face ID or Touch ID is available on supported mobile devices, and self-service recovery links for forgotten credentials and locked accounts are accessible directly from the login screen.

## Key Use Cases

* Sign in to digital banking using a username, password, and OTP — the standard multi-factor flow required on every new device or unrecognised browser
* Select the OTP delivery method that best matches the member's preferences: text message, phone call, or email
* Register a trusted device to skip OTP on future logins from that browser or device, reducing login friction for frequent users
* Complete a first-time session and establish an authenticated digital banking context
* Enable biometric login (Face ID or Touch ID) on a compatible mobile device for one-tap subsequent access
* Access self-service recovery options — Forgot User ID, Forgot Password, or Unlock Account — directly from the login screen without contacting the credit union

## End-to-End Workflow

**Step 1: Open the Login Screen**

Navigate to the Summerville CU digital banking URL to load the login page, which presents the User ID and Password fields along with self-service recovery links for Forgot User ID, Forgot Password, and Unlock Account. This is the only entry point to the platform — no account data or functionality is accessible prior to successful authentication.

<figure><img src="../../.gitbook/assets/img_ba47001101d4.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 2: Enter Credentials and Submit**

Enter your registered User ID and password in the respective fields and click **Log In** to submit your credentials for validation. If the credentials are recognised, the platform immediately advances to the OTP verification step; if they are not, an error is displayed and the session remains unauthenticated.

<figure><img src="../../.gitbook/assets/img_ba47001101d4.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 3: Select OTP Delivery Method**

The Verification screen presents three delivery options for the one-time passcode: **Send me a text message**, **Call me**, or **Send me an email** — all routed to the contact details registered on the account. Select the method most accessible at the time of login; this choice can be changed on subsequent logins and does not alter the registered contact information on the account.

<figure><img src="../../.gitbook/assets/img_af24a462cfc3.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 4: Confirm Email Address (if Email is Selected)**

If email delivery is chosen, the platform displays an input field to confirm or select the registered email address to which the OTP should be sent. Verify the destination address is correct and proceed — the OTP will not be sent until this confirmation step is completed.

<figure><img src="../../.gitbook/assets/img_d002b4246e94.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 5: Enter the OTP and Choose Whether to Trust This Device**

Enter the one-time passcode received via the selected channel into the **Enter code** field; a **Resend** link is available if the code was not received within the expected window. Before submitting, review the **Remember this device** checkbox — checking it registers the current browser or device as trusted, so future logins from this device will skip the OTP step and require only the User ID and password. Trusted devices can be reviewed and revoked at any time from the Device Management page under the More menu.

<figure><img src="../../.gitbook/assets/img_a44197ff9ff7.png" alt="" width="480"><figcaption></figcaption></figure>

**Step 6: Arrive at the Authenticated Dashboard**

Successful OTP entry completes the authentication session and loads the Dashboard, which displays account balances, a quick transfer widget, upcoming scheduled payments, and the full navigation menu. All digital banking features — transfers, bill pay, card controls, account management, and integrations — are now accessible within this authenticated session.

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>
