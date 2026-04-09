**Summerville Federal Credit Union**

nFinia Digital Banking Platform

**Loan Repayment**

Feature Release Notes & Product Guide

Prepared by: Jeeva Krishnamurthy, Senior Product Manager

Tyfone, Inc. \| April 2026 \| Confidential

  ------------------------
  **1. Product Summary**
  ------------------------

Loan Repayment is a core feature of the nFinia Digital Banking platform that enables credit union You to make payments on their loan accounts directly through the digital banking portal. This capability covers one-time payments, scheduled recurring payments, and multiple payment option types including regular payments, next-due-amount payments, payoff amounts, and pay-to-principal options --- all accessible through the Transfer Funds to Own Account workflow.

Within the Summerville Federal Credit Union digital banking portal, Loan Repayment is accessible from the Account Details page of any loan account via the "Make Payment" link, or through Move Money > Transfer Funds to Own Account by selecting a loan account as the destination. The feature integrates with the platform's existing fund transfer infrastructure, providing a guided three-step workflow (Set up Transfer → Review → Finish) that ensures You can make informed payment decisions with clear confirmation at each stage.

For Summerville FCU, Loan Repayment reduces delinquency rates by making it effortless for You to stay current on their obligations. The self-service capability deflects routine payment inquiries from the contact center, while the recurring payment option promotes consistent repayment behavior. You benefit from 24/7 payment access, flexible scheduling, and the ability to make additional principal payments to accelerate their payoff timeline.

**At a Glance**

  -------------------------- ----------------------------------------------------------------------------------------------
  **Attribute**              **Detail**
  **Feature Name**           Loan Repayment (Transfer Funds to Own Account --- Loan)
  **Module**                 Move Money > Transfer Funds to Own Account / Accounts > Account Details > Make Payment
  **User Roles**             Primary Account Holder, Joint Account Holder, Delegated User (with Transfer permissions)
  **Access Level**           Account-level; requires active loan account and funded source account
  **Key Actions**            Make Payment, Schedule Recurring Payment, Pay Next Due Amount, Payoff Loan, Pay to Principal
  **Supported Core**         Ultra Data (UD); standard nFinia transfer infrastructure
  **Regulatory Relevance**   Payment confirmation, transaction audit trail, scheduled transfer disclosures
  -------------------------- ----------------------------------------------------------------------------------------------

  ------------------
  **2. Use Cases**
  ------------------

  --------------------------------------- ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------
  **Use Case**                            **Who Uses It**   **What They Do**                                                                                                                                               **Business Value**
  Make a one-time loan payment            Account Holder    Navigates to loan Account Details, clicks Make Payment, selects source account, chooses payment amount, enters transfer date, reviews and confirms             Enables self-service loan payments without branch visit; reduces delinquency risk
  Set up recurring loan payments          Account Holder    During transfer setup, checks "Make transfer recurring," selects frequency (weekly, bi-weekly, monthly), sets end date or repeat count, reviews and confirms   Automates payment schedule; promotes consistent repayment behavior and reduces missed payments
  Pay next due amount                     Account Holder    Selects "Next due amt" from payment option dropdown to automatically populate the minimum payment due                                                          Simplifies minimum payment process; ensures member pays exactly what is owed for the billing cycle
  Make a payoff payment                   Account Holder    Selects "Payoff amount" from payment option dropdown to populate the full remaining balance                                                                    Enables loan payoff without calling for a payoff quote; accelerates loan closure
  Pay to principal                        Account Holder    Selects "Pay to principal" to apply the entire payment directly to the loan principal                                                                          Allows You to reduce principal faster, lowering total interest paid over the loan term
  View loan account and payment history   Account Holder    Views Account Details showing amount due, payment due date, overdue status, payoff amount, and full transaction history                                        Provides complete loan visibility; helps You track payment progress and remaining balance
  --------------------------------------- ----------------- -------------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------

These use cases reflect the primary loan repayment scenarios for Summerville FCU You. The combination of flexible payment options, recurring scheduling, and self-service payoff capabilities addresses both the credit union's goal of reducing delinquency and your need for convenient, transparent loan management.

  ----------------------------
  **3. End-to-End Workflow**
  ----------------------------

**3.1 Prerequisites**

• Member must be enrolled in Summerville FCU digital banking with an active membership.

• you must hold at least one active loan account (auto loan, personal loan, mortgage, etc.).

• you must have a funded source account (checking or savings) from which to make the payment.

• Transfer permissions must be enabled for your role (relevant for delegated access users).

**3.2 Step-by-Step Workflow**

**Step 1: View Loan Account Overview**

