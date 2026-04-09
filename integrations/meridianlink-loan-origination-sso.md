# MeridianLink Loan Origination — SSO Integration Guide

**Feature:** MeridianLink Loan Origination — Single Sign-On (SSO)
**Platform:** nFinia Digital Banking (Tyfone)
**Credit Union:** Summerville Credit Union
**Prepared by:** Jeeva Krishnamurthy, Senior Product Manager, Business Banking

---

## Section 1 — Product Summary

The MeridianLink Loan Origination SSO feature enables authenticated nFinia digital banking members to initiate loan applications directly from within the online banking portal and be seamlessly transferred into the MeridianLink Consumer Loan Origination System (LOS) — without re-entering credentials or personal information. When a member clicks "Apply for Loans" inside nFinia, the platform passes a secure tokenized reference (tenderref) to MeridianLink, establishing a pre-authenticated session on the member's behalf. This eliminates the friction of a separate login, reduces application abandonment, and positions the credit union's digital lending as a fully integrated experience rather than a bolted-on external tool.

The feature serves authenticated retail members — both primary account holders and joint members — who have an active nFinia session. From the credit union's operational perspective, it also serves loan officers and digital banking administrators who need to ensure the application funnel is functioning correctly and that referral context is passed accurately to MeridianLink for proper pipeline attribution.

For the credit union, this integration directly impacts loan volume by reducing the steps required to start an application. Historically, redirecting members to an external LOS meant re-authentication, re-entry of known data, and significant drop-off. With SSO, the member's identity context travels with them into MeridianLink's "Apply in 3 Steps" flow, creating a cohesive brand experience under the Summerville Credit Union identity. For the member, the benefit is speed and confidence — they are never asked to prove who they are twice within the same session.

This feature lives in the nFinia platform under **Banking > More > Apply for Loans**, and connects outward to the MeridianLink consumer portal at `app.consumer.meridianlink.com`.

| Attribute | Detail |
|---|---|
| Feature Name | MeridianLink Loan Origination — SSO |
| Module | Banking > More > Apply for Loans |
| User Roles | Authenticated Retail Member, Joint Member |
| Access Level | Session-authenticated (active nFinia login required) |
| Key Actions | Select loan type, initiate SSO redirect, complete application in MeridianLink |
| Regulatory Relevance | Identity verification via existing nFinia auth; audit trail via tenderref token; fair lending consistency |

---

## Section 2 — Use Cases

| Use Case | Who Uses It | What They Do | Business Value |
|---|---|---|---|
| Apply for a Personal Loan | Authenticated member | Navigates to Apply for Loans, selects Personal Loans, is SSO'd into MeridianLink Personal Loan flow with credit union branding; selects loan type (Line of Credit, Debt Consolidation, Signature) | Reduces application abandonment; member completes application in one continuous session |
| Apply for a Vehicle Loan | Authenticated member | Selects Vehicle Loans from the Apply for Loans menu; MeridianLink Vehicle Loan flow launches with purpose options (New Car or Truck, New Boat, Motor Home/Travel Trailer, New Motorcycle) | Captures auto lending opportunity at the digital point of need; no separate portal login |
| Apply for a Credit Card | Authenticated member | Selects Credit Cards; MeridianLink Credit Card flow presents purpose selection (Line Increase, MasterCard) | Drives card product cross-sell directly from digital banking; consistent brand experience |
| Token-based identity handoff | nFinia platform + MeridianLink | nFinia generates a tenderref token unique to the member's session (e.g., AMLAKECUG20723) and appends it to the MeridianLink redirect URL | Enables secure, cookieless session handoff without transmitting credentials; supports audit trail and application attribution |
| Credit union branding continuity | Member navigating the application | MeridianLink renders the Summerville Credit Union logo and branding across the Apply in 3 Steps flow | Maintains member trust and brand recognition; reduces perception of leaving the credit union's environment |
| Application dropout recovery | Loan officer / Digital Admin | Monitors MeridianLink pipeline for incomplete applications; tenderref token links back to the originating nFinia member record | Enables proactive outreach to members who started but did not complete an application |

The SSO integration is especially valuable for credit unions like Summerville that serve members who may not distinguish between the digital banking app and the loan application experience. By presenting a unified, branded journey, the credit union reduces cognitive friction at the exact moment a lending decision is being made.

---

## Section 3 — End-to-End Workflow

### 3.1 Prerequisites

- Member must have an active, authenticated nFinia digital banking session (username + password verified; MFA completed if required).
- The MeridianLink SSO integration must be configured in the nFinia back-office with the credit union's MeridianLink tenant URL and tenderref generation logic.
- The member's account must be in good standing (no hard login locks or security freezes that would block session continuation).
- MeridianLink must have the credit union's consumer portal active and the relevant loan products (Personal, Vehicle, Credit Card) enabled.

### 3.2 Step-by-Step Flow

**Step 1 — Navigate to Apply for Loans**
The authenticated member is on the nFinia dashboard. They navigate to **Banking > More > Apply for Loans**. The Apply for Loans screen displays three product categories: Personal Loans, Vehicle Loans, and Credit Cards. Upcoming payment summaries may be displayed in a right-side panel for context.

