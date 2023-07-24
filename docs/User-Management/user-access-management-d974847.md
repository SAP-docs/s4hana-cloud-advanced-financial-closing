<!-- loiod974847a74d34f2795f97d75a90ce8eb -->

# User Access Management

You can control and grant access to task list templates, task lists, and tasks in SAP S/4HANA Cloud for advanced financial closing. By default, users don't have access to these objects.



<a name="loiod974847a74d34f2795f97d75a90ce8eb__section_eys_rpv_rrb"/>

## Access to Apps in General

Users who have been assigned a static role can see the respective apps in the SAP Fiori launchpad \(see [How to Manage Static Role Templates](how-to-manage-static-role-templates-0cca34d.md)\). For the following apps, you need to grant access to users so that they're able to view or edit **task list templates**, **task lists**, **tasks**, and **folders**:

-   *Manage Closing Task Lists*

-   *Process Closing Tasks*

-   *Approve Closing Tasks*

-   *Financial Close Overview* \(derived from the *Read* authorization in the *Task Processing* scope\)

-   *Closing Task Completion* \(derived from the *Read* authorization in the *Task Processing* scope\)

-   *Change Log* \(derived from the *Read* authorization in the *Task Processing* scope\)


In all other apps, users only require a matching static role. A display-only role provides them with read access, while the standard roles always grant full access so that no further access needs to be granted on object level. This affects access to the following apps:


<table>
<tr>
<th valign="top">

Administration Apps



</th>
<th valign="top">

Configuration Apps



</th>
<th valign="top">

System Configuration and Monitoring Apps



</th>
<th valign="top">

Migration Apps



</th>
</tr>
<tr>
<td valign="top">

-   *Manage Users*
-   *Manage User Role Assignments*
-   *Manage Compliance Settings*
-   *Manage Archived Closing Task Lists*



</td>
<td valign="top">

All apps accessed through the *Configuration* tile



</td>
<td valign="top">

-   *Specify Communication Systems*
-   *Monitor Communication Systems*
-   *Monitor Business Logs*



</td>
<td valign="top">

-   *Migrate Configuration Data*
-   *Migrate Closing Task Lists*



</td>
</tr>
</table>



<a name="loiod974847a74d34f2795f97d75a90ce8eb__section_bxk_rpv_rrb"/>

## Grant Access

To grant access for specific scopes, you have two options: scoped user roles and direct assignment. With scoped user roles, you can grant access on a broader scale, while direct assignments grant access on an object basis. You can grant access by choosing either only one method or both methods. Hence, on the one hand, you can assign the user either through a scoped user role or through direct assignment. On the other hand, however, you can also grant access through a combination of both. This gives you the possibility to grant broader access to several users and then further access to specific objects for specific users.



<a name="loiod974847a74d34f2795f97d75a90ce8eb__section_edb_qgc_qrb"/>

## Scoped User Roles

Provided that users have the corresponding static role templates assigned, you control and grant specific access on a first level based on user roles assigned to a specific scope. Within each scope, you can control access in more detail by granting, for example, access in general, system-wide access, or access according to objects or organizational units.

You can create scoped user roles to grant access to the different scopes defined for advanced financial closing.

Within each scope, there are different authorizations that you can assign to a user role. These authorizations take effect as soon as you assign a user to the role or the role to a user.

> ### Note:  
> A substitute of an owner, a user responsible, or a processing user doesn't inherit role assignments. Accordingly, substitutes may need to be assigned to the same user roles as the owners, users responsible, or processing users they're substituting for.



### Scopes

User roles apply explicitly to one of the following scopes:


<table>
<tr>
<th valign="top">

Scope



</th>
<th valign="top">

Apps in Scope



</th>
<th valign="top">

Description



</th>
</tr>
<tr>
<td valign="top">

*Task List Creation*



</td>
<td valign="top">

-   *Manage Closing Task Lists*

-   *Change Log*




</td>
<td valign="top">

Grant access to create and edit task list templates as well as to generate task lists. Users who are granted access for this scope automatically get access to the related entries in the change log.

For more information, see [Task List Creation Scope](task-list-creation-scope-ba4100e.md).



</td>
</tr>
<tr>
<td valign="top">

*Task Processing*



</td>
<td valign="top">

-   *Process Closing Tasks*

-   *Approve Closing Tasks*

-   *Change Log*

-   *Closing Task Completion*

-   *Financial Close Overview*




</td>
<td valign="top">

Grant access to process and approve tasks. Users who are granted access for this scope automatically get access to the related entries in the change log and the apps for reporting.

For more information, see [Task Processing Scope](task-processing-scope-b4f8ec6.md).



</td>
</tr>
</table>



<a name="loiod974847a74d34f2795f97d75a90ce8eb__section_r2p_w3c_qrb"/>

## Direct Assignments

You can grant users direct access without assigning them to any user role or authorization group. Accordingly, the access you grant them by direct assignment only applies to the object you assign them to. Users receive a specific default authorization that is fixed and can't be freely defined.

You can assign users either as **owner**, **user responsible**, or **processing user**. You can also perform this direct assignment using substitutes for individual users or by assigning user groups. When assigning user groups, you provide access to every member of the user group.

For more information about direct assignments, see [Direct User Assignment](direct-user-assignment-f96b217.md).

-   **[Overview of Means and Actions to Grant Access](overview-of-means-and-actions-to-grant-access-1923b89.md "Understand how you can grant which access.")**  
Understand how you can grant which access.
-   **[Task List Creation Scope](task-list-creation-scope-ba4100e.md "Grant access to create and edit task list templates and to generate task
		lists.")**  
Grant access to create and edit task list templates and to generate task lists.
-   **[Task Processing Scope](task-processing-scope-b4f8ec6.md "Grant access to process and approve or reject tasks.")**  
Grant access to process and approve or reject tasks.
-   **[Direct User Assignment](direct-user-assignment-f96b217.md "Grant access by directly assigning a user or user group to a task list template, task
		list, folder, or task.")**  
Grant access by directly assigning a user or user group to a task list template, task list, folder, or task.
-   **[How to Copy User Roles](how-to-copy-user-roles-c16170b.md "Copy scoped user roles.")**  
Copy scoped user roles.
-   **[How to Assign Users to User Roles](how-to-assign-users-to-user-roles-f703a5c.md "Specify the users to whom the user roles you've created apply.")**  
Specify the users to whom the user roles you've created apply.
-   **[How to Manage User Groups](how-to-manage-user-groups-45bb6c9.md "A user group represents a group of users who can be assigned to a particular set of
		closing tasks.")**  
A user group represents a group of users who can be assigned to a particular set of closing tasks.
-   **[How to Manage User Access Using the SCIM API Provided](how-to-manage-user-access-using-the-scim-api-provided-49376ed.md "Manage users, user groups, and user roles through a dedicated API.")**  
Manage users, user groups, and user roles through a dedicated API.

**Parent topic:**[User Management](user-management-ae7fa30.md "Understand how you can manage users and their authorizations in SAP S/4HANA Cloud for advanced financial closing.")

**Next:**[How to Manage Users](how-to-manage-users-c338b30.md "Upload new users to SAP S/4HANA Cloud for advanced financial closing and update certain user attributes.")

**Previous:**[Extended What's New: Switch of Authorization Concept](extended-what-s-new-switch-of-authorization-concept-3155ba8.md "Understand the consequences of the retirement of the old authorization concept.")

