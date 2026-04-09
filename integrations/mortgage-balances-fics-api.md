# Mortgage Balances — FICS API
### Feature Guide · nFinia Digital Banking Platform

---

## . Product Summary

The **Mortgage Balances — FICS API** feature integrates nFinia's OLB (Online Banking) and Mobile Banking platforms with a credit union's FICS loan servicing system via API. It gives you direct, real-time visibility into their FICS-serviced mortgage loan accounts — without leaving the nFinia digital banking environment.

Members with active FICS mortgage loans can view loan details (property address, interest rate, payment schedule), review transaction history, monitor balance breakdowns, manage contact information on file with the servicer, request payoff quotes, access account notes, and message the credit union's mortgage department — all from within the same digital banking session they use for deposits and transfers.

For the credit union, this integration reduces inbound servicing calls by surfacing self-service mortgage data within the primary member channel. It also eliminates the friction of redirecting you to a separate mortgage servicing portal. The feature lives under **Banking > Accounts > [FICS Loan Account]** and is also accessible from the **Mortgage** item in the left-hand sidebar navigation.

| Attribute | Detail |
|---|---|
| Feature Name | Mortgage Balances — FICS API |
| Module | Banking > Accounts > FICS Loan / Sidebar > Mortgage |
| Platforms | OLB (Web), Mobile Banking (iOS/Android), Mobile Browser |
| User Roles | Retail you with active FICS-serviced mortgage loan(s) |
| Access Level | Member-authenticated; account-scoped |
| Key Actions | View loan details, view balances, view transaction history, edit contact info, request payoff, send secure message, access statements, initiate payment (Pay Now via SSO) |
| Integration Type | API (FICS loan servicing system) |
| SSO Dependencies | Pay Now, Paperless Statements (external redirect via SSO token) |

---

## . Use Cases

| Use Case | Who Uses It | What They Do | Business Value |
|---|---|---|---|
| View mortgage loan details | Member with active FICS mortgage | Navigates to Mortgage in sidebar or via Accounts, selects a loan, reviews property address, interest rate, payment schedule, and remaining term | Reduces inbound "what's my balance/rate?" calls to the call center |
| Make an online mortgage payment | Member with upcoming payment due | Clicks **Pay Now** on the account detail screen, acknowledges the external link warning, and completes payment in the FICS-integrated payment portal | Increases on-time payments; reduces servicing friction |
| Request payoff information | Member preparing to sell or refinance | Opens **Loan Information > Request payoff information**, selects delivery method (email/mail/fax), enters required dates, and submits | Replaces paper or phone-based payoff requests with a digital, trackable workflow |
| Update contact information on file | Member whose address or phone has changed | Navigates to **About this loan**, clicks **Edit**, updates fields, and saves | Keeps servicer records current; reduces returned mail and missed communications |
| Download transaction history or balance report | Member preparing for tax filing or refinance | Views **Transaction History** or navigates to **Balances** tab, downloads or prints the year-to-date summary | Supports member financial planning; reduces document request calls |
| Send a secure message to the mortgage department | Member with a loan servicing question | Opens the **Help** tab, types a message in "Send us a message", and submits | Provides a channel-appropriate support path without leaving the banking session |

Credit unions enabling this integration can measurably deflect mortgage servicing calls while surfacing the kind of account detail that earns member trust — especially for the increasingly common scenario where the mortgage is serviced by FICS but the primary banking relationship is with the CU.

---

## . End-to-End Workflow

### Prerequisites

- Member must have an active FICS-serviced mortgage loan linked to their nFinia account.
- The credit union must have the FICS API integration configured and enabled in the nFinia admin settings.
- For **Pay Now** and **Paperless Statements**, a valid SSO token configuration must be in place between nFinia and the FICS payment/document portal.
- Members with multiple FICS loans will see all linked loans in the account selector dropdown.

### Step-by-Step Flow

**Accessing the Mortgage Feature**

1. After logging in, you clicks **Mortgage** in the left-hand sidebar, or navigates via **Banking > Additional Services > Mortgage**, or selects a FICS loan account directly from the **Accounts** list.
2. The system calls the FICS API and retrieves all linked mortgage accounts for the authenticated member.
3. If you has a single loan, the platform loads it directly. If multiple loans exist, a **Select Account** dropdown appears — you selects the desired loan.

**Mortgage Account Dashboard**

4. The **Account Detail** screen loads, displaying the FICS loan identifier, remaining balance, interest rate, next due amount and date, remaining term, and an **Upcoming Payments** panel. A **Pay Now** button and **Quick Transfer** panel are available in the right-hand column.
5. Below the summary, the **Transactions** section lists all historical payments. Each row shows date, amount, principal/interest/tax-insurance split, and remaining balance. Clicking a row expands the transaction detail view, which includes a **Download** button to save an individual transaction record as a PDF.

