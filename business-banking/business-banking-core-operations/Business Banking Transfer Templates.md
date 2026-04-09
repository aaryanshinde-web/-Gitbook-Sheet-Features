**SUMMERVILLE CREDIT UNION · BUSINESS BANKING USER GUIDE · CSUM-04 of 16**

**Transfer Templates**

Module: Business Banking > Payments > Transfer Templates

**Navigation: Dashboard → Business Banking → Transfer Template**

*Sources: Summerville Reports Series A + Series B | Features: nFinia Documentation Features Spreadsheet*

## PRODUCT SUMMARY

Transfer Templates allow business members to create reusable payment configurations for frequently executed ACH and wire transfers. Instead of re-entering recipient details, amounts, and routing information each time, users can save a template and execute it with a single click. Templates support multiple payment types including ACH Payments (CCD), Collections, Payroll, and Domestic Wire Transfers.

The template management screen displays all saved templates in a searchable list with columns for template name, type, number of recipients, last run date, and last paid amount. Business admins can create new templates by selecting a payment type, adding one or more payees, setting amounts, and configuring SEC codes for ACH compliance.

For credit unions, templates are a critical feature for business member retention. Businesses that build templates into their payment workflows become deeply embedded in the platform, increasing switching costs and long-term loyalty.

**At a Glance**


| Attribute            | Detail                                                     |
| -------------------- | ---------------------------------------------------------- |
| Feature Name         | Transfer Templates                                         |
| Module               | Business Banking > Payments > Transfer Templates           |
| Navigation           | Dashboard → Business Banking → Transfer Template           |
| User Roles           | Business Owner, Authorized Signer, Business Admin          |
| Access Level         | Role-based; template creation may require admin privileges |
| Key Actions          | Create, Edit, Run, Delete templates                        |
| Regulatory Relevance | NACHA SEC Code compliance for ACH templates                |


## KEY USE CASES


| Use Case                 | Who Uses It       | What They Do                                                    | Business Value                                                    |
| ------------------------ | ----------------- | --------------------------------------------------------------- | ----------------------------------------------------------------- |
| Recurring Vendor Payment | Business Owner    | Create ACH template for monthly vendor payment                  | Eliminates repetitive data entry for regular payments             |
| Payroll Template         | Business Admin    | Set up payroll template with multiple employee recipients       | One-click payroll execution for all employees                     |
| Wire Template            | Authorized Signer | Create domestic wire template for recurring high-value payments | Reduces wire detail errors and speeds up time-sensitive transfers |
| Template Execution       | Business Owner    | Run existing template to execute saved payment                  | Instant payment execution from saved configuration                |


## STEP-BY-STEP USER GUIDE

**How to get here: Dashboard → Business Banking → Transfer Template**

**Step 1: Log In and Open the Dashboard**

Open your web browser and navigate to the Summerville Credit Union digital banking platform. Enter your username and password on the login screen and click "Log In." If prompted, complete the OTP (One-Time Passcode) verification by entering the code sent to your registered device. After successful authentication, you will land on the Dashboard — also called the Account Overview screen. This is your home base. The Dashboard displays all your business accounts (Savings Accounts, Checking Accounts) with their available and current balances. The top navigation bar shows links to Dashboard, Accounts, Transfer & Pay, Cards, Business Banking, and More. On the right sidebar you will see Related Links (Change Password, Account Settings, View Scheduled Transfers, Account Specific Alerts) and a Quick Transfer widget for fast internal transfers. To proceed to Business Banking features, locate the "Business Banking" tab in the top navigation bar and click on it.

<figure><img src="/.gitbook/assets/img_5c532a850867.png" alt="Figure 1 — Log In and Open the Dashboard" width="620"><figcaption></figcaption></figure>

*Figure 1 — Log In and Open the Dashboard*

**Step 2: Open the Business Banking Hub**

