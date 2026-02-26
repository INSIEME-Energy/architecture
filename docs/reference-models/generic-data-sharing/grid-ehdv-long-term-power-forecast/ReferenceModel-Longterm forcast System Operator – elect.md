---
title: Project INSIEME - Reference Model Template - Task 4.5 - Long-term forecast System Operator - electromobility Heavy Duty Vehicle eHDV
---

# Task 4.5 – Long-term forecast System Operator – electromobility Heavy Duty Vehicle eHDV and electromobility Heavy Duty Vehicle eHDV – System Operator  



We strive to widen scope to forecasts in general if possible in the next iteration, now we focused on the **information exchange** **between System Operator and electromobility Heavy Duty Vehicle eHDV**, **and the long-term forecast from the System Operator in form of grid hosting capacity information**

## Context

(1) flexibility need assessment

(1) A new requirement for electricity system operators, both at transmission and distribution levels, to publish and update information on the capacity available for new connections in their areas of operation would give investors easier access to information of grid capacity availability within the system and thereby accelerate decision-making The European Commission has acknowledged a gap between grid capacity and connection demand as an issue that must be addressed and launched several initiatives on network development plans, grid hosting capacity information and flexibility need assessment.

(2) A new requirement for electricity system operators, both at transmission and distribution levels, to publish and update information on the capacity available for new connections in their areas of operation would give investors easier access to information of grid capacity availability within the system and thereby accelerate decision-making. (Regulation 2024/1747 and Directive 2024/1711)

(3) Grid Action Plan number 6 urges ENTSO-E and the EU DSO Entity to *'(...) establish a pan-EU overview that should give visibility to project developers when conceptualising their projects, such as new renewable or EV recharging infrastructure projects and help developers estimate the risk of connection request approval delays and, thus, have a clearer forecast about when projects can start receiving revenues'.*

(4) Project developers need long-term grid hosting capacity information from System Operators to be able to plan future energy investments.

(5) System Operators need information from project developers, customers and relevant stakeholders about future need of grid hosting capacity to be able to plan for future grid capacity need in the network development plans, to assess future flexibility need and to inform on long-term forecast grid hosting capacity.

(6) The forecast for electromobility Heavy Duty Vehicles future need for capacity can be based on GPS-data from Heavy Duty Vehicles and/or on historical charging data from Heavy Duty Vehicles.

CHAPTER I

**Regarding GENERAL PROVISIONS**

*Issue 1*

**On subject matter and scope**

(1) [IGNORE FOR NOW]

## Definitions

*Issue 2*

**On definitions**

For the purpose of this implementing regulation, the definitions in Article 2 of Directive (EU) 2019/944 [TODO and state that the definitions in other pieces of European Legislation] shall apply. In addition, the following definitions shall apply:

(1) 'eHDV ' in the context of this act, means electromobility Heavy Duty Vehicle

(2) 'eHDV data ' in the context of this act, means data from electromobility Heavy Duty Vehicles

(3) 'eHDV forecast ' in the context of this act, means a forecast about electromobility Heavy Duty Vehicles future need for capacity

## Responsibilities of Market Roles

CHAPTER II

**Regarding [YOUR USE CASE]**

**[NOTE] Typically define responsibilities last and in close coordination with *T5.5 EU Policy and regulation alignment***

*Article XX*

**On responsibilities of ROLE1**

1. ROLE1 shall ...

## Annex

ANNEX A

**A1. The reference model for [YOUR USE CASE]**

### General Information



Table I contains information needed by [Stakeholder1 AND Stakeholder2] to set up for utilising [YOUR USE CASE] in a Member State. Do we need Table 1?

***Table I - General information on Member State environments***
| ID  | Name                                                                                       | Description                                                                                                                                                                                                           |
|-----|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| I1  | [EXAMPLE] National competent authority                                                     | *Name* - Name of appointed national competent authority.<br/>*Website* - Website of appointed national competent authority.<br/>*Official contact* - Contact details for managing the mappings of national practices. |
| I2  | [EXAMPLE] Information about permission administrators in a Member State (at least *one mapping per each active consent administrator in a Member State*) | *Name* - Name of the organisation.<br/>*Type of identification* - May be ACER registration code, Legal Entity Identifier (LEI), Bank Identifier Code (BIC), Energy Identification Code (EIC), Global Location Number (GLN/GS1) or National Identification Code (NIC).<br/>*Identification of organisation* - Code or identification within the identification space nominated above.<br/>*Website* - If applicable, link to website of a web application that is used for consent administration.<br/>*User interface* - URL or user portal.<br/>*Official contact* - Contact details for data sharing.<br/>*Consent management responsibility for* - Metered data administrators for which the consent administrator manages consents. Note that it is also valid for a metered data administrator to utilize several consent administrators for a consent administrator to act for multiple metered data administrators.<br/>*Documentation of access* - A self-sufficient explanation of the Member State provisions with regards to utilize *access to validated historical consumption data by an eligible party*. It is recommended to also include an English version of this documentation.<br/>*Identity service provider* - Identity service provider utilized by the consent administrator to authenticate final customers.<br/>*Eligible party onboarding* - Either a link to the English documentation of the onboarding procedure or a complete, self-sufficient English explanation for how an eligible party can onboard to the productive environment to utilize *sharing of validated historical consumption data with an eligible party*.<br/>*Eligible party test onboarding* - If applicable, either a link to the English documentation of the onboarding procedure or a complete, self-sufficient English explanation for how an eligible party can onboard to a test environment to utilize *sharing of validated historical consumption data with an eligible party*.<br/>*Price list for access to data by eligible parties* - Exhaustive description of all costs for eligible parties. |

