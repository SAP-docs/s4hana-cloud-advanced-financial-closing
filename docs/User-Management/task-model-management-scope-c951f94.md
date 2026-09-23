<!-- loioc951f94d942e48e08a7895e63fed0bf9 -->

# Task Model Management Scope

Grant access to work with task models.



<a name="loioc951f94d942e48e08a7895e63fed0bf9__section_rht_dlc_qrb"/>

## About This Scope



### Apps in This Scope

-   *Manage Task Models*
-   *Task Model Change Log*



### System Dependency of User Roles

User roles created for this scope are technically labelled **system-independent**. You can, however, limit this user role to task models in one or more communication systems by creating a restricted user role.



### Restricting Access

User roles created for this scope can be granted restricted or unrestricted access.

For restricted roles, access is granted based on **communication systems** you assign to the user role. This means that you restrict the access to task models in the specified communication systems.



### Authorizations in This Scope

When creating a user role for this scope, you can choose from the following authorizations:

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



<a name="loioc951f94d942e48e08a7895e63fed0bf9__section_mqj_xmc_qrb"/>

## Actions Allowed Based on Authorization of Scoped User Roles

****


<table>
<tr>
<th valign="top">

Action

</th>
<th valign="top">

*Read*

</th>
<th valign="top">

*Write*

</th>
<th valign="top">

*Publish*

</th>
<th valign="top">

*Delete*

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

 

</td>
<td valign="top">

 

</td>
<td valign="top">

 

</td>
</tr>
<tr>
<td valign="top">

Create Task Models, Task Model Types, and Job Variants

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

Edit Task Models, Task Model Types, and Job Variants

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

Publish Task Models, Task Model Types, and Job Variants

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

Delete Task Models, Task Model Types, and Job Variants

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

Read Corresponding Change Log Entries

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



<a name="loioc951f94d942e48e08a7895e63fed0bf9__section_ljb_rmc_qrb"/>

## How to Manage Access in This Scope

Find more information about how to manage access in this scope in the following documents:

-   **[How to Grant General Access](how-to-grant-general-access-ddf490b.md "Grant general access by assigning one or more authorizations available within this
		scope.")**  
Grant general access by assigning one or more authorizations available within this scope.
-   **[How to Grant Access to Specific Objects](how-to-grant-access-to-specific-objects-1727010.md "Grant access to task models located in specific communication systems.")**  
Grant access to task models located in specific communication systems.

