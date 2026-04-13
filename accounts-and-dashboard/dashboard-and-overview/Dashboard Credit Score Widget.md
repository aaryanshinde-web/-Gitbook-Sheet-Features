---
description: >-
  The Credit Score meter widget on the Dashboard — a visual gauge showing the
  member's current credit score range without leaving the landing screen.
---

# Credit Score Widget

**SUMMERVILLE CREDIT UNION · CONSOLIDATED MEMBER GUIDE · DASHBOARD MODULE**

Module: nFinia Digital Banking > Dashboard > Credit Score Meter Widget

*Sources: Summerville Reports Series A (36 docs) + Series B (25 docs) | Features: nFinia Documentation Features Spreadsheet*

## 01 PRODUCT SUMMARY

The Credit Score Widget is a compact visual gauge displayed on the Dashboard's right panel. It gives the member an at-a-glance view of their current credit score without navigating to the full Credit Score & Financial Tools feature (CSUM-27, accessible via More > Credit Score).

The widget displays a colour-coded semicircular gauge with score range labels — **Poor**, **Fair**, **Good**, **Very Good**, and **Excellent** — and a needle or marker indicating where the member's current score falls. The numeric score is displayed prominently below or within the gauge. A **"Read More"** link at the bottom of the widget navigates to the full Credit Score page where the member can view score factors, score history, FICO FAQs, and manage consent.

The score shown in the widget is the same soft-pull credit bureau score displayed in the full Credit Score feature. It is retrieved via an integrated third-party credit bureau partner and does not impact the member's credit rating. The widget refreshes when the Dashboard loads — it does not poll in real-time.

**Important distinction:** This page documents the **Dashboard widget** — the small gauge visible on the landing screen. For the full Credit Score feature (consent flow, score factors, score history, FICO FAQs, Financial Tools), see [Credit Score & Financial Tools](Credit%20Score%20Financial%20Tools.md) (CSUM-27).

## At a Glance

| Attribute | Detail |
|---|---|
| Feature Name | Credit Score Meter (Dashboard Widget) |
| Module | Dashboard > Right Panel |
| User Roles | All authenticated members who have completed credit score consent |
| Access Level | Post-login; visible on Dashboard if consent has been granted |
| Score Source | Integrated third-party credit bureau (soft pull — no credit impact) |
| Display Elements | Colour gauge, numeric score, score range labels, "Read More" link |
| Actions Available | View score, click "Read More" to navigate to full Credit Score page |
| Pre-Consent State | Widget prompts member to access Credit Score for first-time consent |
| Theme Support | Gauge adapts colours and backgrounds for Light and Dark mode |
| Related Reports | CSUM-02 (Dashboard), CSUM-27 (Credit Score & Financial Tools), CSUM-36 (FICO Score Meter) |

## 02 KEY USE CASES

| Use Case | Who Uses It | What They Do | Business Value |
|---|---|---|---|
| Daily Score Glance | Member monitoring credit health | Views the gauge on Dashboard login — no navigation needed | Instant credit awareness on every login without extra clicks |
| Score Change Detection | Member who recently paid off debt | Notices the gauge needle has moved since last login | Motivates positive financial behaviour by making progress visible |
| Navigate to Full Details | Member who wants to understand score factors | Clicks "Read More" on the widget to go to full Credit Score page | Seamless discovery path from widget to detailed feature |
| First-Time Consent Prompt | New member who hasn't accessed Credit Score yet | Sees widget prompt, clicks to initiate consent flow | Drives adoption of Credit Score feature from the Dashboard |
| Theme-Aware Viewing | Member using Dark Mode | Views the credit score gauge with dark-mode-adapted colours | Consistent, readable experience across both themes |

## 03 END-TO-END WORKFLOW

*Navigation: The Credit Score widget is on the Dashboard right panel. No navigation required — it is visible after login (if consent has been completed).*

### Step 1 — View the Credit Score Widget on the Dashboard

After logging in, the member sees the Credit Score meter widget on the right panel, typically positioned below the Upcoming Payments section. The widget displays:

- A **semicircular colour gauge**: red (Poor) → orange (Fair) → yellow (Good) → light green (Very Good) → green (Excellent)
- A **needle or marker** pointing to the member's current position on the scale
- The **numeric score** (e.g., 720) displayed prominently
- **Score range labels** below the gauge
- A **"Read More"** link at the bottom

