**Dashboard -- Light & Dark Theme**

Feature Delivery Guide

Summerville Federal Credit Union \| nFinia Platform \| April 2026

  ------------------------
  **1. Product Summary**
  ------------------------

The Dashboard Light & Dark Theme feature provides Summerville Federal Credit Union You with the ability to switch their nFinia Online Banking dashboard between a Light Mode and a Dark Mode visual appearance. This personalization option allows You to choose the interface aesthetic that best suits their preference, environment, and accessibility needs.

Light Mode presents the dashboard with a clean, open feel---white and light blue backgrounds, high-contrast dark text, and soft card shadows. Dark Mode transforms the entire interface into a deep navy-purple palette with vibrant accent colors, reducing eye strain in low-light environments while maintaining full readability and feature parity. Every dashboard widget, navigation element, account tile, sidebar link, and footer section adapts seamlessly to the selected theme.

The theme toggle is available to all authenticated You and persists across sessions. It applies to the full post-login experience including the Account Overview, Quick Transfer widget, Credit Score meter, Related Links sidebar, and footer. This feature positions Summerville FCU as a modern, member-centric institution that prioritizes digital experience quality alongside functional banking capabilities.

**At a Glance**

  -------------------------- --------------------------------------------------------------------------
  **Attribute**              **Detail**
  **Feature Name**           Dashboard Light & Dark Theme
  **Module**                 Dashboard / Account Overview
  **User Roles**             All authenticated You
  **Access Level**           User preference; toggle available in Settings or header
  **Key Actions**            Toggle theme, View accounts, Quick Transfer, Credit Score, Related Links
  **Regulatory Relevance**   WCAG 2.1 accessibility compliance; inclusive design
  **Platform Version**       nFinia OLB v10.49+
  -------------------------- --------------------------------------------------------------------------

  ------------------
  **2. Use Cases**
  ------------------

  -------------------------- --------------------------- -------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------
  **Use Case**               **Who Uses It**             **What They Do**                                                                                                                             **Business Value**
  Night-Time Banking         Any Member                  Switches to Dark Mode for comfortable banking in low-light environments; all account info, balances, and actions remain fully accessible     Reduces eye strain; increases session duration and engagement
  Daytime Readability        Any Member                  Uses Light Mode during the day for maximum contrast and readability on bright screens                                                        Optimal legibility in well-lit environments
  Accessibility Preference   Visually Sensitive Member   Selects the theme that best accommodates their visual sensitivity, color perception, or personal comfort                                     Supports WCAG compliance; inclusive banking experience
  Brand Consistency Demo     FI Marketing / Sales        Demonstrates to prospects and board that the credit union offers a modern, customizable digital experience comparable to top-tier neobanks   Competitive differentiation; member acquisition support
  Device Battery Savings     Mobile/Tablet User          Enables Dark Mode on OLED/AMOLED devices to reduce power consumption during banking sessions                                                 Practical benefit that signals tech-savvy platform design
  -------------------------- --------------------------- -------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------

Theme personalization is increasingly table stakes in consumer-facing digital products. By offering both Light and Dark modes, Summerville FCU demonstrates that its digital banking platform matches the experience quality You expect from premium apps like Apple, Google, and leading neobanks. This directly supports member satisfaction and digital adoption metrics.

  ----------------------------
  **3. End-to-End Workflow**
  ----------------------------

**3.1 Prerequisites**

• Member must have an active online banking enrollment with Summerville FCU

• Theme support must be enabled at the FI configuration level (nFinia Admin)

• Compatible browser or device with CSS dark-mode rendering support

**3.2 Step-by-Step Flow**

**Step 1 -- Dashboard (Light Mode):** Member logs into nFinia Online Banking and lands on the Account Overview dashboard in Light Mode (default). The interface presents a clean, white and light-blue color scheme with the Summerville wave logo, navigation bar (Dashboard, Accounts, Move Money, More), account balance tiles with dark navy headers, Quick Transfer widget, Upcoming Payments section, Credit Score meter, and Related Links sidebar. The footer displays branch information, contact details, and compliance logos against a light background.

<figure><img src="/.gitbook/assets/4d84470d6d89d8a6fa87d3208abb4fab251f5cf4.png" alt="" width="340"><figcaption></figcaption></figure>{width="3.9583333333333335in" height="5.947916666666667in"}

*Figure 1: Summerville FCU Dashboard -- Light Mode*

