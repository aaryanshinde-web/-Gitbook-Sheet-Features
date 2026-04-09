<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image7.png" alt="" width="480"><figcaption></figcaption></figure>

March 18th, 2026

Diamond Credit Union

*Business Banking User Manual*

#### 

###   

### Document Version Control

| **Document Name:**   | Diamond Credit Union - Business Banking User Manual |
| -------------------- | --------------------------------------------------- |
| **Document Status:** | Completed                                           |
| **Version Number:**  | 1.0                                                 |
| **Date:**            | 17.03.2026                                          |
| **Author:**          | Aaryan Shinde                                       |
| **Authorized By:**   | Prashant Karpe                                      |
| **Distribution:**    | Confidential                                        |

### Revision History

| **DATE**   | **REMARKS**   | **AUTHOR**    | **VERSION** |
| ---------- | ------------- | ------------- | ----------- |
| 17.03.2026 | Initial Draft | Aaryan Shinde | 1.0         |
|            |               |               |             |

### 

# Table of Contents

> [Document Version Control 2](#document-version-control)
> 
> [Revision History 2](#revision-history)

[**Table of Contents 3**](#table-of-contents)

[***Section 1: Transfers 6***](#section-1-transfers)

> [**1.1 Internal Transfers 6**](#internal-transfers)
> 
> [What are Internal Transfers? 6](#what-are-internal-transfers)
> 
> [Common Use Cases 6](#common-use-cases)
> 
> [Quick Reference 10](#quick-reference)
> 
> [**1.2 Other Diamond Members Transfer
> 11**](#other-diamond-members-transfer)
> 
> [What is Other Diamond Members Transfer?
> 11](#what-is-other-diamond-members-transfer)
> 
> [Common Use Cases 11](#common-use-cases-1)
> 
> [Quick Reference 15](#quick-reference-1)
> 
> [**1.3 ACH Transfer 15**](#ach-transfer)
> 
> [What are ACH Transfers? 16](#what-are-ach-transfers)
> 
> [Common Use Cases 17](#common-use-cases-2)
> 
> [Quick Reference 22](#quick-reference-2)
> 
> [**1.4 Domestic Wire Transfer 23**](#domestic-wire-transfer)
> 
> [What are Domestic Wire Transfers?
> 23](#what-are-domestic-wire-transfers)
> 
> [Quick Reference 27](#quick-reference-3)
> 
> [**1.5 Scheduled Transfers 28**](#scheduled-transfers)
> 
> [What are Scheduled Transfers? 28](#what-are-scheduled-transfers)
> 
> [Common Use Cases 29](#common-use-cases-3)
> 
> [Quick Reference 33](#quick-reference-4)
> 
> [What are Transfer Templates? 34](#what-are-transfer-templates)
> 
> [Workflow 1 — Create a Transfer Template
> 35](#workflow-1-create-a-transfer-template)

[***Section 2: Account Management 41***](#section-2-account-management)

> [**2.1 Transfer Accounts 41**](#transfer-accounts)
> 
> [What are Transfer Accounts? 41](#what-are-transfer-accounts)
> 
> [Common Use Cases 42](#common-use-cases-4)
> 
> [**2.2 Recipient Management 46**](#recipient-management)
> 
> [What is Recipient Management? 46](#what-is-recipient-management)
> 
> [Common Use Cases 46](#common-use-cases-5)
> 
> [Quick Reference 50](#quick-reference-5)

[***Section 3: Administration 51***](#section-3-administration)

> [**3.1 User Management 51**](#user-management)
> 
> [What is User Management? 51](#what-is-user-management)
> 
> [Common Use Cases 51](#common-use-cases-6)
> 
> [Quick Reference 58](#quick-reference-6)
> 
> [**3.2 Role Management 59**](#role-management)
> 
> [What is Role Management? 59](#what-is-role-management)
> 
> [Common Use Cases 59](#common-use-cases-7)
> 
> [Quick Reference 63](#quick-reference-7)
> 
> [**3.3 Approval Requests 64**](#approval-requests)
> 
> [What are Approval Requests? 64](#what-are-approval-requests)
> 
> [Common Use Cases 64](#common-use-cases-8)
> 
> [Quick Reference 68](#)
> 
> [3.4 Banking Services & Permissions 69](#)
> 
> [What is Banking Services? 69](#)
> 
> [Common Use Cases 70](#)
> 
> [Quick Reference 71](#)
> 
> [3.5 Business Alerts 72](#business-alerts)
> 
> [What Are Business Alerts? 72](#)
> 
> [Available Alert Categories 72](#)
> 
> [Common Use Cases 73](#)

[Section 4: Reporting 77](#)

> [4.1 Reports 77](#)
> 
> [What is in the Reports Section? 77](#)
> 
> [Common Use Cases 78](#)
> 
> [Quick Reference 83](#)
> 
> [4.2 Commercial activity 84](#commercial-activity)
> 
> [What is Commercial Activity? 84](#)
> 
> [Transaction Status Reference 84](#)
> 
> [Common Use Cases 85](#)

**Foreword**

This guide consolidates every feature of the Diamond Credit Union nFinia
Business Banking platform into a single, authoritative reference.
Whether you are onboarding a new business member, configuring roles and
permissions, executing a same-day wire transfer, or building a recurring
payroll template — everything you need is here, in order, with
step-by-step screenshots.

The platform is organized into four capability areas:

  - > **Transfers** (the payment tools your team uses every day),

  - > **Account Management** (the payee and account registry that powers
    > those transfers),

  - > **Administration** (the governance layer that controls who can do
    > what), and

  - > **Reporting** (the analytics and audit tools that close the loop
    > on every transaction).

> *"Business banking is not a consumer feature with a higher limit. It
> is a fundamentally different operating environment — one where cash
> visibility, payment controls, and multi-user governance are not
> nice-to-haves, they are existential requirements."*

Each section of this guide follows a consistent structure:

  - > a product overview explaining what the feature does and why it
    > matters,

  - > a Common Use Cases table mapping the feature to real business
    > scenarios,

  - > illustrated step-by-step instructions, and

  - > a Quick Reference table for experienced users.

# Section 1: Transfers

## 1.1 Internal Transfers

Internal Transfers are real-time, fee-free fund movements between
accounts within the same Diamond Credit Union membership. No routing
numbers or external network is required — funds settle immediately.

### What are Internal Transfers?

| **Characteristic** | **Detail**                                      |
| ------------------ | ----------------------------------------------- |
| Settlement speed   | Immediate (real-time)                           |
| Processing fee     | None — free for all within-membership transfers |
| Coverage           | Same FI / same membership only                  |
| Navigation path    | Transfer & Pay → My Diamond Accounts            |

### Common Use Cases

| **Use Case**        | **Description**                                                           |
| ------------------- | ------------------------------------------------------------------------- |
| Cash positioning    | Moving funds between operating, payroll, tax, and reserve accounts daily. |
| Payroll funding     | Transferring funds into a dedicated payroll account before an ACH run.    |
| Expense segregation | Allocating budgets across separate accounts for departments or projects.  |
| Pre-wire staging    | Moving funds internally before initiating a wire or ACH batch.            |

**Step 1 — Open Transfer & Pay**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image19.png" alt="" width="340"><figcaption></figcaption></figure>

Click **Transfer & Pay** in the top nav → click **My Diamond Accounts**.

**Step 2 — Select Source and Destination Accounts**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image16.png" alt="" width="480"><figcaption></figcaption></figure>

The From field pre-populates. Click the **To** dropdown and select the
destination account.

**Step 3 — Enter Amount and Confirm**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image31.png" alt="" width="480"><figcaption></figcaption></figure>

Enter the dollar amount. Click **Continue** → verify the summary → click
**Confirm Transfer**. Transfer completes immediately.

### Quick Reference

| **Step** | **Where**          | **What to do**                                                  |
| -------- | ------------------ | --------------------------------------------------------------- |
| 1        | Transfer & Pay hub | Click Transfer & Pay → My Diamond Accounts                      |
| 2        | Select accounts    | Choose From and To accounts from your Diamond membership        |
| 3        | Confirm            | Enter amount → Continue → Confirm Transfer → instant settlement |

## 1.2 Other Diamond Members Transfer

Other Diamond Members Transfer enables instant, fee-free fund movement
to another Diamond Credit Union account holder. Transfers are processed
immediately with no processing fees.

### What is Other Diamond Members Transfer?

| **Characteristic** | **Detail**                                                        |
| ------------------ | ----------------------------------------------------------------- |
| Settlement speed   | Instant — funds arrive immediately upon confirmation              |
| Processing fee     | None — free for all Diamond-to-Diamond transfers                  |
| Eligibility        | Both sender and recipient must hold Diamond Credit Union accounts |
| Navigation path    | Transfer & Pay → Other Diamond Members                            |

### Common Use Cases

| **Use Case**                  | **Description**                                                                 |
| ----------------------------- | ------------------------------------------------------------------------------- |
| Business-to-business payments | Paying a partner or supplier that also banks with Diamond CU — instant, no fee. |
| Payroll advances              | Issuing a same-day advance to an employee with a Diamond CU account.            |
| Reimbursements                | Instantly reimbursing a colleague with an optional memo for reference.          |
| Shared expense splits         | Splitting costs with a team member who holds a Diamond account.                 |

**Step 1 — Open Transfer & Pay → Other Diamond Members**<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image30.png" alt="" width="340"><figcaption></figcaption></figure>

Click **Transfer & Pay** → **Other Diamond Members**. The form loads
with your default source account.

**Step 2 — Select Recipient**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image20.png" alt="" width="480"><figcaption></figcaption></figure>

Click **Select a Transfer Account** dropdown and choose the destination
Diamond member account.

**Step 3 — Enter Amount, Add Memo, and Confirm**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image24.png" alt="" width="480"><figcaption></figcaption></figure>

Enter the amount. Add an optional **Transaction memo**. Click
**Continue** → review → **Confirm Transfer**.

### Quick Reference

| **Step** | **Where**          | **What to do**                                             |
| -------- | ------------------ | ---------------------------------------------------------- |
| 1        | Transfer & Pay hub | Click Transfer & Pay → Other Diamond Members               |
| 2        | Select recipient   | Click Select a Transfer Account → choose member account    |
| 3        | Confirm            | Enter amount → optional memo → Continue → Confirm Transfer |

##   
1.3 ACH Transfer

ACH Transfer allows authorized users to send or receive funds via the
ACH Network. Transfers are processed in scheduled cycles and typically
settle within one to two business days.

### What are ACH Transfers?

An ACH transfer is an electronic bank-to-bank movement of funds through
the Nacha-operated ACH Network. ACH supports Credits (push money out)
and Debits (pull money in).

| **Characteristic** | **Detail**                                                     |
| ------------------ | -------------------------------------------------------------- |
| Settlement speed   | Same-day ACH or 1–2 business days depending on submission time |
| Processing fee     | No additional fee beyond standard account charges              |
| Directions         | Send Money (Credit) or Receive Money (Debit)                   |
| Entry classes      | CCD, PPD, CTX and others                                       |
| Navigation path    | Business Banking → Transfers → ACH Transfer                    |

### Common Use Cases

| **Use Case**         | **Description**                                                                    |
| -------------------- | ---------------------------------------------------------------------------------- |
| Payroll disbursement | Paying employees by direct deposit via ACH Credit — the most common ACH use case.  |
| Vendor payments      | Settling recurring invoices with contractors through scheduled ACH Credits.        |
| Collections          | Pulling payments from customer accounts via ACH Debit for subscriptions or dues.   |
| Tax payments         | Remitting federal, state, or local tax obligations electronically.                 |
| Cash concentration   | Consolidating balances from multiple branch accounts into a single master account. |

**Step 1 — Log In and Navigate to Business Banking**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image18.png" alt="" width="480"><figcaption></figcaption></figure>

Log in → complete MFA → click **Business Banking** in the top nav →
click **ACH Transfer** under Transfers.

**Step 2 — Choose Transfer Direction and Select Accounts**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image54.png" alt="" width="480"><figcaption></figcaption></figure>

Select **Send Money** or **Receive Money**. Choose your source account
(From) and select a saved external recipient (To).

**Step 3 — Enter Amount, Account Type, and Description**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image40.png" alt="" width="340"><figcaption></figcaption></figure>

Enter the dollar amount, select the **Type of Account receiving funds**,
and choose a **Company entry description** (e.g. Payroll, Tax, CCD).

**Step 4 — Confirm Transfer**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image53.png" alt="" width="480"><figcaption></figcaption></figure>

Click on Confirm Transfer and Verify payment via OTP

### Quick Reference

| **Step** | **Where**            | **What to do**                                                |
| -------- | -------------------- | ------------------------------------------------------------- |
| 1        | Business Banking hub | Click Business Banking → ACH Transfer under Transfers         |
| 2        | Set up Transfer      | Choose Send or Receive Money → select From and To accounts    |
| 3        | Amount & Details     | Enter amount → select account type → select entry description |
| 4        | Transfer Date        | Choose date → note cut-off → Continue → Review → Submit       |

## 1.4 Domestic Wire Transfer

Domestic Wire Transfer enables same-day, irrevocable fund movement to
external U.S. bank accounts via Fedwire. A $20.00 processing fee
applies, and all wires require approver authorization before funds are
released.

### What are Domestic Wire Transfers?

A domestic wire is an individual, near-real-time electronic payment
between U.S. financial institutions. Once processed, funds are
irrevocable. All wires require a designated approver to authorize before
processing begins.

| **Characteristic** | **Detail**                                                       |
| ------------------ | ---------------------------------------------------------------- |
| Settlement speed   | Same business day (if approved and submitted before cut-off)     |
| Reversibility      | Irrevocable once processed — cannot be recalled unilaterally     |
| Approval required  | Yes — a designated approver must authorize before funds are sent |
| Processing fee     | $20.00 per transfer                                              |
| Network            | Fedwire (Federal Reserve real-time gross settlement)             |
| Navigation path    | Business Banking → Transfers → Domestic Wire Transfer            |

**Common Use Cases**

| **Use Case**          | **Description**                                                                   |
| --------------------- | --------------------------------------------------------------------------------- |
| Real estate closings  | Transferring closing cost funds directly to a title company on settlement day.    |
| Large vendor payments | Paying suppliers for high-value invoices where same-day delivery is required.     |
| Business acquisitions | Funding mergers or asset purchases where irrevocable settlement is critical.      |
| Tax remittances       | Sending large tax deposits to government agencies that require wire transfer.     |
| Loan payoffs          | Paying off commercial loans where same-day payment is required to release a lien. |

**Step 1 — Log In and Navigate to Business Banking**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image43.png" alt="" width="620"><figcaption></figcaption></figure>

Log in → click **Business Banking** → click **Domestic Wire Transfer**
under Transfers.

**Step 2 — Select Source and Destination Accounts**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image25.png" alt="" width="620"><figcaption></figcaption></figure>

Select source account (From) and click **Select a Transfer Account**
(To) to choose or add a wire payee.

**Step 3 — Enter Date**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image22.png" alt="" width="620"><figcaption></figcaption></figure>

Enter the amount. Note the **$20.00 processing fee** notice. Set
transfer date. Enter a **Requester Memo** and click **Continue**.

**Step 4 — Review and Submit for Approval**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image44.png" alt="" width="620"><figcaption></figcaption></figure>

Review all details. Click **Confirm Transfer** to submit for approval.
The wire is **not** sent until the approver authorizes.

### Quick Reference

| **Step** | **Where**            | **What to do**                                                 |
| -------- | -------------------- | -------------------------------------------------------------- |
| 1        | Business Banking hub | Business Banking → Domestic Wire Transfer                      |
| 2        | Set up Transfer      | Select source (From) → select or add destination (To)          |
| 3        | Amount & Memo        | Enter amount → note $20 fee → set date → enter Requester Memo  |
| 4        | Review & Confirm     | Review details → Confirm Transfer → approval request submitted |

## 1.5 Scheduled Transfers

Scheduled Transfers allows fund movements to execute automatically on a
future date or recurring cycle. Supports ACH, wire, internal,
template-based, and file upload transfers.

### What are Scheduled Transfers?

| **Characteristic** | **Detail**                                                                                     |
| ------------------ | ---------------------------------------------------------------------------------------------- |
| Execution          | Automated — runs without manual intervention on the configured date                            |
| Frequency options  | One-time, Daily, Weekly, Monthly, or custom interval                                           |
| Transfer types     | External ACH, Internal, Template-based, File Upload                                            |
| Navigation path    | Business Banking → More Options → Scheduled Transfers, or Transfer & Pay → Scheduled Transfers |

### Common Use Cases

| **Use Case**              | **Description**                                                               |
| ------------------------- | ----------------------------------------------------------------------------- |
| Recurring vendor payments | Monthly ACH Credits to pay suppliers automatically without manual initiation. |
| Payroll funding           | Scheduling transfers to a payroll account ahead of each payroll run.          |
| Loan repayments           | Automatically repaying business loans or leases on due dates.                 |
| Tax instalment payments   | Pre-scheduling tax payments to exact due dates set by tax authorities.        |
| Cash concentration        | Sweeping surplus funds into a master account on a recurring schedule.         |

**Step 1 — Navigate to Scheduled Transfers**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image38.png" alt="" width="620"><figcaption></figcaption></figure>

Click **Business Banking** → **More Options** → **Scheduled Transfers**,
or click **Transfer & Pay** → **Scheduled Transfers**.

**Step 2 — View and Filter Existing Schedules**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image46.png" alt="" width="620"><figcaption></figcaption></figure>

The page lists all active schedules. Filter by **Scheduled Transfer
Type**, **Membership**, and **View type** (Fund Transfer / Template /
File Upload).

**Step 3 — Create a New Scheduled Transfer**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image52.png" alt="" width="480"><figcaption></figcaption></figure>

Click **+ Schedule a new transfer** to launch the ACH or Wire flow with
recurring scheduling enabled. Set date, frequency, and confirm.

### Quick Reference

| **Step** | **Where**      | **What to do**                                                 |
| -------- | -------------- | -------------------------------------------------------------- |
| 1        | Navigation     | Business Banking → More Options → Scheduled Transfers          |
| 2        | View schedules | Filter by type, membership, view type → click card for details |
| 3        | New schedule   | Click + Schedule a new transfer → configure and confirm        |

> **1.6 Transfer Templates**

Transfer Templates let you save recipient details, account numbers, and
payment types once and reuse them for every payroll run or recurring
vendor payment. Two workflows: Create and Run.

### What are Transfer Templates?

| **Characteristic** | **Detail**                                                         |
| ------------------ | ------------------------------------------------------------------ |
| Payment types      | ACH Payments, ACH Collections, ACH Payroll, Domestic Wire Transfer |
| Key actions        | Create, Run, Duplicate, Edit, Remove templates                     |
| Cut-off time       | Submit by 4:00 PM EST for same-day processing                      |
| Navigation path    | Business Banking → Transfers → Transfer Template                   |

### Workflow 1 — Create a Transfer Template

**Step 1 — Open Transfer Templates and Create New**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image28.png" alt="" width="340"><figcaption></figcaption></figure>

Navigate to **Business Banking** → **Transfer Template** → click **+
Create a new template**.

**Step 2 — Configure Template Details**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image23.png" alt="" width="480"><figcaption></figcaption></figure>

Enter a **Template name**, select **Type of payment**, **Debit
account**, and **Company entry description**.

**Step 3 — Add Recipients and Save**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image50.png" alt="" width="480"><figcaption></figcaption></figure>

Add recipients in the **Payor/Payee Details** section. Set amounts.
Click **Save template** or **Save and run**.

**Workflow 2 — Run a Transfer Template**

**Step 1 — Open the Template Menu**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image29.png" alt="" width="340"><figcaption></figcaption></figure>

Find the template in the list. Click the **⋯ three-dot menu** → select
**Run**.

**Step 2 — Review, Update Amounts, and Run**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image26.png" alt="" width="480"><figcaption></figcaption></figure>

All saved details are pre-filled. Adjust any **Amount** field for this
run only. Set a **Transfer Date** → click **Run template**.

**Quick Reference — Create**

| **Step** | **Where**        | **What to do**                                               |
| -------- | ---------------- | ------------------------------------------------------------ |
| 1        | Business Banking | Transfer Template → + Create a new template                  |
| 2        | Configure        | Enter name → select payment type → choose debit account      |
| 3        | Recipients       | Add recipients → set amounts → Save template or Save and run |

**Quick Reference — Run**

| **Step** | **Where**     | **What to do**                                          |
| -------- | ------------- | ------------------------------------------------------- |
| 1        | Template list | Find template → click ⋯ menu → Run                      |
| 2        | Review form   | Review pre-populated details → adjust amounts if needed |
| 3        | Submit        | Set transfer date → Run template → confirmation appears |

# Section 2: Account Management

## 2.1 Transfer Accounts

Transfer Accounts is the payee management module where admins register,
verify, and maintain all external and within-CU accounts the business
sends funds to.

### What are Transfer Accounts?

| **Characteristic** | **Detail**                                                                    |
| ------------------ | ----------------------------------------------------------------------------- |
| Account types      | Within CU (Diamond Credit Union) and External (other financial institutions)  |
| Verification       | Automatic (via FI login) or manual entry; VERIFIED badge shown when confirmed |
| Key actions        | Add, view, edit, transfer funds, pull from external account                   |
| Navigation path    | Business Banking → Manage → Transfer Accounts                                 |

### Common Use Cases

| **Use Case**            | **Description**                                                                     |
| ----------------------- | ----------------------------------------------------------------------------------- |
| Adding a vendor account | Registering an external supplier account so payments need no re-entry each time.    |
| Payroll destinations    | Adding employee accounts as verified payees before running payroll templates.       |
| Enabling inbound pulls  | Checking "Pull money from this external account" for collections or reimbursements. |
| Auditing payee details  | Reviewing VERIFIED status, masked account number, and ABA routing for compliance.   |

**Step 1 — Open Transfer Accounts**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image27.png" alt="" width="620"><figcaption></figcaption></figure>

Navigate to **Business Banking** → **Manage** → **Transfer Accounts**.

**Step 2 — View Existing Payees**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image33.png" alt="" width="620"><figcaption></figcaption></figure>

The **Transfer Account Management** page lists all saved payees. Click
**+ Add a new transfer account** to create one.

**Step 3 — View Account Details**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image35.png" alt="" width="620"><figcaption></figcaption></figure>

Click any payee card → use **Transfer Funds** or **⋮ menu** → **More
details** for full account info.

**Step 4 — Add Account Details and Save**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image32.png" alt="" width="620"><figcaption></figcaption></figure>

Click **+ Add a new transfer account** → enter Accountholder's name →
click **+ Add Account** → choose **Payment type** (Within CU or
External) → enter details → **Save Account**.

**Quick Reference**

| **Step** | **Where**   | **What to do**                                             |
| -------- | ----------- | ---------------------------------------------------------- |
| 1        | Navigation  | Business Banking → Manage → Transfer Accounts              |
| 2        | View payees | See all saved payees → click card for details              |
| 3        | Add account | \+ Add a new transfer account → enter name → + Add Account |
| 4        | Save        | Select payment type → enter account details → Save Account |

## 2.2 Recipient Management

Recipient Management is the external payee directory. Pre-registering
recipients means you never re-enter sensitive banking details — saved
recipients are available across all ACH and Wire transfer flows.

### What is Recipient Management?

| **Characteristic** | **Detail**                                                                                |
| ------------------ | ----------------------------------------------------------------------------------------- |
| Payment methods    | ACH and Domestic Wire Transfer                                                            |
| Details stored     | Account holder name, account number, account type, ABA routing, nickname, mailing address |
| Multiple accounts  | A single recipient can hold more than one bank account profile                            |
| Navigation path    | Business Banking → Manage → Recipient Management                                          |

### Common Use Cases

| **Use Case**           | **Description**                                                                   |
| ---------------------- | --------------------------------------------------------------------------------- |
| Payroll direct deposit | Store each employee's bank details once, select them at every payroll cycle.      |
| Vendor payments        | Maintain a directory of suppliers to quickly dispatch recurring invoice payments. |
| Tax remittances        | Save banking details of tax authorities to streamline scheduled payments.         |
| New vendor onboarding  | Set up new payees in advance and verify routing details before first payment.     |

**Step 1 — Navigate to Recipient Management**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image34.png" alt="" width="620"><figcaption></figcaption></figure>

Click **Business Banking** → **Manage** → **Recipient Management**.

**Step 2 — Add a New Recipient**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image45.png" alt="" width="620"><figcaption></figcaption></figure>

Click **+ Add a new transfer account**. Enter the **Accountholder's
name**, then click **+ Add Account**.

**Step 3 — Enter Banking Details and Save**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image42.png" alt="" width="620"><figcaption></figcaption></figure>

In the **Add Account** modal, enter: Payment type, Account holder's
name, Account number, Account type, **ABA routing number** (or use
**Search for a Financial Institution**), and optional Nickname. Enter
address. Click **Save Account** → **Save Transfer Account**.

### Quick Reference

| **Step** | **Where**       | **What to do**                                                     |
| -------- | --------------- | ------------------------------------------------------------------ |
| 1        | Navigation      | Business Banking → Manage → Recipient Management                   |
| 2        | Add recipient   | Enter Accountholder's name → click + Add Account                   |
| 3        | Banking details | Select payment type → enter account details, ABA routing, nickname |
| 4        | Save            | Enter address → Save Account → Save Transfer Account               |

# Section 3: Administration

## 3.1 User Management

User Management is the centralized admin console for controlling who can
access the business account, reviewing roles and permissions, managing
pending signers, invitations, and resolving locked or deactivated
accounts.

### What is User Management?

| **Characteristic** | **Detail**                                                                |
| ------------------ | ------------------------------------------------------------------------- |
| User views         | Active, Invited, New Authorized Signers, Locked, Deactivated              |
| Admin actions      | Edit user, Deactivate, Reactivate, Unlock account, Resend / Cancel invite |
| Navigation path    | Business Banking → Manage → User Management                               |

### Common Use Cases

| **Use Case**               | **Description**                                                               |
| -------------------------- | ----------------------------------------------------------------------------- |
| Onboarding new staff       | Sending invitations, assigning roles, and tracking enrollment completion.     |
| Offboarding employees      | Deactivating former employees to remove account access promptly.              |
| Account lockout resolution | Unlocking accounts for users locked out after too many failed login attempts. |
| Permission audits          | Reviewing each user's role and account access for compliance purposes.        |

**Step 1 — Navigate to User Management**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image47.png" alt="" width="340"><figcaption></figcaption></figure>

Log in → **Business Banking** → **Manage** → **User Management**.

**Step 2 — Review Active Users**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image37.png" alt="" width="480"><figcaption></figcaption></figure>

The **Active users** tab loads by default, listing all users grouped by
role. Click any user card for full details.

**Step 3 — Manage Individual Users**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image39.png" alt="" width="480"><figcaption></figcaption></figure>

The User Information page shows email, phone, user ID, role, and account
access. Use **Edit user** or **Deactivate user** as needed.

**Step 4 — Use the Other Tabs**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image21.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image51.png" alt="" width="480"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image10.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image41.png" alt="" width="620"><figcaption></figcaption></figure>

Use the **New Authorized Signers**, **Invited Users**, **Locked Users**,
and **Deactivated Users** tabs to manage the full user lifecycle.

### Quick Reference

| **Step** | **Where**         | **What to do**                                                   |
| -------- | ----------------- | ---------------------------------------------------------------- |
| 1        | Navigation        | Business Banking → Manage → User Management                      |
| 2        | Active users      | Review users grouped by role → click card for details            |
| 3        | Edit / Deactivate | Edit user details or deactivate access from the user detail page |
| 4        | Other tabs        | Use Invited, Locked, and Deactivated tabs for full lifecycle     |

## 3.2 Role Management

Role Management lets Business Admins create and configure user roles.
Each role defines what features sub-users can access, what transaction
limits apply, and whether the role is enabled.

### What is Role Management?

| **Characteristic**    | **Detail**                                                                          |
| --------------------- | ----------------------------------------------------------------------------------- |
| Role components       | Permissions (feature access), Limits (transaction caps), Users (assigned), Settings |
| Permission categories | Account Information, Alerts, Approvals, Banking Services, Reports, Settings         |
| Navigation path       | Business Banking → Manage → Role Management                                         |

### Common Use Cases

| **Use Case**          | **Description**                                                             |
| --------------------- | --------------------------------------------------------------------------- |
| View-only role        | Read access only — ideal for bookkeepers or auditors.                       |
| Payroll operator role | Allows ACH payroll but not wire transfers.                                  |
| Transaction limits    | Per-activity spending caps so sub-users cannot exceed approved thresholds.  |
| Temporarily disabling | Toggle Enabled off without deleting the role during organisational changes. |

**Step 1 — Open Role Management**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image48.png" alt="" width="620"><figcaption></figcaption></figure>

Navigate to **Business Banking** → **Manage** → **Role Management**.

**Step 2 — View Roles and Configure Permissions**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image1.png" alt="" width="620"><figcaption></figcaption></figure>

Each role card shows **Permissions**, **Limits**, **Users**, and
**Settings** tabs. Click **Permissions** and toggle the **Access
Status** for each feature category.

**Step 3 — Set Limits**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image6.png" alt="" width="480"><figcaption></figcaption></figure>

Click **Limits** to set per-activity transaction caps.

**Step 4 — Set Limits and Settings**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image5.png" alt="" width="620"><figcaption></figcaption></figure>

Click **Settings** to edit role name, description, and toggle
**Enabled**. Click **Save changes**.

### Quick Reference

| **Step** | **Where**         | **What to do**                                                 |
| -------- | ----------------- | -------------------------------------------------------------- |
| 1        | Navigation        | Business Banking → Manage → Role Management                    |
| 2        | View roles        | See all roles → + Add a new role to create one                 |
| 3        | Permissions       | Click Permissions tab → toggle Access Status for each feature  |
| 4        | Limits & Settings | Set transaction limits → configure name, enabled status → Save |

## 3.3 Approval Requests

Approval Requests enforces maker-checker control. Certain transactions —
domestic wires, ACH batches — must be reviewed and approved before
processing. The module provides a full audit trail across five status
tabs.

### What are Approval Requests?

| **Characteristic** | **Detail**                                                                                       |
| ------------------ | ------------------------------------------------------------------------------------------------ |
| Request types      | ACH transfers, Domestic wire transfers, External payments, and other approval-gated transactions |
| Status tabs        | Pending, Approved, Declined, Expired, Cancelled                                                  |
| Key actions        | Expand request, View transfers, Approve, Decline, Cancel request                                 |
| Navigation path    | Business Banking → More Options → Approvals                                                      |

### Common Use Cases

| **Use Case**                  | **Description**                                                                            |
| ----------------------------- | ------------------------------------------------------------------------------------------ |
| Authorizing a wire            | Reviewing and approving a domestic wire before funds are released.                         |
| Approving ACH batch           | Confirming payroll amounts and recipients are correct before processing.                   |
| Declining suspicious requests | Rejecting a transfer that appears incorrect, with the declination recorded for compliance. |
| Compliance and audit review   | Using Approved and Declined tabs to produce a full authorization audit trail.              |

**Step 1 — Navigate to Approvals**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image11.png" alt="" width="480"><figcaption></figcaption></figure>

Click **Business Banking** → **More Options** → **Approvals**.

**Step 2 — View and Act on Pending Requests**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image3.png" alt="" width="340"><figcaption></figcaption></figure>

The **Pending requests** tab opens by default. Click **chevron (›)** to
expand a request, view transfers, then **Approve**, **Decline**, or
**Cancel request**.

**Step 3 — Review Status Tabs**

Use **Approved**, **Declined**, **Expired**, and **Cancelled** tabs for
full lifecycle visibility and compliance audit trail.

### Quick Reference

| **Step** | **Where**      | **What to do**                                                       |
| -------- | -------------- | -------------------------------------------------------------------- |
| 1        | Navigation     | Business Banking → More Options → Approvals                          |
| 2        | Pending tab    | View pending requests → click chevron to expand                      |
| 3        | Act on request | View transfers → Approve / Decline / Cancel as appropriate           |
| 4        | Audit tabs     | Use Approved, Declined, Expired, Cancelled tabs for full audit trail |

## 3.4 Banking Services & Permissions

Banking Services Permission Management enables role-based access control
for core commercial services — ACH, Wire, Positive Pay, Remote Deposit
Capture, Check Reorder, and Check Stop Payment — through the Role
Management console.

### What is Banking Services?

Banking Services is the permission layer within Role Management. A
top-level category toggle must be activated before individual
sub-features can be configured. Once granted, users in that role gain
access to the corresponding tools in the Business Banking Hub and More
menu.

| **Service**            | **Description**                                                    |
| ---------------------- | ------------------------------------------------------------------ |
| Positive Pay           | Review and approve or reject exception items for fraud prevention. |
| Remote Deposit Capture | Deposit checks remotely using the Business Banking portal.         |
| Check Reorder          | Reorder business checks directly from the More menu.               |
| Check Stop Payment     | Issue stop payment orders on business checks. $25.00 fee applies.  |

### Common Use Cases

| **Use Case**                          | **Description**                                                                                                                |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Enabling Positive Pay                 | Activate Positive Pay for the treasury team role to review exception items.                                                    |
| Capturing deposit payments via checks | Deposit multiple checks in one go by clicking pictures of multiple checks. Use a high-speed document scanner to deposit checks |
| Reorder checks                        | Order check leaves by allowing only sub-users with the right authorization to access this utility                              |
| Emergency stop payment                | Authorized users issue a stop payment immediately; $25.00 fee disclosed at point of action.                                    |

**Step 1 — Access Business Services**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image4.png" alt="" width="620"><figcaption></figcaption></figure>

Access features that appear in the **More** menu

### Quick Reference

| **Step** | **Where** | **What to do**                                                   |
| -------- | --------- | ---------------------------------------------------------------- |
| 1        | Verify    | Access appropriate business banking service under the More menu. |

## 3.5 Business Alerts

### What Are Business Alerts?

Business Alerts is the notification management feature within Diamond
Credit Union's nFinia Business Banking portal. It allows Business Admins
and authorised users to configure real-time alerts for business account
activity — covering wire transfers, ACH transactions, fund transfers,
and security events. Alerts are delivered to the user's registered
contact channels and can be individually toggled on or off at any time.

| **Characteristic**        | **Detail**                                                                                  |
| ------------------------- | ------------------------------------------------------------------------------------------- |
| **Access location**       | More \> Business Alerts (from top navigation)                                               |
| **Navigation path (alt)** | Business Banking \> More Options \> Business Alerts                                         |
| **Alert categories**      | Security & Account, Wire Alerts, ACH Alerts, Transfer Alerts                                |
| **Tabs available**        | Alert preferences, General alerts, Account-specific alerts, Business Alerts, Do-Not-Disturb |
| **Toggle granularity**    | Enable/disable all alerts in a category, or control each alert individually                 |
| **Target business**       | Scoped to the selected business membership (e.g. \#0000978866 – Dunder Mifflin, Inc.)       |
| **Current enabled count** | 10 of 18 configured alerts enabled (example shown)                                          |

### **Available Alert Categories**

The Business Alerts tab organises all notifications into four
categories. Each category has a master toggle to enable or disable all
alerts within it, plus individual sub-alert controls when expanded.

| **Alert Category**            | **What It Covers**                                                                                                                      |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Security & Account Alerts** | Transfer security and account-level events such as login anomalies or permission changes.                                               |
| **Wire Alerts**               | All domestic wire transfer notifications including approval needed, transmitted, failed, recurring expiry, expired, and upcoming wires. |
| **ACH Alerts**                | ACH transaction events including batch submissions, returns, and failures. 5 of 7 sub-alerts configurable.                              |
| **Transfer Alerts**           | General fund transfer notifications for internal and external account movements. 1 of 4 sub-alerts configurable.                        |

### **Common Use Cases**

Business Alerts is used by finance teams and business admins to stay
informed about account activity without logging into the portal. The
following represent the most common reasons businesses configure these
alerts:

| **Use Case**                          | **Description**                                                                                                                                                |
| ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Wire approval monitoring**          | Approvers enable Wire Approval Needed alerts so they are immediately notified when a staff member submits a wire for authorisation — reducing approval delays. |
| **Wire transmission confirmation**    | Finance managers enable Wire Transmitted alerts to confirm same-day wires have been sent, supporting cash flow visibility and reconciliation.                  |
| **Failed payment detection**          | Operations staff enable Wire Transfer Failed and ACH failure alerts to catch and investigate failed payments before they cause downstream issues.              |
| **Recurring wire management**         | Treasury teams enable Recurring Wires Expiring and Upcoming alerts to proactively renew or cancel scheduled wires before they lapse.                           |
| **ACH batch oversight**               | Payroll and AP teams enable ACH Alerts to receive confirmation when payroll batches are submitted and to detect any returned items promptly.                   |
| **Security monitoring**               | Business Admins enable Security & Account Alerts to receive real-time notifications of any suspicious or unusual activity on the business account.             |
| **Selective notification management** | Users toggle individual sub-alerts on or off to avoid alert fatigue while keeping only the most business-critical notifications active.                        |
| **Do-Not-Disturb scheduling**         | Staff configure the Do-Not-Disturb tab to suppress non-urgent alerts outside business hours, reducing interruptions while maintaining critical alert coverage. |

**Step 1 — Log In and Navigate to Business Alerts**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image49.png" alt="" width="480"><figcaption></figcaption></figure>

Log in to the Diamond Credit Union portal with your User ID and
Password. Complete MFA if prompted. From the Account Overview, you can
reach Business Alerts two ways:

  - > **Via Business Banking:** Click Business Banking in the top
    > navigation bar. Scroll to the More Options section and click
    > Business Alerts.

  - > **Via More:** Click More in the top navigation bar, then select
    > Business Alerts from the menu.

Both paths land on the same Alert settings page.

**Step 2 — Select Business and Enable Business Alerts**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image36.png" alt="" width="480"><figcaption></figcaption></figure>

The Alert settings page opens on the Business Alerts tab by default. At
the top, the Target Business field shows your business membership (e.g.
\#0000978866 – Dunder Mifflin, Inc.). If you manage multiple businesses,
select the appropriate one from the dropdown

**Step 3 — Configure Individual Alert Categories**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image55.png" alt="" width="480"><figcaption></figcaption></figure>

Each alert category appears as a collapsible card. Click View More on
any card to expand it and access individual alert toggles. Click View
Less to collapse the card again.

For each category you can:

  - > **Enable all at once:** Toggle Enable All \[Category\] Alerts to
    > switch every sub-alert in that group on or off simultaneously.

  - > **Control individually:** Expand the card and toggle each
    > sub-alert independently to customise exactly which events trigger
    > a notification

# Section 4: Reporting

##  4.1 Reports

The Reports section lets authorized users view, filter, and create
financial reports on demand or on a recurring schedule, exported as PDF,
XLSX, or BAI files.

### What is in the Reports Section?

| **Characteristic** | **Detail**                                                                      |
| ------------------ | ------------------------------------------------------------------------------- |
| Report types       | Balance and Activity Statement, ACH Origination, Wire Origination, User Defined |
| Export formats     | PDF, XLSX, BAI                                                                  |
| Frequency          | On demand, Daily, Weekly, Monthly                                               |
| Visibility         | SHARED (all business users) or PRIVATE (creator only)                           |
| Navigation path    | Business Banking → More Options → Reports                                       |

### Common Use Cases

| **Use Case**               | **Description**                                                                          |
| -------------------------- | ---------------------------------------------------------------------------------------- |
| Month-end reconciliation   | Balance and Activity Statement exported as XLSX for accounting software.                 |
| ACH audit trail            | ACH Origination report to verify payroll batches and identify returned items.            |
| Executive reporting        | Monthly Business Activity report set to SHARED for management visibility.                |
| Treasury BAI integration   | BAI file export for import into treasury management or accounting systems.               |
| Compliance support         | Date-ranged activity reports for specific accounts to support regulatory reviews.        |
| Wire transfer verification | Wire Origination Report to confirm outgoing wires had correct amounts and beneficiaries. |

**Step 1 — Navigate to Reports**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image17.png" alt="" width="620"><figcaption></figcaption></figure>

Click **Business Banking** → **More Options** → **Reports**.

**Step 2 — View, Filter, and Create**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image12.png" alt="" width="620"><figcaption></figcaption></figure>The
Reports list shows all saved reports. Filter by name, type, view type
(SHARED/PRIVATE), format, or date range. Click **+ Create new report**
to start a new one.

**Step 3 — Configure the Report**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image14.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image8.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image15.png" alt="" width="620"><figcaption></figcaption></figure>Select
a **Report type**. Enter **Report name**, set **View type**, choose
**Format** (PDF/XLSX/BAI), select **Accounts**, and set **Frequency**.

**Step 4 — Save, Run, and Manage**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image9.png" alt="" width="620"><figcaption></figcaption></figure>

Click **Create and Run** (save + execute now) or **Create** (save for
later). From the reports list, click the **⋮ menu** on any row to **View
History**, **Edit**, or **Delete**.

### Quick Reference

| **Step** | **Where**  | **What to do**                                        |
| -------- | ---------- | ----------------------------------------------------- |
| 1        | Navigation | Business Banking → More Options → Reports             |
| 2        | Filter     | Search by name, type, format, or date range           |
| 3        | Create     | \+ Create new report → select report type → configure |
| 4        | Run        | Click Create and Run or Create                        |
| 5        | Manage     | Click ⋮ menu → View History / Edit / Delete           |

## 

## 

## 

## 

## 

## 

## 

## 

## 

##   

##  4.2 Commercial activity

### **What is Commercial Activity?**

Commercial Activity is the transaction history and audit log feature
within Diamond Credit Union's nFinia Business Banking portal. It
provides authorised Business Admins with a consolidated, real-time view
of all outgoing commercial payment activity for a selected business
membership — including ACH transfers, domestic wire transfers, and
template-based payments. Each transaction entry shows its current
lifecycle status, allowing teams to track payments from creation through
approval to final processing.

| **Characteristic**      | **Detail**                                                                                       |
| ----------------------- | ------------------------------------------------------------------------------------------------ |
| **Access location**     | Business Banking \> More Options \> Commercial Activity OR Transfer & Pay \> Commercial activity |
| **Who can access**      | Business Admins and users with appropriate role permissions                                      |
| **Scope**               | All commercial payment activity for the selected business membership                             |
| **Payment types shown** | ACH Payment, Domestic Wire Transfer, Template-based transfers, Fund transfers                    |
| **Status values**       | Pending approval, Processed, Cancelled                                                           |
| **Columns**             | Date created, Activity (name + tags + ID), Status, Amount                                        |
| **Filters**             | Sort and filter by date, activity type, status, or amount                                        |
| **Detail expansion**    | Click any row chevron (∨) to expand full transaction details including approval workflow         |

### **Transaction Status Reference**

Every transaction in the Commercial Activity log carries one of three
statuses, shown as a badge in the Status column:

| **Status**           | **Meaning**                                                                                                     |
| -------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Pending approval** | The transfer has been submitted and is awaiting authorisation from a designated approver. Funds have not moved. |
| **Processed**        | The transfer has been fully approved and executed. Funds have been debited from the source account.             |
| **Cancelled**        | The transfer was manually cancelled by the requester or an admin before it was approved or processed.           |

### **Common Use Cases**

Commercial Activity is used by finance teams and business admins for
daily payment oversight, reconciliation, and compliance tracking. The
following scenarios represent the most common reasons business users
access this feature:

| **Use Case**                                  | **Description**                                                                                                                                                                  |
| --------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Same-day payment verification**             | Finance managers review Commercial Activity after submitting ACH or wire transfers to confirm the transaction ID, amount, and current status before the end of business day.     |
| **Approval queue monitoring**                 | Business Admins check Pending approval items to identify transfers awaiting authorisation and follow up with approvers to avoid processing delays.                               |
| **Reconciliation and audit trail**            | Accounting teams use the full transaction history — including IDs, dates, amounts, and approval details — to reconcile internal records against the credit union's activity log. |
| **Failed or cancelled payment investigation** | Operations staff filter for Cancelled transactions to investigate why a payment was stopped and determine whether it needs to be resubmitted.                                    |
| **Approval workflow visibility**              | Admins expand individual transactions to view the full approval chain — who requested the transfer, at what time, and which approvers are authorised to action it.               |
| **Payroll and vendor payment confirmation**   | AP teams verify that batch ACH payroll or template-based vendor payments have reached Processed status before notifying recipients.                                              |
| **Multi-payment type oversight**              | Treasury teams use the activity log as a single source of truth across all payment types (ACH, Wire, Template) rather than checking each transfer type separately.               |

**Step 1 — Log In and Navigate to Commercial Activity**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image13.jpg" alt="" width="480"><figcaption></figcaption></figure>

Log in to the Diamond Credit Union portal with your User ID and
Password. Complete MFA if prompted. From the Account Overview, navigate
to Commercial Activity using either path:

  - > **Via Business Banking:** Click Business Banking in the top
    > navigation bar. Scroll to the More Options section and click
    > Commercial Activity.

  - > **Via Transfer & Pay:** Click Transfer & Pay in the top navigation
    > bar. The Commercial activity link also appears in the Related
    > Links panel on the right-hand side of the Business Banking hub.

  - > **Via Related Links:** From the Business Banking hub, click
    > Commercial activity in the Related Links panel on the right.

**Step 2 — Select Business and Review Activity**

<figure><img src="/.gitbook/assets/Diamond-CU-Master-Guide_image2.jpg" alt="" width="480"><figcaption></figcaption></figure>

The Commercial activity page opens under Banking \> Payments \>
Commercial activity. At the top, the Select business dropdown is
pre-populated with your default business membership (e.g. \#0000978866 –
Dunder Mifflin, Inc.). If you manage multiple businesses, select the
appropriate one from the dropdown to filter the activity log to that
entity.

The activity table lists all commercial transactions in
reverse-chronological order. Each row shows:

  - > **Date created:** The date the transfer was submitted.

  - > **Activity:** The transfer name or description, payment type tags
    > (e.g. ACH Payment, Domestic Wire, Template, Fund transfer,
    > One-Time), and the unique transaction ID.

  - > **Status:** Current lifecycle status — Pending approval,
    > Processed, or Cancelled.

  - > **Amount:** The debit amount from the source account.

Use Sort and filter to narrow results by date range, status, or payment
type.
