### <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image11.png" alt="" width="620"><figcaption></figcaption></figure><figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image3.png" alt="" width="480"><figcaption></figcaption></figure>

### 

### 

### 

### 

### 

### 

### 

### 

### 

Delegated Access

Securely Share Account Access with Family & Friends

### 

### 

### 

### 

### 

### 

### 

### 

### 

### 

### 

### 

# Delegated Access 

This release introduces the Delegated Access feature, which allows a
primary retail account holder to grant controlled access to their
accounts to a secondary user. The following detailed breakdown is
organized by the sections outlined in the project's requirements
document, providing a complete overview of all new functionalities and
behaviors.

**Platform:** Web, Mobile

**Release Version:** 10.45

## Overview

This feature enables primary account holders in retail banking to grant
delegated access to secondary users such as family members, friends,
accountants, or caretakers. The delegated access user will have a
controlled level of permissions, ensuring security and compliance.

  - > Important Points:
    
      - > The feature is specifically for retail accounts.
    
      - > Access is controlled and not full, unrestricted access.

## Channels

> The Delegated Access feature is accessible through :

  - > Online Banking

  - > Mobile Banking.

  - > Harmoney: Enables back-office staff to manage secondary users'
    > access and permissions, and provides reports and logs related to
    > this feature.

## User Journey

A primary account holder wants to grant another individual delegated
access to help them manage their account. The user journey is as follows
-

### Adding a Secondary User 

  - > Primary account holder initiates access via the digital banking
    > from the following:
    
      - > More section \> Delegated Access

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image16.png" alt="" width="620"><figcaption></figcaption></figure>

  - > Navigate to \> Delegated Access

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image32.png" alt="" width="620"><figcaption></figcaption></figure>

  - > Related Links \> Delegated Access

<!-- end list -->

  - > Agreement/T\&C will be presented to the member when they are
    > accessing the feature for the first time. Once they accept, OTP
    > verification is required to verify primary's identity (This is a
    > configurable step).

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image13.png" alt="" width="620"><figcaption></figcaption></figure>

  - > First Name, Last Name, DoB, Contact number, Email Address of the
    > new user is to be entered by the primary user. The contact
    > information is later used to verify the identity of the secondary
    > user.

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image29.png" alt="" width="620"><figcaption></figcaption></figure>

### Assign Feature Permissions to the Secondary User

  - > The member can either copy permissions of an existing user (if
    > available) or create new permission.

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image18.png" alt="" width="620"><figcaption></figcaption></figure>
> 
> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image23.png" alt="" width="340"><figcaption></figcaption></figure>

  - > There is a role and user construct in this functionality. Here the
    > roles are static and are called Access Levels. We have 3 access
    > levels : View-Only, Limited Access & Full Access. The permission
    > template for each of these access levels are set by default and
    > they can be configured by each CU according to their policies.
    > They can be found
    > [<span class="underline">here</span>](https://docs.google.com/spreadsheets/d/1cqxdVejIFMhiMlHorFI19a2EISI5RQH_1b9iKaPB7jE/edit?gid=1742618718#gid=1742618718).
    
      - > View Access:
        
          - > Capabilities:
            
              - > Can view all account details, including summaries,
                > balances, and transaction histories.
            
              - > Use Case: Ideal for users who require insight into
                > account data without the ability to make any changes
                > or perform transactions.
    
      - > Limited Access:
        
          - > Capabilities:
            
              - > Includes all "View-only" permissions plus the ability
                > to perform specific transactions and features selected
                > by the primary user (e.g., Bill Pay, Internal/External
                > Transfers, or Mobile Deposits).
        
          - > Use Case: Ideal for users who need to assist with daily
            > financial tasks—like paying a specific bill or depositing
            > a check—without having full control over the account.
    
      - > Full Access
        
          - > Capabilities:
            
              - > Allows the user to perform all major account
                > operations, such as initiating transactions, managing
                > payments, and accessing detailed account information.
        
          - > Restrictions:
            
              - > Cannot change primary's contact details (mobile
                > number, address), Add or delete device information,
                > add a new trusted device using CDA, changing MFA
                > contact information
            
              - > Cannot add another user.
            
              - > Cannot close the account.
            
              - > Cannot overdraw the account.
            
              - > Cannot open new accounts.

