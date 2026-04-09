**Summerville Federal Credit Union**

nFinia Digital Banking Platform

**Certificate Management**

Feature Release Notes & Product Guide

Prepared by: Jeeva Krishnamurthy, Senior Product Manager

Tyfone, Inc. \| April 2026 \| Confidential

  ------------------------
  **1. Product Summary**
  ------------------------

Certificate Management is a core feature of the nFinia Digital Banking platform that enables credit union You to manage their investment certificate (CD) accounts directly through the digital banking portal. This capability allows You to renew certificates, hold balances without renewal, and close certificates at maturity --- all without visiting a branch or calling the contact center.

Within the Summerville Federal Credit Union digital banking portal, Certificate Management is accessible from the Account Details page via the "Manage Certificate" link on any eligible investment account. The feature provides a guided, step-by-step workflow for each maturity option: renewing the certificate for the same or a different term, holding the balance in a non-accruing state, or transferring the balance to a checking or savings account upon maturity.

For Summerville FCU, Certificate Management reduces operational burden on branch staff by enabling self-service certificate lifecycle management. You benefit from 24/7 access to manage their investment accounts on their own schedule, with clear review screens and confirmation steps that ensure informed decision-making. The feature supports Ultra Data core integration and is configured through the nFinia platform's system configuration framework.

**At a Glance**

  -------------------------- ---------------------------------------------------------------------------
  **Attribute**              **Detail**
  **Feature Name**           Certificate Management (Manage Certificate)
  **Module**                 Accounts > Account Details > Manage Certificate
  **User Roles**             Primary Account Holder, Joint Account Holder
  **Access Level**           Account-level; requires eligible Investment (Product ID type "I") account
  **Key Actions**            Renew Certificate, Hold Balance Without Renewing, Close at Maturity
  **Supported Core**         Ultra Data (UD); Correlation planned for future release
  **Regulatory Relevance**   Terms & Conditions acceptance, audit trail, transaction confirmation
  -------------------------- ---------------------------------------------------------------------------

  ------------------
  **2. Use Cases**
  ------------------

  ------------------------------------- ------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------
  **Use Case**                          **Who Uses It**    **What They Do**                                                                                                                                      **Business Value**
  Renew certificate at maturity         Account Holder     Navigates to Account Details, clicks Manage Certificate, selects Renew, chooses term, reviews, and submits renewal request                            Enables self-service certificate renewal without branch visit; retains member deposits
  Rollover to new certificate product   Account Holder     Selects Reinvest/Rollover option, picks a new certificate product from available list, specifies withdrawal amount if partial, reviews and confirms   Provides flexibility to move funds into better-rate products; increases certificate portfolio diversity
  Hold balance without renewing         Account Holder     Selects Hold Balance option, accepts Terms & Conditions, confirms the hold request                                                                    Preserves funds in account without commitment; member retains option to renew or withdraw later
  Close certificate at maturity         Account Holder     Selects Close at Maturity, chooses transfer-to account (Checking/Savings), optionally selects closure reason, accepts T&C, confirms                   Enables orderly certificate closure with funds directed to preferred account; optional reason tracking for FI analytics
  View certificate details              Account Holder     Views Account Details page showing current balance, interest rate, term, and maturity date with Manage Certificate link                               Provides at-a-glance certificate health; single entry point to all management actions
  FI configures maturity options        FI Administrator   Configures MANAGE_CERTIFICATE_CONFIG to enable/disable renewal, hold, and close options per credit union                                            Allows each FI to tailor available options to their product strategy and core system capabilities
  ------------------------------------- ------------------ ----------------------------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------------------------------------------------------------------------------------

These use cases reflect the primary scenarios for Summerville FCU You managing investment certificates. The combination of self-service renewal, flexible rollover options, and orderly closure workflows addresses both the operational efficiency needs of the credit union and the convenience expectations of You who prefer to manage their finances digitally.

  ----------------------------
  **3. End-to-End Workflow**
  ----------------------------

