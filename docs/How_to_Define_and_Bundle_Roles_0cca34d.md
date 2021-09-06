<!-- loio0cca34d98080443b8ce7294e9b4977b4 -->

# How to Define and Bundle Roles



<a name="loio0cca34d98080443b8ce7294e9b4977b4__prereq_gq2_n3n_sjb"/>

## Prerequisites

1.  You've performed onboarding.

    For more information, see [Onboarding](Onboarding_1987953.md).

2.  You've established trust and federation with the UAA.

    For more information, see [Trust and Federation with SAML 2.0 Identity Providers](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cb1bc8f1bd5c482e891063960d7acd78.html)




<a name="loio0cca34d98080443b8ce7294e9b4977b4__context_lxm_n3n_sjb"/>

## Context

As a prerequisite for assigning roles to IdP users or user groups, you also need to configure role collections. A role collection consists of one or more roles from one or more applications and can be used to bundle authorizations within and across applications.

For more information about how to create roles and how to bundle them in role collections using the SAP BTP cockpit, see [Building Roles and Role Collections for Applications](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/eaa6a26291914b348e875a00b6beb729.html).

> ### Caution:  
> Users to whom you assign a static role for system administration, configuration, user management, or compliance can read and change all data in the respective apps. For other apps, access must be granted before users can read and change data. For more information, see [Access Control](Business_Configuration/Access_Control_6fa5e4e.md).



<a name="loio0cca34d98080443b8ce7294e9b4977b4__steps_uj3_43n_sjb"/>

## Procedure

1.  Familiarize yourself with the available role templates.


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
    
2.  Additionally, decide whether you want to make use of the available composite role templates.


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
    
3.  Create role collections from the role templates provided by advanced financial closing. Follow the steps under [Maintain Role Collections](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/d5f1612d8230448bb6c02a7d9c8ac0d1.html).

    > ### Caution:  
    > For a separation of concerns, you might want to avoid combining the role templates `AFC_Define` and `AFC_Process` into one role collection.

    > ### Note:  
    > When creating role collections, keep in mind that an app may link to objects in another app. For example, the *Closing Task Completion* app links to tasks in the *Process Closing Tasks* app. You can create a role collection that includes the role template `AFC_Reporting` but not the role template `AFC_Process`. However, the users with this role collection won't be able to follow the link to the task details in the *Process Closing Tasks* app.

4.  Assign role collections to users. Follow the steps under [Assign Role Collections](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/9e1bf57130ef466e8017eab298b40e5e.html).

5.  Add roles to role collections. Follow the steps under [Add Roles to Role Collections](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7596a0bdab4649ac8a6f6721dc72db19.html).


**Related Information**  


[Access Control](Business_Configuration/Access_Control_6fa5e4e.md "You can control and grant access to task list templates, task lists, tasks, and folders in SAP S/4HANA Cloud for advanced financial closing. By default, users don't have access to these objects.")

