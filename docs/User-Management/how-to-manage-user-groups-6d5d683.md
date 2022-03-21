<!-- loio6d5d6838660749c8956c568641cac333 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# How to Manage User Groups

A user group represents a group of users who can be assigned to a particular set of closing tasks.



<a name="loio6d5d6838660749c8956c568641cac333__prereq_q22_x4m_3kb"/>

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

2.  Under *User Groups*, create a user group and enter a description.

3.  Under *Users*, add the users who are in charge of processing or who are responsible for the same set of tasks.

4.  Save.




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