**3.1 Prerequisites**

• Member must be enrolled in Summerville FCU digital banking with an active membership.

• you must hold at least one eligible Investment account (Product ID type "I" in Ultra Data core).

• The Certificate Management feature must be enabled in the FI's system configuration (MANAGE_CERTIFICATE_CONFIG).

• The certificate must be within its maturity management window for renewal, hold, or closure options to appear.

**3.2 Step-by-Step Workflow**

**Step 1: View Certificate on Account Details**

<figure><img src="/.gitbook/assets/ecf7fd81a0106ba3cb8422c1d9045df07d6a4a7c.png" alt="" width="620"><figcaption></figcaption></figure>{width="4.416666666666667in" height="0.7083333333333334in"}

you log into the Summerville FCU digital banking portal and navigates to their Account Details page for the investment certificate. The page displays key certificate information including Current Balance, Interest Rate, Term (in days), and Maturity Date. A "Manage Certificate" link is prominently displayed, providing the single entry point to all certificate management actions.

**Step 2: Manage Certificate Options**

<figure><img src="/.gitbook/assets/c8c988948de3b52730ceacd99431a2e2a8843970.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.729166666666667in"}

Clicking "Manage Certificate" presents the available maturity options configured for this certificate. The options include Renew Certificate (reinvest the full balance or rollover to a new product), Hold Balance Without Renewing (keep funds in account without accruing additional interest), and Close at Maturity (transfer balance to another account). The available options are determined by the MANAGE_CERTIFICATE_CONFIG system configuration and the core system's availableMaturityOptions response.

**Step 3: Renew Certificate --- Select Renewal Option**

<figure><img src="/.gitbook/assets/575cf0cd493eb7949a8d5815242572f5bd1e6ad6.png" alt="" width="480"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.885416666666667in"}

When you select Renew Certificate, they are presented with renewal options in a guided stepper workflow. Step 1 asks you to choose between renewing the existing certificate (reinvest full balance at current or new term) or reinvesting/rolling over to a new certificate product. The current maturity option is pre-selected based on the currentMaturityOption API response. If you select Reinvest or Rollover, additional fields appear for selecting the rollover product and specifying a partial withdrawal amount.

**Step 4: Select Term**

<figure><img src="/.gitbook/assets/669585442174622e38b603264d9541d2ca0642f3.png" alt="" width="480"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.833333333333333in"}

In Step 2 of the renewal flow, you select the term for the renewed certificate. For Ultra Data core, the term is entered as a number of days with minimum and maximum validation based on the availableReinvestTerms API response (minTerm and maxTerm values). For Correlation core, terms are presented as a dropdown selection. you review the selected term and clicks Next to proceed to the review screen.

**Step 5: Review Renewal Details**

<figure><img src="/.gitbook/assets/24f456174cd789add3372fab19c384fad68c176c.png" alt="" width="480"><figcaption></figcaption></figure>{width="6.458333333333333in" height="6.114583333333333in"}

The Review screen presents a comprehensive summary of the renewal configuration: the certificate account, selected renewal option, chosen term, current balance, interest rate, and maturity date. you can click Back to modify any selection (all previously entered data is retained) or click Renew to submit the renewal request to the core banking system.

**Step 6: Renewal Success**

<figure><img src="/.gitbook/assets/fe703babde4b4a33949d29e04ce60fed688fe00b.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.65625in"}

Upon successful submission, the system displays a confirmation screen with the renewal details and a success message. The screen includes a reference number for the transaction and a link to return to the Accounts page. If the renewal fails due to a recoverable error, a retry option is presented. Customer support contact information is displayed for non-recoverable errors.

**Step 7: Hold Balance Without Renewing**

<figure><img src="/.gitbook/assets/b98be393a3c5f9cea5235173d5fb3503ad024201.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.770833333333333in"}

