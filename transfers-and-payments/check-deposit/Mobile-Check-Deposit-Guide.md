**Summerville FCU**  
Mobile Check Deposit (RDC) Feature Guide

Platform: nFinia Mobile Banking | Prepared by: Jeeva PM | April 2026

**1. PRODUCT SUMMARY**

Mobile Check Deposit — also known as Remote Deposit Capture (RDC) — on
nFinia enables Summerville FCU business You to deposit checks
directly from their mobile device, eliminating the need for a branch
visit. You use their device camera to photograph the front and back
of a check through a guided capture interface with green
corner-alignment overlays that ensure image quality.

The deposit flow walks You through each step: selecting the target
account, entering the check amount, capturing check images using guided
tips, reviewing thumbnails, and submitting. The system validates the
amount against configured deposit limits and checks image quality before
processing.

For Summerville FCU, Mobile Check Deposit reduces teller traffic,
extends deposit availability beyond branch hours, and provides business
You — especially those with limited time to visit in person — with a
fully digital deposit channel. All deposits create an auditable record
in Check Deposit History, supporting Reg CC compliance and BSA/AML
monitoring.

**At-a-Glance**

|                      |                                                                        |
| -------------------- | ---------------------------------------------------------------------- |
| **Attribute**        | **Detail**                                                             |
| Feature Name         | Mobile Check Deposit (Remote Deposit Capture / RDC)                    |
| Module               | Accounts > Deposit                                                    |
| User Roles           | Enrolled Member, Business Account Holder                               |
| Access Level         | Requires RDC enrollment and account eligibility                        |
| Key Actions          | Select account, enter amount, capture front/back check images, submit  |
| Regulatory Relevance | Reg CC (funds availability), BSA/AML (deposit monitoring), audit trail |

**2. USE CASES**

|                                |                            |                                                                                                         |                                                                      |
| ------------------------------ | -------------------------- | ------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| **Use Case**                   | **Who Uses It**            | **What They Do**                                                                                        | **Business Value**                                                   |
| Standard Check Deposit         | Business member            | Selects deposit account, enters check amount, photographs front and back using guided capture, submits  | Eliminates branch visit; deposit available within Reg CC timeframes  |
| First-Time Photo Capture       | New RDC user               | Reviews Photo Tips modal (endorse back, flat surface, align to green corners), then proceeds to capture | Reduces failed deposits and resubmission rates                       |
| Retake Check Image             | Member with blurry capture | Reviews thumbnail, taps Retake Picture on front or back image, recaptures                               | Improves image quality before submission; prevents processing delays |
| Large-Amount Deposit           | Business CFO               | Deposits check within configured limit (e.g. $2,700); system validates amount against account limit     | Enables treasury management without branch dependency                |
| Deposit Confirmation & History | Operations staff / Member  | Views deposit status, receipt number, and channel (Mobile/Online/Branch) in history tab                 | Provides audit trail; supports BSA/AML monitoring                    |

**3. END-TO-END WORKFLOW**

**3.1 Prerequisites**

• RDC enrollment active for you account

• Account eligible for mobile check deposit (configured by Summerville
FCU)

• nFinia mobile app installed with camera permission granted

**3.2 Step-by-Step Flow**

|          |                                                                                        |                                                                              |
| -------- | -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| **Step** | **Action**                                                                             | **System Response**                                                          |
| 1        | Launch nFinia app → tap "Deposit" in bottom navigation bar                             | Deposit screen loads with account selector and amount field                  |
| 2        | Select "To Account" from dropdown (e.g. Student Checking XXX-1234), enter Check Amount | Amount field validates numeric input; deposit limit displayed                |
| 3        | Tap camera icon for Front of Check                                                     | Photo Tips modal appears: Endorse back, flat surface, align to green corners |
| 4        | Dismiss tips → Camera view opens                                                       | Green corner guide overlay displayed in camera viewfinder                    |
| 5        | Align check until corners light up → tap capture button                                | Front check image captured; thumbnail shown in deposit form                  |
| 6        | Tap Back of Check camera icon                                                          | Camera view opens for endorsed back capture                                  |
| 7        | Capture back of endorsed check                                                         | Back thumbnail shown in deposit form alongside front thumbnail               |
| 8        | Review both thumbnails → tap SUBMIT (or RETAKE PICTURE if needed)                      | System validates: amount vs. limit, image quality, account eligibility       |
| 9        | Validation passes                                                                      | Success confirmation screen shown; deposit enters processing queue           |
| 10       | Member views History tab                                                               | Entry created with status "Submitted", timestamp, amount, channel = Mobile   |

