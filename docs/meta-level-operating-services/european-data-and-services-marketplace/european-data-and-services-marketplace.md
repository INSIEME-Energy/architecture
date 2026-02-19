---
title: S7 - European Data and Services Marketplace
order: 7
---

## Function and Objective

Provides a regulated environment for accessing, sharing, and commercialising energy-related data. The EDSM should contain a data catalogue for data indexing and discovery.

![Service Realisation Viewpoint - Data, Services and Models Marketplace](./srv_dataservicesmodelsmp.png)

Data service providers may link into this marketplace to offer their services, such as:

- Forecasting and data analysis for pivotal information model data
- Crowdsourcing of data based (e.g. feature-based request for data)
- Refinement of data
- Storage and accessibility of regulated data (e.g. forecast charging capacity of charging stations collected from Charge Point Operators (CPO), data from the ENTSO-E Transparency Platform, market
  data, etc.)
- Storage and accessibility of statistical data
- Privacy and pseudonymisation

EDSM should contain – possibly in close co-operation with SIMPL – a concept for data provision contract negotiation, cost renumeration and commercialization of data, as well as settlement of
transactions. EDSM should cover both free-of-charge and chargeable services.

## Business Architecture
<!-- 
The Business Architecture focuses on business requirements. It outlines the structure and operation of an organization, including business goals, functions, processes, and organizational structure. 
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

### Business Goals

The European Data and Services Marketplace (EDSM) aims to establish a **trusted, regulated, and interoperable European market infrastructure** for energy-related data, services, and models.  
The strategic business goals of the EDSM are:

- **Enable a European energy data economy** by facilitating cross-border data sharing and interoperability  
- **Support digital innovation** through data-driven and AI-based services  
- **Create sustainable business models** for data, services, and models  
- **Enable monetisation** of digital assets while supporting free-of-charge offerings  
- **Ensure regulatory compliance**, trust, and data sovereignty  
- **Foster ecosystem growth** by enabling multi-stakeholder participation  
- **Promote reuse and interoperability** of existing European digital infrastructures  
- **Support federated governance models** aligned with European dataspace principles  

The EDSM acts as a **market-enabling platform** that transforms data into economic, operational, and strategic value for the European energy sector.

---

### Business Capabilities

To achieve these goals, the EDSM provides the following core business capabilities:

#### Market Enablement
- Digital marketplace creation  
- Data, service, and model commercialisation  
- Ecosystem orchestration  
- Multi-actor market participation  

#### Data Economy Enablement
- Data discovery and indexing  
- Federated data access  
- Trusted data sharing  
- Data sovereignty preservation  

#### Service Economy Enablement
- Data-driven service provisioning  
- AI service provisioning  
- Model training and provision  
- Application and service marketplace support  

#### Governance and Trust
- Identity and trust management  
- Contract-based access control  
- Policy enforcement  
- Regulatory compliance support  
- Auditability and traceability  

#### Economic and Financial Management
- Contract negotiation  
- Compensation mechanisms  
- Transaction tracking  
- Clearing services  
- Billing and invoicing  
- Settlement and monetisation  

#### Interoperability and Federation
- Semantic interoperability  
- Cross-platform integration  
- Dataspace federation  
- Connector-based interoperability  
- Cross-project infrastructure reuse  

These capabilities position the EDSM as a **foundational business infrastructure** for the European energy data ecosystem, enabling scalable, sustainable, and trustworthy digital markets.

From a business perspective, the EDSM acts as a **market-enabling infrastructure** that connects:
- Data providers (e.g. grid operators, CPOs, market operators, statistical authorities)
- Service providers (analytics, forecasting, refinement services)
- Model and AI service providers
- Consumers (energy companies, aggregators, researchers, public authorities)
- Platform operators and regulatory stakeholders

The marketplace supports the full business lifecycle of data, services, and models, including:  
**discovery → negotiation → access → usage → transaction tracking → clearing → billing → settlement**, enabling sustainable economic flows and long-term ecosystem viability.

---

### Service Realization Viewpoint

<!-- 
The Service Realization Viewpoint pattern creates elements that show how one or more business services are realized by the underlying processes (and sometimes by application components). 
Thus, it forms the bridge between the business products viewpoint and the business process view. It provides a "view from the outside" on one or more business processes. 
See: https://sparxsystems.com/resources/tutorials/archimate/#Service-Realization-Viewpoint
-->

<!-- TODO: Insert ArchiMate Service Realization Viewpoint diagram -->

