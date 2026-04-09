**SUMMERVILLE CREDIT UNION · BUSINESS BANKING USER GUIDE · CSUM-06 of 16**

**Role Management**

Module: Business Banking > Role Management

**Navigation: Dashboard → Business Banking → Role Management**

*Sources: Summerville Reports Series A + Series B | Features: nFinia Documentation Features Spreadsheet*

## PRODUCT SUMMARY

Role Management is the administrative backbone of business banking access control within the nFinia platform. It allows business administrators to define roles (such as View-only, Basic Role, or custom roles) that determine what features, transaction types, and monetary limits each user can access. Each role encompasses four configurable dimensions: Permissions (which features are accessible), Limits (transaction amount thresholds per payment type), Users (which team members are assigned to the role), and Settings (role-level configuration).

The system ships with default roles (View-only with a lock icon indicating it cannot be deleted) and supports unlimited custom role creation. Business admins can granularly control access to ACH transfers, wire transfers, bill pay, internal transfers, and administrative functions. Transaction limits can be set per role for daily, per-transaction, and cumulative thresholds.

For credit unions, role management is a critical differentiator that enables them to serve multi-user businesses. It provides the dual-control and segregation-of-duties capabilities that commercial businesses require for regulatory compliance and internal fraud prevention.

**At a Glance**


| Attribute            | Detail                                                                           |
| -------------------- | -------------------------------------------------------------------------------- |
| Feature Name         | Role Management                                                                  |
| Module               | Business Banking > Role Management                                               |
| Navigation           | Dashboard → Business Banking → Role Management                                   |
| User Roles           | Business Admin, Business Owner                                                   |
| Access Level         | Admin-only; requires Role Management permission                                  |
| Key Actions          | View roles, Create role, Edit role, Assign permissions, Set limits, Assign users |
| Regulatory Relevance | Dual-control compliance, segregation of duties, audit trail                      |


## KEY USE CASES


| Use Case               | Who Uses It    | What They Do                                        | Business Value                                          |
| ---------------------- | -------------- | --------------------------------------------------- | ------------------------------------------------------- |
| Create Custom Role     | Business Admin | Add a new role with specific permissions and limits | Tailors access to business organizational structure     |
| Set Transaction Limits | Business Owner | Configure per-role ACH, wire, and payment limits    | Enforces spending controls aligned with business policy |
| Assign Users to Role   | Business Admin | Move team members into appropriate roles            | Ensures each employee has correct level of access       |
| Audit Role Permissions | Business Owner | Review permissions and limits across all roles      | Supports compliance audits and internal controls review |
| View-only Access       | Business Admin | Assign read-only role to bookkeepers or accountants | Provides visibility without transaction authority       |


## STEP-BY-STEP USER GUIDE

**How to get here: Dashboard → Business Banking → Role Management**

**Step 1: Log In and Open the Dashboard**

Open your web browser and navigate to the Summerville Credit Union digital banking platform. Enter your username and password on the login screen and click "Log In." If prompted, complete the OTP (One-Time Passcode) verification by entering the code sent to your registered device. After successful authentication, you will land on the Dashboard — also called the Account Overview screen. This is your home base. The Dashboard displays all your business accounts (Savings Accounts, Checking Accounts) with their available and current balances. The top navigation bar shows links to Dashboard, Accounts, Transfer & Pay, Cards, Business Banking, and More. On the right sidebar you will see Related Links (Change Password, Account Settings, View Scheduled Transfers, Account Specific Alerts) and a Quick Transfer widget for fast internal transfers. To proceed to Business Banking features, locate the "Business Banking" tab in the top navigation bar and click on it.

<figure><img src="/.gitbook/assets/img_5c532a850867.png" alt="Figure 1 — Log In and Open the Dashboard" width="620"><figcaption></figcaption></figure>

*Figure 1 — Log In and Open the Dashboard*

**Step 2: Open the Business Banking Hub**