<figure><img src="/.gitbook/assets/4d84470d6d89d8a6fa87d3208abb4fab251f5cf4.png" alt="Dashboard in Light Mode showing Credit Score meter widget with colour gauge" width="340"><figcaption>Credit Score widget on the Dashboard — Light Mode</figcaption></figure>

### Step 2 — Interpret the Score

The gauge colour ranges correspond to standard credit score brackets:

| Colour | Range | Rating |
|---|---|---|
| Red | 300–579 | Poor |
| Orange | 580–669 | Fair |
| Yellow | 670–739 | Good |
| Light Green | 740–799 | Very Good |
| Green | 800–850 | Excellent |

The member's score and its position on the gauge provide an immediate visual assessment of their credit standing.

### Step 3 — Click "Read More" for Full Details

Clicking the **"Read More"** link navigates the member to the full **Credit Score & Financial Tools** page (CSUM-27). On that page, the member can:

- View key factors affecting their score
- Review score history and trend over time
- Read FICO Score FAQs
- Access Financial Tools (goals, budgeting) where available
- Re-confirm or manage consent

### Pre-Consent State

If the member has not yet completed the credit score consent flow, the widget displays a prompt (e.g., "Access your Credit Score") with a link or button that navigates to the consent screen. After consent is granted, the widget automatically populates with the member's score on subsequent logins.

<figure><img src="/.gitbook/assets/img_c11a5a1ced0c.png" alt="Credit Score consent screen shown when member accesses the feature for the first time" width="480"><figcaption>First-time consent screen (accessed via widget or More menu)</figcaption></figure>

## 04 LIGHT MODE vs. DARK MODE

| Element | Light Mode | Dark Mode |
|---|---|---|
| Card Background | White with subtle shadow | Dark navy/charcoal |
| Gauge Colours | Standard red-orange-yellow-green gradient | Same gradient, slightly brighter for contrast |
| Score Text | Dark text on white background | White/light text on dark background |
| Range Labels | Grey text below gauge | Light grey text below gauge |
| "Read More" Link | Blue link text | Bright blue link text |

Both modes display the same score data with identical functionality.

<figure><img src="/.gitbook/assets/8c7bc558be6f326e79504593b267c6ca1205b01c.png" alt="Dashboard in Dark Mode showing Credit Score meter widget with adapted colours" width="340"><figcaption>Credit Score widget on the Dashboard — Dark Mode</figcaption></figure>

## 05 WIDGET vs. FULL FEATURE COMPARISON

| Capability | Dashboard Widget | Full Credit Score Page (CSUM-27) |
|---|---|---|
| View current score | Yes (gauge + number) | Yes (detailed display) |
| Score range visualisation | Yes (colour gauge) | Yes |
| Key score factors | No | Yes |
| Score history / trend | No | Yes |
| FICO FAQs | No | Yes |
| Consent management | Prompts to consent if needed | Full consent flow |
| Financial Tools (goals, budgets) | No | Yes (where available) |
| "Read More" navigation | Links to full page → | — (this IS the full page) |

## 06 QUICK REFERENCE

| Task | How | Who Can Do It | Notes |
|---|---|---|---|
| View credit score at a glance | Dashboard > Credit Score widget (right panel) | Members with consent completed | Refreshes on Dashboard load |
| Get full score details | Dashboard > Credit Score widget > "Read More" | Members with consent completed | Navigates to CSUM-27 |
| Complete first-time consent | Dashboard > Credit Score widget > "Access your Credit Score" | All members | One-time consent flow |
| View score in Dark Mode | Toggle theme > Dashboard | All members | Gauge adapts automatically |

## Related Pages

- [Dashboard](README.md) — parent page and full Dashboard layout
- [Dashboard & Activities](Dashboard%20Activities.md) — full Dashboard walkthrough
- [Credit Score & Financial Tools](Credit%20Score%20Financial%20Tools.md) — the full Credit Score feature (CSUM-27)
- [FICO Score Meter](../../accounts-and-dashboard/account-features/CSUM-36-FICO-Score-Meter.md) — FICO-specific score documentation
- [Light & Dark Theme](../../settings-help-and-misc/settings-and-preferences/Dashboard%20Light%20Dark%20Theme.md) — theme personalisation
