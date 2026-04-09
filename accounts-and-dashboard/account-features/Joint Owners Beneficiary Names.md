**Accounts -- Joint Owners & Beneficiary Names**

Feature Delivery Guide

Summerville Federal Credit Union \| nFinia Platform \| April 2026

  ------------------------
  **1. Product Summary**
  ------------------------

The Joint Owners & Beneficiary Names feature enhances the Account Detail view in nFinia Online Banking by displaying all account holders and designated beneficiaries directly on the account summary page. Previously, You could only view their own name on the account; with this enhancement, Primary Holders, Joint Holders, and Beneficiaries are listed with their respective roles clearly labeled beneath each name.

This feature serves all retail and business You who hold joint accounts or have designated beneficiaries on deposit accounts. It is particularly valuable for credit unions like Summerville Federal Credit Union, where family membership and multi-owner accounts represent a significant portion of the membership base. By surfacing this information in the digital channel, You no longer need to call or visit a branch to confirm account ownership details.

The feature is accessible from the Account Detail page within the Accounts module. When a member clicks on any account from the Account Overview dashboard, the detail page now includes an expandable \"All Account Holders\" section showing every holder and beneficiary associated with that account. This drives transparency, reduces operational call volume, and supports regulatory compliance by ensuring You can verify account ownership information digitally.

**At a Glance**

  -------------------------- ------------------------------------------------------------------------------
  **Attribute**              **Detail**
  **Feature Name**           Joint Owners & Beneficiary Names Display
  **Module**                 Accounts > Account Detail
  **User Roles**             All authenticated You (Primary Holder, Joint Holder)
  **Access Level**           Read-only; visible to all account holders
  **Key Actions**            View account holders, Expand/Collapse holder list, Identify roles
  **Regulatory Relevance**   Supports account ownership transparency, beneficiary disclosure requirements
  **Platform Version**       nFinia OLB v10.49+
  -------------------------- ------------------------------------------------------------------------------

  ------------------
  **2. Use Cases**
  ------------------

  ------------------------- ----------------- ------------------------------------------------------------------------------------------------------------------ -----------------------------------------------------------------
  **Use Case**              **Who Uses It**   **What They Do**                                                                                                   **Business Value**
  Verify Joint Ownership    Primary Member    Logs in, navigates to Account Detail, expands All Account Holders to confirm who is listed on the account          Reduces branch/call center inquiries about account ownership
  Confirm Beneficiary       Account Holder    Views the beneficiary name and role label on the Account Detail page to verify designated beneficiary is correct   Supports estate planning transparency; reduces disputes
  Family Account Review     Joint Holder      Joint holder logs in to verify their name appears correctly on the shared account with proper role designation     Builds member confidence in account accuracy and data integrity
  Onboarding Verification   New Member        After account opening, new joint holder verifies they appear on the account in digital banking                     Confirms successful account setup without branch visit
  Audit & Compliance        FI Operations     Credit union can point You to the digital channel for self-service ownership verification during audits        Supports NCUA examination readiness and member transparency
  ------------------------- ----------------- ------------------------------------------------------------------------------------------------------------------ -----------------------------------------------------------------

These use cases reflect the reality that joint accounts and beneficiary designations are core to credit union membership. Summerville FCU, like many community credit unions, serves multi-generational families where account ownership clarity is essential. By enabling digital self-service for ownership verification, the credit union reduces operational friction while strengthening member trust.

  ----------------------------
  **3. End-to-End Workflow**
  ----------------------------

**3.1 Prerequisites**

• Member must have an active online banking enrollment with Summerville FCU

• Account must have at least one additional holder or beneficiary configured in the core system

• Feature must be enabled at the FI configuration level (nFinia Admin)

**3.2 Step-by-Step Flow**

**Step 1 -- Dashboard (Account Overview):** Member logs into nFinia Online Banking and lands on the Account Overview dashboard. All enrolled memberships and accounts are displayed as tile cards showing account type, balance, and last activity.

<figure><img src="/.gitbook/assets/0626ee68834c4ae05407526488a70359313c95cc.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.208333333333333in" height="4.208333333333333in"}

*Figure 1: Summerville FCU -- Account Overview Dashboard*

