<!-- loiob96fb86d38f34716bcb3c150c89d707d -->

# How to Grant Access in General

You want certain users to have either general read access or general write access.



<a name="loiob96fb86d38f34716bcb3c150c89d707d__prereq_swt_22h_sjb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_Config`

    -   `AFC_UserRoles`


    For more information about role templates, see [How to Manage Static Role Templates](How_to_Manage_Static_Role_Templates_0cca34d.md).

-   You've had a look at the [overview table](Overview_of_Actions_and_Means_to_Grant_Access_6f05d23.md) to make sure you're using the right means to grant access.

-   The users to whom you want to grant access have a role collection assigned that includes the required role templates. For more information, see [User Management](User_Management_ae7fa30.md).




## Context

To grant general access, you define **system-independent user roles**.

The user roles you create and the access restrictions maintained in them take effect when you assign the respective users to the user role.

> ### Restriction:  
> You **cannot** use this user role to grant access to the *Approve Closing Tasks* app.
> 
> Instead, grant access according to organizational units or assign the approver as the user responsible on the respective folder or task.
> 
> For more information about all access options, see [Overview of Actions and Means to Grant Access](Overview_of_Actions_and_Means_to_Grant_Access_6f05d23.md).



## Procedure

1.  Go to the *Configuration* app and choose *User Roles* from the table.

2.  Create a user role. Under *Type*, select *System-Independent*.

3.  On the *General Information* tab, select one of the following access restrictions:

    <a name="loiob96fb86d38f34716bcb3c150c89d707d__d7e1046"/>General Restrictions


    <table>
    <tr>
    <th valign="top">

    Restriction


    
    </th>
    <th valign="top">

    Description


    
    </th>
    </tr>
    <tr>
    <td valign="top">

    *Unrestricted Read Only*


    
    </td>
    <td valign="top">

    The user has read access to all data.

    The user doesn't have write access to any data at all.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Unrestricted Write*


    
    </td>
    <td valign="top">

    The user always has unrestricted write access to all data.


    
    </td>
    </tr>
    </table>
    
4.  Save.




<a name="loiob96fb86d38f34716bcb3c150c89d707d__postreq_rwn_gzl_bkb"/>

## Next Steps

For your newly created user role to take effect, you need to assign users for whom the defined access restriction applies. For more information, see [How to Assign Users to User Roles](How_to_Assign_Users_to_User_Roles_8729c2d.md).

