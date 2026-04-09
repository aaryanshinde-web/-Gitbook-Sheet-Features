---
description: MeridianLink Loan Origination SSO integration — seamless loan application experience for Diamond Credit Union members within nFinia Digital Banking.
---

# Loan Origination SSO — MeridianLink

**Vendor:** MeridianLink (formerly CRIF Lending Solutions)\
**Module:** More Menu → Apply for a Loan\
**Integration Type:** SSO Redirect

---

## Overview

The MeridianLink integration allows Diamond Credit Union members to initiate and complete loan applications directly from nFinia. Through a single sign-on redirect, members are transferred to MeridianLink's loan origination portal with their identity pre-authenticated, eliminating the need to re-enter personal information.

---

## Key Features

| Feature | Description |
| --- | --- |
| **One-Click Loan Application** | Member taps "Apply" and is taken directly to a pre-populated application form |
| **SSO Authentication** | nFinia session credentials are used to authenticate — no separate login |
| **Product Selection** | Auto, personal, home equity, and other loan types supported |
| **Application Status** | Application status can be checked from within MeridianLink portal |
| **Decision Delivery** | Conditional or final decision displayed in-portal; confirmation sent via email |

---

## Member Flow

1. Member navigates to **More Menu → Loans → Apply for a Loan** in nFinia.
2. nFinia generates a time-limited SSO token for MeridianLink.
3. Member is redirected to the MeridianLink loan origination portal with identity pre-filled.
4. Member selects loan type and completes the application.
5. Upon completion or exit, member is returned to nFinia.

---

## Configuration Notes

{% hint style="info" %}
**Pre-Fill Data:** Member name, address, email, phone, and date of birth are passed via SSO token to pre-populate the application — reducing friction and drop-off rates.
{% endhint %}

| Parameter | Details |
| --- | --- |
| **Auth Method** | SSO token (SAML 2.0 or JWT) |
| **Loan Types** | Auto, Personal, HELOC, Mortgage, Student (per Diamond CU product setup) |
| **Decision Timeline** | Instant for pre-approved offers; 1–3 days for full underwriting |
| **Integration URL** | Configured per Diamond CU MeridianLink tenant |
