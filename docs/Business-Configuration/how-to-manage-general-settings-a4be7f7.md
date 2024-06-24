<!-- loioa4be7f7ef92d49bcba53be34fcd6f94c -->

# How to Manage General Settings

Maintain settings that apply to all objects in SAP Advanced Financial Closing.



<a name="loioa4be7f7ef92d49bcba53be34fcd6f94c__prereq_y22_qyk_3bc"/>

## Prerequisites

Your user must have a role collection assigned that includes the role template `AFC_GeneralSettings`.

For more information about role templates, see [How to Manage Static Role Templates](../User-Management/how-to-manage-static-role-templates-0cca34d.md) and [Static Roles for SAP Advanced Financial Closing](../User-Management/static-roles-for-sap-advanced-financial-closing-b92a241.md).



## Context

In SAP Advanced Financial Closing, generated task lists are archived automatically after a specific **time of inactivity**, independently of their status. The time after which a task list is archived depends on the closing type and on the value set for the *Is Production Task List* indicator. You define this time in the *Manage General Settings* app. The **highest values possible** - which are also the default values delivered by SAP - are defined as follows:




<table>
<tr>
<th valign="top">

Closing Type

</th>
<th valign="top">

Production Task Lists

</th>
<th valign="top">

Non-Production Task Lists

</th>
</tr>
<tr>
<td valign="top">

Month-End Closing

</td>
<td valign="top">

Six months

</td>
<td valign="top">

Three months

</td>
</tr>
<tr>
<td valign="top">

Quarter-End Closing

</td>
<td valign="top">

Nine months

</td>
<td valign="top">

Three months

</td>
</tr>
<tr>
<td valign="top">

Year-End Closing

</td>
<td valign="top">

18 months

</td>
<td valign="top">

Three months

</td>
</tr>
<tr>
<td valign="top">

Special-End Closing

</td>
<td valign="top">

Six months

</td>
<td valign="top">

Three months

</td>
</tr>
</table>

Task lists with status *Obsolete* are archived after one month, independently of the *Is Production Task List* indicator.

Once archived, task lists can be viewed and restored by authorized users. For more information, see [Task List Archiving](../Archiving/task-list-archiving-032bb8e.md).

> ### Note:  
> The archiving settings you make in this app relate to the archiving of task lists in SAP Advanced Financial Closing. They don't cover the archiving settings of objects and data in connected communication systems. For more information about object and data archiving in communication systems, see [Data Archiving in Connected Communication Systems](../Data-Management/data-archiving-in-connected-communication-systems-2829b08.md).



## Procedure

1.  Open the *Manage General Settings* app.

2.  In the *Archiving Times by Closing Type* section, choose the *Edit* button.

    > ### Remember:  
    > You define the archiving times based on months of inactivity. This means that you define how long a task list needs to be inactive before it is archived automatically.
    > 
    > To see changes made previously to the settings, you can display the change log within the *Manage General Settings* app.

    1.  Under *Production Task Lists*, define for each closing type the number of months of inactivity before a production task list is archived.

    2.  Under *Quality Task Lists*, define for each closing type the number of months of inactivity before a quality task list is archived.


3.  Choose *Save* to confirm your changes.




<a name="loioa4be7f7ef92d49bcba53be34fcd6f94c__result_ifn_zqx_3bc"/>

## Results

You have now defined the archiving settings for your task lists. The task lists will now be archived accordingly.

**Related Information**  


[Task List Archiving](../Archiving/task-list-archiving-032bb8e.md "Understand how archiving and restoring in SAP Advanced Financial Closing works.")

[Data Archiving in Connected Communication Systems](../Data-Management/data-archiving-in-connected-communication-systems-2829b08.md "Information about data archiving of objects relating to SAP Advanced Financial Closing.")

