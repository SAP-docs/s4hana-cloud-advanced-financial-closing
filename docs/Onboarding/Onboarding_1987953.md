<!-- loio1987953b694f4f80a63fab2d4e31f19d -->

# Onboarding

Add SAP S/4HANA Cloud for advanced financial closing to your global account and subscribe to the product.



<a name="loio1987953b694f4f80a63fab2d4e31f19d__prereq_rxp_5qb_l4b"/>

## Prerequisites

-   You have already received the email from SAP Business Technology Platform with the technical information regarding your global account for SAP S/4HANA Cloud for advanced financial closing.




## Procedure

1.  Follow the link in the email to get to the SAP BTP cockpit.

    > ### Note:  
    > Initially, only the receiver or receivers of the email have the required authorization to perform these steps. The receiver or receivers of the email are maintained under *Parties Involved* \> *Contact Person IT*.

2.  Choose the global account for which you received the email.

    > ### Note:  
    > If your organization has multiple global accounts, be sure to choose the global account that contains the entitlement to SAP S/4HANA Cloud for advanced financial closing. This account is mentioned in the email you've received.

3.  Add members to your global account. Go to *Members* and choose *Add Members*. Add the relevant members in the dialog box. Choose the ID format according to the IdP you use.

4.  Go to *Subaccounts* and choose *New Subaccount*:

    Create the relevant subaccounts in your global account. On global account level, the number of subscriptions for this application is limited. Specifically, you can subscribe only once to SAP S/4HANA Cloud for advanced financial closing in your global account.

5.  Provide the following information for each subaccount you create and choose *Create*:

    1.  *Display Name*

    2.  *Description*

    3.  *Environment*

    4.  *Provider*

    5.  *Region*:

        The combination of provider and region represents the data center you are using.

        > ### Note:  
        > For SAP S/4HANA Cloud for advanced financial closing, the subaccount needs to be in the same region as the application. Currently `Europe (Frankfurt) (cf-eu10)` and `US (Virginia) (cf-us10)` are available as regions.

    6.  *Subdomain*:

        The subdomain name must be unique for each data center. Therefore, we strongly recommend including a **customer-specific prefix** in the name of the subdomain. Please note that this subdomain is later part of your URL with which you access the application in the browser and also part of the API URL that you provide to your external trading platform.

    > ### Example:  
    > Your subaccount details could look something like this:
    > 
    > -   Display Name: ***AFC Prod***
    > 
    > -   Description: ***Subscribed to SAP S/4HANA Cloud for advanced financial closing - Prod***
    > 
    > -   Environment: ***Cloud Foundry***
    > 
    > -   Provider: ***AWS***
    > 
    > -   Region: ***Europe \(Frankfurt\) \(cf-eu10\)***
    > 
    > -   Subdomain: ***\[CustomerNameAbbreviation\]-afc-prod***

6.  Enable **Cloud Foundry** in your subaccount and provide a name for the organization. We recommend that you use the same name that you used for the subdomain, for example \[CustomerNameAbbreviation\]-afc-prod.

7.  Subscribe to the relevant services.

    1.  Go to *Services* \> *Service Marketplace*, choose the SAP S/4HANA Cloud for advanced financial closing tile, and then choose *Create*.

    2.  In the wizard, select a subscription type and choose *Create*.

    3.  In the confirmation popup, follow the link to the *Instances and Subscriptions* page. Here you can see the status of your subscription.

        > ### Tip:  
        > On this screen, you can also call up your base URL by choosing the link *Go to Application*. You find the link in the *Subscriptions* table overflow menu.


**Related Information**  


[Log On to Your Global Account \(SAP BTP documentation\)](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/latest/en-US/77be28886328492086ab07c003cb8d37.html)

[Subscribe to Multitenant Business Applications in the Cloud Foundry Environment Using the Cockpit \(SAP BTP documentation\)](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/7a3e39622be14413b2a4df7c02ca1170.html)

[Creating Service Instances in Cloud Foundry \(SAP Cloud Service Management Service documentation\)](https://help.sap.com/viewer/09cc82baadc542a688176dce601398de/latest/en-US/6d6846def3c443aa9f83d127353147ce.html)

