---
description: >-
  Approve or deny sensitive account changes from a registered mobile device
  using push-based trusted device verification.
---

# Trusted Devices Prompt

## Summary

The Trusted Device Prompt is nFinia's push-based second-factor verification mechanism that intercepts sensitive member actions — such as disabling account alerts — initiated from a web browser session, and requires confirmation from a pre-enrolled mobile device before the change is processed. Rather than relying on SMS one-time passcodes, which are vulnerable to SIM-swap attacks and phishing, the platform routes the verification directly to a registered phone or tablet, ensuring that both credential ownership and physical device possession are required. For Summerville CU, this means stronger member account protection, a timestamped audit trail for every verified action, and an MFA posture that aligns with NCUA examination expectations.

***

## Use Cases

The most common scenario is a member accessing their account from a web browser who toggles off the Enable Notifications switch — the system immediately intercepts the action and sends a push notification to their enrolled mobile device, blocking the change until they physically confirm it. Members who have registered more than one trusted device can select which phone or tablet receives the verification push, giving them flexibility across devices without reducing security controls. When a member receives a verification request they don't recognize — a signal that their web credentials may have been compromised — they tap "No it's not me" on the mobile confirmation screen, which immediately blocks the action and flags the session as potentially unauthorized. Finally, if the member doesn't respond before the countdown expires, the web session times out automatically and the pending verification is voided, ensuring no approval requests remain open longer than the allowed window.

***

## Step-by-Step Guide

### Step 1 — Open the More Options Menu

From the main Banking navigation, click **More** to expand the full options menu. You'll see a grid of account management areas including Notifications and Alerts, Profile, Manage My Services, and others.

![More Options Screen](<../.gitbook/assets/Unknown image>)

***

### Step 2 — Go to Notifications and Alerts

Select **Notifications and Alerts** from the grid. This opens your Delivery Preferences, where you control how and where the platform sends you account activity alerts.

![Notifications and Alerts — Delivery Preferences](<../.gitbook/assets/Unknown image (1)>)

***

### Step 3 — Toggle Off Enable Notifications

On the Delivery Preferences screen, you'll see the master **Enable Notifications** toggle at the top, along with individual controls for push, SMS, and email alerts. Switching the **Enable Notifications** toggle to OFF is a sensitive action — because disabling alerts reduces your visibility into account activity, the platform doesn't process this immediately and instead routes you through trusted device verification.

***

### Step 4 — Select Your Trusted Device

The **Verify Your Disable Alerts Request** screen appears, listing every mobile device you've previously enrolled as trusted, along with each device's name and the last time it was accessed. Tap the device you want to receive the verification push notification — this is the phone or tablet you're holding right now or have nearby.

![Trusted Device Required — Select Device](<../.gitbook/assets/Unknown image (2)>)

***

### Step 5 — Wait for the Push Notification

After selecting your device, nFinia transitions to a **Verifying Your Disable Alerts Request** waiting screen with a live countdown timer. Do not refresh this page — refreshing will cancel the verification and you'll need to start over. The countdown tells you exactly how long you have (typically around 60 seconds) to approve from your mobile device before the request expires.

![Trusted Device Required — Verification In Progress](<../.gitbook/assets/Unknown image (3)>)

***

### Step 6 — Receive the Push Notification on Your Mobile Device

Your Summerville CU mobile app will deliver a push notification to the device you selected. The notification reads: _"A request to disable your alerts has been initiated. Please confirm this action to proceed."_ Tap the notification to open the Summerville CU app and reach the confirmation screen.

![Mobile Push Notification](<../.gitbook/assets/Unknown image (4)>)

***

### Step 7 — Approve or Deny the Request

The full-screen confirmation view shows you exactly what action is being requested, which device or browser initiated it (e.g., Chrome on Windows), and the timestamp — giving you everything you need to verify this was you. Tap **Yes, it's me** to approve, or **No it's not me** to block the action immediately and protect your account.

![Mobile Confirmation Screen](<../.gitbook/assets/Unknown image (5)>)

***

### Step 8 — Verification Complete

After tapping **Yes, it's me**, the mobile app confirms: _"Advanced Device Security Verified — You have confirmed your identity successfully."_ Tap **Close** to dismiss, and your web session will automatically complete the requested change. An audit log entry is created recording the action, the originating session, the approving device, and the timestamp.

![Advanced Device Security Verified](<../.gitbook/assets/Unknown image (6)>)
