<!-- loio3b9f341b96864674b22e11925cb6a6bb -->

# System Landscape

Understand the system landscape of SAP S/4HANA Cloud for advanced financial closing.



<a name="loio3b9f341b96864674b22e11925cb6a6bb__section_x4j_hjp_psb"/>

## Overview

SAP S/4HANA Cloud for advanced financial closing is a cloud-based hub and can be connected to multiple system instances called communication systems. Therefore, advanced financial closing is only **one instance**. There is no separation into different instances for development \(D\), quality \(Q\), and production \(P\) systems. The benefit of this architecture is that financial close cycles often require spontaneous and quick changes of closing tasks. With advanced financial closing as a single closing hub instance, no transport mechanism or change request is needed, which enables faster reaction times.



### Content

All access and reporting can be controlled for each communication system individually.

Task list templates and task lists are created for specific communication systems and can't be reassigned to other communication systems. Nodes within the closing structure are assigned to a specific communication system upon creation.

> ### Caution:  
> The assignment can't be changed later.

In addition to the production instance of advanced financial closing, you can acquire an additional license to use a test tenant too. You can then connect a sandbox ERP system to this tenant.

The following graphic shows the recommended system landscape if you're using a test tenant, that is, keeping the test tenant environment completely separated from the production tenant environment.

Some areas of this image are interactive. Hover over the areas for a description.

![Graphic depicting the individual communication arrangements of SAP
								S/4HANA Cloud for advanced financial closing with the systems
								connected: On the left, the test tenant is shown connected to a
								sandbox system. On the right, the production tenant is shown
								connected to three systems, a D system, a Q system, and a P system.
								Test and production tenant are kept completely separate.](images/Image_Map_System_Landscape_DQP_Test_Tenant_ff32915.png)

