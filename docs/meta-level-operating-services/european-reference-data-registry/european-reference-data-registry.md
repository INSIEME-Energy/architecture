---
title: S3 - European Reference Data Registry
order: 3
---


## Function and Objective

Hosts certified reference data on roles, actors, and market infrastructures essential for automation.

Typically, this structural data (e.g. lists of important data on Permission Administrators, DSOs or Market Platforms) is highly needed to guarantee an efficient functioning of automated solutions
within the scope of CEEDS. The lack of accessibility of this data places a huge gap for data-driven energy markets as of now (see Deliverable 5.2 of Project EDDIE).

CEEDS Facilitator is responsible to provide standardized interfaces in a Common Information Model for National Data Space Facilitators (NDSF) to provide that data in a standardized manner, as well as
keeping audits and versioning. NDSFs should be responsible to collect and maintain updates of the reference data, and to certify its correctness.

Based on DSSC business and organisational building blocks the motivation for an European Reference Data Registry can be resumed by:
- **Use Case Development**: Data space use cases are settings where two or more participants create business, societal or environmental value from data sharing. Use case development amplifies such value of a data space.
- **Data Space Offering**: The data space offering consists of the set of offerings available in a data space to participants. Offerings contain data product(s), service(s), and the offering description that provides all the information needed for a potential consumer to make a decision whether to consume the data product(s) and/or the service(s) or not.

The main technical building blocks adressed by European Reference Data Registy are:
- **Data Models**: Data models ensure that data is accurately and consistently interpreted when exchanged within a data space. The data model consists of metadata that provides information about semantics, helping to interpret the actual exchanged data. Versioning and version management is a must have functionality for Data Models management.
- **Provenance and traceability**: additional metadata alongside the shared data for auditing and compliance purposes might be required.  

The main functions:
- metadata definition and management, including explicit versioning
- energy market refrence data model representation, maintenance by CEEDS Operator
- reference data model access for CEEDS Participants
- national reference data model definition and management can be maintained by National Data Space Facilitator (NDSF)
- enhancement and mapping of national reference data model to European reference data model will be under the responsiblity of National Data Space Facilitator (NDSF)

## Business Architecture

<!-- 
The Business Architecture focuses on business requirements. It outlines the structure and operation of an organization, including business goals, functions, processes, and organizational structure. 
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

The main actors and systems interacting with European Reference Data Registry service:

Actor/System | Description
---|---
National Data Space Facilitators (NDSF) | Actor responsible for National Data Space management, in particular the definition and maintenance of the specific metadata that can be shared with CEEDS Participants about national data models. The NDSF has access via the National Reference Data Maintenance Service. NDSF are responsible for providing and maintaing updates of the mappings of national data models to common European data model. 
CEEDS Facilitator | Actor having access to the European Referecne Data Registry interface for metadata management. This includes data catalog, service catalog, access management, rights management. The main responsibilit is to define and enhance European refrerence data standard model.
CEEDS Participant | Participant having access to the services related to common European reference data model.
Energy Market Referecne Data | A collection of reference data specific to each national data space used to aggregate specific code lists, taxonomies, schemas, data models.
S3 - European Reference Data Registry | CEEDS service providing access to common European reference data model to CEEDS Participants.

![European Reference Data Registry Service Business Architecture](./business-erdr.drawio.png)



### Service Realization Viewpoint

<!-- 
The Service Realization Viewpoint pattern creates elements that show how one or more business services are realized by the underlying processes (and sometimes by application components). 
Thus, it forms the bridge between the business products viewpoint and the business process view. It provides a "view from the outside" on one or more business processes. 
See: https://sparxsystems.com/resources/tutorials/archimate/#Service-Realization-Viewpoint
-->
![European Reference Data Registry Service Realisation Architecture](./app-erdr.drawio.png)
<!--
<img width="1336" height="902" alt="image" src="https://github.com/user-attachments/assets/574af7c8-876d-4ccd-816f-bb252c7fae51" />
-->
#### Component Descriptions

<!-- TODO: Insert descriptions of Realization Viewpoint components -->

Component | Description
---|---
National Reference Data Maintenance Service | Service allowing the National Data Space Facilitators (NDSF) to create and maintain national reference data and to create mappings from national data models to common European data models.
Interface for NDSF to update national reference data | Interface allowing the NDSF to maintain national reference data models and feeds the to Reference Data Maintenance Service.
Reference Data Maintenance Service | Service ingesting the national data curated and prepared by NDSF and feeding it to the European Reference Data Registry.
Energy Market Refrence Data | Aggregated reference data at national data space level. It has multiple data models and various data sources, including adminitstrative permissions and access rights. The data model is maintained by NDSF.
European Reference Data Registry | Component that ingests data from national data space and transforms it into common European data format. The common European data models are maintained by the CEEDS Facilitator.
Reference Data Provision Service | Service allowing the transfomed data to be exposed to CEEDS Participants.
Common European-wide unique identification | Function part of the Reference Data Provision Service that exposes the UUID of a specific CEEDS Participant 
Change Notifications | Function part of the Reference DAta Provision Service that notifies changes of a specific national data model or changes in common European data model.
Query reference data | Function part of the Reference Data Provision Service that allow for querying and searching of both national and common European data models.
CEEDS Participant Application | Application facing the CEEDS Participant exposing the functions of Referecne Data Provision Service via Web interface.