After clicking "Business Banking" in the top navigation bar, the Business Banking Hub loads. This is the central command center for all commercial banking operations. The Hub is organized into three sections: "Transfers" at the top (with tiles for ACH Transfer, Domestic Wire Transfer, Transfer Template, and Payment From File), "Manage" in the middle (with tiles for Role Management, User Management, Approval Settings, and Recipient Management), and "More Options" at the bottom (with tiles for Commercial Activity, Reports, and Approvals). Each tile is a direct entry point to its corresponding feature. Only tiles your role has permission to access will be visible. From here, locate and click the tile for the feature you need — the next steps will guide you through the specific workflow.

<figure><img src="/.gitbook/assets/img_04cfec25c89e.png" alt="Figure 2 — Open the Business Banking Hub" width="620"><figcaption></figcaption></figure>

*Figure 2 — Open the Business Banking Hub*

**Step 3: Navigate to Transfer Templates**

From the Dashboard, click "Business Banking" in the left-side navigation menu to open the Business Banking Hub. In the Transfers section, click the "Transfer Template" tile. The Transfer Templates dashboard appears, listing all saved payment templates in a table format. You will see filter tabs across the top: Payments, Collections, Payroll, and Domestic Wire Transfer — click any tab to filter templates by type. The table columns show Template Name, Type (e.g., Payments CCD), number of Recipients, Last Run Date, and Last Paid Amount. To run an existing template, click on its row. To create a new template, click the "Create Template" button. Use the search bar to find a specific template by name.

<figure><img src="/.gitbook/assets/img_ea06eafdf1bc.png" alt="Figure 3 — Navigate to Transfer Templates" width="620"><figcaption></figcaption></figure>

*Figure 3 — Navigate to Transfer Templates*

**Step 4: Click Create Template and Enter Details**

Click the "Create Template" button at the top of the Templates dashboard. A creation form opens. Begin by entering a descriptive Template Name (e.g., "Monthly Office Rent" or "Weekly Payroll"). Then select the Payment Type from the dropdown: ACH Payment (CCD) for vendor payments, ACH Collection for pulling funds, Payroll for employee salary distribution, or Domestic Wire for recurring wire transfers. The payment type you select determines which compliance rules and SEC codes apply. Choose carefully, as the payment type cannot be changed after the template is saved.

<figure><img src="/.gitbook/assets/img_6d1609587a04.png" alt="Figure 4 — Click Create Template and Enter Details" width="620"><figcaption></figcaption></figure>

*Figure 4 — Click Create Template and Enter Details*

**Step 5: Configure Source Account and Schedule**

After entering the template name and payment type, additional fields appear. Select the Source Account (the business account funds will be drawn from) using the account dropdown. Set the Effective Date preference: immediate processing, next business day, or a specific calendar date. If this template should run on a recurring schedule, configure the Frequency setting. The form dynamically adjusts based on your selected payment type — wire templates show additional beneficiary bank fields, while ACH templates show SEC code options. Fill in each field and scroll down to continue.

<figure><img src="/.gitbook/assets/img_dd30f9c977c5.png" alt="Figure 5 — Configure Source Account and Schedule" width="620"><figcaption></figcaption></figure>

*Figure 5 — Configure Source Account and Schedule*

**Step 6: Fill in Advanced Configuration Options**

Scroll down to see additional advanced options. These include the Batch Description (text that appears on recipient bank statements), Company Entry Description, and offsetting account settings if applicable. For payroll templates, additional fields for tax references may appear. Fill in all fields relevant to your template type. These details ensure that when the template is executed, it generates fully compliant NACHA records that meet ACH network technical requirements. Leave any optional fields blank if they do not apply to your use case.

<figure><img src="/.gitbook/assets/img_68b95e55b7fe.png" alt="Figure 6 — Fill in Advanced Configuration Options" width="620"><figcaption></figcaption></figure>

*Figure 6 — Fill in Advanced Configuration Options*

**Step 7: Select the SEC Code**

