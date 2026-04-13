---
description: >-
  The Upcoming Payments widget on the Dashboard — a summary of scheduled and
  pending payments visible immediately after login.
---

# Upcoming Payments

**SUMMERVILLE CREDIT UNION · CONSOLIDATED MEMBER GUIDE · DASHBOARD MODULE**

Module: nFinia Digital Banking > Dashboard > Upcoming Payments Widget

*Sources: Summerville Reports Series A (36 docs) + Series B (25 docs) | Features: nFinia Documentation Features Spreadsheet*

## 01 PRODUCT SUMMARY

The Upcoming Payments widget is a read-only summary panel displayed on the right side of the Dashboard. It shows the member any payments that are scheduled, pending, or due in the near future — including bill payments, scheduled transfers, loan payments, and recurring payment obligations.

Each entry in the Upcoming Payments list displays the payee or destination name, the payment amount, and the scheduled date. If no payments are pending, the widget displays a "No upcoming payments" message.

The widget's purpose is situational awareness: the member can see at a glance what payments are coming up without navigating to Move Money > Scheduled Transfers or Bill Pay. It does not allow editing, cancelling, or creating payments — for those actions, the member must navigate to the relevant module.

Upcoming Payments pulls data from multiple sources within the nFinia platform: scheduled internal transfers (CSUM-08), bill pay scheduled payments (CSUM-15), loan payment schedules, and any recurring payment instructions the member has set up. The widget aggregates these into a single, chronologically ordered list.

## At a Glance

| Attribute | Detail |
|---|---|
| Feature Name | Upcoming Payments (Dashboard Widget) |
| Module | Dashboard > Right Panel |
| User Roles | All authenticated members (Personal & Business) |
| Access Level | Post-login; visible on the Dashboard landing screen |
| Data Sources | Scheduled Transfers, Bill Pay, Loan Payments, Recurring Instructions |
| Display Fields | Payee / Destination, Amount, Scheduled Date |
| Actions Available | View only — no edit, cancel, or create from this widget |
| Empty State | "No upcoming payments" message |
| Related Reports | CSUM-02 (Dashboard), CSUM-08 (Scheduled Transfers), CSUM-15 (Bill Pay) |

## 02 KEY USE CASES

| Use Case | Who Uses It | What They Do | Business Value |
|---|---|---|---|
| Payment Due Date Awareness | Any member with scheduled payments | Reviews the Upcoming Payments widget on login to see what's due | Prevents missed payments; reduces late fees and delinquency |
| Cash Flow Planning | Member managing tight budgets | Checks upcoming payment amounts against current account balances on the same screen | Balance tiles + upcoming payments on one screen enables real-time cash flow decisions |
| Bill Pay Verification | Member who just scheduled a bill payment | Confirms the newly scheduled payment appears in Upcoming Payments | Quick verification that the payment was scheduled correctly |
| Loan Payment Tracking | Member with active loans | Sees upcoming loan payment amount and date | Ensures loan payment coverage without navigating to loan account detail |
| Transfer Monitoring | Member with scheduled future transfers | Sees pending transfers in the upcoming list | Confirms scheduled transfers are queued as expected |

## 03 END-TO-END WORKFLOW

*Navigation: The Upcoming Payments widget is on the Dashboard right panel. No navigation required — it is visible immediately after login.*

### Step 1 — View Upcoming Payments on the Dashboard

After logging in, the member sees the Upcoming Payments widget on the right side of the Dashboard, positioned below or alongside the Quick Transfer widget. The widget header reads "Upcoming Payments."

If payments are scheduled, the widget displays a list of entries, each showing:
- **Payee / Destination name** (e.g., "Electric Company", "Savings Auto-Transfer", "Auto Loan Payment")
- **Amount** (e.g., $150.00)
- **Scheduled Date** (e.g., "Apr 18, 2026")

Entries are ordered chronologically — the soonest payment appears first.

### Step 2 — Empty State (No Upcoming Payments)

If the member has no scheduled payments, bill pay items, or recurring transfer instructions, the widget displays: **"No upcoming payments."**

This is the expected state for members who use only on-demand transfers or who have not set up any scheduled payment instructions.

<figure><img src="/.gitbook/assets/img_eb0a7d21423c.png" alt="Dashboard showing the Upcoming Payments section on the right panel" width="480"><figcaption>Dashboard with Upcoming Payments widget visible</figcaption></figure>

### Step 3 — Navigate to Manage Payments (If Needed)

The Upcoming Payments widget is view-only. To edit, cancel, or create payment instructions, the member navigates to the appropriate module:

| Action Needed | Where to Go |
|---|---|
| Edit or cancel a scheduled transfer | Move Money > Scheduled Transfers (CSUM-08) |
| Edit or cancel a bill payment | Move Money > Bill Pay (CSUM-15) |
| Set up a new recurring transfer | Move Money > Transfer to Own Account > Schedule |
| Make an ad-hoc loan payment | Dashboard > Quick Transfer (select loan as "To") or Move Money > Loan Payment |
| View all past and upcoming transfers | Move Money > Transaction History |

## 04 DATA SOURCES & AGGREGATION

The widget aggregates upcoming payment data from multiple nFinia subsystems:

| Source | Payment Type | Example |
|---|---|---|
| Scheduled Transfers (CSUM-08) | Future-dated own-account transfers | "Transfer to Savings — $200.00 — Apr 20" |
| Bill Pay (CSUM-15) | Scheduled bill payments to payees | "Electric Company — $95.50 — Apr 18" |
| Loan Payment Schedule | Recurring or next-due loan payments | "Auto Loan — $350.00 — May 1" |
| Recurring Instructions | Any auto-pay or recurring payment setup | "Monthly Savings — $100.00 — Apr 15" |

The widget refreshes automatically when the Dashboard loads and on pull-to-refresh. It shows payments within a configurable look-ahead window (typically 30 days, FI-configurable).

## 05 QUICK REFERENCE

| Task | How | Who Can Do It | Notes |
|---|---|---|---|
| View upcoming payments | Dashboard > Upcoming Payments widget (right panel) | All members | View-only; auto-populated |
| Edit a scheduled payment | Move Money > Scheduled Transfers | All members | Navigate away from Dashboard |
| Cancel a bill payment | Move Money > Bill Pay | All members | Navigate away from Dashboard |
| Set up a new payment | Move Money > relevant sub-module | All members | Cannot create from Dashboard widget |

## Related Pages

- [Dashboard](README.md) — parent page and full Dashboard layout
- [Dashboard & Activities](Dashboard%20Activities.md) — full Dashboard walkthrough
- [Scheduled Transfers](../../transfers-and-payments/internal-and-own-account-transfers/Scheduled%20Transfers.md) — managing future-dated transfers
- [Bill Pay](../../bill-pay-loans-and-cards/bill-pay-and-loans/Bill%20Pay.md) — managing bill payment instructions
- [Loan Payments & Quick Pay](../../bill-pay-loans-and-cards/bill-pay-and-loans/Loan%20Payments%20Quick%20Pay.md) — loan payment schedules
