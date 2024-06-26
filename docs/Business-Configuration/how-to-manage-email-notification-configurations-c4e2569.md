<!-- loioc4e256920af749ab815d325ac8464302 -->

# How to Manage Email Notification Configurations

Create notification configurations and assign a set of email notification scenarios to a task list.



<a name="loioc4e256920af749ab815d325ac8464302__prereq_wcz_hzb_ckb"/>

## Prerequisites

Your user must have a role collection assigned that includes one of the following role templates:

-   `AFC_Config`

-   `AFC_Settings`

-   `AFC_NotificationsApp`


For more information about role templates, see [How to Manage Static Role Templates](../User-Management/how-to-manage-static-role-templates-0cca34d.md) and [Static Roles for SAP Advanced Financial Closing](../User-Management/static-roles-for-sap-advanced-financial-closing-b92a241.md).



## Context

A notification configuration assigned to a task list controls when and how processing users or users responsible are notified by email. The settings in the notification configuration apply to the task list and to all tasks in the template or task list.

The default notification configuration is prefilled when you create a new task list template in the *Manage Closing Task Lists* app.

> ### Example:  
> The following quick demo shows how to create an email notification configuration performing the steps described below:
> 
> > ### Note:  
> > The following multimedia content displays screens and interfaces in English only. It shows sequences based on the UI as delivered standard by SAP.
> > 
> > Interfaces may differ slightly depending on the version of your apps.



## Procedure

1.  Go to the *Configuration* app and choose *Email Notification Configurations* from the table.

2.  Choose *Create* in the table toolbar.

3.  Enter a name and description for the email notification configuration.

4.  Under *Scenarios*, choose *Add*.

5.  In the table, select the scenarios for which you want notifications to be sent.

6.  Choose *Add* in the dialog footer.

7.  In the *Scenarios* table, select who should receive an email notification for each scenario by checking the box in the corresponding table column.

    You have the following recipients or recipient groups available:

    -   Users responsible
    -   Processing users
    -   Interested users

8.  Choose *Create* in the footer to create the configuration.




<a name="loioc4e256920af749ab815d325ac8464302__result_tlh_34s_qtb"/>

## Results

You have now created an email notification configuration.



<a name="loioc4e256920af749ab815d325ac8464302__postreq_wgv_qjt_3mb"/>

## Next Steps

Assign this email notification configuration to your task list templates, task lists, or tasks to enable notifications for users responsible and processing users.

