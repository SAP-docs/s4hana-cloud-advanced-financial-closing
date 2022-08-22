<!-- loioa86348d6459a4c929ec1f389e38827ad -->

# Synchronization of Communication Systems

Get an overview of the synchronization and validation of data.



<a name="loioa86348d6459a4c929ec1f389e38827ad__section_j5c_zsw_b5b"/>

## Context

As soon as you connect a communication system to SAP S/4HANA Cloud for advanced financial closing, regular synchronization ensures that the data in advanced financial closing is always up to date. During the synchronization, the data is also validated so that no inconsistent data is synchronized. These two aspects are addressed here.



<a name="loioa86348d6459a4c929ec1f389e38827ad__section_mgl_1tw_b5b"/>

## Synchronization

Synchronization between the communication system and advanced financial closing involves two sets of data: business configuration data and master data.

 ![Graphic depicting synchronization between advanced financial closing and the communication system: On the one hand, you have the communication system with its business configuration data and master data. On the other hand, you have advanced financial closing with business configuration data and master data that has already been received from the communication system. These two sets of data are synchronized during synchronization. During this process, business logs are created for both data sets. The logs consist of success, warning, and error messages.](images/Image_System_Synchronization_9881c12.png) 

Synchronization always covers both sets of data. Accordingly, if an error in one set causes synchronization to fail, synchronization fails for both data sets.

 ![Graphic depicting the same synchronization setup as the previous graphic: On the one hand, you have the communication system with its business configuration data and its master data. On the other hand, you have advanced financial closing with business configuration data and master data that has already been received from the communication system. Error messages in the business logs created during synchronization cause synchronization to fail for both data sets.](images/Image_System_Synchronization_Fails_0c014b2.png) 

The following data in advanced financial closing is synchronized with the connected system:


<table>
<tr>
<th valign="top" align="center">

Business Configuration



</th>
<th valign="top" align="center">

Master Data



</th>
</tr>
<tr>
<td valign="top">

Task model types



</td>
<td valign="top">

Accounting principles



</td>
</tr>
<tr>
<td valign="top">

Task list models

> ### Note:  
> Task list model changes in the communication system are applied to task list models only, **not** to task list templates or task lists that the model has been assigned to.



</td>
<td valign="top">

Factory calendars



</td>
</tr>
<tr>
<td valign="top">

Folder models



</td>
<td valign="top">

Fiscal year variants



</td>
</tr>
<tr>
<td valign="top">

Task models



</td>
<td valign="top">

Ledgers



</td>
</tr>
<tr>
<td valign="top">

Task dependencies



</td>
<td valign="top">

Organizational units



</td>
</tr>
<tr>
<td valign="top">

Assignment of tasks to country/region



</td>
<td valign="top">

Parameters



</td>
</tr>
<tr>
<td valign="top">

Assignments of tasks to folder



</td>
<td valign="top">

Task parameters



</td>
</tr>
</table>

> ### Note:  
> Only consistent data is synchronized. If data is deleted in your communication system, it will be set to *orphaned* in advanced financial closing with the next synchronization. This means that the orphaned data can't be used for new task list templates or task lists and their referenced objects.
> 
> If necessary, check the business logs for more information as described under [Logging](../Monitoring-and-Troubleshooting/logging-57375b8.md).



### Daily and Immediate Synchronization

To synchronize data \(for example, if you have changes in your communication system\), you have two options:

1.  You can wait for the **daily synchronization** to run.

    > ### Recommendation:  
    > Ensure that you always have the latest support package \(SP\) installed on your communication system. If this is not the case, synchronization may only take place every seven days instead of daily.

2.  You can trigger **immediate synchronization** using the *Synchronize Now* option in the *Specify Communication Systems* app. If you don't use this option, the communication system will still be synchronized during **daily synchronization**.


> ### Note:  
> Synchronization always uses the active state of the communication system entry in advanced financial closing. This means that any unsaved changes aren't considered and synchronization is performed based on the state last saved.



### Validation

The data that is synchronized is always validated to avoid any inconsistencies in advanced financial closing. The data is validated with regard to the following aspects:

-   Structure

-   Data consistency

-   Data references

    > ### Example:  
    > To synchronize an entity from the *Task Parameter Definition* table, the entity *Parameter Type Value* has to be available if it's referenced in the *Task Parameter Definition* table.


The synchronization results can be accessed in the *Monitor Business Logs* app. They're grouped into the following severity categories:

> ### Remember:  
> In the case of failing synchronizations, check the business logs before opening a ticket. The logs may already reveal the source of the issue.


<table>
<tr>
<th valign="top">

Severity Category



</th>
<th valign="top">

Description



</th>
<th valign="top">

Example



</th>
</tr>
<tr>
<td valign="top" rowspan="2">

*Success*



</td>
<td valign="top">

Data was synchronized successfully.

You also find information about the number of entities that were updated or added.



</td>
<td valign="top">

-   A new entity maintained in the communication system was synchronized.

-   An entity that was updated in the communication system was synchronized.




</td>
</tr>
<tr>
<td valign="top">

Entities that were synchronized before no longer exist in the communication system. They're mentioned as orphaned entities.

> ### Note:  
> Orphaned entities can still be used in existing task list templates and task lists that already reference them. However, they can't be added to any task list template or task list as of the moment they were marked as orphaned.



</td>
<td valign="top">

 



</td>
</tr>
<tr>
<td valign="top">

*Warning*



</td>
<td valign="top">

An issue was found with the affected entities.

Synchronization of the remaining data continues.



</td>
<td valign="top">

-   *Task Country Assignment* table:

    Incomplete table rows on ABAP side

-   A mandatory field or a key field is empty.

-   Entered value doesn't have the correct format, for example, a number is entered in a text field.

-   It is not possible to map the semantic code from ABAP.




</td>
</tr>
<tr>
<td valign="top">

*Error*



</td>
<td valign="top">

An issue was found with the affected entities.

Synchronization of the remaining data **cannot** continue and synchronization consequently fails.



</td>
<td valign="top">

 



</td>
</tr>
</table>

