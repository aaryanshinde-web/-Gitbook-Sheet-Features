**Check Services**

Stop Check & Reorder Check

nFinia Digital Banking Platform

Summerville Federal Credit Union

Product Guide \| April 2026

  ------------------------
  **1. Product Summary**
  ------------------------

Check Services in the nFinia digital banking platform provides You with two essential check management capabilities: Stop Check Payment and Reorder Checks. These features empower credit union You to manage their check-related needs entirely through digital self-service, eliminating the need to call the branch or visit in person.

Stop Check Payment allows You to place a stop payment order on a single check or a series of checks that have been issued but not yet cleared. This is critical for situations involving lost, stolen, or disputed checks. Reorder Checks enables You to place a new checkbook order directly from their digital banking session, pulling verified account details and mailing address from the core system.

Both features are accessible from the More menu hub on the nFinia dashboard, providing a streamlined path for You to manage check services. The platform enforces proper account selection, validates check numbers, and maintains a complete audit trail for compliance purposes.

**At a Glance**

  ---------------------- ----------------------------------------------------------------
  **Attribute**          **Detail**
  Feature Name           Check Services (Stop Check & Reorder Check)
  Module                 Banking > More > Check Stop Payment / Reorder Checks
  User Roles             Personal Member, Business Member, Authorized Signer
  Access Level           Account holder with checking account
  Key Actions            Stop payment on single/series checks, Reorder checkbooks
  Regulatory Relevance   UCC Article 4 stop payment rights, audit trail, fee disclosure
  ---------------------- ----------------------------------------------------------------

  ------------------
  **2. Use Cases**
  ------------------

  ---------------------------- ----------------- ----------------------------------------------------------------- -------------------------------------------------------------
  **Use Case**                 **Who Uses It**   **What They Do**                                                  **Business Value**
  Stop a lost check            Personal Member   Places stop payment on a single check that was lost in the mail   Prevents unauthorized cashing; protects member funds
  Stop a series of checks      Business Member   Stops a range of check numbers after a checkbook is stolen        Blocks multiple potential fraud attempts in one action
  Reorder personal checkbook   Personal Member   Places a checkbook order with verified address from core          Self-service reduces branch workload; faster fulfillment
  Reorder business checks      Business Admin    Orders checks for a business money market or checking account     Business continuity without branch visit
  Dispute prevention           Any Member        Stops payment before a disputed check clears                      Reduces dispute processing costs for the credit union
  Audit compliance             FI Operations     Reviews stop payment history and fee assessments                  Maintains regulatory compliance with UCC stop payment rules
  ---------------------------- ----------------- ----------------------------------------------------------------- -------------------------------------------------------------

These use cases demonstrate how Check Services reduces friction for both personal and business You. By enabling self-service stop payments and check reorders, Summerville FCU can lower call center volume while giving You immediate control over their check management needs.

  ----------------------------
  **3. End-to-End Workflow**
  ----------------------------

**3.1 Prerequisites**

- Active checking or money market account with check-writing privileges

- Valid login credentials for nFinia digital banking

- Check number(s) available for stop payment requests

**3.2 Stop Check Payment Flow**

Step 1: Member logs into the Summerville FCU nFinia portal and lands on the Dashboard. The dashboard displays all accounts with balances, Quick Transfer widget, upcoming payments, and credit score.

<figure><img src="/.gitbook/assets/24c30f617e73e6629d17809c27be42eacd3ba8fb.png" alt="" width="340"><figcaption></figcaption></figure>{width="5.0in" height="7.854166666666667in"}

Step 2: Member clicks the \"More\" button in the top navigation bar to access additional banking services. The More options page displays all available personal banking features including Notifications, User ID and Password, Personal Information, Accounts and Memberships, Alert Settings, Add Membership, Travel Notice, Reorder Checks, Check Stop Payment, and Skip-a-Pay.

<figure><img src="/.gitbook/assets/5d113ae19a7e22fd64da3337eeb9f7f8da6a8917.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.833333333333333in" height="3.3645833333333335in"}

Step 3: Member selects \"Check Stop Payment\" from the More menu. The Check Stop Payment form appears with account selection, check number entry, optional amount, and memo fields. you select their account, enters the check number, optionally enters the check amount, and accepts the terms and conditions before clicking \"Stop Payments.\"

<figure><img src="/.gitbook/assets/3faef7d73969f2738ed25c9ea1984ccea0e21a5c.png" alt="" width="480"><figcaption></figcaption></figure>{width="5.625in" height="5.947916666666667in"}

**3.3 Reorder Checks Flow**

Step 4: To reorder checks, you navigate to Banking > More > Reorder Checks. The system displays the selected account details including membership owner(s), primary owner, email ID, and verified mailing address pulled directly from the core system.

<figure><img src="/.gitbook/assets/70963dd07db7a4dc2a38907cdf9f2294c961f755.png" alt="" width="480"><figcaption></figcaption></figure>{width="5.625in" height="5.302083333333333in"}

