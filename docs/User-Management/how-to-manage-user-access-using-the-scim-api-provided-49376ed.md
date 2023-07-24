<!-- loio49376ed8c58f41e0b84d141824698721 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# How to Manage User Access Using the SCIM API Provided

Manage users, user groups, and user roles through a dedicated API.



<a name="loio49376ed8c58f41e0b84d141824698721__prereq_o2z_qx5_vvb"/>

## Prerequisites

To access the API information available from the user interface of advanced financial closing, your user must have a role collection assigned that includes the role template `AFC_API_Access`.



## Context

You can use the SCIM API to change users, user groups, and user-to-group assignments. You can also perform user-to-role assignments.

> ### Caution:  
> If you use the SCIM API, keep in mind that certain user information is case-sensitive and has to be identical between the different sources. The following user data is affected and has to be identical:
> 
> -   *User ID* in advanced financial closing
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
> Deleted users are not available through the SCIM API, even if assignments still exist in advanced financial closing.

> ### Restriction:  
> The following rate limits apply when using the SCIM API:
> 
> -   You can create a maximum of 10,000 requests per hour.
> 
> -   You can create a maximum of three requests at the same time.



## Procedure

1.  Create an API instance:

    1.  Go to the SAP BTP cockpit.

    2.  Go to the subaccount that contains the entitlement to SAP S/4HANA Cloud for advanced financial closing.

    3.  Ensure that you have enabled the *standard* service plan entitlement for SAP S/4HANA Cloud for advanced financial closing.

        For more information, see [Configure Entitlements and Quotas for Subaccounts](https://help.sap.com/docs/btp/sap-business-technology-platform/configure-entitlements-and-quotas-for-subaccounts).

    4.  From the side panel, choose *Service Marketplace*.

    5.  In the service marketplace, search for `advanced financial closing`.

    6.  Choose the *SAP S/4HANA Cloud for advanced financial closing* tile to open the details.

    7.  Go to the *Service Plans* tab.

        > ### Note:  
        > If you don't see the tab, check that you have performed the previous step to enabled the *standard* service plan entitlement for your subaccount.

    8.  In the table, look for an entry called *standard* with a description identifying it as the API for advanced financial closing that provides an SCIM interface.

    9.  Open the additional options for this entry using the *More* icon <span class="SAP-icons"></span>.

    10. Choose *Create*.

    11. In the *New Instance or Subscription* dialog, provide the following information:


        <table>
        <tr>
        <th valign="top">

        Field


        
        </th>
        <th valign="top">

        Entry


        
        </th>
        </tr>
        <tr>
        <td valign="top">
        
        *Service*


        
        </td>
        <td valign="top">
        
        Keep the default value.


        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Plan*


        
        </td>
        <td valign="top">
        
        Keep the default value.


        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Runtime Environment*


        
        </td>
        <td valign="top">
        
        Enter `Cloud Foundry`.


        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Space*


        
        </td>
        <td valign="top">
        
        Keep the default value.


        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        *Instance Name*


        
        </td>
        <td valign="top">
        
        Enter a name for this instance.


        
        </td>
        </tr>
        </table>
        

2.  Get the service key:

    > ### Tip:  
    > You can also get the service key using a command line tool. For more information about this, see [Access SAP Authorization and Trust Management Service APIs](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/ebc9113a520e495ea5fb759b9a7929f2.html).

    1.  From the side panel, choose *Instances* and find the API instance.

    2.  From the search result list, open the instance details.

    3.  In the *Service Keys* section, choose *Create*.

    4.  Open the service key credentials by clicking on the service key name.

        > ### Recommendation:  
        > Service keys hold sensitive data, such as the *clientid* and *clientsecret* elements.
        > 
        > You may want to pay attention to the security considerations described under [Data Used for SCIM API](../Security/data-used-for-scim-api-62f0a49.md).

        You can use this information for the following cases:

        -   Use the API through your preferred command line tool as described under [Access SAP Authorization and Trust Management Service APIs](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/ebc9113a520e495ea5fb759b9a7929f2.html).

        -   Use the API through your identity management, such as the Identity Provisioning service. Maintain the API information as described below.



3.  **Optional:** Maintain the API information for your source system:

    As a source system, you can use an identity authentication, for example. To do this, follow the steps described under [SAP S/4HANA Cloud for advanced financial closing \(Identity Provisioning documentation for source systems\)](https://help.sap.com/docs/identity-provisioning/identity-provisioning/sap-s-4hana-cloud-for-advanced-financial-closing).

    > ### Note:  
    > Other identity provisioning services may require a different configuration.

4.  Maintain the API information for your target system as described under [SAP S/4HANA Cloud for advanced financial closing \(Identity Provisioning documentation for target systems\)](https://help.sap.com/docs/identity-provisioning/identity-provisioning/target-sap-s-4hana-cloud-for-advanced-financial-closing).

    Some of the information you need to provide may be sensitive data for which security recommendations apply. For more information, see [Data Used for SCIM API](../Security/data-used-for-scim-api-62f0a49.md).

    > ### Note:  
    > The steps described in the documentation refer to Identity Provisioning provided by [SAP Cloud Identity Services](https://help.sap.com/docs/IDENTITY_PROVISIONING/f48e822d6d484fa5ade7dda78b64d9f5/2d2685d469a54a56b886105a06ccdae6.html).
    > 
    > Other identity provisioning services may require a different configuration.

    > ### Remember:  
    > The login name of a user maintained in Identity Provisioning has to be identical to the user ID in advanced financial closing.

5.  **Optional:** After you've configured the source and target system information, you can also use runs in Identity Provisioning to synchronize users and user groups:

    1.  Go to the *Source System Details* menu.

    2.  Go to the *Jobs* tab.

    3.  Choose *Run Now* or *Schedule* for the corresponding action.

    4.  Once the run is finished, you can find the results under the *Job Execution Details* menu.


6.  Using the API documentation provided by the user interface of advanced financial closing, you can now use the API to manage user access:

    1.  From advanced financial closing, open the *Public API* app.

    2.  Open *SCIM*.

    3.  On the next screen, you find all the information needed for this API.

        > ### Note:  
        > The API follows SCIM standards 7644 and 7643. However, it has been extended by functions that you can use to manage user roles, that is, adding users to roles or removing users from them.



**Related Information**  


[Access SAP Authorization and Trust Management Service APIs](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/ebc9113a520e495ea5fb759b9a7929f2.html)

[SAP Cloud Identity Services – Identity Provisioning](https://help.sap.com/docs/identity-provisioning/identity-provisioning/sap-cloud-identity-services-identity-provisioning)

