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
At login, nFinia fetches your card data from Velera using your linked card identifiers.

**Step 2 — Member navigates to Cards module**\
The Cards dashboard displays all debit and credit cards linked to the Velera BIN, with current lock/unlock status, controls, and rewards balance.

**Step 3 — Member makes a change**\
Toggle a card off, sets a merchant category restriction, or configures an alert. nFinia sends the update to Velera via the REST API.

**Step 4 — Velera processes the change**\
Velera applies the control or preference in real time. The enforcement takes effect immediately for subsequent card transactions.

**Step 5 — Real-time alerts delivered**\
When a transaction occurs on the card, Velera sends a webhook event to nFinia, which dispatches a push notification to you.

---

## Covered CSUM Guides

| Guide | Reference |
| --- | --- |
| Card Controls | [Card Controls](../bill-pay-loans-and-cards/card-controls-and-spending/Card%20Controls.md) |
| Card Alerts | [Card Alerts](../bill-pay-loans-and-cards/card-controls-and-spending/Card%20Alerts.md) |
| Spending Limits | [Spending Limits](../bill-pay-loans-and-cards/card-controls-and-spending/Spending%20Limits.md) |
| Location Controls | [Location Controls](../bill-pay-loans-and-cards/card-controls-and-spending/Location%20Controls.md) |
| Usage Controls | [Usage Control](../bill-pay-loans-and-cards/card-controls-and-spending/Usage%20Control.md) |

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
Yes. Controls set via the API are enforced by Velera in real time on subsequent transactions.

**Q: What happens if you travel internationally and haven't set a travel notification?**\
International transactions may be declined by Velera's fraud detection. Members should set a travel notification in nFinia before traveling to prevent this.

**Q: Can rewards be redeemed through nFinia?**\
The Velera integration currently displays the rewards balance. Redemption options depend on Velera's redemption portal configuration for Summerville CU.

---

*Velera (formerly PSCU) is Summerville Credit Union's card processing partner. For technical integration questions, contact the Tyfone Delivery team. For card-related member issues, refer to the FI's member services team.*
