# Prisma Integration

## Summary

The Prisma integration connects nFinia Digital Banking with Prisma Campaigns — the credit union's member engagement and targeted marketing platform — enabling personalised offers and financial wellness prompts to be surfaced directly within the digital banking session. For the credit union, this integration provides a channel to deliver contextually relevant product offers to members based on account behaviour and segment criteria, without requiring the member to visit a separate marketing site or respond to email campaigns.

## Key Use Cases

Credit union marketing teams use the Prisma integration to surface pre-approved loan offers to members whose credit profile and account behaviour indicate high approval likelihood — delivering the offer at the moment the member is already engaged with their finances. Members who see a relevant offer — such as a home equity line or auto loan pre-approval — can express interest or initiate an application directly from the banner or widget within the digital banking session, reducing the steps from awareness to application. Operations staff configure campaign targeting rules in Prisma and verify that the correct offer segments are appearing for the intended member profiles within the nFinia interface.

## Integration Overview

The Prisma integration operates as a server-side data exchange between nFinia and the Prisma Campaigns platform. Member segment data — based on account type, balance tier, product holdings, and behaviour signals — is periodically synced from nFinia to Prisma, which uses this data to determine which campaign creatives to surface to which members. The selected campaign content is returned to nFinia and rendered in designated widget zones on the Dashboard and within relevant account screens.

<figure><img src="../.gitbook/assets/unknown (2).png" alt=""><figcaption></figcaption></figure>

## Configuration Notes

Campaign targeting rules, offer creatives, and display zones are configured within the Prisma platform by the credit union's marketing team. nFinia controls the widget placement and rendering; Prisma controls the content and segmentation logic. Contact the Tyfone Delivery team for integration setup, widget placement changes, or troubleshooting campaign display issues.

<figure><img src="../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/unknown (4).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (5) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

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

| Condition | Outcome |
| ----------------------------------------------- | ---------------------------------------------------------------- |
| Prisma Light (no segmentation) | Ad is visible to ALL you once published |
| No device-specific creative uploaded | Ad will not render on that device type |
| Business events not configured | Ad triggering is managed entirely in Prisma console |
| FI sends membership-level ID (not person-level) | Segmentation and personalized ad serving will not work correctly |

### Completion & Confirmation

* Published ads go live immediately; no additional approval step required
* Prisma begins tracking impressions, clicks, and conversions automatically
* Analytics are accessible in the reporting dashboard within the console

### Error Handling

| Scenario | What Happens | Recovery |
| -------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------ |
| Ad accidentally deleted | Permanent loss; no undo | Re-create the banner; inform the FI of lost statistics |
| Wrong creative uploaded | Update before publishing; after publishing, modify the banner | Edit the banner and republish |
| Credentials changed | Lockout for all you; no self-service reset | Contact Prisma support |
| Test ad left live past 3 PM IST | Production you see test ads | Disable immediately; communicate to FI |
| Device-specific creative missing | Ad does not render on that device | Upload the missing device creative and republish |

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

| Task | Where to Do It | Who Can Do It | Notes |
| ---------------------------- | -------------------------------------------------------- | ------------------------------------ | --------------------------------------------- |
| Create a new banner | Prisma Console > Campaign Management > Create New Banner | Delivery Manager, FI Marketing Admin | Follow IAB dimension standards |
| Upload creative | Banner creation flow > Creative Upload tab | Delivery Manager, FI Marketing Admin | Separate assets required per device type |
| Publish all live ads | Prisma Console > Publish | Delivery Manager, FI Marketing Admin | Publishing is global; affects all enabled ads |
| Enable test ad (safe window) | Prisma Console > Enable Banner | Delivery Manager | 12 PM–3 PM IST only; disable before 3 PM IST |
| Delete a banner | Prisma Console > Banner > Delete | Delivery Manager | Irreversible; all stats permanently lost |
| View analytics | Prisma Console > Reporting / Campaign Analytics | Delivery Manager, FI Marketing Admin | Export available |
| Configure opt-out sync | Prisma Console > Data Sync | Delivery Manager | Used for CCPA compliance |
| Grant view access | Prisma Console > User Management | Delivery Manager | For training only; no edit permissions |
| Set up email/SMS campaign | Prisma Console > Campaigns > Email/SMS | Delivery Manager, FI Marketing Admin | Configure sender details and content |

***
