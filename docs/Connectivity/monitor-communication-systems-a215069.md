<!-- loioa215069e4c534617acde3e03393b3168 -->

# Monitor Communication Systems

You use the *Monitor Communication Systems* app to check the status of your connected communication systems and tackle any issues.

To perform your financial close, you have connected one or more financial communication systems as described in the previous topics. For your financial close to work, the connection to the systems has to work and synchronization of data has to be successful. To get an overview of the current statuses of your systems, you can use the *Monitor Communication Systems* app. The app shows you an overall status for each system and provides detailed information about the source of any issues.



<a name="loioa215069e4c534617acde3e03393b3168__section_yzc_lwt_ytb"/>

## Key Features

-   Overview of overall system statuses

-   Source of any errors

-   Detailed information about checks and synchronization runs

-   Option to start new checks or synchronization runs manually

-   Detailed error messages for specific checks and synchronization runs




<a name="loioa215069e4c534617acde3e03393b3168__section_zgv_l2p_g5b"/>

## Statuses



### Overall System Status

The following system statuses are possible:

<a name="loioa215069e4c534617acde3e03393b3168__d50e960"/>Overall System Status


<table>
<tr>
<th valign="top">

System Status



</th>
<th valign="top">

Description



</th>
</tr>
<tr>
<td valign="top">

*OK*



</td>
<td valign="top">

No connection or synchronization issues were detected. No further action required.



</td>
</tr>
<tr>
<td valign="top">

*Error*



</td>
<td valign="top">

One or more issues were detected. Check the *Status Source* column and the system details for more information. Tackle any issues and restart the check or synchronization run affected.



</td>
</tr>
</table>



### Connection Status

The connection status is checked regularly. However, the frequency depends on the status that was set during the last check. The status is checked as follows:

<a name="loioa215069e4c534617acde3e03393b3168__d50e1013"/>Connection Status Checks


<table>
<tr>
<th valign="top">

Status During Last Check



</th>
<th valign="top">

Time Period After Status Was Set



</th>
<th valign="top">

Check Frequency



</th>
</tr>
<tr>
<td valign="top">

*OK*



</td>
<td valign="top">

Always



</td>
<td valign="top">

Every three hours



</td>
</tr>
<tr>
<td valign="top" rowspan="3">

*Error*



</td>
<td valign="top">

First 24 hours



</td>
<td valign="top">

Every 15 minutes



</td>
</tr>
<tr>
<td valign="top">

Days 1 to 30



</td>
<td valign="top">

Decreasing frequency between every hour and every 12 hours



</td>
</tr>
<tr>
<td valign="top">

After 30 Days



</td>
<td valign="top">

Every 24 hours



</td>
</tr>
</table>

> ### Note:  
> Connection issues can also be detected outside any scheduled checks, for example, when a user tries to schedule a task in the corresponding communication system. If an issue is detected this way, but the connection status is *OK* based on the last connection check, an additional connection check is scheduled to happen within the next 15 minutes. You can then find the results in the *Monitor Communication Systems* app.
> 
> The following graphic illustrates this process:
> 
>  ![Graphic depicting the process leading to an additional connection check: First, a regular check is successful and set the connection status to OK. Then, a user tries to schedule a job in the same communication system. The scheduling fails due to connection issues. Accordingly, an additional connection check is planned to start within the next 15 minutes. If this check is successful, the connection status stays in status OK. If the check fails, the connection status for this system is set to Error.](images/Image_Extraordinary_Connection_Check_f12b958.png) 



### Synchronization Status

The synchronization check follows the frequency and rules as described under [Synchronization of Communication Systems](synchronization-of-communication-systems-a86348d.md).

-   **[How to Check the Overall System Status](how-to-check-the-overall-system-status-f30be05.md "Check the overall statuses of your connected communication systems.")**  
Check the overall statuses of your connected communication systems.
-   **[How to Tackle Connection Issues](how-to-tackle-connection-issues-7b0898e.md "Check the connection status of your communication system and tackle any existing
		issues.")**  
Check the connection status of your communication system and tackle any existing issues.
-   **[How to Tackle Synchronization Issues](how-to-tackle-synchronization-issues-ed8c4ec.md "Check the synchronization status of your communication system and tackle any issues.")**  
Check the synchronization status of your communication system and tackle any issues.

