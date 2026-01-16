---
title: European Vocabulary Hub
order: 2
---

## Function and Objective
Maintains the European Common Information Model and maps national vocabularies for semantic interoperability. 

It is one responsibility of the CEEDS Facilitator to actively participate in the works under the umbrella of Standards Defining Organisations (SDOs) on the adoption and extension of the pivotal European information models. National Data Space Facilitators should be responsible to provide and maintain updates of the mappings.

## Archimate Service Realisation Viewpoint
![European Vocabulary Hub ArchiMate Diagram](./img.png)


## Data Architecture

### Reference data objects
S2 service is used by the folowing procedures:

Model name | Procedure
---|---
IR Demand Response | 	1: General access to Controllable Unit master data by an entitled party
IR Demand Response  | 2: Controllable Unit registration
IR Demand Response  | 5: Suspension of Controllable Unit by an entitled party
IR Demand Response  | 6: Re-activation of Controllable Unit
IR Demand Response  | 29: Bidding and activation of a flexibility product
IR Demand Response  | 30: Temporary limits
IR Demand Response  | 31: Baseline data handling
IR Demand Response  | 32: Making measurement data available
IR Demand Response  | 33: Quantification
IR Demand Response  | 34: (Optional) Baseline Validation 
Household Footprint Calculation | 1: Customer onboarding
Customer Energy Management | 3: Access to historical metering and consumption data
Customer Energy Management  | 6: Access to data for demand response or third-party services
Customer Energy Management  | 	7: Termination, Revocation and offboarding
Collective Energy Sharing (CESU) | 8: Support to short-term flexibility markets 
Flexible Connection Agreements	| 2: Onboarding of flexible customer to FCA in DCI
Flexible Connection Agreements |	3: Revocation of flexible connection agreement by flexible customer
Flexible Connection Agreements  | 4: Termination of FCA by Connecting System Operator
eHDV Long-term Power Forecast |	3: Access to Grid hosting capacity information

## Application Architecture

![European Vocabulary Hub ArchiMate Application Diagram](./application-evh.drawio.png) 

The High Lever Architecture of the European Vocabulary Hub contains:
- Common European module containing: code lists, thesaurus, ontology, data model, data and service catalog
- National or platform specific module containing: data model, data and service catalog 
- Data mapping service for data conversion from national or platform specific to common European model
- Governance module for identity management and data access management. The data access management is done by the National Platform Facilitator 


Module | Component | Description
---|---|---
National Data Space / National Platform / Specific Platform | Client library | Software library failitating the data exchange in a trustfull way between the European Vocabulary Hub and National Data Space / National Platform or Specific Platform.
National Data Space / National Platform / Specific Platform | National Platform intreface | Public interface facilitating the communication and data exchage with the National Data Space / National Platform / Specific Platform via the client library.
National Data Space / National Platform / Specific Platform |  Data model | The data model for specific National Data Space that is used for data transactions between European Vocabulary Hub and National Data Space. This is used by National Platform interface, client library and Data Mapping service.
National Data Space / National Platform / Specific Platform |  Ontology | Optional component that can be used to map and transform the specific data model into European data model. This component is necessary for the alignment with European Vocabulary module in a systematic way.
National Data Space / National Platform / Specific Platform |  Service Catalog | The service catalog provided by the specific National Data Space. Those are the services available for data transactions for the other participats at CEEDS.
Data Mapping | Data Mapping service | Ensures the transformation of National Data Space data to common European Vocabulary format. This module can be part of the National Data Space or Specific Platform
Governance module | Governance | Facilitates the Identity Access Mamagement and the Access Rights Management for the interoperability of National Data Spaces / National Platforms, Specific Platforms with European Vocabulary Hub service. This should take into account the national legislation concerning the data sharing and explicitly implement those restrictions at data model level.
Common European Vocabulary module | Data Mapping interface | Intreface facilitating the connection and data exchage between the common European Vocabulary module and National Data Space / National Data / Specific platform via the Data Mapping service.
Common European Vocabulary module | Code lists | The collection of code lists used by common European ontology and implicitly by Data Model. The code list implementation is recommended to be compatible with EU Vocabularies standards (OASIS GC, RDF).
Common European Vocabulary module | Thesaury | The collection of thesaury used by common European ontology and Data Model. The thesaurus implementation is recommended to be compatible with EU Vocabularies standards.
Common European Vocabulary module | Ontology | The collection of ontologies used as basis for common European Data Model. The ontology implementation is recommended to be compatible with EU Vocabularies standards.
Common European Vocabulary module | Data Model | The common European Vocabulary central concept is the Data Model. This is the traget common data format used by all participants. The Data Model is the targe model for the data comming from National Data Spaces / National Data / Specific platform. The Data Model is managed via the European Vocabulary management interface.
Common European Vocabulary module | Data Catalog | The publicly available catalog for Data Discovery. The data available in the catalog must be available from National Data Spaces and/or Specific Platforms.
Common European Vocabulary module | Service Catalog | The publicly avaialble catalog o services. Service composition might be necessary to accomodate the data requests.
Common European Vocabulary module | Aggregated services | Service aggregator that will expose the avaialble Service Catalog, Data Catalog, Data Models, Schema and Ontologies to CEEDS user via Infromation schema publication service.
Common European Vocabulary module | Information Schema publication | Service that exposes publicly the agreggated internal services. The user will send the reqeust via this service.
Common European Vocabulary module | European Vocabulary managed interface | Intreface that will allow the CEEDS operator to connect and operator to connect and manage the metadata of common European Vocabulary.
Common European Vocabulary module | Client library | Software library allowing the CEEDS Operator or CEEDS user to connect to common European Vocabulary module. The Governance is performed at CEEDS level as part of the overall Governance.


The main function of European Vocabulary Hub is to facilitate the data exchange and interoperability between the federation of existing and future Data Spaces by providing a common ontology and standardised way of communication.

The implementation and deployment is modular and National Platform module can be deployed on the National or Specific Data Space. The Common European Vocabulary module can be deployed as EU shared service or as distributed service.

The European Vocabulary Hub provides services for and interacts with the following actors and systems:

Actor/System | Description
---|---
Specific National Platform | This is a system to system interaction. Only selected National Energy Platforms will connect to CEEDS. The access will be limited only to the selected list from the participants in CEEDS project and only specific sercies and data sets will be exchanged.
National Platform Facilitator | Actor responsible for National Platoform management, in paritcular defineing the specific metadata that can be shared with CEEDS, the maintenance of the corresponding ontology and maintenance of the corresponding data mapping service from National metadata to European Vocabulary metadata.
CEEDS User | Actor having access to the services related to Information Schema.
CEEDS Operator | Actor having access to the European Vocabulary HUB intreface for metadata management. This includes code lists, thesaury, ontology, data service catalog, data catalog, access management, rights management.
S4 - Common European Process Façade | Service connected to S2 - European Vocabulary HUB.
EU Vocabularies | EU platform maintained by Publications Office of EU, repository for code lists, vocabularies, ontrologies.

The main role of European Vocabulary HUB is to create the common minimum data model that will allow existing and future systems and platforms to exchange information in a seeamless way.



## Application Cooperation Viewpoint (Archimate)

Examples for National Platforms and the Interaction

E.g. sequence diagrams for e.g. onboarding, offboarding etc.

## Technology Architecture

## Deployment Diagram (Archimate Deployment View)
