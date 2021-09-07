<!-- loio34ec75546e6842f98fb0c31f889f8603 -->

# How to Connect to SAP S/4HANA

Connect to SAP S/4HANA as your financial communication system to retrieve information about organizational units, the factory calendar, and so on.



<a name="loio34ec75546e6842f98fb0c31f889f8603__prereq_nlf_jzq_4lb"/>

## Prerequisites

-   You have already completed the onboarding process as described under [Onboarding](../Onboarding_1987953.md).

-   Your user must have a role collection assigned that includes the role template `AFC_SystemAdmin`.

    For more information about role templates, see [User Management](../User_Management_ae7fa30.md).

-   You need to have installed and configured the Cloud Connector. For more information, see [How to Install and Configure the Cloud Connector](How_to_Install_and_Configure_the_Cloud_Connector_4cf0fb0.md).

-   The SAP S/4HANA system administrator needs to have enabled OData services in SAP S/4HANA, see [How to Enable OData Services in SAP S/4HANA](How_to_Enable_OData_Services_in_SAP_S4HANA_fb5fe06.md).

-   The SAP S/4HANA system administrator needs to have provided you with the following information:

    -   Back-end URL for the communication system

    -   The technical communication user that was created as described under [How to Create a Technical Communication User](How_to_Create_a_Technical_Communication_User_c4a9b51.md).

    -   Password of the selected user




<a name="loio34ec75546e6842f98fb0c31f889f8603__steps_bwt_shn_sjb"/>

## Procedure

1.  Create a destination in your SAP BTP cockpit. For more information, see [Managing Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/84e45e071c7646c88027fffc6a7bb787.html).

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

    Enter the back-end URL of the communication system that you've received from the , go to the SAP S/4HANA, go system administrator. Make sure to add the SAP client number at the end of the URL. Accordingly, the back-end URL has to have the following format:

    `http://www.example.com:[port number]**/sap/opu/odata/sap/fccx\_communication\_services\_srv?sap-client**=[client]`

    The highlighted part is the same for all SAP S/4HANA systems.


    
    </td>
    </tr>
    <tr>
    <td>

    *Proxy Type*


    
    </td>
    <td>

    ***OnPremise*** 


    
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

    Technical communication user that you've received from the SAP S/4HANA system administrator.


    
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
    
2.  In SAP S/4HANA Cloud for advanced financial closing, go to the *Specify Communication Systems* app.

3.  Enter the following information:


    <table>
    <tr>
    <th>

    Field


    
    </th>
    <th>

    Description


    
    </th>
    </tr>
    <tr>
    <td>

    *Name*


    
    </td>
    <td>

    Enter a name for the communication system.


    
    </td>
    </tr>
    <tr>
    <td>

    *Name of Destination Configuration*


    
    </td>
    <td>

    Enter the name of the destination configuration you've just configured in the SAP BTP cockpit.


    
    </td>
    </tr>
    <tr>
    <td>

    *UI Domain*


    
    </td>
    <td>

    Enter the domain of the SAP Fiori launchpad gateway of your target communication system via which users can access the app UI.

    To get this domain, open the SAP Fiori launchpad of your communication system, copy only the domain, and paste it in the *UI Domain* field.

    > ### Example:  
    > Given the complete URL is as follows:
    > 
    > `https://mylaunchpad.mycompany.corp/sap/bc/ui5_ui5/ui2/ushell/shells/abap/FioriLaunchpad.html?sap-language=en&sap-client=230#Shell-home/`
    > 
    > Then the UI domain is as follows: `https://mylaunchpad.mycompany.corp`

    The UI domain is therefore the first part of the URL of the communication system.


    
    </td>
    </tr>
    <tr>
    <td>

    *UI Endpoint* \(mandatory for communication systems that have an SAP Fiori launchpad\)


    
    </td>
    <td>

    Enter the UI endpoint for the SAP Fiori launchpad of your communication system.

    > ### Example:  
    > Given the complete URL is as follows:
    > 
    > `https://mylaunchpad.mycompany.corp/sap/bc/ui5_ui5/ui2/ushell/shells/abap/FioriLaunchpad.html?sap-language=en&sap-client=230#Shell-home/`
    > 
    > Then the UI endpoint is as follows:`/sap/bc/ui5_ui5/ui2/ushell/shells/abap/FioriLaunchpad.html`

    > ### Note:  
    > The default entry is `/sap/bc/ui2/flp`.
    > 
    > You can overwrite this entry. However, consider the following formatting rules:
    > 
    > -   Entry has to start with /
    > 
    > -   Entry can't end with /

    The UI endpoint is later added to the URL of the communication system after the UI domain.


    
    </td>
    </tr>
    <tr>
    <td>

    *UI Parameters* \(optional\)


    
    </td>
    <td>

    Enter the UI parameters that should be applied for the connection with the communication system.

    > ### Example:  
    > Given the complete URL is as follows:
    > 
    > `https://mylaunchpad.mycompany.corp/sap/bc/ui5_ui5/ui2/ushell/shells/abap/FioriLaunchpad.html?sap-language=en&sap-client=230#Shell-home/`
    > 
    > Then the UI parameters are as follows: `sap-language=en&sap-client=230`

    Enter only the parameters in the format shown in the example without any additional characters.

    The UI parameters are later added to the URL of the communication system after the UI endpoint.


    
    </td>
    </tr>
    <tr>
    <td>

    *Is Production System*


    
    </td>
    <td>

    Decide whether the communication system you want to connect to is a test system or a production system. ***Yes*** indicates that the communication system contains production data, which thereby makes all related task lists potentially relevant to auditing and data retention.

    The default value is ***Yes***.

    > ### Note:  
    > Define a communication system as a production system to prevent the untimely deletion of related task lists.


    
    </td>
    </tr>
    </table>
    
    > ### Tip:  
    > For systems that have an SAP Fiori launchpad, you can check whether the UI domain, UI endpoint, and possibly UI parameters are correct and lead to the correct URL. Choose *Open Target SAP Fiori Launchpad*. If the settings are correct, you're directed to the SAP Fiori launchpad of your communication system.

    > ### Tip:  
    > You can check whether the connection with the communication system works as expected. Choose *Check Connection to Destination*. This will check whether the back-end connection works and whether the system communicates as expected.

