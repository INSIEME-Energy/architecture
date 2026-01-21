---
title: European Vocabulary Hub
order: 2
---

## Contributors

| Responsibility | Name                     | E-Mail                                |
|----------------|--------------------------|---------------------------------------|
| Leader         | Dragos-Constantin Stoica | dragos.stoica@lnds.lu                 |
| Contributor    | Wout van Voornveld       | w.van.voornveld@expertmodeller.energy |
| Contributor    | Tomé Ferreira            | tome.ferreira@ri.se                   |

## Function and Objective

Maintains the European Common Information Model and maps national vocabularies for semantic interoperability.

It is one responsibility of the CEEDS Facilitator to actively participate in the works under the umbrella of Standards Defining Organisations (SDOs) on the adoption and extension of the pivotal
European information models. National Data Space Facilitators should be responsible to provide and maintain updates of the mappings.

## Business Architecture

<!-- 
The Business Architecture focuses on business requirements. It outlines the structure and operation of an organization, including business goals, functions, processes, and organizational structure. 
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->
![European Vocabulary Hub Business Architecture](./business-evh.drawio.png)


### Service Realization Viewpoint

<!-- 
The Service Realization Viewpoint pattern creates elements that show how one or more business services are realized by the underlying processes (and sometimes by application components). 
Thus, it forms the bridge between the business products viewpoint and the business process view. It provides a "view from the outside" on one or more business processes. 
See: https://sparxsystems.com/resources/tutorials/archimate/#Service-Realization-Viewpoint
-->

![European Vocabulary Hub ArchiMate Diagram](./img.png)

#### Component Descriptions

Component | Description
---|---
Data mapping service | Service that transforms national data models into European wide models. Uses schema definitions and client libraries. The communication with National Data Platforms is done via client libraries.
Data mapping service - schema definitions | All necessary data models for exchanging and converting national data to CEEDS data models.
Data mapping service - client libraries | The client libraries are specific for each national data space / national platform of specific platform and facilitates the management of national or platform specific code lists, ontologies, data models, data catalogs, service catalogs that are necessary for exchanging data with CEEDS.
standardised data mapping to pivotal information models | Data transformation from national data model to CEEDS data model. This should support defaul values in case of missing data.
EU-wide register for information models | The register European model(s) is managed by CEEDS operators and fed by National Data Space Facilitator(s). The register is used a data model repository together with data mapping and trasnformation for each verison, from national data model to European common data model.
Information schema publication | Service exposing the European common data model, the schema definitions via the client libraries. Any pariticipant at CEEDS Data Space must have a client library.
Information schema publication - schema definitions | Common European schema definitions. This is the minimum mandatory European schema that allows data exchange between the participants at CEEDS Data Space.
Information schema publication - client libraries | The client libraries used by information schema publication service to exchange data in common Europead format.



## Data Architecture

### Data Objects

The following standards should be used:
- __ISO-8601__ for date/time formats
- __ISO-19139__ for annotation of high-value datasets in geometadata. 


The data objects are extracted from Commission Implementing Regulation (EU) 2023/1162, Annex 1, Table IV - Infromation object exchanged as common European Data Space data model.

__Code lists__

