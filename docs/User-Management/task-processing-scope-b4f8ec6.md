<!-- loiob4f8ec6e1c9745469f1574ee1b1e56e1 -->

# Task Processing Scope

Grant access to process and approve or reject tasks.



<a name="loiob4f8ec6e1c9745469f1574ee1b1e56e1__section_z5g_1kj_qrb"/>

## About This Scope



### Apps in This Scope

-   *Process Closing Tasks*

-   *Approve Closing Tasks*

-   *Change Log*




### System Dependency of Roles

User roles created for this scope can be **system-independent** or **system-dependent**. This means that you can either tie these authorizations to a specific communication system or apply these authorizations across all communication systems.



### Restrictions

User roles created for this scope can be restricted or unrestricted.

For restricted roles, access is granted indirectly through authorization groups, which can be assigned to task list templates and tasks, or through specific organizational units.



### Authorizations in This Scope

When creating a user role for this scope, you can choose from the following authorizations:

**Authorizations for Task Processing**


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



<a name="loiob4f8ec6e1c9745469f1574ee1b1e56e1__section_jtk_1kj_qrb"/>

## Actions Allowed Based on Authorization of Scoped User Roles

****


<table>
<tr>
<th valign="top">

Authorization



</th>
<th valign="top">

*Read*



</th>
<th valign="top">

*Process*



</th>
<th valign="top">

*Plan*



</th>
<th valign="top">

*Parameters*



</th>
<th valign="top">

*User Assignment*



</th>
<th valign="top">

*Approve / Reject*



</th>
</tr>
<tr>
<td valign="top">

Read



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
</tr>
<tr>
<td valign="top">

Download Results



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
<td valign="top">

`X`



</td>
</tr>
<tr>
<td valign="top">

Change Task Status



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



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

Schedule



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



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

Delete Scheduling



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



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

Start Test Run



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



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

Delete Test Run



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



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

Edit Attachments / Notes



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



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

Change Planned Start



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



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

Change Planned Duration



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



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

Change Parameters



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
<td valign="top">

`X`



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

Change User / User Group Responsible



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

`X`



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

Change Processing User / User Group



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

`X`



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

Approve



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
<td valign="top">

`X`



</td>
</tr>
<tr>
<td valign="top">

Reject



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
<td valign="top">

`X`



</td>
</tr>
</table>



<a name="loiob4f8ec6e1c9745469f1574ee1b1e56e1__section_tqn_1kj_qrb"/>

## How to Manage Access in This Scope

Find more information about how to manage access in this scope in the following documents:

-   **[How to Grant General Access](how-to-grant-general-access-2d5fa55.md "Grant general access by assigning one or more authorizations available within this
		scope.")**  
Grant general access by assigning one or more authorizations available within this scope.
-   **[How to Grant System-Wide Access](how-to-grant-system-wide-access-92e1980.md "Grant system-wide access by assigning one or more authorizations available within this
		scope.")**  
Grant system-wide access by assigning one or more authorizations available within this scope.
-   **[How to Grant Access to Specific Objects](how-to-grant-access-to-specific-objects-1d6de41.md "Grant access to specific task list templates, task lists, or tasks by assigning one
		or more authorizations available within this scope.")**  
Grant access to specific task list templates, task lists, or tasks by assigning one or more authorizations available within this scope.
-   **[How to Grant Access by Organizational Units](how-to-grant-access-by-organizational-units-16947f1.md "Grant access to specific organizational units by assigning one or more authorizations
		available within this scope.")**  
Grant access to specific organizational units by assigning one or more authorizations available within this scope.

