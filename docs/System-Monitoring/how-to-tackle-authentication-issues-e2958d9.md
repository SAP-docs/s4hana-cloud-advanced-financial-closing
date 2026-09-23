<!-- loioe2958d9eb0a94f8a954407bbc1d41ed7 -->

# How to Tackle Authentication Issues

Check the status of the certificate-based authentication and tackle any existing issues.



<a name="loioe2958d9eb0a94f8a954407bbc1d41ed7__prereq_u4p_lc5_ytb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_MonitorSystemsApp`

    -   `AFC_SystemAdmin`


    For more information about role templates, see [How to Manage Static Role Templates](../User-Management/how-to-manage-static-role-templates-0cca34d.md) and [Static Roles for SAP Advanced Financial Closing](../User-Management/static-roles-for-sap-advanced-financial-closing-b92a241.md).

-   For issue handling involving steps in the SAP BTP cockpit, you have administrator access to your SAP BTP subaccount.
-   For issue handling involving steps in the communication system, you're authorized to maintain technical communication users in the communication system.



## Context

**Systems of type SAP S/4HANA Cloud Public Edition** can be connected to SAP Advanced Financial Closing using client certificates to authenticate.

For systems that use certificate-based authentication, the authentication status provides more information about the certificate used for authentication between SAP Advanced Financial Closing and the communication system. The status indicates whether everything is ok or whether the certificate is already expired. If the certificate expires without being renewed, the connection between the communication system and SAP Advanced Financial Closing is disrupted.

Authentication issues can mainly originate from the following sources:

-   Certificate
-   Technical communication user
-   Destination configuration



## Procedure

1.  Open the *Monitor Communication Systems* app.

2.  From the table, open the system details of a communication system.

3.  In the *Status* section, check the *Authentication* tile for more details:


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
    
    Shows the status of the certificate used for authentication between SAP Advanced Financial Closing and the communication system. The following statuses are available:

    -   *OK*
    -   *Expired*


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Method*
    
    </td>
    <td valign="top">
    
    Method of authentication for the communication between SAP Advanced Financial Closing and the communication system.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Certificate Valid Until*
    
    </td>
    <td valign="top">
    
    Shows the expiration date of the certificate. If the certificate expires without being renewed, the connection between the communication system and SAP Advanced Financial Closing is disrupted.

    > ### Tip:  
    > If you've opted for automatic renewal when you created the certificate, this date will update after the renewal and the connection will persist.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Certificate Changed On*
    
    </td>
    <td valign="top">
    
    Shows the date and time of the connection check that noticed that the certificate was changed or its validity was updated.
    
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
    
4.  If the status shows as *Expired*, the connection between the communication system and SAP Advanced Financial Closing is disrupted and can't currently be used. To find the source of the issue do the following:

    1.  You can check under *Certificate Valid Until* for the actual expiration date.

    2.  In most cases, you simply need to update the validity of the certificate attached to the technical communication user:

        1.  Open the SAP BTP cockpit and navigate to your subaccount.
        2.  In the left navigation panel, choose *Connectivity* \> *Destination Certificates*.
        3.  Find the certificate used for this communication arrangement.
        4.  Update its validity to make it valid again.
        5.  We recommend that you update the selection under *Automatic Renewal* to `Yes`.

            In that case the certificate is renewed automatically before it expires. The integration with SAP Advanced Financial Closing continues to work even after renewal.

        6.  Back in the *Monitor Communication Systems* app, refresh the tiles or run a new synchronization to get the authentication status updated.

    3.  If the authentication status remains as *Expired* after the previous step, there may be an issue with the assignment of the technical user:

        1.  In your SAP S/4HANA Cloud Public Edition system, go to the *Communication Arrangement* app.
        2.  Find the arrangement for *Financial Task List Integration*, that is, scenario ID `SAP_COM_0566`.
        3.  Back in the *Monitor Communication Systems* app, refresh the tiles or run a new synchronization to get the authentication status updated.
        4.  Under *Inbound Communication*, find the technical communication user and verify that it's the correct one.
        5.  If the user assigned is not the correct one, assign another technical communication user.

            > ### Caution:  
            > The technical communication user has to be the one you created when you set up the integration as described under [How to Set Up the Integration of Financial Task List Management](../Connectivity/how-to-set-up-the-integration-of-financial-task-list-management-24140e9.md).

        6.  Back in the *Monitor Communication Systems* app, refresh the tiles or run a new synchronization to get the authentication status updated.

    4.  If the authentication status remains as *Expired* after the previous steps, there may be an issue with the assignment between technical user and certificate:

        1.  In your SAP S/4HANA Cloud Public Edition system, go to the *Maintain Communication Users* app.

            > ### Tip:  
            > If you're unsure about which technical communication user is the right one, you can go to the *Communication Arrangement* app first. Find the arrangement for *Financial Task List Integration*, that is, scenario ID `SAP_COM_0566`. Under *Inbound Communication*, find the technical communication user and take note of the user name.

        2.  Find the technical communication user for the communication arrangement for SAP Advanced Financial Closing and open its details.
        3.  Under *Certificate*, verify that the correct certificate is attached.
        4.  If the certificate is not the correct one, upload the correct one and save.
        5.  Back in the *Monitor Communication Systems* app, refresh the tiles or run a new synchronization to get the authentication status updated.





## Results

You have now checked the authentication status of your communication system and tackled any issues.

