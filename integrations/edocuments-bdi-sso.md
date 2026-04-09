# eDocuments — BDI — SSO
### Feature Guide | Selfreliance FCU | nFinia Digital Banking Platform
*Authored by Jeeva Krishnamurthy, Senior Product Manager — Tyfone*

---

## . Product Summary

The **eDocuments — BDI — SSO** feature enables credit union you to access their electronic statements and documents directly from within the nFinia digital banking platform — both on web and mobile — without requiring a separate login. When you navigates to "Statements & Tax Forms," nFinia silently authenticates you to the BDI (Business Data, Inc.) document portal via Single Sign-On (SSO), then launches the BDI portal in a new tab or browser window. You lands directly on their documents — no username, no password, no redirect friction.

BDI is the third-party electronic document management system that stores and serves member statements (monthly statements, mortgage statements, and other document types). The integration is deployed at `businessdatainc.com` under the credit union's tenant path (e.g., `/SelfrelianceFCU/`). The SSO token is generated server-side by nFinia and passed securely to BDI, meaning you's BDI session is fully authenticated from the moment the portal opens.

This feature serves retail you and business you alike. It is especially valuable for credit unions with multi-membership households, as BDI's portal natively supports a membership selector dropdown — allowing a single digital banking user to switch between multiple linked account numbers and view statements for each. From the credit union's perspective, the integration reduces paper statement costs, supports regulatory disclosure delivery (the Disclosures tab surfaces the Online Statement Enrollment Disclosure), and provides a self-service archive that reduces inbound call volume from you asking for old statements.

| Attribute | Detail |
|-----------|--------|
| Feature Name | eDocuments — BDI — SSO |
| Module | Banking > More > eStatements / Statements and Tax Forms |
| User Roles | Retail Member, Business Member |
| Access Level | Authenticated you (SSO token issued by nFinia post-login) |
| Key Actions | View documents, Switch membership, Download PDF, View Enrollment, View Disclosures, Search Statements |
| Regulatory Relevance | E-SIGN Act compliance (electronic disclosure delivery), paperless enrollment, audit trail of document delivery |
| Integration Type | SSO redirect to third-party BDI document portal |
| Platforms | Web (desktop browser), Mobile (nFinia app → device browser) |

---

## . Use Cases

| Use Case | Who Uses It | What They Do | Business Value |
|----------|-------------|--------------|----------------|
| **View current monthly statement** | Retail member | Navigates to Statements & Tax Forms → SSO launches BDI portal → selects membership → opens most recent Monthly Statement | Replaces paper delivery; member gets instant self-service access |
| **Download a statement PDF** | Member or joint account holder | Opens a statement in the BDI portal and clicks "View PDF" to download or print a printable version | Supports loan applications, tax filings, and audits without branch involvement |
| **Switch between multiple memberships** | Member with multiple account numbers | Uses the membership dropdown in BDI to toggle between different member numbers linked to your digital banking profile | Eliminates need for multiple logins; serves complex household or business structures |
| **View historical/archived documents** | Member | Clicks "> View all past documents" link within a document type section | Provides self-service access to statement archive; reduces call center volume for historical statement requests |
| **Review enrollment and disclosures** | New member or compliance officer | Navigates to Enrollment or Disclosures tab within BDI portal | Ensures E-SIGN Act compliance; you can view the Online Statement Enrollment Disclosure and confirm paperless opt-in |
| **Search for a specific statement** | Member or FI operations | Uses Statement Search tab (desktop) to locate a document by date or criteria | Faster document retrieval without scrolling through full archive |

The BDI SSO integration is particularly important for credit unions with diverse membership profiles — households with both retail and business accounts, you with multiple share numbers, and you who require mortgage statements alongside standard monthly statements. By surfacing all document types under one authenticated session, Selfreliance FCU eliminates the need for you to maintain a separate BDI login.

---

## . End-to-End Workflow

### Prerequisites

- Member must be enrolled in online/mobile banking on the nFinia platform.
- The credit union must have the BDI eDocuments integration configured and SSO credentials provisioned by Tyfone.
- You must have at least one statement available in BDI under their linked membership number(s).
- On mobile, the nFinia app must be installed and you logged in.

### Step-by-Step Flow

#### Desktop (Web Browser)

**Step 1 — Navigate to eStatements**

You logs into nFinia and clicks **Statements and Tax Forms** in the left sidebar (also accessible via **More** in the navigation menu). The breadcrumb path reads: `Banking > More > eStatements`.

**Step 2 — SSO Processing**

