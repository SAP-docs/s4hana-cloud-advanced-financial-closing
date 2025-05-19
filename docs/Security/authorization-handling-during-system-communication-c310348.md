<!-- loioc3103486249048fc8b75fe731fa60dc9 -->

# Authorization Handling During System Communication

Authorization handling during communication with an on-premise system.



## Context

During communication between the SAP Advanced Financial Closing back end and the connected SAP S/4HANA or SAP ERP communication system, the following two types of user come into play:

-   **Business user**:

    The business user identifies the individual end user.

-   **Technical communication user**:

    The technical communication user is used by the SAP Advanced Financial Closing back end to access the communication system.




<a name="loioc3103486249048fc8b75fe731fa60dc9__section_yvs_dwy_bfc"/>

## Authorization Process

To enable communication with the connected communication system, the following process comes into play:

1.  The SAP Advanced Financial Closing back end **requires the technical communication user data**, which gives access to the communication system. It receives this information from the destination service. \(Steps 1 and 2 in graphic below\)
2.  Since the technical communication user potentially has more authorizations in the communication system than the individual user has, the communication system in turn requires the business user information and the corresponding authorizations so as to **restrict access accordingly**.

    Therefore, the SAP Advanced Financial Closing back end **attaches the business user information** when it uses the technical communication user information to obtain authentication from the communication system. \(Steps 3 and 4 in graphic below\)

3.  The communication system **confirms** that the technical communication user is valid and then **checks the business user information** to restrict access. \(Steps 5 through 7 in graphic below\)

The following graphic depicts this connection:

![The communication process between the SAP Advanced Financial Closing back end and on-premise communication system consists of different steps as described in the paragraphs above.](images/Image_Authorization_Flow_d5b02dd.png)

