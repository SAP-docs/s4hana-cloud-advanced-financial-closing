<!-- loio0d8e37f0589e4ef7a9fbbc48de4c1ea4 -->

# How to Set Up the SAP Build Process Automation Integration for SAP Advanced Financial Closing

Set up an integration with SAP Build Process Automation to use SAP Advanced Financial Closing to trigger workflows.



<a name="loio0d8e37f0589e4ef7a9fbbc48de4c1ea4__prereq_nqx_p4r_zcc"/>

## Prerequisites

-   Your entitlements for SAP Advanced Financial Closing and SAP Build Process Automation are part of the same SAP BTP subaccount.
-   For the steps to be performed with regards to or in SAP Build Process Automation, you need to have the required authorization.
-   For the steps to be performed in SAP Advanced Financial Closing, the following authorizations are required:
    -   Your user must have a role collection assigned that includes one of the following role templates:

        -   `AFC_SystemAdmin`

        -   `AFC_SpecifySystemsApp`


        For more information about role templates, see [How to Manage Static Role Templates](../User-Management/how-to-manage-static-role-templates-0cca34d.md) and [Static Roles for SAP Advanced Financial Closing](../User-Management/static-roles-for-sap-advanced-financial-closing-b92a241.md).





## Context

In SAP Build Process Automation, you can create workflows to perform specific steps, providing conditions and events and a lot more. You can set up an integration between SAP Build Process Automation and SAP Advanced Financial Closing to use SAP Advanced Financial Closing to trigger these workflows. After processing, the status of the workflow is then reported back to SAP Advanced Financial Closing. This way, you can fully integrate workflows into your financial close and use SAP Advanced Financial Closing to trigger them automatically and receive results, and apply an approval process.

> ### Caution:  
> This integration can't be used in parallel to the stand-alone integration described under [Process Automation Integration Based on ABAP](process-automation-integration-based-on-abap-a1d7fe3.md).



## Procedure

1.  If not done yet, subscribe to SAP Build Process Automation as described under [Subscribe to SAP Build Process Automation](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/subscribe-to-sap-build-process-automation) \(SAP Build Process Automation documentation\).

2.  If not done yet, create workflows in SAP Build Process Automation that you want to include into your financial close managed in SAP Advanced Financial Closing. For information on how to do this, see [Use SAP Build Process Automation](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/using-sap-build-process-automation) \(SAP Build Process Automation documentation\).

    > ### Tip:  
    > The authorizations required for steps in SAP Build Process Automation are described under [Authorizations](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/authorizations) \(SAP Build Process Automation documentation\).

    > ### Caution:  
    > SAP Advanced Financial Closing currently doesn't support arrays, relative dates, or custom data types for parameters of workflows in SAP Build Process Automation.

3.  Set up a communication system in SAP Advanced Financial Closing:

    > ### Note:  
    > This communication system can't be added to task list templates. To add workflows to a task list template, the communication system in which the workflow is processed needs to be added to the template.

    1.  In SAP Advanced Financial Closing, go to the *Specify Communication Systems* app.

    2.  Choose *Create* \> *Create Local SAP Build Process Automation System* in the table toolbar.

    3.  Enter the following information:


        <table>
        <tr>
        <th valign="top">

        Field
        
        </th>
        <th valign="top">

        Description
        
        </th>
        </tr>
        <tr>
        <td valign="top">
        
        *Name*
        
        </td>
        <td valign="top">
        
        Enter a name for the communication system.
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *SAP Build Process Automation URL*
        
        </td>
        <td valign="top">
        
        Automatically filled with the URL of your SAP Build Process Automation tenant.
        
        </td>
        </tr>
        </table>
        
    4.  Save.

    5.  Check whether the connection between SAP Advanced Financial Closing and SAP Build Process Automation works by choosing the *Open SAP Build Process Automation* button in the *SAP Build Process Automation* section.

    6.  **Optional:** Under *Notifications*, you can set up notifications about system errors. Follow the steps described under [How to Set Up Notifications About Communication System Errors](../System-Monitoring/how-to-set-up-notifications-about-communication-system-errors-835b2a2.md).





<a name="loio0d8e37f0589e4ef7a9fbbc48de4c1ea4__result_r2l_qxr_zcc"/>

## Results

You have now finished the preparation to use an integration between SAP Advanced Financial Closing and SAP Build Process Automation.

