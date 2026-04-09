# Plaid IAV — Instant Account Verification

**Vendor:** Plaid\
**Status:** Documented\
**Module:** Move Money — External Transfers

## Overview

Plaid's Instant Account Verification (IAV) integration allows nFinia members to securely link external bank accounts for ACH transfers by logging into their external institution via Plaid's verification flow. This eliminates the need for manual micro-deposit verification.

## Key Features

- Instant external account linking via Plaid IAV
- Secure OAuth-based credential flow — nFinia never sees external bank credentials
- Supports linking of checking and savings accounts
- Real-time account ownership and balance verification
- Fallback to micro-deposit verification when IAV is unavailable

## Navigation

**nFinia App:** Move Money → External Transfers → Add External Account → Link via Plaid

## Supported Institutions

Plaid supports thousands of financial institutions across the US, including major banks and credit unions.

> **Documentation Note:** Full integration specifications, Plaid Link configuration, and webhook setup are available in the `plaid-iav-implementation.md` reference document and the IAV Implementation — Plaid guide.
