<!-- loiod8a918e86e3d41419fe6615d8e0d0bbe -->

# How to Set Up Certificate-Based Authentication

Create a destination certificate in the SAP BTP cockpit to enable certificate-based authentication for the connection between SAP Advanced Financial Closing and your SAP S/4HANA Cloud Public Edition system.



## Prerequisites

-   You have administrator access to your SAP BTP subaccount.

-   You're authorized to maintain technical communication users in SAP S/4HANA Cloud Public Edition.




## Context

By default, the connection between SAP Advanced Financial Closing and SAP S/4HANA Cloud Public Edition uses client certificate authentication. If you set up the connection using SAP BTP formations, the certificate is generated and exchanged automatically. If you set up the connection manually, you must create the certificate in the SAP BTP cockpit and then upload it to the communication user in SAP S/4HANA Cloud Public Edition.



## Procedure

**Creating the Certificate**

1.  Open the SAP BTP cockpit and navigate to your subaccount.

2.  In the left navigation panel, choose *Connectivity* \> *Destination Certificates*.

3.  Choose *Create* and provide the following information:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    What to Enter
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Name*
    
    </td>
    <td valign="top">
    
    Enter a meaningful name for the certificate.

    You will need to reference this name when configuring the destination.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Generation Service* \(read-only field\)
    
    </td>
    <td valign="top">
    
    `SAP Certificate Service`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *File Extension*
    
    </td>
    <td valign="top">
    
    Select `PEM`.

    Only PEM format is supported for the connection to SAP Advanced Financial Closing.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Validity*
    
    </td>
    <td valign="top">
    
    Enter a time frame as you wish.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Automatic Renewal*
    
    </td>
    <td valign="top">
    
    We recommend that you choose `Yes`.

    In that case the certificate is renewed automatically before it expires. The integration continues to work even after renewal.
    
    </td>
    </tr>
    </table>
    
4.  Save the certificate.

5.  Choose *Export* to download the certificate to your local machine.


**Assigning the Certificate to the Technical Communication User**

6.  In your SAP S/4HANA Cloud Public Edition system, go to the *Maintain Communication Users* app.

    > ### Tip:  
    > If you're unsure about which technical communication user is the right one, you can go to the *Communication Arrangement* app first. Find the arrangement for *Financial Task List Integration*, that is, scenario ID `SAP_COM_0566`. Under *Inbound Communication*, find the technical communication user and take note of the user name.

7.  Find the technical communication user for the communication arrangement for SAP Advanced Financial Closing and open its details.

8.  Under *Certificate*, choose *Upload* and select the certificate file you have previously created and downloaded.

9.  Save your changes.




## Results

The certificate is created in the SAP BTP cockpit and uploaded to the communication user in SAP S/4HANA Cloud Public Edition. The connection between SAP Advanced Financial Closing and SAP S/4HANA Cloud Public Edition is now secured using client certificate authentication.



## Next Steps

-   If you've switched from user/password-based authentication to certificate-based authentication and you've confirmed that the certificate-based communication works, it's recommended that you remove the password authentication from the technical communication user. This ensures a clean authentication setup.
-   To monitor the certificate status and validity, open the *Monitor Communication Systems*. You can also set up a *Certificate Near Expiration* notification scenario in the *Specify Communication Systems* to receive alerts when the certificate is approaching its expiration date.

    For more information on these two topics, see these pages:

    -   [Monitor Communication Systems](../System-Monitoring/monitor-communication-systems-a215069.md)
    -   [How to Set Up Notifications About Communication System Errors](../System-Monitoring/how-to-set-up-notifications-about-communication-system-errors-835b2a2.md)


**Parent topic:**[SAP S/4HANA Cloud Public Edition](sap-s-4hana-cloud-public-edition-60448a7.md "Connect to your financial cloud system to retrieve information about organizational units, the factory calendar, and so on.")

**Next:**[How to Add the Launchpad Tile in SAP S/4HANA Cloud Public Edition](how-to-add-the-launchpad-tile-in-sap-s-4hana-cloud-public-edition-857efd5.md "Add a tile for SAP Advanced Financial Closing to your launchpad in SAP S/4HANA Cloud Public Edition.")

**Previous:**[How to Create the Destination in the SAP BTP Cockpit](how-to-create-the-destination-in-the-sap-btp-cockpit-6e94409.md "Create a destination for your SAP S/4HANA Cloud Public Edition system in your SAP BTP cockpit.")

