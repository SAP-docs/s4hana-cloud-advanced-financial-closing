<!-- loio0d8e37f0589e4ef7a9fbbc48de4c1ea4 -->

# How to Set Up the SAP Build Process Automation Integration for SAP Advanced Financial Closing

Set up an integration with SAP Build Process Automation to use SAP Advanced Financial Closing to trigger workflows.



<a name="loio0d8e37f0589e4ef7a9fbbc48de4c1ea4__prereq_nqx_p4r_zcc"/>

## Prerequisites

-   For the steps to be performed with regards to or in SAP Build Process Automation, you need to have the required authorization.
-   For the steps to be performed in SAP Advanced Financial Closing, the following authorizations are required:
    -   Your user must have a role collection assigned that includes one of the following role templates:

        -   `AFC_SystemAdmin`

        -   `AFC_SpecifySystemsApp`


        For more information about role templates, see [How to Manage Static Role Templates](../User-Management/how-to-manage-static-role-templates-0cca34d.md) and [Static Roles for SAP Advanced Financial Closing](../User-Management/static-roles-for-sap-advanced-financial-closing-b92a241.md).





## Context

In SAP Build Process Automation, you can create workflows to perform specific steps, providing conditions and events and a lot more. You can set up an integration between SAP Build Process Automation and SAP Advanced Financial Closing to use SAP Advanced Financial Closing to trigger these workflows. After processing, the status of the workflow is then reported back to SAP Advanced Financial Closing. This way, you can fully integrate workflows into your financial close and use SAP Advanced Financial Closing to trigger them automatically and receive results, and apply an approval process.



## Procedure

1.  If not done yet, subscribe to SAP Build Process Automation as described under [Subscribe to SAP Build Process Automation](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/subscribe-to-sap-build-process-automation) \(SAP Build Process Automation documentation\).

2.  In the subaccount in which you have **your subscription for SAP Build Process Automation**, create a service instance for SAP Build Process Automation. For more information, see [Create a Service Instance](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/create-service-instance) \(SAP Build Process Automation documentation\).

    > ### Restriction:  
    > The use of the parameters `environmentId` and `apiKey` currently isn't possible in the way it's described in the linked documentation. For the time being, leave the field under *Or specify the parameters in JSON format* empty and simply choose *Next*.

3.  In the subaccount in which you have **your subscription for SAP Build Process Automation**, create a service key based on the service instance you've just created. For more information, see [Create a Service Key for the SAP Build Process Automation Instance](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/create-service-key-for-sap-build-process-automation-instance) \(SAP Build Process Automation documentation\).

4.  In the subaccount in which you have **your subscription for SAP Advanced Financial Closing**, create a destination for SAP Build Process Automation based on the service key you've just created. For more information, see [Configure SAP Build Process Automation Destinations](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/configure-sap-build-process-automation-destinations) \(SAP Build Process Automation documentation\).


**Setting up a communication system in SAP Advanced Financial Closing**

5.  In SAP Advanced Financial Closing, go to the *Specify Communication Systems* app.

6.  Choose *Create* \> *Create SAP Build Process Automation System* in the table toolbar.

    > ### Note:  
    > This communication system can't be added to task list templates. To add workflows to a task list template, the communication system in which the workflow is processed needs to be added to the template.

7.  Enter the following information:

    1.  *Name*:

        Enter a name for the communication system.

    2.  *System URL*:

        Enter the UI URL of your SAP Build Process Automation application. The URL follows a specific pattern: `https://<subdomain>.<landscape>.build.cloud.sap`.

        > ### Example:  
        > The subdomain of your subaccount is **`example-company`**.
        > 
        > Your SAP Build Process Automation application is in the landscape **`EU10`**.
        > 
        > **Result:** Your UI URL is **`https://example-company.eu10.build.cloud.sap`**.


8.  Save.

9.  Verify that the system URL entered is correct by choosing the *Open SAP Build Process Automation* button in the *SAP Build Process Automation* section.

10. Check whether the connection between SAP Advanced Financial Closing and SAP Build Process Automation works by choosing the *Check Connection* button in the header bar.

11. **Optional:** Under *Notifications*, you can set up notifications about system errors. Follow the steps described under [How to Set Up Notifications About Communication System Errors](../System-Monitoring/how-to-set-up-notifications-about-communication-system-errors-835b2a2.md).


**Creating workflows in SAP Build Process Automation**

12. If not done yet, create workflows in SAP Build Process Automation that you want to include into your financial close managed in SAP Advanced Financial Closing. For information on how to do this, see [How to Create Workflows in SAP Build Process Automation and Integrate Them into the Financial Close](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/SHIP/en-US/24599e4d0fab4d0d9633d0024e89cb4f.html "Set up workflows in SAP Build Process Automation that can then be triggered by SAP Advanced Financial Closing.") :arrow_upper_right:.

    > ### Tip:  
    > The authorizations required for steps in SAP Build Process Automation are described under [Authorizations](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/authorizations) \(SAP Build Process Automation documentation\).

    > ### Caution:  
    > SAP Advanced Financial Closing currently doesn't support arrays, relative dates, or custom data types for parameters of workflows in SAP Build Process Automation.




<a name="loio0d8e37f0589e4ef7a9fbbc48de4c1ea4__result_r2l_qxr_zcc"/>

## Results

You have now finished the preparation to use an integration between SAP Advanced Financial Closing and SAP Build Process Automation.

