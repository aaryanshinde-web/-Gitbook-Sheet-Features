**SUMMERVILLE FEDERAL CREDIT UNION**

nFinia Digital Banking Platform

**Round Up to Savings**

Feature Documentation & Product Guide

Prepared by: Product Management

Date: April 7, 2026

Version: 1.0

**1. Product Summary**

Round Up to Savings is an automated micro-savings feature within the nFinia digital banking platform that enables credit union You to effortlessly grow their savings with every debit card transaction. When enabled, each debit card purchase is automatically rounded up to the next whole dollar amount, and the difference is transferred from your designated checking account into their selected savings account.

This feature serves retail banking You who want a passive, friction-free approach to building their savings. It is particularly valuable for You who find it difficult to set aside money manually. By converting everyday spending into incremental savings, Round Up to Savings aligns with Summerville Federal Credit Union's mission to promote financial wellness and long-term wealth building among its membership.

Round Up to Savings lives under Banking > More > Round Up to Savings in the nFinia platform. You can configure the feature independently, choosing between rounding to the nearest dollar or doubling the round-up amount. The feature includes full self-service management: You can set up, edit, and remove round-up preferences, view cumulative savings metrics (month-to-date, year-to-date, last year, and total), and opt out at any time through a confirmation workflow.

**At a Glance**

  -------------------------- ----------------------------------------------------------------------------------------------
  **Attribute**              **Detail**
  **Feature Name**           Round Up to Savings
  **Module**                 Banking > More > Round Up to Savings
  **User Roles**             Primary Account Holder, Joint Account Holder
  **Access Level**           Member self-service; no admin approval required for enrollment
  **Key Actions**            Set Up, Edit, Remove, View Savings Summary, Opt Out
  **Linked Account Types**   From: Checking accounts; To: Savings accounts (Share Savings, Money Market, Special Savings)
  **Round-Up Options**       Round to nearest dollar (\$0.01--\$0.99 per transaction) or Double the round-up amount
  **Regulatory Relevance**   Regulation E (electronic fund transfers), audit trail for automated transfers
  -------------------------- ----------------------------------------------------------------------------------------------

**2. Use Cases**

  ---------------------------------- ---------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------
  **Use Case**                       **Who Uses It**                          **What They Do**                                                                                                                                          **Business Value**
  **Initial Enrollment**             Primary Member                           Navigates to More > Round Up to Savings, selects a checking (From) and savings (To) account, chooses rounding preference, agrees to T&C, and activates   Drives savings account growth and deepens member engagement with minimal effort
  **Passive Savings Accumulation**   Any enrolled member                      Makes everyday debit card purchases; system automatically rounds up each transaction and transfers the difference to the savings account                  You build savings without conscious effort, increasing average savings balances for the credit union
  **Preference Change**              Enrolled Member                          Edits existing round-up configuration to switch between nearest-dollar and double round-up modes, or changes linked accounts                              Flexibility to adjust savings aggressiveness based on financial goals
  **Savings Progress Review**        Enrolled Member                          Views the savings dashboard showing month-to-date, year-to-date, last year, and total cumulative savings from round-ups                                   Transparency builds trust and motivates continued participation
  **Opt-Out / Removal**              Enrolled Member                          Clicks Remove on an active round-up, confirms opt-out through a Yes/No dialog to deactivate the feature                                                   Full member control; no lock-in ensures positive member experience
  **Multiple Account Setup**         Member with multiple checking accounts   Sets up additional round-up rules for other checking accounts via "Add Round Up to Savings for an account"                                                Maximizes savings capture across all transactional accounts
  ---------------------------------- ---------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------

These use cases demonstrate how Round Up to Savings serves Summerville FCU's strategic goal of improving member financial health. The feature's low friction and full self-service design means it requires no staff intervention, reducing operational cost while driving organic savings account balance growth. For You who struggle with manual savings discipline, the automated round-up mechanism provides a behavioral nudge that compounds over time.

