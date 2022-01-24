<!-- loio835ce12f7d4f4e8cab5df36537aea3c1 -->

# How to Manage Compliance Settings

The compliance settings apply to all apps that are part of advanced financial closing.



<a name="loio835ce12f7d4f4e8cab5df36537aea3c1__prereq_bxw_m3y_rjb"/>

## Prerequisites

Your user must have a role collection assigned that includes the role template `AFC_Compliance`.

For more information about role templates, see [How to Manage Static Role Templates](../User-Management/how-to-manage-static-role-templates-0cca34d.md).



## Context

The following settings are available:

<a name="loio835ce12f7d4f4e8cab5df36537aea3c1__d14e1214"/>Compliance Settings


<table>
<tr>
<th valign="top">

Field



</th>
<th valign="top">

Effect



</th>
</tr>
<tr>
<td valign="top">

*Anonymize Names in Emails*



</td>
<td valign="top">

Specify whether you want real names to be removed from emails sent by the advanced financial closing notification service. The default value is ***No***.



</td>
</tr>
<tr>
<td valign="top">

*Anonymize Completed Task Lists After*



</td>
<td valign="top">

Define a number of months as the time offset after which user names are removed from completed task lists. The default value is ***18*** months.

> ### Note:  
> If you enter ***0***, no anonymization is applied.
> 
> To enable anonymization, the minimum value is ***6*** months.



</td>
</tr>
<tr>
<td valign="top">

*Notify User Before Task Is Due*



</td>
<td valign="top">

To help ensure that tasks are completed before their scheduled end date, you can arrange for email and Fiori notifications to be sent to the processing user or user responsible. Define how many minutes before a task is due users are reminded about the task. The minimum value is ***10*** minutes.

> ### Note:  
> To enable email notifications for a task, an email notification configuration including the scenario *Planned End Time of Task Approaching* must be assigned.



</td>
</tr>
<tr>
<td valign="top">

*Enforce SOX Requirements*



</td>
<td valign="top">

Determine whether the Sarbanes-Oxley Act \(SOX\) compliance applies. The default value is ***Yes***. If the selection is set to *Yes*, the following rules apply:

-   User responsible and processing user of a task must not be the same.

-   Responsible user group and processing user group of a task must not be the same.




</td>
</tr>
</table>



## Procedure

1.  Go to the *Manage Compliance Settings* app.

2.  Choose *Edit*.

3.  Make your settings and save the changes.




<a name="loio835ce12f7d4f4e8cab5df36537aea3c1__result_ofp_5nt_3mb"/>

## Results

The compliance settings for your SAP S/4HANA Cloud for advanced financial closing have been updated.

