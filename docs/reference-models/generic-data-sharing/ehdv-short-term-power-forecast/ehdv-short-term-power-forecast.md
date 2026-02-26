---
title: eHVD Short Term Power Forecast
---


# Reference model for *Short-term Power Forecast*

Task 4.5 -- Electromobility: Short-term Power Forecast

## Context

(1)     For the context of the present document, a short-term forecast considers a time window from the current operational hour and extending up to weeks ahead and differs from a long-term forecast that typically considers a time horizon of 0-10 years.

(2)     The energy sector is undergoing rapid transformation driven by decarbonization, decentralization, digitalization and electrification.

(3)     The growing integration of intermittent production, energy storage, intermittent consumption, such as charging of electric Heavy-Duty Vehicles (eHDV), and electrification of industrial processes increases the need for reliable short-term power forecasts with a time horizon of a couple of weeks down to 15 min.

(4)     The connecting system operator (CSO) must safeguard that the necessary resources (e.g. flexible consumption and production) are planned for and procured in energy and power markets to maintain distribution, transmission and/or system stability.

(5)     Significant grid users (SGU) are subject to specific obligations regarding data exchange, system observability, and participation in grid operations.

(6)     All SGUs are mandated to share power forecasts with CSO to enable such planning (Commission Regulation (EU) 2017/1485 (SO GL)).

(7)     A significant grid user is connected to the grid and affects its operation. These can include Final Customers with a demand of ≥1 MW. The implementation varies across Member States.

(8)     Stakeholders, including Final Customers, Charge Point Operators (CPO) and other market participants, require a harmonized approach to power information sharing. To support the deployment of eHDVs it is necessary to facilitate the transparent flow of information for secure and predictable charge planning.

(9)     Misunderstandings in communication of power information create problems for stakeholders. Users of eHDVs need to know in advance the availability of power for a certain charging stop, to be able to plan, arrive on time with goods and avoid fines for late arrival.

(10)     Currently, there are several business models between CSO and CPO and the only available information is the installed peak power (static information), which may differ significantly from the actual average power per hour for a specific hour of a specific day (dynamic information).

(11)     Business models such as connection agreements, time-based contracts, load-balancing, flexible connection agreements and dynamic connection agreements require a harmonized approach to information sharing.

(12)     Time-based contracts have different power levels for different time periods. The contract is static.

(13)     A flexible connection agreement guarantees the customer a minimum power level. When a curtailment is required, the Connecting System Operator (CSO) informs the customer at a predefined time, specifying the reduced power level.

(14)     A dynamic connection agreement guarantees the customer a minimum power level. At a predefined time, the Connecting System Operator (CSO) informs the customer if additional power beyond the minimum can be delivered.

(15)     Load balancing can be used by a CSO to divide power between different users within a certain pre-defined limit, or it can be applied by a CPO to split available power from the CSO between different chargers on a site.

(16)     It is possible that several combinations of these business models can be applied which hinders estimating the actual average power per hour that can be used for planning of eHDV charging.

## Definitions

CHAPTER I

Regarding GENERAL PROVISIONS

*Issue 1*

**On subject matter and scope**

(1) [IGNORE FOR NOW]

*Issue 2*

**On definitions**

For the purpose of this document, the following definitions shall apply:

## Responsibilities of Market Roles

CHAPTER II

Regarding [YOUR USE CASE]

**[NOTE] Typically define responsibilities last and in close coordination with *T5.5 EU Policy and regulation alignment***

*Article XX*

**On responsibilities of ROLE1**

### Responsibilities of ROLE1

1.  ROLE1 shall ...

## Annex

ANNEX A

**A1. The reference model for [YOUR USE CASE]**

Table I contains information needed by [Stakeholder1 AND Stakeholder2] to set up for utilising [YOUR USE CASE] in a Member State.

### General Information

| ID  | Name                         | Description                                                                                                                                                                                                           |
|-----|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| I1  | To be determined             |                                                                                                                                                                                                                       |

### Relevant Roles

**[TODO] Please describe all *HARMONISED ROLES* below.**

