**SUMMERVILLE CREDIT UNION · BUSINESS BANKING USER GUIDE · CSUM-02 of 16**

**ACH Transfer**

Module: Business Banking > ACH Payment — Send Money

**Navigation: Dashboard → Business Banking → ACH Transfer**

*Sources: Summerville Reports Series A + Series B | Features: nFinia Documentation Features Spreadsheet*

## PRODUCT SUMMARY

The ACH Transfer feature enables business members to send and receive funds electronically through the Automated Clearing House network. The workflow supports both outbound payments (Send Money) to external transfer accounts and inbound collection (Receive Money) from external sources. The transfer follows a guided three-step process: Set up Transfer, Review, and Finish.

Business users select a source account, choose or add an external transfer account as the destination, enter the transfer amount, and optionally provide a description and scheduling details. The system enforces role-based transaction limits set by the business admin, and high-value transactions may trigger OTP verification for additional security. Upon completion, a confirmation screen displays the transaction reference and status.

For credit unions, ACH transfer is a foundational business banking capability that directly competes with commercial banks. Offering a streamlined, self-service ACH workflow reduces operational overhead for both the credit union and its business members.

**At a Glance**


| Attribute            | Detail                                               |
| -------------------- | ---------------------------------------------------- |
| Feature Name         | ACH Transfer                                         |
| Module               | Business Banking > ACH Payment — Send Money          |
| Navigation           | Dashboard → Business Banking → ACH Transfer          |
| User Roles           | Business Owner, Authorized Signer                    |
| Access Level         | Role-based with transaction limits                   |
| Key Actions          | Send Money, Receive Money, Schedule, Review, Confirm |
| Regulatory Relevance | NACHA ACH Rules, Regulation E, BSA/AML monitoring    |


## KEY USE CASES


| Use Case                | Who Uses It       | What They Do                                  | Business Value                                                 |
| ----------------------- | ----------------- | --------------------------------------------- | -------------------------------------------------------------- |
| Vendor Payment          | Business Owner    | Send ACH payment to vendor external account   | Self-service payment reduces check-writing and processing time |
| Payroll Distribution    | Authorized Signer | Send payroll ACH to employee bank accounts    | Digital payroll reduces manual processing burden               |
| Invoice Collection      | Business Owner    | Receive Money from customer external account  | Automated receivables collection improves cash flow            |
| Scheduled Payment       | Business Owner    | Set future date or recurring schedule for ACH | Automates recurring vendor payments                            |
| High-Value Verification | Authorized Signer | Complete OTP verification for large transfers | Additional security layer for high-risk transactions           |


## STEP-BY-STEP USER GUIDE

**How to get here: Dashboard → Business Banking → ACH Transfer**

**Step 1: Log In and Open the Dashboard**

Open your web browser and navigate to the Summerville Credit Union digital banking platform. Enter your username and password on the login screen and click "Log In." If prompted, complete the OTP (One-Time Passcode) verification by entering the code sent to your registered device. After successful authentication, you will land on the Dashboard — also called the Account Overview screen. This is your home base. The Dashboard displays all your business accounts (Savings Accounts, Checking Accounts) with their available and current balances. The top navigation bar shows links to Dashboard, Accounts, Transfer & Pay, Cards, Business Banking, and More. On the right sidebar you will see Related Links (Change Password, Account Settings, View Scheduled Transfers, Account Specific Alerts) and a Quick Transfer widget for fast internal transfers. To proceed to Business Banking features, locate the "Business Banking" tab in the top navigation bar and click on it.

<figure><img src="/.gitbook/assets/img_5c532a850867.png" alt="Figure 1 — Log In and Open the Dashboard" width="620"><figcaption></figcaption></figure>

*Figure 1 — Log In and Open the Dashboard*

**Step 2: Open the Business Banking Hub**

After clicking "Business Banking" in the top navigation bar, the Business Banking Hub loads. This is the central command center for all commercial banking operations. The Hub is organized into three sections: "Transfers" at the top (with tiles for ACH Transfer, Domestic Wire Transfer, Transfer Template, and Payment From File), "Manage" in the middle (with tiles for Role Management, User Management, Approval Settings, and Recipient Management), and "More Options" at the bottom (with tiles for Commercial Activity, Reports, and Approvals). Each tile is a direct entry point to its corresponding feature. Only tiles your role has permission to access will be visible. From here, locate and click the tile for the feature you need — the next steps will guide you through the specific workflow.

