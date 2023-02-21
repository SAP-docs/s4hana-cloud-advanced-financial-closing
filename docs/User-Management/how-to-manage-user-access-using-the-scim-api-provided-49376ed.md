<!-- loio49376ed8c58f41e0b84d141824698721 -->

<link rel="stylesheet" type="text/css" href="../css/sap-icons.css"/>

# How to Manage User Access Using the SCIM API Provided

Manage users, user groups, and user roles through a dedicated API.



<a name="loio49376ed8c58f41e0b84d141824698721__prereq_o2z_qx5_vvb"/>

## Prerequisites

To access the API information available through the user interface of advanced financial closing, your user must have a role collection assigned that includes the role template `AFC_API_Access`.



## Context

You can use the SCIM API to change users, user groups, and user-to-group assignments. You can also perform user-to-role assignments.

> ### Caution:  
> If you use the SCIM API, keep in mind that certain user information is case-sensitive and has to be identical between the different sources. The following user data is affected and has to be identical:
> 
> -   *User ID* in advanced financial closing
> 
> -   *User ID* used in CSV upload of user data
> 
> -   *Login Name* in identity service
> 
> -   *Subject Name Identifier* in IDP / XSUAA
> 
> 
> If this information isn't identical although the data is referring to the same user, multiple users will be maintained.

> ### Note:  
> User-to-role assignments can be maintained for scoped user roles only, since they're part of the new authorization concept. Assignments to user roles that are part of the old authorization concept aren't possible.
> 
> Deleted users are not available through the SCIM API, even if assignments in advanced financial closing still exist.

> ### Restriction:  
> The following rate limits apply when using the SCIM API:
> 
> -   You can create a maximum of 10,000 requests per hour.
> 
> -   You can create a maximum of three requests at the same time.



## Procedure

1.  Create an API instance:

    1.  Go to the SAP BTP cockpit.

    2.  Go to the account that contains the entitlement to SAP S/4HANA Cloud for advanced financial closing.

    3.  From the side panel, choose *Service Marketplace*.

    4.  In the service marketplace, search for ***advanced financial closing***.

    5.  Choose the *SAP S/4HANA Cloud for advanced financial closing* tile to open the details.

    6.  Go to the *Service Plans* tab.

    7.  In the table, you find an entry called *standard* and a description identifying it as API for advanced financial closing that provides an SCIM interface.

    8.  Open the additional options for this entry using the *More* icon <span class="SAP-icons"></span>.

    9.  Choose *Create*.


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

        -   Use the API through your preferred command-line tool as described under [Access SAP Authorization and Trust Management Service APIs](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/ebc9113a520e495ea5fb759b9a7929f2.html).

        -   Use the API through your identity management, such as the Identity Provisioning service. Maintain the API information as described below.