| Role name                                | Role type | Role description                                                                                                                            |
|------------------------------------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Eligible party                           | All       | An 'eligible party' is an entity offering energy-related services to Final Customers. Examples include transmission and distribution system operators, delegated operators and other third parties, aggregators, energy service companies, renewable energy communities, citizen energy communities and balancing service providers. |
| Power forecast data provider             | Business  | A party responsible for providing power forecast data                                                                                        |
| System Operator                          | Business  | A System Operator (SO) is a Distribution System Operator (DSO) and/or Transmission System Operator (TSO)                                    |
| Connecting System Operator               | Business  | Connecting System Operator (CSO) As defined in Article 2 of Network Code on Demand Response (NCDR)                                          |
| Final Customer                           | Business  | As defined in Article 2(3) of Directive (EU) 2019/944, this refers to a party connected to the grid that purchases electricity for its own use. Note: This also includes the case of active Customer(s) and participants of renewable energy communities or citizen energy communities |

### Procedures

**PROCEDURES**

All roles are expected to be accessing information in secure, authenticated manner and through trusted communication channels. For this reason, the authentication steps used for these communication partners are not listed in the scenarios below.

An overview of the main procedures for the use case is presented in Table III. More details are included in Tables IV.1 -- IV. 2.

| No. | Procedure Name                              | Primary Actor                | Preconditions                                         |
|-----|---------------------------------------------|------------------------------|-------------------------------------------------------|
| 1   | Access Short-term Power Forecast data<br/>(Category: Result Submission & Delivery) | Power Forecast data provider | The eligible party has permission to access the requested data. User consent or regulation. |
| 2   | Inform Final Customer<br/>(Category: Result Submission & Delivery) | CSO                          | The eligible party has permission to access the requested data. User consent or regulation. |

All diagrams describing the procedures are of an illustrative nature. Information objects referred to in column Information exchanged (IDs) are defined in Table V (work in progress). Table IV.1 and IV.2 explain the procedures from Table III in further detail, step by step, together with the information exchanged.


#### Procedure 1 - Access Short-term Power Forecast data

| Step No. | Step                                        | Step description                                                                                                                                | Information producer (actor) | Information receiver (actor) | Information exchanged (IDs)                           |
|----------|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|------------------------------|-------------------------------------------------------|
| 1.1      | Send Short-term Power Forecast data request | Process steps for power forecast data transfer: Eligible party specifies the requested power forecast data.                                      | Eligible party               | Power Forecast data provider | (A) Short-term Power Forecast data request            |
| 1.2      | Execute validating request                  | Validate request from eligible party. In case of an invalid request, a meaningful indication is provided                                         | Power Forecast data provider |                              |                                                       |
| 1.3      | Send Invoice                                | If billing is required the Forecast provider provides an invoice. Otherwise, proceed to 1.5.                                                     | Power Forecast data provider | Eligible party               | (B) Short-term Power Forecast Data invoice            |
| 1.4      | Execute Invoice acceptance                  | If billing is requested, the Eligible party accepts the invoice. In case of an invalid request, a meaningful indication is provided.              | Eligible party               | Power Forecast data provider | (C) Short-term Power Forecast Data Invoice acceptance |
| 1.5      | Send Short-term Power Forecast data         | Process steps for Power forecast data transfer: Eligible party receive the requested forecast data.                                               | Power Forecast data provider | Eligible party               | (D) Short-term Power Forecast data                    |

!["Figure1"](./Figure1.png)

Figure 1. Diagram corresponding to the procedure in Table IV.1

#### Procedure 2 - Inform Final Customer