**3. End-to-End Workflow**

**3.1 Prerequisites**

-   Member must have an active checking account with a linked debit card

-   Member must have at least one eligible savings account (Share Savings, Money Market Savings, or Special Savings)

-   Member must be authenticated and logged into the nFinia digital banking platform

-   Feature must be enabled by the credit union in the platform configuration

**3.2 Step-by-Step Flow**

1.  **Start from the Dashboard:** After logging into the nFinia digital banking platform, you land on the **Dashboard / Account Overview** page. This screen displays your account summary, membership details, related links, and quick transfer options. To access Round Up to Savings, you navigate via the top navigation bar.

<figure><img src="/.gitbook/assets/fd69f6c8b01624fae1f8d73a52e431bb9a8d4fb0.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 1: Dashboard --- Account Overview starting point*

2.  **Open the More Menu:** From the top navigation bar, you click **More**. The More menu expands to reveal available self-service features. you click **Round up to savings** which is highlighted with the description "Increase your savings when you transact."

<figure><img src="/.gitbook/assets/3255656de6c4325ca6347991aa2185fccc616569.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 2: More menu showing the Round Up to Savings entry point*

3.  **Select From Account:** The Round Up to Savings setup page loads, displaying an explanation of how the feature works. you select their checking account from the "From account" dropdown. Available options include all checking accounts under their membership (e.g., BONUS CHECKING, MAIN CHECKING). The dropdown displays account name and account number for clear identification.

<figure><img src="/.gitbook/assets/f9d7fa52eb62a6b8436bb5dbd2d1da8be22439c1.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 3: Selecting the source checking account for round-ups*

4.  **Select To Account:** you select their destination savings account from the "To account" dropdown. Eligible savings account types include Share Savings -- Special, Peak Money Market Savings, and other savings products. The dropdown filters to only show savings-eligible accounts under the selected membership.

<figure><img src="/.gitbook/assets/5878fa47299c5fc24131ca44e9e00253e7884048.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 4: Selecting the destination savings account*

5.  **Choose Round-Up Method:** you select one of two rounding options:

-   **Round up to the nearest dollar** --- For a \$9.50 transaction, \$0.50 is transferred to savings (rounds to \$10.00)

-   **Double the round up amount before the deposit** --- For a \$9.50 transaction, \$1.00 is transferred to savings (double the \$0.50 round-up)

Each option includes an "Example" link that displays a tooltip illustrating the calculation with a sample transaction amount.

<figure><img src="/.gitbook/assets/546aa1e48552395e8aad0910ca8030a80fdc72c8.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 5: Round to nearest dollar option with example tooltip (\$9.50 → \$0.50 transferred)*

<figure><img src="/.gitbook/assets/0c61c683bbaf6264b6b083508f892be4b92ed529.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 6: Double the round-up option with example tooltip (\$9.50 → \$1.00 transferred)*

6.  **Agree to Terms & Conditions:** you checks the "I agree to the Round Up to Savings terms and conditions" checkbox. The terms and conditions link opens the full legal agreement. This checkbox must be checked before the "Set up Round Up to Savings" button becomes active.

7.  **Activate Round Up:** you click the "Set up Round Up to Savings" button. The system validates the configuration and activates the round-up rule.

<figure><img src="/.gitbook/assets/1d4aafaa3237b688388a6c61e156552693e84393.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 7: Completed enrollment form with all options selected and T&C accepted*

**3.3 Decision Points & Branching**

-   **Single vs. Double Round-Up:** your choice affects the transfer amount per transaction. Single rounds to the nearest dollar; double multiplies the round-up by 2. You can change this preference at any time after enrollment.

-   **Multiple Checking Accounts:** You with multiple checking accounts can set up separate round-up rules for each. The "Add Round Up to Savings for an account" option enables additional enrollments.

