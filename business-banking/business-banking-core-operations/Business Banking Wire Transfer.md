**SUMMERVILLE CREDIT UNION · BUSINESS BANKING USER GUIDE · CSUM-03 of 16**

**Domestic Wire Transfer**

Module: Business Banking > Domestic Wire Transfer

**Navigation: Dashboard → Business Banking → Domestic Wire Transfer**

*Sources: Summerville Reports Series A + Series B | Features: nFinia Documentation Features Spreadsheet*

## PRODUCT SUMMARY

The Domestic Wire Transfer feature allows business members to send same-day, irrevocable fund transfers to domestic bank accounts through the Federal Reserve wire system. Wire transfers are used for high-value, time-sensitive payments where ACH settlement timelines are insufficient. The workflow mirrors the ACH transfer with a three-step guided process: Set up Transfer, Review, and Finish.

The user selects a source account, picks a pre-configured wire transfer account, enters the amount, and provides wire-specific details including beneficiary information. Wire transfers are subject to stricter limits and may require dual-control approval depending on the business approval settings. OTP verification is enforced for all wire submissions.

For credit unions, offering domestic wire capabilities is essential to serve business members who need to make real estate closings, vendor deposits, or emergency payments that cannot wait for ACH processing.

**At a Glance**


| Attribute            | Detail                                                                |
| -------------------- | --------------------------------------------------------------------- |
| Feature Name         | Domestic Wire Transfer                                                |
| Module               | Business Banking > Domestic Wire Transfer                             |
| Navigation           | Dashboard → Business Banking → Domestic Wire Transfer                 |
| User Roles           | Business Owner, Authorized Signer                                     |
| Access Level         | Role-based with wire-specific limits; dual-control approval may apply |
| Key Actions          | Initiate Wire, Review, Confirm, OTP Verify                            |
| Regulatory Relevance | Regulation J, BSA/AML, OFAC screening, dual-control requirements      |


## KEY USE CASES


| Use Case              | Who Uses It       | What They Do                                        | Business Value                                          |
| --------------------- | ----------------- | --------------------------------------------------- | ------------------------------------------------------- |
| Real Estate Closing   | Business Owner    | Send same-day wire for property purchase or closing | Enables time-critical high-value payments               |
| Vendor Deposit        | Authorized Signer | Wire payment to vendor requiring immediate funds    | Same-day settlement meets urgent payment deadlines      |
| Dual-Control Wire     | Authorized Signer | Submit wire that requires second approval           | Dual-control reduces fraud risk on high-value transfers |
| Wire to New Recipient | Business Owner    | Select from saved wire transfer accounts            | Pre-configured recipients reduce errors in wire details |


## STEP-BY-STEP USER GUIDE

**How to get here: Dashboard → Business Banking → Domestic Wire Transfer**

**Step 1: Log In and Open the Dashboard**

Open your web browser and navigate to the Summerville Credit Union digital banking platform. Enter your username and password on the login screen and click "Log In." If prompted, complete the OTP (One-Time Passcode) verification by entering the code sent to your registered device. After successful authentication, you will land on the Dashboard — also called the Account Overview screen. This is your home base. The Dashboard displays all your business accounts (Savings Accounts, Checking Accounts) with their available and current balances. The top navigation bar shows links to Dashboard, Accounts, Transfer & Pay, Cards, Business Banking, and More. On the right sidebar you will see Related Links (Change Password, Account Settings, View Scheduled Transfers, Account Specific Alerts) and a Quick Transfer widget for fast internal transfers. To proceed to Business Banking features, locate the "Business Banking" tab in the top navigation bar and click on it.

<figure><img src="/.gitbook/assets/img_5c532a850867.png" alt="Figure 1 — Log In and Open the Dashboard" width="620"><figcaption></figcaption></figure>

*Figure 1 — Log In and Open the Dashboard*

**Step 2: Open the Business Banking Hub**

After clicking "Business Banking" in the top navigation bar, the Business Banking Hub loads. This is the central command center for all commercial banking operations. The Hub is organized into three sections: "Transfers" at the top (with tiles for ACH Transfer, Domestic Wire Transfer, Transfer Template, and Payment From File), "Manage" in the middle (with tiles for Role Management, User Management, Approval Settings, and Recipient Management), and "More Options" at the bottom (with tiles for Commercial Activity, Reports, and Approvals). Each tile is a direct entry point to its corresponding feature. Only tiles your role has permission to access will be visible. From here, locate and click the tile for the feature you need — the next steps will guide you through the specific workflow.

<figure><img src="/.gitbook/assets/img_04cfec25c89e.png" alt="Figure 2 — Open the Business Banking Hub" width="620"><figcaption></figcaption></figure>

