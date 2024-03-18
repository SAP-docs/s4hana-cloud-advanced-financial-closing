<!-- loio3b9f341b96864674b22e11925cb6a6bb -->

# System Landscape

Understand the system landscape of SAP Advanced Financial Closing.



<a name="loio3b9f341b96864674b22e11925cb6a6bb__section_x4j_hjp_psb"/>

## Overview

SAP Advanced Financial Closing is a cloud-based hub and can be connected to multiple system instances called communication systems. Therefore, SAP Advanced Financial Closing is only **one instance**. There is no separation into different instances for development \(D\), quality \(Q\), and production \(P\) systems. The benefit of this architecture is that financial close cycles often require spontaneous and quick changes of closing tasks. With SAP Advanced Financial Closing as a single closing hub instance, no transport mechanism or change request is needed, which enables faster reaction times.



### Content

All access and reporting can be controlled for each communication system individually.

Task list templates and task lists are created for specific communication systems and can't be reassigned to other communication systems. Nodes within the closing structure are assigned to a specific communication system upon creation.

> ### Caution:  
> The assignment can't be changed later.

In addition to the production instance of SAP Advanced Financial Closing, you can acquire an additional license to use a test tenant too. You can then connect a non-production ERP system to this tenant.

> ### Tip:  
> For information about the release times for test and production tenant, see <?sap-ot O2O class="- topic/xref " href="8256792f91704e89ac296ede87327510.xml" text="" desc="" xtrc="xref:1" xtrf="file:/home/builder/src/dita-all/crl1564036446177/loio5ac9737f9c0d44818734ea620b69186e_en-US/src/content/localization/en-us/3b9f341b96864674b22e11925cb6a6bb.xml" output-class="" outputTopicFile="file:/home/builder/tp.net.sf.dita-ot/2.3/plugins/com.elovirta.dita.markdown_1.3.0/xsl/dita2markdownImpl.xsl" ?>.

The following graphic shows the recommended system landscape if you're using a test tenant, that is, keeping the test tenant environment completely separated from the production tenant environment.

![Graphic depicting the individual communication arrangements of SAP S/4HANA Cloud for SAP Advanced Financial
                                                  Closing
								with the systems connected: On the left, the test tenant is shown
								connected to a non-production system, such as a sandbox or Q system.
								On the right, the production tenant is shown connected to three
								systems, a D system, a Q system, and a P system. Test and production
								tenant are kept completely separate.](images/Image_Map_System_Landscape_DQP_Test_Tenant_ff32915.png)

