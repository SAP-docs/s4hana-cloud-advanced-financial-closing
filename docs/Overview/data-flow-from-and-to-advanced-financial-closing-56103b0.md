<!-- loio56103b05a24d4347b58e7e52c53f3e63 -->

# Data Flow from and to Advanced Financial Closing

Understand the data flow between advanced financial closing and connected financial communication systems.

After you've connected your financial communication system to SAP S/4HANA Cloud for advanced financial closing, data is sent between both systems. See the graphic below for more information.

 ![Graphic depicting the data flow between advanced financial closing on the SAP Business Technology Platform and the connected financial communication systems. The following data is sent from the financial communication systems to advanced financial closing: organizational data, accounting principles, ledgers, factory calendars, job results (except for spool lists), spool lists (display-only), task models, and task list models. Additionally, SAP S/4HANA and SAP ERP spools are saved in dedicated tables of the financial communication systems. No financial data is replicated. The following data is sent from advanced financial closing to the financial communication systems: triggers to schedule background jobs, parameterization for SAP Fiori applications for intent-based navigation, and authorization data for access checks in the financial communication systems.](images/Image_Data_Flow_Between_AFC_and_Communication_Systems_a5ce2a0.png) 