## Data Architecture

<!-- 
Data Architecture pertains to the management of data, both physical and logical.
It involves data assets, databases, data models, and the governance of data across the enterprise.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

The European Reference Data Registry should be able to handle multiple data models, and versions of same data model. It should contain a repository of metadata that allows defining, storing, and managing the currently identified national data models and the common European data model. The recommended data architecture is a combination of data catalog, meta data repository and basic data tranformation tools - from national data model to and from common European data model, allowing transparent data transactions between CEEDS participants.

Looking at the exiting tools proposed by DSSC that can be used to implement the data architecture the following candidates are suggested:
- SIMPL-Open Catalogue
- Ocean Enterpirse Catalogue and Aquearius Catalogue Cache
- FAIR Data Publisher

### Data Objects

CEEDS data model is based on the reference model for metering and consumption data access as specified in [Annex I of Commission Implementing Regulation (EU) 2023/1162](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32023R1162#anx_1)

The data exchange shall be based on an ETSI-CEN-CENELEC set of standards (e.g. EN IEC 62325-351 and considering other relevant European initiatives such as the Harmonised Electricity Market Role Model (HEMRM) and the International Electrotechnical Commission’s Common Information Model (CIM).

Here are the references for data objects to be used:
- **EN IEC 62325-351** the European Style Market Document (ESMP) as published by [ENTSO-E](https://www.entsoe.eu/publications/electronic-data-interchange-edi-library/#Common_information_model__CIM__European_style_market_profile) consisting of a user guide, XSD, code list and component
- **ISO8601** for date/time formats
- **ISO19139** for annotation of high-value datasets in geometadata.

Further usage of other standards, especially dealing with electro mobility, are still part of ongoing discussion in the CIM TC57 working group 21. The result will be published at the Bridge energy schemas Github.


The data model used by this service is based on reuse of work from previous European projects: [EDDIE](https://github.com/eddie-energy/eddie/tree/main/masterdata), [ENTSO-E](https://www.entsoe.eu), and [Digital4Grids](https://github.com/Digital4Grids/) 


#### List and Specification of Reference Data Objects

Based on identified [Reference models](../../reference-models/reference-models.html), the service S3 will be used by the following procedures:

Procedure: **T4-2_01 Access to Metering and Consumption Data**
- 02 Access to validated historical metering and consumption data by an eligible party
- 03 Termination of service by an eligible party

Pocedure: **T4-2_02 Access to Basic Master Data**
- 02 Access to accounting point master data by an eligible party
- 03 Termination of access to accounting point master data by the eligible party
- 05 Revocation of access to accounting point master data by the final customer
- 06 Access to market party master data
- 07 Access to list of market parties by their role

Procedure: **T4-2_03 Access to implicit flexibility signals**
- 01 Access to residual supply price for period
- 02 Access to residual grid fee for period
- 03 Access to CESU supply price for period
- 04 Access to CESU grid fee for period

Procedure: **T4-2_04 Customer Switching**
- 01 Switching supplier
- _02 Cancellation of switching supplier (optional)_

Procedure: **T4-3_01 Collective Self-Consumption and Energy Communities**
- 01 Registration of a collective energy sharing unit
- 02 CESU operator queries if metering point may be assigned
- 03 Final customer queries if metering point may be assigned to a CESU
- 04 CESU operator requests metering point to be added to the unit [optionally] with the info of
- 05 CESU operator requests metering point to be assigned to CESU data eligible party too
- 06 CESU operator requests accounting point to be removed from CESU a
- 07 Final customer requests its accounting point to be removed from CESU
- 08 Support to short-term flexibility markets
- 09 Energy management w/wo flexibility provision
- 10a Flexibility verification and settlement done by FRP
- 10b Flexibility verification and settlement done by flexibility market operator or other third-party support tool
- 11a Receive self-consumption information for CESU without CESU intervention
- 11b Receive self-consumption information for CESU from CESU dynamic allocation
- 12 CESU internal settlement w/wo flexibility provision
- 13 Direct access to its own data by CESU member
- 14 Change the allocation mechanism of the CESU
- 15 Company qualification for participating in flexibility markets
- 16 Assets qualification for participating in flexibility markets

The payload for each procedure must be modeled and stored in the European Reference Data Registry. 

We will provide in the next sections a non exhaustive list of samples of data models. The European Reference Data Registry must be able to handle any type of data models and data model changes. 

Common European data models extracted form [Annex I of Commission Implementing Regulation (EU) 2023/1162](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32023R1162#anx_1)

![European Reference Data Registry National Competent Aythority](./I1-erdr.drawio.png)

![European Reference Data Registry Information on Member State data management set-up](./I2-erdr.drawio.png)

![European Reference Data Registry Information about metered data administrators in a Member State](./I3-erdr.drawio.png)

![European Reference Data Registry Information about metering point administrators in a Member State](./I4-erdr.drawio.png)

![European Reference Data Registry Information about data access provider](./I5-erdr.drawio.png)

![European Reference Data Registry Information about permission administrators in a Member State](./I6-erdr.drawio.png)

![European Reference Data Registry Information about standardised near real-time interfaces of smart meters or smart metering systems in a Member State](./I7-erdr.drawio.png)

National and platform data models extracted from [EDDIE](https://github.com/eddie-energy/eddie/tree/main/masterdata)

![European Reference Data Registry Data Access Provider](./dap-erdr.drawio.png)

![European Reference Data Registry Data Exchange Environment](./dee-erdr.drawio.png)

![European Reference Data Registry Metered Data Administrator](./mda-erdr.drawio.png)

![European Reference Data Registry Metering Point Administrator](./mpa-erdr.drawio.png)

![European Reference Data Registry National Competent Authority](./nca-erdr.drawio.png)

![European Reference Data Registry Near Realtime Data Interface](./nrdi-erdr.drawio.png)

![European Reference Data Registry Permission Administrator](./pad-erdr.drawio.png)




## Application Architecture

<!-- 
The Application Architecture describes individual applications and their interactions.
It addresses software applications and their role in supporting business processes and functions.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

The European Referece Data Registry service main function is to store and serve the common European data model and data catalogue. As seconday function should provide a services that allows national data platform facilitators to create, store and manage national data models, and to provide the mappings from national data models to common European data models.  
The service can be developed and hosted by National Data Space platform for the part concerning the national data model management and mapping. For the common European data model and data catalogue the service should be centralised and the models must be synchronized (in case of distributed implementation). The service should have the possilibity to function off-line, it is the responsiblity of National Data Space platform to synchronise and update the data from CEEDS.

### Application Cooperation Viewpoint

<!--
The Application Cooperation Viewpoint pattern creates elements a diagram that describe the relationships between applications components  and their locations, the services they provide or utilize and the information that flows between them.
See: https://sparxsystems.com/resources/tutorials/archimate/#Application-Cooperation-Viewpoint
-->

![European Reference Data Registry Application Cooperation](./application-erdr.drawio.png)

The European Reference Data Registry service main function is to store and provide common European data model for CEEDS participants facilitating data exchage. This implies explicit version management of data models. The mapping of national data models to common European data model is the direct responsiblity of the National Data Space Facilitator and to synchronize with the latest version of common European data model. The National Data Space Facilitator must share the mapping with the CEEDS platform so that that all CEEDS participants are able to use the mapping for data transactions.

Taking into account the dynamics of common European data model updates, it is safe to say that offline service is acceptable and S3 - European Reference Data Registry is not on the critical path for CEEDS operations. It is the responsiblity of the local National Data Space Facilitator to synchronize Nataional Data Space refrence data repository with CEEDS reference data repository.

Main operations and procedures

Actor | Operation | Description
---|---|---
National Data Space Facilitator | Manages Energy Market Reference Data | The NDSF is responsible for gathering, updating and mentaining all versions of national reference data, including the access rights structures and service catalogue.
National Data Space Facilitator | Manages Mapping to common European data model | The NDSF is responsible for updating the local copy of the common European data model (including multiple versions) and the mapping of national data model to common European data model. The system should allow the Nataional Data Space Facilitator to push the mappings to CEEDS platform to S3- European Reference Data Registry.
CEEDS Facilitators | Manages common European data model(s) | The CEEDS Facilitator must maintain multiple versions of common European data model as Reference Data Model. A copy of mappings to national data models will be stored along each vesion of common European data model.
CEEDS Participant | Reads and queries common European data model | The CEEDS Participant should be able to retrieve the data catalogue, including multiple versions, and query the European Reference Data Registry.



#### Component Descriptions

<!-- TODO: Insert descriptions of Application Cooperation Viewpoint components -->

## Technology Architecture

<!--
The Technology Architecture involves the IT infrastructure, including hardware, software, networks, and services.
It ensures that the infrastructure supports the application and data requirements of the business.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

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