**[TODO] Please describe all *HARMONISED ROLES* below.**



***Table II - Roles***

| Role name                              | Role type | Role description                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Final customer                         | Business  | This refers to a party connected to the grid that purchases electricity for its own use. Note: this also includes the case of active customers and participants of renewable energy communities or citizen energy communities.                                                                                |
| Competent authority                    | Business  | A competent authority could be a public or private entity in a Member State.                                                                                                                                                                                                                                 |
| Eligible party                         | Business  | An 'eligible party' is an entity offering energy-related services to final customers, such as suppliers, transmission and distribution system operators, delegated operators and other third parties, aggregators, energy service companies, renewable energy communities, citizen energy communities and balancing service providers, as far as they offer energy related services to final customers. |
| eHDV Data Administrator                | Business  | A party responsible for **E**lectric **H**eavy **D**uty **V**ehicle (eHDV) data and distributing these data to eligible parties.                                                                                                                                                                             |
| eHDV Data Permission administrator     | Business  | A party responsible for administering a register of data access permissions for a set of eHDV data, making this information available to final customers and eligible parties in the sector, on request.                                                                                                     |
| eHDV Forecast producer                 | Business  | A party responsible for producing eHDV forecast data                                                                                                                                                                                                                                                         |
| eHDV /Forecast Data access provider    | Business  | A party responsible for access to eHDV /Forecast Data                                                                                                                                                                                                                                                        |
| Electro Mobility Service Provider      | Business  | A party that provides services to the transport company                                                                                                                                                                                                                                                      |
| Grid hosting capacity website provider |           | A party who provides Grid hosting capacity website                                                                                                                                                                                                                                                           |
| General access                         |           | Access for everyone. Access to public data is not constrained and is available to all parties.                                                                                                                                                                                                               |

All roles of type *Business* are expected to be acting in secure, authenticated manner and through trusted communication channels. For this reason, the authentication steps used for these communication partners are not listed in the scenarios below.

### Procedures

The main procedures for the use case are stated in Table III on a overview level and will be explained in more detail in Tables IV.1 - IV.3.

***Table III - Procedure Conditions***

| No. | Procedure name                               | Primary actor             | Pre-condition |
|-----|----------------------------------------------|---------------------------|---------------|
| 1   | Access to eHDV data                          | eHDV data administrator   | None          |
| 2   | Access to eHDV Forecast data                 | Forecast data provider    | None          |
| 3   | Access to Grid hosting capacity information  | DSO                       | None          |

All diagrams describing the scenarios are of an illustrative nature and follow *Business Process Model and Notation 2.0*[^1]*.* Information objects referred in columns *Information exchanged (IDs)* are defined in Table V (To be done). Table IV.1, IV.2 and IV.3 explain the procedures from Table III in more details step by step, together with the information exchanged.

In the following, each procedure is described in steps, whilst each step represents an information exchange between two roles. Each procedure is visualised using a BPMN diagram.

#### Procedure 1 - Access to eHDV data

***Table IV.1 - Procedure steps to access eHDV data***

| Step No. | Step                                              | Step description                                                                                                                                                                       | Information producer (actor) | Information receiver (actor) | Information exchanged (IDs)                       |
|----------|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|------------------------------|---------------------------------------------------|
| 1.1      | Process step for access rights                    | Different access rights for different actors, regulated access, contracted actors, authentication. TBD how to address in reference model, different reference models for different actors or process steps for access rights? |                              |                              |                                                   |
|          | **Process Steps for Data Transfer:**              |                                                                                                                                                                                        |                              |                              |                                                   |
| 1.2      | Request eHDV data                                 | Process Step for eHDV data transfer: Forecast producer specifies the requests eHDV data.                                                                                               | Forecast data provider       | eHDV Data Administrator      | eHDV data request                                 |
| 1.3      | Step for billing                                  | If billing is requested the eHDV Data Administrator provides an invoice                                                                                                                | eHDV Data Administrator      | Forecast data provider       | eHDV Data invoice                                 |
| 1.4      | Step for invoice acceptance                       | If billing is requested the Forecast data providers accepts the invoice                                                                                                                | Forecast data provider       | eHDV Data Administrator      | eHDV Data Invoice acceptance                      |
|          | **Process Steps for Data access:**                |                                                                                                                                                                                        |                              |                              |                                                   |
| 1.5      | Grant access to eHDV data                         | Process Step for eHDV data access: Forecast producer receives access to the requested data                                                                                             | eHDV Data Administrator      | Forecast data provider       | eHDV data                                         |
| 1.6      | Trigger termination of permission                 | Eligible party considers the purpose referred by the permission terminated.                                                                                                            | Eligible party               | eHDV Data Administrator      | Notification of that permission should be terminated |
| 1.7      | Information about terminated permission (voluntary) | eHDV Data Administrator informs eligible party that permission is terminated                                                                                                          | eHDV Data Administrator      | Eligible party               | Notification of permission terminated             |

