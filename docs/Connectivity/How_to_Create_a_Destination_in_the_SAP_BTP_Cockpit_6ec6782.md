<!-- loio6ec67822497649dcaed61baf476fe3aa -->

# How to Create a Destination in the SAP BTP Cockpit

Create a destination for your SAP ERP system in your SAP BTP cockpit.



<a name="loio6ec67822497649dcaed61baf476fe3aa__prereq_vp4_h2b_5qb"/>

## Prerequisites

-   You have already completed the onboarding process as described under [Onboarding](../Onboarding/Onboarding_1987953.md).

-   To connect to your SAP ERP system, you need to have installed and configured the Cloud Connector. For more information, see [How to Install and Configure the Cloud Connector](How_to_Install_and_Configure_the_Cloud_Connector_3d19a8a.md).

-   To connect to your SAP ERP system, you require the SAP ERP connector for SAP S/4HANA Cloud for advanced financial closing. For more information, see [How to Set Up the SAP ERP Connector](How_to_Set_Up_the_SAP_ERP_Connector_b139d1e.md).

-   The SAP ERP system administrator needs to have provided you with the following information:

    -   Back-end URL for the communication system

    -   The technical communication user with the authorization objects mentioned in the SAP ERP connector for SAP S/4HANA Cloud for advanced financial closing documentation. For more information, see [Security Considerations](https://help.sap.com/viewer/c56f7dab0ed341afad9581be5651184f/latest/en-US/c552f0649acd42a7bb8638359ca82897.html).




## Procedure

1.  Open your SAP BTP cockpit.

2.  Create a destination in your SAP BTP cockpit. For more information, see [Managing Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/84e45e071c7646c88027fffc6a7bb787.html).

    Enter the following information in the destination configuration:


    <table>
    <tr>
    <th>

    Field


    
    </th>
    <th>

    What to Enter


    
    </th>
    </tr>
    <tr>
    <td>

    *Name*


    
    </td>
    <td>

    Specify a name for the destination configuration.


    
    </td>
    </tr>
    <tr>
    <td>

    *Type*


    
    </td>
    <td>

     ***HTTP*** 


    
    </td>
    </tr>
    <tr>
    <td>

    *URL*


    
    </td>
    <td>

    Enter the back-end URL of the communication system. Make sure to add the SAP client number at the end of the URL. Accordingly, the back-end URL has to have the following format:

    -   For the proxy type *OnPremise*: `http://www.example.com:[port number]**/sap/fccx?sap-client**=[client]`

    -   For the proxy type *Internet*: `https://www.example.com:[port number]**/sap/fccx?sap-client**=[client]`

    The highlighted parts are the same for all corresponding SAP ERP systems.


    
    </td>
    </tr>
    <tr>
    <td>

    *Proxy Type*


    
    </td>
    <td>

    ***OnPremise*** or ***Internet***


    
    </td>
    </tr>
    <tr>
    <td>

    *Authentication*


    
    </td>
    <td>

    ***BasicAuthentication***


    
    </td>
    </tr>
    <tr>
    <td>

    *User*


    
    </td>
    <td>

    Technical user or other authenticated user


    
    </td>
    </tr>
    <tr>
    <td>

    *Password*


    
    </td>
    <td>

    Password of the selected user


    
    </td>
    </tr>
    </table>
    



<a name="loio6ec67822497649dcaed61baf476fe3aa__result_ctp_s2b_5qb"/>

## Results

You have now created a destination for your SAP ERP system.

**Parent topicColonSymbol** [SAP ERP](SAP_ERP_7b85121.md "Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP ERP system. Perform the last step only if it applies to your use case.")

**Previous topicColonSymbol** [How to Set Up the SAP ERP Connector](How_to_Set_Up_the_SAP_ERP_Connector_b139d1e.md "If you want to connect to SAP ERP, you require the SAP ERP connector for SAP S/4HANA Cloud for advanced financial closing as additional software.")

**Next topicColonSymbol** [How to Connect to SAP ERP](How_to_Connect_to_SAP_ERP_e11be48.md "Connect to your SAP ERP system to retrieve information about organizational units, the factory calendar, and so on.")
