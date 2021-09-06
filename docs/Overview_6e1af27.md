<!-- loio6e1af2743721420782fcb82472c9ce86 -->

# Overview



<a name="loio6e1af2743721420782fcb82472c9ce86__section_ur1_hlm_scb"/>

## About This Guide

> ### Note:  
> This documentation refers to the solution on SAP BTP. For the SAP S/4HANA Cloud version, see [Entity Close](https://help.sap.com/viewer/f28f75c165cc4626ba0359dc47edc4de/latest/en-US/5e4381c85a544720920b78d20d656a4c.html).

This administration guide describes the steps you need to perform as an administrator to set up and run SAP S/4HANA Cloud for advanced financial closing. It covers application-specific information only. For general information about SAP Business Technology Platform \(SAP BTP\), see the [documentation on the SAP Help Portal](https://help.sap.com/viewer/product/BTP).

This guide addresses the following target audience:

-   System administrators

-   Accounting experts

-   Accounting managers




<a name="loio6e1af2743721420782fcb82472c9ce86__section_ow4_5lm_scb"/>

## About SAP S/4HANA Cloud for advanced financial closing

SAP S/4HANA Cloud for advanced financial closing supports you in planning, executing, monitoring, and analyzing financial closing tasks for the entities of your group. For more information about using the functions and features provided, see the [user guide](https://help.sap.com/viewer/b3f5b9cf1ab7498fad5b6f297013d65a/latest/en-US/239ab375e0334c149082cc6851644e8b.html).

SAP S/4HANA Cloud for advanced financial closing is an SAP BTP application that runs in an SAP BTP subaccount. The SAP BTP subaccount is associated with an SAP BTP global account. Your organization may have several SAP BTP global accounts. Please clarify with your sales representative in which SAP BTP global account your entitlement to SAP S/4HANA Cloud for advanced financial closing should be contained. If you have no previous SAP BTP global account, a new one needs to be created. Your sales representative will assist you.

The following graphic shows a high-level architecture. The solution is an application on SAP BTP in the Cloud Foundry environment, which you can connect to SAP S/4HANA or SAP S/4HANA Cloud as your financial communication systems. SAP HANA is used as a database, and attachments are stored in the Object Store on SAP BTP. You must have an identity provider \(IdP\) to be able to configure your user management.

![Diagram of the solution's high-level architecture with an SAP Fiori UI, the advanced financial closing back end, the SAP HANA database, as well as the object store on SAP BTP: Either an SAP IdP or a customer IdP serves as entry point to the advanced financial closing back end. The system’s front end, back end, and databases are part of the SAP BTP subaccount for the Cloud Foundry environment on SAP side. The SAP HANA database and the object store on SAP BTP form the database component. The front end is represented by the SAP Fiori UI. The advanced financial closing back end has two communication channels: one with SAP S/4HANA Cloud on SAP side and one with the customer’s SAP BTP subaccount. The customer’s SAP BTP subaccount contains three components: subscription to advanced financial closing, security controlled through roles and role collections, and the connectivity component represented by destination service and cloud connectors. This connectivity component is connected to the customer’s SAP S/4HANA or SAP ERP system.](images/AFC_High-Level_Architecture_Diagram_726b4eb.png)

-   **[Data Flow from and to Advanced Financial Closing](Data_Flow_from_and_to_Advanced_Financial_Closing_56103b0.md "Data flow between advanced financial
                                                closing
		and connected financial communication systems.")**  
Data flow between advanced financial closing and connected financial communication systems.

