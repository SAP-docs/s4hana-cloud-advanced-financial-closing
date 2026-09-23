<!-- loio1727010ff7724f56bbcd0e71d0e1f759 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# How to Grant Access to Specific Objects

Grant access to task models located in specific communication systems.



<a name="loio1727010ff7724f56bbcd0e71d0e1f759__prereq_hx5_kzj_qrb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates or role template combinations:

    -   `AFC_Config`

    -   `AFC_UserRoles`

    -   `AFC_UserRolesSingleApp`


    For more information about role templates, see [How to Manage Static Role Templates](how-to-manage-static-role-templates-0cca34d.md) and [Static Roles for SAP Advanced Financial Closing](static-roles-for-sap-advanced-financial-closing-b92a241.md).

-   You've familiarized yourself with the information under [Task Model Management Scope](task-model-management-scope-c951f94.md) to ensure that you're using the right means to grant access.




## Context

You can grant access that is restricted to task models in specific communication systems.



## Procedure

1.  Open the *Configuration* app.

    The next screen lists all the configuration apps you're allowed to access.

2.  Choose *User Roles* from the list.

    This brings you to the *Manage User Roles* app.

3.  Go to the *Scoped User Roles* tab.

4.  Choose *Create* in the table toolbar.

5.  Provide the following information:

    1.  Under *Name*, freely define a name for your user role.

    2.  Under *Description*, you can add a description for your user role.

    3.  Under *Scope*, select *Task Model Management*.

    4.  *Type* \(read-only\):

        For scope *Task Model Management*, this is always *System-Independent*.

    5.  Under *Restriction*, select *Restricted*.


6.  Choose *Create* in the dialog footer. The user role is created and opened right away.

7.  **Optional:** If you want to allow user-to-role assignments to be managed through the SCIM API, select the *Exposed via SCIM Group* checkbox in the *General Information* section.

    1.  Confirm that you understand the warning displayed and choose *OK*.


    For more information about user access management through the SCIM API, see [How to Manage User Access Using the SCIM API Provided](../Integration-Capabilities/how-to-manage-user-access-using-the-scim-api-provided-49376ed.md).

8.  Under *Authorizations*, choose *Add* and select an authorization you want to add.

    > ### Note:  
    > *Read* authorization is the minimum authorization required for all user roles. Accordingly, it is added to each user role automatically from the beginning.

    **Authorizations for Task Model Management**


    <table>
    <tr>
    <th valign="top">

    Authorization
    
    </th>
    <th valign="top">

    Description
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Read*
    
    </td>
    <td valign="top">
    
    Read authorization within the scope of this user role.

    This is the minimum authorization, and it's included in all others.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Write*
    
    </td>
    <td valign="top">
    
    Authorization to create and edit task models, task model types, and job variants from within SAP Advanced Financial Closing. This authorization always includes *Read* authorization.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Publish*
    
    </td>
    <td valign="top">
    
    Authorization to publish task models, task model types, and job variants from within SAP Advanced Financial Closing. This authorization always includes *Read* authorization.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Delete*
    
    </td>
    <td valign="top">
    
    Authorization to delete task models, task model types, and job variants from within SAP Advanced Financial Closing. This authorization always includes *Read* authorization.
    
    </td>
    </tr>
    </table>
    
9.  Repeat the previous step to assign additional authorizations.

10. To remove an authorization, choose the corresponding *Delete* icon :x:.

    > ### Remember:  
    > Some authorizations include others. When removing authorizations, you need to start with the broader authorization, since the included authorization is a minimum for the broader one.

11. Under *Assigned Communication Systems*, add the communication systems where the task models for which you want to grant authorization are located.

12. Whenever you made a change to a user role, choose *Activate* in the header.

    This activates the user role and, if users were already assigned, this also synchronizes any changes with the users assigned.




<a name="loio1727010ff7724f56bbcd0e71d0e1f759__result_mcz_31k_qrb"/>

## Results

You have now created a user role within the scope *Task Model Management* for access restricted to task models located in specific communication systems.



<a name="loio1727010ff7724f56bbcd0e71d0e1f759__postreq_ibf_k1k_qrb"/>

## Next Steps

Grant users this access by assigning them to the user role or the role to them. For more information, see [How to Assign Users to User Roles](how-to-assign-users-to-user-roles-f703a5c.md).

