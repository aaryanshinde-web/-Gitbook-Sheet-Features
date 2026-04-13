# Marketing Automation - Prisma

***

## Summary

Prisma is an advertising and engagement platform integrated with Tyfone's nFinia digital banking product. It enables Financial Institutions (FIs) — primarily credit unions and community banks — to display targeted advertisements within their members' digital banking experience: dashboard, account history, transfers, bill pay, and more. The integration is token-based, with Tyfone embedding Prisma placeholders throughout the application and passing a person-level user identifier at login to load personalized ad content.

The primary users of the Prisma console are FI marketing teams and Tyfone delivery/support managers who configure, schedule, and manage ad campaigns. End members (credit union members) are the consumers of these ads. For FIs, Prisma represents a direct revenue opportunity — either by monetizing ad inventory through partner offers or by promoting your own financial products (e.g., auto loans, credit cards, certificates) to you at key moments in your digital banking journey.

| Attribute    | Detail                                                                                               |
| ------------ | ---------------------------------------------------------------------------------------------------- |
| Feature Name | Prisma Ad Integration                                                                                |
| Module       | nFinia Platform — Advertising & Engagement Layer                                                     |
| Key Actions  | Create/configure banners, upload creatives, set targeting, publish, track analytics, manage opt-outs |

***

## Introduction to Prisma

Prisma is an advertising functionality that allows ads to be displayed within various sections of members' banking dashboards and account history. It serves as the campaign management and ad delivery layer for FIs using the nFinia platform. The integration is token-based: Tyfone embeds Prisma ad placeholders throughout nFinia and passes the member's person-level identifier at login, which Prisma uses to serve the appropriate ad content.

**At a high level, Prisma enables FIs to:**

* Display financial product promotions, partner offers, or awareness campaigns directly inside the digital banking app
* Segment audiences by demographics or custom profile attributes (Full version)
* Track campaign reach, click-through, and conversion analytics
* Manage email and SMS campaigns in addition to in-app banners
* Maintain regulatory compliance with marketing opt-out workflows (CCPA)

***

## Key Features and Functionality

### Ad Placement and Display

Prisma supports IAB (International Advertising Bureau) standard ad sizes across multiple placement zones within the nFinia application interface.

| Ad Type                     | Typical Dimensions                 | Placement                                            |
| --------------------------- | ---------------------------------- | ---------------------------------------------------- |
| Leaderboard Top/Bottom      | 728 × 90 px                        | Between page title and content, or bottom of content |
| Square Pop-up (Side Widget) | 250 × 250 px                       | Sidebar top and sidebar bottom                       |
| Full Pop-up / Interstitial  | iPhone: 400 × 300 px; iPad: larger | Overlay on content; limited to certain mobile pages  |
| Mobile Login Banner         | 325 × 50 px                        | Mobile login page only                               |

**Supported Screens:** Ads can be placed on almost any screen — Dashboard, Accounts, Transfers, Deposits, Bill Pay, Remote Deposit Capture (RDC), Statements, and ATM Locators. An **"Others" placeholder** exists for broad multi-screen placement.

**Key Constraints:**

* Prisma currently only supports **pixel** dimensions, which can introduce responsiveness challenges on variable screen sizes.
* **Device-specific creatives** must be configured separately for each device type (e.g., iPad vs. iPhone for interstitials). There is no automatic fallback — if a device-specific image is not set up, the ad will not render on that device.
* The Mobile Login Banner is not recommended for other mobile pages due to interference with navigation elements such as the tab drawer.



### Campaign Management

Campaign management is the core workflow in the Prisma console. The following screenshots illustrate the key screens involved in configuring and managing ad campaigns.

&#x20;_Prisma Console — Campaign Overview / Banner List_

<figure><img src="../.gitbook/assets/unknown (2).png" alt=""><figcaption></figcaption></figure>