-   **Insufficient Funds:** If the checking account has insufficient funds to cover the round-up amount at the time of the debit card transaction, the system behavior is governed by the credit union's overdraft and courtesy pay settings.

**3.4 Completion & Confirmation**

Upon successful activation, the system displays a confirmation banner: "Round Up to Savings preference saved successfully." The page transitions to show the active round-up configuration including the linked accounts, the selected rounding method, and a savings metrics dashboard.

<figure><img src="/.gitbook/assets/0628f15cef1839e75ba9b49d9f077eb61eddaa09.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 8: Confirmation screen with savings metrics dashboard (MTD, YTD, Last Year, Total)*

The savings dashboard displays four key metrics: Month to Date savings, Year to Date savings, Last year savings, and Total savings. Below the metrics, the system confirms the selected rounding method (e.g., "Round Up amounts will be doubled and deposited into your selected savings account").

**3.5 Post-Enrollment Management**

Once enrolled, you can return to the Round Up to Savings page at any time to manage their preferences. The active configuration view displays the linked account pairing, savings metrics, and the current rounding method. Two action links are available: Edit (to modify the rounding method or linked accounts) and Remove (to deactivate the round-up rule).

<figure><img src="/.gitbook/assets/32e419ed84507b239a65f942e72bfe8d542fa180.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 9: Active round-up configuration with Edit and Save options*

**3.6 Opt-Out / Removal**

When a member clicks "Remove" on an active round-up configuration, a modal confirmation dialog appears asking: "Are you sure you want to opt out from Round Up to Savings?" The dialog presents two clear options: "No" (cancel and return to the management view) and "Yes" (confirm removal and deactivate the round-up rule). This two-step confirmation prevents accidental deactivation.

<figure><img src="/.gitbook/assets/d87dd35b6a9d97a41aa998bbdf986731cee0edbe.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 10: Opt-out confirmation dialog with No/Yes options*

**3.7 Error Handling**

-   **Missing Account Selection:** If you attempts to submit without selecting both a From and To account, the system prevents submission and highlights the missing field.

-   **Terms Not Accepted:** The "Set up Round Up to Savings" button remains disabled until the terms and conditions checkbox is checked.

-   **Same Account Selected:** The To account dropdown only displays savings-type accounts, preventing you from selecting the same checking account as both source and destination.

**4. Feature Overview (UI Walkthrough)**

**4.1 More Menu --- Feature Entry Point**

The Round Up to Savings feature is accessed through the More menu in the top navigation bar. It appears alongside other self-service features such as eStatements, Stop Payment, Direct Deposit Form, and Skip-a-Pay. The entry displays the feature name and a brief description: "Increase your savings when you transact."

  --------------------- ----------------- --------------------------------------------------- ---------------------------------------
  **Field / Element**   **Type**          **Description**                                     **Notes**
  Round up to savings   Navigation Link   Entry point to the Round Up to Savings setup page   Highlighted with icon and description
  Feature Description   Label             "Increase your savings when you transact"           Displayed below feature name
  --------------------- ----------------- --------------------------------------------------- ---------------------------------------

**4.2 Round Up to Savings --- Setup Page**

The setup page provides a clear explanation of how the feature works, followed by the configuration form. The page header states: "Round Up to Savings works like an automatic savings account. Your everyday debit card transactions are rounded-up to the next dollar amount and the difference is deposited into your designated savings account."

  -------------------------------- -------------------- ------------------------------------------------------------------------------- ---------------------------------------------------
  **Field / Element**              **Type**             **Description**                                                                 **Notes**
  From account                     Dropdown             Selects the checking account whose debit card transactions will be rounded up   Required; shows all checking accounts
  To account                       Dropdown             Selects the savings account where round-up amounts will be deposited            Required; shows only savings-type accounts
  Round up to the nearest dollar   Radio Button         Rounds each transaction to the next whole dollar; transfers the difference      Includes "Example" tooltip link
  Double the round up amount       Radio Button         Doubles the round-up difference before transferring to savings                  Includes "Example" tooltip link
  Terms and Conditions             Checkbox             Member agreement to the Round Up to Savings terms                               Required; links to full T&C document
  Set up Round Up to Savings       Button (Primary)     Submits the form and activates the round-up rule                                Disabled until all fields complete + T&C accepted
  Cancel                           Button (Secondary)   Returns to the previous page without saving changes                             No confirmation required
  -------------------------------- -------------------- ------------------------------------------------------------------------------- ---------------------------------------------------