<figure><img src="/.gitbook/assets/img_04cfec25c89e.png" alt="Figure 2 — Open the Business Banking Hub" width="620"><figcaption></figcaption></figure>

*Figure 2 — Open the Business Banking Hub*

**Step 3: Navigate to ACH Transfer**

From the Dashboard, click "Business Banking" in the left-side navigation menu. The Business Banking Hub appears. Locate the "Transfers" section at the top of the Hub and click the "ACH Transfer" tile. The ACH Transfer screen opens to Step 1 — "Set up Transfer" with the "Send Money" tab active. You will see a stepper indicator at the top showing three phases: Set up Transfer (highlighted), Review, and Finish. The "From" field is pre-populated with your primary business account (e.g., Business Money Market Account). Below it, the "To" field prompts you to select an External Transfer Account as the payment destination.

<figure><img src="/.gitbook/assets/img_f2a4e3832b99.png" alt="Figure 3 — Navigate to ACH Transfer" width="620"><figcaption></figcaption></figure>

*Figure 3 — Navigate to ACH Transfer*

**Step 4: Select the Destination Account**

Click the "To" dropdown field. A scrollable list of all your pre-configured external transfer accounts appears. These are accounts previously saved through Recipient Management. Each entry shows the recipient's name and masked account number. Scroll through the list and click on the recipient you wish to pay. If your intended recipient does not appear in the list, you will need to add them first via Recipient Management (navigate back to the Hub, click "Recipient Management" under Manage, and add the new account). Once added, return to ACH Transfer and the new recipient will appear in this dropdown.

<figure><img src="/.gitbook/assets/img_b18ef7690214.png" alt="Figure 4 — Select the Destination Account" width="620"><figcaption></figcaption></figure>

*Figure 4 — Select the Destination Account*

**Step 5: Enter the Transfer Amount**

After selecting the destination account, the Amount field appears below. Click into the Amount field and type the dollar amount you wish to send (e.g., 500.00). The system will validate this amount against your role's per-transaction limit and daily cumulative ACH limit. If the amount exceeds your configured limit, the system will block the transaction or require additional verification in a later step. Ensure the amount is correct before proceeding — you will have a chance to review it again on the next screen, but entering the correct amount here saves time.

<figure><img src="/.gitbook/assets/img_2db0218ef1af.png" alt="Figure 5 — Enter the Transfer Amount" width="620"><figcaption></figcaption></figure>

*Figure 5 — Enter the Transfer Amount*

**Step 6: Fill in Description, Date, and Frequency**

Below the Amount field, you will see additional optional fields. In the "Description" field, enter a memo or reference (such as an invoice number or payment note) — this text will appear on the recipient's bank statement. Click the "Effective Date" field to open a date picker and select when the transfer should be processed. If you want this to be a one-time payment, leave the frequency as "One Time." If you need a recurring payment (weekly, bi-weekly, monthly), use the Frequency dropdown to set the schedule. These fields help you automate regular payments and maintain clear records.

<figure><img src="/.gitbook/assets/img_645d70f5babf.png" alt="Figure 6 — Fill in Description, Date, and Frequency" width="620"><figcaption></figcaption></figure>

*Figure 6 — Fill in Description, Date, and Frequency*

**Step 7: Review Your Entries and Click Continue**

Scroll to the bottom of the form to verify all fields are completed: From account, To account, Amount, Description, Effective Date, and Frequency. Review each entry carefully. When everything looks correct, click the "Continue" button at the bottom of the form. This will advance you to Step 2 — Review. If you need to change anything, simply click on the field you wish to edit before clicking Continue. The Continue button will only become active once all required fields are filled in.

<figure><img src="/.gitbook/assets/img_aa246bc133c4.png" alt="Figure 7 — Review Your Entries and Click Continue" width="620"><figcaption></figcaption></figure>

*Figure 7 — Review Your Entries and Click Continue*

