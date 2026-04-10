---
description: >-
  Access eStatements, manage eStatement notifications, and redeem rewards
  through SSO portals.
---

# Velera — Credit Card eStatements & Rewards

_Module: Banking › Cards › Card Details › eStatements / Rewards_

## Summary

This document covers three features available for PSCU credit cardholders in nFinia Digital Banking: Credit Card eStatements, CURewards SSO, and CashBackMall SSO.

Credit Card eStatements lets members access and download their monthly credit card statements as PDFs directly from the Cards module or via eDocuments. Statements are stored at the card level in Velera and formatted per the credit union's branding. Members can also configure their eStatement delivery email address and set up notification alerts when a new statement is available.

CURewards SSO enables members enrolled in the Traditional Rewards program to view their current rewards balance and points expiring soonest — and to redeem them — all without leaving nFinia. CashBackMall SSO provides the same experience for members enrolled in the Cash Back Rewards program.

## At a Glance

| Attribute | Detail |
| --- | --- |
| Feature Names | Credit Card eStatements · CURewards SSO · CashBackMall SSO |
| Module Location | Banking › Cards (card tile) and Banking › eDocuments |
| Statement Format | PDF download — credit union branded, Velera format |
| Delivery Email | Managed separately from Core; members can sync, keep existing, or enter a new address |
| Rewards Programs | Traditional Rewards (CURewards) and Cash Back Rewards (CashBackMall) |
| Channels | Online Banking ✓ |
| Supported Cores | Correlation, Ultradata |
| Release Version | 10.41 |

## Key Use Cases

| Use Case | Member Goal | Steps | Outcome |
| --- | --- | --- | --- |
| Download a credit card statement | Access a monthly PDF statement for a credit card | Cards › select card › eStatements on card tile → tap a statement to download PDF | PDF opens / downloads; formatted per credit union branding |
| Access statements via eDocuments | Find all document types in one place | Search "eDocuments" or navigate to More › eDocuments; filter to credit card statements | All available credit card statements listed alongside other account documents |
| Update eStatement email address | Ensure statement notifications go to the right email | When prompted on first access, choose: sync from Core, keep Velera address, or enter a new one | eStatement notifications are sent to the chosen email address going forward |
| Receive eStatement alerts | Get notified when a new statement is ready | Confirm alert preference during eStatement setup; alerts fire when Velera posts a new statement | Member receives a notification when a new monthly statement is available |
| View & redeem CURewards points | Check rewards balance and redeem points (Traditional Rewards) | Cards › select credit card tile › Redeem/View; SSO launches the CURewards portal | Member sees current points balance and earliest expiry; can redeem via the rewards portal |
| View & redeem CashBack rewards | Check cash back balance and redeem (Cash Back Rewards program) | Cards › select credit card tile › Redeem/View; SSO launches the CashBackMall portal | Member sees available cash back and earliest expiry; can redeem via CashBackMall |

---

## Credit Card eStatements

_📍 Path A: Banking › Cards › \[select card] › eStatements on card tile_
_📍 Path B: Banking › eDocuments (via Search or the More section)_

### Step 1 — Open the Card Tile or eDocuments

Navigate to Cards and locate the credit card you want to view statements for. The card tile includes an eStatements shortcut. Alternatively, use the Search bar or go to More › eDocuments to access statements alongside all other account documents.

<figure><img src="../.gitbook/assets/velera-statements-001.png" alt="" data-size="original"><figcaption>Cards module — locate the credit card tile with the eStatements shortcut.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-002.png" alt="" data-size="original"><figcaption>Tap the eStatements shortcut on the card tile to open the statements list.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-003.png" alt="" data-size="original"><figcaption>Alternate path — reach eStatements via More › eDocuments alongside other account documents.</figcaption></figure>

### Step 2 — Browse and Download a Statement

The eStatements screen lists available monthly statements for the selected credit card. Tap any statement to download it as a PDF. The PDF is styled in the credit union's branding and formatted by Velera. The download begins automatically on selection.

