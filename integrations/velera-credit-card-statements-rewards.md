---
description: Credit Card eStatements, CURewards SSO, and CashBackMall SSO — Velera-powered statement access and rewards portal integration within nFinia Digital Banking for Summerville Credit Union.
---

# Credit Card eStatements & Rewards

**Vendor:** Velera (formerly PSCU)\
**Module:** Banking › Cards and Banking › eDocuments\
**Features:** Credit Card eStatements · CURewards SSO · CashBackMall SSO

---

## Product Summary

This feature set covers three Velera-powered capabilities available to Summerville Credit Union members within nFinia:

1. **Credit Card eStatements** — View and download credit card statements in PDF format directly within the digital banking app. Statements are formatted and branded by Velera.
2. **CURewards SSO** — Single Sign-On access to the CURewards portal for members enrolled in the Traditional Rewards program.
3. **CashBackMall SSO** — Single Sign-On access to the CashBackMall portal for members enrolled in the Cash Back Rewards program.

| Attribute | Detail |
| --- | --- |
| Feature Name | Credit Card eStatements & Rewards SSO |
| Module Location | Banking › Cards; Banking › eDocuments |
| Vendor | Velera (formerly PSCU) |
| Statement Format | PDF (Velera-formatted, CU-branded) |
| Rewards Programs | CURewards (Traditional Rewards), CashBackMall (Cash Back Rewards) |
| SSO Type | Velera-authenticated Single Sign-On |
| Channels | Mobile (iOS, Android), Web |

---

## Use Cases

| # | Use Case | Description |
| --- | --- | --- |
| 1 | View credit card eStatement | Member views the current or a past credit card statement within nFinia |
| 2 | Download credit card statement | Member downloads a PDF copy of their credit card statement |
| 3 | Set email preference for statements | Member configures the email address associated with their eStatement notifications |
| 4 | Access CURewards portal | Member SSOs into the CURewards portal to view and redeem traditional reward points |
| 5 | Access CashBackMall portal | Member SSOs into the CashBackMall portal to earn and redeem cash back rewards |
| 6 | View rewards balance in app | Member views their current rewards points balance within the nFinia Cards module |

---

## Credit Card eStatements

### How to View and Download eStatements

**Step 1 — Navigate to eDocuments**

From the main menu, select **Banking** and tap **eDocuments**. Alternatively, access statements directly from the Cards module by selecting your credit card.

![](</.gitbook/assets/velera-statements-001.png>)

**Step 2 — Select Credit Card Statements**

In the eDocuments section, tap **Credit Card Statements** to view the list of available statements.

![](</.gitbook/assets/velera-statements-002.png>)

**Step 3 — Choose a Statement**

Tap the statement period you want to view. The statement opens as a PDF within the app.

![](</.gitbook/assets/velera-statements-003.png>)

**Step 4 — Download or Share**

To save the statement, tap the download or share icon to export the PDF to your device.

![](</.gitbook/assets/velera-statements-004.png>)

### Email Preference for eStatements

When setting up eStatements, members are presented with three email options for statement delivery notifications:

| Option | Description |
| --- | --- |
| Sync from Core | Use the email address on file with the credit union's core system |
| Keep Velera email | Use the email address already registered in Velera's system |
| Enter new email | Manually enter a different email address for eStatement notifications |

---

## CURewards SSO (Traditional Rewards)

Members enrolled in Summerville Credit Union's Traditional Rewards program can access the CURewards portal directly from within nFinia via Single Sign-On.

**How to Access CURewards**

**Step 1 — Navigate to Cards**

From the main menu, select **Banking** and tap **Cards**. Select your credit card.

![](</.gitbook/assets/velera-statements-005.png>)

**Step 2 — Tap "Rewards"**

On the Card Details screen, tap the **Rewards** or **View Rewards** option to launch the CURewards portal.

![](</.gitbook/assets/velera-statements-006.png>)

**Step 3 — CURewards Portal Opens**

You are seamlessly signed into the CURewards portal via SSO. From here, view your points balance, browse redemption options, and redeem rewards.

![](</.gitbook/assets/velera-statements-007.png>)

---

## CashBackMall SSO (Cash Back Rewards)

Members enrolled in the Cash Back Rewards program can access the CashBackMall portal directly from within nFinia via Single Sign-On.

**How to Access CashBackMall**

**Step 1 — Navigate to Cards**

From the main menu, select **Banking** and tap **Cards**. Select your credit card.

![](</.gitbook/assets/velera-statements-008.png>)

**Step 2 — Tap "Cash Back Rewards"**

On the Card Details screen, tap **Cash Back Rewards** or **CashBackMall** to launch the portal.

![](</.gitbook/assets/velera-statements-009.png>)

**Step 3 — CashBackMall Portal Opens**

You are seamlessly signed into the CashBackMall portal via SSO. Browse participating merchants, activate offers, and track your cash back earnings.

![](</.gitbook/assets/velera-statements-010.png>)

---

## Key Notes

- **Statement format:** Credit card statements are generated and formatted by Velera. They are branded with Summerville Credit Union's identity but produced by Velera's statement rendering engine.
- **SSO authentication:** Both CURewards and CashBackMall use Velera-authenticated SSO, so members do not need separate login credentials for the rewards portals.
- **Rewards program eligibility:** CURewards and CashBackMall availability depends on which rewards program the member is enrolled in. Not all members may have access to both portals.
- **Email preference at eStatement enrollment:** Members set their preferred notification email during the eStatement enrollment flow. This can be updated later through account settings.

---

## FAQs

**Q: Where can I find my credit card statements?**\
Navigate to **Banking › eDocuments › Credit Card Statements**, or access them directly from your credit card's detail page in the Cards module.

**Q: Are statements available as PDFs?**\
Yes. Credit card statements are available in PDF format for viewing within the app and downloading to your device.

**Q: What is CURewards?**\
CURewards is Summerville Credit Union's Traditional Rewards program. Members earn points on qualifying credit card purchases and can redeem them through the CURewards portal, accessible via SSO from within nFinia.

**Q: What is CashBackMall?**\
CashBackMall is the Cash Back Rewards program, offering cash back earnings at participating merchants. Members can access the CashBackMall portal directly from within nFinia via SSO.

**Q: Do I need a separate login for the rewards portals?**\
No. Both CURewards and CashBackMall use Single Sign-On (SSO) through Velera, so you are automatically authenticated when accessing the portals from within nFinia.

**Q: Which email address will receive my eStatement notifications?**\
During eStatement enrollment, you can choose to use your core system email, your existing Velera email, or enter a new email address specifically for eStatement notifications.

---

*For technical integration questions, contact the Tyfone Delivery team. For member-facing rewards and statement inquiries, refer to Summerville Credit Union's member services team.*
