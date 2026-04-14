---
description: External ACH Transfer
---
# External ACH Transfer

## Summary

External ACH Transfer enables members to send and receive funds between their Summerville CU accounts and accounts held at other financial institutions — using the ACH network with standard 1–3 business day settlement. For business members funding a business account from a personal account at another bank, paying a vendor whose banking relationship is at a different institution, or collecting a receivable via ACH pull, this feature provides a fully self-service external transfer channel that avoids wire fees for non-time-critical payments.

## Key Use Cases

Business members initiate ACH pushes to fund a business operating account from an external personal or business account when internal account balances fall below operating thresholds. Members use ACH pull to collect a payment from a customer or partner who has authorised the debit — entering the external account details and the collection amount directly in the transfer form. Members also use External ACH to transfer personal funds from a credit union account to a brokerage or investment account held elsewhere, consolidating cash movement within a single authenticated session rather than initiating the transfer from the receiving institution.

## Step-by-Step Guide

**Step 1 — Navigate to External ACH Transfer**

From the Move Money menu, select **External Transfer** to open the External ACH Transfer form. If this is the first external transfer, the member must first add and verify the external account — either through Plaid instant verification or micro-deposit confirmation — before the transfer can be initiated.

<figure><img src="../../.gitbook/assets/Screenshot 2026-04-13 at 3.16.24 PM.png" alt=""><figcaption></figcaption></figure>

**Step 2 — Select Accounts, Enter Amount, and Choose Direction**

Select the Summerville CU account as either the source (push) or destination (pull), then select the verified external account for the other side of the transaction. Enter the transfer amount and select the transfer direction — **Send** to push funds out or **Receive** to pull funds in — then choose a delivery date or select immediate initiation.

<figure><img src="../../.gitbook/assets/image (6) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Step 3 — Review and Confirm**

The confirmation screen displays the full transfer details — source account, destination account, amount, direction, and estimated settlement date. Click **Submit** to initiate the ACH transaction; a confirmation reference number is issued and the transfer enters the ACH processing queue for the next available batch.

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

### Error Handling

| Scenario | Member Experience | Recovery |
| --- | --- | --- |
| External account not yet verified | Transfer form blocks submission | Complete Plaid IAV or micro-deposit verification first |
| Insufficient funds in source account | Inline validation error on submission | Fund the source account or reduce the transfer amount |
| ACH return (R01, R02, R03) | Notification in Inbox; transfer reversed | Verify external account details and resubmit |
| Daily transfer limit exceeded | Limit error shown on form | Split into multiple transfers or contact the credit union to review limits |
