**SUMMERVILLE FEDERAL CREDIT UNION**

nFinia Digital Banking Platform

**Reward Points & Credit Card Management**

Product Feature Guide

Prepared by: Jeeva Krishnamurthy, Senior Product Manager

Tyfone, Inc. \| April 2026

**1. Product Summary**

The Reward Points & Credit Card Management module within the nFinia digital banking platform provides credit union You with comprehensive visibility into their credit card accounts and associated reward programs. You can view credit card balances, available credit, payment due dates, and total amounts owed directly from their account dashboard. The reward points subsystem surfaces earned, available, redeemed, and expiring point balances at a glance, enabling You to make timely redemption decisions before points expire.

This feature serves individual and business You who hold credit card products issued through Summerville Federal Credit Union. It integrates with the card processor to display real-time card status (Active/Locked/Unlocked), linked card numbers, and cardholder names. For credit unions, offering a transparent, self-service reward points experience directly within the digital banking platform reduces call center volume, increases card engagement, and strengthens member loyalty by making reward value immediately visible and actionable.

The module lives under the Accounts section of nFinia. You access it by selecting their credit card account from the account overview. The reward points detail is available both inline on the credit card account page and via a dedicated Reward Points popup modal that provides a tabular breakdown of all linked cards and their individual reward balances.

**At a Glance**

  ---------------------- -------------------------------------------------------------------------------------
  **Attribute**          **Detail**
  Feature Name           Reward Points & Credit Card Management
  Module                 Dashboard > More Menu > Credit Card > Reward Points
  User Roles             Primary Member, Joint Account Holder, Business Owner
  Access Level           Account-level (visible to You with credit card products)
  Key Actions            View Card Details, Check Reward Balance, Redeem Points, View Expiring Points
  Regulatory Relevance   TILA disclosure compliance, card status transparency, PCI-DSS (masked card numbers)
  ---------------------- -------------------------------------------------------------------------------------

**2. Use Cases**

  ------------------------------------ ------------------------------- ----------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------
  **Use Case**                         **Who Uses It**                 **What They Do**                                                                                                                    **Business Value**
  Check reward points balance          Primary Member                  Opens credit card account page, views earned/available/redeemed/expiring points at a glance                                         Increases reward awareness and encourages card usage; reduces call center inquiries about point balances
  Redeem reward points                 Primary Member                  Clicks Redeem/View link from credit card page or Reward Points modal to initiate redemption                                         Drives member engagement with card products; improves card profitability through increased transaction volume
  Monitor expiring points              Primary Member / Joint Holder   Reviews expiring points count and expiration date; plans redemption before points lapse                                             Reduces member dissatisfaction from lost points; proactive notification drives redemption activity
  Review linked card details           Business Owner / Admin          Opens Reward Points modal to see all linked cards, their status (Active/Locked), cardholder names, and individual reward balances   Enables business account managers to track employee card rewards across the organization
  Verify card status                   Primary Member                  Checks card lock/unlock status and toggles as needed from the Cards in Account section                                              Self-service card control reduces fraud risk and eliminates the need to call the credit union
  View credit card statement summary   Primary Member                  Reviews credit limit, available credit, payment due date, and total due from the card overview section                              Enables informed financial decisions; transparent disclosure supports TILA compliance
  ------------------------------------ ------------------------------- ----------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------

These use cases reflect the primary ways credit union You interact with their credit card and reward point information. For Summerville FCU, providing this self-service experience directly in the digital banking platform eliminates the need for You to call in or use a separate card processor portal, creating a unified experience that strengthens the credit union\'s digital relationship with its You.

**3. End-to-End Workflow**

**3.1 Prerequisites**

- Member must be enrolled in nFinia digital banking with active credentials.

- Member must hold at least one credit card product issued through the credit union.

- Credit card must be linked to you\'s digital banking profile by the FI.

- Reward points program must be enabled on the card product by the card processor.

**3.2 Step-by-Step Flow**

Step 1: Member logs into nFinia digital banking and lands on the Dashboard. The account overview displays all linked accounts including checking, savings, and credit card accounts with current balances. The bottom navigation provides quick links and the More menu for accessing additional features.

<figure><img src="/.gitbook/assets/24c30f617e73e6629d17809c27be42eacd3ba8fb.png" alt="" width="340"><figcaption></figcaption></figure>{width="3.75in" height="5.885416666666667in"}

The Dashboard shows you\'s full account portfolio at a glance. Credit card accounts are listed alongside deposit accounts, displaying the current balance. you can navigate to specific features through the top navigation bar or the More menu hub at the bottom of the page.

