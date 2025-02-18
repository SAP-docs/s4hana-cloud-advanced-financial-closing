<!-- loio6e944094643a43c48e0230081880ddb0 -->

# How to Create a Destination in the SAP BTP Cockpit

Create a destination for your SAP S/4HANA Cloud Public Edition system in your SAP BTP cockpit.



<a name="loio6e944094643a43c48e0230081880ddb0__prereq_bx5_mfb_5qb"/>

## Prerequisites

-   You have already completed the onboarding process as described under [Onboarding](../Onboarding/onboarding-1987953.md).

-   The SAP S/4HANA Cloud Public Edition system administrator needs to have completed the set-up instructions as described under [How to Set Up the Integration of Financial Task List Management](how-to-set-up-the-integration-of-financial-task-list-management-24140e9.md).




## Procedure

1.  Open your SAP BTP cockpit.

2.  Create a destination in your SAP BTP cockpit. For more information, see [Managing Destinations](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/84e45e071c7646c88027fffc6a7bb787.html).

    Enter the following information in the destination configuration:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    What to Enter
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Name*
    
    </td>
    <td valign="top">
    
    Specify a name for the destination configuration.
    
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
    
    *URL*
    
    </td>
    <td valign="top">
    
    Enter the back-end URL of the communication system. Make sure to add the SAP client number at the end of the URL. Accordingly, the back-end URL has to have the following format:

    <code>https://www.example.com:[port number]<b>/sap/opu/odata/sap/fccx_communication_services_srv?sap-client=100</b></code>

    The highlighted part is the same for all SAP S/4HANA Cloud Public Edition systems.
    
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
    
    `BasicAuthentication`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *User*
    
    </td>
    <td valign="top">
    
    Technical communication user that you've received from the SAP S/4HANA Cloud Public Edition system administrator.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Password*
    
    </td>
    <td valign="top">
    
    Password of the selected user
    
    </td>
    </tr>
    </table>
    



<a name="loio6e944094643a43c48e0230081880ddb0__result_jlm_sfb_5qb"/>

## Results

You have now created a destination for your SAP S/4HANA Cloud Public Edition system.