| Step No. | Step                                                              | Step description | Information producer (actor) | Information receiver (actor) | Information exchanged (IDs)                                      |
|----------|-------------------------------------------------------------------|------------------|------------------------------|------------------------------|------------------------------------------------------------------|
| 2.1      | Send Power Level information for firm connection agreement        |                  | CSO                          | Final Customer               | (E) Power level information                                      |
| 2.2      | Send Power Level information for time-based contracts             |                  | CSO                          | Final Customer               | (F) Power level information for time-based contracts             |
| 2.3      | Send Load Balancing information                                   |                  | Eligible party               | Final Customer               | (G) Load Balancing information                                   |
| 2.4      | Send Power Level information for flexible connection agreement    |                  | CSO                          | Final Customer               | (H) Power level information for flexible connection agreement (how long) |
| 2.5      | Send Power Level information for dynamic connection agreement     |                  | CSO                          | Final Customer               | (I) Power level information for dynamic connection agreement     |


!["Figure1"](./Figure2.png)

Figure 2. Diagram corresponding to the procedure in Table IV.2

### Data Exchanged

**INFORMATION OBJECTS**

The technical specification of information objects is under development.

| ID  | Name of information object                                                 | Definition of attributes of exchanged information object                                                                                                      |
|-----|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (A) | Short-term Power Forecast data request                                     | *Timestamp* - Timestamp when the data package has been generated. Datetime object according to ISO8601<br/>*Dataset for area [degree] (WGS 84)* - A dataset of coordinates defining a geographical area (polygon)<br/>*(Optional) mRID* - Master Resource Identifier is a global consistent identification of any network model object. MRID will be used when agreed with eligible party that that produces information.<br/>*Periodicity (constant)* - e.g., quarterly or hourly<br/>*Time period start* - Datetime object according to ISO8601<br/>*Time period end* - Datetime object according to ISO8601<br/>*Forecast object* - e.g., maximum over 60 minutes, 95% confidence interval over one day, etc. |
| (B) | Short-term Power Forecast data Invoice                                     | *Timestamp* - Timestamp when data request was processed. Datetime object according to ISO8601<br/>*Invoice Specifications* - A standard invoice generated in line with the supplier's specifications |
| (C) | Short-term Power Forecast data Invoice acceptance                          | *Timestamp* - Timestamp when Invoice was processed. Datetime object according to ISO8601<br/>*Acceptance acknowledgement* - A standard invoice acceptance acknowledgement generated in line with the customer's specifications |
| (D) | Short-term Power Forecast data                                             | *Timestamp* - Timestamp when the data package has been generated. Datetime object according to ISO8601<br/>*Dataset identification* - The identification name of the dataset<br/>*(Optional) Dataset for area [degree] (WGS 84)* - Dataset of coordinates defining a geographical area (polygon)<br/>*If dataset represents mRID* - Master Resource Identifier is a global consistent identification of any network model object. MRID will be used when agreed with eligible party that that produces information.<br/>*Unit* - [MW]<br/>*Quantity* - Predicted volume to be consumed or generated<br/>*Time period start* - Datetime object according to ISO8601<br/>*Time period end* - Datetime object according to ISO8601<br/>*(Optional) Forecast accuracy* - Standard deviation, confidence intervals, etc. Alternatively, best/worst case scenarios |
| (E) | Power level information                                                    | *Timestamp* - Timestamp when the data package has been generated. Datetime object according to ISO8601<br/>*Metering point identification* - The identification name of the Final Customer<br/>*Unit* - [MW]<br/>*Type of connection* - Consumption / Production<br/>*Quantity* - Volume for consumption or production<br/>*Time period start* - Datetime object according to ISO8601<br/>*Time period end* - Datetime object according to ISO8601 |
| (F) | Power level information for time-based contracts                           |                                                                                                                                                               |
| (G) | Load Balancing information                                                 | *To be determined* - To be determined                                                                                                                         |
| (H) | Power level information for flexible connection agreement (how long)       | *Timestamp* - Timestamp when the data package has been generated. Datetime object according to ISO8601<br/>*Metering point identification* - The identification name of the Final Customer<br/>*Unit* - [MW]<br/>*Type of connection* - Consumption / Production<br/>*Flexible Quantity* - Volume for consumption or production<br/>*Firm Quantity* - Volume for consumption or production<br/>*Time period start* - Datetime object according to ISO8601<br/>*Time period end* - Datetime object according to ISO8601 |
| (I) | Power level information for dynamic connection agreement                   |                                                                                                                                                               |