<figure><img src="/.gitbook/assets/941cb6109ca40bea557207ec0807c5bc303d7582.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.395833333333333in" height="4.666666666666667in"}

you log into the Summerville FCU digital banking portal and navigates to Accounts Overview, filtering by Loan Accounts. The overview displays each loan with its account name (e.g., "2019 BMW 0001"), Amount Due, Payment Due / Next Due Date, Payoff Amount, and quick action links including "History" and "Transfer Funds." Overdue loans are highlighted with a red "Overdue" indicator and the next due date in red text.

**Step 2: View Loan Account Details**

<figure><img src="/.gitbook/assets/faeef6b4b3667130c900a8c85083cd8af8943042.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.28125in" height="4.791666666666667in"}

Clicking on the loan account opens the Account Details page, which provides a comprehensive view of the loan including Amount Due (\$498.67), Payment Due / Next Due Date (\$0.95 due on Oct 27, 2025), and links to "Make Payment," "Skip-a-Pay," and "See more." Below the summary card, the Transactions section displays the full payment history with deposits, payment credits, and balance progression. you click "Make Payment" to initiate the loan repayment workflow.

**Step 3: Set Up Transfer --- Select Payment Option**

<figure><img src="/.gitbook/assets/419e72b26bfd162ab5880db184ed7f1c29b3e76d.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.333333333333333in" height="4.854166666666667in"}

The Transfer Funds to Own Account screen opens with the three-step progress indicator (Set up Transfer → Review → Finish). Step 1 displays the From account (source checking/savings) and To account (the loan). The Payment Option dropdown provides four choices: Select (default), Next due amt, Payoff amount, Pay to principal, and Make a regular payment. you also has the option to check "Make transfer recurring" to set up automated payments. The "Make this my preferred source account" checkbox allows saving the source account for future payments.

**Step 4: Enter Payment Amount and Date**

<figure><img src="/.gitbook/assets/10fe725cbd98588d807375aa0160fc96f3875611.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.416666666666667in" height="4.895833333333333in"}

After selecting a payment option (e.g., "Make a regular payment"), you enter the Amount to be transferred and an optional Transaction memo (limited to 23 characters). The Transfer Date field defaults to today's date with a calendar picker for scheduling future payments. A "Make transfer recurring" checkbox is available for setting up automated payment schedules. you click "Continue" to proceed to the review step.

**Step 5: Configure Recurring Payment (Optional)**

<figure><img src="/.gitbook/assets/edbb99947b19a2bbc25e91dd2a8f1a343140cc84.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="4.895833333333333in"}

When "Make transfer recurring" is checked, additional scheduling fields appear: Frequency (Weekly transfer, Bi-Weekly, Monthly, etc.), Repeat (Until end date, Number of times, Until cancelled), and End Date. The system displays a confirmation summary such as "Scheduled Weekly transfer, until April 15, 2026." This enables You to automate their loan payments on a consistent schedule, reducing the risk of missed payments.

**Step 6: Review Transfer**

<figure><img src="/.gitbook/assets/dd6109a2a1574b388fad5f07085bfa600a88d76f.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.385416666666667in" height="3.34375in"}

The Review screen (Step 2 of 3) presents a complete summary of the payment: the transfer amount (\$1.00), From account (PREFD C 0040 with available balance), To account (2019 BMW 0001), Transfer date, and recurring schedule details if applicable. you can click "Back" to modify any details, "Cancel" to abort, or "Confirm Transfer" to submit the payment. This review step ensures you have full visibility before committing.

**Step 7: Transfer Success**

<figure><img src="/.gitbook/assets/98f2b25b450f321bfa1599a03392160bc3a15a0b.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.427083333333333in" height="3.8020833333333335in"}

Upon successful submission, the Finish screen (Step 3 of 3) displays a green checkmark with "Successfully Sent" confirmation showing the transfer amount, source and destination accounts, and transfer date. A "Print" link allows you to generate a receipt, and the "Done" button returns to the main banking view. The transaction is immediately recorded in the account's transaction history.

**3.3 Decision Points & Branching**

The Loan Repayment workflow includes several decision points:

• Payment Option Selection: Choosing "Next due amt" or "Payoff amount" auto-populates the amount field from the loan's API data. "Pay to principal" directs the entire payment to principal reduction. "Make a regular payment" allows free-form amount entry.

• Recurring vs. One-Time: Checking "Make transfer recurring" expands the form to show Frequency, Repeat, and End Date fields. Unchecked, the payment processes as a single one-time transfer.