When you select Hold Balance Without Renewing, the system presents a confirmation screen explaining that the certificate will not be renewed and the balance will remain in the account without accruing additional interest post-maturity. you must accept the Terms and Conditions via a checkbox before the Submit button becomes active. This ensures informed consent and creates an audit trail of your decision.

**Step 8: Hold Balance Success**

<figure><img src="/.gitbook/assets/7e1a6c25cc3eb8257cfea0e0382c24f292b6fbf9.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.770833333333333in"}

After accepting the terms and submitting, the system confirms the hold request with a success screen. The balance remains accessible and you retains the option to renew the certificate at a later date, transfer the balance, or withdraw funds without penalty.

**Step 9: Close at Maturity**

<figure><img src="/.gitbook/assets/eb74ebde9fa15467ce03d3f776ca08c93aebe26a.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.21875in"}

When you select Close at Maturity, they are prompted to select a transfer-to account (filtered to eligible Checking, Savings, or Loan accounts based on the accountConfigs and memberConfigs configuration). An optional reason selector is displayed if IS_CLOSE_CERTIFICATE_REASON_MANDATORY is configured; selecting "Other" reveals a free-text input field. you must accept the Terms and Conditions before submitting the closure request.

**Step 10: Close at Maturity Success**

<figure><img src="/.gitbook/assets/a33297f340a1a2f1327dda3fa8729d45f6493e2a.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.770833333333333in"}

The system confirms the certificate closure with a success screen showing the transfer details, destination account, and a reference number. The certificate balance is transferred to the selected account and the certificate account is marked for closure.

**3.3 Decision Points & Branching**

The Certificate Management workflow includes several decision points that affect the user journey:

• Renewal Option Selection: Choosing "Renew existing certificate" follows a straightforward term selection flow. Choosing "Reinvest or Rollover" adds an additional step to select the target certificate product from rolloverTypeList and optionally specify a partial withdrawal amount.

• Partial Withdrawal: If you opts to withdraw a portion of the balance during rollover, the system validates the amount against minimum and maximum thresholds and requires selection of an eligible transfer-to account.

• Core System Variation: Ultra Data presents term selection as a free-text day input with min/max validation. Correlation presents terms as a dropdown selection. The widgetType configuration key controls which input is displayed.

• Closure Reason: The reason field on Close at Maturity is optional or required based on IS_CLOSE_CERTIFICATE_REASON_MANDATORY configuration. Reasons are maintained in nFinia configs and tracked in Harmoney for analytics.

**3.4 Completion & Confirmation**

All three workflows (Renew, Hold Balance, Close at Maturity) conclude with a confirmation screen that includes: a success/failure status message, transaction reference number, summary of the action taken, customer support contact information, and a navigation link to return to the Accounts page. Successful transactions generate an audit log entry and may trigger member notifications depending on the FI's alert configuration.

**3.5 Error Handling**

Common failure scenarios include: invalid term entry (outside minTerm/maxTerm range) which triggers inline validation, withdrawal amount exceeding available balance which displays an error message, core system timeout which presents a retry option, and Terms & Conditions not accepted which keeps the Submit button disabled. For non-recoverable errors, the system displays customer support contact information and a reference ID for troubleshooting.

  ------------------------------------------
  **4. Feature Overview (UI Walkthrough)**
  ------------------------------------------

**4.1 Account Details --- Certificate Information**

This screen displays the investment certificate's key metrics and provides the entry point to certificate management.

  --------------------- ----------------- ------------------------------------------- ----------------------------------------
  **Field / Element**   **Type**          **Description**                             **Notes**
  Current Balance       Label             Displays the current certificate balance    Read-only; sourced from core system
  Interest Rate         Label             Current APY/APR for the certificate         Read-only
  Term                  Label             Certificate term displayed in days          e.g., "731 days"
  Maturity Date         Label             Date when the certificate matures           Format: Month DD, YYYY
  Show more             Expandable Link   Reveals additional account details          Toggles detailed view
  Manage Certificate    Action Link       Opens the certificate management workflow   Blue text link; entry point to feature
  --------------------- ----------------- ------------------------------------------- ----------------------------------------