Name | Description | Values
---|---|---
<a id="cl-direction"></a>Direction | Flow direction metered by the metering point. This can be either solely production, consumption, or combined. | <ul><li>Solely production</li><li>Consumption</li><li>Combined</li></ul>
<a id="cl-energy-product"></a>Energy product  | Energy product measured by the metering point (for example, active energy, re-active energy) | <ul><li>Active energy</li><li>Re-active energy</li></ul>
<a id="cl-unit-of-measure"></a>Unit of measure | The measurement unit in which the quantities have been stated |Suggested EU Vocabularies code list [Measurement Unit](https://op.europa.eu/en/web/eu-vocabularies/concept-scheme/-/resource?uri=http://publications.europa.eu/resource/authority/measurement-unit#), and conpcept scheme [Supplemantary Units](https://op.europa.eu/en/web/eu-vocabularies/concept-scheme/-/resource?uri=http://data.europa.eu/gzn/su/SU#) can be used to add CEEDS specific measuring units

<a id="mpi"></a>__Metering point identificaion__

Attribute | XML data type | Comments
---|---|---
Metering point identifier | Unique ID | Unique identifier for the metering point within the metered data administrator’s meter identification space.

<a id="mds"></a>__Metered data specification__
Attribute | XML data type | Comments
---|---|---
Reading start timestamp | Timestamp |Start of the time interval covered by the data package.
Reading end timestamp | Timestamp | End of the time interval covered by the data package.
Direction | [Code](#cl-direction) | Flow direction metered by the metering point. This can be either solely production, consumption, or combined
Energy product | [Code](#cl-energy-product) | Energy product measured by the metering point (for example, active energy, re-active energy)

Specific code list for Direction and Energy product must be created and maintaned by National Data Space facilitator(s) and shared with the common European vocabulary.

<a id="mdr"></a>__Metered data request__

Attribute | XML data type | Comments
---|---|---
Metering point identifier| Unique ID | Unique identifier for the metering point within the metered data administrator’s meter identification space.
Metered data specification |Object | Information object [Metered data specification](#mds)

<a id="rvi"></a>__Request validation information__

Attribute | XML data type | Comments
---|---|---
Validation result | Text | Information about the outcome of the validation step.

<a id="vhd"></a>__Validated historical data__

_Meta information_ for validated historical data

Attribute | XML data type | Comments
---|---|---
Metering point identifier | Unique ID | Unique identifier for the metering point within the metered data administrator’s meter identification space.
Creation timestamp | Timestamp | Timestamp when the data package has been generated.
Energy product | [Code](#cl-energy-product) | Energy product measured by the metering point (for example, active energy, re-active energy).
Reading start timestamp | Timepstamp | Start timestamp of the time series.
Reading end timestamp | Timestamp |  End timestamp of the time series.
Unit of measure | [Code](#cl-unit-of-measure) | The measurement unit in which the quantities in field ‘Quantity’ have been stated.


_Time series information (once per interval in reading)_ for validated historical data

Attribute | XML data type | Comments
---|---|---
Start timestamp | Timestamp | Start timestamp of interval.
End timestamp | Timestamp | End timestamp of interval.
Direction | [Code](#cl-direction) | Flow direction metered by the metering point. This can either be production, consumption or combined.
Quality of reading | String | Indication of the quality of the interval reading (for instance, based on the fact that the value is metered or estimated).
Quantity | Numeric |  Volume consumed or generated.

<a id="vhdfci"></a>__Validated historical data with final customer information__

Attribute | XML data type | Comments
---|---|---
Validated historical data | Object | Information object [Validated historical data](#vhd)
Final customer | Party | Information that allows the eligible party to potentially verify that it gets the data for the correct final customer.


<a id="ppi"></a>__Preset permission information__

Attribute | XML data type | Comments
---|---|---
Eligible party | Party | Eligible party for which the permission has been given.
Metering point identifier | Unique ID | Unique identifier for the metering point within the metered data administrator’s meter identification space.
Metered data specification | Object | Information object [Metered data specification](#mds)
Purpose | Text | The specified, explicit and legitimate purpose for which the eligible party intends to process the data. For non-personal data this is optional.
Transmission schedule | Text | For future data covered by the permission, but not available at the time the permission is established, the periodicity - when and how often - data packages are to be made available where applicable.
Permission limit timestamp | Timestamp | The timestamp by which the eligible party has to delete the received data, even if the processing purpose is not fulfilled by then.

<a id="bpi"></a>__Basic permission information__

Attribute | XML data type | Comments
---|---|---
Final customer | Party | Final customer that has given the permission.
Eligible party | Party | Eligible party for which the permission has been given.
Metered data request | Object | Information object [Metered data request](#mdr)
Purpose | Text |  The specified explicit and legitimate purpose for which data is processed. For non-personal data this is optional.
Transmission schedule | Text | For future data covered by the permission, but not available at the time the permission is established, the periodicity - when and how often - data packages are to be made available where applicable (for example, in data exchange scenarios where data is pushed rather than requested).
Permission maximum lifetime | Timestamp |  The timestamp after which the eligible party has to consider the permission as expired or revoked, even if the processing purpose is not fulfilled by then.


<a id="epi"></a>__Established permission information__

Attribute | XML data type | Comments
---|---|---
Permission identifier | Unique ID | A unique identifier of the permission.
Creation timestamp | Timestamp | Creation timestamp the permission administrator has attached to the permission.
Basic permission information | Object | Information object [Basic permission information](#bpi)

<a id="nts"></a>__Notification of termination of service__

Attribute | XML data type | Comments
---|---|---
Permission identifier| Unique ID | A unique identifier of the permission referring to information object [Established permission information](#epi)
Termination timestamp | Timestamp | Timestamp indicating the point in time when the service is considered terminated by the eligible party.

<a id="dilp"></a>__Details of information on listed permission__
Attribute | XML data type | Comments
---|---|---
Details of the permission | Object | Attributes of the permission as described in [Established permission information](#epi)
Reason for the end of permission | Text | If permission is not active anymore, the reason for why the permission administrator considers the permission has ended. For instance, this can indicate fulfilment of purpose, reach of permission end timestamp, revocation of final customer or termination by the eligible party.
Permission end timestamp | Timestamp |  If permission is not active anymore, the timestamp since when the permission administrator considers the permission as ended

<a id="rnpa"></a>__Revocation notification by permission administrator__
Attribute | XML data type | Comments
---|---|---
Permission identifier| Unique ID | A unique identifier of the permission referring to information object [Established permission information](#epi)
Permission end timestamp | Timestamp | Timestamp for when the revocation should be considered active.

<a id="dfar"></a>__Data flow activation request__

Attribute | XML data type | Comments
---|---|---
Meter identifier| Unique ID | Identifier for the metering device or the metering point required by the meter operator to identify the correct meter.
Other required information | Text | Listing of all other attributes needed by the meter operator to enable the data flow.

<a id="cdfa"></a>__Confirmation of data flow activation__

Attribute | XML data type | Comments
---|---|---
Physical connectivity| Text |Information on the physical interface of the meter and how to connect external devices.
Cipher | Text | Mandatory, if a cipher is needed to de-crypt the flow of information
Credentials | Text | Mandatory, if credentials are needed to access the smart meter interface.
Other required information | Text | Listing of all other attributes needed by the meter operator to enable the data flow and interpret it semantically.

<a id="rmd"></a>__Raw meter data__

Attribute | XML data type | Comments
---|---|---
Data package | Object | List of attributes in the received raw data. If a reference to a standard is provided here in the mappings of national practices, this standard must be publicly available in an easily accessible form or free of charge. Otherwise, all elements of the respective data package must be listed and mapped.

<a id="pmd"></a>__Process-able meter data__

Attributes described are a minimum – other data items may also be provided and documented if available in national settings

Attribute | XML data type | Comments
---|---|---
Meter data timestamp | Timestamp | Time of data capture as regarded by the smart meter or smart metering system.
Active import power value | Numeric | Instantaneous forward active power P+ (in W)
Active import power unit of measure | [Code](#cl-unit-of-measure) | Value from Unit of Measure code list
Active export power value | Numeric | Instantaneous reverse active power P- (in W)
Active export power unit of measure | [Code](#cl-unit-of-measure) | Value from Unit of Measure code list
Import active energy A+ | Numeric |  Forward active energy A+ (in Wh)
Import active energy A+ unit of measure | [Code](#cl-unit-of-measure) | Value from Unit of Measure code list
Export active energy | Numeric |  Reverse active energy A- (in Wh)
Export active energy unit of measure | [Code](#cl-unit-of-measure) | Value from Unit of Measure code list

### Reference data objects

S2 service is used by the folowing procedures:

| Model name                       | Procedure                                                                | Information exchanged |
|----------------------------------|-------------------------------------------------------------------------|---|
| IR Demand Response               | 	1: General access to Controllable Unit master data by an entitled party | [Preset permission information](#ppi)<br/>[Basic permission information](#bpi)<br/>[Established permission information](#epi)
| IR Demand Response               | 2: Controllable Unit registration                                        | [Metering point identification](#mpi)<br/>[Metered data specifications](#mds)<br/>[Preset permission information](#ppi)<br/>[Basic permission information](#bpi)<br/>[Established permission information](#epi)<br/>[Data flow activation request](#dfar)
| IR Demand Response               | 5: Suspension of Controllable Unit by an entitled party                  | [Revocation notification by permission administrator](#rnpa)<br/>[Established permission information](#epi)
| IR Demand Response               | 6: Re-activation of Controllable Unit                                    | [Preset permission information](#ppi)<br/>[Basic permission infomation](#bpi)<br/>[Established permission information](#epi)<br/>[Metered data specifications](#mds)<br/>[Validated historical data](#vhd)<br/>[Validated historical data with final customer information](#vhdfci)
| IR Demand Response               | 29: Bidding and activation of a flexibility product                      | [Metered data specification](#mds)<br/>[Metered data request](#mdr)<br/>[Request validation information](#rvi)<br/>[Data flow activation request](#dfar)<br/>[Confirmation of data flow activation](#cdfa)
| IR Demand Response               | 30: Temporary limits                                                     | [Validated historical data](#vhd)<br/>[Validated historical data with final custormer information](#vhdfci)
| IR Demand Response               | 31: Baseline data handling                                               | [Metered data specifications](#mds)<br/>[Metered request data](#mrd)<br/>[Request validation information](#rvi)
| IR Demand Response               | 32: Making measurement data available                                    | [Raw data meter](#rdm)
| IR Demand Response               | 33: Quantification                                                       | [Process-able meter data](#pmd) 
| IR Demand Response               | 34: (Optional) Baseline Validation                                       | [Validated historical data](#vhd)<br/>[Request validation information](#rvi)
| Household Footprint Calculation  | 1: Customer onboarding                                                   | [Basic permission information](#bpi)<br/>[Established permission information](#epi)<br/>[Request validation information](#rvi)
| Customer Energy Management       | 3: Access to historical metering and consumption data                    | [Validated historical data with final customer information](#vhdfci)<br/>[Request validation information](#rvi)
| Customer Energy Management       | 6: Access to data for demand response or third-party services            | [Validated historical data with final customer information](#vhdfci)<br/>[Request validation information](#rvi)<br/>[Raw meter data](#rmd)<br/>[Process-able meter data](#pmd)
| Customer Energy Management       | 7: Termination, Revocation and offboarding                               | [Notification of termination of service](#nts) <br/> [Established permission information](#epi)<br/>[Details of information on listed permission](#dilp)<br/>[Revocation notification by permission administrator](#rnpa)
| Collective Energy Sharing (CESU) | 8: Support to short-term flexibility markets                             | [Metered data request](#mdr)<br/>[Data flow acrtivation request](#dfar)<br/>[Confirmation of data flow activation](#cdfa)
| Flexible Connection Agreement    | 2: Onboarding of flexible customer to FCA in DCI                         | [Basic permission information](#bpi)<br/>[Established permission information](#epi)<br/>[Request validation information](#rvi)
| Flexible Connection Agreements   | 3: Revocation of flexible connection agreement by flexible customer      | [Notificatoin of termination of service](#nts)<br/>[Established permission information](#epi)<br/>[Details of information on listed permission](#dilp)<br/>[Revocation notification by permission administrator](#rnpa)
| Flexible Connection Agreements   | 4: Termination of FCA by Connecting System Operator                      | [Notificatoin of termination of service](#nts)<br/>[Established permission information](#epi)<br/>[Details of information on listed permission](#dilp)<br/>[Revocation notification by permission administrator](#rnpa)
| eHDV Long-term Power Forecast    | 3: Access to Grid hosting capacity information                           | [Preset permission information](#ppi)<br/>[Basic permission information](#bpi)<br/>[Establish permission information](#epi)

## Application Architecture

<!-- 
The Application Architecture describes individual applications and their interactions.
It addresses software applications and their role in supporting business processes and functions.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

![European Vocabulary Hub ArchiMate Application Diagram](./application-evh.drawio.png)

The main function of European Vocabulary Hub is to facilitate the data exchange and interoperability between the federation of existing and future Data Spaces by providing a common ontology and
standardised way of communication. The European Vocabulary HUB creates the common minimum data model that will allow existing and future systems and platforms to exchange information in a seeamless way.

The implementation and deployment is modular and National Platform module can be deployed on the National or Specific Data Space. The Common European Vocabulary module can be deployed as EU shared
service or as distributed service.

The Application Architecture of the European Vocabulary Hub contains:

- Common European module containing: code lists, thesaurus, ontology, data model, data and service catalog
- National or platform specific module containing: data model, data and service catalog
- Data mapping service for data conversion from national or platform specific to common European model
- Governance module for identity management and data access management. The data access management is done by the National Platform Facilitator

| Module                                                      | Component                             | Description                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| National Data Space / National Platform / Specific Platform | Client library                        | Software library failitating the data exchange in a trustfull way between the European Vocabulary Hub and National Data Space / National Platform or Specific Platform.                                                                                                                                                                                         |
| National Data Space / National Platform / Specific Platform | National Platform intreface           | Public interface facilitating the communication and data exchage with the National Data Space / National Platform / Specific Platform via the client library.                                                                                                                                                                                                   |
| National Data Space / National Platform / Specific Platform | Data model                            | The data model for specific National Data Space that is used for data transactions between European Vocabulary Hub and National Data Space. This is used by National Platform interface, client library and Data Mapping service.                                                                                                                               |
| National Data Space / National Platform / Specific Platform | Ontology                              | Optional component that can be used to map and transform the specific data model into European data model. This component is necessary for the alignment with European Vocabulary module in a systematic way.                                                                                                                                                   |
| National Data Space / National Platform / Specific Platform | Service Catalog                       | The service catalog provided by the specific National Data Space. Those are the services available for data transactions for the other participats at CEEDS.                                                                                                                                                                                                    |
| Data Mapping                                                | Data Mapping service                  | Ensures the transformation of National Data Space data to common European Vocabulary format. This module can be part of the National Data Space or Specific Platform                                                                                                                                                                                            |
| Governance module                                           | Governance                            | Facilitates the Identity Access Mamagement and the Access Rights Management for the interoperability of National Data Spaces / National Platforms, Specific Platforms with European Vocabulary Hub service. This should take into account the national legislation concerning the data sharing and explicitly implement those restrictions at data model level. |
| Common European Vocabulary module                           | Data Mapping interface                | Intreface facilitating the connection and data exchage between the common European Vocabulary module and National Data Space / National Data / Specific platform via the Data Mapping service.                                                                                                                                                                  |
| Common European Vocabulary module                           | Code lists                            | The collection of code lists used by common European ontology and implicitly by Data Model. The code list implementation is recommended to be compatible with EU Vocabularies standards (OASIS GC, RDF).                                                                                                                                                        |
| Common European Vocabulary module                           | Thesaury                              | The collection of thesaury used by common European ontology and Data Model. The thesaurus implementation is recommended to be compatible with EU Vocabularies standards.                                                                                                                                                                                        |
| Common European Vocabulary module                           | Ontology                              | The collection of ontologies used as basis for common European Data Model. The ontology implementation is recommended to be compatible with EU Vocabularies standards.                                                                                                                                                                                          |
| Common European Vocabulary module                           | Data Model                            | The common European Vocabulary central concept is the Data Model. This is the traget common data format used by all participants. The Data Model is the targe model for the data comming from National Data Spaces / National Data / Specific platform. The Data Model is managed via the European Vocabulary management interface.                             |
| Common European Vocabulary module                           | Data Catalog                          | The publicly available catalog for Data Discovery. The data available in the catalog must be available from National Data Spaces and/or Specific Platforms.                                                                                                                                                                                                     |
| Common European Vocabulary module                           | Service Catalog                       | The publicly avaialble catalog o services. Service composition might be necessary to accomodate the data requests.                                                                                                                                                                                                                                              |
| Common European Vocabulary module                           | Aggregated services                   | Service aggregator that will expose the avaialble Service Catalog, Data Catalog, Data Models, Schema and Ontologies to CEEDS user via Infromation schema publication service.                                                                                                                                                                                   |
| Common European Vocabulary module                           | Information Schema publication        | Service that exposes publicly the agreggated internal services. The user will send the reqeust via this service.                                                                                                                                                                                                                                                |
| Common European Vocabulary module                           | European Vocabulary managed interface | Intreface that will allow the CEEDS operator to connect and operator to connect and manage the metadata of common European Vocabulary.                                                                                                                                                                                                                          |
| Common European Vocabulary module                           | Client library                        | Software library allowing the CEEDS Operator or CEEDS user to connect to common European Vocabulary module. The Governance is performed at CEEDS level as part of the overall Governance.                                                                                                                                                                       |

The European Vocabulary Hub provides services for and interacts with the following actors and systems:

| Actor/System                        | Description                                                                                                                                                                                                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Specific National Platform          | This is a system to system interaction. Only selected National Energy Platforms will connect to CEEDS. The access will be limited only to the selected list from the participants in CEEDS project and only specific sercies and data sets will be exchanged.                                     |
| National Platform Facilitator       | Actor responsible for National Platoform management, in paritcular defineing the specific metadata that can be shared with CEEDS, the maintenance of the corresponding ontology and maintenance of the corresponding data mapping service from National metadata to European Vocabulary metadata. |
| CEEDS User                          | Actor having access to the services related to Information Schema.                                                                                                                                                                                                                                |
| CEEDS Operator                      | Actor having access to the European Vocabulary HUB intreface for metadata management. This includes code lists, thesaury, ontology, data service catalog, data catalog, access management, rights management.                                                                                     |
| S4 - Common European Process Façade | Service connected to S2 - European Vocabulary HUB.                                                                                                                                                                                                                                                |
| EU Vocabularies                     | EU platform maintained by Publications Office of EU, repository for code lists, vocabularies, ontrologies.                                                                                                                                                                                        |
### Application Cooperation Viewpoint

<!--
The Application Cooperation Viewpoint pattern creates elements a diagram that describe the relationships between applications components  and their locations, the services they provide or utilize and the information that flows between them.
See: https://sparxsystems.com/resources/tutorials/archimate/#Application-Cooperation-Viewpoint
-->

![European Vocabulary Hub Application Cooperation Diagram](./cooperation-evh.drawio.png)
National Platforms interaction with CEEDS Platform

![European Vocabulary Hub Onboarding Sequence Diagram](./onboarding-evh.drawio.png)
Procedure for onboarding 

![European Vocabulary Hub Offboarding Sequence Diagram](./offboarding-evh.drawio.png)
Procedure for offboarding

#### Component Descriptions

Component | Description 
---|---
National Data Space Facilitator(s) | Actor responsible for management and intreface with the Local actors at National Data Space level or National Platform or Specific Platform. Main responsiblity is to manage the access and data model update for CEEDS National platform.
National Data Space | Specific implementation of Data Space at national level. It may be a specific data space, also. The system is managed by National Data Space Facilitator and it communicates with CEEDS via National Data Space client libraries.
CEEDS Platform | Europeean Data Space for connecting National Data Spaces and transforming data to and from those systems into common European data format as defined and managed by service S2 - European Vocabulary Hub. 

The main interactions of sercive S2 - European Vocabulary Hub are:
- system to sytem with National Data Space via client libraries, for data exchange and transformation
- user interface with CEEDS users for data consumption in common European format 
- user interface with CEEDS operators for managing the common European format. It is possible to have an alterntive way intreacting system to system using client libraries.

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