Click the SEC Code dropdown to select the appropriate Standard Entry Class code for your ACH template. Common options include CCD (Corporate Credit or Debit) for business-to-business payments and PPD (Prearranged Payment and Deposit) for employee payroll. Each code has a description to help you choose correctly. Selecting the wrong SEC code can result in NACHA rule violations, so confirm the correct code with your finance team if unsure. This field is required — you cannot proceed without selecting an SEC code. For wire templates, this field will not appear as it applies only to ACH transactions.

<figure><img src="/.gitbook/assets/img_7de66dd23b4b.png" alt="Figure 7 — Select the SEC Code" width="620"><figcaption></figcaption></figure>

*Figure 7 — Select the SEC Code*

**Step 8: Add Payees to the Template**

After configuring the header details, you will be prompted to add payees (recipients). Click "Add Payee" to open a searchable list of all saved transfer accounts from your Recipient Management directory. Click on each recipient you want to include in this template. For payroll templates, select all employees. For vendor payments, select the relevant vendor accounts. You can add multiple payees — each selected payee becomes a line item in the template. If the recipient you need is not in the list, you will need to add them through Recipient Management first, then return here.

<figure><img src="/.gitbook/assets/img_e452e14f3bdf.png" alt="Figure 8 — Add Payees to the Template" width="620"><figcaption></figcaption></figure>

*Figure 8 — Add Payees to the Template*

**Step 9: Confirm the Added Payee**

After selecting a payee, the system confirms the addition by displaying the payee's name and account details within the template. You will see a green checkmark or "Added" indicator confirming the recipient was successfully included. To add more payees, click "Add Another Payee" and repeat the selection process. Review the list of added payees to ensure all intended recipients are included. You can remove a payee by clicking the remove/delete icon next to their entry if one was added in error.

<figure><img src="/.gitbook/assets/img_764db965d644.png" alt="Figure 9 — Confirm the Added Payee" width="620"><figcaption></figcaption></figure>

*Figure 9 — Confirm the Added Payee*

**Step 10: Set Payment Amounts for Each Payee**

With all payees added, the form now displays each recipient as a row with an editable Amount field. Click into each payee's Amount field and enter the default payment amount for that recipient. For fixed recurring payments (e.g., monthly rent, fixed salaries), enter the exact amount. For variable payments, you can enter an estimated amount and update it before each template execution. The system calculates and displays the Total Template Amount at the bottom so you can verify the total outflow. Ensure all amounts are correct before saving.

<figure><img src="/.gitbook/assets/img_4e4252c23e0b.png" alt="Figure 10 — Set Payment Amounts for Each Payee" width="620"><figcaption></figcaption></figure>

*Figure 10 — Set Payment Amounts for Each Payee*

**Step 11: Save the Template**

After verifying all payees and amounts, click "Save Template" (or equivalent save button). The system displays a success confirmation showing the template name, type, number of recipients, and total amount. Your template is now saved and available in the Templates Dashboard for future use. You can navigate back to the templates list to execute it immediately, or it will be available the next time you need to run this payment. The template can be edited, duplicated, or deleted at any time by authorized users.

<figure><img src="/.gitbook/assets/img_efd8611e9d9f.png" alt="Figure 11 — Save the Template" width="620"><figcaption></figcaption></figure>

*Figure 11 — Save the Template*

**Step 12: Verify the New Template in the Dashboard**

You are returned to the Transfer Templates dashboard. Verify that your newly created template appears in the list. It will show the template name, type, recipient count, and an empty "Last Run" column since it has not been executed yet. To run the template, click on its row — the system will pre-fill all configured payment details and walk you through the standard Review → Submit workflow. To edit the template, click the edit/actions button on the template row. Your template is now ready for operational use.

<figure><img src="/.gitbook/assets/img_729fb28e7e11.png" alt="Figure 12 — Verify the New Template in the Dashboard" width="620"><figcaption></figcaption></figure>

*Figure 12 — Verify the New Template in the Dashboard*

