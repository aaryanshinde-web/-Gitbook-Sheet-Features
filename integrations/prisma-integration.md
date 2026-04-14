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