nFinia generates a secure SSO token server-side and opens the BDI portal URL in a **new browser tab**. The nFinia page itself displays a confirmation message:

> *"This feature has been opened in another tab."*

No credentials are passed visibly to you — the authentication is fully transparent.

![Desktop — nFinia Statements and Tax Forms page showing SSO redirect confirmation](/.gitbook/assets/bdi-001.jpg)

**Step 3 — BDI Portal Loads (Desktop)**

The BDI portal opens at `uatestmt.businessdatainc.com/SelfrelianceFCU/ShowDocList.do`. The portal displays you's name and a membership number dropdown pre-selected with your primary membership. The top navigation bar shows four tabs: **Documents**, **Enrollment**, **Disclosures**, and **Statement Search**.

![Desktop — BDI portal Documents tab with membership dropdown and document list](/.gitbook/assets/bdi-002.jpg)

**Step 4 — Select Membership (if multiple exist)**

If you has multiple account numbers linked, they click the dropdown and select the desired membership. Each option is listed as `[MemberNumber] - [Name/Entity]`.

![Desktop — BDI member selector dropdown open showing multiple memberships](/.gitbook/assets/bdi-003.jpg)

**Step 5 — View Documents**

After selecting a membership, the Documents tab populates with document type sections (e.g., **Monthly Statement**, **Mortgage Statement**). Each section shows the three most recent documents by date with read/unread envelope icons. A "> View all past documents" link provides access to the full archive.

![Desktop — BDI Monthly Statement document list for selected membership](/.gitbook/assets/bdi-004.jpg)

**Step 6 — Open a Statement**

Clicking a statement date opens the document detail view. The page displays you's name, masked account number (e.g., `XXXXXXXX05`), Period Ending date, and a **View PDF** button. Each account appears as a labeled section (e.g., MONEY MARKET (#0008), SAVINGS (#0100), CLASSIC CHECKING (#0001)) with a summary grid showing Starting Balance, Ending Balance, Debit(s), Credit(s), and YTD Dividends. A **Show details** button expands the full transaction list. A reporting information section at the bottom shows annual totals.

![Desktop — BDI statement detail view showing account summary sections](/.gitbook/assets/bdi-005.jpg)

---

#### Mobile (nFinia App)

**Step 1 — Open the Side Menu**

You taps the hamburger menu (≡) in the nFinia mobile app to open the side navigation panel. The panel lists **Statements & Tax Forms** with the subtitle "View statements & Tax Forms."

![Mobile — nFinia side menu showing Statements & Tax Forms entry point](/.gitbook/assets/bdi-006.jpg)

**Step 2 — Tap "Statements & Tax Forms"**

Tapping this option triggers the SSO. A **Processing...** spinner appears briefly while nFinia generates the SSO token and initiates the redirect to BDI.

**Step 3 — BDI Portal Opens in Device Browser**

The device's default browser launches and opens the BDI portal. You lands on the **Documents** tab with your name and the membership dropdown pre-selected. The portal immediately displays the available document types — **Monthly Statement** and **Mortgage Statement** — with the three most recent entries per type.

![Mobile — BDI portal Documents tab showing membership selector and document list](/.gitbook/assets/bdi-009.jpg)

**Step 4 — Select Membership**

Tapping the dropdown on mobile opens a radio-button picker showing all linked membership numbers. The currently selected membership is indicated with a filled radio button.

![Mobile — BDI membership selector dropdown open on mobile with radio buttons](/.gitbook/assets/bdi-008.jpg)

**Step 5 — View Documents**

After selecting a membership, the Documents page updates to show that membership's document sections. The mobile layout shows **Monthly Statement** and **Mortgage Statement** sections, each with the three most recent entries and a "> View all past documents" link.

![Mobile — BDI Documents tab showing Monthly Statement and Mortgage Statement sections](/.gitbook/assets/bdi-010.jpg)

**Step 6 — Open a Statement**

Tapping a statement date opens the detail view: member name, masked account number, Period Ending date, View PDF button, and per-account summary sections with balances and transaction totals.

![Mobile — BDI statement detail view showing Classic Checking and Savings account summaries](/.gitbook/assets/bdi-011.jpg)

![Mobile — BDI statement detail view with Money Market and Savings data and View PDF button](/.gitbook/assets/bdi-012.jpg)

### Decision Points & Branching

**Single vs. multiple memberships:** If you has only one membership number, the dropdown still renders but only shows one option. If multiple memberships exist, you selects the desired one to load the correct document set.

**Read vs. unread documents:** A closed envelope icon indicates the document has not been opened before; an open envelope icon indicates you has previously viewed it. This provides a visual delivery confirmation for each statement.

