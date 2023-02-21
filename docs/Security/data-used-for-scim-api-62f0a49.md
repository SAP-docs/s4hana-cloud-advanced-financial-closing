<!-- loio62f0a49c5206431ebea7a4b06c43b3b5 -->

# Data Used for SCIM API

Security considerations for data relevant for the use of the SCIM API.



<a name="loio62f0a49c5206431ebea7a4b06c43b3b5__section_dpp_4hf_jwb"/>

## Context

For SAP S/4HANA Cloud for advanced financial closing, you can use an SCIM API to manage users as described under [How to Manage User Access Using the SCIM API Provided](../User-Management/how-to-manage-user-access-using-the-scim-api-provided-49376ed.md).



<a name="loio62f0a49c5206431ebea7a4b06c43b3b5__section_wby_b3f_jwb"/>

## Sensitive Data Used for SCIM API

When using the SCIM API, you need to enter a client ID and a client secret. The *clientid* and *clientsecret* elements of API service keys are sensitive data. Therefore, SAP recommends keeping the data safe and performing regular secret rotations.

