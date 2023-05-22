<!-- loio3155ba8cff11434fae9b3fafdb00d0ab -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# Extended What's New: Switch of Authorization Concept

Understand the consequences of the retirement of the old authorization concept.



<a name="loio3155ba8cff11434fae9b3fafdb00d0ab__section_v3p_zlv_3xb"/>

## Context

> ### Note:  
> Changes in the concept affect mainly the authorizations granted for the following apps:
> 
> -   *Manage Closing Task Lists*
> -   *Process Closing Tasks*
> -   *Approve Closing Tasks*
> 
> Authorizations for the reporting apps *Financial Close Overview* and *Closing Task Completion* are granted based on the *Read* authorization for the *Task Processing* scope.

With the release made available in January 2022, we introduced a new authorization concept, which has existed in parallel to the previously existing concept since. The new authorization concept introduced scoped user roles as opposed to the existing user roles of the old concept. Additionally, the new authorization concept on its own is more restrictive in the authorizations granted through direct user assignments. However, since both concepts existed in parallel and direct user assignments had to be handled the same way for both, some authorizations were granted for compatibility reasons with the intention of removing them once the old authorization concept was retired.



<a name="loio3155ba8cff11434fae9b3fafdb00d0ab__section_w3p_zlv_3xb"/>

## Retirement of the Old Authorization Concept

In January 2023, we announced the retirement of the old authorization concept planned for May 2023. A step-by-step retirement process has been carried out since, involving the following steps:

1.  In February 2023, user roles that were part of the old authorization concept - that is, non-scoped user roles - were set to read-only. Accordingly, editing these roles and adding users to them was no longer possible.
2.  In March 2023, any drafts for non-scoped user roles that still existed at the time the release was made available were removed.
3.  In May 2023, the old authorization concept and the roles that were part of it were retired with the following consequences:
    -   Old user roles are no longer considered for authorizations.

        > ### Note:  
        > These old user roles are still visible in the *Manage User Roles* app on the corresponding tab. You can still remove assignments from them or delete them, but they can't be assigned anymore and won't be considered for authorizations in advanced financial closing.

    -   Authorizations granted through direct assignments have changed, since authorizations granted for compatibility reasons were removed.




<a name="loio3155ba8cff11434fae9b3fafdb00d0ab__section_stk_2mv_3xb"/>

## Consequences of the Authorization Concept Switch

In the following table, you can find a detailed overview of the consequences this switch - and especially the retirement of the old concept - entails:


<table>
<tr>
<th valign="top">

Criterion



</th>
<th valign="top">

Old Authorization Concept



</th>
<th valign="top">

New Authorization Concept



</th>
<th valign="top">

More Information



</th>
</tr>
<tr>
<td valign="top">

General Approach



</td>
<td valign="top">

User roles were defined mainly by restriction type and system dependency. User roles granted authorizations to perform actions in different apps and thus for different responsibilities that would mostly be spread between different users.

Direct user assignment to a task list or task granted access without the need of assigning a user role.



</td>
<td valign="top">

User roles are connected to scopes. For each role, authorizations are assigned, such as the *Read*, *Create*, or *Process* authorization. Additionally, access may be restricted to specific objects or organizational units. Also, a possible system dependency can still be defined for each role.

Direct user assignment to a task list or task still grants access without the need of assigning a user role, but in a more differentiated way to ensure segregation of duties.



</td>
<td valign="top">

[User Access Management](user-access-management-d974847.md)



</td>
</tr>
<tr>
<td valign="top">

User Roles



</td>
<td valign="top">

User roles were defined by type \(restricted/unrestricted\) and a possible system dependency. However, they granted authorizations that weren't connected to the specific responsibility - or scope - of either creating task lists or processing and approving tasks.



</td>
<td valign="top">

Scoped user roles introduce the approach of granting access based on the user's responsibilities of either creating task lists \(*Task List Creation* scope\) or processing and approving tasks \(*Task Processing* scope\). These roles allow for a more detailed and restrictive authorization approach, granting users only those authorizations required. Within each role, you can still decide which authorizations should be granted for this scope, such as the *Read*, *Create*, or *Process* authorization.



</td>
<td valign="top">

-   [Task List Creation Scope](task-list-creation-scope-ba4100e.md)
-   [Task Processing Scope](task-processing-scope-b4f8ec6.md)



</td>
</tr>
<tr>
<td valign="top">

Direct User Assignment



</td>
<td valign="top">

Direct assignment to a task list, folder, or task as owner, user responsible, processing user, or as part of a user group in the corresponding responsibility granted access independently of user roles. Some direct assignments granted users the authorization to perform actions in different apps solely based on the direct assignment, for example, in the *Manage Closing Task Lists* app and in the *Process Closing Tasks* app.



</td>
<td valign="top">

Direct assignments still grant access independently of user roles. However, a more differentiated approach was taken to ensure segregation of duties. Users can perform actions only within one scope, allowing the owner, for example, to perform several actions in the *Manage Closing Task Lists* app, but no actions in the *Process Closing Tasks* app.

The table below highlights the authorizations for direct assignments that were previously granted for compatibility reasons but were revoked with the retirement of the old authorization concept.



</td>
<td valign="top">

[Direct User Assignment](direct-user-assignment-f96b217.md)



</td>
</tr>
</table>



### Direct Assignment Authorizations in the New Authorization Concept

> ### Note:  
> Since authorizations for substitutes are derived from the user they're substituting for, the substitutes' authorizations are affected in the same way as the user they're assigned.

** **


<table>
<tr>
<th valign="top">

Scope Affected



</th>
<th valign="top">

Actions



</th>
<th valign="top">

Owner / Owner Group



</th>
<th valign="top">

User / User Group Responsible \(Task List Template / Task List\)



</th>
<th valign="top">

User / User Group Responsible \(Organizational Unit Folder\)



</th>
<th valign="top">

User / User Group Responsible \(Task\)



</th>
<th valign="top">

Processing User / User Group



</th>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Read



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Create



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Copy



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Edit / Save



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Recalculate Paths



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Delete



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Generate



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Change Task List Status



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Change User Assignments \(Quick Actions\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Check SOX Compliance



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

Check Compatibility



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Read



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Download Results



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Change Task Status



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Schedule



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Delete Scheduling



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Start Test Run



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Delete Test Run



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Edit Attachments/Notes



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

:heavy_check_mark:



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Change Planned Start



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Change Planned Duration



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Recalculate Paths



</td>
<td valign="top">

 



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Change Parameters



</td>
<td valign="top">

 



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
<td valign="top">

<span style="color:#ffffff;"><span style="background-color:#cc1919;"><span class="SAP-icons"></span></span></span> \(revoked as of May 2023\)



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Change User / User Group Responsible



</td>
<td valign="top">

 



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Change Processing User / User Group



</td>
<td valign="top">

 



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Approve



</td>
<td valign="top">

 



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

Reject



</td>
<td valign="top">

 



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

:heavy_check_mark:



</td>
<td valign="top">

 



</td>
</tr>
</table>

**Parent topic:** [User Management](user-management-ae7fa30.md "Understand how you can manage users and their authorizations in SAP S/4HANA Cloud for advanced financial closing.")

**Next:** [User Access Management](user-access-management-d974847.md "You can control and grant access to task list templates, task lists, and tasks in SAP S/4HANA Cloud for advanced financial closing. By default, users don't have access to these objects.")