After clicking "Business Banking" in the top navigation bar, the Business Banking Hub loads. This is the central command center for all commercial banking operations. The Hub is organized into three sections: "Transfers" at the top (with tiles for ACH Transfer, Domestic Wire Transfer, Transfer Template, and Payment From File), "Manage" in the middle (with tiles for Role Management, User Management, Approval Settings, and Recipient Management), and "More Options" at the bottom (with tiles for Commercial Activity, Reports, and Approvals). Each tile is a direct entry point to its corresponding feature. Only tiles your role has permission to access will be visible. From here, locate and click the tile for the feature you need — the next steps will guide you through the specific workflow.

<figure><img src="/.gitbook/assets/img_04cfec25c89e.png" alt="Figure 2 — Open the Business Banking Hub" width="620"><figcaption></figcaption></figure>

*Figure 2 — Open the Business Banking Hub*

**Step 3: Navigate to Role Management**

From the Dashboard, click "Business Banking" in the left-side navigation menu to open the Business Banking Hub. In the "Manage" section, click the "Role Management" tile. The Role Management dashboard appears, listing all roles defined for your business. Each role is displayed as a card showing the role name, the number of active users assigned to it, and a lock icon for system-protected roles (like "View-only") that cannot be deleted. You will see tabs on each card: Permissions, Limits, Users, and Settings. Click any tab to expand that dimension for the selected role. To create a new role, click "Create New Role" at the top of the page.

<figure><img src="/.gitbook/assets/img_8d45475efcb3.png" alt="Figure 3 — Navigate to Role Management" width="620"><figcaption></figcaption></figure>

*Figure 3 — Navigate to Role Management*

**Step 4: View and Configure Role Permissions**

Click the "Permissions" tab on any role card to expand the permission configuration panel. You will see a checklist of toggle switches for every business banking feature: ACH Transfer (Send/Receive), Wire Transfer, Transfer Templates, Payment From File, Role Management, User Management, Approval Settings, Recipient Management, Commercial Activity, Reports, Approvals, Business Alerts, and more. To enable a feature for this role, toggle the switch to ON (active color). To remove access, toggle it OFF (grayed out). A "Select All" option at the top enables every permission at once. Changes are saved when you click "Save" at the bottom of the panel.

<figure><img src="/.gitbook/assets/img_7e357dc169f1.png" alt="Figure 4 — View and Configure Role Permissions" width="620"><figcaption></figcaption></figure>

*Figure 4 — View and Configure Role Permissions*

**Step 5: Scroll to See All Permission Categories**

Scroll down within the Permissions panel to see additional permission categories not visible in the initial view. These extended permissions cover payment processing controls (can this role initiate vs. only approve transactions), administrative access (can this role manage other roles or users), reporting permissions (which report types are visible), and alert configuration rights. Review every category to ensure the role has exactly the access it needs — no more, no less. For example, an "AP Clerk" role should have ACH Transfer and Recipient Management enabled, but Role Management and User Management disabled.

<figure><img src="/.gitbook/assets/img_60ce07d30c13.png" alt="Figure 5 — Scroll to See All Permission Categories" width="620"><figcaption></figcaption></figure>

*Figure 5 — Scroll to See All Permission Categories*

**Step 6: Set Transaction Limits for the Role**

Click the "Limits" tab on the role card. A table appears with rows for each payment type (ACH Transfer, Wire Transfer, Internal Transfer, Bill Pay) and columns for Per-Transaction Limit and Daily Cumulative Limit. Click into each dollar amount field and type the appropriate limit value. For example, set ACH Per-Transaction to $5,000 and ACH Daily Cumulative to $25,000 for a basic role. These limits are enforced in real-time — if a user assigned to this role attempts a transaction exceeding these thresholds, the system will block it. Click "Save" when finished. Adjust limits based on business need and risk tolerance.

<figure><img src="/.gitbook/assets/img_3620d7ef4a06.png" alt="Figure 6 — Set Transaction Limits for the Role" width="620"><figcaption></figcaption></figure>

*Figure 6 — Set Transaction Limits for the Role*

**Step 7: View Users Assigned to the Role**

Click the "Users" tab on the role card to see all team members currently assigned to this role. Each entry shows the user's name, email, and status (Active, Locked, etc.). To add a user to this role, click "Add User" and select from the list of unassigned users. To remove a user from the role, click the remove button next to their name. Removing a user from a role revokes all permissions associated with that role immediately. The user will need to be reassigned to a different role to regain access.

