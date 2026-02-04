---
title: European Reference Data Registry
order: 3
---

## Contributors

| Responsibility | Name                     | E-Mail                          |
|----------------|--------------------------|---------------------------------|
| Leader         | Dragos-Constantin Stoica | dragos.stoica@lnds.lu           |
| Contributor    | Benjamin Ellmer          | benjamin.ellmer@fh-hagenberg.at |
| Contributor    | Georg Hartner            | georg.hartner@eddie.energy      |


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
- **Data Models**: Data models ensure that data is accurately and consistently interpreted when exchanged within a data space. The data model consists of metadata that provides information about semantics, helping to interpret the actual exchanged data. 
- **Provenance and traceability**: additional metadata alongside the shared data for auditing and compliance purposes might be required.  

The main functions:
- metadata definition and management
- energy market refrence data model representation, maintenance by CEEDS Operator
- reference data model access for CEEDS Participants
- national reference data model definition and management can be maintained by National Data Space Facilitator (NDFS)
- enhancement and mapping of national reference data model to European reference data model 

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

### Data Objects

<!-- TODO: Insert list/table of data objects and their descriptions -->
CEEDS data model is based on the reference model for metering and consumption data access as specified in [Annex I of Commission Implementing Regulation (EU) 2023/1162](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32023R1162#anx_1)


#### List and Specification of Reference Data Objects

Based on identified [Reference models](../../reference-models/reference-models.html), the service S3 will be used by the following procedures.


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
