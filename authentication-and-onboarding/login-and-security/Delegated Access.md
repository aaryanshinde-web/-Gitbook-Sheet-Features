**Summerville Federal Credit Union**

nFinia Digital Banking Platform

**Delegated Access**

Feature Release Notes & Product Guide

Prepared by: Jeeva Krishnamurthy, Senior Product Manager

Tyfone, Inc. \| April 2026 \| Confidential

  ------------------------
  **1. Product Summary**
  ------------------------

Delegated Access is a core feature of the nFinia Digital Banking platform that enables primary account holders to securely grant secondary users controlled access to their financial accounts. This capability is essential for business banking, joint account holders, caregivers managing finances for dependents, and any scenario where multiple individuals need visibility or transactional authority over shared accounts.

Within the Summerville Federal Credit Union digital banking portal, Delegated Access is accessible from the Dashboard under the Secondary Users section. The feature provides a comprehensive management framework that includes adding secondary users, assigning granular feature-level permissions, defining account access and transaction limits, monitoring secondary user activity, and managing the end-to-end enrolment lifecycle.

For Summerville FCU, Delegated Access strengthens the business banking value proposition by providing the multi-user authorization frameworks that commercial You require. It reduces operational burden on branch staff by enabling self-service user management while maintaining full audit trails and compliance controls. Business You benefit from the ability to delegate routine banking tasks to trusted employees without exposing full account credentials, ensuring both convenience and security.

**At a Glance**

  ---------------------- ---------------------------------------------------------------------------------------------
  **Attribute**          **Detail**
  Feature Name           Delegated Access (Secondary User Management)
  Module                 Business Banking > Dashboard > Secondary Users
  User Roles             Primary Account Holder, Secondary User, FI Administrator
  Access Level           Role-based with granular feature permissions (View Only, Full Access, Custom)
  Key Actions            Add User, Assign Permissions, Set Account Access & Limits, Monitor Activity, Approve/Deny
  Regulatory Relevance   BSA/AML compliance, dual-control authorization, full audit trail, 24-hour invitation expiry
  ---------------------- ---------------------------------------------------------------------------------------------

  ------------------
  **2. Use Cases**
  ------------------

  -------------------------------------------- -------------------------- ------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------
  **Use Case**                                 **Who Uses It**            **What They Do**                                                                                                          **Business Value**
  Grant employee access to business accounts   Business Owner (Primary)   Adds a secondary user, assigns feature permissions and selects specific accounts to share with transaction limits         Enables delegation of routine banking tasks to trusted staff without sharing full credentials
  Approve or deny pending transactions         Primary Account Holder     Reviews secondary user's pending transfers in the Approvals tab and approves or denies each transaction                   Maintains dual-control over fund movements, reducing fraud risk and ensuring compliance
  Monitor secondary user activity              Primary Account Holder     Views the Secondary User Activity log filtered by user, date, and transaction type to see all actions taken               Provides full visibility and audit trail for delegated actions, supporting regulatory requirements
  Secondary user self-enrolment                Invited Secondary User     Receives email invitation, clicks Accept, creates credentials, verifies identity via OTP, and logs in                     Self-service onboarding reduces FI operational burden and enables immediate access within 24-hour window
  Manage permissions after onboarding          Primary Account Holder     Accesses User Profile to edit permissions, change account access, adjust limits, or deactivate the user                   Allows dynamic permission management as business roles evolve without requiring branch visits
  View shared account as secondary user        Secondary User             Logs into the portal with delegated credentials and accesses only the accounts and features granted by the primary user   Enables controlled participation in account management without full ownership privileges
  -------------------------------------------- -------------------------- ------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------

These use cases reflect the core scenarios encountered by Summerville FCU's business You who need to delegate banking authority. The combination of granular permissions, dual-control approvals, and comprehensive activity logging addresses both the operational convenience requirements of small businesses and the compliance obligations of the credit union.

  ----------------------------
  **3. End-to-End Workflow**
  ----------------------------

**3.1 Prerequisites**

• Primary account holder must be enrolled in Summerville FCU digital banking with an active membership.

