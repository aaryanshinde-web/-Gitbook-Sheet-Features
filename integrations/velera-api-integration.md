---
description: Velera (formerly PSCU) API integration — powering card controls, alerts, and rewards features within nFinia Digital Banking for Summerville Credit Union.
---

# Velera API Integration

**Vendor:** Velera (formerly PSCU)\
**Module:** Cards — Controls, Alerts & Rewards\
**Integration Type:** Embedded API (Server-to-Server)

---

## Overview

Velera (rebranded from PSCU in 2024) is Summerville Credit Union's card processing network. The Velera API integration exposes card management capabilities — including card controls, spending alerts, and rewards balance — directly within nFinia's Cards module, giving you a unified experience without leaving the app.

Members can lock or unlock their debit and credit cards instantly, set spending restrictions by merchant category or geography, receive real-time push notifications for transaction activity, and view their rewards balance — all from within the nFinia digital banking platform.

---

## Key Features

| Feature | Description |
| --- | --- |
| **Card On/Off Toggle** | Instantly lock or unlock a debit or credit card |
| **Spending Controls** | Set limits by merchant category, transaction type, or geography |
| **Location Controls** | Restrict card use to domestic or specific geographic regions |
| **Real-Time Alerts** | Push notifications for transactions, declines, and balance thresholds |
| **Rewards Balance** | View current reward points balance and redemption options |
| **Travel Notifications** | Notify Velera of travel dates to prevent out-of-country declines |

---

## Integration Details

| Parameter | Details |
| --- | --- |
| **API Type** | REST (JSON) |
| **Auth Method** | OAuth 2.0 client credentials |
| **Real-Time Events** | Webhook-based push from Velera to nFinia |
| **Card Types Supported** | Debit and Credit cards issued under Summerville CU's Velera BIN |
| **Integration Mode** | Server-to-server; no direct member-to-Velera communication |
| **Data Sync** | Member card data synced from Velera at login and on-demand refresh |

---

## How It Works

When you navigate to the Cards section in nFinia, the platform makes a server-side call to the Velera API using your card identifiers. Velera returns current card status, spending control settings, alerts configuration, and rewards balance. Changes you make (e.g., toggling a card off, adding a merchant restriction) are sent back to Velera via the API in real time.

Real-time transaction alerts are delivered from Velera to nFinia via webhook, which then triggers push notifications to your enrolled device.

---

## End-to-End Workflow

**Step 1 — Member logs into nFinia**\
When you log into the nFinia digital banking platform, the system automatically initiates a server-side call to the Velera API using your linked card identifiers. This happens in the background during session initialisation, so by the time you navigate to the Cards module, your card data is already loaded and ready to display.

**Step 2 — Member navigates to Cards module**\
Navigate to the Cards section from the top navigation bar. The Cards dashboard displays all debit and credit cards issued under Summerville CU's Velera BIN. Each card tile shows its current lock/unlock status, and the detail view provides access to spending controls, alert configuration, and rewards balance — all populated in real time from Velera's API response.

**Step 3 — Member makes a change**\
When you make a change — such as toggling a card off, setting a merchant category restriction, or configuring a spend alert — nFinia immediately sends the updated preference to Velera via the REST API. The request is signed with the platform's OAuth 2.0 client credentials and contains only the specific change being made, not the member's full card details.

**Step 4 — Velera processes the change**\
Upon receiving the API request, Velera validates the change and applies it to the card's control profile in real time. Enforcement is immediate — the next transaction on that card will be subject to the updated rules. There is no batch processing or overnight sync required.

**Step 5 — Real-time alerts delivered**\
When a qualifying transaction occurs on the card, Velera's system dispatches a webhook event to the nFinia platform. nFinia processes the event payload and pushes a notification to your enrolled device — delivering the alert within seconds of the transaction occurring. This near-instant notification loop is what enables members to detect and respond to suspicious card activity in real time.

---

## Covered Feature Guides

| Guide | Reference |
| --- | --- |
| Card Controls | [Card Controls](../bill-pay-loans-and-cards/card-controls-and-spending/card-controls.md) |
| Card Alerts | [Card Alerts](../bill-pay-loans-and-cards/card-controls-and-spending/card-alerts.md) |
| Spending Limits | [Spending Limits](../bill-pay-loans-and-cards/card-controls-and-spending/spending-limits.md) |
| Location Controls | [Location Controls](../bill-pay-loans-and-cards/card-controls-and-spending/location-controls.md) |
| Usage Controls | [Usage Control](../bill-pay-loans-and-cards/card-controls-and-spending/usage-control.md) |

---

## Configuration Notes

{% hint style="info" %}
**Branding Note:** Velera was rebranded from PSCU in 2024. Any legacy documentation referencing "PSCU" refers to the same integration.
{% endhint %}

{% hint style="warning" %}
**BIN Configuration:** Card controls and alerts only apply to cards issued under Summerville CU's Velera BIN. Cards from other networks will not appear in this module.
{% endhint %}

---

## Error Handling

| Scenario | Member Experience | Resolution |
| --- | --- | --- |
| Velera API unavailable | Card controls screen shows an error or spinner | Retry; contact Tyfone Support if issue persists |
| Card not found in Velera | Card does not appear in the Cards module | Verify card is issued under the Velera BIN; contact FI support |
| Webhook delivery failure | Member does not receive transaction alert | Check webhook configuration in Velera integration settings |
| OAuth token expired | API calls fail silently | nFinia automatically refreshes the client credential token on expiry |

---

## FAQs

**Q: Which cards are visible in the Velera card controls module?**\
Only debit and credit cards issued under Summerville Credit Union's Velera BIN are visible. Cards from other processors are not supported.

**Q: Are card controls enforced immediately?**\
Yes. Controls set through the nFinia interface are transmitted to Velera via the REST API and applied to the card's control profile in real time. The very next transaction on the card will be subject to the updated setting — there is no delay, batch sync, or confirmation window.

**Q: What happens if you travel internationally without setting a travel notification?**\
Velera's fraud detection system may automatically decline international transactions if no travel notification is on file for those dates and destinations. This is a protective measure against card fraud, but it can result in legitimate purchases being blocked while abroad. Members should set a travel notification in nFinia before departure to ensure their cards are approved at international terminals during the travel window.

**Q: Can rewards be redeemed through nFinia?**\
The current Velera integration surfaces your rewards balance within the nFinia Cards module so you can see your accumulated points at a glance. Redemption options — such as cash back, gift cards, or travel — depend on how Summerville CU has configured the Velera rewards portal. Contact the credit union or visit the Velera redemption portal for available options.

---

*Velera (formerly PSCU) is Summerville Credit Union's card processing partner. For technical integration questions, contact the Tyfone Delivery team. For card-related member issues, refer to the FI's member services team.*