> **Note**: Although users with Full Access can manage most aspects of
> the account, critical actions remain restricted to protect account
> integrity and ensure that key decisions (e.g., account closure or
> adding new users) are controlled by the primary account holder.

  - > Rule of allocation of feature permission:
    
      - > By default Create new Permission will be selected in radio
        > button
    
      - > By default 1st role (usually view only) coming from MCB will
        > be will be selected so that permissions of that role will be
        > visible
    
      - > Users will be able to change permission selection for any
        > access level. This enables the user to be able to assign any
        > newly released feature to sub user after the Delegate Access
        > Feature is live
    
      - > If the user will select/de-select the permission radio button,
        > then irrespective of role it will become custom access level
        > and custom access will be assigned. In this case permissions
        > selected from the previous role be selected instead of Actual
        > Master Custom Access Level. Ex - By default View Only is
        > selected & user clicks on a new radio button, then view only
        > permissions will remain selected but the assigned role will be
        > Custom.
    
      - > If External accounts permission is ON, the external account
        > will be available in the account access list and also in the
        > fund transfer drop down. If the permissions are not enabled,
        > the accounts will not be displayed for assignment.

  - > If a user selects copy permission from an existing user then
    > selected user roles & permissions will be highlighted after
    > refreshing the page. Rules mentioned above will still be
    > applicable in this case.

### Account Access & Limits

  - > After selecting the permissions that the primary wants to assign
    > to the secondary user, next the user can move on to selecting the
    > accounts they want to share. Here, primary can share access to
    > their own accounts & External accounts. Primary or Joint can only
    > delegate access to the accounts that they are primary or joint on.
    > They cannot delegate on any other lower membership types.

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image39.png" alt="" width="480"><figcaption></figcaption></figure>

  - > The allocated Account will be visible to secondary users only if
    > membership / account is not deleted or closed by the Owner.

  - > The owner will be able to update the limit & will be able to
    > revoke the account access from secondary users.

  - > After providing the access, primary users have to set the transfer
    > limit for each account.

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image24.png" alt="" width="340"><figcaption></figcaption></figure>

  - > Following rules will apply on the transfer limit
    
      - > Primary Users can set only send limits.
    
      - > Secondary users cannot transfer more than the primary user
        > limit.
    
      - > For an individual secondary user, available transfer limit at
        > the time of transfer will be calculated like this (Primary
        > user transfer limit - Transfer already done by all secondary
        > users)
    
      - > The transfer limit logic is cumulative for all secondary
        > users. For example, if the primary user's per-transfer limit
        > is $1000, and User A has spent $500 and User B has spent $500,
        > User C will not be allowed to transact as the limit has been
        > reached.
    
      - > If the primary's limit is lowered by an admin, the limits for
        > the delegated access user are automatically lowered as well.
    
      - > The receive money limit will be the common limit for FI from
        > the policy engine. Limit check will be done by the policy
        > only.
    
      - > If there are only user level or member level limits defined at
        > the policy engine, the same limits will be copied by default
        > for every account that is selected by the primary to share.
    
      - > Secondary users cannot directly initiate transactions to the
        > core system. All transactions are processed on behalf of the
        > primary user only. The secondary user activity will be
        > captured in logs for audit purposes.
    
      - > Most restrictive limits will be applied amongst account type
        > limits, policy engine limits, secondary user limits.
    
      - > If Account is not allowed in the "Source" account of fund
        > transfer, that account will not be available in the limits
        > screen.
    
      - > If Account is not allowed in the "Destination" account of fund
        > transfer, the account will be displayed for transfer out
        > limits.

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image19.png" alt="" width="480"><figcaption></figcaption></figure>

**Transaction Limits & Transaction Types at Account Level** :

