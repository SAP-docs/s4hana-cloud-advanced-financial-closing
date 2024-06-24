<!-- loiob6e6eb25710a4c97b935a69a9bb35ad6 -->

# Archiving Spool Results in Connected Communication Systems Using `AFC_OBJSTR`

Archive spool results relating to SAP Advanced Financial Closing.

You can use archiving object `AFC_OBJSTR` to archive spool results in SAP Advanced Financial Closing.

> ### Note:  
> Data archiving is available for on-premise systems only.

**Tables**

`AFC_OBJSTR` archives data from several tables. To check which tables these are, call up transaction `SARA`, enter the archiving object, and choose *Database Tables*. You can display the relevant tables in the lower part of the screen.



## Prerequisites

The following prerequisite must be fulfilled before a spool list relating to SAP Advanced Financial Closing can be archived:

The residence time is fulfilled.

> ### Note:  
> You define the residence time as described under [Performing an Application-Specific Configuration](archiving-spool-results-in-connected-communication-systems-using-afc-objstr-b6e6eb2.md#loiob6e6eb25710a4c97b935a69a9bb35ad6__section_afc_performing_app-specific_config) on this page.



<a name="loiob6e6eb25710a4c97b935a69a9bb35ad6__section_afc_performing_app-specific_config"/>

## Performing an Application-Specific Configuration

Before you can use archiving object `AFC_OBJSTR`, you must first make residence time settings in *Application-Specific Customizing* under *AFC ILM Configuration*:

> ### Note:  
> Alternatively, you can go to transaction `AFC_ILM_MANAGE`.

1.  Create a new entry.
2.  Define the residence key as *Spool Result Residence Days*.
3.  Under *Residence Days*, define the residence time in days, that is, the minimum time that the objects need to remain in the database tables.



## Defining Write Variants

When you schedule the archiving run, you must enter an existing variant or create a new one. You can do so in transaction `SARA`.

A write variant contains the parameters for `AFC_OBJSTR` so that spool lists can be archived.

SAP delivers the following parameters:

-   *Result Object Type*

    Type of the object that is to be archived.

-   *Stream Type*

    File type of the objects to be archived, that is, PDF or CSV.




## Displaying Spool Lists Archived with `AFC_OBJSTR`

Archived objects are archived in the communication system, but they can still be accessed in SAP Advanced Financial Closing in the same way as unarchived objects as long as the files exist in the archive. Once the files are deleted from the archive, they can no longer be accessed in SAP Advanced Financial Closing.