*Figure 2 — Open the Business Banking Hub*

**Step 3: Navigate to Domestic Wire Transfer**

From the Dashboard, click "Business Banking" in the left-side navigation menu to open the Business Banking Hub. In the Transfers section at the top, click the "Domestic Wire Transfer" tile. The Wire Transfer screen opens to Step 1 — "Set up Transfer." The "From" field is pre-populated with your business account (e.g., Business Money Market Account) showing the credit union name (Summerville CU) and masked account number. Below it, the "To" field prompts you to select a saved Wire Transfer Account. Note: Wire recipients are separate from ACH recipients — they contain additional beneficiary bank routing details required by the Fedwire system.

<figure><img src="/.gitbook/assets/img_75362dbdbb04.png" alt="Figure 3 — Navigate to Domestic Wire Transfer" width="620"><figcaption></figcaption></figure>

*Figure 3 — Navigate to Domestic Wire Transfer*

**Step 4: Select the Wire Recipient**

Click the "To" dropdown to expand the list of saved wire transfer accounts. Each entry shows the beneficiary name and associated bank details. Scroll through and click on the recipient you want to wire funds to. If the recipient you need is not listed, you must first add them through Recipient Management (go back to the Hub → Recipient Management → Add Transfer Account, and select "Wire" as the account type). Important: Wire transfers are irrevocable once submitted. There is no recall mechanism, so double-check you are selecting the correct beneficiary before proceeding.

<figure><img src="/.gitbook/assets/img_231cf092d0df.png" alt="Figure 4 — Select the Wire Recipient" width="620"><figcaption></figcaption></figure>

*Figure 4 — Select the Wire Recipient*

**Step 5: Verify the Selected Beneficiary**

After selecting a wire transfer account, the "To" field displays the beneficiary's name and account details. Verify that both the "From" account (your business account) and the "To" account (the wire beneficiary) are correct. The screen now shows both parties side by side so you can confirm the payment direction. If you selected the wrong recipient, click the "To" dropdown again to change your selection. Do not proceed to the amount entry until you have confirmed the correct beneficiary, as wire errors are extremely difficult to reverse.

<figure><img src="/.gitbook/assets/img_8353b8218d8b.png" alt="Figure 5 — Verify the Selected Beneficiary" width="620"><figcaption></figcaption></figure>

*Figure 5 — Verify the Selected Beneficiary*

**Step 6: Enter the Wire Amount**

Click into the Amount field and enter the dollar amount for the wire transfer. Wire transfers typically involve larger amounts than ACH ($10,000+). The system validates your entry against your role's per-transaction wire limit and daily wire cumulative limit (configured in Role Management → Limits). If the amount exceeds your role's threshold, the transaction will be flagged for dual-control approval or additional verification. Enter the exact amount including cents (e.g., 25000.00). Verify the amount is correct before proceeding.

<figure><img src="/.gitbook/assets/img_b67b27aada0b.png" alt="Figure 6 — Enter the Wire Amount" width="620"><figcaption></figcaption></figure>

*Figure 6 — Enter the Wire Amount*

**Step 7: Complete Additional Wire Details and Continue**

Scroll to the bottom of the wire transfer form. Fill in any additional required fields: beneficiary bank details, wire reference information, and any special instructions. These fields capture the detail required by the Fedwire system for processing. Once all fields are complete, the "Continue" button becomes active. Review all entries one final time, then click "Continue" to advance to Step 2 — Review. Incomplete or inaccurate wire details are the most common cause of wire transfer failures, so take extra care at this step.

<figure><img src="/.gitbook/assets/img_b4bab0125ea4.png" alt="Figure 7 — Complete Additional Wire Details and Continue" width="620"><figcaption></figcaption></figure>

*Figure 7 — Complete Additional Wire Details and Continue*

**Step 8: Review and Submit the Wire Transfer**

You are now on Step 2 — "Review." The screen presents a comprehensive summary of your wire transfer: source account, beneficiary name and account, wire amount, beneficiary bank routing number, and any reference notes. Read every detail carefully — wire transfers are irrevocable once released. If you spot an error, click "Back" to return to Step 1 and make corrections. If everything is accurate, click "Submit." The system will then prompt OTP verification (a one-time passcode sent to your registered device). After OTP verification, the wire is submitted. If your business has dual-control configured for wires (in Approval Settings), the wire goes to the Approvals queue for a second authorized user to approve before release.

<figure><img src="/.gitbook/assets/img_31af89da007e.png" alt="Figure 8 — Review and Submit the Wire Transfer" width="620"><figcaption></figcaption></figure>

*Figure 8 — Review and Submit the Wire Transfer*