**Step 8: Review the Transfer Summary**

You are now on Step 2 — "Review." The stepper at the top highlights the Review phase. The screen displays a read-only summary of your ACH transfer: source account, destination account, transfer amount, description, effective date, and frequency. Read through every detail carefully. This is your last chance to catch errors before submission. If you spot a mistake, click "Back" to return to Step 1 and correct it. If everything is accurate, click "Submit" (or "Continue") to proceed to confirmation.

<figure><img src="/.gitbook/assets/img_1b5a91dd70cc.png" alt="Figure 8 — Review the Transfer Summary" width="620"><figcaption></figcaption></figure>

*Figure 8 — Review the Transfer Summary*

**Step 9: Verify the Description/Memo Text**

Take a moment to verify the description/memo field in the review summary. This is the text that will travel with the ACH transaction and appear on the recipient's bank statement. Make sure it contains the correct reference information (invoice number, PO number, or payment purpose). If your organization uses specific coding conventions for payments, confirm the description follows your standard format. A clear, accurate description enables easy reconciliation for both your business and the recipient.

<figure><img src="/.gitbook/assets/img_e700f3ffdd96.png" alt="Figure 9 — Verify the Description/Memo Text" width="620"><figcaption></figcaption></figure>

*Figure 9 — Verify the Description/Memo Text*

**Step 10: Confirm and Submit the Payment**

On the final review screen, verify the complete transaction summary one last time: From account, To account, Amount, Description, Effective Date, and Frequency. When you are satisfied that all details are correct, click the "Submit" button. If your business has dual-control approval settings configured (set in Approval Settings), the transaction will be routed to the Approvals queue for a second authorized user to approve before processing. If no dual-control is required, the payment advances directly to the next step.

<figure><img src="/.gitbook/assets/img_635c9465ee1b.png" alt="Figure 10 — Confirm and Submit the Payment" width="620"><figcaption></figcaption></figure>

*Figure 10 — Confirm and Submit the Payment*

**Step 11: Acknowledge the Confirmation Dialog**

After clicking Submit, a confirmation dialog appears in the center of the screen. This dialog restates the payment amount and asks you to confirm one final time. Click "Yes, Submit" (or the equivalent confirm button) to authorize the payment. Click "Cancel" if you want to abort. This two-click pattern (Submit + Confirm) is a safety mechanism to prevent accidental payments. The dialog requires your deliberate action — it will not auto-dismiss or time out.

<figure><img src="/.gitbook/assets/img_242dceeb7e42.png" alt="Figure 11 — Acknowledge the Confirmation Dialog" width="620"><figcaption></figcaption></figure>

*Figure 11 — Acknowledge the Confirmation Dialog*

**Step 12: Enter the One-Time Passcode (If Required)**

If the transfer amount exceeds your role's standard threshold, the system will display an OTP (One-Time Passcode) verification screen. Check your registered mobile device or email for a 5-digit verification code. Enter the code in the individual digit boxes shown on screen. Click "Verify" (or equivalent) to proceed. If you did not receive the code, click "Resend" to request a new one. The OTP expires after a short time window, so enter it promptly. This security step ensures that even if your session were compromised, a high-value transfer cannot be completed without access to your physical device.

<figure><img src="/.gitbook/assets/img_24bf28a3900c.png" alt="Figure 12 — Enter the One-Time Passcode (If Required)" width="620"><figcaption></figcaption></figure>

*Figure 12 — Enter the One-Time Passcode (If Required)*

**Step 13: View the Success Confirmation**

The screen advances to Step 3 — "Finish." A success confirmation is displayed with a green checkmark or success indicator. You will see the completed transaction details: confirmation/reference number, transfer amount, source and destination accounts, and processing status. Save or note down the confirmation number for your records — you can use it for future reference, reconciliation, or dispute resolution. From this screen, you can click to start a new transfer or navigate back to the Business Banking Hub. The transaction now appears in your Commercial Activity ledger.

<figure><img src="/.gitbook/assets/img_3015d8ecaca2.png" alt="Figure 13 — View the Success Confirmation" width="620"><figcaption></figcaption></figure>

*Figure 13 — View the Success Confirmation*