Step 2: Member taps the \'More\' option from the bottom navigation or the +More menu link. The More Menu Hub opens, displaying a grid of all available banking features organized by category.

<figure><img src="/.gitbook/assets/5d113ae19a7e22fd64da3337eeb9f7f8da6a8917.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.833333333333333in" height="3.3645833333333335in"}

The More Menu Hub provides a centralized navigation point for features beyond the primary tabs. You can access Cards, Check Services, Reward Points, Skip-a-Pay, and other account management features from this hub. you select the credit card account or navigates to the Cards section to access reward points.

Step 3: Member selects the credit card account (e.g., \'P-Money\'s Credit Card (\#160)\') from the Accounts section. The system navigates to the Credit Card Account Detail view showing the full card summary and reward points balance.

<figure><img src="/.gitbook/assets/3ac017b513676685e7cb991f11e2120fc2e369ad.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.833333333333333in" height="2.8333333333333335in"}

The Credit Card Account Detail screen displays: card image and name, credit limit (\$5,000.00), available credit (\$1,241.67), payment due date and amount, total due (\$3,758.33). Below the summary, the \'Cards in this account\' section shows linked card numbers (masked), card type (Visa Signature), cardholder name, and lock/unlock status toggle. The Reward Points summary row shows Earned to Date (3,914 points), Rewards Points Available (57,496), Redeemed to Date (0 points), and Expiring Points (58 points on 04/30/2025).

Step 4: Member clicks \'Redeem/View\' link to open the Reward Points modal for detailed information and card-level breakdown.

<figure><img src="/.gitbook/assets/86142214e31c42bcdc8c075973a8c2595fb98abd.png" alt="" width="620"><figcaption></figcaption></figure>{width="5.833333333333333in" height="1.8958333333333333in"}

The Reward Points modal displays a card-level breakdown: card number (masked), status (ACTIVE), cardholder name (PERCIVAL F CEREZO), and a Redeem/View action link. The summary header shows: Earned to Date (0 points for current period), Rewards Points Available (3,000), Redeemed to Date (-2,500), and Expiring Points (3,000 on 11/30/2028).

Step 5: Member clicks \'Redeem/View\' within the modal to navigate to the card processor\'s reward redemption interface or an embedded redemption workflow.

**3.3 Decision Points & Branching**

- If you have no credit card products, the credit card section does not appear in the Accounts view.

- If the reward points program is not enabled on the card, the reward points row is hidden.

- If the card is locked, you see \'Locked\' status and must unlock before certain card actions are available.

- If points are expiring soon, the expiring points count and date are highlighted to prompt action.

**3.4 Completion & Confirmation**

Upon viewing reward points, no system state changes occur (read-only operation). When a member initiates a redemption through the Redeem/View link, the system routes to the card processor\'s redemption flow. Upon successful redemption, the Redeemed to Date counter increments and Available Points decreases accordingly. you receive a confirmation notification within the nFinia Inbox.

**3.5 Error Handling**

- Card processor unavailable: The system displays \'Reward points information is temporarily unavailable. Please try again later.\' The credit card balance information remains visible from cached data.

- Insufficient points for redemption: The redemption interface validates the minimum point threshold and prevents submission with an inline error message.

- Session timeout during redemption: you are redirected to login; partial redemptions are not processed.

**4. Feature Overview (UI Walkthrough)**

**Credit Card Account Detail Screen**

