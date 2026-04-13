---
description: >-
  CSUM-02 — The post-login landing screen layout and the Activities Since Last
  Login security audit log.
---

# Dashboard & Activities

**SUMMERVILLE CREDIT UNION · CONSOLIDATED MEMBER GUIDE · CSUM-02 of 30**

Module: nFinia Digital Banking > Dashboard

*Sources: Summerville Reports Series A (36 docs) + Series B (25 docs) | Features: nFinia Documentation Features Spreadsheet*

## 01 PRODUCT SUMMARY

The Dashboard — Banking Summary is the first screen the member encounters after completing multi-factor authentication. It is the command centre of the nFinia digital banking experience: a single, consolidated view presenting the member's complete financial picture — all account balances, recent transactions, pending items, and primary action shortcuts — without requiring navigation to individual account pages.

The Dashboard is organised into distinct zones. The **centre column** displays account summary tiles — one card per account (Checking, Savings, Loans, CDs, Lines of Credit) showing the account name, masked number, and current balance. Clicking any account tile navigates to the **Accounts** module (CSUM-03: Account Overview & Transaction History), where the member can view full transaction history, search transactions, and access account-level services.

The **right panel** contains three widgets stacked vertically: the **Quick Transfer** form (a compact way to move funds between own accounts without leaving the Dashboard), the **Upcoming Payments** section (showing scheduled payments with due dates and amounts), and the **Credit Score meter** (a visual gauge displaying the member's current score range). Below these, the **Related Links sidebar** provides one-click access to common self-service tasks like Change Password, Download E-Statements, and Manage Alerts.

The **footer** contains persistent quick links to Security Policy, Branch Appointments, Locations, Rates, and Text Banking.

The **Activities Since Last Login** feature (accessible via More > Recent Activities) presents a real-time audit log of all account events that occurred since the member's previous session, providing an instant security check and activity summary.

## At a Glance

| Attribute | Detail |
|---|---|
| Module | nFinia Dashboard (post-login landing screen) |
| Accounts Shown | All accounts under the active membership |
| Dashboard Zones | Account tiles (centre), Quick Transfer + Upcoming Payments + Credit Score + Related Links (right panel), Footer quick links |
| Quick Actions | Transfer, Pay, Deposit, Alerts, Move Money |
| Activities Log | Events since last login (More > Recent Activities) |
| Refresh | Pull-to-refresh or auto-refresh on session open |
| Related Reports | CSUM-01 (Login), CSUM-03 (Account Overview), CSUM-31 (Recent Activities) |

## 02 KEY USE CASES

| Use Case | Who Uses It | What They Do | Business Value |
|---|---|---|---|
| Morning Balance Check | Member starting their day | Open app, view Dashboard for all account balances | Single-screen financial overview without navigating to each account |
| Quick Transfer | Member moving funds between accounts | Use the Quick Transfer widget on the Dashboard to complete a transfer | Fastest path to internal transfer without full Move Money navigation |
| Post-Login Security Review | Security-conscious member | View Activities Since Last Login for unexpected events | Instant detection of unauthorized account activity |
| Navigate to Accounts | Member needing transaction detail | Click an account tile on the Dashboard | Direct path to Account Overview & Transaction History (CSUM-03) |
| Check Upcoming Payments | Member tracking bills | Review the Upcoming Payments widget on the right panel | At-a-glance view of scheduled payments without navigating to Move Money |
| Glance at Credit Score | Member monitoring credit health | View the Credit Score meter widget on the Dashboard | Quick score check without navigating to the full Credit Score feature |

## 03 STEP-BY-STEP GUIDE

*Navigation: The Dashboard is the landing screen immediately after successful login. No additional navigation is required.*

### Step 1 — Land on the Dashboard

After logging in, the member arrives at the Dashboard. The screen displays:

- **Top navigation bar** with links to Dashboard, Accounts, Move Money, More, and a search bar
- **Greeting banner** ("Good Morning, [Member Name]")
- **Account summary tiles** in the centre column showing all account balances
- **Quick Transfer widget** on the right panel
- **Upcoming Payments** section on the right panel
- **Credit Score meter** with the member's current score range
- **Related Links sidebar** with self-service shortcuts
- **Footer** with Security Policy, Branch Appointments, Locations, Rates, Text Banking

<figure><img src="/.gitbook/assets/img_eb0a7d21423c.png" alt="Dashboard landing screen showing account tiles, Quick Transfer widget, Upcoming Payments, Credit Score meter, and Related Links" width="480"><figcaption>Step 1: Dashboard landing screen after login</figcaption></figure>

### Step 2 — Click an Account Tile to Navigate to Accounts

Clicking any account tile on the Dashboard navigates to the **Accounts** module. The Account Overview page (CSUM-03) displays a full list of all account types with balances, and from there the member can drill into any individual account's transaction history.

> **Note:** Clicking an account tile does NOT expand details inline on the Dashboard — it navigates away to the Accounts feature.

<figure><img src="/.gitbook/assets/img_d627ced1170e.png" alt="Account Overview page showing full list of accounts after clicking a Dashboard tile" width="480"><figcaption>Step 2: Accounts feature — Account Overview reached from Dashboard</figcaption></figure>

### Step 3 — Use Quick Transfer from the Dashboard

The Quick Transfer widget allows the member to move funds between their own accounts without leaving the Dashboard. The member selects a "From" account, a "To" account, enters an amount, and clicks Transfer. A confirmation screen appears.

For a full walkthrough of Quick Transfer and Quick Pay, see [Quick Pay & Quick Transfer](Dashboard%20Quick%20Pay.md).

### Step 4 — Review Upcoming Payments

The Upcoming Payments widget on the right panel shows any scheduled or pending payments with their due dates and amounts. If no payments are scheduled, the widget displays "No upcoming payments."

For details, see [Upcoming Payments](Dashboard%20Upcoming%20Payments.md).

### Step 5 — Check Credit Score Widget

The Credit Score meter displays a colour-coded gauge (red → yellow → green) with the member's current score, score range labels (Poor, Fair, Good, Very Good, Excellent), and a "Read More" link that navigates to the full Credit Score feature.

For details, see [Credit Score Widget](Dashboard%20Credit%20Score%20Widget.md).

### Step 6 — Access Related Links

The Related Links sidebar provides one-click navigation to common tasks: Change Password, Download E-Statements, Manage Alerts, Direct Deposit Form, and more.

For details, see [Related Links](Dashboard%20Related%20Links.md).

### Step 7 — View Activities Since Last Login

To review activity since the last session, the member clicks **More** in the top navigation bar, then selects **Recent Activities**. The Activities log displays all events (transfers, payments, logins, alert triggers) in reverse chronological order with timestamps.

<figure><img src="/.gitbook/assets/img_4a4de4ca3296.png" alt="Recent Activities modal showing chronological list of account events since last login" width="480"><figcaption>Step 7: Activities Since Last Login</figcaption></figure>

### Step 8 — Log Off Securely

The member clicks the **Log Out** icon in the top navigation bar. A confirmation modal appears prompting the member to confirm they want to end their session. Clicking "Proceed" logs the member out and returns to the login screen.

<figure><img src="/.gitbook/assets/img_109f62839cb9.png" alt="Logout confirmation modal" width="340"><figcaption>Step 8: Log Off Securely</figcaption></figure>