**4.3 Round Up to Savings --- Active Configuration & Dashboard**

After enrollment, the page transitions to show the active round-up configuration. This view serves as the management hub where You can monitor savings progress and modify their preferences. (See Figure 9 in Section 3.5 for the screenshot.)

  ---------------------------------------- -------------- ------------------------------------------------------------------------------------------------------------- --------------------------------------
  **Field / Element**                      **Type**       **Description**                                                                                               **Notes**
  Add Round Up to Savings for an account   Link/Toggle    Enables setup of additional round-up rules for other checking accounts                                        Shown at top of active config view
  Account Pairing Display                  Label          Shows From Account → To Account pairing (e.g., BONUS CHECKING \#10 to SHARE SAVINGS -- SPECIAL \#29)          Bold formatting for account names
  Month to Date savings                    Metric Label   Cumulative round-up savings for the current calendar month                                                    Displays dollar amount
  Year to Date savings                     Metric Label   Cumulative round-up savings for the current calendar year                                                     Displays dollar amount
  Last year savings                        Metric Label   Total round-up savings from the previous calendar year                                                        Displays dollar amount
  Total savings                            Metric Label   All-time cumulative round-up savings since enrollment                                                         Displays dollar amount
  Rounding Method Display                  Label          Confirms active method: "Round Up amounts will be doubled and deposited into your selected savings account"   Updates based on selected preference
  Edit / Remove                            Action Links   Edit opens inline editing; Remove triggers opt-out confirmation dialog                                        Available per active round-up rule
  ---------------------------------------- -------------- ------------------------------------------------------------------------------------------------------------- --------------------------------------

**4.4 Opt-Out Confirmation Dialog**

When a member clicks "Remove," a modal dialog confirms the action before deactivating. (See Figure 10 in Section 3.6 for the screenshot.)

  ---------------------- -------------------- -------------------------------------------------------------- ---------------------------------------
  **Field / Element**    **Type**             **Description**                                                **Notes**
  Confirmation Message   Dialog Text          "Are you sure you want to opt out from Round Up to Savings?"   Modal overlay on current page
  No                     Button (Secondary)   Cancels the removal and returns to the management view         Outlined style
  Yes                    Button (Primary)     Confirms removal and deactivates the round-up rule             Filled/dark style with checkmark icon
  ---------------------- -------------------- -------------------------------------------------------------- ---------------------------------------

**5. Quick Reference**

  ---------------------------- -------------------------------------------------------------- ------------------- --------------------------------------
  **Task**                     **Navigation Path**                                            **Who Can Do It**   **Notes**
  Set up Round Up to Savings   More > Round up to savings                                    Account Holder      Requires checking + savings accounts
  Choose rounding method       Round Up setup page                                            Account Holder      Nearest dollar or double round-up
  View savings progress        More > Round up to savings (post-enrollment)                  Account Holder      MTD, YTD, Last Year, Total metrics
  Edit round-up preferences    Round Up dashboard > Edit                                     Account Holder      Change method or linked accounts
  Add another account          Round Up dashboard > Add Round Up to Savings for an account   Account Holder      Set up additional checking accounts
  Remove / Opt out             Round Up dashboard > Remove                                   Account Holder      Confirmation dialog required
  ---------------------------- -------------------------------------------------------------- ------------------- --------------------------------------

*--- End of Document ---*