_Segment Creation: Go to Segments > New Segment. Segments can be created from queries, from another segment or from a spreadsheet. You can find more information in the Prisma Resources_ [_here_](https://help.prismacampaigns.com/getting-started/integrate-data-segments/create-segments/)_._

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



&#x20;_Campaign Creation & Audience Targeting :_ Once the Segment is created, you can go over to the Campaigns > New Campaign to create an Ad and select the segment for targeting.&#x20;

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



_Banner Creation :_ You can create campaigns for multiple channels in this section and choose from Banners, Email, SMS, Push, etc. You can read more about it [here](https://help.prismacampaigns.com/getting-started/channel-design/add-banners/)&#x20;

<figure><img src="../.gitbook/assets/unknown (4).png" alt=""><figcaption></figcaption></figure>

&#x20;_Creative Upload :_ _Image and HTML Ad also can be configured by directly adding the HTML code in the edit HTML Banner section._&#x20;

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

_Funnel Configuration :_ The funnel consists of everything that happens from the moment a person shows interest in a campaign.  You can read more about it [here](https://help.prismacampaigns.com/getting-started/channel-design/add-banners/)&#x20;

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Key campaign management capabilities:**

**Banner Creation** involves specifying:

* **Banner Name** (e.g., "Auto Loan Q4 Promotion")
* **Target Devices/Screens** — select specific screens (e.g., fund transfer landing page, accounts page) and device types (mobile, tablet)
* **Resolution** — must match the placement zone requirements (e.g., 320×480 for some mobile banners)
* **Creative Upload** — upload image assets; an AI image generator is also available in the console
* **Funnel (Web Redirection)** — configure the URL you are directed to upon clicking the ad; can integrate with services like Accurify for sign-up flows or lightweight marketing applications built within Prisma

**Advanced Campaign Features:**

* **A/B Testing** — set up two creative variants for different user sets within the same campaign and compare performance
* **HTML Ads** — HTML content can be pasted directly into the ad creative field, enabling responsive designs that adapt to different screen sizes (recommended for cross-device campaigns)
* **Email & SMS Campaigns** — Prisma supports configuring sender details, designing content, and dispatching email and SMS campaigns directly from the console
* **Business Events** — Prisma can receive events (e.g., `processStarted` for new account openings) with contextual parameters (e.g., `customerID`) to trigger specific campaigns. _Current state: nFinia does not currently send business events to Prisma; ad triggering is managed entirely on the Prisma side._

**Publishing and Deletion:**

* Ads must be **explicitly published** to go live; publishing applies across all enabled ads simultaneously
* **Deletion is permanent and irreversible** — there is no undo, and all associated statistics (reach, clicks, conversions) are permanently lost upon deletion

### Reporting and Analytics

Prisma provides campaign-level tracking and reporting for each active ad.&#x20;

&#x20;_Prisma Analytics Dashboard — Reach, Clicks, and Conversion Tracking_

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Tracked Metrics:**

* Number of you reached (impressions)
* Clicks and conversions (you who clicked and completed an action on the linked destination)
* Full funnel analytics — from impression → click → conversion — with export capability

**Data Synchronization:**

Prisma supports structured data sync (file-based with column mappings) for two key operational use cases:

1. **Segmentation data ingestion** — FIs push member profile data (demographics, custom attributes) to Prisma to build targeting segments
2. **Marketing opt-out communication** — Tyfone uses Prisma's data sync to pass CCPA opt-out preferences from nFinia to Prisma. The opt-out option is accessible via the "More" menu and "Offer Space" within nFinia (intentionally placed to be unobtrusive while remaining compliant)

***

## Operational Guidelines and Cautions

### Test vs. Production Environment

> ⚠️ **Critical:** For most FIs, Prisma's test and production environments are the **same instance**. Enabling an ad in "test" makes it live to real you immediately.

| Guideline                | Detail                                                                     |
| ------------------------ | -------------------------------------------------------------------------- |
| Shared Environment       | Test = Production for most FI deployments                                  |
| Permitted Testing Window | 12:00 PM – 3:00 PM IST (low-traffic US hours)                              |
| Mandatory Disable        | All test ads must be disabled before 3:00 PM IST                           |
| Responsible Party        | Tyfone Delivery Manager                                                    |
| Login Credentials        | Do NOT change; no self-service reset; requires Prisma support intervention |

**Why this matters:** A test ad accidentally left live during US business hours will be displayed to all production you.&#x20;

### Data Ingestion and User Identification

Accurate member identification is foundational to Prisma's ad serving and segmentation capabilities. You can read more about this [here](https://help.prismacampaigns.com/getting-started/integrate-data-segments/uploading-data-to-prisma/)&#x20;

| Concern                | Current Approach                                                       |
| ---------------------- | ---------------------------------------------------------------------- |
| Data Feed Source       | FI sends data directly to Prisma (Tyfone no longer intermediates)      |
| Identifier Level       | Must be **person-level** (not membership-level)                        |
| Recommended Identifier | Tokenized external ID (e.g., a custom field in Symitar mapping to SSN) |
| nFinia's Role          | Fetches the external ID at login and loads Prisma ads                  |
| Schema Flexibility     | Prisma supports custom profile schema expansion beyond default fields  |

**Segmentation Limitation:** nFinia does not currently support triggering Prisma segments or campaigns based on real-time user actions (e.g., "member just deposited over $1,000"). Segmentation today is based on static data pushed by the FI. The business events infrastructure exists in Prisma but is not yet wired into nFinia — this is a future enhancement opportunity.

### Data Loss and Irreversibility

| Scenario                  | Consequence                             | Recovery                                                          |
| ------------------------- | --------------------------------------- | ----------------------------------------------------------------- |
| Ad banner deleted         | Permanent; cannot be recovered          | FI must re-create the banner and all associated data from scratch |
| Statistics lost on delete | All reach/click/conversion data is gone | No recovery; inform the FI and advise re-creation                 |

### Access and Permissions

| Access Level        | Who Has It                                 | What They Can Do                                    |
| ------------------- | ------------------------------------------ | --------------------------------------------------- |
| Full Console Access | Tyfone Delivery Managers, Support Managers | Create, modify, publish, delete campaigns           |
| View Access         | Training personnel                         | View interface and campaign setup; no modifications |

**Important:** When accessing the Prisma console — even in a view capacity — exercise extreme caution. Do not delete, modify, or publish live campaigns. The consequences of accidental changes (especially deletions) cannot be undone.

***

## End-to-End Workflow: Creating and Publishing an Ad Campaign

### Prerequisites

* FI has an active Prisma subscription (Full or Light)
* Person-level external ID has been configured in the FI's core system and is being pushed to Prisma via data sync
* nFinia has been configured with Prisma placeholders and the token-based integration is active
* You have delivery manager or marketing admin access to the Prisma console
* Creative assets (images) are prepared and sized to the correct IAB dimensions for the target placement

### Step-by-Step Flow

1. **Log in to the Prisma console** using the credentials provided for the FI. Do not change these credentials.
2. **Navigate to Campaign Management** and select "Create New Banner."
3. **Enter banner details:**
   * Banner Name (descriptive and FI-specific, e.g., "Auto Loan Spring 2026")
   * Select target screens (e.g., Dashboard, Accounts)
   * Select target devices (mobile, tablet, or both)
4. **Set ad dimensions** to match the placement zone (e.g., 728×90 for leaderboard, 250×250 for side pop-up). Note that only pixel units are supported.
5. **Upload creative:** Attach the image asset or paste HTML content. If using device-specific creatives (e.g., different images for iPhone vs. iPad), upload separate assets for each device type.
6. **Configure funnel (optional):** Enter the destination URL for click-through redirection. Optionally integrate with third-party sign-up flows via Accurify or similar services.
7. **Set targeting (Full version only):** Define the audience segment (e.g., you aged 25–45 with checking accounts). Segments must already exist or be built from pushed FI data.
8. **Configure A/B test (optional):** Define two creative variants and the percentage split between user groups.
9. **Review all settings** and confirm the testing window if this is a test campaign (12 PM–3 PM IST only).
10. **Publish the campaign.** Publishing makes the ad live immediately for all eligible you. Verify the ad is displaying correctly in the app.
11. **Monitor analytics** in the Prisma reporting dashboard: track reach, clicks, and conversion against campaign goals.
12. **Disable test ads** before 3 PM IST if running a test campaign.

### Decision Points & Branching

| Condition                                       | Outcome                                                          |
| ----------------------------------------------- | ---------------------------------------------------------------- |
| Prisma Light (no segmentation)                  | Ad is visible to ALL you once published                          |
| No device-specific creative uploaded            | Ad will not render on that device type                           |
| Business events not configured                  | Ad triggering is managed entirely in Prisma console              |
| FI sends membership-level ID (not person-level) | Segmentation and personalized ad serving will not work correctly |

### Completion & Confirmation

* Published ads go live immediately; no additional approval step required
* Prisma begins tracking impressions, clicks, and conversions automatically
* Analytics are accessible in the reporting dashboard within the console

### Error Handling

| Scenario                         | What Happens                                                  | Recovery                                               |
| -------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------ |
| Ad accidentally deleted          | Permanent loss; no undo                                       | Re-create the banner; inform the FI of lost statistics |
| Wrong creative uploaded          | Update before publishing; after publishing, modify the banner | Edit the banner and republish                          |
| Credentials changed              | Lockout for all you; no self-service reset                    | Contact Prisma support                                 |
| Test ad left live past 3 PM IST  | Production you see test ads                                   | Disable immediately; communicate to FI                 |
| Device-specific creative missing | Ad does not render on that device                             | Upload the missing device creative and republish       |

***

## . FAQs

**Q: What is Prisma?**\
Prisma is an advertising platform integrated with nFinia that allows FIs to display targeted ads within their members' digital banking app. The integration is token-based.

**Q: What's the difference between Prisma Full and Light?**\
Prisma Full supports audience segmentation and per-user targeting. Prisma Light delivers ads to all you without targeting capability, at a lower cost.

**Q: Why must testing be done within specific hours?**\
For most FIs, Prisma's test and production environments are the same. Any enabled ad — including test ads — is immediately visible to live you. Testing is restricted to 12 PM–3 PM IST to minimize exposure during US peak hours.

**Q: Can a deleted ad be recovered?**\
No. Deletion is permanent and irreversible. All associated data including statistics is permanently lost. The FI must re-create the banner from scratch.

**Q: Can nFinia trigger campaigns based on real-time member actions?**\
Not currently. Segmentation is based on static profile data pushed by the FI to Prisma. The business events infrastructure exists but is not yet utilized by nFinia.

**Q: How are marketing opt-outs handled?**\
Tyfone uses Prisma's data sync feature to push member opt-out preferences (CCPA) from nFinia to Prisma. The opt-out option is accessible in nFinia's "More" menu and "Offer Space."

**Q: Can HTML be used for ad creatives?**\
Yes. HTML content can be pasted directly into the creative field, enabling responsive ad designs that adapt across screen sizes.

**Q: How is user data protected when sent to Prisma?**\
FIs should send a tokenized, person-level external ID (not raw SSN). Many FIs create a custom field in their core system (e.g., Symitar) that maps to the SSN and push this external ID to Prisma instead.

***

## Quick Reference

| Task                         | Where to Do It                                           | Who Can Do It                        | Notes                                         |
| ---------------------------- | -------------------------------------------------------- | ------------------------------------ | --------------------------------------------- |
| Create a new banner          | Prisma Console > Campaign Management > Create New Banner | Delivery Manager, FI Marketing Admin | Follow IAB dimension standards                |
| Upload creative              | Banner creation flow > Creative Upload tab               | Delivery Manager, FI Marketing Admin | Separate assets required per device type      |
| Publish all live ads         | Prisma Console > Publish                                 | Delivery Manager, FI Marketing Admin | Publishing is global; affects all enabled ads |
| Enable test ad (safe window) | Prisma Console > Enable Banner                           | Delivery Manager                     | 12 PM–3 PM IST only; disable before 3 PM IST  |
| Delete a banner              | Prisma Console > Banner > Delete                         | Delivery Manager                     | Irreversible; all stats permanently lost      |
| View analytics               | Prisma Console > Reporting / Campaign Analytics          | Delivery Manager, FI Marketing Admin | Export available                              |
| Configure opt-out sync       | Prisma Console > Data Sync                               | Delivery Manager                     | Used for CCPA compliance                      |
| Grant view access            | Prisma Console > User Management                         | Delivery Manager                     | For training only; no edit permissions        |
| Set up email/SMS campaign    | Prisma Console > Campaigns > Email/SMS                   | Delivery Manager, FI Marketing Admin | Configure sender details and content          |

***

_This guide was prepared by Jeeva Krishnamurthy, Senior Product Manager, Commercial & SMB Digital Banking at Tyfone. For questions about Prisma integration configuration or campaign setup, contact the Tyfone Delivery team._