|               | **Transaction Types**                   |                                         |                                         |
| ------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
|               | Between My Accounts Within Credit Union | To Another Member                       | To External Account                     |
| Per Transfer  | Max Value: Primary's Per Transfer Limit | Max Value: Primary's Per Transfer Limit | Max Value: Primary's Per Transfer Limit |
| Daily Limit   | Max Value: Primary's Daily Limit        | Max Value: Primary's Daily Limit        | Max Value: Primary's Daily Limit        |
| Monthly Limit | Max Value: Primary's Monthly Limit      | Max Value: Primary's Monthly Limit      | Max Value: Primary's Monthly Limit      |

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image37.png" alt="" width="480"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image38.png" alt="" width="620"><figcaption></figcaption></figure>

  - > Transfer goes via make-checker when the secondary user exceeds the
    > transfer limit (daily, per transfer, monthly) assigned by the
    > primary user. Meaning, if the secondary users cross their limit,
    > an approval request will be sent to the primary account holder. If
    > they cross primary's limits (set by the FI via policy engine),
    > approval will not be sent and transfer will fail. These requests
    > will be visible to both the user and the primary in the Approval
    > Requests section. The primary can approve or decline the approval
    > request by adding their comments

  - > Secondary users CANNOT approve requests on primary's behalf. This
    > permission should not be assigned to secondary users.

  - > Secondary users will NOT have delegated access feature permission.
    > And hence, they will not be able to add another user.

  - > Joint at Member level
    
      - > In a case where joint a member adds a secondary user, the
        > primary user of M1 member won't be see the secondary user
        > because the secondary user is added at the user level not at
        > the member level
    
      - > Primary members will not get the notification of the secondary
        > user added by a joint member today.
    
      - > Primary members won't see secondary users added by a joint
        > member, and won't be able to perform any role change or
        > feature change on behalf of the joint member of the same
        > membership.

  - > When a primary member unenrolls themselves, even the secondary
    > user loses access to their accounts

Note: Primary account holders can revoke / manage access levels anytime.
Permissions can be controlled both by FI-staff and the primary member.

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image26.png" alt="" width="620"><figcaption></figcaption></figure>

### Profile Switcher

  - > Profile Switcher section will contain a dedicated section for
    > Delegated Access that will contain all the access given to the
    > secondary from the primary user.

  - > For both Logged in as primary & Logged in as secondary who is a CU
    > member :
    
      - > All memberships and All personal memberships will retain the
        > existing behaviour and have the accounts shared by primary in
        > delegated access in fund transfer. Permissions will be what
        > they have in their all memberships switcher.

  - > Only when they switch to their delegated access profile, those
    > accounts and permissions should be reflected that is assigned to
    > them - not all permissions (for eg some SSOs may not be available
    > to them)

  - > Logged in as secondary user who is not a CU member - this user
    > will have behaviour according to the delegated access profile
    > selected

<table>
<thead>
<tr class="header">
<th><strong>Switcher Profile</strong></th>
<th><strong>Behavior</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>All Memberships</td>
<td><p>Account → Retail + Business all accounts shown</p>
<p>Fund Transfer(Own Account) → Retail → Business &amp; Business → Retail allowed</p>
<p>Fund Transfer(Other Member + External)</p>
<p>Retail → Retail,</p>
<p>Business → Business allowed</p>
<p>Schedule Transfer(Other Member + External) → Retail + Business memberships displayed. SRT will be listed based on member selected</p>
<p>Manage Recipient → Retail + Business Recipients shown</p>
<p>Requests → Delegated Access + All Business listed</p>
<p>Add Secondary User → Retail + Business Accounts shown</p></td>
</tr>
<tr class="even">
<td>All Personal</td>
<td><p>Account → Only Retail accounts shown</p>
<p>Fund Transfer(Own Account) → Only Retail → Retail allowed</p>
<p>Fund Transfer(Other Member + External)</p>
<p>Only Retail → Retail allowed</p>
<p>Schedule Transfer(Other Member + External) → Only Retail allowed. SRT will be listed based on member selected</p>
<p>Manage Recipient → Only Retail Recipients shown</p>
<p>Requests → Only Delegated Access shown</p>
<p>Add Secondary User → Retail + Business Accounts shown</p></td>
</tr>
<tr class="odd">
<td>All Business</td>
<td><p>Account → Only Business accounts shown</p>
<p>Fund Transfer(Own Account) → Only Business → Business allowed</p>
<p>Fund Transfer(Other Member + External)</p>
<p>Only Business → Business recipients allowed</p>
<p>Schedule Transfer(Other Member + External) → Only Business allowed. SRT will be listed based on member selected</p>
<p>Manage Recipient → Only Business Recipients shown</p>
<p>Requests → Delegated Access + All Business memberships shown. Details will be displayed based on member selected</p>
<p>Add Secondary User → Retail + Business Accounts shown</p></td>
</tr>
<tr class="even">
<td>Individual Business Selected</td>
<td><p>Account → Individual Business accounts shown</p>
<p>Fund Transfer(Own Account) → Only individual Business → Individual Business allowed</p>
<p>Fund Transfer(Other Member + External)</p>
<p>Only Individual Business → Individual Business recipients allowed</p>
<p>Schedule Transfer(Other Member + External) → Only Individual Business is listed. SRT will be listed based on member selected</p>
<p>Manage Recipient → Only Individual Business Recipients shown</p>
<p>Requests → Delegated Access + Individual Business memberships shown. Details will be displayed based on member selected</p>
<p>Add Secondary User → Retail + Business Accounts shown</p></td>
</tr>
</tbody>
</table>

