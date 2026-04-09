---
description: Velera (formerly PSCU) API integration — powering card controls, alerts, and rewards features within nFinia Digital Banking for Diamond Credit Union.
---

# Velera API Integration

**Vendor:** Velera (formerly PSCU)\
**Module:** Cards — Controls, Alerts & Rewards\
**Integration Type:** Embedded API (Server-to-Server)

---

## Overview

Velera (rebranded from PSCU in 2024) is Diamond Credit Union's card processing network. The Velera API integration exposes card management capabilities — including card controls, spending alerts, and rewards balance — directly within nFinia's Cards module, giving members a unified experience without leaving the app.

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

| Parameter | Details |
| --- | --- |
| **API Type** | REST (JSON) |
| **Auth Method** | OAuth 2.0 client credentials |
| **Real-Time Events** | Webhook-based push from Velera to nFinia |
| **Card Types Supported** | Debit and Credit cards issued under Diamond CU's Velera BIN |
