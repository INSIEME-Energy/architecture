---
title: European Reference Data Registry
order: 3
---

## Contributors

| Responsibility | Name                     | E-Mail                |
|----------------|--------------------------|-----------------------|
| Leader         | Dragos-Constantin Stoica | dragos.stoica@lnds.lu |

## Function and Objective

Hosts certified reference data on roles, actors, and market infrastructures essential for automation.

Typically, this structural data (e.g. lists of important data on Permission Administrators, DSOs or Market Platforms) is highly needed to guarantee an efficient functioning of automated solutions
within the scope of CEEDS. The lack of accessibility of this data places a huge gap for data-driven energy markets as of now (see Deliverable 5.2 of Project EDDIE).

CEEDS Facilitator is responsible to provide standardized interfaces in a Common Information Model for National Data Space Facilitators (NDSF) to provide that data in a standardized manner, as well as
keeping audits and versioning. NDSFs should be responsible to collect and maintain updates of the reference data, and to certify its correctness.

## Business Architecture

<!-- 
The Business Architecture focuses on business requirements. It outlines the structure and operation of an organization, including business goals, functions, processes, and organizational structure. 
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

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

## Data Architecture

<!-- 
Data Architecture pertains to the management of data, both physical and logical.
It involves data assets, databases, data models, and the governance of data across the enterprise.
See: https://www.fconsulting.tech/togaf-10-understanding-the-7-core-concepts/
-->

### Data Objects

<!-- TODO: Insert list/table of data objects and their descriptions -->
The reference model for metering and consumption data access as specified in Annex I of Commission Implementing Regulation (EU) 2023/1162

#### Schema Definition for European Reference Data Object

ID | Name | Description
---|---|---
I1 | National competent authority | Description of Naitonal authority minimum information
I2 | Information on Member State data management set-up | Description of Member State minimum information for data management set-up
I3 | Information about metered data administrators in a Member State | One mapping per each active metered data administrator in a Member State
I4 | Information about metering point administrators in a Member State | One mapping per each active metering point administrator in a Member State
I5 | Information about data access provider | At least one actor must be mapped per each metering point in a Member State
I6 | Information about permission administrators in a Member State | At least one mapping per each active permission administrator in a Member State
I7 | Information about standardised near real-time interfaces of smart meters or smart metering systems in a Member State as by Article 20 point (a) of Directive (EU) 2019/944 | At least one mapping for each interface specification in use for smart meters deployed after July 4 2019 in a Member State must be applicable


#### List and Specification of Reference Data Objects

