<!-- loio5839c73985d34eaaa21413ab92846b6e -->

# Audit Log Integration

Audit logs for security-relevant events.



<a name="loio5839c73985d34eaaa21413ab92846b6e__section_e2k_1jg_f1c"/>

## Context

SAP Advanced Financial Closing is integrated into the SAP Audit Log service for SAP BTP. This means that logs for several security-relevant events in SAP Advanced Financial Closing are written to this audit log in addition to logs from other SAP solutions.

The logs created by SAP Advanced Financial Closing can be extracted using the SAP Audit Log Management service and viewed using the SAP Audit Log Viewer service.



<a name="loio5839c73985d34eaaa21413ab92846b6e__section_kvv_wkg_f1c"/>

## Logs Written by SAP Advanced Financial Closing

SAP Advanced Financial Closing writes audit logs for the following events:


<table>
<tr>
<th valign="top">

Event Type

</th>
<th valign="top">

Event Logged

</th>
<th valign="top">

Event Text

</th>
<th valign="top">

Additional Information

</th>
<th valign="top">

Information Included

</th>
</tr>
<tr>
<td valign="top">

Security event

</td>
<td valign="top">

Malware detection during file upload

</td>
<td valign="top">

AFC: Malware detected during file upload

</td>
<td valign="top">

SAP Advanced Financial Closing runs virus scans when users upload files, such as attachments or template files used to update user details or assignments. If malware is detected during an upload, the upload is prohibited and an audit log about this event is written.

</td>
<td valign="top">

-   Malware scan result
-   File name
-   MIME type of file



</td>
</tr>
<tr>
<td valign="top">

Security event

</td>
<td valign="top">

Access to system

</td>
<td valign="top">

AFC: Data access by SAP Development Support

</td>
<td valign="top">

SAP support may be required to access customer systems to ensure availability of the customer system according to the service level agreements as agreed in the contractual agreement between SAP and the customer, by active monitoring, prompt issue detection, and incident prevention. This access always requires SAP support to be authorized to do this. Reasons for system access by SAP support include the following:

-   Issue investigation \(only if the issue can't be reproduced otherwise\)
-   Software lifecycle management



</td>
<td valign="top">

-   Description and purpose of the query
-   SQL query
-   User



</td>
</tr>
<tr>
<td valign="top">

Security event

</td>
<td valign="top">

Deletion of communication system

</td>
<td valign="top">

AFC: Communication System was deleted

</td>
<td valign="top">

A communication system entry in SAP Advanced Financial Closing was deleted and can no longer be used for task list templates or task lists.

</td>
<td valign="top">

-   Communication system ID
-   Communication system name
-   Destination configuration name
-   Value of *Is Production System* indicator
-   URL



</td>
</tr>
</table>



<a name="loio5839c73985d34eaaa21413ab92846b6e__section_ffn_5f3_f1c"/>

## How to Access Applications Relating to the SAP Audit Log Service

For information about how to subscribe to the SAP Audit Log service and how to access audit logs, see [Audit Logging in the Cloud Foundry Environment \(SAP BTP documentation\)](https://help.sap.com/docs/btp/sap-business-technology-platform/audit-logging-in-cloud-foundry-environment?locale=en-US) and its underlying pages.