### Secondary User Activity:

In this section, all the transactions by secondary users can be viewed
and filtered by every user. Here, all transactions are shown
irrespective of the profile switcher selected

### <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image27.png" alt="" width="620"><figcaption></figcaption></figure>

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image6.png" alt="" width="620"><figcaption></figcaption></figure>
> 
> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image35.png" alt="" width="620"><figcaption></figcaption></figure>

### Future Enhancements:

  - > **Behaviour**: Scheduled transfer detail link may show "no active
    > SRT message" immediately after submitting an SRT (scheduled ACH)
    > because the core reference ID isn't retrieved at post time.
    
      - > Scope: Affects ACH SRTs shown under Commercial Activity;
        > internal transfers are not impacted because they aren't
        > displayed there.
    
      - > Behavior: The newly submitted SRT won't appear in Commercial
        > Activity immediately; it becomes visible after a refresh or
        > when viewing under the SRT page/list.
    
      - > Root cause: ACH transactions are stored on the core; reference
        > ID is available on retrieve/edit/delete calls but not captured
        > on the initial post response.
    
      - > Limitations: Reversal for SRTs isn't supported because the
        > core (Symitar) doesn't return individual SRTs; reversal works
        > only for individual transactions.
    
      - > Next steps: Future enhancement required to read and persist
        > the core reference ID on post so Commercial Activity can link
        > immediately after submission.

