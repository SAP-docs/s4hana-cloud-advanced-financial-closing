<!-- loio2105a6f5987b4e0bb641a1c3da7a6c9f -->

# How to Grant System-Wide Access

For all objects of a connected financial communication system, you want certain users to have no access, general read access, or general write access.



<a name="loio2105a6f5987b4e0bb641a1c3da7a6c9f__prereq_tvy_3mn_lkb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_Config`

    -   `AFC_UserRoles`


    For more information about role templates, see [How to Manage Static Role Templates](how-to-manage-static-role-templates-0cca34d.md).

-   You've had a look at the [overview table](overview-of-actions-and-means-to-grant-access-6f05d23.md) to make sure you're using the right means to grant access.

-   The users to whom you want to grant access have a role collection assigned that includes the required role templates. For more information, see [User Management](user-management-ae7fa30.md).




## Context

To grant system-wide access, you define **system-dependent user roles**.

> ### Restriction:  
> You **cannot** use this means of granting access for the *Manage Closing Task Lists* app.
> 
> Instead, grant general access or grant access to specific task list templates or task lists.
> 
> For more information about all access options, see [Overview of Actions and Means to Grant Access](overview-of-actions-and-means-to-grant-access-6f05d23.md).

The user roles you create and the access restrictions maintained in them take effect when you assign the respective users to the user role.



## Procedure

1.  Go to the *Configuration* app and choose *User Roles* from the table.

2.  Create a user role. Under *Type*, select *System-Dependent*.

3.  Select the communication system for which you want to define access.

4.  On the *General Information* tab, select one of the following access restrictions:

    <a name="loio2105a6f5987b4e0bb641a1c3da7a6c9f__d15e1198"/>General Restrictions


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
    
5.  Save.




<a name="loio2105a6f5987b4e0bb641a1c3da7a6c9f__postreq_rwn_gzl_bkb"/>

## Next Steps

For your newly created user role to take effect, you need to assign users for whom the defined access applies. For more information, see [How to Assign Users to User Roles](how-to-assign-users-to-user-roles-8729c2d.md).

