---
description: Credit Card Management (Phase 1) — Full-service credit card controls, alerts, and travel notifications via Velera (PSCU) within nFinia Digital Banking for Summerville Credit Union.
---

# Credit Card Management

**Vendor:** Velera (formerly PSCU)\
**Module:** Banking › Cards\
**Feature:** Card Management — Credit Card (PSCU Phase 1)\
**Release Version:** 10.38

---

## Product Summary

Credit Card Management (Phase 1) provides Summerville Credit Union you with comprehensive self-service control over your credit cards directly within the nFinia digital banking app. Powered by Velera (formerly PSCU), you can activate new cards, manage card controls, set spending limits, configure alerts, and report lost or stolen cards — all without contacting the credit union.

| Attribute | Detail |
| --- | --- |
| Feature Name | Card Management — Credit Card (PSCU Phase 1) |
| Module Location | Banking › Cards |
| Supported Card Types | Full-service credit cards (PSCU/Optis), In-House Credit (Wilmington/Optis) |
| Vendor | Velera (formerly PSCU) |
| Release Version | 10.38 |
| Channels | Mobile (iOS, Android), Web |

---

## Use Cases

| # | Use Case | Description |
| --- | --- | --- |
| 1 | View card info and rewards | View credit card details, current balance, and rewards points |
| 2 | Activate a new card | Activate a newly received credit card within the app |
| 3 | Toggle card on/off | Instantly lock or unlock a credit card to prevent or allow transactions |
| 4 | Set spending limits | Configure transaction-level or period-level spending caps |
| 5 | Configure card alerts | Set up real-time push notifications for specific transaction events |
| 6 | Set domestic controls | Restrict card use by merchant category within domestic regions |
| 7 | Set international controls | Enable or restrict card use for international transactions; set country-level permissions |
| 8 | Report lost or stolen card | Mark a card as lost or stolen to initiate a replacement |
| 9 | Set a travel notification | Notify Velera of travel plans to prevent out-of-country declines |

---

## Step-by-Step Guides

### 1. Card Info & Rewards

**Step 1 — Navigate to Cards**

From the main menu, select **Banking** and tap **Cards**.

![](</.gitbook/assets/velera-card-mgmt-001.png>)

**Step 2 — Select Your Credit Card**

Tap your credit card to open the Card Details screen.

![](</.gitbook/assets/velera-card-mgmt-002.png>)

**Step 3 — View Card Info and Rewards**

The Card Details screen displays your card number (masked), expiry date, current balance, available credit, and rewards points balance.

![](</.gitbook/assets/velera-card-mgmt-003.png>)

---

### 2. Activate a New Card

**Step 1 — Open Card Details**

Navigate to **Banking › Cards** and select the card that shows as inactive or pending activation.

![](</.gitbook/assets/velera-card-mgmt-004.png>)

**Step 2 — Tap "Activate Card"**

Tap the **Activate Card** button. You may be prompted to confirm the last four digits of the card or enter a PIN.

![](</.gitbook/assets/velera-card-mgmt-005.png>)

**Step 3 — Confirm Activation**

Follow the on-screen prompts to complete activation. Once confirmed, the card status updates to active.

![](</.gitbook/assets/velera-card-mgmt-006.png>)

---

### 3. Card On/Off Toggle

**Step 1 — Open Card Details**

Navigate to **Banking › Cards** and select your credit card.

![](</.gitbook/assets/velera-card-mgmt-007.png>)

**Step 2 — Toggle the Card**

Tap the **Card On/Off** toggle. The card is instantly locked (Off) or unlocked (On). A locked card will decline all transactions.

![](</.gitbook/assets/velera-card-mgmt-008.png>)

---

### 4. Spending Limits

**Step 1 — Open Card Controls**

From Card Details, tap **Spending Limits** or navigate to **Card Controls › Spending Limits**.

![](</.gitbook/assets/velera-card-mgmt-009.png>)

**Step 2 — Set a Limit**

Choose the limit type (per transaction, per day, or per month) and enter the maximum amount. Tap **Save**.

![](</.gitbook/assets/velera-card-mgmt-010.png>)

**Step 3 — Confirm**

The spending limit is applied immediately. Transactions exceeding the limit will be declined.

![](</.gitbook/assets/velera-card-mgmt-011.png>)

---

### 5. Card Alerts

**Step 1 — Open Card Alerts**

From Card Details, tap **Card Alerts** or navigate to **Card Controls › Alerts**.

![](</.gitbook/assets/velera-card-mgmt-012.png>)

**Step 2 — Configure Alert Types**

Toggle on the alerts you want to receive — such as transaction approval, transaction decline, balance threshold, or card-not-present transactions.

![](</.gitbook/assets/velera-card-mgmt-013.png>)

**Step 3 — Save Preferences**

Tap **Save**. Alerts are delivered as push notifications to your enrolled device.

