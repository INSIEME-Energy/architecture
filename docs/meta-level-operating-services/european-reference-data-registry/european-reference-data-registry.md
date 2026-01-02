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

* Member State information
| Attribute | XML data type | Comments |
|------|-----|------|
| CountryCode | ISO 3166-1 alpha-2 | Standardised two-letter code for MS |
| Name | String | Name of MS |
| Remarks | Text | Remarks on the state of the MS, specificities that should be covered etc. |
| Last update | Datetime | Last point in time reference data for the Member State has been updated. |

### General Member State information

