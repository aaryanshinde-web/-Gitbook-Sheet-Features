**SUMMERVILLE CREDIT UNION · BUSINESS BANKING USER GUIDE · CSUM-10 of 16**

**Approval Requests**

Module: Business Banking > Approvals

**Navigation: Dashboard → Business Banking → Approvals**

*Sources: Summerville Reports Series A + Series B | Features: nFinia Documentation Features Spreadsheet*

## PRODUCT SUMMARY

The Approval Requests feature provides a centralized queue for reviewing and acting on pending business banking transactions that require authorization. The interface organizes requests across status tabs: Pending Requests, Approved Requests, Declined Requests, Expired Requests, and Cancelled Requests, giving full lifecycle visibility.

Each pending request displays the transaction type (ACH, Wire), amount, requester name, number of pending approvals, and expiration date. Authorized approvers can review transaction details, approve or decline requests, and add comments. The system tracks all approval actions for audit purposes.

For credit unions, the approval queue is the execution layer of dual-control policies. It ensures that no transaction subject to multi-party authorization can be processed without the required number of approvals, providing both regulatory compliance and fraud protection.

**At a Glance**


| Attribute            | Detail                                            |
| -------------------- | ------------------------------------------------- |
| Feature Name         | Approval Requests                                 |
| Module               | Business Banking > Approvals                      |
| Navigation           | Dashboard → Business Banking → Approvals          |
| User Roles           | Authorized Signer, Business Owner, Business Admin |
| Access Level         | Role-based; requires Approval permission          |
| Key Actions          | View requests, Approve, Decline, Filter by status |
| Regulatory Relevance | Dual-control enforcement, approval audit trail    |


## KEY USE CASES


| Use Case                   | Who Uses It       | What They Do                                       | Business Value                                  |
| -------------------------- | ----------------- | -------------------------------------------------- | ----------------------------------------------- |
| Approve Pending Payment    | Authorized Signer | Review and approve pending ACH or wire request     | Enforces dual-control before payment processing |
| Decline Suspicious Request | Business Owner    | Decline a transaction that appears unauthorized    | Fraud prevention through human review           |
| Review Approval History    | Business Admin    | Audit approved, declined, and expired transactions | Supports compliance reviews and internal audits |
| Monitor Expired Requests   | Business Owner    | Identify payments that expired without approval    | Ensures critical payments are not missed        |


## STEP-BY-STEP USER GUIDE

**How to get here: Dashboard → Business Banking → Approvals**

**Step 1: Log In and Open the Dashboard**

Open your web browser and navigate to the Summerville Credit Union digital banking platform. Enter your username and password on the login screen and click "Log In." If prompted, complete the OTP (One-Time Passcode) verification by entering the code sent to your registered device. After successful authentication, you will land on the Dashboard — also called the Account Overview screen. This is your home base. The Dashboard displays all your business accounts (Savings Accounts, Checking Accounts) with their available and current balances. The top navigation bar shows links to Dashboard, Accounts, Transfer & Pay, Cards, Business Banking, and More. On the right sidebar you will see Related Links (Change Password, Account Settings, View Scheduled Transfers, Account Specific Alerts) and a Quick Transfer widget for fast internal transfers. To proceed to Business Banking features, locate the "Business Banking" tab in the top navigation bar and click on it.

<figure><img src="/.gitbook/assets/img_5c532a850867.png" alt="Figure 1 — Log In and Open the Dashboard" width="620"><figcaption></figcaption></figure>

*Figure 1 — Log In and Open the Dashboard*

**Step 2: Open the Business Banking Hub**

After clicking "Business Banking" in the top navigation bar, the Business Banking Hub loads. This is the central command center for all commercial banking operations. The Hub is organized into three sections: "Transfers" at the top (with tiles for ACH Transfer, Domestic Wire Transfer, Transfer Template, and Payment From File), "Manage" in the middle (with tiles for Role Management, User Management, Approval Settings, and Recipient Management), and "More Options" at the bottom (with tiles for Commercial Activity, Reports, and Approvals). Each tile is a direct entry point to its corresponding feature. Only tiles your role has permission to access will be visible. From here, locate and click the tile for the feature you need — the next steps will guide you through the specific workflow.

