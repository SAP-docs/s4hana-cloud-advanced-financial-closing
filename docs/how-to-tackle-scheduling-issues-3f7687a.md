<!-- loio3f7687ae18c4447085a391da18bbbc30 -->

# How to Tackle Scheduling Issues

Check the scheduling status of your communication system and tackle any existing issues.



<a name="loio3f7687ae18c4447085a391da18bbbc30__prereq_xnr_jcg_vvb"/>

## Prerequisites

Your user must have a role collection assigned that includes one of the following role templates:

-   `AFC_MonitorSystemsApp`

-   `AFC_SystemAdmin`


For more information about role templates, see [How to Manage Static Role Templates](User-Management/how-to-manage-static-role-templates-0cca34d.md).



## Context

The scheduling queue information reflects the status of the scheduling queue of a communication system and provides an overview of the tasks for which the scheduling is in preparation. It also shows how many of those are overdue. A task scheduling is considered overdue under the following conditions:

-   **Task that is scheduled to start immediately:** Task is considered overdue **immediately** if scheduling doesn't happen.

-   **Task that is scheduled for a specific point in time:** Task is considered overdue if it still hasn't been scheduled **15 minutes before** the scheduled start.


> ### Remember:  
> If the connection check doesn't show any successful result for twelve hours, the following processes are deactivated until the connection check is successful again:
> 
> -   Synchronization of master data
> 
> -   Scheduling of *Job* tasks



## Procedure

1.  Open the *Monitor Communication Systems* app.

2.  From the table, open the system details of a communication system.

3.  In the *Status* section, check the *Scheduling* tile for more details:


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
    
        The status is displayed only when a connection issue has caused the scheduling to be deactivated for the moment. The status is then *Paused*.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        *In Preparation*


    
    </td>
    <td valign="top">
    
        Shows the number of task executions that are currently being worked on and that are yet to be scheduled.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        *Overdue*


    
    </td>
    <td valign="top">
    
        Shows the number of tasks that are still in the scheduling queue but haven't been scheduled in time. A task is considered overdue under the following conditions:

    -   **Tasks for which a planned start time is maintained:** A task is considered overdue as of 15 minutes before the planned start time if the scheduling hasn't happened yet.

    -   **Tasks which have been scheduled to start immediately \(no planned start time maintained\):** A task is immediately considered overdue.



    
    </td>
    </tr>
    </table>
    
4.  For more information about the scheduling queue, choose *Show Schedulings* on the *Scheduling* tile. This brings you to an overview of the scheduling queue for this communication system.

    1.  If all schedulings are running as expected, no further action is required.

    2.  If task schedulings are considered overdue, one of the following issues may be the reason:

        -   A large number of task schedulings is currently in the queue.

            > ### Note:  
            > The system is still working on the queue and schedules tasks as soon as possible.

        -   Performance of the communication system is low. You may want to check what is impacting the system performance.


        > ### Recommendation:  
        > Independent of the reason for the delay, you may want to inform users that there is a delay in scheduling.





<a name="loio3f7687ae18c4447085a391da18bbbc30__result_ibv_kxm_vvb"/>

## Results

You have now checked the scheduling status of your communication system.

