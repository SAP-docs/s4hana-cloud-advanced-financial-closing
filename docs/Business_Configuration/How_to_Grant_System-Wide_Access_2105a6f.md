<!-- loio2105a6f5987b4e0bb641a1c3da7a6c9f -->

# How to Grant System-Wide Access

For all objects of a connected financial communication system, you want certain users to have no access, general read access, or general write access.



<a name="loio2105a6f5987b4e0bb641a1c3da7a6c9f__prereq_tvy_3mn_lkb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes the role template `AFC_Config`.

    For more information about role templates, see [User Management](../User_Management_ae7fa30.md).

-   You've had a look at the [overview table](Overview_of_Actions_and_Means_to_Grant_Access_6f05d23.md) to make sure you're using the right means to grant access.

-   The users to whom you want to grant access have a role collection assigned that includes the required role templates. For more information, see [User Management](../User_Management_ae7fa30.md).




## Context

To grant system-wide access, you define **system-dependent user roles**.

> ### Restriction:  
> You **cannot** use this means of granting access for the *Define Closing Tasks* app.
> 
> Instead, grant general access or grant access to specific task list templates or task lists.
> 
> For more information about all access options, see [Overview of Actions and Means to Grant Access](Overview_of_Actions_and_Means_to_Grant_Access_6f05d23.md).

The user roles you create and the access restrictions maintained in them take effect when you assign the respective users to the user role.



## Procedure

1.  Go to the *Configuration* app and choose *User Roles* from the table.

2.  Create a user role. Under *Type*, select *System-Dependent*.

3.  Select the communication system for which you want to define access.

4.  On the *General Information* tab, select one of the following access restrictions:

    <a name="loio2105a6f5987b4e0bb641a1c3da7a6c9f__d15e1016"/>General Restrictions


    <table>
    <tr>
    <th>

    Restriction


    
    </th>
    <th>

    Description


    
    </th>
    </tr>
    <tr>
    <td>

    *Unrestricted Read Only*


    
    </td>
    <td>

    The user has read access to all data.

    The user doesn't have write access to any data at all.


    
    </td>
    </tr>
    <tr>
    <td>

    *Unrestricted Write*


    
    </td>
    <td>

    The user always has unrestricted write access to all data.


    
    </td>
    </tr>
    </table>
    
5.  Save.




<a name="loio2105a6f5987b4e0bb641a1c3da7a6c9f__postreq_rwn_gzl_bkb"/>

## Next Steps

For your newly created user role to take effect, you need to assign users for whom the defined access applies. For more information, see [How to Assign Users to User Roles](How_to_Assign_Users_to_User_Roles_8729c2d.md).
