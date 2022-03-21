<!-- loioba4100eba36940588d837922691349ba -->

# Task List Creation Scope

Grant access to create and edit task list templates and to generate task lists.



<a name="loioba4100eba36940588d837922691349ba__section_rht_dlc_qrb"/>

## About This Scope



### Apps in This Scope

-   *Manage Closing Task Lists*

-   *Change Log*




### System Dependency of Roles

User roles created for this scope are **always system-independent**. This means that you can't tie these authorizations to a specific communication system.



### Restrictions

User roles created for this scope can be restricted or unrestricted.

> ### Note:  
> The authorization *Create* can only be given to unrestricted roles.

For restricted roles, access is granted indirectly through authorization groups, which can be assigned to task list templates and task lists.



### Authorizations in This Scope

When creating a user role for this scope, you can choose from the following authorizations:

<a name="loioba4100eba36940588d837922691349ba__d15e3621"/>Authorizations for Task List Creation


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



<a name="loioba4100eba36940588d837922691349ba__section_mqj_xmc_qrb"/>

## Actions Allowed Based on Authorization of Scoped User Roles

<a name="loioba4100eba36940588d837922691349ba__table_sc2_3nc_qrb"/>


<table>
<tr>
<th valign="top">

Actions Allowed



</th>
<th valign="top">

*Read*



</th>
<th valign="top">

*Create* \(only for unrestricted roles\)



</th>
<th valign="top">

*Write*



</th>
<th valign="top">

*Generate*



</th>
<th valign="top">

*User Assignment*



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
</tr>
<tr>
<td valign="top">

Create



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

Copy



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

Edit / Save



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

Delete



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

Generate



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

Change Task List Status



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

Change User Assignments \(Quick Actions\)



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

Check SOX Compliance



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

Check Compatibility



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
</table>



<a name="loioba4100eba36940588d837922691349ba__section_ljb_rmc_qrb"/>

## How to Manage Access in This Scope

Find more information about how to manage access in this scope in the following documents:

-   **[How to Grant Access in General](how-to-grant-access-in-general-dc228ef.md "Grant general access by assigning one or more authorizations available within this
		scope.")**  
Grant general access by assigning one or more authorizations available within this scope.
-   **[How to Grant Access to Specific Objects](how-to-grant-access-to-specific-objects-822ddcf.md "Grant access to specific task list templates and task lists by assigning one or more
		authorizations available within this scope.")**  
Grant access to specific task list templates and task lists by assigning one or more authorizations available within this scope.