**Step 2 — Select a Loan Type**
The member clicks one of the three loan type options. The nFinia platform registers the selection and initiates the SSO handoff process.

**Step 3 — Token Generation (System)**
nFinia generates a unique tenderref token tied to the member's current session and account identity (e.g., `AMLAKECUG20723`). This token encodes the credit union identifier and is used by MeridianLink to validate the source of the request and pre-populate known member data.

**Step 4 — Redirect to MeridianLink**
The member's browser is redirected to the appropriate MeridianLink consumer portal URL with the tenderref appended as a query parameter:
- Personal Loan: `app.consumer.meridianlink.com/pl/PersonalLoan.aspx?tenderref=AMLAKECUG020723`
- Vehicle Loan: `app.consumer.meridianlink.com/vl/VehicleLoan.aspx?tenderref=AMLAKECUG020723`
- Credit Card: `app.consumer.meridianlink.com/cc/CreditCard.aspx?tenderref=AMLAKECUG020723`

**Step 5 — MeridianLink Receives and Validates Token**
MeridianLink validates the tenderref against the credit union's integration configuration. Upon successful validation, the member's session is established in MeridianLink without requiring a separate login. The Summerville Credit Union logo and branding are rendered.

**Step 6 — Product Purpose Selection**
The member is presented with the "Apply in 3 Steps" flow header and prompted to select a purpose for their loan. This is the first active data entry step in the MeridianLink application. Options vary by product type (see Section 4 for field details).

**Step 7 — Complete the 3-Step Application**
The member progresses through MeridianLink's standard three-step application flow: (1) Loan Purpose & Product Selection, (2) Personal / Financial Information, (3) Review & Submit. Pre-populated fields from the tenderref reduce data entry burden.

**Step 8 — Submission and Pipeline Entry**
Upon submission, the application enters the credit union's MeridianLink loan pipeline for processing by the lending team. The member receives an on-screen confirmation and may receive an email notification from MeridianLink.

### 3.3 Decision Points & Branching

- **If the member selects Personal Loans:** They are presented with an initial qualifier — "This is a Line of Credit" — before selecting a purpose (Debt Consolidation, Signature). This determines the loan product sub-type routed in MeridianLink.
- **If the member selects Vehicle Loans:** They proceed directly to purpose selection (Motor Home/Travel Trailer, New Boat, New Car or Truck, New Motorcycle) with no preliminary qualifier.
- **If the member selects Credit Cards:** They select a purpose (Line Increase, MasterCard) and proceed to Continue. The Credit Card flow is the most abbreviated at the purpose-selection stage.
- **If the tenderref is invalid or expired:** MeridianLink will reject the handoff. The member may see an error page on the MeridianLink portal. Resolution requires the member to return to nFinia and re-initiate the flow.
- **If the member is not authenticated in nFinia:** The Apply for Loans option is not accessible — authentication is enforced at the nFinia session level before the SSO link is ever generated.

### 3.4 Completion & Confirmation

Upon submitting the completed application in MeridianLink, the member receives a confirmation screen within the MeridianLink portal indicating the application has been received. The application is logged in the credit union's MeridianLink pipeline with the tenderref as the origination identifier. No explicit confirmation is sent back to the nFinia session (the member remains on the MeridianLink portal after submission).

### 3.5 Error Handling

- **Invalid tenderref:** Member sees a MeridianLink error page. Advised to return to the digital banking portal and retry. No member data is exposed.
- **MeridianLink portal unavailable:** Member is unable to complete the redirect. nFinia does not currently display a custom error page for LOS unavailability — the browser will show a standard connection error.
- **Session timeout in nFinia before redirect completes:** The tenderref may not be generated. Member will need to log back into nFinia and re-initiate the flow.
- **Unsupported loan product:** If a product is not enabled in the credit union's MeridianLink configuration, the member may reach a blank or error state on the MeridianLink portal. Credit union admins should verify product enablement matches what is displayed in nFinia.

---

## Section 4 — Feature Overview (UI Walkthrough)

### Screen 1 — Apply for Loans (nFinia Portal)

