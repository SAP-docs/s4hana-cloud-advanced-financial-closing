<!-- loioc338b300dd01425bb74c04f0833f417c -->

# How to Manage Users

Upload new users to SAP S/4HANA Cloud for advanced financial closing and update certain user attributes.



<a name="loioc338b300dd01425bb74c04f0833f417c__prereq_sqn_c1c_ckb"/>

## Prerequisites

-   Your user must have a role collection assigned that includes one of the following role templates:

    -   `AFC_SystemAdmin`

    -   `AFC_UserAdmin`


    For more information about role templates, see [How to Manage Static Role Templates](How_to_Manage_Static_Role_Templates_0cca34d.md).

-   The users you want to upload must be maintained in your identity provider \(IdP\) including the following user attributes:

    -   `logonName`

    -   `givenName`

    -   `familyName`

    -   `email`





## Context

Users who are maintained in the IdP are able to sign in to SAP S/4HANA Cloud for advanced financial closing without any additional setting. They can access the apps according to the static role templates that are assigned to them.

In addition, you can upload users manually to advanced financial closing in advance so that you can assign user roles to them and enter them as users responsible or processing users, for example. For all user attributes that are maintained in the IdP, you have to do this only once. If certain user attributes aren't maintained in your IdP, you can use the upload function to keep these attributes up to date. In the *Manage Users* app, you can see all users available in advanced financial closing, independently of whether they were uploaded or created through their first sign-in.

You **must maintain** the user attributes `logonName`, `givenName`, `familyName`, and `email` in the IdP. In advanced financial closing, you can only maintain these attributes via the initial user upload or until the users have signed in for the first time. You can't use the upload to update these attributes.

You **can** maintain the following user attributes in the IdP and have to map them to the corresponding user attributes in advanced financial closing. Alternatively, you can maintain these attributes by uploading users manually.

<a name="loioc338b300dd01425bb74c04f0833f417c__table_bsc_sgc_hlb"/>User Attributes


<table>
<tr>
<th valign="top">

Identity Provider



</th>
<th valign="top">

Advanced Financial Closing



</th>
</tr>
<tr>
<td valign="top">

`Address`



</td>
<td valign="top">

`address`



</td>
</tr>
<tr>
<td valign="top">

`Phone`



</td>
<td valign="top">

`phone`



</td>
</tr>
<tr>
<td valign="top">

`Mobile`



</td>
<td valign="top">

`mobile`



</td>
</tr>
<tr>
<td valign="top">

`Fax`



</td>
<td valign="top">

`fax`



</td>
</tr>
<tr>
<td valign="top">

`Department`



</td>
<td valign="top">

`department`



</td>
</tr>
<tr>
<td valign="top">

`Function`



</td>
<td valign="top">

`function`



</td>
</tr>
<tr>
<td valign="top">

`Division`



</td>
<td valign="top">

`function` \(if function is empty\)



</td>
</tr>
</table>

> ### Note:  
> The information provided by the IdP always takes precedence. User attributes from the IdP overwrite the information stored in advanced financial closing when the users sign in to the app.

> ### Caution:  
> Make sure that the user attribute `email` isn't empty and is always maintained correctly. The following features can't be used if the email isn't entered correctly because they rely on the email address to find the respective user in the connected financial communication systems:
> 
> -   Task scheduling using this user
> 
> -   Notifications and email to this user



## Procedure

1.  Go to the *Manage Users* app.

2.  Download the template file.

3.  Fill the template file with your users according to the format provided.

    > ### Note:  
    > -   The *ID* field is mandatory, and the value entered must match the user ID maintained in the IdP. Note that the field is case-sensitive.
    > 
    > -   For information about which language codes are allowed, refer to [Language Codes Allowed for User Upload](Language_Codes_Allowed_for_User_Upload_51c9133.md).
    > 
    > -   Use semicolons as column separators.
    > 
    > -   Save the file with UTF-8 encoding.
    > 
    > -   The fields containing numbers have to be formatted as **text** prior to saving the CSV file.

4.  Choose *Upload Users* and select the file you prepared.

5.  Review the results of the upload in the dialog that summarizes the changes.




<a name="loioc338b300dd01425bb74c04f0833f417c__result_u45_nyd_rkb"/>

## Results

The users are uploaded with source *CSV Upload*. Once the respective users have signed in for the first time, the source is updated to *Identity Provider*. From then on, the identity provider is the source of the user information.

> ### Note:  
> User information provided by the IdP is updated via the IdP. However, you need to update the user information manually which you've uploaded in your CSV file but which you haven't maintained in the IdP.

-   **[Language Codes Allowed for User Upload](Language_Codes_Allowed_for_User_Upload_51c9133.md "")**  


**Parent topic:** [User Management](User_Management_ae7fa30.md "")

**Next:** [How to Manage Static Role Templates](How_to_Manage_Static_Role_Templates_0cca34d.md "Define and bundle static roles and assign them to users.")

**Previous:** [User Access Management](User_Access_Management_6fa5e4e.md "You can control and grant access to task list templates, task lists, and tasks in SAP S/4HANA Cloud for advanced financial closing. By default, users don't have access to these objects.")

