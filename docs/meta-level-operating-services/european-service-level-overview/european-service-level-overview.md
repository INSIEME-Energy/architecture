---
title: S5 - European Service Level Overview
order: 5
---

## Function and Objective
Monitors and publishes service availability, reliability, and KPIs across CEEDS and Member States Data Space or Data Solutions. 

National Data Space Facilitators (NDSF) shall be responsible to provide reliable, up-to-date and correct assessments of service levels, whilst the CEEDS Facilitator shall be responsible to publish a visual overview, and machine-readable information for the operational use by European-wide actors. 

The European Service Level Overview should cover the following functionalities:
- CEEDS services self check and report,
- Registration API for period health check of CEEDS services and Participant services
- Visual dashboard for direct monitoring of the service status
- Notification mechanisms (email, SMS, direct message etc.) of the responsible in case of service degradation or intervention. The CEEDS services are responsibility of CEEDS facilitator and the National Data Spaces or National Data Platforms are the responsibility of the NDSFs.
- Establish a framework for a trusted environment by providing verifiable evidence that services and processes are functioning and executed according to agreed rules and regulations.

From DSSC point of view the service must cover:
1. **Observability** - the ability to monitor, measure and understand the internal states of processes through its outputs such as logs, metrics and traces.
1. **Traceability** - the quality of having an origin or course of development that may be found or followed.
1. **Provenance** - the place of origin or earliest known history of something. Usually it is the backwards-looking direction of a data value chain which is also referred to as provenance tracking.

| Roles | Responsibilities |
|---|---|
National Data Space Facilitator(s) (NDFS) | <ul><li>Creates National Data Space entries for observability and traceability</li><li>Registers the information with S5 - European Service Level Monitoring.</li><li>Designates contact information in case of National Data Service malfunction or interruption.</li></ul>
CEEDS Facilitator | <ul><li>Manages the observability and traceability entries.</li><li>Creates CEEDS self check entries</li><li>Designates the contacts in case of intervention and support.</li></ul>
CEEDS Participant | <ul><li>Can access and visualize the dashboard, and status reports.</li><li>Can request to register new observability and traceability entries.</li></ul>

## Business Architecture

<!-- 
The Business Architecture focuses on business requirements. It outlines the structure and operation of an organization, including business goals, functions, processes, and organizational structure. 
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

The European Service Level Overview provides services for and interacts with the following actors and systems:

| Actor/System | Description |
---|---
National Data Space Facilitator (NDSF) | The NDSF interacts with S5 via API or the Web interface allowing to define the national systems observability and traceability parameters. This includes mandatory contact for system support and service.
National Data Space / National Data Platform | Each system that interacts with CEEDS or provides specific data and/or services from a Participant at CEEDS. The system must be able to respond to check calls from S5. The NDSF will define and configure those endpoints so that the data collected for monitoring and alert by CEEDS S5 should be fully available.
CEEDS Participant | Any physical person or system that will interact with CEEDS. In particular, CEEDS must be able to register the transactions between participants for audit and traceability.
CEEDS Facilitator | A physical person that will configure the internal CEEDS services data for monitoring and traceability. The responsibility is only to CEEDS components and services, for national data spaces and national systems the NDSF is responsible.
CEEDS services | Any service that is part of CEEDS:<ul><li>S1 - CEEDS Participants Registry (CPR)</li><li>S2 - European Vocabulary Hub (EVH)</li><li>S3 - European Reference Data Registry (ERDR)</li><li>S4 - Common API for European-wide Processes (CAEP)</li><li>S6 - European Interoperability Testing Service (EITS)</li><li>S7 - EU-wide Regulated-Domain Services (ERDS)</li><li>S8 - European Data and Services Marketplace (EDSM)</li><li>Digital Customer Interface (DCI)</li></ul> Those services must implement an API allowing health check and status request.


![European Service Level Overview Business Architecture ArchiMate Diagram](./business-eslo.drawio.png)


### Service Realization Viewpoint

<!-- 
The Service Realization Viewpoint pattern creates elements that show how one or more business services are realized by the underlying processes (and sometimes by application components). 
Thus, it forms the bridge between the business products viewpoint and the business process view. It provides a "view from the outside" on one or more business processes. 
See: https://sparxsystems.com/resources/tutorials/archimate/#Service-Realization-Viewpoint
-->

![European Service Level Overview service realization ArchiMate Diagram](./app-eslo.drawio.png)


#### Component Descriptions

<!-- TODO: Insert descriptions of Realization Viewpoint components -->

