<!-- loio49376ed8c58f41e0b84d141824698721 -->

# How to Manage User Access Using the SCIM API Provided

Manage users, user groups, and user roles through a dedicated API.



<a name="loio49376ed8c58f41e0b84d141824698721__prereq_o2z_qx5_vvb"/>

## Prerequisites

-   You've created an API instance and service key for API integration scenarios for SAP Advanced Financial Closing as described under [How to Create an API Instance and Service Binding for API Integration Scenarios](how-to-create-an-api-instance-and-service-binding-for-api-integration-scenarios-4058064.md).

-   To access the API information available from the user interface of SAP Advanced Financial Closing, your user must have a role collection assigned that includes the role template `AFC_API_Access`.

-   If you want to change **user-to-role assignments** using the SCIM API, you need to create the user roles in SAP Advanced Financial Closing first as described under [User Access Management](../User-Management/user-access-management-d974847.md).

    You don't need to assign users to the roles yet because you can do that using the SCIM API.




## Context

Working with the Identity Provisioning service or Identity Authentication service, you can use the SCIM API to change users, user groups, user-to-group assignments, and user-to-role assignments following the SCIM standard. User role assignments are also available as an SCIM extension. Accordingly, you can perform user-to-role assignments using the SCIM API also when you work with a custom implementation instead of the Identity Provisioning service or Identity Authentication service.

> ### Caution:  
> If you use the SCIM API, keep in mind that certain user information is case-sensitive and has to be identical between the different sources. The following user data is affected and has to be identical:
> 
> -   *User ID* in SAP Advanced Financial Closing
> 
> -   *User ID* used in the CSV upload of user data
> 
> -   *Login Name* in the identity service
> 
> -   *Subject Name Identifier* in IDP / XSUAA
> 
> 
> If this information isn't identical even though the data refers to the same user, multiple users will be maintained.

> ### Note:  
> -   Deleted users are not available through the SCIM API, even if assignments still exist in SAP Advanced Financial Closing.

> ### Restriction:  
> The following rate limits apply when using the SCIM API:
> 
> -   You can create a maximum of 10,000 requests per hour.
> 
> -   You can create a maximum of three requests at the same time.



### Different Means to Manage User Access

In SAP Advanced Financial Closing, you have different means to manage specific aspects of user access:

-   Manage user access in SAP Advanced Financial Closing directly.
-   Manage user access through an identity provider.
-   Manage user access using the SCIM API provided.

Some of these different means to manage user access offer a subset of available functions. Additionally, when using the SCIM API provided, you need to pay attention to the following effects:

-   You can't synchronize a user group using the SCIM API if a draft already exists for this user group in SAP Advanced Financial Closing. You may find corresponding error messages in the synchronization log.
-   A user group that has been synchronized using the SCIM API becomes a read-only group in SAP Advanced Financial Closing. However, you can reactivate the *Edit* function in SAP Advanced Financial Closing by choosing *Reactivate Edit Function* for the affected group in the *Manage User Groups* app.

    > ### Note:  
    > After another synchronization through the SCIM API, the changes you made in SAP Advanced Financial Closing after reactivating the *Edit* function will be overwritten and the group will become read-only again.

-   Ensure that you don't synchronize empty user groups using the SCIM API, since users may be able to assign these groups to objects in SAP Advanced Financial Closing.

> ### Tip:  
> To have a better overview of the source of a user or user group, you can add the *Source* column to the lists in the *Manage Users* app and in the *Manage User Groups* app.



## Procedure

