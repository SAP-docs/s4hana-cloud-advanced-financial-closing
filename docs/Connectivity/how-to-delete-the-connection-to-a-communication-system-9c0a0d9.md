<!-- loio9c0a0d9edb744cb8bbfbf7eb55b5b1ab -->

# How to Delete the Connection to a Communication System

Delete the connection between SAP Advanced Financial Closing and the communication system.



<a name="loio9c0a0d9edb744cb8bbfbf7eb55b5b1ab__prereq_osc_vx5_3tb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_SystemAdmin`

    -   `AFC_SpecifySystemsApp`


    For more information about role templates, see [How to Manage Static Role Templates](../User-Management/how-to-manage-static-role-templates-0cca34d.md) and [Static Roles for SAP Advanced Financial Closing](../User-Management/static-roles-for-sap-advanced-financial-closing-b92a241.md).

-   The communication system **must not have been synchronized** yet.

-   


<a name="loio9c0a0d9edb744cb8bbfbf7eb55b5b1ab__context_c1x_wx5_3tb"/>

## Context

The connection to a communication system can be removed only if no synchronization has taken place yet. The reason for this is that, after synchronization, objects are referenced, and deleting the connection would disrupt this reference.



<a name="loio9c0a0d9edb744cb8bbfbf7eb55b5b1ab__steps_xqc_xx5_3tb"/>

## Procedure

1.  Open the *Specify Communication Systems* app.

2.  From the table, select the communication system for which you want to delete the connection to SAP Advanced Financial Closing.

3.  Choose *Delete* in the table toolbar.




<a name="loio9c0a0d9edb744cb8bbfbf7eb55b5b1ab__result_dvk_bjv_3tb"/>

## Results

You have now deleted the connection between SAP Advanced Financial Closing and the selected communication system.

> ### Note:  
> Deleting the connection between the communication system and SAP Advanced Financial Closing doesn't delete the destination on the SAP BTP. If you want to delete the SAP BTP destination as well, you need to do this in the SAP BTP cockpit.