**Loan Information Tabs**

6. Clicking **View more loan information** or navigating to the **Fics Loan** account detail opens the tabbed **Loan Information** view with five tabs: **About this loan**, **Balances**, **Account notes**, **Statement and documents**, and **Help**.
7. **About this loan** (default): Displays a full loan detail card — property address, date registered, next due payment amount and date, current interest rate (APR), payment frequency, remaining term, maturity date, a **Current payment breakdown** section (principal and interest, tax and insurance, total), and a **Contact information** section showing home phone, business phone, email address, and mailing address with an **Edit** link.
8. Clicking **Edit** opens the **Update mortgage contact information** modal. All fields are required unless marked optional. Fields include: First name (Optional), Last name (Optional), Address 1, Address 2 (Optional), City/Town, State, ZIP Code, Email address, Phone number (home), Business phone (Optional), and Extension (Optional). Clicking **Save** submits the update to FICS. A success banner appears on confirmation.
9. **Balances**: Displays a detailed balance breakdown pulled from FICS — Principal, Deferred principal, Tax and insurance, Subsidy, Unapplied, Unpaid late charges, Returned check charges, Loss draft, and Negative amortization. Below is a **Current year-to-date totals** section. A **Download balances year-to-date totals** link opens the browser's print dialog for you to save or print the balance report as a PDF.
10. **Account notes**: Displays any servicer-entered notes on the account. A search bar and date-range filter are available. Notes are displayed in chronological order with a sort option.
11. **Statement and documents**: Provides access to you's paperless statements via SSO redirect to the FICS document portal.
12. **Help**: Displays credit union mortgage contact information (phone number, support hours, mailing address) and a **Send us a message** text area. Submitting the message delivers a secure inquiry to the credit union's mortgage team. A success confirmation banner appears after submission.

### Request Payoff Information

13. From the **Loan Information** screen, clicking **Request payoff information** opens a modal with the following fields:
    - **I need this information on or before** (date, required): The date by which you needs the payoff quote.
    - **Estimated date of payoff** (date, required): The date by which you intends to pay off the mortgage.
    - **Send payoff information to**: Radio selection — My email (pre-filled from profile), My mailing address, or My fax number. Each selection reveals the relevant detail field.
    - **Phone number** (pre-filled, required): Contact number for you.
14. Clicking **Submit** sends the payoff request to the FICS system. On success, a green confirmation banner — "Your request for payoff information has been successfully sent." — appears on the Loan Information screen.

### Pay Now

15. On the **Account Detail** screen, clicking **Pay Now** displays an **External Link Warning** dialog informing you they are navigating outside of nFinia to the FICS payment portal. The dialog shows a disclaimer about external site policies and offers **Cancel** and **Proceed** buttons.
16. Clicking **Proceed** initiates the SSO handoff and opens the FICS payment portal in a new browser tab, pre-authenticated via SSO token.

### Error Handling

- **No mortgage accounts found**: If the authenticated member has no linked FICS loans, the Mortgage page displays: _"There are no mortgage accounts."_
- **Invalid loan ID**: If the FICS API returns an error for a loan ID, you sees a generic error state on the account detail page with options to go back or return to the home page.
- **Pay Now / SSO session expired**: If the SSO token has expired before you clicks Pay Now again, the external payment portal returns a **Login Error** screen. You should return to nFinia and retry.

---

## . Screen-by-Screen Walkthrough

### Mortgage Landing Page

Accessible via the **Mortgage** icon in the left sidebar or through **Banking > Additional Services > Mortgage**. If you has no FICS-linked loans, the page shows an empty state. Otherwise, a loan selector appears.

![Mortgage landing page — sidebar navigation and empty state](/.gitbook/assets/fics-001.jpg)

When you has multiple FICS accounts, a **Select Account** dropdown appears populated with all linked FICS loan accounts.

![FICS loan account selector dropdown](/.gitbook/assets/fics-002.jpg)

---

### Mortgage Account Detail

The main account overview screen for a selected FICS loan. This is the hub from which you accesses all mortgage self-service functions.

![Mortgage account detail — loan summary, Pay Now, Upcoming Payments, Quick Transfer](/.gitbook/assets/fics-003.jpg)