**3.3 Decision Points & Error Handling**

|                                          |                                                                      |
| ---------------------------------------- | -------------------------------------------------------------------- |
| **Condition**                            | **System Behavior**                                                  |
| Amount exceeds configured deposit limit  | "Exceeds deposit limit" error shown; deposit blocked until corrected |
| Image quality insufficient (blurry/dark) | "Image quality insufficient" prompt; member directed to retake       |
| Account not eligible for RDC             | Account not shown in deposit dropdown                                |
| Network failure during submission        | Draft preserved; retry option shown on next app open                 |

**3.4 Completion**

Upon successful submission, a confirmation screen is displayed. The
transaction is recorded in Check Deposit History with status
"Submitted," timestamp, amount, and channel (Mobile). An audit log entry
is created with deposit event details for BSA/AML and Reg CC compliance.

**4. FEATURE OVERVIEW — UI WALKTHROUGH**

**Screen 1: Deposit Form — Initial State**

<figure><img src="/.gitbook/assets/64afc208a3772843837d1c9c315c68a6ed676afc.png" alt="" width="340"><figcaption></figcaption></figure>

*Figure 1: Deposit form with account selector and camera buttons*

|                             |                       |                                                            |
| --------------------------- | --------------------- | ---------------------------------------------------------- |
| **Field / Element**         | **Type**              | **Description**                                            |
| To Account                  | Dropdown              | Selects the target deposit account (e.g. Student Checking) |
| Check Amount                | Numeric input         | Dollar amount of check being deposited; required           |
| Email                       | Text input (optional) | Email address for deposit confirmation notification        |
| Front Check [camera icon] | Button                | Opens camera or Photo Tips modal for front image capture   |
| Back Check [camera icon]  | Button                | Opens camera for endorsed back image capture               |
| Bottom Nav                  | Navigation bar        | Accounts | Deposit | Transfer | Bill Pay                   |

**Screen 2: Photo Tips Modal**

<figure><img src="/.gitbook/assets/e03a6bc5d4860110e2dbe8ed156d240f649b3f6c.png" alt="" width="340"><figcaption></figcaption></figure>

*Figure 2: Photo Tips guidance before camera opens*

|                     |              |                                                                      |
| ------------------- | ------------ | -------------------------------------------------------------------- |
| **Field / Element** | **Type**     | **Description**                                                      |
| Tip Text            | Instructions | Endorse back of check; place on flat surface; align to green corners |
| Proceed Button      | Button       | Dismisses modal and opens camera view for check capture              |

**Screen 3: Deposit Form — Account & Amount Selected**

<figure><img src="/.gitbook/assets/e0f8dd163bc5a4b2d9aa373fa9c7e8ea55809399.png" alt="" width="340"><figcaption></figcaption></figure>

*Figure 3: Account selected (Student Checking) and amount $2,700
entered*

|                         |                   |                                                           |
| ----------------------- | ----------------- | --------------------------------------------------------- |
| **Field / Element**     | **Type**          | **Description**                                           |
| To Account              | Dropdown (filled) | Student Checking XXX-XXX-XXX-1234 selected                |
| Check Amount            | Numeric (filled)  | $2,700.00 entered                                         |
| Deposit Limit Indicator | Display           | Configured limit shown (e.g. $2,700 max for this account) |

**Screen 4: Front Check Camera (Landscape)**

<figure><img src="/.gitbook/assets/c5080b3fd480e9b55e0c6ebe434616bdede0a906.png" alt="" width="620"><figcaption></figcaption></figure>