This is the primary screen You see when selecting a credit card account. It provides a complete snapshot of the card\'s financial status and reward points.

  -------------------------- ---------------- ---------------------------------------------------------------------------------------------------- -----------------------------------------------
  **Field / Element**        **Type**         **Description**                                                                                      **Notes**
  Card Image & Name          Label            Displays card artwork, product name, and account number (e.g., \'P-Money\'s Credit Card (\#160)\')   Read-only; sourced from card processor
  Credit Limit               Label            Maximum credit line on the account (e.g., \$5,000.00)                                                Read-only
  Available Credit           Label            Remaining available credit (e.g., \$1,241.67)                                                        Read-only; updates in real-time
  Due Date / Amount          Label            Next payment due date and minimum payment amount                                                     Read-only; supports TILA disclosure
  Total Due                  Label            Full outstanding balance (e.g., \$3,758.33)                                                          Read-only
  Card Number                Label (masked)   Last 4 digits of linked card (e.g., xxxx-xxxx-xxxx-8960)                                             PCI-DSS compliant masking
  Card Type                  Label            Card brand and tier (e.g., Visa Signature)                                                           Read-only
  Cardholder Name            Label            Full name on card (e.g., PERCIVAL F CEREZO)                                                          Read-only
  Status Toggle              Toggle           Locked / Unlocked card status with inline toggle switch                                              you can lock/unlock card instantly
  Earned to Date             Label            Cumulative points earned since account opening (e.g., 3,914)                                         Read-only
  Rewards Points Available   Label            Current redeemable point balance (e.g., 57,496)                                                      Read-only
  Redeemed to Date           Label            Cumulative points redeemed (e.g., 0 points)                                                          Read-only
  Expiring Points            Label            Points expiring with date (e.g., 58 points on 04/30/2025)                                            Highlighted when expiration is within 90 days
  View Account               Link             Navigates to detailed account transaction history                                                    Opens in same view
  Redeem/View                Link             Opens Reward Points modal or navigates to redemption interface                                       Primary CTA for reward interaction
  -------------------------- ---------------- ---------------------------------------------------------------------------------------------------- -----------------------------------------------

**Reward Points Modal**

This modal provides a card-level breakdown of reward points across all linked cards on the credit card account. It is triggered by clicking \'Redeem/View\' on the credit card detail screen.

  -------------------------- ---------------- ------------------------------------------------------------------------------ ---------------------------------------------
  **Field / Element**        **Type**         **Description**                                                                **Notes**
  Earned to Date             Label            Points earned in the current reporting period                                  May differ from lifetime total on main page
  Rewards Points Available   Label            Current redeemable balance across all linked cards                             Real-time from processor
  Redeemed to Date           Label            Points redeemed in the current period (negative value indicates redemptions)   Negative format (e.g., -2,500)
  Expiring Points            Label            Points expiring with date across all cards                                     Includes expiration date
  Card Number                Label (masked)   Last 4 digits of each linked card in table format                              PCI-DSS compliant
  Status                     Label            Card status (ACTIVE, LOCKED, CLOSED)                                           Color-coded: green for ACTIVE
  Name on Card               Label            Cardholder name for each linked card                                           Read-only
  Reward Points              Link             Redeem/View action link per card for individual card redemption                Opens processor redemption flow
  Close (X)                  Button           Closes the modal and returns to credit card detail screen                      Top-right corner
  -------------------------- ---------------- ------------------------------------------------------------------------------ ---------------------------------------------

**5. Quick Reference**

  ----------------------------- ------------------------------------------------------------------------- ------------------------------ ---------------------------------------------------------
  **Task**                      **Navigation Path**                                                       **Who Can Do It**              **Notes**
  View credit card balance      Dashboard > More Menu > [Credit Card Name]                            Primary Member, Joint Holder   Shows credit limit, available credit, amounts due
  Check reward points balance   Dashboard > More Menu > [Credit Card] > Reward Points row            Primary Member                 Inline display of earned, available, redeemed, expiring
  Open Reward Points modal      Dashboard > More Menu > [Credit Card] > Redeem/View                  Primary Member                 Shows card-level breakdown with redemption links
  Redeem reward points          Reward Points modal > Redeem/View (per card)                             Primary Member                 Routes to card processor redemption interface
  Lock/Unlock card              Dashboard > More Menu > [Credit Card] > Cards in Account > Toggle   Primary Member                 Instant card control; no call to CU required
  View account transactions     Dashboard > More Menu > [Credit Card] > View Account                 Primary Member, Joint Holder   Full transaction history with filters
  ----------------------------- ------------------------------------------------------------------------- ------------------------------ ---------------------------------------------------------

**6. Conclusion**

The Reward Points & Credit Card Management module delivers a self-service, transparent experience for Summerville FCU You to manage their credit card accounts and maximize the value of their reward programs. By integrating real-time card data, reward balances, and redemption capabilities directly into the nFinia digital banking platform, the credit union eliminates the need for You to navigate separate card processor portals or contact the call center for routine reward inquiries.

Key benefits for Summerville FCU include reduced operational costs from fewer inbound calls about reward balances, increased credit card engagement through visibility of available and expiring points, and strengthened member loyalty through a unified digital experience. The PCI-DSS compliant card masking and TILA-aligned disclosure of credit terms ensure regulatory compliance while maintaining a member-friendly interface.

Future enhancements may include push notifications for expiring points, reward point projections based on spending patterns, and one-click redemption for statement credits directly within the nFinia platform.