| Field / Element | Type | Description |
|---|---|---|
| FICS LOAN [Account Number] | Label | Loan identifier pulled from FICS |
| Loan account in Membership # | Label | Linked membership/share account number |
| Payment Due / Next Due Date | Label | Next scheduled payment amount and due date, highlighted in orange when approaching |
| Interest Rate | Label | Current annual interest rate (APR) |
| Interest Paid YTD | Label | Year-to-date interest paid, with info icon tooltip |
| Remaining term | Label | Months remaining on the loan |
| Pay now | Button | Initiates SSO redirect to FICS payment portal |
| Upcoming Payments panel | Display | Shows next scheduled payment with loan type and due date |
| Quick Transfer | Panel | Allows standard nFinia internal transfer to linked accounts |

---

### Transaction History

The transaction list under the account detail. Shows all historical FICS loan transactions with date, payment type, amount, and remaining balance. Configurable by date range.

![Mortgage transaction history list](/.gitbook/assets/fics-004.jpg)

Expanding a transaction row reveals the full payment breakdown (principal, interest, tax and insurance, deferred principal, subsidy, unapplied) along with the exact **Paid date** and a **Download** button to export the transaction record.

![Expanded transaction detail with Download button](/.gitbook/assets/fics-005.jpg)

---

### Loan Information — About This Loan

The **About this loan** tab is the default view within the **Loan Information** section. It provides a comprehensive summary of all loan attributes and payment obligations.

![Loan Information screen showing all five tabs](/.gitbook/assets/fics-006.jpg)

![About This Loan — full loan details with APR, payment breakdown](/.gitbook/assets/fics-007.jpg)

| Field | Description |
|---|---|
| Property address | Physical address of the mortgaged property |
| Date registered | Date the mortgage was originated/registered |
| Next due payment amount | Amount of the next scheduled payment |
| Next due payment date | Date the next payment is due |
| Current interest rate | Stated as X.XXX% APR |
| Payment frequency | Monthly, bi-weekly, etc. |
| Remaining term | Months remaining |
| Maturity date | Final payment date of the loan |
| Current payment breakdown | Principal and interest / Tax and insurance / Total payment amount |
| Contact information | Home phone, Business phone, Email address, Mailing address with Edit link |

---

### Edit Contact Information

Accessible via the **Edit** link in the **Contact information** section of **About this loan**. Updates the contact record in FICS for this loan account.

![Update mortgage contact information modal](/.gitbook/assets/fics-008.jpg)

| Field | Required | Notes |
|---|---|---|
| First name | Optional | Pre-filled from FICS record |
| Last name | Optional | Pre-filled from FICS record |
| Address 1 | Required | Street address |
| Address 2 | Optional | Apartment/suite/unit |
| City/Town | Required | — |
| State | Required | Dropdown |
| ZIP Code | Required | — |
| Email address | Required | — |
| Phone number (Home) | Required | — |
| Business phone | Optional | — |
| Extension | Optional | — |

---

### Loan Information — Balances

The **Balances** tab provides a real-time breakdown of all balance components on the FICS loan, plus year-to-date payment totals.

![Balances tab — full balance breakdown and year-to-date totals](/.gitbook/assets/fics-009.jpg)

The **Download balances year-to-date totals** link opens a print-formatted view of the balance report, which you can save as a PDF. The report header includes the credit union name, generation date/time, member name, loan number, and loan account number.

![Downloaded balance PDF — year-to-date totals report](/.gitbook/assets/fics-010.jpg)

| Balance Component | Description |
|---|---|
| Principal | Outstanding principal balance |
| Deferred principal | Any deferred principal amount |
| Tax and insurance | Escrow balance for taxes and insurance |
| Subsidy | Any subsidy applied to the loan |
| Unapplied | Funds received but not yet applied |
| Unpaid late charges | Outstanding late fees |
| Returned check charges | NSF/returned check fees |
| Loss draft | Insurance loss draft balance |
| Negative amortization | Negative amortization amount if applicable |

---

### Loan Information — Account Notes

The **Account notes** tab displays servicer-entered notes for this loan. Members can search notes by keyword and filter by date range.

![Account Notes tab — search, date filter, and notes list](/.gitbook/assets/fics-011.jpg)

| Element | Description |
|---|---|
| Search for notes | Keyword search field |
| From / To date pickers | Filter notes by date range |
| Sort by | Dropdown — Newest first / Oldest first |
| Notes list | Displayed chronologically; shows note content |

---

### Loan Information — Help

The **Help** tab provides credit union mortgage contact information alongside a secure messaging form. Members can send a message directly to the mortgage department without leaving the banking session.

![Help tab — support contact info and secure messaging form](/.gitbook/assets/fics-012.jpg)

