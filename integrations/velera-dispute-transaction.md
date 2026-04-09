---
description: Dispute a Transaction — Credit card dispute submission and tracking via Velera (PSCU) Dispute Management Console within nFinia Digital Banking for Summerville Credit Union.
---

# Dispute a Transaction

**Vendor:** Velera (formerly PSCU)\
**Module:** Banking › Cards › Card Details › Transaction History › Raise Dispute\
**Integration Type:** Velera Dispute Management Console (via nFinia)

---

## Product Summary

The Dispute a Transaction feature allows Summerville Credit Union you to submit and track credit card disputes directly within the nFinia digital banking app. Disputes are processed through the Velera (PSCU) Dispute Management Console, and you can monitor the status of their submitted disputes through the Support Messages section (powered by Zendesk).

| Attribute | Detail |
| --- | --- |
| Feature Name | Dispute a Transaction |
| Module Location | Banking › Cards › Card Details › Transaction History › Raise Dispute |
| Supported Cards | Credit cards only (Debit card disputes not supported) |
| Dispute Processing | Velera (PSCU) Dispute Management Console |
| Dispute Tracking | Support Messages (Zendesk integration) |
| Dispute Amount | Full or partial transaction amount |
| Channels | Mobile (iOS, Android), Web |
| Supported Cores | Correlation, Ultradata |
| Release Version | 10.41 |

---

## Use Cases

| # | Use Case | Description |
| --- | --- | --- |
| 1 | Dispute a merchant charge | Member disputes a charge from a merchant they believe is incorrect or unauthorized |
| 2 | Dispute potential fraud | Member reports a transaction they did not make or authorize |
| 3 | Submit a partial dispute | Member disputes only a portion of a transaction amount |
| 4 | Track a submitted dispute | Member checks the status of a previously submitted dispute |
| 5 | Reply with additional information | Member responds to a request for more information on an open dispute |

---

## Step-by-Step Guide

### How to Dispute a Transaction

**Step 1 — Navigate to Cards**

From the main menu, select **Banking** and tap **Cards**.

![](</.gitbook/assets/velera-dispute-001.png>)

**Step 2 — Select the Card**

Tap the credit card for which you want to dispute a transaction.

![](</.gitbook/assets/velera-dispute-002.png>)

**Step 3 — View Transaction History**

On the Card Details screen, scroll down to view your transaction history. Tap the transaction you want to dispute.

![](</.gitbook/assets/velera-dispute-003.png>)

**Step 4 — Tap "Raise Dispute"**

On the Transaction Details screen, tap **Raise Dispute** at the bottom of the screen.

![](</.gitbook/assets/velera-dispute-004.png>)

**Step 5 — Select Dispute Reason**

Choose the reason for your dispute from the list of available options (e.g., "I did not make this transaction," "The amount is incorrect," "Item not received").

![](</.gitbook/assets/velera-dispute-005.png>)

**Step 6 — Enter Dispute Details**

Fill in the required information based on your selected dispute reason. For partial disputes, enter the amount you are disputing.

![](</.gitbook/assets/velera-dispute-006.png>)

**Step 7 — Review and Submit**

Review the dispute details and tap **Submit**. You will receive a confirmation that your dispute has been submitted.

![](</.gitbook/assets/velera-dispute-007.png>)

**Step 8 — Track Your Dispute**

Navigate to **Support Messages** from the main menu to track the status of your submitted dispute. You can also reply to requests for additional information directly within Support Messages.

![](</.gitbook/assets/velera-dispute-008.png>)

---

## Key Notes

- **Credit cards only:** The Raise Dispute option is available for credit card transactions only. Debit card disputes must be handled through a different channel — contact the credit union directly.
- **Partial disputes:** Members can dispute a portion of a transaction by entering a specific amount during the dispute submission flow.
- **Dispute tracking:** All submitted disputes appear in **Support Messages** (Zendesk), where you can view status updates and respond to requests for additional information.
- **Processing:** Disputes are routed to Velera's Dispute Management Console for processing. Resolution timelines depend on the nature of the dispute and Velera's review process.

---

## FAQs

**Q: Can I dispute a debit card transaction through this feature?**\
No. The Raise Dispute option is available for credit card transactions only. For debit card disputes, contact Summerville Credit Union directly.

**Q: Can I dispute only part of a transaction?**\
Yes. When entering dispute details, you can specify a partial amount to dispute rather than the full transaction amount.

**Q: How do I track the status of my dispute?**\
Navigate to **Support Messages** from the main menu. Your submitted disputes will appear there, along with any status updates or requests for additional information from the credit union.

**Q: What types of disputes can I submit?**\
Common dispute reasons include unauthorized transactions, incorrect amounts, items not received, and duplicate charges. The available options are listed during the dispute submission flow.

**Q: How long does it take to resolve a dispute?**\
Resolution timelines vary based on the dispute type and are determined by Velera's dispute processing procedures. You will receive updates through Support Messages.

---

*For technical integration questions, contact the Tyfone Delivery team. For member-facing disputes and support, refer to Summerville Credit Union's member services team.*