**Mobile vs. desktop behavior:** On desktop, BDI opens in a new tab and nFinia remains open in the original tab. On mobile, BDI opens in the device's default browser as a separate session; the nFinia native app remains running in the background.

### Completion & Confirmation

You has successfully accessed their eDocuments when the BDI portal loads with your name, membership dropdown, and document list visible. On the nFinia side, the "This feature has been opened in another tab" banner (desktop) or the browser opening (mobile) confirms SSO was initiated successfully.

Downstream effects: the document's read status updates in BDI when opened, supporting the FI's electronic delivery tracking for E-SIGN compliance purposes.

### Error Handling

**SSO fails / session expired:** If the nFinia session has expired or the SSO token cannot be generated, the redirect will fail or display a BDI error page. You should return to nFinia, log in again, and retry.

**No documents available:** If the selected membership has no statements in BDI yet (e.g., newly opened account), the document sections will be empty. The Enrollment tab can be used to verify paperless enrollment status.

**Membership not found in BDI:** If you's account number is not linked in BDI's system, the dropdown may not populate correctly. This is a back-office configuration issue requiring the FI's operations team to ensure the membership is enrolled in BDI's eStatements program.

---

## . Feature Overview (UI Walkthrough)

### Screen 1 — nFinia Mobile Side Menu (Entry Point)

The side menu in the nFinia mobile app serves as the primary navigation panel for less frequently accessed features. "Statements & Tax Forms" is listed as a top-level menu item identifiable by the document icon and subtitle.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Statements & Tax Forms | Menu item (tappable row) | Entry point to the eDocuments SSO feature | Tapping initiates SSO token generation and redirect to BDI |
| Document icon | Icon | Visual indicator for the statements feature | Displayed left of the label |
| Subtitle text | Label | "View statements & Tax Forms" | Descriptive help text below the feature name |

![Mobile — nFinia side menu with Statements & Tax Forms highlighted](/.gitbook/assets/bdi-013.jpg)

---

### Screen 2 — nFinia Desktop: Statements and Tax Forms Page (Post-SSO)

After clicking the sidebar link, nFinia displays a placeholder page confirming the SSO redirect fired. The BDI portal has already opened in a new browser tab.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Page title | Heading | "Statements and Tax Forms" | Static heading on nFinia side |
| Breadcrumb | Label | `Banking > More > eStatements` | Confirms navigation context |
| Redirect info banner | Info banner | "This feature has been opened in another tab." | Confirms BDI portal opened successfully in new tab |
| Left sidebar | Navigation | Full nFinia navigation remains accessible | nFinia session stays active |

![Desktop — nFinia Statements and Tax Forms with SSO redirect banner](/.gitbook/assets/bdi-014.jpg)

---

### Screen 3 — BDI Portal: Documents Tab

The main landing screen of the BDI portal after SSO authentication. Displays you's name, membership selector, and document type sections.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Member name header | Label | Logged-in member's full name | Pulled from nFinia SSO token |
| Membership dropdown | Dropdown | Selects which membership number's documents to display | Format: `[Number] - [Name]`; pre-selected with primary membership |
| Documents tab | Navigation tab | Active tab (default landing) | Underlined indicator on active tab |
| Enrollment tab | Navigation tab | Navigates to enrollment management screen | |
| Disclosures tab | Navigation tab | Navigates to legal disclosures screen | |
| Statement Search tab | Navigation tab | Navigates to statement search (desktop only) | Not shown on mobile nav |
| Document type section header | Section | Groups documents by type (e.g., "Monthly Statement") | Dark navy background, white text, with document-type icon |
| Document entry row | Tappable row | Date of each statement (e.g., "Feb 28, 2025") with read-status icon | Tapping opens document detail |
| Read status icon (closed envelope) | Icon | Document not yet viewed | |
| Read status icon (open envelope) | Icon | Document previously viewed | |
| View all past documents | Link | Expands full document archive | Appears below three most recent entries |

![Desktop — BDI Documents tab with membership dropdown and statement list](/.gitbook/assets/bdi-015.jpg)

![Mobile — BDI Documents tab showing Monthly and Mortgage Statement sections](/.gitbook/assets/bdi-016.jpg)

---

### Screen 4 — BDI Portal: Membership Selector Dropdown

