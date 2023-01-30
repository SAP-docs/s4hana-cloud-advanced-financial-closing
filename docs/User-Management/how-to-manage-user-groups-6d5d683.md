<!-- loio6d5d6838660749c8956c568641cac333 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# How to Manage User Groups

A user group represents a group of users who can be assigned to a particular set of closing tasks.



<a name="loio6d5d6838660749c8956c568641cac333__prereq_q22_x4m_3kb"/>

## Prerequisites

> ### Caution:  
> This part of the documentation refers to the **old authorization concept**. New assignments to roles of this concept will no longer be possible as of February 2023. Existing assignments remain valid until May.
> 
> Therefore, please switch to the new authorization concept. Make sure that you remove existing user-to-role assignments from old roles and use assignments to scoped user roles instead. When switching to the new concept, pay special attention to direct assignments, since authorizations granted for compatibility reasons will be removed in May.
> 
> Please find information about the new authorization concept in this guide under [User Access Management \(New Authorization Concept\)](user-access-management-new-authorization-concept-d974847.md). This section also covers the new authorization logic of direct user assignments under [Direct User Assignment](direct-user-assignment-f96b217.md).

Your user must have a role collection assigned that includes one of the following role templates:

-   `AFC_Config`

-   `AFC_UserAdmin`

-   `AFC_UserGroupsApp`


For more information about role templates, see [How to Manage Static Role Templates](how-to-manage-static-role-templates-0cca34d.md).



## Context

In the *Manage Closing Task Lists* app, task lists, tasks, or folders can be assigned to user groups instead of individual users. This setting has the following effects:

-   When you monitor and report on tasks using the *Financial Close Overview* and the *Closing Task Completion* apps, the names of the users assigned to tasks are not visible. Instead, you can only see the user group name that the user belongs to.

-   Notifications from the task list are sent to the users of the assigned user group.

-   In the *Process Closing Tasks* app, users assigned to a user group can see all tasks their group is assigned to as processing user group or as responsible user group.




<a name="loio6d5d6838660749c8956c568641cac333__steps_ojx_msk_ctb"/>

## Procedure

1.  Go to the *Configuration* app and choose *User Groups* from the table.

2.  **Creating a single user group**

    > ### Example:  
    > The following quick demo shows how to create a user group performing the steps described below:
    > 
    > > ### Note:  
    > > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
    > > 
    > > Interfaces may differ slightly depending on the version of your apps.

3.  To create a new user group, perform the following steps:

    1.  On the *User Groups* tab, create a user group and enter a description.

    2.  Under *Users*, add the users who are in charge of processing or who are responsible for the same set of tasks.

    3.  Choose *Create* to create the user group.


4.  **Creating Several User Groups at Once**

    > ### Example:  
    > The following quick demo shows how to create several user groups at once performing the steps described below:
    > 
    > > ### Note:  
    > > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
    > > 
    > > Interfaces may differ slightly depending on the version of your apps.

5.  To create several new user groups at once, perform the following steps:

    1.  On the *User Groups* tab, download the template.

    2.  In the CSV file, enter the user groups you want to create and for each group, enter one user that will be assigned to the group upon creation.

        > ### Note:  
        > Provide each user group only **once** and assign only one user to it. You can assign several users in one batch to the user group once it has been created.

    3.  Go back to the *Manage User Groups* app.

    4.  On the *User Groups* tab, choose *Upload User Groups*.

    5.  Select the CSV file you've prepared and choose *Upload*.


6.  **Uploading Several User-to-Group Assignments at Once**

    > ### Example:  
    > The following quick demo shows how to create several user-to-group assignments at once performing the steps described below:
    > 
    > > ### Note:  
    > > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
    > > 
    > > Interfaces may differ slightly depending on the version of your apps.

7.  To assign several users in one batch to user groups, perform the following steps:

    > ### Note:  
    > The user groups and users affected have to exist in advanced financial closing before you can upload assignments.

    1.  On the *User-to-Group Assignments* tab, download the template.

    2.  In the CSV file, enter the assignments you want to upload.

        > ### Note:  
        > On each line, you provide only one user group and only one user. However, you can mention each user group and user several times. This means that you can use this template to assign several users to several user groups in one batch.

    3.  Go back to the *Manage User Groups* app.

    4.  On the *User-to-Group Assignments* tab, choose *Upload Assignments*.

    5.  Select the CSV file you've prepared and choose *Upload*.





<a name="loio6d5d6838660749c8956c568641cac333__result_dvs_xqt_3mb"/>

## Results

-   All users who belong to an owner group or to a responsible or processing user group of an object automatically have access to that object.

    > ### Caution:  
    > The substitutes of the users assigned to this user group don't inherit access to the objects.

-   You can get an overview of the assignments of users to user groups on the *User-to-Group Assignments* tab.

    > ### Tip:  
    > Using column-specific filters, you can enter specific criteria for your search.
    > 
    > Additionally, you can group entries by specific criteria using the *Group* option that you can find in the settings for this table.

    To export the overview, you can use the *Export to Spreadsheet* icon <span class="SAP-icons"></span> on the table toolbar.