### Enrolment of a Secondary User:

  - > The secondary user will receive an invite from the primary user to
    > get access to the account shared by the primary user. The
    > invitation expires after 24 hours. This is similar to Business
    > banking sub-user flow.

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image36.png" alt="" width="620"><figcaption></figcaption></figure>

  - > The secondary user must choose whether they have credentials to
    > access digital banking or not. If they have credentials to access,
    > the account will be mapped to that user. If not, they will be
    > prompted to enroll themselves.

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image28.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image12.png" alt="" width="620"><figcaption></figcaption></figure><figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image25.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image21.png" alt="" width="620"><figcaption></figcaption></figure><figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image20.png" alt="" width="620"><figcaption></figcaption></figure>

  - > Log-in Method:
    
      - > No login credentials
        
          - > Username and password are created for the secondary user
        
          - > No dependency on the core
        
          - > OTP is sent to email and phone number for verification
    
      - > Existing login credentials
        
          - > They will be required to login to digital banking
        
          - > Profile switcher is available to see accounts where access
            > is given
    
      - > The secondary user logs in with their own credentials but
        > accesses everything else within the profile as primary.
        > However, these activities are captured in the activity logs as
        > secondary users (except for transaction activity.

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image4.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image10.png" alt="" width="620"><figcaption></figcaption></figure>

### View of the User Profile after enrolment: 

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image40.png" alt="" width="480"><figcaption></figcaption></figure>

### Notifications & Alerts 

#### Alerts to the Secondary User: 

  - > Secondary user invite (Email Only)

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image42.png" alt="" width="620"><figcaption></figcaption></figure>

  - > Secondary user contact update (Email)

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image33.png" alt="" width="620"><figcaption></figcaption></figure>

  - > Secondary user account access update (Email & SMS) - Configuration

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image34.png" alt="" width="620"><figcaption></figcaption></figure>

#### Alerts to the Primary User: Email & SMS

  - > Transaction approval when the secondary user exceeds the limit
    > assigned to them.

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image41.png" alt="" width="620"><figcaption></figcaption></figure>

## 

## Configurations

### Delegated Access Configuration (Backend)

These settings control the Delegated Access feature, which allows a
primary user to grant a secondary user secure access to their account.

| **Technical Key**                              | **Description**                                                                                                                                                                                                             |
| ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DELEGATED\_ACCESS\_ENABLED                     | Delegated Access Feature Status: Indicates if the feature is turned ON (Y) or off.                                                                                                                                          |
| DELEGATED\_ACCESS\_FEATURE\_PAYMENT\_RAIL\_MAP | **Delegated Payment Options:** Specifies which payment types are available to users with delegated access, such as transfers to external accounts (ACH), transfers to an owned account, and internal institution transfers. |
| INVITATION\_EXPIRATION\_SECONDS                | **Invitation Expiration Time:** The amount of time (in seconds) that the delegated access invitation is valid before it expires. (Currently set to 86,400 seconds, or 24 hours).                                            |

### Transaction Policy and Approval Configuration (Backend)

| **Technical Key**                                | **Description**                                                                                                                                                                                        |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| TRANSACTION\_ACCESS\_CONTROL\_ENGINE\_ENABLED    | **Transaction Approval Engine Status:** Indicates if the security/policy system for checking transactions is turned ON (Y).                                                                            |
| OWN\_ACCOUNT\_POLICY\_ENABLED                    | **Internal Transfer Policy Status:** Indicates if the security/policy system should check transfers between a user's own accounts.                                                                     |
| TRANSACTIONS\_TO\_VALIDATE\_WITH\_POLICY\_ENGINE | **Transactions Requiring Policy Check:** A list of specific transaction actions (like creating, editing, or deleting various transfers) that must be checked by the approval engine before proceeding. |
| USER\_EVENTS\_EXCHANGE\_WITH\_POLICY\_ENGINE     | **User Events Sent to Policy System:** A list of user actions (like adding a new recipient) that are sent to the policy system for logging or further security checks.                                 |
| NON\_APPLICABLE\_FEATURES\_IN\_BUSINESS\_BANKING | Disabled Business Banking Features: A list of feature codes (by their ID number) that are intentionally turned off and not available for Business Banking users.                                       |

### Other Configurations:

  - > The permission template for each of these access levels are set by
    > default and they can be configured by each CU according to their
    > policies.

  - > Agreement/T\&C will be presented to the member when they are
    > accessing the feature for the first time. Once they accept, OTP
    > verification is required to verify primary's identity (This is a
    > configurable step).

## 

### Delegated Access Configuration (Frontend)

| **Key**                             | **Value/Status** | **Description**                                                                                                                                                            |
| ----------------------------------- | ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DELEGATE\_ACCESS\_MASTER\_ROLE\_ID  | 133              | This is the internal ID used to identify the top-level role that grants Delegated Access authority.                                                                        |
| IS\_DELEGATE\_ACCESS\_ENABLED       | Y/N              | Enables/Disables the Delegated Access feature for Online Banking (OLB) and Mobile Banking (MB).                                                                            |
| DELEGATED\_ACCESS\_ENABLED          | Y/N              | Enables/Disables the Delegated Access feature for Mobile Banking (MB) and Mobile Commercial Banking (MCB).                                                                 |
| IS\_ENABLE\_BUSINESS\_BANKING\_LITE | Y/N              | If set to 'Y' (along with ENABLE\_BUSINESS\_BANKING as 'Y'), this is a specific setup to enable only Delegated Access without the full suite of Business Banking features. |
| ENABLE\_BUSINESS\_BANKING           | Y/N              | Master switch to enable/disable the full Business Banking suite for Mobile Banking (MB) and Mobile Commercial Banking (MCB).                                               |
| DELEGATE\_ACCESS\_CONFIG            | {}               | This is the placeholder for the detailed feature configuration analyzed in the previous response (e.g., limits, access levels).                                            |
| RETAIL\_USER\_BLOCKED\_FEATURE      | (Old Config)     | An older configuration used to block specific features for standard retail users.                                                                                          |

### Payment Rails (Front End)

