<!-- loioc4a9b51a49c5411eadeb7f7208b6b9cc -->

# How to Create a Technical Communication User

Create a technical communication user for your SAP S/4HANA system.



## Context

You need to create a technical communication user with specific authorizations to enable the connection between advanced financial closing and the communication system. The required authorizations can't be granted by assigning the technical communication user to a `SAPALL` profile. Instead, the technical communication user needs to have a specific `PFCG` role assigned as described here.



## Procedure

1.  In your communication system, open transaction `PFCG`.

2.  Enter an ID for the role and choose *Single Role*.

3.  Enter a description and choose *Save*.

4.  In change mode, go to the *Menu* tab and choose *Insert*.

5.  Go to *Edit* \> *Insert Authorization Default*.

6.  \(Only applicable if gateway and business back-end system are the same\) Under *Default Authorization*, select ***SAP Gateway: Service Group Metadata***.

    The following information is filled out automatically:


    <table>
    <tr>
    <th>

    Program ID


    
    </th>
    <th>

    Object Type


    
    </th>
    </tr>
    <tr>
    <td>

    `R3TR`


    
    </td>
    <td>

    `IWSG`


    
    </td>
    </tr>
    </table>
    
    1.  Under *TADIR Service*, use the value help and search for the technical service name that was used during service activation as described under [How to Enable OData Services in SAP S/4HANA](How_to_Enable_OData_Services_in_SAP_S4HANA_fb5fe06.md). For example, the default *****\[ZFCCX\_COMMUNICATION\_SERVICES\_SRV\]\******.

7.  Under *Default Authorization*, select ***SAP Gateway Business Suite Enablement - Service***.

    The following information is filled out automatically:


    <table>
    <tr>
    <th>

    Program ID


    
    </th>
    <th>

    Object Type


    
    </th>
    </tr>
    <tr>
    <td>

    `R3TR`


    
    </td>
    <td>

    `IWSV`


    
    </td>
    </tr>
    </table>
    
    1.  Under *TADIR Service*, use the value help and search for ***FCCX\_COMMUNICATION\_SERVICES\_SRV 0001***, and apply this service.

    2.  Choose *Copy*.

8.  For this last authorization, the *OP Variant* needs to have been selected on the *Applications* tab if this is supported by your release:


    <table>
    <tr>
    <th>

    Active


    
    </th>
    <th>

    Type


    
    </th>
    <th>

    Name


    
    </th>
    <th>

    Variant


    
    </th>
    <th>

    Description


    
    </th>
    </tr>
    <tr>
    <td>

    ***Selected***


    
    </td>
    <td>

    SAP Gateway Business Suite Enablement - Service


    
    </td>
    <td>

    FCCX\_COMMUNICATION\_SERVICES\_SRV 0001


    
    </td>
    <td>

    FCCX\_COMMUNICATION\_SERVICES\_SRVO


    
    </td>
    <td>

    `OP Variant`


    
    </td>
    </tr>
    </table>
    
9.  The following authorization object needs to be maintained:


    <table>
    <tr>
    <th>

    Authorization Object


    
    </th>
    <th>

    Field Name \(Heading\)


    
    </th>
    <th>

    Value


    
    </th>
    </tr>
    <tr>
    <td rowspan="2">

    `S_BTCH_NA1`


    
    </td>
    <td>

    `PROGRAM`


    
    </td>
    <td>

    `FCCX_APJ_PROCESSOR`


    
    </td>
    </tr>
    <tr>
    <td>

    `BTCUNAME`: *Background User Name for Authorization Check*


    
    </td>
    <td>

    Enter one of the following:

    -   `*`: Using the asterisk, you ensure that you don't have to list all relevant users explicitly.

    -   List all relevant business users explicitly.


    
    </td>
    </tr>
    </table>
    
10. On the *User* tab, add the technical communication user.

    > ### Note:  
    > If you use separate systems for the gateway back end and the business back end, the users created for both systems must be dialog users. These users require authorization object `S_RFCACL`. Depending on your release, this object is provided with the default authorization *SAP Gateway Business Suite Enablement - Service*.

    > ### Tip:  
    > It's not recommended to add any other or additional profiles to the technical communication user.

11. Save the role.




<a name="loioc4a9b51a49c5411eadeb7f7208b6b9cc__result_ktt_rxz_4pb"/>

## Results

You have now created a technical communication user that can be used to connect your communication system to SAP S/4HANA Cloud for advanced financial closing.



<a name="loioc4a9b51a49c5411eadeb7f7208b6b9cc__postreq_n4n_hqz_4pb"/>

## Next Steps

Provide your BTP account administrator for advanced financial closing with the information of the technical communication user.

**Parent topicColonSymbol** [SAP S/4HANA](SAP_S4HANA_15a3a5b.md "Perform the following steps to connect SAP S/4HANA Cloud for advanced financial closing to your SAP S/4HANA system. Perform the last two steps only if they apply to your use case.")

**Previous topicColonSymbol** [How to Enable OData Services in SAP S/4HANA](How_to_Enable_OData_Services_in_SAP_S4HANA_fb5fe06.md "Enable OData services to be able to connect SAP S/4HANA to SAP S/4HANA Cloud for advanced financial closing.")

**Next topicColonSymbol** [How to Create a Destination in the SAP BTP Cockpit](How_to_Create_a_Destination_in_the_SAP_BTP_Cockpit_5c2b2f0.md "Create a destination for your SAP S/4HANA system in your SAP BTP cockpit.")

