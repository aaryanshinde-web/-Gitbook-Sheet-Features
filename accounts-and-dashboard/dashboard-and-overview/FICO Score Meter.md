**SUMMERVILLE FEDERAL CREDIT UNION**

nFinia Digital Banking Platform

**FICO® Score Meter**

Feature Documentation & Product Guide

Prepared by: Product Management

Date: April 8, 2026

Version: 1.0

**1. Product Summary**

The FICO® Score Meter is a self-service credit monitoring feature within the nFinia digital banking platform that provides credit union You with free access to their FICO® Score directly from their online banking portal. The feature displays your current credit score, a visual score meter with industry-standard ranges (300--850), and personalized key factors that are influencing their score. This empowers You to monitor their credit health without needing third-party services or hard inquiries.

This feature serves all retail banking You who hold active accounts with Summerville Federal Credit Union. It is accessible under the Additional Services navigation path and requires no special enrollment---You simply navigate to the FICO Score page to view their latest score. The score is pulled periodically from Experian data using the FICO® Score 8 model, which is the same scoring model the credit union uses for lending decisions.

The FICO® Score Meter lives under Home > Additional Services > FICO Score in the nFinia platform. The page presents a visual dashboard with your numeric score, a color-coded meter graphic (green through red), key factors affecting the score with educational explanations, and a link to additional credit education resources. A FICO® Score History section below provides trend tracking over time.

**At a Glance**

  -------------------------- --------------------------------------------------------------------------------------------
  **Attribute**              **Detail**
  **Feature Name**           FICO® Score Meter
  **Module**                 Home > Additional Services > FICO Score
  **User Roles**             Primary Account Holder, Joint Account Holder
  **Access Level**           Member self-service; no enrollment or admin approval required
  **Key Actions**            View Score, Review Key Factors, Access Credit Education, Track Score History
  **Score Model**            FICO® Score 8, based on Experian data
  **Score Range**            300 (min) to 850 (max)
  **Regulatory Relevance**   Fair Credit Reporting Act (FCRA), FICO trademark compliance, Experian data usage agreement
  -------------------------- --------------------------------------------------------------------------------------------

**2. Use Cases**

  -------------------------------- ---------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------
  **Use Case**                     **Who Uses It**        **What They Do**                                                                                                                                                **Business Value**
  **Check Credit Score**           Account Holder         Navigates to Additional Services > FICO Score to view their current FICO® Score displayed on a color-coded meter ranging from 300 to 850                       You stay informed about credit health without third-party services; reduces calls to member services about credit inquiries
  **Understand Score Factors**     Account Holder         Reviews the Key Factors section to understand what is positively or negatively impacting their score (e.g., account age, payment history)                       Financial literacy improvement; You can take actionable steps to improve their creditworthiness
  **Pre-Loan Self-Assessment**     Prospective Borrower   Checks FICO score before applying for a loan or credit card to gauge approval likelihood and expected rate tier                                                 Better-prepared loan applicants; fewer declined applications; You understand rate pricing
  **Track Score Over Time**        Account Holder         Scrolls to FICO Score History section to view score trends and changes across multiple reporting periods                                                        You can correlate financial behavior with score changes; promotes long-term financial planning
  **Access Credit Education**      Any Member             Clicks the "Click for more credit education" link to access educational resources about credit building, score improvement strategies, and financial wellness   Positions the credit union as a trusted financial advisor; supports NCUA financial literacy objectives
  **Monitor for Identity Theft**   Account Holder         Regularly checks score to detect unexpected drops that may indicate fraudulent accounts or unauthorized credit inquiries                                        Early fraud detection reduces member losses and credit union liability; builds trust in digital banking security
  -------------------------------- ---------------------- --------------------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------

These use cases demonstrate how the FICO® Score Meter serves both member empowerment and credit union strategic objectives for Summerville FCU. By providing free, no-impact access to credit scores within digital banking, the feature drives member engagement, reduces reliance on third-party credit monitoring services, and positions the credit union as a comprehensive financial wellness partner. The educational component is particularly valuable for You who may be building or rebuilding credit.