1.  **Optional:** Maintain the API information for your source system:

    As a source system, you can use an identity authentication, for example. To do this, follow the steps described under [SAP Advanced Financial Closing \(Identity Provisioning documentation for source systems\)](https://help.sap.com/docs/identity-provisioning/identity-provisioning/sap-s-4hana-cloud-for-advanced-financial-closing).

    > ### Note:  
    > The steps described in the documentation refer to Identity Provisioning provided by [SAP Cloud Identity Services](https://help.sap.com/docs/IDENTITY_PROVISIONING/f48e822d6d484fa5ade7dda78b64d9f5/2d2685d469a54a56b886105a06ccdae6.html).
    > 
    > Other identity provisioning services may require a different configuration.

2.  Maintain the API information for your target system as described under [SAP Advanced Financial Closing \(Identity Provisioning documentation for target systems\)](https://help.sap.com/docs/identity-provisioning/identity-provisioning/target-sap-s-4hana-cloud-for-advanced-financial-closing).

    Some of the information you need to provide may be sensitive data for which security recommendations apply. For more information, see [Data Used for API Integrations](../Security/data-used-for-api-integrations-62f0a49.md).

    > ### Note:  
    > The steps described in the documentation refer to Identity Provisioning provided by [SAP Cloud Identity Services](https://help.sap.com/docs/IDENTITY_PROVISIONING/f48e822d6d484fa5ade7dda78b64d9f5/2d2685d469a54a56b886105a06ccdae6.html).
    > 
    > Other identity provisioning services may require a different configuration.

    > ### Remember:  
    > The login name of a user maintained in Identity Provisioning has to be identical to the user ID in SAP Advanced Financial Closing.

3.  **Optional:** Using the API documentation provided by the user interface of SAP Advanced Financial Closing, you can use the API to find and test user access management options:

    > ### Note:  
    > The preferred option is to use the SCIM API from within your identity provisioning service. Use the approach described below mainly for **testing purposes**, not for production purposes.

    1.  From SAP Advanced Financial Closing, open the *Public APIs* app.

    2.  Open *SCIM*.

    3.  On the next screen, you find all the information needed for this API.

        > ### Note:  
        > The API follows SCIM standards `7644` and `7643`. However, it has been extended by functions that you can use to manage user roles, that is, adding users to roles or removing users from them **if you don't** manage them through the groups in Identity Provisioning service.


4.  After you've configured the source and target system information, you can use runs in Identity Provisioning to synchronize users and user groups:

    Use the following source and target system assignments:


    <table>
    <tr>
    <th valign="top">

    Source System
    
    </th>
    <th valign="top">

    Target System
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    Identity Provisioning provided by SAP Cloud Identity Services or another identity provisioning service you use
    
    </td>
    <td valign="top">
    
    SAP Advanced Financial Closing
    
    </td>
    </tr>
    </table>
    
    > ### Note:  
    > The following step description refers to Identity Provisioning provided by SAP Cloud Identity Services. If you're using another identity provisioning service, follow the specific steps for the service.

    1.  Go to the *Source System Details* menu.

    2.  Go to the *Jobs* tab.

    3.  Choose *Run Now* or *Schedule* for the corresponding action.

    4.  Once the run is finished, you can find the results in the provisioning logs under *Identity Provisioning* \> *Provisioning Logs*.


5.  Special use case **synchronization of user-to-role assignments**:

    You can create user roles only in SAP Advanced Financial Closing. Using the SCIM API, you can merely update the user assignments to roles, you can't create or change the role itself. Accordingly, before you can use the SCIM API to manage user-to-role assignments, you first need to create user roles as described under [User Access Management](../User-Management/user-access-management-d974847.md). You don't need to assign users to the roles yet because you can do that using the SCIM API. Once user roles have been created, perform the following steps:

    > ### Remember:  
    > Only roles for which the *Exposed via SCIM Group* checkbox has been selected can be managed using the SCIM API.

    1.  Run a synchronization from SAP Advanced Financial Closing to the identity provisioning service.

        Use the following source and target system assignments:


        <table>
        <tr>
        <th valign="top">

        Source System
        
        </th>
        <th valign="top">

        Target System
        
        </th>
        </tr>
        <tr>
        <td valign="top">
        
        SAP Advanced Financial Closing
        
        </td>
        <td valign="top">
        
        Identity Provisioning provided by SAP Cloud Identity Services or another identity provisioning service you use
        
        </td>
        </tr>
        </table>
        
        > ### Tip:  
        > Consider using filtering options for your synchronization to influence which user roles are synchronized and subsequently available for user-to-role assignment within your identity provisioning service. Filtering options are described under [SAP Advanced Financial Closing \(Identity Provisioning documentation for source systems\)](https://help.sap.com/docs/identity-provisioning/identity-provisioning/sap-s-4hana-cloud-for-advanced-financial-closing).

        > ### Note:  
        > The following step description refers to Identity Provisioning provided by SAP Cloud Identity Services. If you use a different identity provisioning service, follow the specific steps for that service.

        1.  Go to the *Source System Details* menu.
        2.  Go to the *Jobs* tab.
        3.  Choose *Run Now* or *Schedule* for the corresponding action.
        4.  Once the run is finished, you can find the results in the provisioning logs under *Identity Provisioning* \> *Provisioning Logs*.

    2.  Add or remove user-to-role assignments in your identity provisioning service as required.

        For Identity Provisioning provided by SAP Cloud Identity Services, perform the following steps:

        1.  Go to *Users & Authorizations* \> *Groups*.
        2.  Search for the user role for which you want to change the user assignments.

            > ### Note:  
            > User roles are considered 'groups' in Identity Provisioning. However, you can differentiate user groups and roles by their type. User roles are groups of type *Authorization*.
            > 
            > We recommend that you avoid giving user roles names that are identical to or very similar to the names of user groups. Even though you can differentiate user groups and roles by their type, an identical or similar name might be confusing.

        3.  Open the user role details.
        4.  Add and remove members.

    3.  Now synchronize the changes back to SAP Advanced Financial Closing:

        > ### Caution:  
        > If you've changed the user-to-role assignments directly in SAP Advanced Financial Closing in the meantime, these changes are overwritten with the user-to-role assignments from the identity provisioning service during a synchronization.
        > 
        > **Best Practice**
        > 
        > Due to this behavior, you have two strategies available for managing user-to-role assignments:
        > 
        > -   Create user roles in SAP Advanced Financial Closing but manage all user-to-role assignments from then on using the SCIM API.
        > -   Create user roles in SAP Advanced Financial Closing and also manage all user-to-role assignments in SAP Advanced Financial Closing directly.
        > 
        > If you mix the role assignment options, inconsistencies or unwanted effects might arise.
        > 
        > However, you can also opt to use different strategies for different roles, that is, manage some user roles following the first strategy and some user roles following the second strategy. You can achieve this if you work with filtering options for your synchronization to influence which user roles are synchronized and subsequently available for user-to-role assignment within your identity provisioning service. Filtering options are described under [SAP Advanced Financial Closing \(Identity Provisioning documentation for source systems\)](https://help.sap.com/docs/identity-provisioning/identity-provisioning/sap-s-4hana-cloud-for-advanced-financial-closing).

        Use the following source and target system assignments:


        <table>
        <tr>
        <th valign="top">

        Source System
        
        </th>
        <th valign="top">

        Target System
        
        </th>
        </tr>
        <tr>
        <td valign="top">
        
        Identity Provisioning provided by SAP Cloud Identity Services or another identity provisioning service you use
        
        </td>
        <td valign="top">
        
        SAP Advanced Financial Closing
        
        </td>
        </tr>
        </table>
        
        > ### Note:  
        > The following step description refers to Identity Provisioning provided by SAP Cloud Identity Services. If you use a different identity provisioning service, follow the specific steps for that service.

        1.  Go to the *Source System Details* menu.
        2.  Go to the *Jobs* tab.
        3.  Choose *Run Now* or *Schedule* for the corresponding action.
        4.  Once the run is finished, you can find the results in the provisioning logs under *Identity Provisioning* \> *Provisioning Logs*.



**Related Information**  


[Access SAP Authorization and Trust Management Service APIs](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/ebc9113a520e495ea5fb759b9a7929f2.html)

[SAP Cloud Identity Services – Identity Provisioning](https://help.sap.com/docs/identity-provisioning/identity-provisioning/sap-cloud-identity-services-identity-provisioning)

