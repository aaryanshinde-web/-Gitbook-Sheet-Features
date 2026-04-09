**Dashboard Quick Links**

Security Policy, Branch Appointments, Locations, Rates & Text Banking

nFinia Digital Banking Platform

Summerville Federal Credit Union

Product Guide \| April 2026

  ------------------------
  **1. Product Summary**
  ------------------------

The nFinia Dashboard Quick Links provide You with instant access to essential credit union information and services directly from the bottom of the post-login dashboard. These five footer links --- Security Policy, Branch Appointments, Locations, Rates, and Text Banking --- serve as persistent navigation anchors that connect the digital banking experience to the credit union's broader service ecosystem.

Security Policy connects You to the credit union's online security guidelines and fraud prevention resources. Branch Appointments integrates with the Penni scheduling platform to enable self-service appointment booking at physical branches. Locations and Rates link to the Tyfone nFinia platform's public-facing pages displaying branch details, ATM locations, and current interest rates. Text Banking provides a command reference for SMS-based banking services, allowing You to check balances and transaction history via text message.

Together, these quick links bridge the gap between digital and physical banking channels, ensuring You can access critical information without leaving their authenticated session.

**At a Glance**

  -------------------- -----------------------------------------------------------------------------------------
  **Attribute**        **Detail**
  Feature Name         Dashboard Quick Links (Footer Navigation)
  Module               Dashboard > Footer Section
  User Roles           All authenticated You (Personal & Business)
  Access Level         Post-login; visible on all dashboard views
  Key Links            Security Policy, Branch Appointments, Locations, Rates, Text Banking
  Integration Points   Penni (appointments), Tyfone public pages (locations/rates), SMS gateway (text banking)
  -------------------- -----------------------------------------------------------------------------------------

  ------------------
  **2. Use Cases**
  ------------------

  -------------------------------- ---------------------- ------------------------------------------------------------------------------ ----------------------------------------------------------------
  **Use Case**                     **Who Uses It**        **What They Do**                                                               **Business Value**
  Review security practices        Any Member             Clicks Security Policy to read fraud prevention tips and security guidelines   Reduces social engineering and phishing success rates
  Book a branch appointment        Personal Member        Clicks Branch Appointments to schedule a visit via Penni                       Reduces walk-in wait times; improves branch efficiency
  Find branch or ATM               Any Member             Clicks Locations to view branches, hours, and ATM network on the platform      Drives foot traffic; reduces support calls for branch info
  Check current rates              Prospective Borrower   Clicks Rates to view loan, savings, and certificate rates on the platform      Encourages product adoption; transparent rate disclosure
  Set up text banking              Mobile Member          Clicks Text Banking to view SMS commands (SV BAL, SV HIST, etc.)               Extends banking access to basic phones; quick balance checks
  Quick reference during session   Any Member             Uses footer links during an active banking session without logging out         Seamless cross-channel experience without session interruption
  -------------------------------- ---------------------- ------------------------------------------------------------------------------ ----------------------------------------------------------------

The Dashboard Quick Links serve as an always-available bridge between digital banking and the credit union's physical and communication channels. For Summerville FCU, these links drive engagement across all service channels while keeping you within the authenticated digital experience.

  ----------------------------
  **3. End-to-End Workflow**
  ----------------------------

**3.1 Dashboard Overview**

The Summerville FCU dashboard is your primary landing page after login. It displays account balances, Quick Transfer, upcoming payments, credit score, and related links. At the very bottom of the dashboard, the footer section contains the five quick links.

<figure><img src="/.gitbook/assets/24c30f617e73e6629d17809c27be42eacd3ba8fb.png" alt="" width="340"><figcaption></figcaption></figure>{width="4.791666666666667in" height="7.520833333333333in"}

**3.2 Security Policy**

The Security Policy link opens the credit union's security guidelines page. This page outlines best practices for online banking safety, including password management, phishing awareness, device security, and what to do if fraud is suspected. The content is maintained by the credit union and served through the nFinia platform.

**3.3 Branch Appointments (Penni Integration)**

Clicking Branch Appointments launches the Penni scheduling platform. Penni provides a multi-step appointment booking flow: Personal Info, Appointment Type, Date & Time, and Confirmation. You enter their name, email, phone number, and can optionally add notes before selecting an available time slot at their preferred branch.

<figure><img src="/.gitbook/assets/5b13eb218018fc050193b60811631162d4f8078c.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.625in" height="4.197916666666667in"}

**3.4 Locations & Rates**

The Locations and Rates links connect to Summerville FCU's pages on the Tyfone nFinia platform. The platform --- branded as "Dramatically Different: Digital Banking + Payments + AI" --- hosts the credit union's branch locator with hours, addresses, and ATM information, as well as current rate tables for savings, checking, certificates, and loan products.

<figure><img src="/.gitbook/assets/964a5c60cb2fb66a33a7a9655ca4baef87341ccf.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.833333333333333in" height="3.0625in"}

**3.5 Text Banking**

The Text Banking link opens a reference page listing all available SMS commands. You send text commands to the short code 28640 to interact with their accounts. Available commands include SV HELP (list commands), SV BAL (default account balance), SV BAL ALL (all account balances), SV HIST (transaction history), and SV STOP (deactivate text banking).

<figure><img src="/.gitbook/assets/d81a50f5a5078c8188072b36c8634d6e9fe78a9b.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.833333333333333in" height="3.0729166666666665in"}

**3.6 Completion**