**3. End-to-End Workflow**

**3.1 Prerequisites**

-   Member must have an active deposit account (checking or savings) with Summerville FCU

-   Member must be authenticated and logged into the nFinia digital banking platform

-   FICO Score service must be enabled by the credit union in the nFinia platform configuration

-   Credit bureau data feed (Experian) must be active and you must have a reportable credit file

**3.2 Step-by-Step Flow**

1.  **Start from the Dashboard:** After logging into the nFinia digital banking platform, you land on the Account Overview / Dashboard page. This screen displays account balances, membership details, quick transfer options, and upcoming payments. To access the FICO Score feature, you navigate via the top navigation bar.

<figure><img src="/.gitbook/assets/0626ee68834c4ae05407526488a70359313c95cc.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 1: Dashboard --- Account Overview starting point*

2.  **Open the More Menu:** From the top navigation bar, you click More. The expanded menu hub reveals all available self-service features organized in a grid layout. you locates Additional Services or navigates directly to the FICO Score page from the available feature tiles.

<figure><img src="/.gitbook/assets/3255656de6c4325ca6347991aa2185fccc616569.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 2: More Menu --- Self-service feature hub*

3.  **View FICO® Score:** The FICO Score page loads displaying your current score prominently. The page includes: (a) the FICO® Score badge showing the numeric score (e.g., 400) with the tagline "The score lenders use," (b) a color-coded FICO® Score Meter graphic with ranges from 300 (min) through 580, 670, 740, 800, to 850 (max), and (c) the date the score was last pulled. The score is based on the FICO® Score 8 model using Experian data.

<figure><img src="/.gitbook/assets/79c37bde1ec9f0e2abda936af6cfe7b9639b23f0.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.041666666666667in" height="3.5416666666666665in"}

*Figure 3: FICO® Score Meter --- Score display with key factors and credit education*

4.  **Review Key Factors:** To the right of the score meter, the Key Factors section displays personalized explanations of what is affecting your score. Each factor includes a bold title and detailed explanation. Common factors include: (1) "Length of time accounts have been established" --- explains how the age of the oldest account and average account age impact the score, and (2) "Too few accounts currently paid as agreed" --- explains how missed payments or low number of accounts in good standing affect the score. Each factor includes a "Keep in mind" section with actionable guidance.

5.  **Access Credit Education:** At the bottom of the FICO Score card, you can click "Click for more credit education" to access additional resources about credit building, score improvement strategies, and financial wellness content. This link redirects to educational materials provided through the credit bureau partnership.

6.  **View Score History:** Below the main FICO Score card, the "Your FICO® Score History" section displays a historical timeline of your score changes across multiple reporting periods. This allows you to track trends, identify improvements or declines, and correlate score changes with financial behavior.

**3.3 Decision Points & Branching**

-   **No Credit File:** If you does not have a reportable credit file with Experian, the system displays an informational message explaining that a FICO Score cannot be generated. you are advised to contact the credit union for further assistance.

-   **Score Improvement vs. Decline:** The Key Factors section dynamically adjusts based on your current score profile. You with declining scores see factors focused on areas needing improvement, while You with stable or improving scores see reinforcing factors.

-   **Multiple Memberships:** The FICO Score is tied to your credit profile (SSN-based), not individual accounts. You with multiple memberships see the same score across all memberships.

**3.4 Completion & Confirmation**

The FICO Score page is a read-only informational display. There is no submission or confirmation step. The score updates automatically based on the credit bureau's reporting cycle (typically monthly). The "pulled on" date at the bottom of the score card confirms when the score was last refreshed. You can return to this page at any time to check their current score without impacting their credit.

**3.5 Error Handling**

-   **Service Unavailable:** If the FICO Score service is temporarily unavailable or the credit bureau data feed is interrupted, the page displays an appropriate error message and advises you to try again later.

