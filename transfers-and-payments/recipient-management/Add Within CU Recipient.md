# CSUM-Add-Within-CU-Recipient

**DIAMOND CREDIT UNION · BUSINESS BANKING GUIDE · Add Within-CU Recipient**

**Add Within-CU Recipient**

Module: nFinia Digital Banking > Business Banking > Transfer & Pay > Recipient Management

_Platform: Diamond Credit Union nFinia | Feature: Within CU Recipient Management | Workflow: Add Within-CU Recipient End-to-End_

> **01 PRODUCT SUMMARY**

The Add Within-CU Recipient workflow enables business admins to register payees who hold accounts at the same credit union, directly within the nFinia Business Banking platform. Because both the originating and destination accounts are held at Diamond Credit Union, no external routing number or institution lookup is required — the platform resolves the recipient account entirely from its own membership records using the membership number, account type, and last name.

The Within CU payment type offers a streamlined registration path compared to ACH or wire recipients: the admin enters the membership number, selects the account type, and provides the account holder’s last name for identity verification. The platform then validates these details against member records before allowing the recipient to be saved — a security control that prevents unauthorized payee registration.

For credit unions deploying nFinia for commercial You, Within CU transfers are common for inter-member payments, loan funding, and internal account movements. The recipient record is stored under a named transfer account with a user-defined nickname, and operates within the same role-based access controls as all Business Banking payment features.

**At a Glance**

| **Attribute**        | **Detail**                                               |
| -------------------- | -------------------------------------------------------- |
| Feature Name         | Add Within-CU Recipient                                  |
| Module               | Business Banking > Transfer & Pay > Recipient Management |
| User Roles           | Business Admin, Authorized Signer                        |
| Payment Type         | Within CU (intra-credit union only)                      |
| Verification Fields  | Membership number, Account type, Last name               |
| Key Actions          | Create Recipient, Add Account, Validate Member, Save     |
| Regulatory Relevance | Member identity verification, internal transfer controls |

> **02 STEP-BY-STEP GUIDE**
>
> _Navigation: Dashboard > Business Banking > Transfer & Pay > Recipient Management > + Add a new transfer account._

**Step 1 — Dashboard**

The business admin logs into the nFinia platform and lands on the personalized dashboard, which presents a real-time view of all account balances, upcoming loan obligations, and a Quick Transfer widget — giving the business member immediate visibility into their cash position. From here, the admin navigates to Business Banking to begin setting up a new intra-credit union recipient.

<figure><img src="/.gitbook/assets/image1 (8).png" alt="" width="480"><figcaption></figcaption></figure>

_Step 1: Dashboard_

**Step 2 — Business Banking Hub**

The Business Banking hub consolidates all commercial payment and administrative operations in a single navigation layer — ACH origination, wire transfers, payment file uploads, user and role management, approvals, and reporting. The admin navigates to Recipient Management via Transfer & Pay to begin adding a new Within CU transfer account.

<figure><img src="/.gitbook/assets/image2 (8).png" alt="" width="480"><figcaption></figcaption></figure>

_Step 2: Business Banking Hub_

**Step 3 — Transfer Account Management**

The Transfer Account Management screen displays all saved external recipients linked to the business’s accounts, organized as a searchable grid showing each recipient’s name, account count, and associated membership. The admin clicks “+ Add a new transfer account” to begin registering a new payee.

<figure><img src="/.gitbook/assets/image3 (8).png" alt="" width="480"><figcaption></figcaption></figure>

_Step 3: Transfer Account Management_

**Step 4 — Add Transfer Account**

On the Add Transfer Account screen, the admin enters the accountholder’s name — this becomes the top-level identity record for the recipient, under which one or more payment accounts can be linked. Once the name is entered, the admin clicks “+ Add Account” to define the payment method and account details.

<figure><img src="/.gitbook/assets/image4 (8).png" alt="" width="620"><figcaption></figcaption></figure>

_Step 4: Add Transfer Account_

**Step 5 — Add Account: Payment Type Selection**

The Add Account modal presents three payment type options: Within CU (for transfers to accounts held at the same credit union), ACH (for external bank accounts via the ACH network), and Domestic Wire. The admin selects “Within CU” — this restricts the transfer to You of the same institution and requires membership-based verification rather than external routing details.

<figure><img src="/.gitbook/assets/image5 (5).png" alt="" width="620"><figcaption></figcaption></figure>

_Step 5: Payment Type Selection_

**Step 6 — Add Account: Within CU Form**

With Within CU selected, the form reveals four fields: Membership number, Account type (Checking or Savings), Last name, and Nickname. Unlike the ACH path, no routing number or institution search is required — the platform resolves the destination account entirely from the credit union’s own membership records.

<figure><img src="/.gitbook/assets/image6 (4).png" alt="" width="620"><figcaption></figcaption></figure>

_Step 6: Within CU Form — Empty_

**Step 7 — Add Account: Within CU Details Entered**

The admin enters the recipient’s membership number (123456), selects Checking as the account type — which surfaces the Account# field, pre-populated from the membership record — and provides the last name (Smith) for identity verification. A nickname (“Adam S.”) is added to label this account for easy selection in future transfer workflows.

<figure><img src="/.gitbook/assets/image7 (3).png" alt="" width="620"><figcaption></figcaption></figure>

_Step 7: Within CU Form — Filled_

**Step 8 — Validation & Save**

Upon attempting to save, the platform validates the submitted membership number, account number, and last name against the credit union’s member records — a security control that prevents unauthorized recipient registration. If the details do not match, an inline error is displayed and the admin is prompted to re-enter valid information before the recipient can be saved.

<figure><img src="/.gitbook/assets/image8 (3).png" alt="" width="480"><figcaption></figcaption></figure>

_Step 8: Validation Result — Add Transfer Account_
