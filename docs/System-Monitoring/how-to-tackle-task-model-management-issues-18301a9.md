<!-- loio18301a93bfc04f1e808c4a7e4d6c4611 -->

# How to Tackle Task Model Management Issues

Check the status of the task model management and tackle any existing issues.



<a name="loio18301a93bfc04f1e808c4a7e4d6c4611__prereq_u4p_lc5_ytb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_MonitorSystemsApp`

    -   `AFC_SystemAdmin`


    For more information about role templates, see [How to Manage Static Role Templates](../User-Management/how-to-manage-static-role-templates-0cca34d.md) and [Static Roles for SAP Advanced Financial Closing](../User-Management/static-roles-for-sap-advanced-financial-closing-b92a241.md).

-   For issue handling involving steps in the communication system, you're authorized to maintain the required settings in the communication system.



## Context

For systems that can allow task model management from within SAP Advanced Financial Closing, the task model management status indicates whether any issues exist.

Task model management issues can mainly originate from the following sources:

-   Settings in SAP Advanced Financial Closing
-   Settings in the communication system



## Procedure

1.  Open the *Monitor Communication Systems* app.

2.  From the table, open the system details of a communication system.

3.  In the *Status* section, check the *Task Model Management* tile for more details:


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
    
    *Status*
    
    </td>
    <td valign="top">
    
    Shows the status of the task model management connection. The following statuses are possible:

    -   *OK*

        Everything is working as expected.

    -   *Error*

        The system doesn't allow the selection made for *Task Model Management Allowed* or there are inconsistent settings in the communication system.



    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Task Model Management Allowed*
    
    </td>
    <td valign="top">
    
    Shows whether task model management is allowed for this communication system. The following values are possible:

    -   **For SAP S/4HANA Cloud Public Edition:**
        -   Yes

            Authorized users can create, edit, publish, and delete task models in SAP Advanced Financial Closing.


    -   For SAP S/4HANA Cloud Private Edition and SAP S/4HANA:
        -   Yes, with current settings

            Authorized users can create, edit, publish, and delete task models in SAP Advanced Financial Closing. This setting aligns with the *Current Settings* indicator of the underlying database tables in the communication system.

        -   Yes, with transport

            Authorized users can create, edit, publish, and delete task models in SAP Advanced Financial Closing. In the communication system, a transport request needs to exist. Users working on the task model need to enter the transport request upon publishing. In task list templates, users can then create tasks from these models.

            Based on the transport request, you can transport published task models between different system, for example, from your Quality system to the Production system.

        -   Yes, without transport

            Authorized users can create, edit, publish, and delete task models in SAP Advanced Financial Closing. In the communication system, no transport request is required. Accordingly, no transport between systems is possible.


    -   For all systems:
        -   No

            Users can't create task models in SAP Advanced Financial Closing. In task list templates, users can still create tasks from already existing models.




    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Last Checked On*
    
    </td>
    <td valign="top">
    
    Shows the date and time of the last status check, independently of whether the check was successful or not.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Status Changed On*
    
    </td>
    <td valign="top">
    
    Shows the date and time of when the current status was set.
    
    </td>
    </tr>
    </table>
    
4.  If the status shows as *Error*, perform the following checks:

    1.  Confirm that the selection under *Task Model Management Allowed* is correct:

        1.  Take note of the setting, it's mentioned on the tile as well.
        2.  Go to the communication system and verify that this setting is actually allowed.
        3.  If the setting is not allowed by the communication system, adjust the setting in SAP Advanced Financial Closing in the *Specify Communication Systems* app.
        4.  To confirm that the fix worked, choose *Check Task Model Management Setting* in the *Specify Communication Systems* app or *Check Settings* on the *Task Model Management* tile in the *Monitor Communication Systems* app.

    2.  Confirm that the table settings in the back end of your communication system are correct:

        1.  Go to the communication system.
        2.  Verify that the table settings are correct.
        3.  If they're not correct, fix them.
        4.  To confirm that the fix worked, choose *Check Settings* on the *Task Model Management* tile in the *Monitor Communication Systems* app.





## Results

You have now checked the task model management status of your communication system and tackled any issues.