-   **Score Not Available:** For new You or You without sufficient credit history, the system explains that a score cannot be generated and provides guidance on building credit.

-   **Data Refresh Delay:** If the score has not been updated within the expected cycle, the "pulled on" date helps you and support staff identify whether a refresh is pending.

**4. Feature Overview (UI Walkthrough)**

**4.1 FICO® Score Display Card**

The primary score display card occupies the left portion of the FICO Score page. It provides your numeric score, visual meter, and branding information. (See Figure 3 in Section 3.)

  ----------------------- --------------- --------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------
  **Field / Element**     **Type**        **Description**                                                                                                                   **Notes**
  FICO® Score Badge       Display         Shows your numeric FICO score in large bold text with "FICO SCORE --- The score lenders use" branding                     Read-only; updates on credit bureau cycle
  Score Meter Graphic     Visualization   Color-coded semicircular gauge showing score position within the 300--850 range. Green (high) through yellow (mid) to red (low)   Ranges: 300, 580, 670, 740, 800, 850
  Score Pull Date         Label           Displays when the score was last retrieved: "The FICO Score pulled on [date] is the FICO Score 8 based on Experian data"        Confirms data freshness
  Credit Education Link   Link            "Click for more credit education" --- navigates to external credit education resources                                            Opens in new window/tab
  FICO Trademark Notice   Label           Legal disclaimer: "FICO and 'The score lenders use' are registered trademarks of Fair Isaac Corporation"                          Required for FICO branding compliance
  ----------------------- --------------- --------------------------------------------------------------------------------------------------------------------------------- -------------------------------------------

**4.2 Key Factors Panel**

The Key Factors section appears to the right of the score card and provides personalized explanations of the primary drivers affecting your credit score. (See Figure 3 in Section 3.)

  --------------------- -------------- -------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------
  **Field / Element**   **Type**       **Description**                                                                                          **Notes**
  Factor Title          Label (Bold)   Numbered factor name (e.g., "1. Length of time accounts have been established")                          Typically 2--4 factors displayed
  Factor Explanation    Text Block     Detailed explanation of how this factor impacts the score, referencing your specific situation   Personalized per your credit profile
  Keep in Mind          Text Block     Actionable guidance section explaining what behaviors generally improve or worsen this factor            Educational content; same across all You with this factor
  --------------------- -------------- -------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------

**4.3 Score History**

The FICO Score History section appears below the main score card and provides a chronological view of score changes over time. This enables You to track their credit trajectory and correlate financial decisions with score movements.

  ------------------------- --------------- ------------------------------------------------------------------------------- -----------------------------------------
  **Field / Element**       **Type**        **Description**                                                                 **Notes**
  Score History Chart       Visualization   Timeline or chart showing FICO Score values across multiple reporting periods   Updates with each new score pull
  Historical Score Values   Data Points     Individual score values with corresponding dates for each reporting period      Typically shows 6--12 months of history
  ------------------------- --------------- ------------------------------------------------------------------------------- -----------------------------------------

**5. Quick Reference**

  ------------------------- -------------------------------------------------------- ------------------- -----------------------------------------
  **Task**                  **Navigation Path**                                      **Who Can Do It**   **Notes**
  View FICO Score           Additional Services > FICO Score                        Account Holder      No enrollment required; read-only
  Review Key Factors        Additional Services > FICO Score > Key Factors panel   Account Holder      Personalized to your credit profile
  Track Score History       Additional Services > FICO Score > Score History       Account Holder      Shows 6--12 months of score changes
  Access Credit Education   FICO Score page > "Credit education" link               Any Member          External resource; opens new tab
  Verify Score Freshness    FICO Score page > "Pulled on" date                      Account Holder      Score refreshes on credit bureau cycle
  Contact Support           FICO Score page > Support button                        Any Member          Chat widget for live assistance
  ------------------------- -------------------------------------------------------- ------------------- -----------------------------------------

*--- End of Document ---*
