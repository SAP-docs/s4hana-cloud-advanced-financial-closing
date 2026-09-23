<!-- loio13b0b26ff64144438369c3501a4eb239 -->

# How to Install and Configure the Cloud Connector for On-Premise Systems

If you want to connect to an external **on-premise system**, you need to install and configure the Cloud Connector as **additional software**.



## Context

The Cloud Connector serves as a link between SAP BTP applications and on-premise systems.

Accordingly, if your external system is an **on-premise system**, you need to install the Cloud Connector to enable the communication between your system and SAP Advanced Financial Closing. For non-on-premise systems, the Cloud Connector is not required.



<a name="loio13b0b26ff64144438369c3501a4eb239__steps_kvd_3xr_1pb"/>

## Procedure

1.  Install the Cloud Connector following the relevant procedure for your operating system as described under [Cloud Connector Installation](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/57ae3d62f63440f7952e57bfcef948d3.html?&locale=en-US).

2.  Perform the initial configuration steps described under [Initial Configuration](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/db9170a7d97610148537d5a84bf79ba2.html).

    > ### Note:  
    > You can't use port 443 as virtual host for your destination.

3.  Connect your subaccounts to the Cloud Connector as described under [Managing Subaccounts](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/f16df12fab9f4fe1b8a4122f0fd54b6e.html?&locale=en-US).

    If needed, you can find information about how to use more than one system with the Cloud Connector under [Set Up an HTTP Destination](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/create-http-destinations).

    > ### Remember:  
    > You can't use port 443 as virtual host for your destination.




<a name="loio13b0b26ff64144438369c3501a4eb239__result_egy_vtr_1pb"/>

## Results

You have now installed and configured the Cloud Connector.

**Parent topic:**[External Systems](external-systems-9ca3083.md "Connect to your external financial system to retrieve information about organizational units, the factory calendar, and so on.")

**Previous:**[How to Create the Destination in the SAP BTP Cockpit](how-to-create-the-destination-in-the-sap-btp-cockpit-4916c1e.md "Create a destination for your external system in your SAP BTP cockpit.")

