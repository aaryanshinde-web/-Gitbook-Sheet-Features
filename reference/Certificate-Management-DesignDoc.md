<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image4.png" alt="" width="620"><figcaption></figcaption></figure>

www.tyfone.com

**<span class="smallcaps">Certificate Management</span>**

Revision History

<table>
<thead>
<tr class="header">
<th>Date</th>
<th>Remarks</th>
<th><blockquote>
<p>Version</p>
</blockquote></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>14/11/2024</td>
<td>Initial draft</td>
<td><blockquote>
<p>1.0</p>
</blockquote></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

Contents

[Overview 4](#overview)

[**Documents 4**](#documents)

[Non-Goals or Out of Scope 5](#non-goals-or-out-of-scope)

[Configuration Details 5](#configuration-details)

[**Implementation 7**](#implementation)

> [1. Renew Certificate 8](#renew-certificate)
> 
> [2. Hold Balance Without Renewing 14](#hold-balance-without-renewing)
> 
> [3. Close at maturity 15](#close-at-maturity)

[OLB Specifications 17](#olb-specifications)

> [JIRA Tickets 17](#jira-tickets)
> 
> [Branching Details 17](#branching-details)

[**Sequence Diagram 17**](#sequence-diagram)

[Wireframes 20](#wireframes)

> [Folder Structure 30](#folder-structure)

[MB Specifications 31](#mb-specifications)

> [JIRA Tickets 31](#jira-tickets-1)
> 
> [Branching Details 31](#branching-details-1)
> 
> [Implementation 31](#implementation-1)
> 
> [Tools used to create diagrams 32](#tools-used-to-create-diagrams)
> 
> [Points to be discussed: 32](#points-to-be-discussed)

# Overview

This feature allows users to manage **INVESTMENT** accounts via the
"**Manage Certificate**" option on the Account Details page. The
investment account eligibility will be decided by customer(CU) and from
nFinia platform.

As part of the "Manage Certificate" feature users can do::

1\. **Renew Certificate:** Renew the certificate for the same or a new
term, with options to renew the full balance or withdraw a partial
amount.

2\. **Hold Balance:** Hold the certificate balance without renewal by
agreeing to terms.

3\. **Close at Maturity:** Transfer the balance to Share/Checking
account and close the certificate.

# Documents

  - > Migration docs for Certificate Management from Cubus to nFinia can
    > be found
    > [<span class="underline">here</span>](https://docs.google.com/document/d/1u64Lk2jIvEjeWA-SdhmehrYKIWDm-0cjfRbqHTJp0-8/edit?tab=t.0)

  - > OLB and MB Design / Mock-ups -
    > [<span class="underline">here</span>](https://www.figma.com/design/ZGW1btKeOdlDxe1trZuJpP/Cubus-One-nFinia-Migration-%7C-Certificate-Management?node-id=579-5913&node-type=frame&t=UqDVgqgGR8F51NHM-0)

# Non-Goals or Out of Scope

On Current release, we are only covering the Ultra Data(UD) core
implementation

Supported Core(s): **Ultra Data**

Out of Scope on Current release: **Correlation**

Below Maturity options are not supported in the OUCU implementation

1)  > **Cheque to Self** - Delivering the physical check to primary
    > address on maturity

2)  > **Cheque to third party** - Delivering the physical check to third
    > party address on maturity

# Configuration Details

Both MB and OLB will use the same configuration set.

<table>
<tbody>
<tr class="odd">
<td><p>{<br />
"MANAGE_CERTIFICATE_CONFIG": {<br />
"AVAILABLE_MATURITY_OPTIONS": [<br />
"REINVEST",<br />
"ROLLOVER_TO_ANOTHER",<br />
"CLOSE_AT_MATURITY"<br />
],<br />
"MANAGE_CERTIFICATE_OPTIONS": [<br />
{<br />
"key": "REINVEST",<br />
"slug": "reinvest",<br />
"value": {<br />
"key": "RENEWAL_OPTIONS",<br />
"header": "Renew Certificate",<br />
"flow": [<br />
{<br />
"key": "RENEWAL_OPTIONS",<br />
"title": "Renewal Option",<br />
"desc": "Renew Option description",<br />
"info": "Renew Option info text",<br />
"termKey": "reinvest",<br />
"widgetType": "selection or radiogroup",<br />
"widgetValues": {<br />
"REINVEST_EXISTING": "Renew the existing certificate",<br />
"ROLLOVER_TO_ANOTHER": "Reinvest or rollover to new certificate"<br />
}<br />
},<br />
{<br />
"key": "TERM_PERIOD",<br />
"title": "Term",<br />
"widgetType": "input/selection/radiogroup",<br />
"widgetValues": {<br />
"key": "availableReinvestTerms or rolloverTypeList"<br />
}<br />
},<br />
{<br />
"key": "REVIEW",<br />
"title": "Review"<br />
},<br />
{<br />
"key": "FINISH",<br />
"title": "finish",<br />
"redirectSlug": "/tabs/accounts"<br />
}<br />
]<br />
}<br />
},<br />
{<br />
"key": "ROLLOVER_TO_ANOTHER",<br />
"slug": "rollover_to_another",<br />
"value": {<br />
"accountConfigs": [<br />
{<br />
"key": "accountGroup",<br />
"values": [<br />
"CHECKING",<br />
"SAVINGS",<br />
"LOAN"<br />
]<br />
}<br />
],<br />
"memberConfigs": [<br />
{<br />
"key": "ownershipType",<br />
"values": [<br />
"primary"<br />
]<br />
}<br />
],<br />
"IS_CLOSE_CERTIFICATE_REASON_MANDATORY": false<br />
}<br />
},<br />
{<br />
"key": "CLOSE_AT_MATURITY",<br />
"slug": "close_at_maturity",<br />
"value": {</p>
<p>"accountConfigs": [<br />
{<br />
"key": "accountGroup",<br />
"values": [<br />
"CHECKING",<br />
"SAVINGS",<br />
"LOAN"<br />
]<br />
}<br />
],<br />
"memberConfigs": [<br />
{<br />
"key": "ownershipType",<br />
"values": [<br />
"primary"<br />
]<br />
}<br />
],<br />
"IS_CLOSE_CERTIFICATE_REASON_MANDATORY": false<br />
}<br />
}<br />
]<br />
}<br />
}</p></td>
</tr>
</tbody>
</table>

# Implementation

It covers the implementation of Manage Certificate functionalities,
including Renew Certificate, Hold Balance Without Renewing, and Close at
Maturity. Below are the eligibility criteria to qualify for a Management
Certificate based on customer configuration.

For example, in the UD core system, Manage Certificate eligibility is
determined based on the **ProductID** type **"I"** which stands for
INVESTMENT accounts.

Mandatorily the need to check feature is enabled or not under system
configurations under **MANAGE\_CERTIFICATE\_OPTIONS** with key **slug**
and similar to **Hold balance** and **Close On Maturity**.

Below are the available maturity options currently supported by

**UDCore:**

"availableMaturityOptions":"REINVEST,TRANSFER\_TO\_ACCOUNT,ROLLOVER\_TO\_ANOTHER\_I\_TYPE"

## Renew Certificate

Supported Core(s): Ultra Data(UD) and Correlation

Renew the certificate for the same or a new term, with options to renew
the full balance or withdraw a partial amount.

Check the eligibility criteria based on API response data received from
MCB or by module configuration configurations. Validate the Key
availableMaturityOptions is for REINVEST value present or not and also
check the system configuration to decide whether to listing is required
under management certificate or not by referring system config key
AVAILABLE\_MATURITY\_OPTIONS and value is REINVEST to validate whether
to display on UI or not. If both the conditions are satisfied display
the Reinvest option on UI under manage certificate

This feature can be accessed through the account details screen by
clicking on **Manage Certificate** link/button or using Quick links.

**UD Core:** Validate the **productID** value is **"I"** for check
eligibility for **Investment** accounts

Refer UD Core section for Screens:
[<span class="underline">https://www.figma.com/design/ZGW1btKeOdlDxe1trZuJpP/Cubus-One-nFinia-Migration-%7C-Certificate-Management?node-id=581-14299\&node-type=frame\&t=mw51Wd9JdhXbBG9S-0</span>](https://www.figma.com/design/ZGW1btKeOdlDxe1trZuJpP/Cubus-One-nFinia-Migration-%7C-Certificate-Management?node-id=581-14299&node-type=frame&t=mw51Wd9JdhXbBG9S-0)

**Correlation:** Yet To Decide

Use the **MANAGE\_CERTIFICATE\_OPTIONS** to decide the flow on the
REINVEST step to complete the renewal of the certificate.

**Step-1: Renewal Options**

On Step-1, below Renewal Options will be displayed based on the
configurations on clicking on Review option from Manage certificate.

Based on the key \`currentMaturityOption\`, the radio button will be
selected by default. If the current maturity option is available on the
provided config options. It will not auto select any radio button by
default. The user has to select the option maturity option and otherwise
display an inline error message to select the option.

Currently it supports the options below.

**Option 1: Reinvest:**

Reinvest the full amount, including any returns, into the same product
for another term.

**Option 2: Rollover**:

Users choose to withdraw the interest while continuing the investment
with only the principal.

**Option 3: Renew with Partial Withdrawal**:

Users specify how much they want to withdraw and reinvest the remaining
amount for another term.

**Ultra Data:**

In current **Ultra Data** implementation, it supports two renewal
options "**Renew"** existing and "**Reinvest** or **Rollover".**

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image21.png" alt="" width="620"><figcaption></figcaption></figure>

If the user selects Reinvest/Rollover, display a dropdown with available
certificate options from the API response key rolloverTypeList. On
selecting the rollover option from the list continue to the next step.

When user reinvesting, it should populate with Withdrawal amount TEXT
field and eligible Transfer account should be selected. Inline
validation should be added if user is not selected the required fields

While reinvesting/rollover the certificate, need to add validations for
the minimum and maximum values of the Withdrawal Amount and eligible
source account to be selected.

The eligibility of Transfer Funds account filter is based on the Member
and Account configurations.

<table>
<tbody>
<tr class="odd">
<td>{<br />
"accountConfigs": [<br />
{<br />
"key": "accountGroup",<br />
"values": [<br />
"CHECKING",<br />
"SAVINGS",<br />
"LOAN"<br />
]<br />
}<br />
],<br />
"memberConfigs": [<br />
{<br />
"key": "ownershipType",<br />
"values": [<br />
"primary"<br />
]<br />
}<br />
]<br />
}</td>
</tr>
</tbody>
</table>

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image19.png" alt="" width="620"><figcaption></figcaption></figure>

RollOver: TBD

**Step-2: Term**

On step-2, Users can select the **Term** for the Renewal option based on
the key **availableReinvestTerms** and the widget will be decided based
on the configuration key **widgetType.**

**Correlation:**

For Correlation, the rollover certificate term will be displayed in
**SELECTION** based on the response received. Do not select any default
certificate term and add inline validation if user does not provide the
input.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image22.png" alt="" width="620"><figcaption></figcaption></figure>

On selecting the certificate term and click on the Next button, display
the summery user selected on this screen

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image23.png" alt="" width="620"><figcaption></figcaption></figure>

**UltraData:**

The Term limits in Days and the input type is **TEXT FIELD.** The limits
of the input field will be validated from **availableReinvestTerms**
keys **minTerm** and **maxTerm.**

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image24.png" alt="" width="480"><figcaption></figcaption></figure>

**Step-3: Review**

On the summary screen display the renewal/rollover information selected
by the user. On clicking on the **Back** button the user should navigate
back to the previous screen by retaining entered data. On click on Renew
proceed with submitting the data and display the status on the next
step.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image18.png" alt="" width="620"><figcaption></figcaption></figure>

**Step-4: Finish (Success/Failure)**

On Step-4, display the renewal of certificate status and include
customer support. On recoverable errors provide and retry option on UI
to resubmit Renew request.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image20.png" alt="" width="620"><figcaption></figcaption></figure>

## Hold Balance Without Renewing

Supported Core(s): Correlation

Holding the balance means that the certificate account will not be
renewed at the end of its term. The balance will remain in the account
without accruing any additional interest post maturity date. Balance
will remain accessible and can be held in this state indefinitely.

Future Options:

  - > Transfer the balance to another savings or investment account.

  - > Renew the certificate at a later date based on the prevailing
    > terms and interest rates.

  - > Withdraw the balance without any penalties.

Users have to accept the Terms and conditions to submit the Holds for
Balance without Renewing and accepting TnC they can continue to complete
the holds request.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image27.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image25.png" alt="" width="620"><figcaption></figcaption></figure>

## Close at maturity

Supported Core(s): Ultra Data(UD) and Correlation

When a user selects close at maturity, the end user has to select a
transfer account to deposit the certificate account closure. The reason
selection is an optional field based on configuration and the reasons
will be received from API, if user selected OTHER then need to populate
with input field which takes a string input and is included in
certificate closure request.

Reasons will be maintained on Configs and will be submitted to nFInia
not Ultra Data. This data used to track on Harmony

The user has to accept the **Terms and conditions** before closing the
certificate account. The Terms and conditions can be fetched using
static content request or as fallback can be maintained on local
strings.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image10.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image26.png" alt="" width="620"><figcaption></figcaption></figure>

# <span class="smallcaps">OLB Specifications</span>

## **JIRA Tickets** 

  - > Epic:
    > [<span class="underline">https://tyfone.atlassian.net/browse/NFIN-31630</span>](https://tyfone.atlassian.net/browse/NFIN-31630)

  - > Design:
    > [<span class="underline">https://tyfone.atlassian.net/browse/NFIN-31888</span>](https://tyfone.atlassian.net/browse/NFIN-31888)

## **Branching Details**

OLB URL:
[<span class="underline">https://feature-certificate-management.tyfone.com</span>](https://feature-certificate-management.tyfone.com)

MCB BASE URL: **bankingapiserver\_certificate**

Source for the feature branch:
[<span class="underline">10.34-ux2.5-dev</span>](https://github.com/TyfoneInc/nfiniaolb/tree/10.34-ux2.5-dev)  
Feature Branch: **feature-certificate-management-NFIN-31630**

# Sequence Diagram

1.  > **Renew Certificate:**

<!-- end list -->

  - > Renew the existing certificate
    > balance:<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image8.png" alt="" width="480"><figcaption></figcaption></figure>

  - > Renew by withdrawing partial amount from balance:

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image5.png" alt="" width="480"><figcaption></figcaption></figure>

2.  > **Hold Balance without Renewing:**

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image3.png" alt="" width="620"><figcaption></figcaption></figure>

3.  > **Close at maturity:**

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image1.png" alt="" width="620"><figcaption></figcaption></figure>

# Wireframes

1.  > **Account Details Page:**
    
    1.  > "**Manage Certificate**" Option on Account Details Page.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image2.png" alt="" width="620"><figcaption></figcaption></figure>

2.  > **Manage Certificate Page:**
    
    1.  > Available Certificate options:

> <figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image17.png" alt="" width="620"><figcaption></figcaption></figure>

3.  > **Renew Certificate Page:** The first option of the radio button
    > will be selected by default.
    
    1.  > Renew the existing certificate:

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image6.png" alt="" width="480"><figcaption></figcaption></figure>

2.  > Term Page: User has to select the **Term** after selecting the
    > **Renewal option**

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image13.png" alt="" width="480"><figcaption></figcaption></figure>

3.  > Review Page: After selecting the **term** the user will redirected
    > to the **review** page

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image15.png" alt="" width="480"><figcaption></figcaption></figure>

4.  > Success Page: After submitting the request for **renewal** the
    > **success** screen will be displayed.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image16.png" alt="" width="620"><figcaption></figcaption></figure>

5.  > Reinvest or rollover to new certificate: On selecting this option
    > the user will have to select the option for **Rollover**
    > Certificate.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image12.png" alt="" width="480"><figcaption></figcaption></figure>

4.  > Hold Balance Without Renewing (Corelation Core):
    
    1.  > Here the user will be displayed a static content along with
        > the checkbox for agreeing TnC.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image7.png" alt="" width="620"><figcaption></figcaption></figure>

2.  > Success Screen: After the successful completion of request the
    > success screen will be displayed.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image11.png" alt="" width="620"><figcaption></figcaption></figure>

5.  > Close at Maturity:
    
    1.  > Here the user will be asked to select the transfer to accounts
        > and select the reason along with a checkbox for agreeing the
        > TnC.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image14.png" alt="" width="620"><figcaption></figcaption></figure>

2.  > Success Screen: After successful completion of the closure request
    > the success screen will be displayed.

<figure><img src="/.gitbook/assets/Certificate-Management-DesignDoc_image9.png" alt="" width="620"><figcaption></figcaption></figure>

## 

## **Folder Structure**

Controller:

1.  > app\\Http\\Controllers\\Web\\WebCertificateManagementController.php

Service:

1.  > app\\Services\\Impl\\OLB\\CertificateManagementService.php

Model:

1.  > app\\Models\\CertificateManagement.php

Blade File**:**

Folder:
resources\\views\\themes\\theme1\\product\\web\\certificate\_management\\

1.  > certificate\_management.blade.php

2.  > certificate\_renew.blade.php

3.  > certificate\_hold\_bal\_without\_renewing.blade.php

4.  > certificate\_close.blade.php

5.  > certificate\_finish.blade.php

JavaScript File:

Folder: resources\\assets\\themes\\theme1\\olb\\web\\js\\

1.  > certificate\_management\\

# <span class="smallcaps">MB Specifications</span>

## **JIRA Tickets** 

  - > Epic:
    > [<span class="underline">https://tyfone.atlassian.net/browse/NFIN-31630</span>](https://tyfone.atlassian.net/browse/NFIN-31630)

  - > Design:
    > [<span class="underline">https://tyfone.atlassian.net/browse/NFIN-31887</span>](https://tyfone.atlassian.net/browse/NFIN-31887)

## **Branching Details**

  - > Feature Branch:
    > **feature/NFIN-31630/10.38.certificate-management**

## **Implementation**

Manage Certificate should be enabled when the module is enabled and
renew and close any maturity features will be enabled based on API
response and system/local configurations.

Below are the folder created for Manage certificate feature

Under src -\> pages, create new folder **manage-certificate** and create
below folders and angular modules.

  - > Manage-certificate.module
    
      - > Renew certificate module
    
      - > Reinvest or Rollover module
    
      - > Close at Maturity module

  - > Each module will have respective **html, scss**, **page.ts** and
    > **spec** files under each module.

Below is the MB screen Figma link for both Correlation and Ultra data
core.

[<span class="underline">Figma</span>](https://www.figma.com/design/ZGW1btKeOdlDxe1trZuJpP/Cubus-One-nFinia-Migration-%7C-Certificate-Management?node-id=552-419&node-type=frame&t=9zQNzOgnw6nRVDJV-0)

## **Tools used to create diagrams**

[<span class="underline">https://www.websequencediagrams.com/</span>](https://www.websequencediagrams.com/)  
[<span class="underline">https://app.creately.com/d/start/dashboard</span>](https://app.creately.com/d/start/dashboard)

## **Points to be discussed:**

  - > Need to pre-populate principle amount by default for Rollover of
    > certificate.
