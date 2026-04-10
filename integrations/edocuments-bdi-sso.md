# eDocuments — BDI SSO

***

## Summary

The **eDocuments — BDI — SSO** feature enables you to access your electronic statements and documents directly from within the nFinia digital banking platform — both on web and mobile — without requiring a separate login. When you navigate to "Statements & Tax Forms," nFinia silently authenticates you to the BDI (Business Data, Inc.) document portal via Single Sign-On (SSO), then launches the BDI portal in a new tab or browser window. You land directly on your documents — no username, no password, no redirect friction.

BDI is the third-party electronic document management system that stores and serves member statements (monthly statements, mortgage statements, and other document types). The integration is deployed at `businessdatainc.com` under the credit union's tenant path (e.g., `/SummervileCU/`). The SSO token is generated server-side by nFinia and passed securely to BDI, meaning your BDI session is fully authenticated from the moment the portal opens.

This feature serves retail and business members alike. It is especially valuable for credit unions with multi-membership households, as BDI's portal natively supports a membership selector dropdown — allowing a single digital banking user to switch between multiple linked account numbers and view statements for each. From the credit union's perspective, the integration reduces paper statement costs, supports regulatory disclosure delivery (the Disclosures tab surfaces the Online Statement Enrollment Disclosure), and provides a self-service archive that reduces inbound call volume from members asking for old statements.

| Attribute            | Detail                                                                                                         |
| -------------------- | -------------------------------------------------------------------------------------------------------------- |
| Feature Name         | eDocuments — BDI — SSO                                                                                         |
| Module               | Banking > More > eStatements / Statements and Tax Forms                                                        |
| User Roles           | Retail Member, Business Member                                                                                 |
| Access Level         | Authenticated member (SSO token issued by nFinia post-login)                                                   |
| Key Actions          | View documents, Switch membership, Download PDF, View Enrollment, View Disclosures, Search Statements          |
| Regulatory Relevance | E-SIGN Act compliance (electronic disclosure delivery), paperless enrollment, audit trail of document delivery |
| Integration Type     | SSO redirect to third-party BDI document portal                                                                |
| Platforms            | Web (desktop browser), Mobile (nFinia app → device browser)                                                    |

***

## Use Cases

| Use Case                                | Who Uses It                          | What They Do                                                                                                             | Business Value                                                                                                      |
| --------------------------------------- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| **View current monthly statement**      | Retail member                        | Navigates to Statements & Tax Forms → SSO launches BDI portal → selects membership → opens most recent Monthly Statement | Replaces paper delivery; instant self-service access                                                                |
| **Download a statement PDF**            | Member or joint account holder       | Opens a statement in the BDI portal and clicks "View PDF" to download or print a printable version                       | Supports loan applications, tax filings, and audits without branch involvement                                      |
| **Switch between multiple memberships** | Member with multiple account numbers | Uses the membership dropdown in BDI to toggle between different member numbers linked to your digital banking profile    | Eliminates need for multiple logins; serves complex household or business structures                                |
| **View historical/archived documents**  | Member                               | Clicks "> View all past documents" link within a document type section                                                   | Provides self-service access to statement archive; reduces call center volume for historical statement requests     |
| **Review enrollment and disclosures**   | New member or compliance officer     | Navigates to Enrollment or Disclosures tab within BDI portal                                                             | Ensures E-SIGN Act compliance; you can view the Online Statement Enrollment Disclosure and confirm paperless opt-in |
| **Search for a specific statement**     | Member or FI operations              | Uses Statement Search tab (desktop) to locate a document by date or criteria                                             | Faster document retrieval without scrolling through full archive                                                    |

The BDI SSO integration is particularly important for credit unions with diverse membership profiles — households with both retail and business accounts, members with multiple share numbers, and members who require mortgage statements alongside standard monthly statements. By surfacing all document types under one authenticated session, the credit union eliminates the need for members to maintain a separate BDI login.

***

## End-to-End Workflow

### Prerequisites

* You must be enrolled in online/mobile banking on the nFinia platform.
* The credit union must have the BDI eDocuments integration configured and SSO credentials provisioned by Tyfone.
* You must have at least one statement available in BDI under your linked membership number(s).
* On mobile, the nFinia app must be installed and you must be logged in.

### Step-by-Step Flow

#### Desktop (Web Browser)

**Step 1 — Navigate to eStatements**

Log in to nFinia and click **Statements and Tax Forms** in the left sidebar (also accessible via **More** in the navigation menu). The breadcrumb path reads: `Banking > More > eStatements`.

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

**Step 2 — BDI Portal Loads (Desktop)**

The BDI portal opens at `uatestmt.businessdatainc.com/SummervilleCU/ShowDocList.do`. The portal displays your name and a membership number dropdown pre-selected with your primary membership. The top navigation bar shows four tabs: **Documents**, **Enrollment**, **Disclosures**, and **Statement Search,**&#x49;f you have multiple account numbers linked, click the dropdown and select the desired membership. Each option is listed as `[MemberNumber] - [Name/Entity]`.

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

**Step 3 — View Documents and open a statement**