**Step 2 -- Account Detail (Joint Owners & Beneficiary View):** Member clicks on a specific account tile (e.g., Savings Account) to open the Account Detail page. The page displays account balances (Available, Current, Minimum), quick action links (Internal Transfer, See More), and the All Account Holders section. Expanding this section reveals each holder with their role: Primary Holder, Joint Holder, or Beneficiary. The right sidebar provides related links including Change Password, Account Settings, Download E-Statements, and more.

<figure><img src="/.gitbook/assets/a6c93798a570e4af43975ecfb4e05b0aade0c037.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.729166666666667in" height="3.9375in"}

*Figure 2: Account Detail -- Joint Owners & Beneficiary Names*

**3.3 Decision Points & Branching**

• If the account has no additional holders or beneficiaries, the All Account Holders section displays only the primary holder name.

• If you are a Joint Holder (not Primary), they see the same holder list but cannot modify ownership.

• The feature is read-only; no editing of holder/beneficiary information is possible through the digital channel. Changes must be made through branch or back-office operations.

**3.4 Completion & Confirmation**

This is a view-only feature with no transactional confirmation. you simply views the account holder information. The data is sourced in real-time from the core banking system, ensuring accuracy. No notifications or audit log entries are generated for viewing this information.

**3.5 Error Handling**

• If the core system is unavailable, the All Account Holders section may display a loading indicator or fallback message.

• If holder data is incomplete in the core, the field may show the holder name without a role label.

• No destructive errors are possible since this is a read-only display feature.

  ------------------------------------------
  **4. Feature Overview (UI Walkthrough)**
  ------------------------------------------

**Account Detail Page**

The Account Detail page is the primary screen for this feature. It displays account summary information, balance details, and the new All Account Holders section. The page is accessed by selecting any account from the Account Overview dashboard (Figures 1--2).

**Field Reference -- Account Detail**

  ------------------------- -------------------- -------------------------------------------------------------------------------------------------------------- ------------------------------------------------------
  **Field / Element**       **Type**             **Description**                                                                                                **Notes**
  Account Title             Label                Displays account type and membership number                                                                    e.g., \"Savings Account in Membership \#0000979019\"
  Available Balance         Label                Current available balance for the account                                                                      May show negative values in red
  Current Balance           Label                Ledger balance of the account                                                                                  Updated in real-time from core
  Minimum Balance           Label                Minimum balance recorded for the period                                                                        Informational; no alerts triggered
  Internal Transfer         Link                 Quick link to initiate a transfer from this account                                                            Opens Move Money > Internal Transfer
  See More                  Link                 Expands additional account actions                                                                             Toggles visibility of secondary actions
  All Account Holders       Expandable Section   Lists all holders and beneficiaries with role labels: Primary Holder, Joint Holder, Beneficiary                NEW in this release; data sourced from core
  Holder Name               Label                Full name of each account holder or beneficiary                                                                Displayed in a grid layout
  Role Label                Label                Role designation: Primary Holder, Joint Holder, or Beneficiary                                                 Appears below each holder name in smaller text
  Transactions Section      Table                Displays recent transactions with date range filter, search, export, and print options                         Default: Last 30 days
  Related Links (Sidebar)   Link List            Quick access to Change Password, Account Settings, Download E-Statements, View Scheduled Transfers, and more   Contextual to the selected account
  ------------------------- -------------------- -------------------------------------------------------------------------------------------------------------- ------------------------------------------------------

  ------------------------
  **5. Quick Reference**
  ------------------------

  ---------------------------- ------------------------------------------------------------------- ------------------- --------------------------------------
  **Task**                     **Navigation Path**                                                 **Who Can Do It**   **Notes**
  View account holders         Accounts > [Account] > All Account Holders                      All You         Expand section to see full list
  Verify beneficiary           Accounts > [Account] > All Account Holders                      All You         Beneficiary shown with role label
  Check account balances       Accounts > [Account]                                             All You         Available, Current, Minimum balances
  Initiate internal transfer   Accounts > [Account] > Internal Transfer                        All You         Quick link on Account Detail page
  View transactions            Accounts > [Account] > Transactions                             All You         Filterable by date range
  Download E-Statements        Accounts > [Account] > Related Links > Download E-Statements   All You         Sidebar link on Account Detail
  ---------------------------- ------------------------------------------------------------------- ------------------- --------------------------------------

*--- End of Document ---*
