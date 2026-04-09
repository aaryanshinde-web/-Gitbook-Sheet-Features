**SUMMERVILLE CREDIT UNION · BUSINESS BANKING USER GUIDE · CSUM-05 of 16**

**Payment From File**

Module: Business Banking > Payments > Payments From File

**Navigation: Dashboard → Business Banking → Payment From File**

*Sources: Summerville Reports Series A + Series B | Features: nFinia Documentation Features Spreadsheet*

## PRODUCT SUMMARY

The Payment From File feature enables business members to upload batch payment files formatted according to NACHA specifications for bulk ACH processing. This is designed for businesses that generate payment files from their ERP or accounting systems and need to submit them directly through the digital banking platform without manual re-entry.

The interface provides three views: Upload (to submit new NACHA files), Active File(s) (showing files currently being processed), and Upload History (displaying previously submitted files with their processing status and details). The system validates the uploaded file format and provides clear error messaging if the file does not meet NACHA specifications.

For credit unions, payment from file is a treasury management capability that directly competes with commercial bank offerings. It enables larger businesses to maintain their existing ERP payment workflows while using the credit union for execution.

**At a Glance**


| Attribute            | Detail                                                                |
| -------------------- | --------------------------------------------------------------------- |
| Feature Name         | Payment From File                                                     |
| Module               | Business Banking > Payments > Payments From File                      |
| Navigation           | Dashboard → Business Banking → Payment From File                      |
| User Roles           | Business Owner, Authorized Signer                                     |
| Access Level         | Role-based; requires ACH payment permissions                          |
| Key Actions          | Upload file, View active files, View upload history, Download details |
| Regulatory Relevance | NACHA file format compliance, BSA/AML batch monitoring                |


## KEY USE CASES


| Use Case             | Who Uses It       | What They Do                                               | Business Value                                             |
| -------------------- | ----------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| ERP Payroll Upload   | Business Owner    | Upload NACHA file from payroll system for batch processing | Bridges ERP systems with credit union payment rails        |
| Vendor Batch Payment | Authorized Signer | Submit batch ACH file for multiple vendor payments         | Single file upload replaces dozens of individual transfers |
| File Status Tracking | Business Owner    | Monitor active files and review upload history             | Visibility into batch processing status and outcomes       |
| Failed File Review   | Business Admin    | Review rejected file details and error messages            | Quick identification and resolution of file format issues  |


## STEP-BY-STEP USER GUIDE

**How to get here: Dashboard → Business Banking → Payment From File**

**Step 1: Log In and Open the Dashboard**

Open your web browser and navigate to the Summerville Credit Union digital banking platform. Enter your username and password on the login screen and click "Log In." If prompted, complete the OTP (One-Time Passcode) verification by entering the code sent to your registered device. After successful authentication, you will land on the Dashboard — also called the Account Overview screen. This is your home base. The Dashboard displays all your business accounts (Savings Accounts, Checking Accounts) with their available and current balances. The top navigation bar shows links to Dashboard, Accounts, Transfer & Pay, Cards, Business Banking, and More. On the right sidebar you will see Related Links (Change Password, Account Settings, View Scheduled Transfers, Account Specific Alerts) and a Quick Transfer widget for fast internal transfers. To proceed to Business Banking features, locate the "Business Banking" tab in the top navigation bar and click on it.

<figure><img src="/.gitbook/assets/img_5c532a850867.png" alt="Figure 1 — Log In and Open the Dashboard" width="620"><figcaption></figcaption></figure>

*Figure 1 — Log In and Open the Dashboard*

**Step 2: Open the Business Banking Hub**

After clicking "Business Banking" in the top navigation bar, the Business Banking Hub loads. This is the central command center for all commercial banking operations. The Hub is organized into three sections: "Transfers" at the top (with tiles for ACH Transfer, Domestic Wire Transfer, Transfer Template, and Payment From File), "Manage" in the middle (with tiles for Role Management, User Management, Approval Settings, and Recipient Management), and "More Options" at the bottom (with tiles for Commercial Activity, Reports, and Approvals). Each tile is a direct entry point to its corresponding feature. Only tiles your role has permission to access will be visible. From here, locate and click the tile for the feature you need — the next steps will guide you through the specific workflow.

<figure><img src="/.gitbook/assets/img_04cfec25c89e.png" alt="Figure 2 — Open the Business Banking Hub" width="620"><figcaption></figcaption></figure>

*Figure 2 — Open the Business Banking Hub*

**Step 3: Navigate to Payment From File**

From the Dashboard, click "Business Banking" in the left-side navigation menu to open the Business Banking Hub. In the Transfers section, click the "Payment From File" tile. The Payments From File screen opens to the "Upload" tab. You will see a drag-and-drop upload zone in the center of the screen and a "Browse" button for selecting files from your computer. The screen displays accepted file format requirements — the system requires standard NACHA (ACH) format. To upload a file, either drag your NACHA file directly onto the upload zone, or click "Browse" to open a file picker and select the file. The system immediately validates the file format upon selection.

<figure><img src="/.gitbook/assets/img_2ef9ac565a46.png" alt="Figure 3 — Navigate to Payment From File" width="620"><figcaption></figcaption></figure>

*Figure 3 — Navigate to Payment From File*

**Step 4: Check Active Files Being Processed**

After uploading a file, click the "Active File(s)" tab to monitor its processing status. This tab shows all NACHA files currently in the processing pipeline. Each entry displays the file name, upload timestamp, processing status (e.g., "Validating," "Pending Approval," "Processing"), number of transactions in the file, and total dollar amount. If your business has dual-control approval configured for ACH payments, the file will show "Pending Approval" until the required approvers authorize it through the Approvals queue. Refresh the page or check back periodically to monitor progress. Files typically move through validation within minutes.

<figure><img src="/.gitbook/assets/img_d0360d9c1d01.png" alt="Figure 4 — Check Active Files Being Processed" width="620"><figcaption></figcaption></figure>

*Figure 4 — Check Active Files Being Processed*

**Step 5: Review Upload History**

Click the "Upload History" tab to view all previously submitted payment files. The table shows File Name, Upload Date, Processing Status (Completed, Failed, Partially Processed), Transaction Count, Total Amount, and available Actions (download receipt, view details). Use the date range filter to locate files from specific time periods. This tab is your primary reconciliation tool for batch payments — verify that each batch was processed correctly and identify any failed files. Click on any row to drill into the file details. You can also download processing receipts for your accounting records.

<figure><img src="/.gitbook/assets/img_994495435cae.png" alt="Figure 5 — Review Upload History" width="620"><figcaption></figcaption></figure>

*Figure 5 — Review Upload History*

**Step 6: View Individual Transaction Details Within a File**

Click on any file entry (from Active Files or Upload History) to open the file detail view. This screen breaks down the individual transactions contained within the NACHA file. Each transaction record shows the payee name, masked account number, amount, SEC code, and processing status. If any transactions within the batch failed validation or processing, they are highlighted with error codes and descriptions. Use this view to identify exactly which payments succeeded and which failed. For failed transactions, note the error code — common issues include invalid routing numbers, closed accounts, or amount limit violations. You can correct the failed entries in your ERP system and re-upload only the failed transactions.

<figure><img src="/.gitbook/assets/img_deee96573ec0.png" alt="Figure 6 — View Individual Transaction Details Within a File" width="620"><figcaption></figcaption></figure>

*Figure 6 — View Individual Transaction Details Within a File*