![](</.gitbook/assets/velera-card-mgmt-014.png>)

---

### 6. Domestic Controls

**Step 1 — Open Domestic Controls**

From Card Details, navigate to **Card Controls › Domestic Controls**.

![](</.gitbook/assets/velera-card-mgmt-015.png>)

**Step 2 — Set Merchant Category Restrictions**

Enable or disable card use for specific merchant categories (e.g., gas stations, restaurants, online retailers). Toggle categories on or off as needed.

![](</.gitbook/assets/velera-card-mgmt-016.png>)

**Step 3 — Save Controls**

Tap **Save**. Restrictions take effect immediately for subsequent transactions in the selected categories.

![](</.gitbook/assets/velera-card-mgmt-017.png>)

---

### 7. International Controls

**Step 1 — Open International Controls**

From Card Details, navigate to **Card Controls › International Controls**.

![](</.gitbook/assets/velera-card-mgmt-018.png>)

**Step 2 — Enable or Restrict International Use**

Toggle international card use on or off. To allow use in specific countries, select countries from the available list.

> **Note:** The Velera API does not support location names that include numbers. Map-based country selection is not supported; country selection is list-based only.

![](</.gitbook/assets/velera-card-mgmt-019.png>)

**Step 3 — Save Controls**

Tap **Save**. International controls are applied immediately.

![](</.gitbook/assets/velera-card-mgmt-020.png>)

---

### 8. Report Lost or Stolen Card

**Step 1 — Open Card Details**

Navigate to **Banking › Cards** and select the affected credit card.

![](</.gitbook/assets/velera-card-mgmt-021.png>)

**Step 2 — Tap "Report Lost/Stolen"**

Tap the **Report Lost/Stolen** option. You will be asked to confirm your intent, as this action initiates a card block and replacement process.

![](</.gitbook/assets/velera-card-mgmt-022.png>)

**Step 3 — Confirm and Submit**

Confirm the report. The card is immediately blocked, and a replacement card will be issued per Summerville Credit Union's card replacement policy.

![](</.gitbook/assets/velera-card-mgmt-023.png>)

---

### 9. Travel Notification

**Step 1 — Open Travel Notifications**

From Card Details, tap **Travel Notification** or navigate to **Card Controls › Travel Notification**.

![](</.gitbook/assets/velera-card-mgmt-024.png>)

**Step 2 — Enter Travel Details**

Enter your travel destination(s) and travel dates (departure and return). This informs Velera's fraud detection system to allow transactions from those locations during your trip.

![](</.gitbook/assets/velera-card-mgmt-025.png>)

**Step 3 — Submit**

Tap **Submit**. Velera records the travel notification, reducing the likelihood of international transaction declines during your trip.

![](</.gitbook/assets/velera-card-mgmt-026.png>)

---

## Key Notes

- **Velera API location name limitation:** The Velera API does not support location names that contain numbers. When configuring international controls or travel notifications, country and location names must be alphanumeric without numeric characters in the name.
- **Map-based selection not supported:** Country selection for international controls is list-based only; a map-based interface is not available due to Velera API constraints.
- **Real-time enforcement:** All card controls (on/off, spending limits, domestic/international restrictions) are enforced by Velera in real time on subsequent transactions.
- **Lost/stolen card process:** Reporting a card as lost or stolen immediately blocks the card. Card replacement timelines are determined by Summerville Credit Union's card issuance process.
- **Travel notifications prevent fraud blocks:** Members traveling internationally should set a travel notification before departure. Without one, Velera's fraud detection may decline international transactions as suspicious activity.

---

## FAQs

**Q: Which credit cards are managed through this feature?**\
Full-service credit cards issued under Summerville Credit Union's Velera (PSCU) program and In-House Credit cards (Wilmington/Optis) are supported.

**Q: Are card controls enforced immediately?**\
Yes. All changes made through nFinia are sent to Velera via API in real time and take effect on subsequent transactions immediately.

**Q: Can I unlock my card after locking it?**\
Yes. The Card On/Off toggle can be switched back on at any time to unlock the card.

**Q: What happens when I report my card as lost or stolen?**\
The card is immediately blocked, preventing any further transactions. A replacement card will be issued according to Summerville Credit Union's card replacement policy.

**Q: Do I need to set a travel notification for domestic travel?**\
No. Travel notifications are primarily intended for international travel to prevent fraud-related declines. Domestic travel typically does not require a notification.

**Q: Can I restrict specific types of merchants?**\
Yes. Domestic Controls allow you to restrict card use by merchant category (e.g., entertainment, gas stations, online purchases).

**Q: What if a country isn't available in the international controls list?**\
The available country list is managed by Velera. If a country is not listed, contact Summerville Credit Union's member services team for assistance.

---

*For technical integration questions, contact the Tyfone Delivery team. For member-facing card management support, refer to Summerville Credit Union's member services team.*
