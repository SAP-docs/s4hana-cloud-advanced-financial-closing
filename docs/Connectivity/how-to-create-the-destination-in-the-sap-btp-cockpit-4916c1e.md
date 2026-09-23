<!-- loio4916c1ea4a654ee9baf076f0d4e7cb52 -->

# How to Create the Destination in the SAP BTP Cockpit

Create a destination for your external system in your SAP BTP cockpit.



<a name="loio4916c1ea4a654ee9baf076f0d4e7cb52__prereq_bx5_mfb_5qb"/>

## Prerequisites

-   You have already completed the onboarding process as described under [Onboarding](../Onboarding/onboarding-1987953.md).
-   You have prepared the integration of your external system with SAP Advanced Financial Closing as described on these pages:

    -   [Integration with External Systems](../Integration-Capabilities/integration-with-external-systems-90573ae.md)
    -   [How to Set Up an Integration with an External System for SAP Advanced Financial Closing](../Integration-Capabilities/how-to-set-up-an-integration-with-an-external-system-for-sap-advanced-financial-closing-6db4864.md)

    .




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
    
    Enter the back-end URL of the external communication system.

    `<URL_OF_EXTERNAL_SYSTEM>`

    > ### Note:  
    > Systems with proxy type *Internet* must start with `https://`.
    > 
    > Systems with proxy type *OnPremise* must start with `http://`.
    > 
    > The proxy type is explained in the next row just below.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Proxy Type*
    
    </td>
    <td valign="top">
    
    -   `Internet`
    -   `OnPremise` \(for external on-premise systems only\)


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Authentication*
    
    </td>
    <td valign="top">
    
    Choose the authentication type of your communication system.

    > ### Note:  
    > `NO_AUTH` **is not** supported.


    
    </td>
    </tr>
    </table>
    



<a name="loio4916c1ea4a654ee9baf076f0d4e7cb52__result_jlm_sfb_5qb"/>

## Results

You have now created a destination for your external system.

**Parent topic:**[External Systems](external-systems-9ca3083.md "Connect to your external financial system to retrieve information about organizational units, the factory calendar, and so on.")

**Next:**[How to Install and Configure the Cloud Connector for On-Premise Systems](how-to-install-and-configure-the-cloud-connector-for-on-premise-systems-13b0b26.md "If you want to connect to an external on-premise system, you need to install and configure the Cloud Connector as additional software.")

**Previous:**[How to Connect to a External System as a Communication System](how-to-connect-to-a-external-system-as-a-communication-system-ea13039.md "Connect to your external system to retrieve information about organizational units, the factory calendar, and so on.")