DELEGATE\_ACCESS\_PAYMENT\_RAILS.  
These are the types of money movement features available to a delegate,
provided they are enabled ("isEnabled": true).

| **Key**            | **Label**           | **Slug**               | **Description**                                              |
| ------------------ | ------------------- | ---------------------- | ------------------------------------------------------------ |
| OWN\_ACCOUNT       | To Own Account      | own\_account\_transfer | Transfers between accounts owned by the parent user.         |
| INTRA\_INSTITUTION | To Internal Member  | internal\_transfer     | Transfers to other members within the same bank/institution. |
| STANDARD\_ACH      | To External Account | ach\_transfer          | Transfers to accounts at different banks (ACH).              |

### Delegate Access Limits (Frontend)

These define the financial constraints (limits) that can be set for a
delegate user's transactions.

| **Limit Key**                              | **Display Label**      | **Edit Label** | **Description**                                            |
| ------------------------------------------ | ---------------------- | -------------- | ---------------------------------------------------------- |
| MAX\_TRANSACTION\_AMOUNT\_PER\_TRANSACTION | Per Transfer Limit     | Per Transfer   | The maximum amount allowed for a single transaction.       |
| MAX\_DAILY\_AMOUNT\_LIMIT                  | Daily Transfer Limit   | Daily Limit    | The maximum cumulative amount allowed in a 24-hour period. |
| MAX\_MONTHLY\_AMOUNT\_LIMIT                | Monthly Transfer Limit | Monthly Limit  | The maximum cumulative amount allowed in a 30-day period.  |

### General Settings

| **Configuration Key**         | **Value Type**   | **Description**                                                                                                                                                         |
| ----------------------------- | ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| SHOW\_TERMS\_CONDITIONS       | true/false       | Controls whether the Terms and Conditions must be displayed (and potentially accepted) during the setup process.                                                        |
| GET\_ALL\_MEMBERS             | true/false       | Controls if all members of the organization/bank can be searched and invited as delegates.                                                                              |
| SHOW\_ONLY\_BUSINESS\_MEMBERS | true/false       | If GET\_ALL\_MEMBERS is true, this controls whether the search is filtered to only show Business Banking members.                                                       |
| DONT\_SHOW\_ACCOUNT\_ICON     | true             | Hides the account icon in the user interface, likely for a cleaner look when viewing delegated accounts.                                                                |
| ALLOW\_EDIT\_PERMISSIONS      | Array of strings | Specifies which delegate status types allow the parent user to edit the delegate's permissions (e.g., you can edit an ACTIVE or INACTIVE user, but likely not a DRAFT). |

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## 

## Harmoney

  - > Search for the primary member using the search functionality in
    > Harmoney. In the primary member's profile, in the secondary access
    > section, all accounts that member has secondary access to will be
    > visible at a glance.

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image5.png" alt="" width="620"><figcaption></figcaption></figure>

  - > Go to Overview & Support \> Secondary Users to perform more
    > actions

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image14.png" alt="" width="620"><figcaption></figcaption></figure>

  - > This section will have all the secondary users listed and
    > categorised as active and inactive

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image8.png" alt="" width="620"><figcaption></figcaption></figure>

  - > Within the secondary user profile, the admin can make changes to
    > the access level, permissions and account access.

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image1.png" alt="" width="620"><figcaption></figcaption></figure>

  - > When the admins change the access level, the default permissions
    > and limits that are defined for each access level will be applied
    > automatically

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image31.png" alt="" width="620"><figcaption></figcaption></figure>

  - > The admins can still choose to apply or revoke the permissions
    > after the access level has been changed.

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image30.png" alt="" width="620"><figcaption></figcaption></figure>

  - > The primary's own accounts, external accounts and internal account
    > access can be modified by the admin and only the type of transfer
    > can only be modified for the accounts that are eligible as a
    > source.

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image7.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image22.png" alt="" width="620"><figcaption></figcaption></figure>

  - > The admins can also modify the limits for such eligible accounts:
    > per transfer, daily, monthly limits

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image9.png" alt="" width="620"><figcaption></figcaption></figure>

  - > The secondary user's transaction activity can be viewed in
    > Accounts and Activity \> Secondary user activity

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image15.png" alt="" width="620"><figcaption></figcaption></figure>

  - > The secondary user profile will be tagged with the "Secondary
    > User" label for easy identification. Please note that this tag
    > will only be visible for secondary users who are not members of
    > the credit union

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image17.png" alt="" width="620"><figcaption></figcaption></figure>

  - > All the secondary users actions can be viewed in the Transactions
    > section

