<!-- loioe11be48cbd964724bb052f58729eb88c -->

# How to Connect to SAP ERP

Connect to your SAP ERP system to retrieve information about organizational units, the factory calendar, and so on.



<a name="loioe11be48cbd964724bb052f58729eb88c__prereq_lrk_shn_sjb"/>

## Prerequisites

-   You have already completed the onboarding process as described under [Onboarding](../Onboarding/Onboarding_1987953.md).

-   Your user must have a role collection assigned that includes the role template `AFC_SystemAdmin`.

    For more information about role templates, see [How to Manage Static Role Templates](../User_Management/How_to_Manage_Static_Role_Templates_0cca34d.md).

-   To connect to your SAP ERP system, you need to have installed and configured the Cloud Connector. For more information, see [How to Install and Configure the Cloud Connector](How_to_Install_and_Configure_the_Cloud_Connector_3d19a8a.md).

-   To connect to your SAP ERP system, you require the SAP ERP connector for SAP S/4HANA Cloud for advanced financial closing. For more information, see [How to Set Up the SAP ERP Connector](How_to_Set_Up_the_SAP_ERP_Connector_b139d1e.md).

-   The SAP ERP system administrator needs to have provided you with the following information:

    -   Back-end URL for the communication system

    -   The technical communication user with the authorization objects mentioned in the SAP ERP connector for SAP S/4HANA Cloud for advanced financial closing documentation. For more information, see [Security Considerations](https://help.sap.com/viewer/c56f7dab0ed341afad9581be5651184f/latest/en-US/c552f0649acd42a7bb8638359ca82897.html).


-   The destination in the SAP BTP cockpit has already been created as described under [How to Create a Destination in the SAP BTP Cockpit](How_to_Create_a_Destination_in_the_SAP_BTP_Cockpit_6ec6782.md).




<a name="loioe11be48cbd964724bb052f58729eb88c__steps_bwt_shn_sjb"/>

## Procedure

1.  In SAP S/4HANA Cloud for advanced financial closing, go to the *Specify Communication Systems* app.

2.  Enter the following information:


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

    *Name of Destination Configuration*


    
    </td>
    <td valign="top">

    Enter the name of the destination configuration that was configured in the SAP BTP cockpit.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *UI Domain*


    
    </td>
    <td valign="top">

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
    <td valign="top">

    *UI Endpoint* \(mandatory for communication systems that have an SAP Fiori launchpad\)


    
    </td>
    <td valign="top">

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
    <td valign="top">

    *UI Parameters* \(optional\)


    
    </td>
    <td valign="top">

    Enter the UI parameters that are to be applied for the connection with the communication system.

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
    <td valign="top">

    *Is Production System*


    
    </td>
    <td valign="top">

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

3.  Save.

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
    >     -   If no entries are displayed, the connection doesn't work properly. Perform the steps described for issues with the connection to the communication system under [Error Handling](../Monitoring_and_Troubleshooting/Error_Handling_e5eb3d8.md).




<a name="loioe11be48cbd964724bb052f58729eb88c__result_lw2_q15_plb"/>

## Results

The following data in advanced financial closing is synchronized daily with the connected system:


<table>
<tr>
<th valign="top">

Business Configuration



</th>
<th valign="top">

Master Data



</th>
</tr>
<tr>
<td valign="top">

Task model types



</td>
<td valign="top">

Accounting principles



</td>
</tr>
<tr>
<td valign="top">

Task list models



</td>
<td valign="top">

Factory calendars



</td>
</tr>
<tr>
<td valign="top">

Folder models



</td>
<td valign="top">

Fiscal year variants



</td>
</tr>
<tr>
<td valign="top">

Task models



</td>
<td valign="top">

Ledgers



</td>
</tr>
<tr>
<td valign="top">

Task dependencies



</td>
<td valign="top">

Organizational units



</td>
</tr>
<tr>
<td valign="top">

Assignment of tasks to country/region



</td>
<td valign="top">

Parameters



</td>
</tr>
<tr>
<td valign="top">

Assignments of tasks to folder



</td>
<td valign="top">

Task parameters



</td>
</tr>
</table>

> ### Note:  
> Only consistent data is synchronized. If data is deleted in your communication system, it will also be deleted in advanced financial closing with the next synchronization. This means that the deleted data can't be used for new task list templates or task lists, and their referenced objects.
> 
> If needed, check the business logs for more information as described under [Logging](../Monitoring_and_Troubleshooting/Logging_57375b8.md).



<a name="loioe11be48cbd964724bb052f58729eb88c__postreq_u1n_gfq_jpb"/>

## Next Steps

You have two options for the initial data synchronization with the communication system: You can trigger **immediate synchronization** using the *Synchronize Now* option in the *Specify Communication Systems* app. If you don't use this option, the communication system will still be synchronized during **daily synchronization**.

**Parent topic:** [SAP ERP](SAP_ERP_7b85121.md "Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP ERP system. Perform the last step only if it applies to your use case.")

**Next:** [How to Create a Destination in the SAP BTP Cockpit](How_to_Create_a_Destination_in_the_SAP_BTP_Cockpit_6ec6782.md "Create a destination for your SAP ERP system in your SAP BTP cockpit.")

**Previous:** [How to Configure Local Settings in Communication Systems](How_to_Configure_Local_Settings_in_Communication_Systems_3e2c737.md "Configure your local settings for better use with advanced financial closing.")

**Related Information**  


[Authorization Handling During System Communication](../Security/Authorization_Handling_During_System_Communication_c310348.md "Authorization handling during communication with an on-premise system.")

