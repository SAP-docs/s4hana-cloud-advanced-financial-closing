<!-- loiob92a2411e4164270964903c502e22340 -->

# Static Roles for Advanced Financial Closing

Static roles enable users to see the affected apps on their SAP Fiori launchpad.



## Available Role Templates


<table>
<tr>
<th>

Role Template



</th>
<th>

Description



</th>
<th>

Tiles on SAP Fiori Launchpad



</th>
</tr>
<tr>
<td>

 `AFC_SystemAdmin` 



</td>
<td>

-   Maintains solution-specific settings, for example, a connection to financial communication systems

-   Adapts the UI of apps for customer-specific use \(additionally, the role template `FlexKeyUser` is needed\).

    For more information about UI adaptation, see [Adapting the UI](https://help.sap.com/viewer/3d99fdeadde04524bdd33d35f1e13777/latest/en-US/d868950a1e8c4b0f9b9453176939a19b.html) in the SAP Fiori Launchpad documentation.

-   Creates public view variants \(additionally, the role template `FlexKeyUser` is needed\).

    For more information, see [How to Share View Variants](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/SHIP/en-US/2fee7b5a83294d748953a9db5cc96326.html "Share your view variants with other users.") :arrow_upper_right:.




</td>
<td>

System administration:

-   *Manage Users*
-   *Specify Communication Systems*



</td>
</tr>
<tr>
<td>

 `AFC_UserAdmin` 



</td>
<td>

-   Maintains users and the assignments between users and roles.

-   Maintains user groups




</td>
<td>

-   *Manage Users*
-   *Manage User Role Assignments*

Configuration:

-   *Manage User Groups*



</td>
</tr>
<tr>
<td>

 `AFC_UserRoles` 



</td>
<td>

Maintains user roles and authorization groups



</td>
<td>

Configuration:

-   *Manage User Roles*

-   *Manage Authorization Groups*




</td>
</tr>
<tr>
<td>

 `AFC_Compliance` 



</td>
<td>

Maintains general compliance settings



</td>
<td>

*Manage Compliance Settings*



</td>
</tr>
<tr>
<td>

 `AFC_Config` 



</td>
<td>

Maintains application-specific data, for example, configuration settings, or master data



</td>
<td>

Configuration:

-   *Manage Authorization Groups*
-   *Manage Country/Region Groups*
-   *Manage Email Notification Configurations*
-   *Manage User Groups*
-   *Manage User Roles*



</td>
</tr>
<tr>
<td>

 `AFC_Settings` 



</td>
<td>

Maintains application-specific settings, like notifications and country/region groups



</td>
<td>

Configuration:

-   *Manage Country/Region Groups*

-   *Manage Email Notification Configurations*




</td>
</tr>
<tr>
<td>

 `AFC_UserManagement` 



</td>
<td>

Maintains assignments between user and roles



</td>
<td>

*Manage User Role Assignments*



</td>
</tr>
<tr>
<td>

 `AFC_Define` 



</td>
<td>

Maintains task list templates and task lists



</td>
<td>

-   *Define Closing Tasks*
-   *Change Log*



</td>
</tr>
<tr>
<td>

 `AFC_Approve` 



</td>
<td>

Approves tasks



</td>
<td>

-   *Approve Closing Tasks*

-   *Change Log*



</td>
</tr>
<tr>
<td>

 `AFC_Process` 



</td>
<td>

Processes task lists and tasks



</td>
<td>

-   *Process Closing Tasks*
-   *Change Log*



</td>
</tr>
<tr>
<td>

 `AFC_Reporting` 



</td>
<td>

Monitors overall progress of closing activities and tracks task completion



</td>
<td>

Reporting:

-   *Financial Close Overview*
-   *Closing Task Completion*



</td>
</tr>
<tr>
<td>

 `AFC_KeyUser` 



</td>
<td>

-   Adapts the UI of apps for customer-specific use \(additionally, the role template `FlexKeyUser` is needed\).

    For more information about UI adaptation, see [Adapting the UI](https://help.sap.com/viewer/3d99fdeadde04524bdd33d35f1e13777/latest/en-US/d868950a1e8c4b0f9b9453176939a19b.html) in the SAP Fiori Launchpad documentation.

-   Creates public view variants \(additionally, the role template `FlexKeyUser` is needed\).

    For more information, see [How to Share View Variants](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/SHIP/en-US/2fee7b5a83294d748953a9db5cc96326.html "Share your view variants with other users.") :arrow_upper_right:.




</td>
<td>

All apps in advanced financial closing



</td>
</tr>
<tr>
<td>

 `FlexKeyUser` 



</td>
<td>

-   Adapts the UI of apps for customer-specific use \(additionally, either the role template `AFC_SystemAdmin` or the role template `AFC_KeyUser` is needed\).

    For more information about UI adaptation, see [Adapting the UI](https://help.sap.com/viewer/3d99fdeadde04524bdd33d35f1e13777/latest/en-US/d868950a1e8c4b0f9b9453176939a19b.html) in the SAP Fiori Launchpad documentation.

-   Creates public view variants \(additionally, either the role template `AFC_SystemAdmin` or the role template `AFC_KeyUser` is needed\).

    For more information, see [How to Share View Variants](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/SHIP/en-US/2fee7b5a83294d748953a9db5cc96326.html "Share your view variants with other users.") :arrow_upper_right:.




</td>
<td>

All apps in advanced financial closing



</td>
</tr>
<tr>
<td>

 `Business_Process_Specialist_BL_AccessAll` 



</td>
<td>

Reviews logs as an administrator



</td>
<td>

*Monitor Business Logs*



</td>
</tr>
</table>



<a name="loiob92a2411e4164270964903c502e22340__section_w3j_2c3_5qb"/>

## Available Composite Role Templates


<table>
<tr>
<th>

Role Template



</th>
<th>

Included Role Templates



</th>
</tr>
<tr>
<td>

AFC\_Expert



</td>
<td>

-   AFC\_Define
-   AFC\_Config



</td>
</tr>
<tr>
<td>

AFC\_Manager



</td>
<td>

-   AFC\_Reporting
-   AFC\_Approve
-   AFC\_UserManagement



</td>
</tr>
</table>