> <figure><img src="/.gitbook/assets/Delegated-Access-Release-Notes_image2.png" alt="" width="620"><figcaption></figcaption></figure>

  - > **Admin Operations Report :**

## Frequently Asked Questions (FAQs) 

### A. End User FAQs (Primary Account Holder & Secondary User)

#### 1\. General

Q: What is Delegated Access?

A: Delegated Access allows a primary retail account holder to grant
controlled access to their accounts to another trusted individual (the
secondary user), such as a family member, caretaker, or accountant. This
is intended to help the primary user manage their account-related tasks.

Q: Who can I grant delegated access to?

A: The member can grant access to any individual who can assist you with your
finances, including family members, friends, or professional service
providers.

Q: What channels can I use this feature on?

A: The Delegated Access feature is available on Online Banking (web) and
Mobile Banking.

#### 2\. For the Primary Account Holder

Q: What types of access can I grant?

A: The member can choose from three main access levels:

  - > View Access: The secondary user can only see account summaries,
    > balances, and transaction history. They cannot perform
    > transactions.

  - > Limited Access: The member can specifically select certain features and
    > transactions (like bill payments or mobile deposits) for the
    > secondary user to perform.

  - > Full Access: The secondary user can perform most account
    > activities, but key restricted actions remain (e.g., closing
    > accounts, changing default settings).

Q: Can I set limits on what the secondary user can transfer?

A: Yes. The member must set transfer limits for each account you grant access
to, including a per-transfer limit, a daily limit, and a monthly limit.

Q: How does the transfer limit work if I have multiple delegated users?

A: The transfer limit is cumulative across all secondary users. The
available limit for an individual secondary user at the time of transfer
is calculated by taking your set primary limit and subtracting all
transfers already made by all your delegated users.

Q: Can the secondary user open new accounts or change my settings?

A: No. Even with Full Access, the secondary user is explicitly
restricted from high-security actions, including: adding or removing
other delegated users, closing accounts, overdrawing accounts, opening
new accounts, or changing default account settings.

Q: How do I revoke or update a secondary user's access?

A: The member have full control and can update the limits or completely revoke
a secondary user's account access at any time through the Secondary User
management section.

#### 3\. For the Secondary User

Q: How do I get access to the account?

A: The primary user must send you an email invitation to enroll.

Q: How long is the invitation valid?

A: The enrollment invitation will expire after 24 hours. If it expires,
the primary user will need to re-send the invitation.

Q: Do I need to be a member of the Credit Union to be a secondary user?

A: No. If you are not a member, you will create your own new login
credentials during enrollment. If you are already a member, you can use
your existing credentials and switch between your personal profile and
the delegated access profile.

Q: What happens if I try to transfer more than the limit set by the
primary user?

A: If you exceed the set transfer limit, an approval request will be
automatically sent to the primary account holder. The transaction will
not complete without their approval.

Q: Can I grant access to someone else from the account I'm delegated to?

A: No. Secondary users are restricted from accessing the Delegated
Access feature itself and cannot create or manage other delegated users.

### 

### B. Admin User FAQs (Harmoney Console)

Q: Can Admin staff create, modify, or delete a delegated user?

A: No. Admin staff can view delegated members and their permissions in
the Harmoney Console, but they cannot directly create or delete a
delegated member.

Q: What visibility do Admin users have into delegated access activity?

A: Admin users have comprehensive visibility:

  - > The primary member's profile will display all delegated users,
    > their access level, added date, and last login.

  - > The delegated user's profile will show their specific access
    > level, added date, and last login.

  - > All activities performed by a delegated user are captured in the
    > activity logs and can be viewed via database scripts.

Q: What happens to a delegated user's limits if an Admin modifies the
primary user's limits?

A: If an Admin lowers the primary user's overall transfer limit, the
limits for the delegated access users will be automatically lowered as
well, ensuring that no delegated user can transact above the updated
master limit.