**4.2 Manage Certificate --- Options Page**

Presents the available maturity options for the certificate based on system configuration and core API response.

  ------------------------------- -------------- ---------------------------------------------------- ------------------------------------------------------------
  **Field / Element**             **Type**       **Description**                                      **Notes**
  Renew Certificate               Radio Button   Select to begin the certificate renewal workflow     Available when REINVEST is in AVAILABLE_MATURITY_OPTIONS
  Hold Balance Without Renewing   Radio Button   Select to hold funds without renewal                 Supported on Correlation core
  Close at Maturity               Radio Button   Select to close the certificate and transfer funds   Available when CLOSE_AT_MATURITY is configured
  Next                            Button         Proceeds to the selected option's workflow           Primary blue button; disabled until selection made
  Cancel                          Button         Returns to Account Details                           Secondary outlined button
  ------------------------------- -------------- ---------------------------------------------------- ------------------------------------------------------------

**4.3 Renew Certificate --- Renewal Option (Step 1)**

First step of the renewal stepper where you select their preferred renewal method.

  ----------------------------------------- -------------- -------------------------------------------------------------------- ------------------------------------------------
  **Field / Element**                       **Type**       **Description**                                                      **Notes**
  Stepper Progress                          UI Indicator   Shows current position: Renewal Option > Term > Review > Finish   4-step progress indicator
  Renew the existing certificate            Radio Button   Reinvest full balance into same product type                         Auto-selected if currentMaturityOption matches
  Reinvest or rollover to new certificate   Radio Button   Move funds to a different certificate product                        Shows additional rollover product dropdown
  Rollover Product Dropdown                 Dropdown       Lists available certificate products from rolloverTypeList           Visible only when Rollover is selected
  Withdrawal Amount                         Text Input     Amount to withdraw during rollover                                   Validated against min/max thresholds
  Transfer To Account                       Dropdown       Eligible destination account for withdrawn funds                     Filtered by accountConfigs and memberConfigs
  Next                                      Button         Proceeds to Term selection                                           Validates required fields before advancing
  Cancel                                    Button         Returns to Manage Certificate options                                
  ----------------------------------------- -------------- -------------------------------------------------------------------- ------------------------------------------------

**4.4 Renew Certificate --- Term Selection (Step 2)**

Second step where you specifies the renewal term for their certificate.

  --------------------- ------------ --------------------------------------------------- -------------------------------------------
  **Field / Element**   **Type**     **Description**                                     **Notes**
  Term (Days)           Text Input   Member enters desired term in days (Ultra Data)     Validated: minTerm ≤ value ≤ maxTerm
  Term Selection        Dropdown     Member selects from available terms (Correlation)   Pre-populated from availableReinvestTerms
  Next                  Button       Proceeds to Review screen                           Validates term selection
  Back                  Button       Returns to Renewal Option step with data retained   Preserves all selections
  --------------------- ------------ --------------------------------------------------- -------------------------------------------

**4.5 Renew Certificate --- Review (Step 3)**

Summary screen for you to verify all renewal details before submission.

  --------------------- ---------- ------------------------------------------- -----------------------------------
  **Field / Element**   **Type**   **Description**                             **Notes**
  Certificate Account   Label      Account number and description              Read-only summary
  Renewal Option        Label      Selected renewal type (Reinvest/Rollover)   
  Selected Term         Label      Chosen term in days                         
  Current Balance       Label      Balance being renewed                       
  Interest Rate         Label      Rate applicable to renewal                  
  Maturity Date         Label      New projected maturity date                 
  Back                  Button     Returns to Term step                        Retains entered data
  Renew                 Button     Submits renewal request to core system      Primary action; triggers API call
  --------------------- ---------- ------------------------------------------- -----------------------------------

**4.6 Hold Balance Without Renewing**