<figure><img src="/.gitbook/assets/img_04cfec25c89e.png" alt="Figure 2 — Open the Business Banking Hub" width="620"><figcaption></figcaption></figure>

*Figure 2 — Open the Business Banking Hub*

**Step 3: Navigate to Approvals and Review Pending Requests**

From the Dashboard, click "Business Banking" in the left-side navigation menu to open the Business Banking Hub. Scroll down to the "More Options" section and click the "Approvals" tile. The Approvals page opens to the "Pending Requests" tab — your primary action queue. Each pending transaction is displayed as a row showing: Transaction Type (ACH Payment, Domestic Wire), Amount, Requester Name (who initiated the payment), Approvals Pending (e.g., "1 of 2"), and Expiration Date. To act on a request, click the row to expand the full details, then click "Approve" to authorize or "Decline" to reject. The badge on the Pending tab shows the total count of items awaiting your action.

<figure><img src="/.gitbook/assets/img_69c55b81e970.png" alt="Figure 3 — Navigate to Approvals and Review Pending Requests" width="620"><figcaption></figcaption></figure>

*Figure 3 — Navigate to Approvals and Review Pending Requests*

**Step 4: Review Approved Transactions**

Click the "Approved Requests" tab to see all transactions that have received the required approvals and been released for processing. Each entry shows the transaction details, the names of all approvers, their approval timestamps, and the processing status. Use this tab to verify that approved transactions were processed correctly. Filter by date range to review approvals for specific periods. This serves as your positive audit trail for compliance reviews — it documents who approved what and when.

<figure><img src="/.gitbook/assets/img_8b5a0cd26018.png" alt="Figure 4 — Review Approved Transactions" width="620"><figcaption></figcaption></figure>

*Figure 4 — Review Approved Transactions*

**Step 5: Review Declined Transactions**

Click the "Declined Requests" tab to see transactions that were rejected by an approver. Each entry shows the transaction details, who declined it, when, and any comments provided. Declined transactions are not automatically retried — the original initiator must create a new transaction if the payment is still needed. Review this tab regularly: a high number of declines may indicate unauthorized activity, incorrect amounts, or training gaps that need attention.

<figure><img src="/.gitbook/assets/img_17dc8264cfd5.png" alt="Figure 5 — Review Declined Transactions" width="620"><figcaption></figcaption></figure>

*Figure 5 — Review Declined Transactions*

**Step 6: Check Expired Requests**

Click the "Expired Requests" tab to see transactions that were not approved within the configured time window. Each entry shows the transaction details, submission date, expiration date, and how many approvals were received vs. required. Expired requests cannot be retroactively approved — the initiator must resubmit the transaction. A high volume of expired requests indicates that approvers are not monitoring the queue regularly. Consider enabling Business Alerts for approval notifications to ensure approvers are promptly notified of pending items.

<figure><img src="/.gitbook/assets/img_123d92091a80.png" alt="Figure 6 — Check Expired Requests" width="620"><figcaption></figcaption></figure>

*Figure 6 — Check Expired Requests*

**Step 7: Review Cancelled Requests**

Click the "Cancelled Requests" tab to see transactions voluntarily withdrawn by the initiator before receiving all required approvals. Each entry shows who cancelled it and when. This tab completes the full lifecycle view: Pending → Approved / Declined / Expired / Cancelled. Use all five tabs together during compliance audits to demonstrate that your dual-control approval process is functioning correctly and that all transaction outcomes are documented.

<figure><img src="/.gitbook/assets/img_930f55c6cd56.png" alt="Figure 7 — Review Cancelled Requests" width="620"><figcaption></figcaption></figure>

*Figure 7 — Review Cancelled Requests*

