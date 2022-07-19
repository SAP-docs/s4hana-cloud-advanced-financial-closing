<!-- loio822ddcf75cb3484183ab11f4648039a0 -->

# How to Grant Access to Specific Objects

Grant access to specific task list templates and task lists by assigning one or more authorizations available within this scope.



<a name="loio822ddcf75cb3484183ab11f4648039a0__prereq_hmn_1bj_qrb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_Config`

    -   `AFC_UserRoles`


    For more information about role templates, see [How to Manage Static Role Templates](how-to-manage-static-role-templates-0cca34d.md).

-   You've familiarized yourself with the information under [Task List Creation Scope](task-list-creation-scope-ba4100e.md) to ensure that you're using the right means to grant access.




## Context

You can grant access that is restricted to specific task list templates and task lists. The authorizations you select for this user role then only apply to templates and task lists to which the selected authorization groups are assigned. Access is also granted to underlying folders and tasks. The following graphic explains the relationship between the aspects involved:

 ![Graphic depicting the relationship between objects and user roles: A user is assigned to a user role, which in turn has authorizations assigned. Additionally, authorization groups are assigned to the user role and to task list templates or task lists at the same time. This assignment on both sides (user role and task list) establishes the relationship between user and object and it grants access. Access to the task list or template automatically grants access to underlying folders and tasks.](images/Image_New_Auth_Concept_-_DEF_scope_Access_to_Specific_Objects_b23b76d.png) 

The abstraction level between user roles and specific objects enables you to grant access to collections of objects, for example, according to the domain of expertise.

> ### Example:  
> **Quick Demo: Access to Specific Objects Within the *Task List Creation* Scope**
> 
> The following quick demo shows how to create a user role within the *Task List Creation* scope granting *Generate* access to specific object types performing the steps described below:
> 
> > ### Note:  
> > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
> > 
> > Interfaces may differ slightly depending on the version of your apps.



## Procedure

1.  Open the *Configuration* app and choose *Authorization Groups*.

2.  Choose *Create*.

3.  Provide the following information:

    1.  Under *Name*, freely define a name for your authorization group.

    2.  Under *Applied To*, select *Task List Template / Task List*.

    3.  Under *Description*, you can add a description for your authorization group.


4.  Save.

5.  Go back to the *Configuration* app and choose *User Roles*.

6.  Go to the *Scoped User Roles* tab.

7.  Choose *Create*.

8.  Provide the following information:

    1.  Under *Name*, freely define a name for your user role.

    2.  Under *Description*, you can add a description for your user role.

    3.  Under *Scope*, select *Task List Creation*.

    4.  *Type* \(read-only\):

        For the scope *Task List Creation*, this is always *System-Independent*.

    5.  Under *Restriction*, select *Restricted*.


9.  Choose *Create*.

10. Under *Authorizations*, choose *Add* and select an authorization you want to add.

    > ### Note:  
    > A user role must have at least one authorization assigned.

    <a name="loio822ddcf75cb3484183ab11f4648039a0__d15e3581"/>Authorizations for Task List Creation


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

    Read authorization within the scope of this user role. This is the minimum authorization, and it's included in all others.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Create*


    
    </td>
    <td valign="top">

    Authorization to create and copy task list templates. This authorization always includes *Read* authorization.

    This authorization can't be assigned to restricted user roles.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Write*


    
    </td>
    <td valign="top">

    Authorization to edit and delete task list templates and task lists. This authorization always includes *Read* authorization and *User Assignment* authorization.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Generate*


    
    </td>
    <td valign="top">

    Authorization to generate task lists and change the status of task lists. This authorization always includes *Read* authorization.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *User Assignment*


    
    </td>
    <td valign="top">

    Authorization to change processing users or user groups, and users responsible or responsible user groups within the scope of this user role. This authorization allows changes **only through quick actions**. This authorization always includes *Read* authorization.


    
    </td>
    </tr>
    </table>
    
    > ### Note:  
    > The *Read* authorization will automatically be added if you add another authorization before adding *Read*.

    1.  Repeat the previous step to assign additional authorizations.

    2.  To remove an authorization, select it and choose *Delete*.

        > ### Remember:  
        > Some authorizations include others. When removing authorizations, you need to start with the broader authorization, since the included authorization is a minimum for the broader one.


11. Under *Task List Templates* and *Task Lists*, add the authorization group you created before to define access to the specific objects of the respective object type.

    > ### Note:  
    > You can add several authorization groups if the selected authorizations need to be applied to several authorization groups. Keep in mind that all users who have this role assignment have access to **all objects** that these authorization groups are assigned to on task list level.

12. Choose *Activate*.

    This activates the user role and, if users were already assigned, this also synchronizes any changes with the users assigned.




<a name="loio822ddcf75cb3484183ab11f4648039a0__result_jfj_ljj_qrb"/>

## Results

You have now created a user role within the scope *Task List Creation* for access restricted to task lists and templates that have the selected authorization groups assigned. This authorization applies to entire templates or task lists, including their folders and tasks.



<a name="loio822ddcf75cb3484183ab11f4648039a0__postreq_wm2_tjj_qrb"/>

## Next Steps

Grant users this access by assigning them to the user role or the role to them. For more information, see [How to Assign Users to User Roles](how-to-assign-users-to-user-roles-f703a5c.md).