• The Delegated Access feature must be enabled for the membership by the FI administrator.

• The primary user must have at least one eligible account (checking, savings, or loan) to share.

• The secondary user must have a valid email address to receive the invitation.

**3.2 Step-by-Step Workflow**

**Step 1: Log in to Summerville FCU Dashboard**

<figure><img src="/.gitbook/assets/f3baee20922a81473c94f88c7dc5d2b96ed0796f.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="4.041666666666667in"}

The primary user logs into the Summerville Federal Credit Union digital banking portal and lands on the Dashboard. The Dashboard provides a consolidated view of account summaries, recent transactions, quick actions, and key financial insights.

From the Dashboard, the user navigates to the Secondary Users section under Personal Settings to access all Delegated Access functionality.

**Step 2: Secondary Users Management Hub**

<figure><img src="/.gitbook/assets/0ec0dff056ede78dfade7488479121ffa9fa7130.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="2.9166666666666665in"}

The Secondary Users hub is the central management screen with three primary tabs: Secondary User Management, Approvals, and Secondary User Activity. The right sidebar provides Related Links for quick navigation.

From this screen, the primary user can view all existing secondary users, manage pending approvals, and access the activity audit log. This serves as the command center for all delegated access operations.

**Step 3: Add a New Secondary User --- Enter Details**

<figure><img src="/.gitbook/assets/a851a2002507b398b2253c12d54d9e0f16988566.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="4.979166666666667in"}

To add a new secondary user, the primary user clicks the Secondary User Management tab and selects "Add User." The system presents a form requiring First Name, Last Name, Email Address, and Phone Number.

The phone number field includes a country code selector (defaulting to United States +1). All fields are required. The system validates the email format before allowing the user to proceed to the next step.

**Step 4: Assign Feature Permissions**

<figure><img src="/.gitbook/assets/314b280fe493ea3ebe0b0d955541a9c6a577cc97.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="3.6875in"}

The next step presents the Select Feature Permissions screen. The primary user can either clone permissions from an existing secondary user or create new custom permissions.

This two-path approach streamlines the process: for businesses with standardized roles, cloning an existing user's permissions ensures consistency; for unique access needs, the custom path provides full flexibility.

**Step 5: Configure Granular Access Levels**

<figure><img src="/.gitbook/assets/59f2458c39fe2ece67c1207229727be003744c50.png" alt="" width="340"><figcaption></figcaption></figure>{width="6.458333333333333in" height="11.927083333333334in"}

When creating new permissions, the system displays three access levels: View Only (can only view features and account details), Full Access (complete account access with no restricted actions), and Custom (view details and perform selected actions).

The permissions grid covers Account Information, Alerts, Approvals, Banking Services, Settings, Support, and Transfers/Payments. Each category can be expanded to toggle individual features on or off, providing precise control over what the secondary user can do.

**Step 6: Select Accounts to Share**

<figure><img src="/.gitbook/assets/326cb39659e4673b99328a239831187ecf61a191.png" alt="" width="480"><figcaption></figcaption></figure>{width="6.458333333333333in" height="7.958333333333333in"}

After setting permissions, the primary user selects which specific accounts to share with the secondary user. The screen lists all own accounts including savings, checking, credit cards, and loans with their account numbers and membership details.

At least one account must be selected to proceed. This granular account selection ensures the secondary user only sees the accounts relevant to their role, protecting the primary user's other financial relationships.

**Step 7: Configure Transaction Limits**

<figure><img src="/.gitbook/assets/935e9be6a2101d256f329c761d236618cfc93e37.png" alt="" width="340"><figcaption></figcaption></figure>{width="6.458333333333333in" height="10.1875in"}

For each shared account, the primary user can set transaction limits that control the maximum amounts the secondary user can transact. Limits can be configured per transaction type (transfers, payments, etc.) and per time period (daily, weekly, monthly).

This limit-setting capability is critical for business banking compliance. It ensures that delegated users cannot exceed authorized transaction thresholds, providing a financial safeguard that satisfies both the business owner and regulatory requirements.

