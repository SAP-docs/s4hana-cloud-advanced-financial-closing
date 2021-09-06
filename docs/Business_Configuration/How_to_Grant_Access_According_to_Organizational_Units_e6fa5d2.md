<!-- loioe6fa5d22299b4e62a2e7f6e79227d63c -->

# How to Grant Access According to Organizational Units

You want to grant users access to objects in specific company codes, controlling areas, or plants.



<a name="loioe6fa5d22299b4e62a2e7f6e79227d63c__prereq_k3g_42h_sjb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes the role template `AFC_Config`.

    For more information about role templates, see [User Management](../User_Management_ae7fa30.md).

-   An administrator has connected your financial communication systems. For more information, see [Connectivity](../Connectivity/Connectivity_200deae.md).

-   Task lists are structured according to the organizational units to which you want to grant access.

-   You've had a look at the [overview table](Overview_of_Actions_and_Means_to_Grant_Access_6f05d23.md) to make sure you're using the right means to grant access.

-   The users to whom you want to grant access have a role collection assigned that includes the required role templates. For more information, see [User Management](../User_Management_ae7fa30.md).




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
> For more information about all access options, see [Overview of Actions and Means to Grant Access](Overview_of_Actions_and_Means_to_Grant_Access_6f05d23.md).



## Procedure

1.  Go to the *Configuration* app and choose *User Roles* from the table.

2.  Create a user role. Under *Type*, select *System-Dependent*.

3.  Select the communication system to which you want to define access.

4.  On the *General Information* tab, select one of the following access restrictions:

    <a name="loioe6fa5d22299b4e62a2e7f6e79227d63c__d15e922"/>Instance-Level Restrictions


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

    *Restricted Read Only*


    
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

    *Restricted Read and Restricted Write*


    
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
    
5.  Define the access further under *Company Codes*, *Controlling Areas*, and/or *Plants* by adding the respective organizational units and the access to them \(read or write access\).

    > ### Note:  
    > The default value always restricts access to the most restricted that is possible with the attributes defined under *General Information*.

    > ### Tip:  
    > You can change the access selection for multiple entries simultaneously. This applies to user roles for which you define read or write access for each entry individually. Select the entries for which you would like to set a new access level, choose *Change Access*, and then choose the new access level.

6.  Save.




<a name="loioe6fa5d22299b4e62a2e7f6e79227d63c__postreq_rwn_gzl_bkb"/>

## Next Steps

For your newly created user role to take effect, you need to assign users for whom the defined access restrictions apply. For more information, see [How to Assign Users to User Roles](How_to_Assign_Users_to_User_Roles_8729c2d.md).