• Transfer Date: You can schedule payments for today (immediate) or a future date using the calendar picker. Future-dated payments appear as scheduled transfers in your queue.

• Source Account Selection: You can choose from any eligible funded account. The "Make this my preferred source account" checkbox stores the selection for future loan payments.

**3.4 Completion & Confirmation**

All loan payments conclude with a confirmation screen showing the transfer amount, source/destination accounts, and transfer date. For one-time payments, funds are debited immediately (or on the scheduled date). For recurring payments, the schedule is created and the first payment processes on the specified start date. Each transaction generates an audit log entry and appears in the loan account's transaction history. You can print a receipt from the success screen.

**3.5 Error Handling**

Common failure scenarios include: insufficient funds in the source account (displays balance error and prevents submission), amount exceeds payoff balance (validation error), invalid transfer date (past dates rejected), and system timeout during submission (retry option displayed). For scheduled recurring transfers, if a future payment fails due to insufficient funds, the system generates a failed transfer notification while subsequent scheduled payments continue.

  ------------------------------------------
  **4. Feature Overview (UI Walkthrough)**
  ------------------------------------------

**4.1 Loan Accounts Overview**

Displays all loan accounts with key metrics and quick action links.

  ----------------------------- ------------- -------------------------------------------------------- -------------------------------------------
  **Field / Element**           **Type**      **Description**                                          **Notes**
  Account Name                  Label         Loan account name (e.g., "2019 BMW 0001")                Click to open Account Details
  Membership Info               Label         Loan Account in Membership with account number           Read-only
  Amount Due                    Label         Current amount due on the loan                           Displays "ℹ" info icon for details
  Payment Due / Next Due Date   Label         Next payment amount and due date                         Red text and "Overdue" badge if past due
  Payoff Amount                 Label         Total payoff balance for the loan                        Includes "Transfer Funds" action link
  History                       Action Link   Opens transaction history for the loan                   Blue text link
  Transfer Funds                Action Link   Initiates the loan payment workflow                      Navigates to Transfer Funds screen
  Group by / Filter by          Dropdowns     Filter accounts by account group, membership, and type   Defaults to "Loan Accounts" when filtered
  ----------------------------- ------------- -------------------------------------------------------- -------------------------------------------

**4.2 Loan Account Details**

Detailed view of a single loan account with payment actions and transaction history.

  ----------------------------- ----------------- ------------------------------------------------------------------ -----------------------------------------
  **Field / Element**           **Type**          **Description**                                                    **Notes**
  Viewing account details for   Dropdown          Account selector to switch between loan accounts                   Pre-populated with current loan
  Edit account name             Action Link       Allows renaming the loan account                                   Blue text link
  Amount Due                    Label             Current payment amount due                                         
  Payment Due / Next Due Date   Label             Due date with overdue indicator if applicable                      Red "Overdue" text for past-due amounts
  Make Payment                  Action Link       Initiates the Transfer Funds to Own Account flow                   Primary entry point for loan repayment
  Skip-a-Pay                    Action Link       Opens skip-a-payment workflow if eligible                          Subject to FI configuration
  See more                      Expandable Link   Reveals additional loan details (rate, term, etc.)                 Toggles expanded view
  Transactions                  Table             Full transaction history with date, description, amount, balance   Searchable, exportable, printable
  ----------------------------- ----------------- ------------------------------------------------------------------ -----------------------------------------

**4.3 Transfer Funds --- Set Up Transfer (Step 1)**

The main payment setup form with account selection, payment options, and scheduling.

  --------------------------------------- ---------------- ------------------------------------------------------------------------------- ------------------------------------------------------------
  **Field / Element**                     **Type**         **Description**                                                                 **Notes**
  From Account                            Account Card     Source account with name, number, and available balance                         "Change" link to select different source
  To Account                              Account Card     Destination loan account with name, number, and balance                         "Change" link to select different loan
  Make this my preferred source account   Checkbox         Saves source account as default for future payments                             Persists across sessions
  Payment option                          Dropdown         Select: Next due amt, Payoff amount, Pay to principal, Make a regular payment   Auto-populates amount for first three options
  Amount to be transferred                Currency Input   Dollar amount for the payment                                                   Pre-filled or manual entry based on option
  Transaction memo (optional)             Text Input       Optional memo attached to the transfer                                          Max 23 characters; cannot be used with scheduled transfers
  Transfer Date                           Date Picker      Date for the payment to process                                                 Calendar picker; defaults to today
  Make transfer recurring                 Checkbox         Enables recurring payment scheduling                                            Reveals Frequency, Repeat, and End Date fields
  Frequency                               Dropdown         Weekly, Bi-Weekly, Monthly, Quarterly, etc.                                     Visible only when recurring is checked
  Repeat                                  Dropdown         Until end date, Number of times, Until cancelled                                Controls recurrence termination
  End date                                Date Picker      Final date for recurring payments                                               Visible when "Until end date" is selected
  Cancel                                  Button           Aborts the transfer and returns to previous screen                              Secondary outlined button
  Continue                                Button           Validates inputs and proceeds to Review step                                    Primary blue button
  --------------------------------------- ---------------- ------------------------------------------------------------------------------- ------------------------------------------------------------