Activated by clicking/tapping the membership dropdown. On desktop this is a standard HTML select list; on mobile it renders as a modal picker with radio buttons.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Membership dropdown | Dropdown (desktop) / Radio picker (mobile) | Lists all linked memberships for the authenticated user | Selecting a different membership reloads the document list for that member number |
| Selected indicator | Highlight (desktop) / Filled radio (mobile) | Marks the currently active membership | |
| Membership entry | List item | Format: `[Number] - [Member Name or Entity]` | Can include personal names and institutional names (e.g., "Selfreliance FCU") |
| Section header (mobile picker) | Label | Shows document type context (e.g., "Monthly Statement") | Displayed above the membership list in the mobile picker |

![Desktop — BDI membership dropdown open with multiple options](/.gitbook/assets/bdi-017.jpg)

![Mobile — BDI membership picker with radio button selection](/.gitbook/assets/bdi-018.jpg)

---

### Screen 5 — BDI Portal: Statement Detail View

Opened when you clicks or taps a specific statement date. Shows the full statement with per-account summaries and a PDF download option.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Member name | Label | Full name of account holder | Displayed at top of statement view |
| Masked account number | Label | Format: `XXXXXXXX##` (last 2 digits visible) | Full number available in PDF version |
| Period Ending | Label | Statement period end date (e.g., "Period Ending: 10/31/2024") | |
| View PDF | Button/Link | Downloads or opens full PDF version of the statement | Shown with PDF icon in top-right of header area |
| Account section header | Section | Account type and share number (e.g., "MONEY MARKET (#0008)") | Dark navy background, white bold text |
| Starting Balance | Data cell | Opening balance for the statement period | Displayed in a 2-column or 3-column summary grid |
| Ending Balance | Data cell | Closing balance for the statement period | |
| Debit(s) | Data cell | Total debits with transaction count (e.g., "114 Debit(s)") | |
| Credit(s) | Data cell | Total credits with transaction count | |
| YTD Dividends | Data cell | Year-to-date dividend amount for the account | |
| Show details | Button | Toggle to expand full transaction-level detail for the account | Expands beneath the summary grid |
| Reporting Information | Section | Annual summary: Share Account Totals, Total Dividends Paid Year to Date | Labeled by year (e.g., "2024 REPORTING INFORMATION") |

![Desktop — BDI statement detail with account sections and View PDF button](/.gitbook/assets/bdi-019.jpg)

![Mobile — BDI statement detail showing Classic Checking and Savings summaries](/.gitbook/assets/bdi-020.jpg)

![Mobile — BDI statement detail showing Money Market and Savings with View PDF](/.gitbook/assets/bdi-021.jpg)

---

### Screen 6 — BDI Portal: Disclosures Tab

Accessed by tapping/clicking the **Disclosures** tab in the BDI portal navigation bar.

| Field / Element | Type | Description | Notes |
|-----------------|------|-------------|-------|
| Disclosures section header | Section header | "Disclosures" label in dark navy | |
| Online Statement Enrollment Disclosure | Link | Opens the full text of the E-SIGN / paperless enrollment disclosure | Required for regulatory compliance with electronic document delivery; you can review the terms of their paperless enrollment |

![Mobile — BDI Disclosures tab with Online Statement Enrollment Disclosure](/.gitbook/assets/bdi-022.jpg)

---

## . Quick Reference

| Task | Navigation Path | Who Can Do It | Notes |
|------|----------------|---------------|-------|
| Access eDocuments (Desktop) | Sidebar > Statements and Tax Forms | Any authenticated member | BDI portal opens in new browser tab via SSO |
| Access eDocuments (Mobile) | Hamburger menu (≡) > Statements & Tax Forms | Any authenticated member | BDI portal opens in device's default browser |
| Switch membership in BDI | BDI portal > Documents tab > Membership dropdown | Any authenticated member | Lists all memberships linked to the nFinia digital banking profile |
| View a statement | BDI portal > Documents > [Statement date] | Any authenticated member | Opens full statement detail with per-account summary |
| Download statement as PDF | BDI portal > Statement detail > View PDF | Any authenticated member | Opens printable/downloadable PDF of the selected statement |
| View full document archive | BDI portal > Documents > "> View all past documents" | Any authenticated member | Expands full history beyond the three most recent entries |
| View legal disclosures | BDI portal > Disclosures tab | Any authenticated member | Online Statement Enrollment Disclosure for E-SIGN compliance |
| Search for a specific statement | BDI portal > Statement Search tab | Any authenticated member | Desktop only; not available on mobile navigation |

---

*Guide produced using the Jeeva Krishnamurthy Bank3 Report Format. Feature observed on the Selfreliance FCU staging deployment of nFinia (`summerville.nfinia.com BDI portal: `uatestmt.businessdatainc.com/SelfrelianceFCU/`.*