| Element | Description |
|---|---|
| Phone support timings | Credit union mortgage department hours |
| Mailing address | Physical mailing address |
| Send us a message | Free-text input, 249 character limit |
| Submit button | Sends secure message; activates only when message field is populated |

On successful submission, a green banner — _"Your message has been sent."_ — appears above the message field.

---

### Request Payoff Information

Accessible from the **Request payoff information** button on the **Loan Information** header. This function allows you to formally request a payoff quote from the credit union, specifying the delivery channel and date parameters.

![Request Payoff Information form — OLB view with field tooltips](/.gitbook/assets/fics-013.jpg)

![Request Payoff Information — Mobile Banking app view showing full form](/.gitbook/assets/fics-014.jpg)

| Field | Required | Description |
|---|---|---|
| I need this information on or before | Required | Date picker — desired receipt date for the payoff quote |
| Estimated date of payoff | Required | Date picker — intended mortgage payoff date |
| Send payoff information to | Required | Radio: My email / My mailing address / My fax number |
| Email field | Conditional | Shown when "My email" is selected; pre-filled from profile |
| Mailing address field | Conditional | Shown when "My mailing address" is selected |
| Fax number field | Conditional | Shown when "My fax number" is selected; member must enter |
| Phone number | Required | Pre-filled from profile; editable |

> **Note:** Both the **Payoff Date** and **Estimated payoff date** fields are required. Submitting without completing them returns field-level validation errors. The selected delivery channel field (email, address, or fax) is also required — leaving it blank triggers a validation error reading _"Send Payoff To field cannot be empty."_

On successful submission, the modal closes and a green confirmation banner appears on the Loan Information screen:

![Payoff request submitted — success confirmation banner](/.gitbook/assets/fics-015.jpg)

---

### Pay Now

The **Pay Now** button on the Account Detail screen redirects you to the FICS-integrated external payment portal via SSO. Before leaving the nFinia environment, the platform displays an **External Link Warning** dialog.

![External Link Warning — Pay Now SSO redirect confirmation](/.gitbook/assets/fics-016.jpg)

The dialog explains that you is navigating outside of nFinia to a third-party site and that the credit union is not responsible for the external site's policies. You may **Cancel** to stay, or click **Proceed** to complete the SSO handoff and open the payment portal.

---

### Account Settings — Hiding a FICS Loan

Members can control the visibility of their FICS loan accounts through **Account Settings** (accessible via the settings gear icon on the account). Accounts can be set to **Show account** or **Hide account**. Hidden accounts are suppressed from the primary Accounts view.

![Account Settings — Show/Hide a FICS loan account](/.gitbook/assets/fics-017.jpg)

> **Note:** Hiding a FICS loan via Account Settings suppresses it from the Accounts list but should not suppress it from the Mortgage feature. Ensure the correct visibility scoping is applied at the FI configuration level.

---

### Mobile Browser Experience

The Mortgage Balances — FICS feature is fully accessible through mobile browsers (Chrome, Safari). The layout adapts to smaller screens. Transaction detail screens display all fields vertically and include the same **Download** functionality available on desktop.

![Mobile browser — expanded transaction detail on mobile](/.gitbook/assets/fics-018.jpg)

---

## . Quick Reference

| Task | Navigation Path | Platform | Notes |
|---|---|---|---|
| Access mortgage accounts | Sidebar > Mortgage **or** Banking > Additional Services > Mortgage | OLB, Mobile | Requires active FICS loan linked to member account |
| View loan details (rate, term, address) | Mortgage account > View more loan information > About this loan | OLB, Mobile | Real-time FICS data |
| Edit contact information | About this loan > Edit (Contact information section) | OLB, Mobile | Updates FICS servicer record |
| View balance breakdown | Loan information > Balances | OLB, Mobile | Includes all escrow/fee components |
| Download year-to-date balance report | Loan information > Balances > Download balances year-to-date totals | OLB | Opens print dialog; save as PDF |
| View/search account notes | Loan information > Account notes | OLB, Mobile | Notes entered by servicer |
| Request payoff information | Loan information > Request payoff information | OLB, Mobile | Delivery via email, mail, or fax |
| Make a mortgage payment | Account detail > Pay Now | OLB, Mobile | SSO redirect to FICS payment portal |
| Send message to mortgage team | Loan information > Help > Send us a message | OLB, Mobile | 249-character limit |
| Download transaction record | Account detail > Transactions > [expand transaction] > Download | OLB, Mobile Browser | PDF per transaction |
| Access paperless statements | Loan information > Statement and documents | OLB | SSO redirect to FICS document portal |
| Hide/show a FICS loan | Account detail > Settings gear > Account Settings | OLB | Controls Accounts list visibility |
