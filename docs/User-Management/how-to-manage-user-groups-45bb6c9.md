<!-- loio45bb6c91e94a4d3bafbf4b752c918c3e -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# How to Manage User Groups

A user group represents a group of users who can be assigned to a particular set of closing tasks.



<a name="loio45bb6c91e94a4d3bafbf4b752c918c3e__prereq_q22_x4m_3kb"/>

## Prerequisites

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




## Procedure

1.  Go to the *Configuration* app and choose *User Groups* from the table.


**Creating a single user group**

> ### Example:  
> The following quick demo shows how to create a user group performing the steps described below:
> 
> > ### Note:  
> > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
> > 
> > Interfaces may differ slightly depending on the version of your apps.

2.  To create a new user group, perform the following steps:

    1.  Go to the *User Groups* tab.

    2.  Choose *Create* in the table toolbar.

    3.  Under *General Information*, provide a name for the user group.

    4.  You can also enter a description.

    5.  Under *Users*, choose *Add* and select users you want to add.

    6.  Choose *Add* in the dialog footer.

    7.  Choose *Create* in the footer to create the user group.



**Creating Several User Groups at Once**

> ### Example:  
> The following quick demo shows how to create several user groups at once performing the steps described below:
> 
> > ### Note:  
> > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
> > 
> > Interfaces may differ slightly depending on the version of your apps.

3.  To create several new user groups at once, perform the following steps:

    1.  Go to the *User Groups* tab.

    2.  Download the template from the table toolbar.

    3.  In the CSV file, enter the user groups you want to create and for each group, enter one user that will be assigned to the group upon creation.

        > ### Note:  
        > Provide each user group only **once** and assign only one user to it. You can assign several users in one batch to the user group once it has been created.

    4.  Go back to the *Manage User Groups* app.

    5.  On the *User Groups* tab, choose *Upload User Groups* in the table toolbar.

    6.  Choose *Add* and select the CSV file you've prepared.

    7.  Choose *Upload* in the dialog footer.



**Uploading Several User-to-Group Assignments at Once**

> ### Example:  
> The following quick demo shows how to create several user-to-group assignments at once performing the steps described below:
> 
> > ### Note:  
> > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
> > 
> > Interfaces may differ slightly depending on the version of your apps.

4.  To assign several users in one batch to user groups, perform the following steps:

    > ### Note:  
    > The user groups and users affected have to exist in SAP Advanced Financial Closing before you can upload assignments.

    1.  Go to the *User-to-Group Assignments* tab.

    2.  Download the template from the table toolbar.

    3.  In the CSV file, enter the assignments you want to upload.

        > ### Note:  
        > On each line, you provide only one user group and only one user. However, you can mention each user group and user several times. This means that you can use this template to assign several users to several user groups in one batch.

    4.  Go back to the *Manage User Groups* app.

    5.  On the *User-to-Group Assignments* tab, choose *Upload Assignments* in the table toolbar.

    6.  Choose *Add* and select the CSV file you've prepared.

    7.  Choose *Upload* in the dialog footer.





<a name="loio45bb6c91e94a4d3bafbf4b752c918c3e__result_dvs_xqt_3mb"/>

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


