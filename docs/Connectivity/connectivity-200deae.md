<!-- loio200deaea523b48da939c33fcf8f2e0e4 -->

# Connectivity

Connect your financial cloud or on-premise systems to SAP S/4HANA Cloud for advanced financial closing.

You can connect SAP S/4HANA Cloud for advanced financial closing to the following solutions:

-   SAP S/4HANA Cloud

-   SAP S/4HANA 1809 SPS04 and higher

-   SAP S/4HANA 1909 FPS02 and higher

-   SAP S/4HANA 2020 and all following releases

-   SAP ERP 6.0, enhancement package 4 and higher


> ### Note:  
> Some functions may be available only as of higher SPs or back-end releases.

For more information about connectivity, see the SAP BTP documentation under [Connectivity in the Cloud Foundry Environment](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/34010ace6ac84574a4ad02f5055d3597.html).



<a name="loio200deaea523b48da939c33fcf8f2e0e4__section_j4f_b4j_rkb"/>

## Use

The connection allows you to do the following, for example:

-   In the *Manage Closing Task Lists* app:

    -   You can define a default financial communication system for your task list templates. Business attributes, such as the factory calendar or ledger, are then governed by default by the financial communication system specified and are incorporated into the task list template.


-   In the *Process Closing Tasks* app:

    -   When you process tasks of type *SAP Fiori Application* in a task list defined for the respective communication system, you’re automatically forwarded to the app in the respective system's launchpad.

        > ### Note:  
        > If the closing business transaction type refers to a transaction and not to a semantic object and action, you automatically navigate to the transaction rendered as html GUI. In this case, the following rules apply:
        > 
        > -   The Internet Transaction Server \(ITS\) has to be active in your communication system. This is set up by default.
        > 
        > -   The user processing the task needs to have a user in the communication system and be authenticated, ideally using single sign-on \(SSO\).
        > 
        > -   Context parameters such as fiscal year, fiscal year period and company code are **not** handed over to the target window.


    -   When you process tasks of type *Job* that are run in the communication system, the status and results of these scheduling jobs are returned to SAP S/4HANA Cloud for advanced financial closing. You can see the details for each task in the *Monitor Business Logs* app. For more information, see [Logging](../Monitoring-and-Troubleshooting/logging-57375b8.md).



-   **[SAP S/4HANA Cloud](sap-s-4hana-cloud-60448a7.md "Depending on your system, follow one of the instructions listed here to connect SAP S/4HANA Cloud for advanced financial closing to your SAP S/4HANA Cloud system.")**  
Depending on your system, follow one of the instructions listed here to connect SAP S/4HANA Cloud for advanced financial closing to your SAP S/4HANA Cloud system.
-   **[SAP S/4HANA](sap-s-4hana-15a3a5b.md "Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP S/4HANA system. Perform the last
		two steps only if they apply to your use case.")**  
Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP S/4HANA system. Perform the last two steps only if they apply to your use case.
-   **[SAP ERP](sap-erp-7b85121.md "Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP ERP system. Perform the last
		step only if it applies to your use case.")**  
Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP ERP system. Perform the last step only if it applies to your use case.
-   **[How to Delete the Connection to a Communication System](how-to-delete-the-connection-to-a-communication-system-9c0a0d9.md "Delete the connection between advanced financial
                                                closing and the communication
		system.")**  
Delete the connection between advanced financial closing and the communication system.
-   **[Monitor Communication Systems](monitor-communication-systems-a215069.md "You use the Monitor Communication
                                                                           Systems app to check the status of your connected communication systems and tackle any
		issues.")**  
You use the *Monitor Communication Systems* app to check the status of your connected communication systems and tackle any issues.
-   **[Synchronization of Communication Systems](synchronization-of-communication-systems-a86348d.md "Get an overview of the synchronization and validation of data.")**  
Get an overview of the synchronization and validation of data.