4.  Save.

    > ### Tip:  
    > You can check whether the connection you set up works:
    > 
    > 1.  After the first synchronization, go to the *Define Closing Tasks* app.
    > 
    > 2.  Create a template.
    > 
    > 3.  Under *Communication System*, enter the corresponding system.
    > 
    > 4.  Open the value help for the *Ledger* or *Factory Calendar ID* field.
    > 
    >     **Results**:
    > 
    >     -   If entries are displayed, the connection works. Exit the value help and choose *Cancel* to cancel template creation.
    > 
    >     -   If no entries are displayed, the connection doesn't work properly. Perform the steps described for issues with the connection to the communication system under [Error Handling](../Error_Handling_e5eb3d8.md).




<a name="loio34ec75546e6842f98fb0c31f889f8603__result_djr_2d5_plb"/>

## Results

The following data in advanced financial closing is synchronized daily with the connected system:


<table>
<tr>
<th>

Business Configuration



</th>
<th>

Master Data



</th>
</tr>
<tr>
<td>

Task model types



</td>
<td>

Accounting principles



</td>
</tr>
<tr>
<td>

Task list models



</td>
<td>

Factory calendars



</td>
</tr>
<tr>
<td>

Folder models



</td>
<td>

Fiscal year variants



</td>
</tr>
<tr>
<td>

Task models



</td>
<td>

Ledgers



</td>
</tr>
<tr>
<td>

Task dependencies



</td>
<td>

Organizational units



</td>
</tr>
<tr>
<td>

Assignment of tasks to country/region



</td>
<td>

Parameters



</td>
</tr>
<tr>
<td>

Assignments of tasks to folder



</td>
<td>

Task parameters



</td>
</tr>
</table>

> ### Note:  
> Only consistent data is synchronized. If data is deleted in your communication system, it will also be deleted in advanced financial closing with the next synchronization. This means that the deleted data can't be used for new task list templates or task lists, and their referenced objects.
> 
> If needed, check the business logs for more information as described under [Logging](../Logging_57375b8.md).



<a name="loio34ec75546e6842f98fb0c31f889f8603__postreq_erd_jfq_jpb"/>

## Next Steps

You have two options for the initial data synchronization with the communication system: You can trigger **immediate synchronization** using the *Synchronize Now* option in the *Specify Communication Systems* app. If you don't use this option, the communication system will still be synchronized during **daily synchronization**.

**Related Information**  


[Authorization Handling During System Communication](../Security/Authorization_Handling_During_System_Communication_c310348.md "Authorization handling during communication with an on-premise system.")