| Reference Model                     | Procedure                                                               | NCA | PA | MDA | DAP |
|-------------------------------------|-------------------------------------------------------------------------|-----|----|-----|-----|
| IR Demand Response                  | 1: General access to Controllable Unit master data by an entitled party |     |    |     |     |
| IR Demand Response                  | 2: Controllable Unit registration                                       |     |    |     |     |
| IR Demand Response                  | 3: Update Controllable Unit information                                 |     |    |     |     |
| IR Demand Response                  | 4: De-registration Controllable Unit                                    |     |    |     |     |
| IR Demand Response                  | 5: Suspension of Controllable Unit by an entitled party                 |     |    |     |     |
| IR Demand Response                  | 6: Re-activation of Controllable Unit                                   |     |    |     |     |
| IR Demand Response                  | 7: Service Provider registration                                        |     |    |     |     |
| IR Demand Response                  | 8: Service Provider application for qualification                       |     |    |     |     |
| IR Demand Response                  | 9: Service contract revocation by Final Customer                        |     |    |     |     |
| IR Demand Response                  | 10: Service contract termination by Service Provider                    |     |    |     |     |
| IR Demand Response                  | 11: SP Customer switching or new registration on CU                     |     |    |     |     |
| IR Demand Response                  | 12: Cancellation of SP registration on CU                               |     |    |     |     |
| IR Demand Response                  | 15: De-registration of Service Provider                                 |     |    |     |     |
| IR Demand Response                  | 16: Suspension of Service Provider qualification by System Operator     |     |    |     |     |
| IR Demand Response                  | 17: Revocation of service provider                                      |     |    |     |     |
| IR Demand Response                  | 18: Reactivation service provider                                       |     |    |     |     |
| IR Demand Response                  | 19: SPU or SPG grid pre-qualification                                   |     |    |     |     |
| IR Demand Response                  | 20: SPG or SPU product prequalification                                 |     |    |     |     |
| IR Demand Response                  | 21: SPG or SPU product verification                                     |     |    |     |     |
| IR Demand Response                  | 22: SPU or SPG registration                                             |     |    |     |     |
| IR Demand Response                  | 23: SPU or SPG update                                                   |     |    |     |     |
| IR Demand Response                  | 24: SPU or SPG de-registration                                          |     |    |     |     |
| IR Demand Response                  | 25: SPU or SPG application                                              |     |    |     |     |
| IR Demand Response                  | 26: SPU or SPG suspension                                               |     |    |     |     |
| IR Demand Response                  | 27: SPU or SPG re-activation                                            |     |    |     |     |
| IR Demand Response                  | 28: General access to SPU or SPG master data by an entitled party       |     |    |     |     |
| IR Demand Response                  | 29: Bidding and activation of a flexibility product                     |     |    |     |     |
| IR Demand Response                  | 30: Temporary limits                                                    |     |    |     |     |
| IR Demand Response                  | 31: Baseline data handling                                              |     |    |     |     |
| IR Demand Response                  | 32: Making measurement data available                                   |     |    |     |     |
| IR Demand Response                  | 33: Quantification                                                      |     |    |     |     |
| IR Demand Response                  | 34: (Optional) Baseline Validation                                      |     |    |     |     |
| Household Footprint Calculation     | 1: Customer onboarding                                                  |     |    |     |     |
| Household Footprint Calculation     | 2: Footprint calculation                                                |     |    |     |     |
| Customer Energy Management          | 1: Customer onboarding to energy management service                     |     |    |     |     |
| Customer Energy Management          | 2: Configuration of goals and preferences                               |     |    |     |     |
| Customer Energy Management          | 3: Access to historical metering and consumption data                   |     |    |     |     |
| Customer Energy Management          | 4: Access to real-time or near real-time data                           |     |    |     |     |
| Customer Energy Management          | 5: Provision of recommendations and alerts                              |     |    |     |     |
| Customer Energy Management          | 6: Access to data for demand response or third-party services           |     |    |     |     |
| Customer Energy Management          | 7: Termination, Revocation and offboarding                              |     |    |     |     |
| Customer Energy Management          | Implicit Flexibility - Access to grid fee                               |     |    |     |     |
| Customer Energy Management          | Implicit Flexibility - Access to ISP energy price                       |     |    |     |     |
| Customer Energy Management          | ? Implicit Flexibility - Access to ESU grid fee                         |     |    |     |     |
| Customer Energy Management          | ? Implicit Flexibility - Access to ESU energy price                     |     |    |     |     |
| Collective Energy Sharing (CESU)    | 8: Support to short-term flexibility markets                            |     |    |     |     |
| Flexible Connection Agreements      | 1: Initialization of Digital Customer Interface (DCI)                   |     |    |     |     |
| Flexible Connection Agreements      | 2: Onboarding of flexible customer to FCA in DCI                        |     |    |     |     |
| Flexible Connection Agreements      | 3: Revocation of flexible connection agreement by flexible customer     |     |    |     |     |
| Flexible Connection Agreements      | 4: Termination of FCA by Connecting System Operator                     |     |    |     |     |
| Flexible Connection Agreements      | 5: Activation / limitation of flexibility event                         |     |    |     |     |
| eHDV Long-term Power Forecast       | 1: Access to eHDV data                                                  |     |    |     |     |
| eHDV Long-term Power Forecast       | 2: Access to long-term Power Forecast data                              |     |    |     |     |
| eHDV Long-term Power Forecast       | 3: Access to Grid hosting capacity information                          |     |    |     |     |
| eHDV Short-term Power Forecast      | 1: Access Vehicle (eHDV) data                                           |     |    |     |     |
| eHDV Short-term Power Forecast      | 2: Access Road/Traffic data                                             |     |    |     |     |
| eHDV Short-term Power Forecast      | 3: Determine Transport Plan and Charging Plan                           |     |    |     |     |
| Grid-eHDV Short-term Power Forecast | 1: Access Short-term Power Forecast data                                |     |    |     |     |
| Grid-eHDV Short-term Power Forecast | 2: Inform Final Customer                                                |     |    |     |     |
| AIGridOpt (SO–AI Vendor)	           | 1: Establish legal and contractual framework                            |     |    |     |     |
| AIGridOpt (SO–AI Vendor)	           | 2: Set up vendor-hosted secure environment                              |     |    |     |     |
| AIGridOpt (SO–AI Vendor)	           | 3: Prepare and transfer training data                                   |     |    |     |     |
| AIGridOpt (SO–AI Vendor)	           | 4: Train AI models and validate performance                             |     |    |     |     |
| AIGridOpt (SO–AI Vendor)	           | 5: Deploy AI service for day-ahead grid planning                        |     |    |     |     |
| AIGridOpt (SO–AI Vendor)	           | 6: Use AI outputs in SO planning processes                              |     |    |     |     |
| AIGridOpt (SO–AI Vendor)	           | 7: Monitor service performance and compliance                           |     |    |     |     |
| AIGridOpt (SO–AI Vendor)	           | 8: Update and re-train models                                           |     |    |     |     |

