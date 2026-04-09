# CSUM-View-Multiple-Account-Recipient

**DIAMOND CREDIT UNION · BUSINESS BANKING GUIDE · View Multiple-Account Recipient**

**View Multiple-Account Recipient**

Module: nFinia Digital Banking > Business Banking > Transfer & Pay > Recipient Management

_Platform: Diamond Credit Union nFinia | Feature: Transfer Account Details | Workflow: View and Inspect a Multi-Account Recipient_

> **01 PRODUCT SUMMARY**

The View Multiple-Account Recipient workflow covers how a business admin locates an existing recipient, reviews all linked accounts from a single Transfer Account Details screen, and drills into individual Account Details modals to inspect full account records. This read path is the primary way admins confirm recipient data before initiating a payment, especially when a single payee holds accounts of different types or at different institution branches.

The Transfer Account Details screen surfaces every linked account in one consolidated view, each row showing the nickname, payment method, and financial institution alongside a dedicated “Provide Funds” action. The Account Details modal goes deeper, displaying the complete verified record — account holder name, account type, account number, ABA routing number, institution name and address — and surfaces a VERIFIED badge for any account that has passed ACH pre-notification validation.

For credit unions, this visibility layer is critical to payment accuracy and audit readiness. Admins can confirm the exact institution and routing details for each account before funds are moved, reducing the risk of misdirected payments and ACH returns. The VERIFIED status indicator gives operations staff confidence that an account has been validated against NACHA pre-note requirements before use in a live transaction.

**At a Glance**

| **Attribute**     | **Detail**                                                                      |
| ----------------- | ------------------------------------------------------------------------------- |
| Feature Name      | View Multiple-Account Recipient                                                 |
| Module            | Business Banking > Transfer & Pay > Recipient Management                        |
| User Roles        | Business Admin, Authorized Signer                                               |
| Key Screens       | Transfer Account Management, Transfer Account Details, Account Details modal    |
| Verification      | VERIFIED badge displayed for ACH pre-noted accounts                             |
| Account Details   | Nickname, account type, account number, ABA routing, institution name & address |
| Actions Available | Provide Funds, Edit Account, Remove Transfer Account                            |

> **02 STEP-BY-STEP GUIDE**
>
> _Navigation: Business Banking > Transfer & Pay > Recipient Management > [Select recipient] > [Select account row]._

**Step 1 — Transfer Account Management**

The admin navigates to Transfer Account Management via Transfer & Pay, which displays all saved recipients as a searchable grid. Each card shows the recipient name, account count, and associated membership — recipients with multiple linked accounts are visible at a glance by their account count. The admin clicks the target recipient to open their Transfer Account Details view.

<figure><img src="/.gitbook/assets/image1 (8).png" alt="" width="480"><figcaption></figcaption></figure>

_Step 1: Transfer Account Management — Select Recipient_

**Step 2 — Transfer Account Details: Two Accounts**

The Transfer Account Details screen for Jamie Smith (Dunder Mifflin, Inc.) displays both linked ACH accounts in a single view: “Jamie” and “James,” each showing its nickname, payment method, and financial institution. Every account row carries an independent “Provide Funds” button, allowing the admin to direct a payment to either account without modifying the recipient record or selecting from a separate list.

<figure><img src="/.gitbook/assets/image2 (8).png" alt="" width="480"><figcaption></figcaption></figure>

_Step 2: Transfer Account Details — Multiple Accounts_

**Step 3 — Account Details: James (Savings)**

Clicking the overflow menu on an account row opens the Account Details modal, surfacing the complete record for that account: account type, account holder name, ABA routing number, and the resolved financial institution name and address. This view lets the admin confirm the correct account is targeted before initiating a transfer — particularly important when a recipient has multiple accounts at the same institution.

<figure><img src="/.gitbook/assets/image3 (8).png" alt="" width="480"><figcaption></figcaption></figure>

_Step 3: Account Details Modal — James (Savings, ACH)_

**Step 4 — Account Details: Jamie (Checking, Verified)**

The Account Details modal for “Jamie” displays a VERIFIED status badge, confirming this account has passed ACH pre-notification validation — a NACHA best practice that sends a zero-dollar test entry before the first live credit or debit. The admin can review the full record — account holder Jamie Smith, account type Checking, account number, ABA routing number 063106145, and BANK OF AMERICA, N.A. at 620 South Tryon Street, Charlotte, NC — and edit or save directly from this modal.

<figure><img src="/.gitbook/assets/image4 (8).png" alt="" width="620"><figcaption></figcaption></figure>

_Step 4: Account Details Modal — Jamie (Checking, VERIFIED)_