3.  \(Optional\) Maintain the API information for your source system:

    As source system, you can, for example, use an identity authentication. To do this, follow the steps described under [Identity Authentication](https://help.sap.com/docs/IDENTITY_PROVISIONING/f48e822d6d484fa5ade7dda78b64d9f5/e4e25f1fae094c2a89ad62159e1cd230.html).

    > ### Note:  
    > Other identity provisioning services may require a different configuration.

4.  Maintain the API information for your target system:

    The steps described here refer to Identity Provisioning provided by [SAP Cloud Identity Services](https://help.sap.com/docs/IDENTITY_PROVISIONING/f48e822d6d484fa5ade7dda78b64d9f5/2d2685d469a54a56b886105a06ccdae6.html).

    > ### Note:  
    > Other identity provisioning services may require a different configuration.

    > ### Remember:  
    > The login name of a user maintained in Identity Provisioning has to be identical to the user ID in advanced financial closing.

    1.  Follow the steps described under [SCIM System](https://help.sap.com/docs/IDENTITY_PROVISIONING/f48e822d6d484fa5ade7dda78b64d9f5/04278923ec8b4b34ac912897062be317.html).

    2.  For the properties referred to, enter the following information:

        **Mandatory Properties**


        <table>
        <tr>
        <th valign="top">

        Property Name


        
        </th>
        <th valign="top">

        Value


        
        </th>
        </tr>
        <tr>
        <td valign="top">

        `Type`


        
        </td>
        <td valign="top">

        ***HTTP***


        
        </td>
        </tr>
        <tr>
        <td valign="top">

        `URL`


        
        </td>
        <td valign="top">

        Enter the URL provided by the service key under *"endpoints"* \> *"scim2"*.


        
        </td>
        </tr>
        <tr>
        <td valign="top">

        `ProxyType`


        
        </td>
        <td valign="top">

        ***Internet***


        
        </td>
        </tr>
        <tr>
        <td valign="top">

        `Authentication`


        
        </td>
        <td valign="top">

        ***BasicAuthentication***


        
        </td>
        </tr>
        <tr>
        <td valign="top">

        `User`


        
        </td>
        <td valign="top">

        Enter the user ID provided by the service key under *"uaa"* \> *"clientid"*.


        
        </td>
        </tr>
        <tr>
        <td valign="top">

        `Password`


        
        </td>
        <td valign="top">

        Enter the password provided by the service key under *"uaa"* \> *"clientsecret"*.


        
        </td>
        </tr>
        <tr>
        <td valign="top">

        `OAuth2TokenServiceURL`


        
        </td>
        <td valign="top">

        Enter the following URL concatenation:

        -   Enter the URL provided by the service key under *"uaa"* \> *"url"*.

        -   Add the following suffix: ***/oauth/token***


        > ### Example:  
        > The URL provided by the service key is *www.example.com*.
        > 
        > Accordingly, you enter the following value in your identity management:
        > 
        > ***www.example.com/oauth/token***


        
        </td>
        </tr>
        </table>
        
        > ### Note:  
        > Some of the information you need to provide may be sensitive data for which security recommendations apply. For more information, see [Data Used for SCIM API](../Security/data-used-for-scim-api-62f0a49.md).

    3.  \(Optional\) The SCIM implementation offers further possibilities that you can leverage with the following modifications to the target system properties, you've maintained. To perform any of the following modifications, go to the *Transformations* tab in your target system details:

        -   **Enterprise User:** To transfer enterprise user information, remove the following section under *user* \> *menu*:

            ```
            {
            "targetPath": "$['urn:ietf:params:scim:schemas:extension:enterprise:2.0:User']",
            "type": "remove"
            }
            ```

        -   **Groups:** To synchronize groups, remove the following indicator in the *group* section:

            ```
            "ignore": true
            ```


        If you've performed both modifications, the overall transformation looks as follows:

        ```
        {
          "user": {
            "mappings": [
              {
                "sourcePath": "$",
                "targetPath": "$"
              },
              {
                "targetPath": "$.id",
                "type": "remove"
              },
              {
                "sourceVariable": "entityIdTargetSystem",
                "targetPath": "$.id"
              },
              {
                "condition": "$.emails[0].length() > 0",
                "constant": true,
                "targetPath": "$.emails[0].primary"
              }
            ]
          },
          "group": {
            "mappings": [
              {
                "sourcePath": "$",
                "targetPath": "$"
              },
              {
                "targetPath": "$.id",
                "type": "remove"
              },
              {
                "sourceVariable": "entityIdTargetSystem",
                "targetPath": "$.id"
              },
              {
                "targetPath": "$.members",
                "type": "remove"
              },
              {
                "sourcePath": "$.members[*].value",
                "preserveArrayWithSingleElement": true,
                "optional": true,
                "targetPath": "$.members[?(@.value)]",
                "functions": [
                  {
                    "type": "resolveEntityIds"
                  }
                ]
              }
            ]
          }
        }
        ```


5.  \(Optional\) After you've configured the source and target system information, you can also use runs in Identity Provisioning to synchronize users and user groups:

    1.  Go to the *Source System Details* menu.

    2.  Go to the *Jobs* tab.

    3.  Choose *Run Now* or *Schedule* for the corresponding action.

    4.  Once the run is finished, you can find the results under the *Job Execution Details* menu.


6.  Using the API documentation provided through the user interface of advanced financial closing, you can now use the API to manage user access:

    1.  In advanced financial closing, go to the *Public API* app.

    2.  Open *SCIM*.

    3.  On the next screen, you find all the information needed for this API.

        > ### Note:  
        > The API follows SCIM standard 7644 and 7643. However, it has been extended by functions to manage user roles, that is, adding users to roles or removing user from them.



**Related Information**  


[Access SAP Authorization and Trust Management Service APIs](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/ebc9113a520e495ea5fb759b9a7929f2.html)

[SCIM System](https://help.sap.com/docs/IDENTITY_PROVISIONING/f48e822d6d484fa5ade7dda78b64d9f5/04278923ec8b4b34ac912897062be317.html)

