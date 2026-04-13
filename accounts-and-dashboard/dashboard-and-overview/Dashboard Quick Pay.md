---
description: >-
  Quick Pay and Quick Transfer — the Dashboard widget that lets members move
  funds between their own accounts without leaving the landing screen.
---

# Quick Pay & Quick Transfer

**SUMMERVILLE CREDIT UNION · CONSOLIDATED MEMBER GUIDE · DASHBOARD MODULE**

Module: nFinia Digital Banking > Dashboard > Quick Transfer Widget

*Sources: Summerville Reports Series A (36 docs) + Series B (25 docs) | Features: nFinia Documentation Features Spreadsheet*

## 01 PRODUCT SUMMARY

The Quick Transfer widget is a compact transfer form embedded directly on the post-login Dashboard. It allows members to move funds between their own accounts — checking to savings, savings to checking, or any internal account combination — without navigating away from the Dashboard to the full Move Money Hub.

Quick Pay extends the same concept to loan payments: a member can make a payment toward their loan account directly from the Dashboard by selecting the loan as the destination account in the Quick Transfer widget, entering an amount, and confirming.

The widget is designed for speed. The "From" and "To" dropdowns are pre-populated with all accounts under the member's active membership, the amount field accepts manual entry, and the Transfer button submits the transaction immediately. A confirmation screen shows the transfer details (from, to, amount, date) and a success message. The entire flow takes three taps or clicks.

This widget mirrors the functionality available in Move Money > Transfer to Own Account (CSUM-06), but without the navigation overhead. For transfers to other members, external accounts, or more complex payment types, the member must use the full Move Money Hub.

## At a Glance

| Attribute | Detail |
|---|---|
| Feature Name | Quick Transfer / Quick Pay (Dashboard Widget) |
| Module | Dashboard > Right Panel |
| User Roles | All authenticated members (Personal & Business) |
| Access Level | Post-login; visible on the Dashboard landing screen |
| Transfer Types | Own account to own account; own account to own loan |
| Key Actions | Select From account, Select To account, Enter amount, Confirm transfer |
| Limitations | Internal transfers only — no external, no other-member, no Zelle, no bill pay |
| Related Reports | CSUM-02 (Dashboard), CSUM-06 (Transfer to Own Account), CSUM-08 (Scheduled Transfers) |

## 02 KEY USE CASES

| Use Case | Who Uses It | What They Do | Business Value |
|---|---|---|---|
| Quick Savings Top-Up | Member with extra checking balance | Uses Quick Transfer to move funds from Checking to Savings without leaving Dashboard | Fastest possible internal transfer — three taps, no navigation |
| Cover a Shortfall | Member with low checking balance | Transfers from Savings to Checking to cover an upcoming debit | Prevents overdraft or NSF without opening Move Money |
| Quick Loan Payment | Member with a loan due date approaching | Selects Loan account as "To" destination, enters payment amount | On-the-spot loan payment from the Dashboard — no separate Bill Pay or Loan Payment flow |
| Morning Funds Shuffle | Member managing multiple accounts | Reviews balances on Dashboard tiles, immediately moves funds via widget | Balances and transfer tool on same screen — no context switching |
| One-Time Small Transfer | Member moving a small amount | Enters amount, confirms — done in seconds | Avoids the overhead of the full Move Money flow for simple transfers |

## 03 END-TO-END WORKFLOW

*Navigation: The Quick Transfer widget is on the Dashboard right panel. No navigation required — it is visible immediately after login.*

### Step 1 — Locate the Quick Transfer Widget

After logging in, the member sees the Quick Transfer widget on the right side of the Dashboard. The widget contains three fields: "From" (dropdown), "To" (dropdown), and "Amount" (text input), plus a "Transfer" button.

<figure><img src="/.gitbook/assets/img_eb0a7d21423c.png" alt="Dashboard with Quick Transfer widget visible on the right panel" width="480"><figcaption>Step 1: Quick Transfer widget on the Dashboard</figcaption></figure>

### Step 2 — Select the "From" Account

The member clicks the "From" dropdown. A list of all accounts under their membership appears — each showing the account name, masked account number, and current balance. The member selects the source account.

<figure><img src="/.gitbook/assets/img_cf945ff36b05.png" alt="Account selection dropdown showing available accounts with balances" width="340"><figcaption>Step 2: Select the From account</figcaption></figure>

### Step 3 — Select the "To" Account

The member clicks the "To" dropdown. The same account list appears (minus the already-selected "From" account). The member selects the destination account. For a **Quick Pay** loan payment, the member selects their loan account here.

### Step 4 — Enter the Transfer Amount

The member types the amount to transfer in the "Amount" field. The field accepts numeric input with decimal places (e.g., 150.00). No minimum or maximum is enforced in the widget itself — server-side validation applies transfer limits.

### Step 5 — Click Transfer

The member clicks the **Transfer** button. The system validates the input (sufficient balance, valid accounts, within transfer limits) and processes the transfer.

### Step 6 — Review Confirmation

A confirmation screen appears showing:
- From account name and masked number
- To account name and masked number
- Transfer amount
- Transfer date
- Confirmation number
- Success message

The member can navigate back to the Dashboard or initiate another transfer.

### Error Handling

| Error Condition | System Behaviour |
|---|---|
| Insufficient balance in "From" account | Error message displayed; transfer not processed |
| Same account selected for From and To | Validation prevents submission |
| Amount exceeds daily transfer limit | Error message with limit information displayed |
| Session timeout during transfer | Member redirected to login; transfer not processed |
| System unavailable | Generic error message with retry option |

## 04 RELATIONSHIP TO MOVE MONEY

The Quick Transfer widget is a **shortcut** — it provides a subset of the functionality available in the full Move Money module. Here is how they compare:

| Capability | Quick Transfer (Dashboard) | Move Money Hub |
|---|---|---|
| Transfer between own accounts | Yes | Yes |
| Loan payment (Quick Pay) | Yes | Yes |
| Transfer to other CU members | No | Yes (CSUM-09) |
| External ACH transfer | No | Yes (CSUM-10) |
| Wire transfer | No | Yes (CSUM-12) |
| Bill Pay | No | Yes (CSUM-15) |
| Zelle / P2P | No | Yes (CSUM-17) |
| Schedule future transfer | No | Yes (CSUM-08) |
| Recurring transfer setup | No | Yes (CSUM-08) |

For any transfer type beyond own-account or loan payment, the member should navigate to **Move Money** in the top navigation bar.

## 05 QUICK REFERENCE

| Task | How | Who Can Do It | Notes |
|---|---|---|---|
| Transfer between own accounts | Dashboard > Quick Transfer widget | All members | Immediate execution |
| Make a loan payment (Quick Pay) | Dashboard > Quick Transfer > select Loan as "To" | Members with loan accounts | Same widget, loan as destination |
| Schedule a future transfer | Move Money > Transfer to Own Account > Schedule | All members | Not available from Dashboard widget |
| Transfer to another member | Move Money > Transfer to Other Members | All members | Not available from Dashboard widget |

## Related Pages

- [Dashboard](README.md) — parent page and full Dashboard layout
- [Dashboard & Activities](Dashboard%20Activities.md) — full Dashboard walkthrough
- [Transfer to Own Account & Scheduled](../../transfers-and-payments/internal-and-own-account-transfers/Transfer%20Own%20Account%20Scheduled.md) — the full Move Money version
- [Loan Payments & Quick Pay](../../bill-pay-loans-and-cards/bill-pay-and-loans/Loan%20Payments%20Quick%20Pay.md) — comprehensive loan payment documentation