<figure><img src="../.gitbook/assets/velera-statements-004.png" alt="" data-size="original"><figcaption>eStatements screen — monthly statements listed newest-first for the selected card.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-005.png" alt="" data-size="original"><figcaption>Tap a statement row to initiate the PDF download.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-006.png" alt="" data-size="original"><figcaption>Downloaded PDF — rendered in the credit union's branding by Velera.</figcaption></figure>

### Step 3 — Set Your eStatement Delivery Email

When you access credit card eStatements for the first time, you will be prompted to confirm the email address where statement notifications should be sent. The email address stored in the core banking system may differ from the one Velera holds for your card. You will be given three options:

| Option | Description |
| --- | --- |
| **Option 1 — Sync from Core** | Update the email in Velera to match the address currently on file in the core system |
| **Option 2 — Keep Velera address** | Continue using the email address that Velera already has on file for this card |
| **Option 3 — Enter a new address** | Type a different email address to use specifically for credit card eStatement delivery |

> ⚠️ **Note:** Your credit card eStatement email can be different from the email used for other account types. Changing it here only affects credit card statement notifications via Velera.

<figure><img src="../.gitbook/assets/velera-statements-007.png" alt="" data-size="original"><figcaption>First-access prompt — choose how to set your eStatement delivery email.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-008.png" alt="" data-size="original"><figcaption>Option 1 — Sync from Core: Velera adopts the email currently on file in the core system.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-009.png" alt="" data-size="original"><figcaption>Option 2 — Keep Velera address: continue using the email Velera already has on file.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-010.png" alt="" data-size="original"><figcaption>Option 3 — Enter a new address: type a different email for eStatement delivery.</figcaption></figure>

### Step 4 — Configure eStatement Alerts

You can receive a notification each time a new credit card statement becomes available. Configure your alert preferences in the eStatements section. Once set up, an alert is sent when Velera posts a new monthly statement.

<figure><img src="../.gitbook/assets/velera-statements-011.png" alt="" data-size="original"><figcaption>eStatements alerts panel — toggle notifications for new monthly statements.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-012.png" alt="" data-size="original"><figcaption>Choose delivery channel — push, email, or both — for eStatement alerts.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-013.png" alt="" data-size="original"><figcaption>Confirmation screen — alert preference saved.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-014.png" alt="" data-size="original"><figcaption>Sample alert — the notification members receive when a new statement posts.</figcaption></figure>

---

## CURewards SSO (Traditional Rewards)

_📍 Navigation: Banking › Cards › \[select credit card tile] › Redeem/View_

Members enrolled in the Traditional Rewards program can view their rewards balance and the points expiring soonest directly from the credit card tile in nFinia. Tapping Redeem/View launches the CURewards portal via single sign-on (SSO), where members can browse and redeem their accumulated points without needing a separate login.

> ℹ️ **Tip:** Rewards points are shown on the card tile for a quick balance check. For full redemption options, tap Redeem/View to open the CURewards portal.

<figure><img src="../.gitbook/assets/velera-statements-015.png" alt="" data-size="original"><figcaption>Credit card tile — rewards balance and nearest expiry shown at a glance.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-016.png" alt="" data-size="original"><figcaption>Tap Redeem/View to launch the CURewards portal via SSO.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-017.png" alt="" data-size="original"><figcaption>CURewards portal — browse and redeem points without a separate login.</figcaption></figure>

---

## CashBackMall SSO (Cash Back Rewards)

_📍 Navigation: Banking › Cards › \[select credit card tile] › Redeem/View_

Members enrolled in the Cash Back Rewards program can view their available cash back balance and the cash back expiring soonest from the credit card tile. Tapping Redeem/View launches the CashBackMall portal via SSO, where members can browse shopping offers and redeem their cash back rewards.

> ℹ️ **Tip:** The cash back balance and nearest expiry are shown on the card tile at a glance. For full redemption and shopping options, tap Redeem/View to open CashBackMall.

<figure><img src="../.gitbook/assets/velera-statements-018.png" alt="" data-size="original"><figcaption>Credit card tile — cash back balance and nearest expiry shown at a glance.</figcaption></figure>

<figure><img src="../.gitbook/assets/velera-statements-019.png" alt="" data-size="original"><figcaption>CashBackMall portal — shopping offers and cash back redemption via SSO.</figcaption></figure>
