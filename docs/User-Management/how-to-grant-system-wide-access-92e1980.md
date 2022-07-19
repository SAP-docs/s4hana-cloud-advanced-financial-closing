<!-- loio92e1980503e24d0fbb363c8787c55a51 -->

# How to Grant System-Wide Access

Grant system-wide access by assigning one or more authorizations available within this scope.



<a name="loio92e1980503e24d0fbb363c8787c55a51__prereq_kym_2yj_qrb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_Config`

    -   `AFC_UserRoles`


    For more information about role templates, see [How to Manage Static Role Templates](how-to-manage-static-role-templates-0cca34d.md).

-   You've familiarized yourself with the information under [Task Processing Scope](task-processing-scope-b4f8ec6.md) to ensure that you're using the right means to grant access.




## Context

You can grant access that is tied to a specific communication system without being restricted to specific objects or organizational units. You can still decide which authorizations to grant. This means that even though user access isn't restricted to specific objects or organizational units, system-wide access doesn't necessarily mean that users can perform all actions.

> ### Example:  
> **Quick Demo: System-Wide Access Within the *Task Processing* Scope**
> 
> *Task Processing* scope granting system-wide *User Assignment* access performing the steps described below:
> 
> > ### Note:  
> > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
> > 
> > Interfaces may differ slightly depending on the version of your apps.



## Procedure

1.  Open the *Configuration* app and choose *User Roles*.

2.  Go to the *Scoped User Roles* tab.

3.  Choose *Create*.

4.  Provide the following information:

    1.  Under *Name*, freely define a name for your user role.

    2.  Under *Description*, you can add a description for your user role.

    3.  Under *Scope*, select *Task Processing*.

    4.  Under *Type*, select *System-Dependent*.

    5.  Under *Restriction*, select *Unrestricted*.

    6.  Under *Communication System*, select the communication system for which the user role applies.


5.  Choose *Create*.

6.  Under *Authorizations*, choose *Add* and select an authorization you want to add.

    > ### Note:  
    > A user role must have at least one authorization assigned.

    > ### Remember:  
    > For users who have this role assignment, the authorizations selected apply across all task lists generated for the selected communication system.

    <a name="loio92e1980503e24d0fbb363c8787c55a51__d15e3677"/>Authorizations for Task Processing


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

    *Process*


    
    </td>
    <td valign="top">

    Authorization to process tasks. This authorization covers actions related to task status changes, scheduling, test runs, attachments, and notes. This authorization always includes *Read* authorization.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Plan*


    
    </td>
    <td valign="top">

    Authorization to change attributes that refer to the planning of a task. This authorization covers changes of planned start and planned duration. This authorization always includes *Read* authorization.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Parameters*


    
    </td>
    <td valign="top">

    Authorization to change parameters within the scope of this user role. This authorization always includes *Read* authorization.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *User Assignment*


    
    </td>
    <td valign="top">

    Authorization to change processing users or user groups, and users responsible or responsible user groups within the scope of this user role. This authorization always includes *Read* authorization.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Approve / Reject*


    
    </td>
    <td valign="top">

    Authorization to approve and reject tasks that require approval. This authorization always includes *Read* authorization.


    
    </td>
    </tr>
    </table>
    
    > ### Note:  
    > The *Read* authorization will automatically be added if you add another authorization before adding *Read*.

    1.  Repeat the previous step to assign additional authorizations.

    2.  To remove an authorization, select it and choose *Delete*.

        > ### Remember:  
        > Some authorizations include others. When removing authorizations, you need to start with the broader authorization, since the included authorization is a minimum for the broader one.


7.  Choose *Activate*.

    This activates the user role and, if users were already assigned, this also synchronizes any changes with the users assigned.




<a name="loio92e1980503e24d0fbb363c8787c55a51__result_cqq_4yj_qrb"/>

## Results

You have now created a user role for system-wide access within the The following quick demo shows how to create a user role within the *Task Processing* scope.



<a name="loio92e1980503e24d0fbb363c8787c55a51__postreq_www_4yj_qrb"/>

## Next Steps

Grant users this access by assigning them to the user role or the role to them. For more information, see [How to Assign Users to User Roles](how-to-assign-users-to-user-roles-f703a5c.md).