This is the entry point screen within the nFinia digital banking portal. It presents the three available loan product categories and serves as the launch pad for all MeridianLink SSO redirects. The URL remains within the nFinia domain (`summerville.nfinia.com

![Apply for Loans — nFinia Portal](/.gitbook/assets/meridian-001.png)

| Field / Element | Type | Description | Notes |
|---|---|---|---|
| Personal Loans | Navigation link | Initiates SSO redirect to MeridianLink Personal Loan application | Redirects to /pl/PersonalLoan.aspx |
| Vehicle Loans | Navigation link | Initiates SSO redirect to MeridianLink Vehicle Loan application | Redirects to /vl/VehicleLoan.aspx |
| Credit Cards | Navigation link | Initiates SSO redirect to MeridianLink Credit Card application | Redirects to /cc/CreditCard.aspx |
| Upcoming Payments panel | Informational display | Shows member's upcoming payment obligations for context | Read-only; does not affect loan application flow |
| Navigate to (search bar) | Input / Navigation | Allows member to navigate to other nFinia features | Not specific to loan application; standard nFinia navigation widget |

---

### Screen 2 — Personal Loan Application (MeridianLink)

After selecting Personal Loans, the member is redirected to the MeridianLink consumer portal displaying the Personal Loan application. The credit union's branding (Summerville Credit Union logo) is rendered. The "Apply in 3 Steps" progress indicator is shown at the top. This is Step 1 of the MeridianLink application flow.

![Personal Loan Application — MeridianLink](/.gitbook/assets/meridian-002.png)

| Field / Element | Type | Description | Notes |
|---|---|---|---|
| Apply in 3 Steps (header) | Progress indicator | Visual step tracker showing the member's position in the 3-step application | Steps are: Purpose Selection → Personal Info → Review & Submit |
| Summerville Credit Union logo | Branding element | Credit union logo rendered by MeridianLink using SSO configuration | Maintained for brand continuity |
| "This is a Line of Credit" | Selection button | Qualifier that categorizes the personal loan as a revolving line of credit product | Clicking this modifies the loan sub-type routed in MeridianLink |
| Select a purpose (required) | Selection group | Purpose field for the personal loan; options include Debt Consolidation and Signature | Required field; drives product routing in LOS |
| Debt Consolidation | Selection button | Indicates purpose of consolidating existing debts | Standard personal loan purpose code |
| Signature | Selection button | Unsecured signature loan — no collateral | Standard personal loan purpose code |

---

### Screen 3 — Vehicle Loan Application (MeridianLink)

After selecting Vehicle Loans, the member lands on the MeridianLink Vehicle Loan application. Purpose selection is the first data entry point, with options reflecting the credit union's enabled vehicle loan products.

![Vehicle Loan Application — MeridianLink](/.gitbook/assets/meridian-003.png)

| Field / Element | Type | Description | Notes |
|---|---|---|---|
| Apply in 3 Steps (header) | Progress indicator | Same 3-step flow as Personal Loan; consistent across all product types | |
| Summerville Credit Union logo | Branding element | SSO-configured branding maintained in MeridianLink vehicle loan flow | |
| Select a purpose (required) | Selection group | Vehicle loan purpose; determines collateral type and underwriting path | Required field |
| Motor Home / Travel Trailer | Selection button | Recreational vehicle loan category | Maps to specific collateral and LTV guidelines |
| New Boat | Selection button | Marine loan category | |
| New Car or Truck | Selection button | Standard auto loan — new vehicle | Most common vehicle loan purpose |
| New Motorcycle | Selection button | Motorcycle loan category | |

---

### Screen 4 — Credit Card Application (MeridianLink)

After selecting Credit Cards, the member sees the MeridianLink Credit Card application. This is the most streamlined of the three product flows at the purpose-selection stage, offering two options and a Continue button to advance.

![Credit Card Application — MeridianLink](/.gitbook/assets/meridian-004.png)

| Field / Element | Type | Description | Notes |
|---|---|---|---|
| Apply in 3 Steps (header) | Progress indicator | Consistent 3-step flow across all product types | |
| Summerville Credit Union logo | Branding element | Credit union branding maintained via SSO configuration | |
| Select a purpose (required) | Selection group | Credit card purpose; drives product routing | Required field; marked with asterisk |
| Line Increase | Selection button | Request to increase the credit limit on an existing card | Not a new account application — modifies existing account |
| MasterCard | Selection button | New MasterCard credit card application | New account origination path |
| *Required Field(s) | Form note | Indicates the purpose field is mandatory before proceeding | Standard MeridianLink form validation |
| Continue | Action button | Advances the member to the next step in the application flow | Disabled or inactive until a purpose is selected |

---

## Section 5 — Quick Reference

| Task | Navigation Path | Who Can Do It | Notes |
|---|---|---|---|
| Apply for a Personal Loan | Banking > More > Apply for Loans > Personal Loans | Authenticated retail member | SSO redirect to MeridianLink; tenderref auto-generated |
| Apply for a Vehicle Loan | Banking > More > Apply for Loans > Vehicle Loans | Authenticated retail member | Purpose options: Motor Home, Boat, Car/Truck, Motorcycle |
| Apply for a Credit Card | Banking > More > Apply for Loans > Credit Cards | Authenticated retail member | Options: Line Increase or new MasterCard |
| Verify SSO integration is active | nFinia back-office > Integrations > MeridianLink SSO | Credit union digital banking admin | Check tenderref generation config and MeridianLink tenant URL |
| Monitor loan pipeline from SSO-originated applications | MeridianLink loan pipeline > filter by tenderref prefix | Loan officer / LOS admin | tenderref prefix (e.g., AMLAKECU) identifies nFinia-originated applications |
| Retry failed SSO redirect | Return to Banking > More > Apply for Loans and re-select loan type | Authenticated member | Generates a fresh tenderref; resolves most token expiry errors |

---

*Guide prepared by Jeeva Krishnamurthy, Senior Product Manager — Tyfone nFinia Platform. For integration configuration questions, contact the Tyfone implementation team. For MeridianLink LOS product questions, contact your MeridianLink relationship manager.*
