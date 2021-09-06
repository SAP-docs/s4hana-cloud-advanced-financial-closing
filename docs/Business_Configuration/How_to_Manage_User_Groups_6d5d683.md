<!-- loio6d5d6838660749c8956c568641cac333 -->

# How to Manage User Groups

A user group represents a group of users who can be assigned to a particular set of closing tasks.



<a name="loio6d5d6838660749c8956c568641cac333__prereq_q22_x4m_3kb"/>

## Prerequisites

Your user must have a role collection assigned that includes the role template `AFC_Config`.

For more information about role templates, see [User Management](../User_Management_ae7fa30.md).



## Context

In the *Define Closing Tasks* app, task lists, tasks, or folders can be assigned to user groups instead of individual users. This setting has the following effects:

-   When you monitor and report on tasks using the *Financial Close Overview* and the *Closing Task Completion* apps, the names of the users assigned to tasks are not visible. Instead, you can only see the user group name that the user belongs to.

-   Notifications from the task list are sent to the users of the assigned user group.

-   In the *Process Closing Tasks* app, users assigned to a user group can see all tasks their group is assigned to as processing user group or as responsible user group.




## Procedure

1.  Go to the *Configuration* app and choose *User Groups* from the table.

2.  Under *User Groups*, create a user group and enter a description.

3.  Under *Users*, add the users who are in charge of processing or who are responsible for the same set of tasks.




<a name="loio6d5d6838660749c8956c568641cac333__result_dvs_xqt_3mb"/>

## Results

All users who belong to an owner group or to a responsible or processing user group of an object automatically have access to that object.

> ### Caution:  
> The substitutes of the users assigned to this user group don't inherit access to the objects.

