<!-- loio0f2fcd871f154e969e1234d52e0ea7f8 -->

# How to Grant Access According to Specific Objects

You want to grant users access to specific task list templates, tasks lists, and tasks.



<a name="loio0f2fcd871f154e969e1234d52e0ea7f8__prereq_swt_22h_sjb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes the role template `AFC_Config`.

    For more information about role templates, see [How to Manage Static Role Templates](How_to_Manage_Static_Role_Templates_0cca34d.md).

-   You've had a look at the [overview table](Overview_of_Actions_and_Means_to_Grant_Access_6f05d23.md) to make sure you're using the right means to grant access.

-   The users to whom you want to grant access have a role collection assigned that includes the required role templates. For more information, see [User Management](User_Management_ae7fa30.md).

-   You've decided on the access you want to grant and which authorization groups you need.




## Context

To grant access according to objects, you define **system-independent user roles**. Access to specific task list templates, task lists, and tasks is defined indirectly via **authorization groups**.

> ### Restriction:  
> You can use this type of user role to grant access to task list templates and task lists in the *Define Closing Tasks* app. While read access can be restricted to specific objects within the template or task list, write access can be granted only for the whole template, for the task list, or not at all.

> ### Restriction:  
> You **cannot** use this user role to grant access to the *Approve Closing Tasks* app.
> 
> Instead, grant access according to organizational units or assign the approver as the user responsible on the respective folder or task.
> 
> For more information about all access options, see [Overview of Actions and Means to Grant Access](Overview_of_Actions_and_Means_to_Grant_Access_6f05d23.md).

> ### Tip:  
> If financial close is done centrally for all your legal entities, you can, for example, set up one authorization group for each subledger. This enables you to provide authorizations for closing activities in accordance with the authorizations for subledger accounting, such as:
> 
> -   Accounts Receivable \(A/R\)
> 
> -   Accounts Payable \(A/P\)
> 
> -   Asset Accounting
> 
> -   Overhead Accounting
> 
> -   Production Accounting
> 
> -   Inventory Accounting
> 
> -   Sales Accounting
> 
> -   Taxes
> 
> -   General Ledger

The user roles you create and the restrictions maintained in them take effect when you assign the respective users to the user role and the defined authorization groups to the relevant objects.



## Procedure

1.  Go to the *Configuration* app and choose *Authorization Groups*

2.  Create the authorization groups you want to assign to your user role. Decide which objects the authorization group applies to:

    -   Select *Task List Template / Task List* to grant access to task list templates and task lists in the *Define Closing Tasks* app.

    -   Select *Task* to grant access to tasks in any of the apps to which the respective users have access with their static role.

    > ### Tip:  
    > Provide a meaningful description so that other users who want to make use of the authorization group can apply it correctly.

3.  Go to the *Configuration* app and choose *User Roles* from the table.

4.  Create a user role. Under *Type*, select *System-Independent*.

5.  On the *General Information* tab, select one of the access restrictions listed below.

    <a name="loio0f2fcd871f154e969e1234d52e0ea7f8__d15e928"/>Instance-Level Restrictions


    <table>
    <tr>
    <th>

    Restriction


    
    </th>
    <th>

    Description


    
    </th>
    <th>

    Instance restrictions must be maintained


    
    </th>
    </tr>
    <tr>
    <td>

    **


    
    </td>
    <td>

    The user has read access only to the instances that you define.

    The user doesn't have write access to any data at all.


    
    </td>
    <td>

    For read access


    
    </td>
    </tr>
    <tr>
    <td>

    *Restricted Read and Restricted WriteRestricted Read Only*


    
    </td>
    <td>

    The user has read access only to the instances that you define.

    The user has write access only to the instances that you define.


    
    </td>
    <td>

    For read and for write access


    
    </td>
    </tr>
    <tr>
    <td>

    *Unrestricted Read and Restricted Write*


    
    </td>
    <td>

    The user has read access to all data.

    The user has write access only to the instances that you define.


    
    </td>
    <td>

    For write access


    
    </td>
    </tr>
    </table>
    
6.  Define the access further under *Task List Templates*, *Task Lists*, and/or *Tasks* by adding the authorization groups and the access to them \(read or write access\).

    > ### Note:  
    > The default value always restricts access to the most restricted that is possible with the attributes defined under *General Information*.

    > ### Note:  
    > A user who has the role template `AFC_Process` assigned always has read access to all task lists in the *Process Closing Tasks* app.

    > ### Tip:  
    > You can change the access selection for multiple entries simultaneously. This applies to user roles for which you define read or write access for each entry individually. Select the entries for which you would like to set a new access level, choose *Change Access*, and then choose the new access level.

7.  Save.




<a name="loio0f2fcd871f154e969e1234d52e0ea7f8__postreq_rwn_gzl_bkb"/>

## Next Steps

The following tasks need to be completed for your newly created user role to take effect.

-   Assign users to whom the defined access restrictions apply. For more information, see [How to Assign Users to User Roles](How_to_Assign_Users_to_User_Roles_8729c2d.md).

-   In the *Define Closing Tasks* app, assign authorization groups to task list templates, task lists, or tasks. Each task list template, task list, or task can have only one authorization group assigned.


