---
description: FICS Mortgage API integration — surfacing mortgage loan balances and details within nFinia Digital Banking for Diamond Credit Union members.
---

# Mortgage Balances — FICS API

**Vendor:** FICS (Financial Industry Computer Systems)\
**Module:** Accounts — Loan Detail\
**Integration Type:** Embedded API (Server-to-Server)

---

## Overview

The FICS API integration enables nFinia to retrieve and display mortgage loan account data directly from the FICS loan servicing system. Members with mortgage accounts held at Diamond Credit Union see their mortgage balance, payment history, and next payment due date alongside their other accounts on the Dashboard and Accounts pages.

---

## Key Features

| Feature | Description |
| --- | --- |
| **Mortgage Balance Display** | Current principal balance shown on the Accounts dashboard |
| **Payment Due Date** | Next scheduled payment date and amount |
| **Payoff Quote** | Payoff balance as of today (where supported) |
| **Loan Detail Page** | Dedicated account detail view for mortgage loan accounts |
| **Transaction History** | Recent payment history pulled from FICS |

---

## Data Flow

```
Member (nFinia App)
     │
     ▼
nFinia Platform (Tyfone)
     │  REST API call with account identifiers
     ▼
FICS Mortgage Servicing System
     │  Returns loan data (balance, due date, history)
     ▼
nFinia Platform → renders in Account Detail UI
```

---

## Configuration Notes

{% hint style="warning" %}
**API Credentials Required:** The FICS API endpoint URL, API key, and member account identifier mapping must be configured in the Tyfone admin portal during implementation.
{% endhint %}

| Parameter | Details |
| --- | --- |
| **API Type** | REST (JSON) |
| **Auth Method** | API Key in request header |
| **Data Refresh** | On-demand per page load (not cached) |
| **Error Handling** | Graceful — mortgage tile is hidden if API is unreachable |