#### Procedure 2 - Access to eHDV Forecast data

***Table IV.2 - Procedure steps to access eHDV Forecast data***

| Step No. | Step                                              | Step description                                                                                                                                                                       | Information producer (actor) | Information receiver (actor) | Information exchanged (IDs)       |
|----------|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|------------------------------|-----------------------------------|
| 2.1      | Process step for access rights                    | Different access rights for different actors, regulated access, contracted actors, authentication. TBD how to address in reference model, different reference models for different actors or process steps for access rights? |                              |                              |                                   |
|          | **Process Steps for Data Transfer:**              |                                                                                                                                                                                        |                              |                              |                                   |
| 2.2      | Request eHDV Forecast data                        | Process steps for eHDV forecast data transfer: Eligible party specifies the requested eHDV forecast data.                                                                              | Eligible party               | eHDV Forecast data provider  | Forecast data request             |
| 2.3      | Step for billing                                  | If billing is requested the eHDV Forecast provider provides an invoice                                                                                                                 | eHDV Forecast data provider  | Eligible party               | Forecast Data invoice             |
| 2.4      | Step for invoice acceptance                       | If billing is requested the Eligible party accepts the invoice                                                                                                                         | Eligible party               | eHDV Forecast data provider  | Forecast Data Invoice acceptance  |
|          | **Process Steps for Data access:**                |                                                                                                                                                                                        |                              |                              |                                   |
| 2.5      | Grant access to eHDV Forecast data                | **Process steps** for **eHDV** forecast **data transfer:** Eligible party receive the requested eHDV forecast data.                                                                    | eHDV Forecast data provider  | Eligible party               | Forecast data                     |
| 2.6      | Trigger termination of permission                 | Eligible party considers the purpose referred by the permission terminated.                                                                                                            | Eligible party               | eHDV Forecast data provider  | Notification of permission terminated |
| 2.7      | Information about terminated permission (voluntary) | eHDV Data Administrator informs eligible party that permission is terminated                                                                                                          | eHDV Forecast data provider  | Eligible party               | Notification of permission terminated |

#### Procedure 3 - Access to Grid hosting capacity information

***Table IV.3 - Procedure steps to access grid hosting capacity information***

| Step No. | Step                                          | Step description                                                                                                                                                                                                                                                             | Information producer (actor)           | Information receiver (actor)           | Information exchanged (IDs)              |
|----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|----------------------------------------|------------------------------------------|
| 3.1      | Provide grid hosting capacity                 | SO provides Grid hosting capacity information to grid hosting capacity website provider                                                                                                                                                                                      | SO                                     | Grid hosting capacity website provider | Grid Hosting Capacity information        |
| 3.2      | Publish grid hosting capacity information     | Grid hosting capacity website provider publishes grid hosting capacity information on website                                                                                                                                                                                 | Grid hosting capacity website provider | General access                         | Publish grid hosting capacity information |
| 3.3      | Specify grid hosting capacity area (voluntary) | Eligible party has the possibility to define geographical area of interest on the webpage for Grid hosting capacity information on a public webpage. The webpage then presents the Grid hosting capacity information for that area for the Eligible party that put the request. | General access                         | Grid hosting capacity website provider | Grid Hosting Capacity Area information   |
| 3.4      | Read grid hosting capacity information        | Eligible party can read Grid hosting capacity information for the selected area directly on the webpage.                                                                                                                                                                      | Grid hosting capacity website provider | General access                         | Grid Hosting Capacity information        |
| 3.5      | Download grid hosting capacity information    | Eligible party can download Grid hosting capacity information for the selected area directly from the webpage.                                                                                                                                                                | Grid hosting capacity website provider | General access                         | Grid Hosting Capacity information        |

[^1]: Business Process Model and Notation 2.0: [https://www.omg.org/spec/BPMN/2.0.2/PDF](https://www.omg.org/spec/BPMN/2.0.2/PDF)
