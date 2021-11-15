<!-- loio5c2b2f088a4f4fb0bb4921815264a167 -->

# How to Create a Destination in the SAP BTP Cockpit

Create a destination for your SAP S/4HANA system in your SAP BTP cockpit.



<a name="loio5c2b2f088a4f4fb0bb4921815264a167__prereq_ew2_4r1_5qb"/>

## Prerequisites

-   You have already completed the onboarding process as described under [Onboarding](../Onboarding/Onboarding_1987953.md).

-   You need to have installed and configured the Cloud Connector. For more information, see [How to Install and Configure the Cloud Connector](How_to_Install_and_Configure_the_Cloud_Connector_4cf0fb0.md).

-   The SAP S/4HANA system administrator needs to have enabled OData services in SAP S/4HANA, see [How to Enable OData Services in SAP S/4HANA](How_to_Enable_OData_Services_in_SAP_S4HANA_fb5fe06.md).

-   The SAP S/4HANA system administrator needs to have provided you with the following information:

    -   Back-end URL for the communication system

    -   The technical communication user that was created as described under [How to Create a Technical Communication User](How_to_Create_a_Technical_Communication_User_c4a9b51.md).

    -   Password of the selected user





## Procedure

1.  Open your SAP BTP cockpit.

2.  Create a destination. For more information, see [Managing Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/84e45e071c7646c88027fffc6a7bb787.html).

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

     ***HTTP*** 


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *URL*


    
    </td>
    <td valign="top">

    Enter the back-end URL of the communication system that you've received from the , go to the SAP S/4HANA, go system administrator. Make sure to add the SAP client number at the end of the URL. Accordingly, the back-end URL has to have the following format:

    `http://www.example.com:[port number]**/sap/opu/odata/sap/fccx\_communication\_services\_srv?sap-client**=[client]`

    The highlighted part is the same for all SAP S/4HANA systems.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Proxy Type*


    
    </td>
    <td valign="top">

    ***OnPremise*** 


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Authentication*


    
    </td>
    <td valign="top">

    ***BasicAuthentication***


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *User*


    
    </td>
    <td valign="top">

    Technical communication user that you've received from the SAP S/4HANA system administrator.


    
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
    



<a name="loio5c2b2f088a4f4fb0bb4921815264a167__result_fsc_1s1_5qb"/>

## Results

You have now created a destination for your SAP S/4HANA system.

**Parent topic:** [SAP S/4HANA](SAP_S4HANA_15a3a5b.md "Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP S/4HANA system. Perform the last two steps only if they apply to your use case.")

**Next:** [How to Create a Technical Communication User](How_to_Create_a_Technical_Communication_User_c4a9b51.md "Create a technical communication user for your SAP S/4HANA system.")

**Previous:** [How to Connect to SAP S/4HANA](How_to_Connect_to_SAP_S4HANA_34ec755.md "Connect to SAP S/4HANA as your financial communication system to retrieve information about organizational units, the factory calendar, and so on.")

