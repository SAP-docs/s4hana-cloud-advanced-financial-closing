<!-- loio3ba6624d4312453f8ef3106293dd6811 -->

# How to Create the Destination in the SAP BTP Cockpit

Create a destination for your SAP Build Process Automation system in your SAP BTP cockpit.



<a name="loio3ba6624d4312453f8ef3106293dd6811__prereq_bx5_mfb_5qb"/>

## Prerequisites

-   You have already completed the onboarding process as described under [Onboarding](../Onboarding/onboarding-1987953.md).

-   You have subscribed to SAP Build Process Automation and created an environment, apiKey, service instance, and service key as described under [How to Set Up the SAP Build Process Automation Integration for SAP Advanced Financial Closing](../Integration-Capabilities/how-to-set-up-the-sap-build-process-automation-integration-for-sap-advanced-financial-cl-0d8e37f.md).




## Context

For an integration for SAP Advanced Financial Closing, you need to create the following destination in the subaccount that has both subscriptions SAP Advanced Financial Closing and SAP Build Process Automation:

-   `sap_process_automation_service`: This destination is required for technical scenarios. For example, scenarios where there are no logged-in user details available, specifically in ready-to-use live process content packages such as [https://api.sap.com/package/com.sap.content.managesalesorders/](https://api.sap.com/package/com.sap.content.managesalesorders/) to invoke business rules using the decisions API or by calling workflow APIs.


For more information, see [Configure SAP Build Process Automation Destinations](https://help.sap.com/docs/build-process-automation/sap-build-process-automation/configure-sap-build-process-automation-destinations) \(SAP Build Process Automation documentation\), but keep in mind the following for an integration with SAP Advanced Financial Closing:

-   You need to create **only the one destination** `sap_process_automation_service`, not the destination `sap_process_automation_service_user_access`.
-   Destination needs to be created in the subaccount that has the subscription for SAP Advanced Financial Closing, while the environment had to be created in the subaccount that has the subscription to SAP Build Process Automation.

> ### Caution:  
> If the subscriptions for SAP Advanced Financial Closing and SAP Build Process Automation are in different subaccounts, don't use the SAP Build Process Automation booster to create the destination. The booster creates destinations in the SAP Build Process Automation subscription subaccount. If SAP Build Process Automation and SAP Advanced Financial Closing are in different subaccounts, the destination won't be accessible from SAP Advanced Financial Closing. Follow the manual configuration steps instead.



## Procedure

1.  In the SAP BTP cockpit, go to the subaccount in which you have your subscription for SAP Advanced Financial Closing.

2.  To create a destination for SAP Build Process Automation in this subaccount, choose *Connectivity* \> *Destinations*.

3.  Choose *Create Destination*.

4.  Choose *Blank Template* and enter the following details using the values from the SAP Build Process Automation service key you've just created as described under [How to Set Up the SAP Build Process Automation Integration for SAP Advanced Financial Closing](../Integration-Capabilities/how-to-set-up-the-sap-build-process-automation-integration-for-sap-advanced-financial-cl-0d8e37f.md):


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Value
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Name*
    
    </td>
    <td valign="top">
    
    Enter a name for the destination. You'll reference this name when setting up the communication system in SAP Advanced Financial Closing.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Type*
    
    </td>
    <td valign="top">
    
    `HTTP`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Proxy Type*
    
    </td>
    <td valign="top">
    
    `Internet`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Authentication*
    
    </td>
    <td valign="top">
    
    `OAuth2ClientCredentials`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *URL*
    
    </td>
    <td valign="top">
    
    Value of `endpoints.api` from the service key
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Client ID*
    
    </td>
    <td valign="top">
    
    Value of `uaa.clientid` from the service key
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Client Secret*
    
    </td>
    <td valign="top">
    
    Value of `uaa.clientsecret` from the service key
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Token Service URL*
    
    </td>
    <td valign="top">
    
    Value of `uaa.url` from the service key, followed by `/oauth/token`
    
    </td>
    </tr>
    </table>
    
    > ### Remember:  
    > Only this destination is required for the SAP Advanced Financial Closing integration. The second destination described in the SAP Build Process Automation documentation \(`sap_process_automation_service_user_access` with authentication type `OAuth2JWTBearer`\) isn't required and doesn't need to be created for the SAP Advanced Financial Closing integration.

5.  Choose *Save*.

6.  To check the availability of the destination connection, choose *Check Connection*.




<a name="loio3ba6624d4312453f8ef3106293dd6811__result_jlm_sfb_5qb"/>

## Results

You have now created a destination for your SAP Build Process Automation system.



## Next Steps

Connect to your SAP Build Process Automation system as a communication system as described under [How to Connect to an SAP Build Process Automation System as a Communication System](how-to-connect-to-an-sap-build-process-automation-system-as-a-communication-system-9de0a5c.md).

**Parent topic:**[SAP Build Process Automation](sap-build-process-automation-7385663.md "Perform the following steps to connect SAP Advanced Financial Closing to your SAP Build Process Automation system.")

**Previous:**[How to Connect to an SAP Build Process Automation System as a Communication System](how-to-connect-to-an-sap-build-process-automation-system-as-a-communication-system-9de0a5c.md "Connect to your SAP Build Process Automation system to include workflows from SAP Build Process Automation in your financial close in SAP Advanced Financial Closing.")

