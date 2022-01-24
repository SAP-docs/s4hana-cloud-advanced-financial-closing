<!-- loioe6fa5d22299b4e62a2e7f6e79227d63c -->

# How to Grant Access According to Organizational Units

You want to grant users access to objects in specific company codes, controlling areas, or plants.



<a name="loioe6fa5d22299b4e62a2e7f6e79227d63c__prereq_k3g_42h_sjb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_Config`

    -   `AFC_UserRoles`


    For more information about role templates, see [How to Manage Static Role Templates](how-to-manage-static-role-templates-0cca34d.md).

-   An administrator has connected your financial communication systems. For more information, see [Connectivity](../Connectivity/connectivity-200deae.md).

-   Task lists are structured according to the organizational units to which you want to grant access.

-   You've had a look at the [overview table](overview-of-actions-and-means-to-grant-access-6f05d23.md) to make sure you're using the right means to grant access.

-   The users to whom you want to grant access have a role collection assigned that includes the required role templates. For more information, see [User Management](user-management-ae7fa30.md).




## Context

To grant access according to organizational units, you define **system-dependent user roles**. For these user roles, the organizational hierarchy is taken into account.

> ### Example:  
> When you grant a user access to a company code, that user also has access to all objects in subfolders, such as tasks belonging to a specific plant in this company code.

The user roles you create and the access restrictions maintained in them take effect when you assign the respective users.

> ### Restriction:  
> You **cannot** use this means of granting access for the *Define Closing Tasks* app.
> 
> Instead, grant general access or grant access to specific task list templates or task lists.
> 
> For more information about all access options, see [Overview of Actions and Means to Grant Access](overview-of-actions-and-means-to-grant-access-6f05d23.md).



## Procedure

1.  Go to the *Configuration* app and choose *User Roles* from the table.

2.  Create a user role. Under *Type*, select *System-Dependent*.

3.  Select the communication system to which you want to define access.

4.  On the *General Information* tab, select one of the following access restrictions:

    <a name="loioe6fa5d22299b4e62a2e7f6e79227d63c__d14e1049"/>Instance-Level Restrictions


    <table>
    <tr>
    <th valign="top">

    Restriction


    
    </th>
    <th valign="top">

    Description


    
    </th>
    <th valign="top">

    Instance restrictions must be maintained


    
    </th>
    </tr>
    <tr>
    <td valign="top">

    *Restricted Read Only*


    
    </td>
    <td valign="top">

    The user has read access only to the instances that you define.

    The user doesn't have write access to any data at all.


    
    </td>
    <td valign="top">

    For read access


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Restricted Read and Restricted Write*


    
    </td>
    <td valign="top">

    The user has read access only to the instances that you define.

    The user has write access only to the instances that you define.


    
    </td>
    <td valign="top">

    For read and for write access


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Unrestricted Read and Restricted Write*


    
    </td>
    <td valign="top">

    The user has read access to all data.

    The user has write access only to the instances that you define.


    
    </td>
    <td valign="top">

    For write access


    
    </td>
    </tr>
    </table>
    
5.  Define the access further under *Company Codes*, *Controlling Areas*, and/or *Plants* by adding the respective organizational units and the access to them \(read or write access\).

    > ### Note:  
    > The default value always restricts access to the most restricted that is possible with the attributes defined under *General Information*.

    > ### Caution:  
    > The organizational units you maintain in the role are independent of each other and always give access to the specific organizational unit and all underlying organizational units. This means that if you add a controlling area to this role, you can't restrict the access to specific company codes within this controlling area by additionally assigning these company codes. You can, however, add several company codes to one role, even without adding a controlling area or plant. In that case, you only grant access to the specific company codes and all their underlying organizational units.

    > ### Tip:  
    > You can change the access selection for multiple entries simultaneously. This applies to user roles for which you define read or write access for each entry individually. Select the entries for which you would like to set a new access level, choose *Change Access*, and then choose the new access level.

6.  Save.




<a name="loioe6fa5d22299b4e62a2e7f6e79227d63c__postreq_rwn_gzl_bkb"/>

## Next Steps

For your newly created user role to take effect, you need to assign users for whom the defined access restrictions apply. For more information, see [How to Assign Users to User Roles](how-to-assign-users-to-user-roles-8729c2d.md).

