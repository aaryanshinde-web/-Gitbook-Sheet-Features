<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image1.png" alt="" width="620"><figcaption></figcaption></figure>

www.tyfone.com

**<span class="smallcaps">Custom Account Grouping</span>**

Release Notes

# 

# **<span class="smallcaps">Overview</span>**

Users can create, edit and delete custom groups and sections as well as
move individual accounts to any section or group of their choosing. This
Allows users to define and manage their own groupings of accounts within
the online banking platform. This feature will empower users to organize
their financial information in a way that aligns with their personal
preferences and needs. Users should have the ability to:

1.  > **Create Custom Groups:** Define new, user-named groups to
    > categorize accounts (e.g., "Family Expenses," "Investment
    > Portfolio," "Business Accounts").

2.  > **Edit Custom Groups:** Modify the names of existing custom
    > groups.

3.  > **Delete Custom Groups:** Remove custom groups when they are no
    > longer needed. Deleting a group should not delete the accounts
    > within it; instead, accounts will likely revert to a default
    > "Ungrouped" or similar state.

4.  > **Create Sections within Groups:** Further subdivide custom groups
    > into logical sections. For instance, within a "Family Expenses"
    > group, users might create sections for "Groceries," "Utilities,"
    > and "Entertainment."

5.  > **Edit Sections:** Change the names of sections within a group.

6.  > **Delete Sections:** Remove sections from a group. Again, accounts
    > within a deleted section should be handled appropriately,
    > potentially moving to the parent group's root level.

7.  > **Move Individual Accounts:** Transfer any individual account
    > (checking, savings, credit card, loan, etc.) to any custom group
    > or section. This drag-and-drop or similar intuitive mechanism will
    > provide flexibility in how users organize their finances.

This custom account grouping functionality aims to enhance user
experience by providing a more personalized and organized view of their
financial accounts. It will allow users to quickly locate specific
accounts and gain a better understanding of their overall financial
situation based on their self-defined categories.

**Release: 10.44**

# **<span class="smallcaps">User Journey</span>**

1.  > Accessing the Manage Group Page:
    
    1.  > The Manage Group feature can be accessed from the "Accounts /
        > Accounts overview" Page. The user has an option to select the
        > "Account Group". The account group dropdown will have an
        > option to select "Manage Group", along with all the custom
        > groups created.

<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image2.png" alt="" width="620"><figcaption></figcaption></figure>

2.  Manage Custom Group Page: The user will be redirected to the Edit
    Custom Group Page. Here the group name which is selected by default
    on the accounts page will be rendered here. For eg: If the user has
    selected a group, "Group A" as their by default group. When clicked
    on "Manage Group" from the accounts dropdown will render the "Group
    A" on Custom Account Grouping Page. The selected group name will be
    highlighted on the left panel.

<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image8.png" alt="" width="620"><figcaption></figcaption></figure>

<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image3.png" alt="" width="620"><figcaption></figcaption></figure>

  - > This page is divided into two sections. The left section, where
    > the user is able to see system group information and user created
    > groups along with a button to add a new custom group.

  - > By clicking on "New custom group" (the button on the left panel)
    > users will be able to add a new custom group. To finish setting up
    > the custom group user has to enter the Group Name, Section Name
    > and Add at least one account to the section. On clicking the "Add
    > Section" button a new section will be created. Similar behavior is
    > for the "Add Accounts" button as well. On Clicking the Cancel
    > button the user will be redirected to the Accounts Page. On Click
    > of Save button the request will be submitted and the newly created
    > Group will be displayed on the Accounts Page.

  - > The custom account grouping page features two main sections. On
    > the left, users can view system-defined groups and their own
    > created groups, along with an option to create a new custom group.
    > The right section enables users to add new groups and modify
    > existing ones.

The user has entered the Group Name and Section Name.The user has
provided a group name and a section name.

<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image7.png" alt="" width="620"><figcaption></figcaption></figure>

  - > The user has added the accounts into the section. Once an account
    > has been added, it will not be visible in subsequent dropdown as
    > the account is previously added.

  - > The dropdown list should be updated on adding or removing the
    > accounts from the section.

  - > After an account is added to a section, it will be disabled in
    > subsequent dropdown lists. The dropdown list will dynamically
    > update whenever accounts are added or removed from the section to
    > reflect the current selection. Here when an account is selected
    > the account gets disabled. In the subsequent dropdown that account
    > cannot be selected.

<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image6.png" alt="" width="620"><figcaption></figcaption></figure>

The below screenshot shows the system group, the user is not allowed to
Edit/Delete/Rename this group.

<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image4.png" alt="" width="620"><figcaption></figcaption></figure>

We have also introduced the Expand / Collapse View for the Sections to
avoid long scrolling of the page if multiple sections or multiple
accounts are added. On clicking the collapse icon, The value on the
Section Name will be rendered and on clicking on Expand the Section will
be expanded.

<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image5.png" alt="" width="620"><figcaption></figcaption></figure>

We also have the option to sort the groups. On clicking the "Manage"
link, the page below will be rendered where the user can have the sort
options similar to what we have for accounts and sections. On clicking
the Save button the group order will be updated and the new order will
be applicable on Account Page, and Custom Account Grouping page.

<figure><img src="/.gitbook/assets/Custom-Account-Grouping-Release-Notes_image9.png" alt="" width="620"><figcaption></figcaption></figure>
