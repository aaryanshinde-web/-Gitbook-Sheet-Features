---
description: >-
  Raise disputes for credit card transactions with full control over amounts and
  reasons.
---

# Velera — Dispute a Transaction

**Dispute a Transaction**

_Module: Banking › Cards › Card Details › Transaction History › Raise Dispute_

### Summary

The Dispute a Transaction feature allows members to raise a dispute for a credit card transaction directly from nFinia Digital Banking. Disputes are submitted to Velera (PSCU) and processed through the Velera Dispute Management Console. Once a dispute is submitted, members receive status updates and can track the progress of their dispute via the Support Messages section of the Inbox — powered by Zendesk integration.

Members can dispute either the full transaction amount or a partial amount, select the reason for the dispute from a dynamic list provided by Velera, and provide any additional information required. If a reason that implies fraud is selected, members are also prompted to consider reporting their card as lost or stolen.

**At a Glance**

| Feature Name           | Dispute a Transaction                                                           |
| ---------------------- | ------------------------------------------------------------------------------- |
| **Module Location**    | Banking › Cards › Card Details › Transaction History › Raise Dispute            |
| **Supported Cards**    | Credit cards only — debit card transactions cannot be disputed via this feature |
| **Dispute Processing** | Velera (PSCU) Dispute Management Console                                        |
| **Dispute Tracking**   | Via Zendesk — viewable in "Support Messages" in the Inbox                       |
| **Dispute Amount**     | Full amount or partial amount (member's choice)                                 |
| **Channels**           | Online Banking ✓                                                                |
| **Supported Cores**    | Correlation, Ultradata                                                          |
| **Release Version**    | 10.41                                                                           |

### Key Use Cases

| Use Case                    | Member Goal                                                        | Steps                                                                                                                             | Outcome                                                                                 |
| --------------------------- | ------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| Dispute a merchant charge   | Challenge a charge the member does not recognize or disagrees with | Navigate to the transaction in card history, tap Raise Dispute, select a merchant-related reason, enter amount, and submit        | Dispute submitted to Velera; member receives a Zendesk confirmation in Support Messages |
| Dispute a potential fraud   | Report a suspicious or unauthorized charge                         | Select a fraud-related reason; an alert prompts consideration of reporting the card as lost or stolen before continuing to submit | Dispute submitted; member can also initiate a lost/stolen card report in parallel       |
| Submit a partial dispute    | Dispute only a portion of a transaction amount                     | On the amount screen, choose Partial and enter the specific amount to dispute                                                     | Only the specified partial amount is submitted for dispute                              |
| Track a submitted dispute   | Check the current status of a dispute after submission             | Go to Inbox › Support Messages to find the Zendesk thread for the dispute                                                         | Member sees current status (e.g. Submitted, In Review, Resolved) updated by CU staff    |
| Reply with more information | Provide additional details to the credit union after submitting    | Open the dispute thread in Support Messages and reply directly in the Zendesk thread                                              | CU staff receive the supplemental information and can act on it                         |

### Step-by-Step Guide

\| _📍 Navigation path: Banking › Cards › \[select card] › Transaction History › Kebab menu (⋮) on transaction › Raise Dispute_ |

**User Journey Overview**

Login → Cards Overview → Cards → Transaction History → Kebab menu on transaction → Raise Dispute

![](../.gitbook/assets/velera-dispute-001.png)

**Step 1 Navigate to Transaction History**

From the nFinia home screen, navigate to Banking › Cards and select the credit card you want to dispute a transaction on. Open Card Details and locate the transaction in the Transaction History list. Tap the Kebab menu (⋮) icon on the transaction and select Raise Dispute.

\| ⚠️ Note: The Raise Dispute option is only available for Credit Card transactions. Velera does not support disputes for debit card transactions. If the transaction is outside the eligible dispute period, a notice will be shown to the member. |

| ![](../.gitbook/assets/velera-dispute-002.png) | ![](../.gitbook/assets/velera-dispute-003.png) |
| :--------------------------------------------: | :--------------------------------------------: |

**Step 2 Select a Dispute Reason**

The dispute reason screen displays a list of reasons dynamically pulled from the Velera Dispute Management Console. Review the list and select the reason that best describes the issue with the transaction.

\| ℹ️ Tip: Dispute reasons are configured in the Velera Dispute Management Console by your credit union. The list shown to members reflects exactly what has been set up there. |

| ![](../.gitbook/assets/velera-dispute-004.png) | ![](../.gitbook/assets/velera-dispute-005.png) |
| :--------------------------------------------: | :--------------------------------------------: |

**Step 3 Fraud Alert & Additional Questions**

If the selected reason implies fraud (e.g. an unauthorized charge), an alert is shown prompting the member to consider reporting their card as lost or stolen. This ensures the appropriate fraud-handling steps are taken. For non-fraud reasons, additional questions specific to that reason type are shown — these questions are also configured in Velera and surfaced dynamically.

| ![](../.gitbook/assets/velera-dispute-006.png) | ![](../.gitbook/assets/velera-dispute-007.png) |
| :--------------------------------------------: | :--------------------------------------------: |

**Step 4 Enter the Dispute Amount**

Choose to dispute the full transaction amount or enter a partial amount. If disputing a partial amount, tap Partial and type in the specific dollar value you want to dispute. Complete any remaining required fields before proceeding.

| ![](../.gitbook/assets/velera-dispute-008.png) | ![](../.gitbook/assets/velera-dispute-009.png) | ![](../.gitbook/assets/velera-dispute-010.png) |
| :--------------------------------------------: | :--------------------------------------------: | :--------------------------------------------: |

**Step 5 Review Dispute Details**

Once all the details have been filled in, a summary screen is shown for review. Verify that the transaction details, reason, and amount are correct before submitting.

![](../.gitbook/assets/velera-dispute-011.png)

| ![](../.gitbook/assets/velera-dispute-012.png) | ![](../.gitbook/assets/velera-dispute-013.png) |
| :--------------------------------------------: | :--------------------------------------------: |

**Step 6 Submit the Dispute**

After reviewing the details, tap Submit to send the dispute to Velera. A Zendesk ticket is automatically created at the time of submission so the member can track the dispute status. If the Zendesk ticket submission fails, the member will have the opportunity to retry.

![](../.gitbook/assets/velera-dispute-014.png) ![](../.gitbook/assets/velera-dispute-015.png)

\| ■ Tracking Your Dispute via Support Messages |

Velera does not provide real-time dispute status updates directly to members. As a solution, Summerville Credit Union uses Zendesk integration to send status alerts and enable dispute tracking within nFinia. When the credit union staff updates the status of the dispute in the Velera Dispute Management Console, they also update the corresponding Zendesk ticket — which triggers an alert to the member.

\| ⚠️ Note: There is no automatic sync between Velera and Zendesk. CU staff must update both systems manually to ensure members receive accurate status notifications. |

**Step 7 Track Your Dispute in Support Messages**

After a dispute is submitted, open the Inbox from the nFinia navigation and tap Support Messages. The dispute thread is listed there with the current status (e.g. Submitted, In Review, Resolved). Status updates are reflected here as the credit union staff progresses the dispute in Velera and updates the Zendesk ticket.

| ![](../.gitbook/assets/velera-dispute-016.png) | ![](../.gitbook/assets/velera-dispute-017.png) |
| :--------------------------------------------: | :--------------------------------------------: |

**Step 8 Reply with Additional Information**

If the credit union requests more information or if the member has additional details to provide, they can reply directly in the Support Messages thread. The reply is sent to the credit union via Zendesk.

| ![](../.gitbook/assets/velera-dispute-018.png) | ![](../.gitbook/assets/velera-dispute-019.png) |
| :--------------------------------------------: | :--------------------------------------------: |

\| ℹ️ Tip: Keep an eye on your Notifications and Inbox for status alert emails from Zendesk. You will receive an alert each time the credit union updates the status of your dispute. |