<figure><img src="/.gitbook/assets/img_0fceaeeac761.png" alt="Figure 7 — View Users Assigned to the Role" width="620"><figcaption></figcaption></figure>

*Figure 7 — View Users Assigned to the Role*

**Step 8: Review Role Settings**

Click the "Settings" tab to view role-level configuration. Here you can edit the role name and description. The description field should document the role's purpose (e.g., "For accounts payable staff who process vendor payments"). Settings may also include role-specific behaviors like whether transactions initiated by this role require approval from another role. Update the settings as needed and click "Save."

<figure><img src="/.gitbook/assets/img_172e9b24de22.png" alt="Figure 8 — Review Role Settings" width="620"><figcaption></figcaption></figure>

*Figure 8 — Review Role Settings*

**Step 9: Edit an Existing Role**

To modify an existing role, click the "Edit" button on the role card. The role editor opens with all four dimensions (Permissions, Limits, Users, Settings) in editable mode. Make your changes — add or remove permissions, adjust limits, reassign users, or update the description. When finished, click "Save" to apply changes. All changes take effect immediately for all users assigned to this role. Be cautious when editing roles with active users, as permission changes affect their access in real-time.

<figure><img src="/.gitbook/assets/img_97f899c30c5e.png" alt="Figure 9 — Edit an Existing Role" width="620"><figcaption></figcaption></figure>

*Figure 9 — Edit an Existing Role*

**Step 10: Create a New Role — Enter the Role Name**

Click "Create New Role" from the Role Management dashboard. A creation form opens. Enter a descriptive role name in the Name field (e.g., "AP Clerk," "CFO," "Branch Manager," or "Auditor"). Choose a name that clearly reflects the role's function within your organization, as this name will appear throughout the platform wherever role assignments are displayed. Click "Continue" or "Next" to proceed to permission configuration.

<figure><img src="/.gitbook/assets/img_51dad663417d.png" alt="Figure 10 — Create a New Role — Enter the Role Name" width="620"><figcaption></figcaption></figure>

*Figure 10 — Create a New Role — Enter the Role Name*

**Step 11: Confirm the Role Name and Proceed**

The role name is now entered in the field. Verify the spelling and clarity of the name. If it needs correction, click into the field and edit it. When satisfied, click "Continue" to advance to the privilege selection step. The role name can be changed later through the Settings tab if needed, but it is best practice to set a clear, descriptive name from the start to maintain an organized role structure.

<figure><img src="/.gitbook/assets/img_cfe6587bdb36.png" alt="Figure 11 — Confirm the Role Name and Proceed" width="620"><figcaption></figcaption></figure>

*Figure 11 — Confirm the Role Name and Proceed*

**Step 12: Select Feature Privileges for the New Role**

The privilege selection step presents high-level feature categories organized into logical groups (Transfers, Management, Reporting, etc.). Click the checkbox or toggle next to each feature group this role should access. Within each selected group, individual features can be toggled on or off for more granular control. A summary counter shows how many of the total available privileges are enabled. Select only the features necessary for this role's job function — following the principle of least privilege minimizes security risk. Click "Continue" to proceed to entitlement configuration.

<figure><img src="/.gitbook/assets/img_1bd620c4d1b8.png" alt="Figure 12 — Select Feature Privileges for the New Role" width="620"><figcaption></figcaption></figure>

*Figure 12 — Select Feature Privileges for the New Role*

**Step 13: Configure Detailed Entitlements and Save**

The entitlements step provides the finest level of access control. Within each selected privilege group, individual actions are listed with toggle switches. For example, within "ACH Transfer" you may see: Initiate ACH Send, Initiate ACH Receive, Approve ACH, View ACH History, and Cancel Pending ACH. Toggle each action on or off based on what this role should be able to do. After configuring all entitlements, click "Save" (or "Create Role") to finalize. The new role immediately appears in the Role Management dashboard and is ready for users to be assigned to it.

<figure><img src="/.gitbook/assets/img_f2c55d215091.png" alt="Figure 13 — Configure Detailed Entitlements and Save" width="620"><figcaption></figcaption></figure>

*Figure 13 — Configure Detailed Entitlements and Save*

