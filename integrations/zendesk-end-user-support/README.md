---
description: >-
  ZenDesk End User Support Portal integration — member-facing help center and
  ticket submission within nFinia Digital Banking.
---

# End User Support Portal - ZenDesk

**Vendor:** Zendesk\
**Module:** Member Support & Help Center\
**Integration Type:** SSO / Embedded Widget

***

## Overview

The ZenDesk integration brings a full-featured member support portal directly into the nFinia digital banking experience. Members can browse a searchable knowledge base, submit support tickets, and track ticket status - all without leaving the app or calling the credit union.

***

## Key Features

| Feature | Description |
| -------------------------- | --------------------------------------------------------------------------------------------- |
| **Knowledge Base** | Searchable articles covering common member questions and how-to guides |
| **Ticket Submission** | Members can open support requests with attachments directly from nFinia |
| **Ticket Status Tracking** | Real-time status updates on open and resolved tickets |
| **SSO Authentication** | Member is authenticated automatically via nFinia session — no separate ZenDesk login required |
| **Chat Widget** | Optional live-chat widget surfaced within the app (requires ZenDesk Chat add-on) |

***

## Member Flow

1. Member navigates to **More Menu → Help & Support** within nFinia.
2. The ZenDesk portal is loaded in an embedded webview, authenticated via SSO token.
3. You can search articles, open a ticket, or start a chat session.
4. Tickets submitted are routed to the Caltech Employees Federal Credit Union ZenDesk workspace.
5. Email notifications keep you updated on ticket progress.

***

## Configuration Notes

{% hint style="info" %}
**Prerequisite:** A ZenDesk account with SSO (JWT or OAuth) must be provisioned for Caltech Employees Federal Credit Union. Contact the Tyfone implementation team for SSO token configuration.
{% endhint %}

| Parameter | Details |
| ------------------ | -------------------------------------------------------------------- |
| **Authentication** | JWT-based SSO using nFinia member session |
| **Subdomain** | `summervillecu.zendesk.com` |
| **Ticket Routing** | Routed to the `nfinia-support` view in the ZenDesk workspace |
| **Branding** | ZenDesk Help Center theme customizable to match Caltech Employees FCU brand |