Confirmation screen where you agrees to hold funds without certificate renewal.

  --------------------- ---------------- ------------------------------------------------------------- -------------------------------------------------
  **Field / Element**   **Type**         **Description**                                               **Notes**
  Information Text      Static Content   Explains that balance will remain without accruing interest   Loaded from static content API or local strings
  Terms & Conditions    Checkbox         Member must accept T&C before submitting                      Submit disabled until checked
  Submit                Button           Confirms the hold balance request                             Enabled only after T&C acceptance
  Cancel                Button           Returns to Manage Certificate options                         
  --------------------- ---------------- ------------------------------------------------------------- -------------------------------------------------

**4.7 Close at Maturity**

Form for closing the certificate and transferring the balance to another account.

  --------------------- ------------ ----------------------------------------------------- ----------------------------------------------------
  **Field / Element**   **Type**     **Description**                                       **Notes**
  Transfer To Account   Dropdown     Eligible Checking, Savings, or Loan accounts          Filtered by accountConfigs; primary ownership only
  Reason for Closure    Dropdown     Optional/required based on config; reasons from API   Selecting "Other" shows text input
  Reason (Other)        Text Input   Free-text reason when "Other" is selected             String input included in closure request
  Terms & Conditions    Checkbox     Member must accept T&C before closing                 Required for submission
  Submit                Button       Submits closure request to core system                Enabled after T&C and account selection
  Cancel                Button       Returns to Manage Certificate options                 
  --------------------- ------------ ----------------------------------------------------- ----------------------------------------------------

  ------------------------
  **5. Quick Reference**
  ------------------------

  ------------------------------- ------------------------------------------------------------------------------ ------------------- --------------------------------------------
  **Task**                        **Navigation Path**                                                            **Who Can Do It**   **Notes**
  View certificate details        Accounts > Account Details                                                    Account Holder      Shows balance, rate, term, maturity date
  Open Manage Certificate         Account Details > Manage Certificate                                          Account Holder      Requires eligible Investment account
  Renew existing certificate      Manage Certificate > Renew > Renewal Option > Term > Review > Renew       Account Holder      Full balance reinvested at selected term
  Rollover to new certificate     Manage Certificate > Renew > Rollover > Select Product > Review > Renew   Account Holder      Optional partial withdrawal available
  Hold balance without renewal    Manage Certificate > Hold Balance > Accept T&C > Submit                     Account Holder      Balance accessible; no interest accrual
  Close certificate at maturity   Manage Certificate > Close > Select Account > Accept T&C > Submit          Account Holder      Funds transferred to selected account
  Configure maturity options      System Config > MANAGE_CERTIFICATE_CONFIG                                   FI Administrator    Controls which options are available
  Enable/disable feature          System Config > MANAGE_CERTIFICATE_OPTIONS                                  FI Administrator    Per-slug enable: reinvest, rollover, close
  ------------------------------- ------------------------------------------------------------------------------ ------------------- --------------------------------------------

  -------------------
  **5. Conclusion**
  -------------------

Certificate Management is a critical self-service capability for Summerville Federal Credit Union's digital banking offering on the nFinia platform. The feature addresses a fundamental gap in you experience by enabling account holders to manage the full lifecycle of their investment certificates --- from renewal and rollover to balance holds and maturity closures --- without requiring branch visits or phone calls.

The guided stepper workflow with clear review screens and Terms & Conditions acceptance ensures You make informed decisions while creating the audit trail required for regulatory compliance. The configurable architecture --- driven by MANAGE_CERTIFICATE_CONFIG and core system API responses --- allows Summerville FCU to tailor the available options to their product strategy and core system capabilities. The Ultra Data core integration is fully supported in the current release, with Correlation core support planned for future iterations.

For Summerville FCU, Certificate Management strengthens member retention by providing the digital convenience that today's You expect. You who can easily renew their certificates online are more likely to keep their deposits with the credit union rather than shopping competitor rates. The feature reduces operational costs by deflecting routine certificate management inquiries from the contact center and branch staff, allowing them to focus on higher-value advisory interactions.
