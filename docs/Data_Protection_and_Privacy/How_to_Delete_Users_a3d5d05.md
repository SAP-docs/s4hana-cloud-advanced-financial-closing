<!-- loioa3d5d0560f3a4e368c95c1bb661bb594 -->

# How to Delete Users



<a name="loioa3d5d0560f3a4e368c95c1bb661bb594__prereq_ysh_fzc_kkb"/>

## Prerequisites

Your user must have a role collection assigned that includes the role template `AFC_SystemAdmin`.



## Context

> ### Caution:  
> To revoke all access to SAP S/4HANA Cloud for advanced financial closing from users, it is not enough to delete them using the *Manage Users* app. You need to **revoke further access rights**. For more information, see the procedure, results, and next steps described below.

When you delete users from SAP S/4HANA Cloud for advanced financial closing, there is no retention period, which means that the user data is deleted directly. However, there are different means to reactivate deleted users.

To delete a user, do the following:



## Procedure

1.  Open the *Manage Users* app.

2.  Select the user you want to delete and choose *Delete*.

    > ### Note:  
    > You can display all deleted users by selecting *Deleted* in the *Status* filter.

3.  To avoid the reactivation of a user through a new logon via the IdP, you also need to unassign the user from all role collections **relevant for SAP S/4HANA Cloud for advanced financial closing**. This way, access to all apps for advanced financial closing is revoked. You can delete the user from role collections using the SAP BTP cockpit. For more information, see [Delete Users from Role Collections](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/latest/en-US/4f8a242839a947f9a6f379650480c776.html).




<a name="loioa3d5d0560f3a4e368c95c1bb661bb594__result_xhj_v4w_gnb"/>

## Results

-   The user's data is now removed from the system. The user is now displayed as a deleted user. The only information that remains is the user ID. However, keep in mind that users who have been deleted can be reactivated. For more information, see the section about next steps below.

-   A deleted user's ID might still be displayed in the system, for example, in logs or in relation to objects.




<a name="loioa3d5d0560f3a4e368c95c1bb661bb594__postreq_e3k_rnw_gnb"/>

## Next Steps

-   To reactivate users, upload them again to match them to their previous ID. Alternatively, users can log in via the IdP to reactivate their account. After users have been reactivated, they are assigned to the same role collections and user roles as they were before the deletion.