| Component | Description |
|---|---|
| CEEDS register for service monitoring | The interface is available for the CEEDS Facilitator to register the status and health check information for CEEDS service and for S5 self diagnostic.
| EU-wide register for service monitoring | The interface allows the NDSFs to register the information about National Data Spaces status and health check information. The execution rights are managed by the CEEDS Facilitator. 
| Observability and traceability definition | Internal repository where all check points are stored, both CEEDS and National Data Space specific. The data collected by the execution of those controls will be processed and displayed on the dashboard.
| Dashboard and Monitoring | Application facing the users: CEEDS Participants and NDSFs designated contacts.



## Data Architecture

<!-- 
Data Architecture pertains to the management of data, both physical and logical.
It involves data assets, databases, data models, and the governance of data across the enterprise.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->
The European Service Level Overview should be able to collect data about the status and health of internal CEEDS services, including itself, and all external national data spaces or data platforms that are supposed to be available for transactions between CEEDS Participants. The services should be able to collect data for dashboards and alert generation. The CEEDS Facilitator and maintainers responsibility and intervention area is limited. For National Data Space the NDSF must designate a contact to be notified automatically and trigger the intervention to reestablish the service.


### Data Objects

<!-- TODO: Insert list/table of data objects and their descriptions -->

The data collected by the European Service Level Overview must provide a concise and clear status of the CEEDS ecosystem, both central Data Space level and national level. This includes self diagnostic data. The type of data collected is explicitly defined by either CEEDS Facilitator or by NDSFs. The data is related to:
- System status (e.g. OK/NOK)
- System health check (e.g. 200 OK, 500 INTERNAL SERVE ERROR)
- System availability (e.g. 501 NOT IMPLEMENTED, 503 SERVICE UNAVAILABLE)
- Transaction status (e.g. INITIATED, IN PROGRESS, FAILED, OK, Transaction initiated, Payment received)
- CEEDS Participant activity (e.g. Successful login, Failed authentication, Data request)

The data can be in any format: JSON, plain text, XML, log etc and should be processed and displayed in an uniform way by the tool that will be selected.

List of CEEDS services to be monitored:
- S1 - CEEDS Participants Registry
- S2 - European Vocabulary Hub
- S3 - European Reference Data Registry
- S4 - Common API for European-wide Process
- S5 - European Service Level Overview (self check and monitoring)
- S6 - EU-level Interoperability Testing Service
- S7 - EU-wide Regulated-Domain Services
- S8 - European Data and Service Marketplace
- DCI - Digital Customer Interface

The services and transactions associated with the [Reference Models](../../reference-models/reference-models.html) Deployment Procedures, that will implement: Commercial Domain Reference Procedures, Regulated Domain Reference Procedures, and Data Sharing Focused Procedures. For each of those procedures the NDSF must provide the full URL for service health check, the expected response for OK and NOK, and contact information (email) in case of NOK response. Transactions initiated by Data Space Users will
 be monitored and traced by the S5 service.

## Application Architecture

<!-- 
The Application Architecture describes individual applications and their interactions.
It addresses software applications and their role in supporting business processes and functions.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

### Application Cooperation Viewpoint

<!--
The Application Cooperation Viewpoint pattern creates elements a diagram that describe the relationships between applications components  and their locations, the services they provide or utilize and the information that flows between them.
See: https://sparxsystems.com/resources/tutorials/archimate/#Application-Cooperation-Viewpoint
-->

<!-- TODO: Insert ArchiMate Cooperation Viewpoint diagram -->

#### Component Descriptions

<!-- TODO: Insert descriptions of Application Cooperation Viewpoint components -->

## Technology Architecture

<!--
The Technology Architecture involves the IT infrastructure, including hardware, software, networks, and services.
It ensures that the infrastructure supports the application and data requirements of the business.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

The following software solutions were considered for European Service Level Overview:
- [Apache Airflow](https://airflow.apache.org/) with [n8n](https://n8n.io/), [DAG Schetch Tool](https://github.com/camilocbarrera/dst), or [EasyDAG](https://www.easydag.com/) for workflow design
- [Apache NiFi](https://nifi.apache.org/) with [n8n](https://n8n.io/)
- [Kestra](https://kestra.io/)

### Deployment View

<!-- 
The Implementation and Deployment Viewpoint pattern creates elements and a diagram that relate programs and projects to the parts of the architecture that they implement.
This view allows modeling of the scope of programs, projects, project activities in terms of the plateaus that are realized or the individual architecture elements that are affected.
In addition, the way the elements are affected may be indicated by annotating the relationships.
See: https://sparxsystems.com/resources/tutorials/archimate/#Application-Cooperation-Viewpoint
-->

<!-- TODO: Insert ArchiMate Deployment View diagram -->

#### Component Descriptions

<!-- TODO: Insert descriptions of Deployment View components -->
