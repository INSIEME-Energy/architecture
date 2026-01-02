---
title: European Reference Data Registry
order: 3
---

## Function and Objective
Hosts certified reference data on roles, actors, and market infrastructures essential for automation. 

Typically, this structural data (e.g. lists of important data on Permission Administrators, DSOs or Market Platforms) is highly needed to guarantee an efficient functioning of automated solutions within the scope of CEEDS. The lack of accessibility of this data places a huge gap for data-driven energy markets as of now (see Deliverable 5.2 of Project EDDIE). 

CEEDS Facilitator is responsible to provide standardized interfaces in a Common Information Model for National Data Space Facilitators (NDSF) to provide that data in a standardized manner, as well as keeping audits and versioning. NDSFs should be responsible to collect and maintain updates of the reference data, and to certify its correctness.

## Archimate Service Realisation Viewpoint

<img width="1336" height="902" alt="image" src="https://github.com/user-attachments/assets/574af7c8-876d-4ccd-816f-bb252c7fae51" />

## Archimate Application Cooperation Viewpoint

## Reference Data Objects(s)

### Schema Definition for European Reference Data Object

### List and Specification of Reference Data Objects

#### National competent authority
  
| Attribute | XML data type | Comments |
|------|-----|------|
| ID | Unique ID | Unique ID of master data element within CEEDS. |
| Code | ISO 3166-1 alpha-2 | Standardised two-letter code for MS |
| Name | String | Name of national competent authoriy as of Commission Implementing Regulation (EU) 2023/1162 |
| Remarks | Text | Remarks on the state of the MS, specificities that should be covered etc. |
| Last update | Datetime | Last point in time reference data for the Member State has been updated. |

#### Permission administrator

As of Commission Implementing Regulation (EU) 2023/1162, a Permission Administrator is a party, which...

| Attribute | XML data type | Comments |
|------|-----|------|
| ID | Unique ID | Unique ID of master data element within CEEDS. |
| Country | ISO 3166-1 alpha-2 | Standardised two-letter code for MS |
| Market Role | Harmonised European Role | Official role in the HEMRM. (e.g. DSO) |
| Full name | String | Full name of the organisation. |
| Shortname | String | Short name of the organisation. | 
| Logo | Blob | Logo of the organisation (TODO image specs) |
| Type of identification | String | Name of identification space (e.g. EAN, EIC, National codes, etc.). |
| Identification | String | Identification of the organisation within the identification space. |
| Online Application URL | URL | URL to the online application for managing permissions. |
| Website | URL | Official website of the organisation. |
| Official contact | String | e.g. the email address that can be used in relation to access to metering and consumption data. |
| Permission Administration for | List | List of metered data administrators the PA is acting for. |
| Documentation of access | String | Explanation of how access to metering and consumption data can be realised by an eligible party. |
| Identity service provider | String | Information on the Identity Service Provider employed as of the reference model. |
| Eligible party onboarding (LIVE) | String | Full description for how to onboard to LIVE environment. |
| Eligible party onboarding (TEST) | String | Full description for how to onboard to TEST environment. |
| Price list for access to data by eligible party | String | Information on the pricing model (including NDFS structure. |


### General Member State information