#### National competent authority

| Attribute   | XML data type      | Comments                                                                                    |
|-------------|--------------------|---------------------------------------------------------------------------------------------|
| ID          | Unique ID          | Unique ID of master data element within CEEDS.                                              |
| Code        | ISO 3166-1 alpha-2 | Standardised two-letter code for MS                                                         |
| Name        | String             | Name of national competent authoriy as of Commission Implementing Regulation (EU) 2023/1162 |
| Remarks     | Text               | Remarks on the state of the MS, specificities that should be covered etc.                   |
| Last update | Datetime           | Last point in time reference data for the Member State has been updated.                    |

#### Permission administrator

As of Commission Implementing Regulation (EU) 2023/1162, a Permission Administrator is a party responsible for administering a register of data access permissions for a set of metering points, making
this information available to final customers and eligible parties in the sector, on request. The responsiblities of Permission Administrator are defined in Art. 8.

| Attribute                                       | XML data type            | Comments                                                                                         |
|-------------------------------------------------|--------------------------|--------------------------------------------------------------------------------------------------|
| ID                                              | Unique ID                | Unique ID of master data element within CEEDS.                                                   |
| Country                                         | ISO 3166-1 alpha-2       | Standardised two-letter code for MS                                                              |
| Market Role                                     | Harmonised European Role | Official role in the HEMRM. (e.g. DSO)                                                           |
| Full name                                       | String                   | Full name of the organisation.                                                                   |
| Shortname                                       | String                   | Short name of the organisation.                                                                  | 
| Logo                                            | Blob                     | Logo of the organisation (TODO image specs)                                                      |
| Type of identification                          | String                   | Name of identification space (e.g. EAN, EIC, National codes, etc.).                              |
| Identification                                  | String                   | Identification of the organisation within the identification space.                              |
| Online Application URL                          | URL                      | URL to the online application for managing permissions.                                          |
| Website                                         | URL                      | Official website of the organisation.                                                            |
| Official contact                                | String                   | e.g. the email address that can be used in relation to access to metering and consumption data.  |
| Permission Administration for                   | List                     | List of metered data administrators the PA is acting for.                                        |
| Documentation of access                         | String                   | Explanation of how access to metering and consumption data can be realised by an eligible party. |
| Identity service provider                       | String                   | Information on the Identity Service Provider employed as of the reference model.                 |
| Eligible party onboarding (LIVE)                | String                   | Full description for how to onboard to LIVE environment.                                         |
| Eligible party onboarding (TEST)                | String                   | Full description for how to onboard to TEST environment.                                         |
| Price list for access to data by eligible party | String                   | Information on the pricing model (including NDFS structure.                                      |

#### General Member State information

Attribute | XML data type | Comments
---|---|---
ID | Unique ID | Unique ID of master data element within CEEDS for the Member State.
Name | String | Name of data management and exchange environment in accordance with Article 23 of Directive (EU) 2019/944.
Website | URL | Link to website explaining the provisions for data access in a Member State
Official contact | Text | Contact details of the entity responsible for national data management provisions.
National regulatory basis | Text | Reference to the legal basis for the data sharing infrastructure.
Documentation | Text | Description of the Member State provisions with regards to data access.

#### National metered data administrators in a Memeber State

Multiple entries should be made for each active metered data administrator in a Member State.

Attribute | XML data type | Comments
---|---|---
ID | Unique ID | Unique ID of master data element within CEEDS for the Member State.
Name | String | Name of the organisation
Type of identification | Code | ACER registration code, Legal Entity Identifier (LEI), Bank Identifier Code (BIC), Energy Identification Code (EIC), Global Location Number (GLN/GS1) or National Identification Code (NIC).
Identification of organisation | Code | Code or identification of the organisation (nominated as _metered data administrator_) based on the types of identification mentioned in the previous field.
Website | URL | Link to website or application that is used to download data.
Official contact | Text | Contact details of the entity responsible for data access by final customers or eligible parties.
Metering grid area | Text |  Description of the set of metering points for which the metered data administrator is administering metered data.
Status | Code | Code specifying the status of the metered data administrator (e.g. Active, Inactive, Suspended etc.)

#### National metering point adminitrator in a Member State

One mapping per each active metering point administrator in a Member State.

Attribute | XML data type | Comments
--|---|---
ID | Unique ID | Unique ID of master data element within CEEDS for the Member State.
Name | String | Name of the organisation.
Type of identification | Code | ACER registration code, Legal Entity Identifier (LEI), Bank Identifier Code (BIC), Energy Identification Code (EIC), Global Location Number (GLN/GS1) or National Identification Code (NIC).
Identification of organisation | Code |  Code or identification of the organisation (nominated as ‘metering point administrator’) based on the types of identification mentioned in the previous field.
Website | URL | Link to website or application that is used to download data.
Official contact | Text | Contact details of the entity responsible for data access by final customers or eligible parties.
Metering grid area | Text | Description of the set of metering points the metering point administrator is responsible for.

#### Information about data access provider in a Member State

At least one actor must be mapped per each metering point in a Member State.

Attribute | XML data type | Comments
--|---|---
ID | Unique ID | Unique ID of master data element within CEEDS for the Member State.
Name | String | Name of the organisation.
Type of identification | Code | ACER registration code, Legal Entity Identifier (LEI), Bank Identifier Code (BIC), Energy Identification Code (EIC), Global Location Number (GLN/GS1) or National Identification Code (NIC).
Identification of organisation | Code | Code or identification of the organisation based on the types of identification mentioned in the previous field.
Website | URL | If applicable, link to website of a web application that is used for final customer data access.
Official contact | Text | Contact details of the entity responsible for final customer data access.
Permission management responsibility for | String | Metered data administrators for which the data access provider manages final customer data access.
Identity service provider | String | Identity service provider utilised by the data access provider to authenticate final customers.


#### Information about standardised near Real-Time interface of smartmetering system in a Memeber State

At least one mapping for each interface specification in use for smart meters deployed after July 4 2019 in a Member State must be applicable

Attribute | XML data type | Comments
--|---|---
ID | Unique ID | Unique ID of master data element within CEEDS for the Member State.
Name | String | Type designation of the meter model.
Basic class of interface utilised | String |Provide voltage level for which meter model is used. For medium and high voltage, please specify in detail standardised interface or remote access being used. For low voltage, answers should follow the classification (choose applicable option(s)): H1 (as defined in CEN/CENELEC/ETSI TR 50572:2011), H2 (as defined in CEN/CENELEC/ETSI TR 50572:2011), H3 (as defined in CEN/CENELEC/ETSI TR 50572:2011), Remote access (specify in detail)
Vendor | String | Name of the vendor organisation of the smart meter or smart metering system components
Metering point administrators using the model| String | Identifiers of the metering point administrators using the model.
Physical interface standard | String | Name and version of the standard used.
Communication protocol | String | Name and version of the standard used.
Data formats | String | Name and version of the standard used.

The following code lists can be standardized:
- Physical interface standard
- Communication protocol
- Data formats

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
