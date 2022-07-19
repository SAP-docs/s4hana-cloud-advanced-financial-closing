<!-- loiob92a2411e4164270964903c502e22340 -->

# Static Roles for Advanced Financial Closing

Static roles enable users to see the affected apps on their SAP Fiori launchpad.



## Available Role Templates

<a name="loiob92a2411e4164270964903c502e22340__d15e223"/>Role Templates


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
</tr>
<tr>
<td valign="top">

 `AFC_SystemAdmin` 



</td>
<td valign="top">

-   Maintains solution-specific settings, for example, a connection to financial communication systems

-   Adapts the UI of apps for customer-specific use \(additionally, the role template `FlexKeyUser` is needed\).

    For more information about UI adaptation, see [Adapting the UI](https://help.sap.com/docs/BTP/3d99fdeadde04524bdd33d35f1e13777/d868950a1e8c4b0f9b9453176939a19b.html?locale=en-US) in the SAP Fiori Launchpad documentation.

-   Creates public view variants \(additionally, the role template `FlexKeyUser` is needed\).

    For more information, see [How to Share View Variants](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/SHIP/en-US/2fee7b5a83294d748953a9db5cc96326.html "Share your view variants with other users.") :arrow_upper_right:.




</td>
<td valign="top">

System administration:

-   *Manage Users*
-   *Specify Communication Systems*



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

AFC\_Expert



</td>
<td valign="top">

-   AFC\_Define
-   AFC\_Config



</td>
</tr>
<tr>
<td valign="top">

AFC\_Manager



</td>
<td valign="top">

-   AFC\_Reporting
-   AFC\_Approve
-   AFC\_UserManagement



</td>
</tr>
</table>