**4.4 Transfer Review (Step 2)**

Confirmation screen displaying all payment details before submission.

  ---------------------------- -------------- ------------------------------------------ ------------------------------------------------------------
  **Field / Element**          **Type**       **Description**                            **Notes**
  Transfer Amount              Label          The payment amount displayed prominently   Large centered text
  From Account                 Account Card   Source account with available balance      Read-only summary
  To Account                   Account Card   Destination loan account                   Read-only summary
  Transfer date                Label          Scheduled payment date                     
  Scheduled transfer details   Label          Recurring schedule summary if applicable   e.g., "Scheduled Bi-Weekly transfer, until April 15, 2026"
  Back                         Button         Returns to Step 1 with data retained       Left-aligned
  Cancel                       Button         Aborts the transfer                        Secondary outlined button
  Confirm Transfer             Button         Submits the payment for processing         Primary blue button
  ---------------------------- -------------- ------------------------------------------ ------------------------------------------------------------

**4.5 Transfer Success (Step 3)**

Confirmation screen displayed after successful payment submission.

  --------------------- --------------- -------------------------------------------------- ---------------------
  **Field / Element**   **Type**        **Description**                                    **Notes**
  Success Icon          Graphic         Green checkmark indicating successful transfer     
  "Successfully Sent"   Label           Confirmation message with transfer amount          Large centered text
  From / To Accounts    Account Cards   Source and destination accounts with balances      Read-only
  Transfer date         Label           Date the payment was processed                     
  Print                 Action Link     Generates a printable receipt of the transaction   Opens print dialog
  Done                  Button          Returns to the main banking view                   Primary blue button
  --------------------- --------------- -------------------------------------------------- ---------------------

  ------------------------
  **5. Quick Reference**
  ------------------------

  -------------------------- --------------------------------------------------------------------------- ------------------- ---------------------------------------
  **Task**                   **Navigation Path**                                                         **Who Can Do It**   **Notes**
  View loan accounts         Accounts > Accounts Overview > Filter: Loan Accounts                      Account Holder      Shows all loans with payment status
  Make a loan payment        Account Details > Make Payment > Set up Transfer > Review > Confirm     Account Holder      3-step guided workflow
  Pay next due amount        Make Payment > Payment option: Next due amt                                Account Holder      Auto-populates minimum payment due
  Pay off loan               Make Payment > Payment option: Payoff amount                               Account Holder      Auto-populates full remaining balance
  Pay to principal           Make Payment > Payment option: Pay to principal                            Account Holder      Entire payment applied to principal
  Set up recurring payment   Make Payment > Check "Make transfer recurring" > Set frequency/end date   Account Holder      Automates future payments on schedule
  View payment history       Account Details > Transactions                                             Account Holder      Searchable, exportable, printable
  Print payment receipt      Transfer Success > Print                                                   Account Holder      Available after successful payment
  -------------------------- --------------------------------------------------------------------------- ------------------- ---------------------------------------

  -------------------
  **6. Conclusion**
  -------------------

Loan Repayment is a foundational self-service capability for Summerville Federal Credit Union's digital banking offering on the nFinia platform. The feature addresses a critical member need by enabling convenient, flexible loan payments through the same Transfer Funds infrastructure used across the platform, ensuring a consistent and familiar user experience.

The guided three-step workflow (Set up Transfer → Review → Finish) with clear confirmation screens ensures You make informed payment decisions. The multiple payment options --- next due amount, payoff, pay-to-principal, and regular payments --- cater to diverse member needs, from minimum obligation fulfillment to accelerated debt reduction. The recurring payment capability is particularly valuable for reducing delinquency by automating consistent repayment schedules.

For Summerville FCU, Loan Repayment strengthens member retention by removing friction from the repayment process. You who can easily manage their loan payments digitally are less likely to fall behind and more likely to remain engaged with the credit union for future lending needs. The feature reduces contact center volume for routine payment inquiries and provides full transaction audit trails that support the credit union's operational and compliance requirements.
