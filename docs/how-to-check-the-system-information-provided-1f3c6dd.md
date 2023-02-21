<!-- loio1f3c6ddae438455f82ae2ec8191c35c8 -->

# How to Check the System Information Provided

Check that the system information provided is correct.



<a name="loio1f3c6ddae438455f82ae2ec8191c35c8__prereq_htj_xfh_fvb"/>

## Prerequisites

Your user must have a role collection assigned that includes one of the following role templates:

-   `AFC_MonitorSystemsApp`

-   `AFC_SystemAdmin`

-   `AFC_MonitorSystemsApp_Display`


For more information about role templates, see [How to Manage Static Role Templates](User-Management/how-to-manage-static-role-templates-0cca34d.md).



## Context

For systems that have an SAP Fiori launchpad, you can easily check whether the system information provided in the *Specify Communication Systems* app is correct. The check verifies that the UI domain, UI endpoint, and possibly UI parameters are correct and that they lead to the correct URL.



## Procedure

1.  Open the *Monitor Communication Systems* app.

2.  In the table listing all communication systems, select the communication system you want to check.

3.  In the table toolbar, choose *Check UI Settings*.

    The SAP S/4HANA Cloud for advanced financial closing application now uses the SAP Fiori launchpad information provided for the communication system in the *Specify Communication Systems* app and tries to call up the corresponding SAP Fiori launchpad.

    > ### Tip:  
    > You also have this option available in the communication system details in the *SAP Fiori Launchpad* section.

    1.  If the system successfully calls up the relevant SAP Fiori launchpad, no further action with regard to the system information is required.

    2.  If the system isn't able to call up the relevant SAP Fiori launchpad, check the system information and fix any issues that exist.

        > ### Note:  
        > Fixing issues with the system information may require you to have additional authorizations or to contact a system administrator who has the authorization required.





<a name="loio1f3c6ddae438455f82ae2ec8191c35c8__result_h4v_vfh_fvb"/>

## Results

You have now checked the system information provided for a specific communication system.