After selecting a membership, the Documents tab populates with document type sections (e.g., **Monthly Statement**, **Mortgage Statement**). Each section shows the three most recent documents by date with read/unread envelope icons. A "> View all past documents" link provides access to the full archive,Clicking a statement date opens the document detail view. The page displays your name, masked account number (e.g., `XXXXXXXX05`), Period Ending date, and a **View PDF** button. Each account appears as a labeled section (e.g., MONEY MARKET (#0008), SAVINGS (#0100), CLASSIC CHECKING (#0001)) with a summary grid showing Starting Balance, Ending Balance, Debit(s), Credit(s), and YTD Dividends. A **Show details** button expands the full transaction list. A reporting information section at the bottom shows annual totals.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

***

#### Mobile (nFinia App)

**Step 1 — Open the Side Menu**

Tap the hamburger menu (≡) in the nFinia mobile app to open the side navigation panel. The panel lists **Statements & Tax Forms** with the subtitle "View statements & Tax Forms."

<figure><img src="../.gitbook/assets/Screenshot 2026-04-10 at 9.13.04 PM.png" alt="" width="243"><figcaption></figcaption></figure>

**Step 2 — Tap "Statements & Tax Forms"**

Tapping this option triggers the SSO. A **Processing...** spinner appears briefly while nFinia generates the SSO token and initiates the redirect to BDI.

**Step 3 — BDI Portal Opens in Device Browser**

The device's default browser launches and opens the BDI portal. You land on the **Documents** tab with your name and the membership dropdown pre-selected. The portal immediately displays the available document types — **Monthly Statement** and **Mortgage Statement** — with the three most recent entries per type.

<figure><img src="../.gitbook/assets/Screenshot 2026-04-10 at 9.14.39 PM.png" alt="" width="244"><figcaption></figcaption></figure>

**Step 4 — Select Membership**

Tapping the dropdown on mobile opens a radio-button picker showing all linked membership numbers. The currently selected membership is indicated with a filled radio button.

<figure><img src="../.gitbook/assets/Screenshot 2026-04-10 at 9.15.17 PM.png" alt="" width="242"><figcaption></figcaption></figure>

**Step 5 — View Documents**

After selecting a membership, the Documents page updates to show that membership's document sections. The mobile layout shows **Monthly Statement** and **Mortgage Statement** sections, each with the three most recent entries and a "> View all past documents" link.

<figure><img src="../.gitbook/assets/Screenshot 2026-04-10 at 9.15.46 PM.png" alt="" width="245"><figcaption></figcaption></figure>

**Step 6 — Open a Statement**

Tapping a statement date opens the detail view: your name, masked account number, Period Ending date, View PDF button, and per-account summary sections with balances and transaction totals.

<figure><img src="../.gitbook/assets/Screenshot 2026-04-10 at 9.16.17 PM.png" alt="" width="563"><figcaption></figcaption></figure>

### Decision Points & Branching

**Single vs. multiple memberships:** If you have only one membership number, the dropdown still renders but only shows one option. If multiple memberships exist, select the desired one to load the correct document set.

**Read vs. unread documents:** A closed envelope icon indicates the document has not been opened before; an open envelope icon indicates you have previously viewed it. This provides a visual delivery confirmation for each statement.

**Mobile vs. desktop behavior:** On desktop, BDI opens in a new tab and nFinia remains open in the original tab. On mobile, BDI opens in the device's default browser as a separate session; the nFinia native app remains running in the background.

### Completion & Confirmation

You have successfully accessed your eDocuments when the BDI portal loads with your name, membership dropdown, and document list visible. On the nFinia side, the "This feature has been opened in another tab" banner (desktop) or the browser opening (mobile) confirms SSO was initiated successfully.

Downstream effects: the document's read status updates in BDI when opened, supporting the FI's electronic delivery tracking for E-SIGN compliance purposes.

### Error Handling

**SSO fails / session expired:** If the nFinia session has expired or the SSO token cannot be generated, the redirect will fail or display a BDI error page. Return to nFinia, log in again, and retry.

**No documents available:** If the selected membership has no statements in BDI yet (e.g., newly opened account), the document sections will be empty. The Enrollment tab can be used to verify paperless enrollment status.

**Membership not found in BDI:** If your account number is not linked in BDI's system, the dropdown may not populate correctly. This is a back-office configuration issue requiring the FI's operations team to ensure the membership is enrolled in BDI's eStatements program.

***

## Quick Reference

| Task                            | Navigation Path                                      | Who Can Do It            | Notes                                                              |
| ------------------------------- | ---------------------------------------------------- | ------------------------ | ------------------------------------------------------------------ |
| Access eDocuments (Desktop)     | Sidebar > Statements and Tax Forms                   | Any authenticated member | BDI portal opens in new browser tab via SSO                        |
| Access eDocuments (Mobile)      | Hamburger menu (≡) > Statements & Tax Forms          | Any authenticated member | BDI portal opens in device's default browser                       |
| Switch membership in BDI        | BDI portal > Documents tab > Membership dropdown     | Any authenticated member | Lists all memberships linked to the nFinia digital banking profile |
| View a statement                | BDI portal > Documents > \[Statement date]           | Any authenticated member | Opens full statement detail with per-account summary               |
| Download statement as PDF       | BDI portal > Statement detail > View PDF             | Any authenticated member | Opens printable/downloadable PDF of the selected statement         |
| View full document archive      | BDI portal > Documents > "> View all past documents" | Any authenticated member | Expands full history beyond the three most recent entries          |
| View legal disclosures          | BDI portal > Disclosures tab                         | Any authenticated member | Online Statement Enrollment Disclosure for E-SIGN compliance       |
| Search for a specific statement | BDI portal > Statement Search tab                    | Any authenticated member | Desktop only; not available on mobile navigation                   |