The Service Realization Viewpoint describes how business objectives are implemented through **digital services, platforms, and technical components** within the EDSM ecosystem.

#### Middleware Layer

Providing governance, identity management, semantic interoperability, and discovery services, including:

- **Federated Catalog Discovery**
  - **Data Catalog**
  - **Service Catalog**
  - **Model Catalog**
- Identity management
- Data model services
- Semantic interoperability
- Integration with European core services (S1, S2, S3)
- **Integration with the OneNet Connector**

The Middleware acts as the **control and governance plane** of the EDSM ecosystem.

---

#### Data Space Connector Layer

The **Data Space Connector** layer enables **trusted and federated data exchange**.

This layer provides:
- Generic data sharing  
- Dataset management  
- Secure data exchange  
- Contract negotiation and compensation  
- Policy-based access control  
- Data service creation  
- End-to-end encrypted communication  

**Implementation assumption:**
- The **OneNet Connector** can be used as the technical implementation of the connector layer  
- The Data Space Connector layer is **integrated with the OneNet Middleware**

This layer represents the **transactional and operational core** of data sharing and data exchange.

---

#### Marketplace Layer *(To Be Identified and Evaluated)*

The Marketplace represents the **commercial and user-facing interface** of the EDSM.

It provides:
- **Data Catalog**
- **Service Catalog**
- **Model Catalog**
- **Model Training and Provision**
- Service and application provisioning
- User interaction interfaces
- Access to AI services and data-driven applications
- Integration with billing and invoicing systems

**Marketplace identification assumptions:**
The Marketplace solution is **not yet defined** and will be identified and evaluated based on:
- Reuse of existing project solutions
- Alignment with European dataspace initiatives
- Interoperability and governance requirements

**Candidate solutions under evaluation:**
- **SIMPL**
- **ENERSHARE**
- **Other existing European platforms or project solutions**

---

#### Clearing House *(To Be Identified and Evaluated)*

The Clearing House is a **separate and independent component**, integrated with the **Data Space Connector layer**.

It provides:
- Data transaction logging  
- Monitoring of data exchanges  
- Traceability of data flows  
- Auditability of transactions  
- Integration with Data Space and Marketplace  

The Clearing House ensures **transparency, accountability, and trust** across all data exchanges.

To Be Identified...SIMPL ??

---

#### Billing System *(To Be Identified and Evaluated)*

The Billing System is integrated with the **Marketplace** and provides:
- Cost calculation  
- Invoicing  
- Payment management  
- Support for free-of-charge and chargeable services  
- Integration with external financial systems  

It enables **data, service, and model monetisation** and supports sustainable business models.

To Be Identified...SIMPL ??

---

#### External Integration Services

The EDSM integrates with other services:

- **S1 – Identity Register**  
  Authentication, identity management, trust services

- **S2 – European Vocabulary Hub**  
  Semantic interoperability and controlled vocabularies

- **S3 – European Reference Data Registry**  
  Reference data governance and harmonisation


#### Component Descriptions

##### Middleware
Central governance and orchestration layer providing:
- Federated discovery (Data, Service, Model)
- Identity management
- Semantic interoperability
- Integration with OneNet Connector
- Integration with European core services (S1, S2, S3)

---

##### Data Space Connector
Operational layer providing:
- Federated data sharing
- Secure data exchange
- Contract-based access
- Compensation mechanisms
- Policy enforcement
- Integration with OneNet Middleware
- Implementation through OneNet Connector

---

##### Marketplace *(To Be Identified and Evaluated)*
Commercial layer providing:
- Data, Service, and Model catalogs
- Model training and provision
- Application and service provisioning
- User access interfaces
- Billing and monetisation integration

Candidate implementations under evaluation:  
**SIMPL, ENERSHARE, other European solutions**

---

##### Clearing House
Governance and trust layer providing:
- Transaction logging
- Exchange monitoring
- Traceability
- Auditability
- Integration with Data Space + Connector and Marketplace

---

##### Billing System
Economic layer providing:
- Cost calculation
- Invoicing
- Payments
- Monetisation support
- Financial integration

---

##### External Core Services
- **S1 – Identity Register**
- **S2 – European Vocabulary Hub**
- **S3 – European Reference Data Registry**

<!-- TODO: Insert descriptions of Realization Viewpoint components -->

## Data Architecture

<!-- 
Data Architecture pertains to the management of data, both physical and logical.
It involves data assets, databases, data models, and the governance of data across the enterprise.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

### Data Objects

<!-- TODO: Insert list/table of data objects and their descriptions -->

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
