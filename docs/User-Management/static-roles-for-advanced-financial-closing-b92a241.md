<!-- loiob92a2411e4164270964903c502e22340 -->

# Static Roles for Advanced Financial Closing

Static roles enable users to see the affected apps on their SAP Fiori launchpad.



## Available Role Templates

> ### Note:  
> Some role templates have a corresponding **display-only** role template, which grants access to the same app but with restricted authorizations. In general, the display-only role templates allow users to view and export information, but not to create, upload, edit, or delete any information.
> 
> For detailed information, see the corresponding columns in the following table.

<a name="loiob92a2411e4164270964903c502e22340__d17e1053"/>Role Templates


<table>
<tr>
<th valign="top">

Role Template



</th>
<th valign="top">

Description



</th>
<th valign="top">

Tiles on SAP Fiori Launchpad



</th>
<th valign="top">

Display-Only Role Template



</th>
<th valign="top">

Description for Display-Only Role



</th>
</tr>
<tr>
<td valign="top">

 `AFC_SystemAdmin` 



</td>
<td valign="top">

-   Maintains solution-specific settings, for example, a connection to financial communication systems

-   Adapts the UI of apps for customer-specific use \(additionally, the role template `FlexKeyUser` is needed\).

    For more information about UI adaptation, see [Adapting the UI](https://help.sap.com/docs/BTP/3d99fdeadde04524bdd33d35f1e13777/d868950a1e8c4b0f9b9453176939a19b.html?locale=en-US) in the SAP Fiori Launchpad documentation.

-   Monitors system statuses and tackles any issues with connected systems \(additionally, the role template `Business_Process_Specialist_BL_AccessAll` is needed\)

-   Creates public view variants \(additionally, the role template `FlexKeyUser` is needed\).

    For more information, see [How to Share View Variants](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/SHIP/en-US/2fee7b5a83294d748953a9db5cc96326.html "Share your view variants with other users.") :arrow_upper_right:.




</td>
<td valign="top">

System administration:

-   *Manage Users*
-   *Specify Communication Systems*
-   *Monitor Communication Systems*



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_SpecifySystemsApp` 



</td>
<td valign="top">

Maintains connections to financial communication systems



</td>
<td valign="top">

-   *Specify Communication Systems*



</td>
<td valign="top">

`AFC_SpecifySystemsApp_Display`



</td>
<td valign="top">

-   Views and exports system information

-   Views and exports in-app change logs

-   Checks the connection of communication systems

-   **Cannot** maintain, edit, or synchronize communication systems

-   **Cannot** delete the connection to communication systems




</td>
</tr>
<tr>
<td valign="top">

 `AFC_MonitorSystemsApp` 



</td>
<td valign="top">

-   Monitors system statuses

-   Tackles issues with connected systems


To be able to view synchronization logs, a user additionally requires role template `Business_Process_Specialist_BL_AccessAll`.



</td>
<td valign="top">

-   *Monitor Communication Systems*



</td>
<td valign="top">

`AFC_MonitorSystemsApp_Display`



</td>
<td valign="top">

-   Views and exports system information

-   Checks the connection of communication systems

-   **Cannot** synchronize communication systems




</td>
</tr>
<tr>
<td valign="top">

 `AFC_Migration` 



</td>
<td valign="top">

Migrates data if a migration from SAP S/4HANA Cloud for advanced financial closing as part of SAP S/4HANA Cloud to the SAP BTP solution takes place.



</td>
<td valign="top">

-   *Migrate Configuration Data*
-   *Migrate Closing Task Lists*



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_Compliance` 



</td>
<td valign="top">

Maintains general compliance settings



</td>
<td valign="top">

-   *Manage Compliance Settings*



</td>
<td valign="top">

`AFC_Compliance_Display`



</td>
<td valign="top">

-   Views compliance settings

-   Views and exports in-app change logs

-   **Cannot** change compliance settings




</td>
</tr>
<tr>
<td valign="top">

 `AFC_UserAdmin` 



</td>
<td valign="top">

-   Maintains users and the assignments between users and roles.

-   Maintains user groups




</td>
<td valign="top">

-   *Manage Users*
-   *Manage User Role Assignments*
-   *Manage User Groups* \(Configuration\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_Config` 



</td>
<td valign="top">

Maintains application-specific data, for example, configuration settings, or master data



</td>
<td valign="top">

-   *Manage Authorization Groups* \(Configuration\)
-   *Manage Country/Region Groups* \(Configuration\)
-   *Manage Email Notification Configurations* \(Configuration\)
-   *Manage User Groups* \(Configuration\)
-   *Manage User Roles* \(Configuration\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_Settings` 



</td>
<td valign="top">

Maintains application-specific settings, such as notifications and country/region groups



</td>
<td valign="top">

-   *Manage Country/Region Groups* \(Configuration\)
-   *Manage Email Notification Configurations* \(Configuration\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_UserRoles` 



</td>
<td valign="top">

Maintains user roles and authorization groups



</td>
<td valign="top">

-   *Manage User Roles* \(Configuration\)
-   *Manage Authorization Groups* \(Configuration\)



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_AuthGroupsApp` 



</td>
<td valign="top">

Maintains authorization groups



</td>
<td valign="top">

-   *Manage Authorization Groups* \(Configuration\)



</td>
<td valign="top">

`AFC_AuthGroupsApp_Display`



</td>
<td valign="top">

-   Views and exports authorization group information

-   Views and exports in-app change logs

-   **Cannot** create, edit, or delete authorization groups




</td>
</tr>
<tr>
<td valign="top">

 `AFC_CountryGroupsApp` 



</td>
<td valign="top">

Maintains country/region groups



</td>
<td valign="top">

-   *Manage Country/Region Groups* \(Configuration\)



</td>
<td valign="top">

`AFC_CountryGroupsApp_Display`



</td>
<td valign="top">

-   Views and exports country/region group information

-   Views and exports in-app change logs

-   **Cannot** create, edit, or delete country/region groups




</td>
</tr>
<tr>
<td valign="top">

 `AFC_NotificationsApp` 



</td>
<td valign="top">

Maintains email notification configurations



</td>
<td valign="top">

-   *Manage Email Notification Configurations* \(Configuration\)



</td>
<td valign="top">

`AFC_NotificationsApp_Display`



</td>
<td valign="top">

-   Views and exports information about email notification configurations

-   Views and exports in-app change logs

-   **Cannot** create, edit, or delete email notification configurations




</td>
</tr>
<tr>
<td valign="top">

 `AFC_UserGroupsApp` 



</td>
<td valign="top">

Maintains user groups



</td>
<td valign="top">

-   *Manage User Groups* \(Configuration\)



</td>
<td valign="top">

`AFC_UserGroupsApp_Display`



</td>
<td valign="top">

-   Views and exports user group information

-   Views and exports in-app change logs

-   **Cannot** upload, create, edit, or delete user groups

-   **Cannot** upload user-to-group assignments

-   **Cannot** download the template for user-to-group assignment creation




</td>
</tr>
<tr>
<td valign="top">

 `AFC_UserRolesSingleApp` 



</td>
<td valign="top">

Maintains user roles



</td>
<td valign="top">

-   *Manage User Roles* \(Configuration\)



</td>
<td valign="top">

`AFC_UserRolesSingleApp_Display`



</td>
<td valign="top">

-   Views and exports user role information

-   Views and exports in-app change logs

-   **Cannot** create, edit, or delete user roles




</td>
</tr>
<tr>
<td valign="top">

 `AFC_ManageUsersApp` 



</td>
<td valign="top">

Maintains and deletes users



</td>
<td valign="top">

-   *Manage Users*



</td>
<td valign="top">

`AFC_ManageUsersApp_Display`



</td>
<td valign="top">

-   Views and exports user information

-   Views and exports in-app change logs

-   **Cannot** upload, edit, or delete users

-   **Cannot** download the template for user creation




</td>
</tr>
<tr>
<td valign="top">

 `AFC_UserManagement` 



</td>
<td valign="top">

Maintains assignments between user and roles



</td>
<td valign="top">

-   *Manage User Role Assignments*



</td>
<td valign="top">

`AFC_UserManagement_Display`



</td>
<td valign="top">

-   Views and exports user-to-role assignment information

-   Views and exports in-app change logs

-   **Cannot** upload, edit, or delete user-to-role assignments

-   **Cannot** download the template for user-to-role assignment creation




</td>
</tr>
<tr>
<td valign="top">

 `AFC_Define` 



</td>
<td valign="top">

Maintains task list templates and task lists



</td>
<td valign="top">

-   *Manage Closing Task Lists*
-   *Change Log*



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_Process` 



</td>
<td valign="top">

Processes task lists and tasks



</td>
<td valign="top">

-   *Process Closing Tasks*
-   *Change Log*



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_Approve` 



</td>
<td valign="top">

Approves tasks



</td>
<td valign="top">

-   *Approve Closing Tasks*
-   *Change Log*



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_Reporting` 



</td>
<td valign="top">

Monitors overall progress of closing activities and tracks task completion



</td>
<td valign="top">

-   *Financial Close Overview*
-   *Closing Task Completion*



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `Business_Process_Specialist_BL_AccessAll` 



</td>
<td valign="top">

Reviews logs as an administrator



</td>
<td valign="top">

-   *Monitor Business Logs*



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `AFC_KeyUser` 



</td>
<td valign="top">

-   Adapts the UI of apps for customer-specific use \(additionally, the role template `FlexKeyUser` is needed\).

    For more information about UI adaptation, see [Adapting the UI](https://help.sap.com/docs/BTP/3d99fdeadde04524bdd33d35f1e13777/d868950a1e8c4b0f9b9453176939a19b.html?locale=en-US) in the SAP Fiori Launchpad documentation.

-   Creates public view variants \(additionally, the role template `FlexKeyUser` is needed\).

    For more information, see [How to Share View Variants](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/SHIP/en-US/2fee7b5a83294d748953a9db5cc96326.html "Share your view variants with other users.") :arrow_upper_right:.




</td>
<td valign="top">

All apps in advanced financial closing



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

 `FlexKeyUser` 



</td>
<td valign="top">

-   Adapts the UI of apps for customer-specific use \(additionally, either the role template `AFC_SystemAdmin` or the role template `AFC_KeyUser` is needed\).

    For more information about UI adaptation, see [Adapting the UI](https://help.sap.com/docs/BTP/3d99fdeadde04524bdd33d35f1e13777/d868950a1e8c4b0f9b9453176939a19b.html?locale=en-US) in the SAP Fiori Launchpad documentation.

-   Creates public view variants \(additionally, either the role template `AFC_SystemAdmin` or the role template `AFC_KeyUser` is needed\).

    For more information, see [How to Share View Variants](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/SHIP/en-US/2fee7b5a83294d748953a9db5cc96326.html "Share your view variants with other users.") :arrow_upper_right:.




</td>
<td valign="top">

All apps in advanced financial closing



</td>
<td valign="top">

 



</td>
<td valign="top">

 



</td>
</tr>
</table>



<a name="loiob92a2411e4164270964903c502e22340__section_w3j_2c3_5qb"/>

## Available Composite Role Templates


<table>
<tr>
<th valign="top">

Role Template



</th>
<th valign="top">

Included Role Templates



</th>
</tr>
<tr>
<td valign="top">

`AFC_Expert`



</td>
<td valign="top">

-   `AFC_Define`
-   `AFC_Config`



</td>
</tr>
<tr>
<td valign="top">

`AFC_Manager`



</td>
<td valign="top">

-   `AFC_Reporting`
-   `AFC_Approve`
-   `AFC_UserManagement`



</td>
</tr>
</table>

