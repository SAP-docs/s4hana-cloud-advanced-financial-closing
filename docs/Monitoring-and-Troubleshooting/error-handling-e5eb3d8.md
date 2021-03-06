<!-- loioe5eb3d828cca43fcae562532a43c7bbd -->

# Error Handling

See how to handle issues.

Depending on what has caused the error, please do the following:

-   **Issues with the connection to the communication system**

    The communication issue can have different reasons. Perform the following steps:

    1.  Check that the settings in the *Specify Communication Systems* app are correct.

        1.  Check that the information entered for the communication system is correct.

        2.  Check that the URL information is correct. For systems that have an SAP Fiori launchpad, you can use the *Open Target SAP Fiori Launchpad* function for this. This function is available on the details page for each communication system.

        3.  Now check that the connection to the destination works. You can use the *Check Connection* function for this. This function is available on the overview page and on the details page for each communication system.


    2.  Check that the destination settings in the SAP BTP cockpit are correct. Additionally, check that the system can be reached. You do this by checking the system availability using the corresponding option in the *Actions* column.

    3.  For systems using the Cloud Connector, check that the settings in the Cloud Connector are correct. Additionally, check that the system can be reached from the Cloud Connector. You do this by checking the system availability using the corresponding option in the *Actions* column.

    4.  For SAP ERP systems, check that the settings in the SAP ERP connector for SAP S/4HANA Cloud for advanced financial closing are correct.

    5.  Check that the synchronization run between SAP S/4HANA Cloud for advanced financial closing and the communication system was successful. You can find this information in the *Monitor Business Logs* app in advanced financial closing.

    6.  If the settings are correct and the synchronization was successful, but the data isn't displayed in advanced financial closing, for example in the *Manage Closing Task Lists* app, please go to the [SAP Support Portal](https://support.sap.com) and create an incident under the component `FIN-FIO-FCC`.


-   **Issues when connecting to your on-premise communication system with the Cloud Connector**

    Please follow the instructions on how to connect to an on-premise communication system under [Connectivity](../Connectivity/connectivity-200deae.md) and the underlying topics.

-   **Issues when configuring destinations**

    Please follow the instructions under [Connectivity](../Connectivity/connectivity-200deae.md) and the underlying topics. If you still can't solve the issue, create an incident under the component `FIN-FIO-FCC` in the [SAP Support Portal](https://support.sap.com).


For all other unexpected issues, create an incident under the component `FIN-FIO-FCC` in the [SAP Support Portal](https://support.sap.com).