**Step 8: Review and Confirm Setup**

<figure><img src="/.gitbook/assets/707e7e7bdfaf54bc063a76b95801ba5055de95f4.png" alt="" width="480"><figcaption></figcaption></figure>{width="6.458333333333333in" height="7.25in"}

The system presents a comprehensive review screen summarizing all configured settings: user details, assigned permissions, selected accounts, and transaction limits. The primary user can go back to modify any section or confirm to send the invitation.

Upon confirmation, the system generates a secure invitation email that is sent to the secondary user's registered email address. The invitation includes a unique link that expires within 24 hours for security purposes.

**3.3 Secondary User Enrolment**

**Step 9: Invitation Email Received**

<figure><img src="/.gitbook/assets/926c73fd76372a6ba6abd3b0d115f3b26d31c0fe.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="4.65625in"}

The secondary user receives an email notification from the platform informing them that the primary account holder has invited them to access their account in Summerville FCU Digital Banking.

The email contains an "Accept Invitation" button, clear instructions to complete setup, and a security notice that the invitation expires in 24 hours. If the recipient was not expecting the invitation, they are advised to ignore it.

**Step 10: Begin Enrolment --- Login or Register**

<figure><img src="/.gitbook/assets/c67b52a301cba107d43d9f40f3e4228244f51bd5.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="3.6354166666666665in"}

Clicking the invitation link takes the secondary user to the enrolment landing page. The system asks whether they already have login credentials (for existing digital banking users) or need to create new ones.

This branching logic supports two scenarios: existing You who already have portal credentials can link the delegated access to their existing login, while new users proceed through the full registration flow.

**Step 11: Create Account Credentials**

<figure><img src="/.gitbook/assets/9fb4c0bd0220d8a80221484108dd21f5eec35f52.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="4.96875in"}

New secondary users create their account by entering a username and password. The system enforces strong credential requirements: username must be 8--25 characters without spaces or special symbols, and the password must be 8--20 characters with at least one number, one letter, one uppercase letter, one lowercase letter, and one special character.

A progress stepper at the top (Create your account → Identity verification → One-Time Passcode → Success) shows the user where they are in the four-step enrolment process.

**Step 12: Enrolment Complete**

<figure><img src="/.gitbook/assets/c6691b82bd52b4e53370ffcbfc59280c14902d42.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="2.7708333333333335in"}

After identity verification and OTP confirmation, the secondary user sees a "Congratulations!" success screen confirming they have been successfully enrolled into digital banking. A "Log in" button allows immediate access.

Upon first login, the secondary user's dashboard will display only the accounts and features that the primary user has authorized, ensuring the principle of least privilege is maintained from the very first session.

**3.4 Post-Setup Management & Monitoring**

**Step 13: View and Edit User Profile**

<figure><img src="/.gitbook/assets/18a57863c251a6f03a298c96202ca435815184b0.png" alt="" width="480"><figcaption></figcaption></figure>{width="6.458333333333333in" height="7.90625in"}

After enrolment, the primary user can access the secondary user's profile to view and modify all delegated access settings. The User Profile screen displays user management details, account control settings, current access level, and shared accounts with their limits.

From this screen, the primary user can edit permissions, change account access, adjust transaction limits, reset the secondary user's password, or deactivate the user entirely. This provides ongoing lifecycle management for delegated access.

**Step 14: Review Pending Approvals**

<figure><img src="/.gitbook/assets/6c1bbd71c0e6dc800e22dd6e4e95ecd0b8ee9d6b.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.010416666666667in"}

The Secondary User Activity screen provides a comprehensive audit log of all actions taken by secondary users. The primary user can filter by secondary user name and view transaction details including date, activity type, status (Pending approval, Processed), and amount.

Each transaction entry shows full details: the fund transfer type, source and destination accounts, memo fields, and approval status. Pending transactions can be approved or denied directly from this view, enabling the dual-control authorization workflow that is critical for business banking compliance.

**3.5 Notification & Alert System**

**Step 15: Alerts to Secondary User**