Step 5: Member reviews the pre-populated information including account number, owner details, and mailing address. After confirming the details are correct, they click \"Place checkbook order\" to submit the request.

**3.4 Decision Points & Branching**

- Single Check vs. Series: You can choose to stop a single check by number or a series of consecutive checks.

- Fee Assessment: A stop payment fee (as configured by the credit union) is disclosed before submission. The current fee is displayed on the Check Stop Payment screen.

- Terms Acceptance: You must accept the Terms and Conditions before the stop payment can be processed.

- Account Eligibility: Only accounts with check-writing privileges appear in the account dropdown.

**3.5 Completion & Confirmation**

Upon successful submission, You receive an on-screen confirmation with a reference number. The stop payment order or check reorder is logged in the system for audit purposes. Email and/or push notifications are sent based on you\'s alert preferences.

**3.6 Error Handling**

- Invalid Check Number: System validates the check number format and range before submission.

- Already Cleared Check: If the check has already been processed, the system displays an error indicating the stop payment cannot be placed.

- Insufficient Funds for Fee: If the stop payment fee exceeds available balance, the request is declined.

  -------------------------
  **4. Feature Overview**
  -------------------------

**4.1 Check Stop Payment**

The Check Stop Payment screen allows You to place a stop payment order on issued checks. It provides single check or series options, amount entry, and terms acceptance.

  ---------------------- ------------------ -------------------------------------------------- --------------------------------------------------------------
  **Field / Element**    **Type**           **Description**                                    **Notes**
  Select account         Dropdown           Account to stop the check on                       Required; only checking/money market accounts shown
  Number of Checks       Radio Button       Single Check or Series of Checks                   Determines whether one or multiple check numbers are stopped
  Check number           Input              The check number to stop payment on                Required; numeric validation
  Amount on Check        Input (Currency)   Dollar amount on the check                         Optional; helps identify the specific check
  Memo                   Textarea           Reason or notes for the stop payment               Optional; stored for audit trail
  Terms and Conditions   Checkbox + Link    Acceptance of stop payment terms                   Required; includes fee disclosure
  Stop Payments          Button (Primary)   Submits the stop payment request                   Disabled until terms are accepted
  Upcoming payments      Widget             Shows scheduled payments for context               Read-only sidebar widget
  Related links          Navigation         Change Password, E-Statements, Transfers, Alerts   Quick access to related features
  ---------------------- ------------------ -------------------------------------------------- --------------------------------------------------------------

**4.2 Reorder Checks**

The Reorder Checks screen displays verified account and address information and allows You to place a checkbook order with a single click.

  ----------------------- ------------------ ------------------------------------------------------------------------------- --------------------------------------------
  **Field / Element**     **Type**           **Description**                                                                 **Notes**
  Select account          Dropdown           Account to reorder checks for                                                   Required; shows eligible checking accounts
  Membership owner(s)     Label              Name(s) of account owners                                                       Read-only; pulled from core system
  Primary owner           Label              Primary account holder name                                                     Read-only
  Email ID                Label              Email on file for the account                                                   Read-only; for confirmation delivery
  Mailing address         Label              Verified address from core system                                               Read-only; checks shipped to this address
  Place checkbook order   Button (Primary)   Submits the check reorder request                                               Initiates the order fulfillment process
  Related Links           Navigation         Change Password, Set default deposit, Check Stop Payment, Commercial activity   Cross-navigation to related features
  ----------------------- ------------------ ------------------------------------------------------------------------------- --------------------------------------------

  ------------------------
  **5. Quick Reference**
  ------------------------

  --------------------------- ------------------------------------------------- ------------------- ----------------------------------
  **Task**                    **Navigation Path**                               **Who Can Do It**   **Notes**
  Stop payment on a check     Dashboard > More > Check Stop Payment           Account Holder      Single or series; fee applies
  Reorder checkbook           Dashboard > More > Reorder Checks               Account Holder      Address from core; no editing
  View stop payment history   Dashboard > More > Check Stop Payment           Account Holder      Historical stop orders listed
  Access via Related Links    Any page > Related Links > Check Stop Payment   Account Holder      Cross-linked from Reorder Checks
  --------------------------- ------------------------------------------------- ------------------- ----------------------------------

  -------------------
  **6. Conclusion**
  -------------------

Check Services in the nFinia digital banking platform delivers essential check management capabilities through an intuitive self-service interface. Stop Check Payment and Reorder Checks together address the most common check-related member needs, reducing branch and call center burden while maintaining full regulatory compliance.

For Summerville Federal Credit Union, these features reinforce the value proposition of digital banking by making routine financial tasks accessible 24/7. The integration with the core system ensures data accuracy for check reorders, while built-in validation and terms acceptance protect both you and the institution during stop payment processing.
