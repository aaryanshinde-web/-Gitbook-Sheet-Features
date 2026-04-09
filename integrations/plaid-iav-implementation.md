---
description: Plaid Instant Account Verification (IAV) integration — fast, secure external account linking for ACH transfers within nFinia Digital Banking.
---

# Plaid IAV — Instant Account Verification

**Vendor:** Plaid\
**Module:** Move Money → External Transfers — Add External Account\
**Integration Type:** Embedded SDK (Client-Side)

---

## Overview

Plaid Instant Account Verification (IAV) enables Diamond Credit Union members to link external bank accounts for ACH transfers in seconds — without waiting for the traditional 1–3 day micro-deposit verification process. Members authenticate directly with their external bank through Plaid's secure, encrypted Link flow, and the account is verified and ready to use immediately.

---

## Key Features

| Feature | Description |
| --- | --- |
| **Instant Verification** | Accounts at 12,000+ supported institutions verified in real time |
| **Micro-Deposit Fallback** | Non-IAV banks fall back to traditional micro-deposit verification automatically |
| **Read-Only Access** | Plaid only reads account/routing numbers — no transaction data is stored |
| **Re-authentication** | Expired tokens prompt the member to re-authenticate via the Link flow |
| **Supported Account Types** | Checking and savings accounts at supported institutions |

---

## Member Flow

1. Member navigates to **Move Money → External ACH → Add External Account**.
2. Plaid Link modal launches within nFinia.
3. Member selects their bank from the institution search.
4. Member enters their online banking credentials (directly to Plaid — never stored by nFinia or Diamond CU).
5. Plaid verifies the account and returns the verified account/routing number to nFinia.
6. The external account is immediately available for ACH transfer initiation.

---

## Security & Compliance

{% hint style="warning" %}
**Credential Handling:** Member banking credentials are entered directly into Plaid's encrypted Link flow. Diamond Credit Union and nFinia never see or store these credentials.
{% endhint %}

| Control | Details |
| --- | --- |
| **Data Encryption** | TLS 1.2+ for all data in transit |
| **Credential Storage** | Plaid does not store member credentials after verification |
| **Regulatory Compliance** | Plaid is SOC 2 Type II certified and CCPA/GDPR compliant |
| **Token Lifespan** | Access tokens expire; members re-authenticate if connection lapses |

---

## Related Documentation

- [External ACH Transfer — CSUM-08](../transfers-and-payments/external-ach-wire-and-instant/CSUM-08-External-ACH-Transfer.md)
