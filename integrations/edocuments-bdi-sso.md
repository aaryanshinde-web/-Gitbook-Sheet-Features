---
description: BDI SSO eDocuments integration — secure electronic statement and document delivery for Diamond Credit Union members via nFinia Digital Banking.
---

# eDocuments — BDI SSO

**Vendor:** BDI (Banking Document Intelligence)\
**Module:** More Menu → eDocuments / Statements\
**Integration Type:** SSO Redirect

---

## Overview

The BDI integration provides Diamond Credit Union members with on-demand access to electronic statements, tax documents, notices, and other official correspondence — all delivered securely through the nFinia app. Members authenticate once through nFinia and are seamlessly redirected to the BDI eDocuments portal.

---

## Key Features

| Feature | Description |
| --- | --- |
| **eStatements** | Monthly account statements in PDF format |
| **Tax Documents** | Year-end tax forms (1099-INT, 1098, etc.) |
| **Notices & Letters** | Regulatory notices and correspondence from Diamond CU |
| **Document Search** | Filter documents by account, type, and date range |
| **Paperless Enrollment** | Members can enroll in / opt out of paper statements |
| **Download & Print** | PDF download available for all documents |

---

## Member Flow

1. Member navigates to **More Menu → eDocuments** in nFinia.
2. nFinia generates a time-limited SSO token and redirects the member to the BDI portal.
3. The BDI portal authenticates the member automatically — no separate login.
4. Member browses, views, and downloads documents.
5. Session expires after inactivity; member is returned to nFinia.

---

## Configuration Notes

{% hint style="info" %}
**Enrollment Prompt:** First-time users are prompted to enroll in eStatements and agree to receive electronic communications in lieu of paper mail.
{% endhint %}

| Parameter | Details |
| --- | --- |
| **Auth Method** | SSO token (SAML or JWT, per BDI configuration) |
| **Supported Formats** | PDF |
| **Retention Period** | Up to 7 years (configurable per Diamond CU policy) |
| **Accessibility** | Documents are screen-reader compatible PDFs |