*Figure 4: Camera viewfinder with green corner alignment guides for
front of check*

|                     |             |                                                                  |
| ------------------- | ----------- | ---------------------------------------------------------------- |
| **Field / Element** | **Type**    | **Description**                                                  |
| Camera Viewfinder   | Live camera | Full-screen camera view oriented to capture check                |
| Green Corner Guides | Overlay     | Visual alignment corners; turn green when check properly aligned |
| Capture Button      | Button      | Takes photo when check is aligned and in focus                   |

**Screen 5: Back Check Camera (Landscape)**

<figure><img src="/.gitbook/assets/459e49c05b3731e5b9c010ad9cf2257fb35ee201.png" alt="" width="620"><figcaption></figcaption></figure>

*Figure 5: Camera view for capturing endorsed back of check*

|                         |             |                                             |
| ----------------------- | ----------- | ------------------------------------------- |
| **Field / Element**     | **Type**    | **Description**                             |
| Camera Viewfinder       | Live camera | Full-screen view for endorsed back of check |
| Corner Alignment Guides | Overlay     | Same guidance system as front capture       |
| Capture Button          | Button      | Takes photo of back of endorsed check       |

**Screen 6: Review & Submit**

<figure><img src="/.gitbook/assets/acfa3869fc989a7fff84017541cf0f041e4823dc.png" alt="" width="340"><figcaption></figcaption></figure>

*Figure 6: Review screen with front and back thumbnails before
submission*

|                     |                  |                                                       |
| ------------------- | ---------------- | ----------------------------------------------------- |
| **Field / Element** | **Type**         | **Description**                                       |
| Front Thumbnail     | Image preview    | Captured front check image — tap to enlarge or retake |
| Back Thumbnail      | Image preview    | Captured back (endorsed) check image                  |
| SUBMIT Button       | Primary action   | Submits deposit for processing                        |
| RETAKE PICTURE      | Secondary action | Discards and recaptures front or back image           |

**Screen 7: Front Check Retake View**

<figure><img src="/.gitbook/assets/21700c244149842d703e2ff4fbc2e99a5e71de76.png" alt="" width="340"><figcaption></figcaption></figure>

*Figure 7: Front image review with retake option available*

|                     |           |                                                        |
| ------------------- | --------- | ------------------------------------------------------ |
| **Field / Element** | **Type**  | **Description**                                        |
| Front Image Preview | Full view | Enlarged view of front check image for quality review  |
| RETAKE PICTURE      | Button    | Discards current front image and reopens camera        |
| Check Details       | Display   | Date, check amount, account info displayed below image |

**Screen 8: Back Check Retake View**

<figure><img src="/.gitbook/assets/deb630aa4b4b10a13730ed0850b566322c6c5e20.png" alt="" width="340"><figcaption></figcaption></figure>

*Figure 8: Back image review with retake option — shows endorsement
area*

|                     |           |                                                       |
| ------------------- | --------- | ----------------------------------------------------- |
| **Field / Element** | **Type**  | **Description**                                       |
| Back Image Preview  | Full view | Enlarged view of back (endorsed) check image          |
| RETAKE PICTURE      | Button    | Discards back image and reopens camera for re-capture |
| Endorsement Area    | Visual    | Back image should show member endorsement signature   |

**5. QUICK REFERENCE**

|                           |                                                 |                              |                                                 |
| ------------------------- | ----------------------------------------------- | ---------------------------- | ----------------------------------------------- |
| **Task**                  | **Navigation Path**                             | **Who Can Do It**            | **Notes**                                       |
| Deposit a check           | App > Deposit tab > Fill form > Submit       | Enrolled member (RDC active) | Camera permission required                      |
| View deposit history      | App > Deposit > History tab                   | Member                       | Shows all channels: Mobile, Online, Branch, ATM |
| Retake check image        | Deposit flow > Review screen > Retake Picture | Member                       | Available before submission only                |
| Check deposit limit       | Deposit form — displayed automatically          | Member                       | Configured per account type by Summerville FCU  |
| View deposit confirmation | Success screen after submit                     | Member                       | Shows receipt number, amount, status            |