Each quick link opens the relevant content within the platform or in an integrated partner service (Penni). You can navigate back to the dashboard at any time using the top navigation bar. No confirmation or submission is required for informational links (Security Policy, Locations, Rates, Text Banking). The Branch Appointments flow through Penni concludes with a confirmation screen and email/SMS notification.

  -------------------------
  **4. Feature Overview**
  -------------------------

**4.1 Security Policy Page**

The Security Policy page provides credit union You with essential security information to protect their accounts and personal data.

  --------------------- --------------- ----------------------------------------------------------- ----------------------------------
  **Field / Element**   **Type**        **Description**                                             **Notes**
  Page Title            Heading         Security Policy / Online Security                           Branded with Summerville styling
  Security Guidelines   Content Block   Best practices for password, device, and account security   Maintained by FI; CMS-editable
  Fraud Reporting       Content Block   Instructions for reporting suspected fraud                  Includes phone number and email
  Footer Navigation     Links           Return to Dashboard and other quick links                   Persistent footer available
  --------------------- --------------- ----------------------------------------------------------- ----------------------------------

**4.2 Branch Appointments (Penni)**

The Penni appointment scheduling flow guides You through a four-step process to book a branch visit.

  ----------------------------------- ------------------ ------------------------------------------------------------------ ------------------------------------------
  **Field / Element**                 **Type**           **Description**                                                    **Notes**
  First Name                          Input              your first name                                                Required
  Last Name                           Input              your last name                                                 Required
  Your Email                          Input              Email for confirmation delivery                                    Required; validated format
  Your Phone                          Input              Phone number for SMS reminders                                     Required; formatted input
  Receive text message confirmation   Checkbox           Opt-in for SMS appointment reminders                               Optional; standard messaging rates apply
  Additional Information              Textarea           Notes for the branch staff                                         Optional; do not include sensitive info
  Continue                            Button (Primary)   Advances to Appointment Type step                                  Validates required fields
  Progress Steps                      Stepper            Personal Info > Appointment Type > Date & Time > Confirmation   Visual progress indicator
  ----------------------------------- ------------------ ------------------------------------------------------------------ ------------------------------------------

**4.3 Locations & Rates (Tyfone Platform)**

The Locations and Rates pages are hosted on the Tyfone nFinia platform and display branch, ATM, and rate information.

  --------------------------------------- ------------------------ ------------------------------------------------------- -------------------------------------
  **Field / Element**                     **Type**                 **Description**                                         **Notes**
  Branch Locator                          Interactive Map / List   Shows all branch locations with addresses and hours     Filterable by service type
  ATM Network                             Map / List               Displays shared ATM network locations                   Includes surcharge-free ATMs
  Savings Rates                           Rate Table               Current APY for savings and money market products       Updated per FI schedule
  Certificate Rates                       Rate Table               Current APY by term for share certificates              Updated per FI schedule
  Loan Rates                              Rate Table               Current rates for auto, personal, mortgage, and HELOC   Updated per FI schedule
  See our solution / Learn our strategy   CTA Buttons              Platform marketing CTAs on Tyfone page                  Links to Tyfone product information
  --------------------------------------- ------------------------ ------------------------------------------------------- -------------------------------------

**4.4 Text Banking**

The Text Banking page provides a command reference for SMS-based banking services. You text commands to short code 28640 to interact with their accounts.

  ------------------ ------------- ----------------------------------------------------- -------------------------------------------
  **Text Command**   **Type**      **Description**                                       **Notes**
  SV HELP            SMS Command   Returns the list of available text commands           Starting point for new text banking users
  SV BAL             SMS Command   Returns the balance of the default account            Quick balance check without login
  SV BAL ALL         SMS Command   Returns balances for all linked accounts              Full account overview via text
  SV HIST            SMS Command   Returns transaction history for the default account   Recent transactions only
  SV STOP            SMS Command   Deactivates the text banking service                  Can be re-enabled through digital banking
  ------------------ ------------- ----------------------------------------------------- -------------------------------------------

  ------------------------
  **5. Quick Reference**
  ------------------------

  -------------------------- ----------------------------------------- ------------------- --------------------------------------
  **Task**                   **Navigation Path**                       **Who Can Do It**   **Notes**
  View security guidelines   Dashboard Footer > Security Policy       All You         Informational; no action required
  Book branch appointment    Dashboard Footer > Branch Appointments   All You         Opens Penni scheduling flow
  Find branch or ATM         Dashboard Footer > Locations             All You         Platform-hosted locator page
  View current rates         Dashboard Footer > Rates                 All You         Platform-hosted rate tables
  Set up text banking        Dashboard Footer > Text Banking          All You         SMS to 28640 with SV prefix commands
  Check balance via text     Text \'SV BAL\' to 28640                  Enrolled You    No login required; instant response
  -------------------------- ----------------------------------------- ------------------- --------------------------------------

  -------------------
  **6. Conclusion**
  -------------------

The Dashboard Quick Links provide Summerville Federal Credit Union You with seamless access to essential services and information directly from their digital banking dashboard. By integrating Security Policy, Branch Appointments (via Penni), Locations, Rates, and Text Banking into persistent footer navigation, the nFinia platform creates a unified experience that connects digital and physical banking channels.

These features reduce the need for You to search the credit union website separately, lower call center volume for routine inquiries, and drive engagement across all service channels. The Penni appointment integration is particularly valuable, enabling You to schedule branch visits without leaving their authenticated session. Text Banking extends account access to the simplest mobile devices, ensuring no you are left behind in the digital transformation.

For Summerville FCU, maintaining these quick links demonstrates a commitment to member convenience and multi-channel service delivery that differentiates the credit union in a competitive market.
