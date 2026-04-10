---
description: >-
  Official feature documentation for SummerVille Credit Union's nFinia Digital
  Banking platform — covering all tracked features, vendor integrations, and
  reference guides.
cover: .gitbook/assets/cover.png
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# README

Welcome to the **Summerville Credit Union nFinia Platform Documentation** — the single authoritative reference for all features, integrations, and technical specifications tracked in the Feature Documentation Tracking sheet.

This space is maintained by the Tyfone product and implementation team and is organized to mirror the nFinia app's own navigation structure, making it easy to locate documentation for any feature a member may encounter.

***

## What's Inside

| Section                    | What You'll Find                                                                                                                                                                                                                    |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Authentication & Login** | Login flow, MFA (CSUM-01, CSUM-22), Trusted Devices & Cryptographic Auth (CSUM-25)                                                                                                                                                  |
| **Dashboard**              | Dashboard Activities (CSUM-02), Recent Activities & Insights (CSUM-21)                                                                                                                                                              |
| **Accounts**               | Account Overview (CSUM-03, CSUM-04), Credit Score (CSUM-24), Profile & Membership (CSUM-23)                                                                                                                                         |
| **Cards**                  | Card Controls, Card Alerts, Spending Limits, Location Controls, Usage Controls                                                                                                                                                      |
| **Move Money**             | Transfer Hub (CSUM-05), Own Account & Member Transfers (CSUM-06–07), External ACH (CSUM-08), FedNow (CSUM-09), Wire (CSUM-12), Zelle (CSUM-11), Bill Pay (CSUM-14), Quick Pay (CSUM-13), Skip-A-Pay (CSUM-18), Mobile Check Deposit |
| **More Menu**              | Alerts & Notifications (CSUM-16), Inbox (CSUM-17), Personal Info (CSUM-19), Settings (CSUM-20)                                                                                                                                      |
| **Vendor Integrations**    | Prisma, Direct/Web Connect, ZenDesk, FICS API, BDI SSO, Velera, MeridianLink, Plaid IAV                                                                                                                                             |
| **Reference Documents**    | SummerVille CU Master Guide, Delegated Access, Certificate Management, Custom Account Grouping, Joint Owners & Beneficiary                                                                                                          |

***

## How to Use This Guide

{% hint style="info" %}
**Navigation Tip:** Use the left sidebar to browse by module, or press `Ctrl+K` / `Cmd+K` to search any feature by name or CSUM number.
{% endhint %}

Documentation is organized into three tiers:

1. **Step-by-step CSUM Guides** — End-to-end walkthroughs for every feature, with screenshots and use-case tables. Reference numbers follow the format `CSUM-XX`.
2. **Vendor Integration Pages** — Configuration, architecture, and member-facing flow documentation for all third-party integrations.
3. **Reference Documents** — Release notes, design specifications, and master guides converted from source DOCX files.

***

## Platform Overview

The **nFinia** digital banking platform from **Tyfone** powers Summerville Credit Union's member-facing digital experience across:

| Channel         | Notes                                                      |
| --------------- | ---------------------------------------------------------- |
| **Web Browser** | Full-featured desktop experience at `diamondcu.nfinia.com` |
| **iOS App**     | Native iPhone and iPad app with biometric authentication   |
| **Android App** | Native Android app, feature-parity with iOS                |

All channels share a unified feature set. Where channel-specific behavior exists, it is called out within the relevant CSUM guide.

***

## Document Conventions

| Convention    | Meaning                                                 |
| ------------- | ------------------------------------------------------- |
| `CSUM-XX`     | Consolidated Step-by-Step Member guide reference number |
| **Bold text** | UI element label, button, or field name                 |
| `Code`        | System value, URL, or technical identifier              |
| > Blockquote  | Important note or callout                               |
| 💡 Hint block | Tip, warning, or prerequisite                           |

***

## Maintenance & Updates

This documentation is synced via **GitHub Sync** from the repository `aaryanshinde-web/-Gitbook-Sheet-Features` (branch: `main`). Changes pushed to the repository are automatically reflected here within minutes.

| Item                | Detail                                        |
| ------------------- | --------------------------------------------- |
| **Platform**        | Tyfone nFinia                                 |
| **Client**          | Summerville Credit Union                      |
| **Maintained by**   | Tyfone Product & Implementation Team          |
| **Source Repo**     | `aaryanshinde-web/-Gitbook-Sheet-Features`    |
| **Sync Branch**     | `main`                                        |
| **Feature Tracker** | Feature Documentation Tracking (Google Sheet) |