<figure><img src="/.gitbook/assets/86de7fc2065967a5c7ce74d902d91e83c567a91e.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="4.875in"}

Secondary users receive email notifications for key events in the delegated access lifecycle. These include invitation emails, enrolment confirmations, transaction approval/denial notifications, and account access change alerts.

The notification system ensures secondary users stay informed about their access status and any actions taken on transactions they initiated, maintaining transparency throughout the delegated access relationship.

**Step 16: Alerts to Primary User**

<figure><img src="/.gitbook/assets/008087bd12f428858a8969f81d10eb63152327c3.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="5.135416666666667in"}

Primary account holders receive notifications when secondary users perform significant actions, including fund transfers that require approval, account access requests, and profile changes.

These alerts enable the primary user to maintain oversight of delegated activities without having to constantly monitor the portal, supporting the dual-control governance model.

**3.6 Harmoney Integration --- Secondary User in Core**

**Step 17: Member Profile in Core System**

<figure><img src="/.gitbook/assets/3eea5ffdd4e8c21db17119e5e27aa78cba560fa5.png" alt="" width="620"><figcaption></figcaption></figure>{width="6.458333333333333in" height="4.072916666666667in"}

The Delegated Access feature integrates with the Harmoney core banking system. When a secondary user is added through the digital banking portal, their profile is reflected in the core system's member management module.

This integration ensures that delegated access relationships are maintained consistently across both the digital banking platform and the core banking infrastructure, providing a single source of truth for user access and permissions.

  ------------------------
  **4. Quick Reference**
  ------------------------

  -------------------------------------- --------------------------------------------------------------------------- ------------------------ -------------------------------------------------------------
  **Task**                               **Navigation Path**                                                         **Who Can Do It**        **Notes**
  Add secondary user                     Dashboard > Secondary Users > Secondary User Management > Add User       Primary Account Holder   Requires email and phone for invitation
  Clone permissions from existing user   Add User > Select Feature Permissions > Use existing user's permissions   Primary Account Holder   Copies feature permissions; accounts must still be selected
  Set custom permissions                 Add User > Select Feature Permissions > Create new permissions            Primary Account Holder   Three levels: View Only, Full Access, Custom
  Select accounts to share               Add User > Select Accounts to share                                        Primary Account Holder   At least one account required
  Set transaction limits                 Add User > Account Access & Limits                                         Primary Account Holder   Per-transaction and per-period limits available
  Approve/deny transactions              Dashboard > Secondary Users > Approvals                                   Primary Account Holder   Pending transactions shown with full details
  View secondary user activity           Dashboard > Secondary Users > Secondary User Activity                     Primary Account Holder   Filterable by user, date, transaction type
  Edit user permissions                  Secondary User Management > User Profile > Permissions > Edit            Primary Account Holder   Changes take effect immediately
  Deactivate secondary user              Secondary User Management > User Profile > Deactivate User                Primary Account Holder   Revokes all access; can be reactivated
  Accept invitation                      Email > Accept Invitation link                                             Invited Secondary User   Invitation expires in 24 hours
  Enrol as secondary user                Invitation link > Create account > Verify identity > OTP                 Secondary User           4-step enrolment process
  -------------------------------------- --------------------------------------------------------------------------- ------------------------ -------------------------------------------------------------

  -------------------
  **5. Conclusion**
  -------------------

Delegated Access is a foundational capability for Summerville Federal Credit Union's business banking offering on the nFinia platform. The feature addresses a critical gap in the credit union's digital services by enabling primary account holders to securely and granularly delegate banking authority to secondary users. With comprehensive permission management, account-level access controls, transaction limits, dual-control approvals, and full activity auditing, the feature provides the enterprise-grade multi-user framework that business You expect from their primary financial institution.

The self-service enrolment workflow reduces operational overhead for branch staff while maintaining robust security controls including 24-hour invitation expiry, strong credential requirements, and multi-factor identity verification. The integration with Harmoney core banking ensures consistency across the technology stack. For Summerville FCU, Delegated Access strengthens member retention by meeting the multi-user needs of growing businesses that might otherwise seek commercial banking services from larger institutions.