**Step 2 -- Dashboard (Dark Mode):** Member toggles the theme to Dark Mode. The entire dashboard transforms to a deep navy-purple palette. Account tiles use vibrant gradient backgrounds, the navigation bar and header shift to dark tones with bright accent text, the Quick Transfer widget and Credit Score meter adapt their backgrounds and text colors for dark-mode readability, and the footer transitions to a matching dark scheme. All functionality remains identical---only the visual presentation changes. Balances, links, widgets, and actions are all fully accessible in both themes.

<figure><img src="/.gitbook/assets/8c7bc558be6f326e79504593b267c6ca1205b01c.png" alt="" width="340"><figcaption></figcaption></figure>{width="3.8541666666666665in" height="5.84375in"}

*Figure 2: Summerville FCU Dashboard -- Dark Mode*

**3.3 Decision Points & Branching**

• Theme selection persists across sessions via user preference stored server-side; you does not need to re-select on each login.

• If the FI has not enabled Dark Mode at the configuration level, only Light Mode is available and no toggle is displayed.

• Both themes maintain identical navigation paths, widget layouts, and feature access---no functionality is lost or altered by theme selection.

**3.4 Completion & Confirmation**

Theme switching is instant with no page reload required. The system applies the new color palette via CSS class toggling. you see an immediate visual transition. The preference is saved automatically and reflected on the next login.

**3.5 Error Handling**

• If the browser does not support CSS custom properties (very rare in modern browsers), the system falls back to Light Mode.

• If the preference save fails, the theme reverts to the default on next login but the current session remains in the selected theme.

• No destructive errors are possible as theme switching is purely cosmetic.

  ------------------------------------------
  **4. Feature Overview (UI Walkthrough)**
  ------------------------------------------

**Dashboard Components -- Light vs. Dark**

Both themes render the same set of dashboard components. The table below documents each component and how it adapts between Light and Dark modes.

  ----------------------- ------------ ---------------------------------------------------------------------------------------------- -------------------------------------------------------------------
  **Component**           **Type**     **Light Mode Appearance**                                                                      **Dark Mode Appearance**
  Header / Logo           Navigation   White background, Summerville wave logo, dark text navigation links                            Deep navy background, same logo, light/white text links
  Navigation Bar          Nav Links    Light blue background; Dashboard, Accounts, Move Money, More in dark text                      Dark purple background; same items in bright/white text
  Greeting Banner         Label        \"Good Morning, Simon Williams\" in dark text on light background                              Same greeting in white text on dark background
  Promotional Banner      Marketing    \"Take a load off\" direct deposit promo on blue gradient card                                 Same promo with adjusted gradient for dark context
  Account Tiles           Data Cards   Dark navy tile headers with white text; white body with balances                               Vibrant gradient tile headers; dark body with light text balances
  Quick Transfer Widget   Form         White card with standard form inputs, blue Transfer button                                     Dark card with adapted inputs, bright Transfer button
  Upcoming Payments       Widget       White card with border, \"No upcoming payments\" message                                       Dark card with adapted border and text colors
  Credit Score Meter      Widget       White card with colored gauge (red-yellow-green), score ranges, Read More link                 Dark card with same gauge; adapted text and background
  Related Links Sidebar   Link List    White card with blue text links: Change Password, Download E-Statements, etc.                  Dark card with bright blue/white links, arrow indicators
  Footer                  Layout       Light background with branch info, contact hours, NCUA/Equal Housing logos, Summerville logo   Deep navy footer with same content in light text; logos adapted
  ----------------------- ------------ ---------------------------------------------------------------------------------------------- -------------------------------------------------------------------

  ------------------------
  **5. Quick Reference**
  ------------------------

  ------------------------- ------------------------------------ ------------------- ------------------------------
  **Task**                  **Navigation Path**                  **Who Can Do It**   **Notes**
  Switch to Dark Mode       Settings > Theme or header toggle   All You         Persists across sessions
  Switch to Light Mode      Settings > Theme or header toggle   All You         Default theme for new users
  View account balances     Dashboard > Balances                All You         Identical in both themes
  Initiate Quick Transfer   Dashboard > Quick Transfer widget   All You         Same form in both themes
  View Credit Score         Dashboard > Credit Score widget     All You         Gauge adapts to theme colors
  Access Related Links      Dashboard > Related Links sidebar   All You         Links adapt to theme
  ------------------------- ------------------------------------ ------------------- ------------------------------

*--- End of Document ---*
