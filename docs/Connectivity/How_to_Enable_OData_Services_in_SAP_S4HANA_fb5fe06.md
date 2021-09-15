<!-- loiofb5fe06295fd493f80e89df3a9c57b7a -->

# How to Enable OData Services in SAP S/4HANA

Enable OData services to be able to connect SAP S/4HANA to SAP S/4HANA Cloud for advanced financial closing.



## Context

The administrator of your SAP S/4HANA system needs to perform the following steps to enable OData Services and check the virus scan profile to ensure the connection works.



## Procedure

1.  **Enabling OData Services**
2.  In the SAP Reference IMG \(transaction `SPRO`\) of your SAP S/4HANA system, navigate to *SAP NetWeaver* \> *SAP Gateway* \> *OData Channel* \> *Administration* \> *General Settings* \> *Activate and Maintain Services*

3.  Choose *Add Service*.

4.  In the *Filter* section, make the following entries and press [Enter\]:

    -   *System Alias*: for example, ***LOCAL***

    -   *External Service Name*: ***FCCX\_COMMUNICATION\_SERVICES***

    > ### Note:  
    > The *System Alias* refers to the RFC Destination that points to the system where your service is running.

5.  Select the service and choose *Add Selected Services*.

6.  On the *Add Service* screen, you can change the technical service name. However, it is recommended that you keep the default setting: *****ZFCCX\_COMMUNICATION\_SERVICES*****.

7.  On the *Activate and Maintain Services* screen, you can test the service by double-clicking it and choosing *Call Browser*. Please note down the URL.

8.  **Checking Virus Scan Profile**
9.  In the SAP Reference IMG \(transaction `SPRO`\) of your SAP S/4HANA system, navigate to *SAP NetWeaver* \> *SAP Gateway* \> *OData Channel* \> *Administration* \> *General Settings* \> *Define Virus Scan Profiles*.

10. Under *V2 Virus Scan Options*, check that a virus scan profile is selected and that the *Virus Scan Switched Off* option is **not** selected.

11. Open transaction `VSCAN` and check whether a virus scan definition is maintained.

    1.  If none is maintained, maintain a definition.

        For more information, see [Setting Up a Virus Scan Provider \(ABAP\)](https://help.sap.com/viewer/3cd5ac93e7ec4690bd804f0d23fed9da/latest/en-US/4df582ed472d41c4e10000000a42189c.html).

    2.  If you can't maintain a definition, go to the virus scan profile as described in the previous steps and select the *Virus Scan Switched Off* option.




<a name="loiofb5fe06295fd493f80e89df3a9c57b7a__postreq_x2m_hgz_mlb"/>

## Next Steps

Provide the system administrator of advanced financial closing with the URL you've just copied when you called up the browser.

**Parent topicColonSymbol** [SAP S/4HANA](SAP_S4HANA_15a3a5b.md "Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP S/4HANA system. Perform the last two steps only if they apply to your use case.")

**Previous topicColonSymbol** [How to Install and Configure the Cloud Connector](How_to_Install_and_Configure_the_Cloud_Connector_4cf0fb0.md "If you want to connect to SAP S/4HANA, you need to install and configure the Cloud Connector as additional software.")

**Next topicColonSymbol** [How to Create a Technical Communication User](How_to_Create_a_Technical_Communication_User_c4a9b51.md "Create a technical communication user for your SAP S/4HANA system.")

