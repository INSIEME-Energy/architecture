---
title: INSIEME T4.5.1 – Long-Term Grid Hosting Capacity and eHDV Forecast Data Reference Model
---

# INSIEME Reference Model
## Long-Term Grid Hosting Capacity Information and eHDV Power Forecast Data Exchange

---

## Context / Whereas

(1) This reference model defines interoperability procedures governing information exchange between Connecting System Operators (CSOs) and electric Heavy-Duty Vehicle (eHDV) ecosystem stakeholders.

(2) The model supports long-term forecasting processes covering a time horizon of 0–10 years. Long-term forecasting complements short-term operational forecasting and supports network development planning.

(3) The reference model aims to enable transparent, interoperable and secure exchange of information regarding:

- Forecasts of grid hosting capacity availability
- Forecasts of future eHDV charging demand

(4) This reference model contributes to implementation of European legislative and policy frameworks including:

- Directive (EU) 2019/944
- Regulation (EU) 2023/1804 (AFIR)
- Regulation (EU) 2024/1747
- Directive (EU) 2024/1711
- CO₂ Regulation (EU) 2019/1242
- Grid Action Plan initiatives

(5) The electrification of heavy-duty transport requires significant grid expansion planning, including infrastructure for large-scale charging deployment.

(6) Connecting System Operators require aggregated and forward-looking charging demand information to support:

- Network Development Plans
- Ten-Year Network Development Plans (TYNDPs)
- Flexibility needs assessments
- Hosting capacity forecasts

(7) Forecast information must respect confidentiality, privacy, and competitiveness considerations and shall rely on aggregated and anonymised datasets where appropriate.

(8) The reference model defines common rules for:

- Role model
- Process model
- Information model

The reference model remains technology neutral.

---

## Definitions

For the purposes of this reference model:

### Reference Model
Procedures describing minimum information exchange requirements between market participants.

### Connecting System Operator (CSO)
A system operator responsible for connecting final customers or infrastructure to the electricity grid.

### eHDV
Electric Heavy-Duty Vehicle.

### eHDV Data
Data describing operational behaviour, usage or charging demand characteristics of eHDVs.

### eHDV Long-Term Forecast
Forecast describing future eHDV charging demand requirements.

### Grid Hosting Capacity Long-Term Forecast
Forecast describing available connection capacity within the grid over a 1–10 year horizon.

### Data Area
Geographic aggregation zone used for forecasting or reporting.

### Data Set
Power or energy data defined over time and geographic scope.

### Eligible Party
Entity offering energy-related services or infrastructure planning services requiring forecast or hosting capacity information.

---

## Responsibilities of Market Roles

### Responsibilities of Connecting System Operator

The Connecting System Operator shall:

1. Compile grid hosting capacity information.
2. Produce long-term hosting capacity forecasts.
3. Provide hosting capacity information to authorised publication platforms.
4. Support network planning and expansion processes.

---

### Responsibilities of eHDV Data Administrator

The eHDV Data Administrator shall:

1. Store and maintain eHDV operational datasets.
2. Provide authorised access to aggregated and anonymised eHDV data.
3. Ensure compliance with data governance and confidentiality requirements.

---

### Responsibilities of eHDV Permission Administrator

The eHDV Permission Administrator shall:

1. Administer access permissions to eHDV data.
2. Maintain permission registries.
3. Ensure compliance with non-disclosure agreements and regulatory requirements.

---

### Responsibilities of eHDV Forecast Producer

The eHDV Forecast Producer shall:

1. Produce forecasts of future charging demand.
2. Use authorised and aggregated input datasets.
3. Provide validated forecast outputs to authorised stakeholders.

---

### Responsibilities of Power Forecast Data Provider

The Power Forecast Data Provider shall:

1. Provide long-term power forecast datasets.
2. Validate forecast requests.
3. Ensure quality and consistency of forecast information.

---

### Responsibilities of Grid Hosting Capacity Publication Provider

The publication provider shall:

1. Publish hosting capacity information.
2. Maintain public and secure access interfaces.
3. Ensure timely and reliable publication of grid hosting capacity information.

---

## Annex

---

## General Information

### Table I – General Information on Member State Environment

| ID | Name | Description |
|------|------------|----------------|
| I1 | National Competent Authority | Authority responsible for regulatory oversight |
| I2 | National Data Exchange Environment | Description of national data governance and exchange frameworks |
| I3 | eHDV Data Administrators | Organisations managing eHDV datasets |
| I4 | Forecast Data Providers | Organisations providing forecast datasets |
| I5 | Hosting Capacity Publication Platforms | Platforms providing hosting capacity information |

---

## Relevant Roles

### Table II – Role Model

| Role Name | Role Type | Role Description |
|------------|-------------|-------------------|
| Eligible Party | Business | Entity requesting access to forecast or hosting capacity data |
| Connecting System Operator | Business | Operator responsible for customer connection to grid |
| eHDV Data Administrator | Business | Responsible for storing and distributing eHDV data |
| eHDV Permission Administrator | Business | Responsible for managing data access permissions |
| eHDV Forecast Producer | Business | Responsible for generating eHDV forecast data |
| Power Forecast Data Provider | Business | Responsible for providing long-term power forecasts |
| Hosting Capacity Publication Provider | Business | Responsible for publishing hosting capacity information |

---

## Procedures

All roles shall operate using secure and authenticated communication channels.

---

### Table III – Procedure Overview

| No. | Procedure Name | Primary Actor | Preconditions |
|--------|--------------------------|-----------------|----------------|
| 1 | Access to eHDV Data | eHDV Data Administrator | Active permission available |
| 2 | Access to Long-Term Power Forecast Data | Power Forecast Data Provider | Active permission available |
| 3 | Access to Grid Hosting Capacity Information | Connecting System Operator | None |

---

## Procedure 1 – Access to eHDV Data

| Step | Description | Information Producer | Information Consumer | Information Object |
|------------|-----------------|------------------|------------------|------------------|
| 1.1 | Submit eHDV Data Request | Forecast Producer | eHDV Data Administrator | eHDV Data Request |
| 1.2 | Validate Request | eHDV Data Administrator | Forecast Producer | Request Validation |
| 1.3 | Provide Invoice (Optional) | eHDV Data Administrator | Forecast Producer | Invoice |
| 1.4 | Transfer eHDV Data | eHDV Data Administrator | Forecast Producer | eHDV Data |

---

## Procedure 2 – Access to Long-Term Power Forecast Data

| Step | Description | Information Producer | Information Consumer | Information Object |
|------------|-----------------|------------------|------------------|------------------|
| 2.1 | Submit Forecast Request | Eligible Party | Forecast Data Provider | Forecast Request |
| 2.2 | Validate Request | Forecast Data Provider | Eligible Party | Request Validation |
| 2.3 | Provide Invoice (Optional) | Forecast Data Provider | Eligible Party | Invoice |
| 2.4 | Transfer Forecast Data | Forecast Data Provider | Eligible Party | Forecast Data |

---

## Procedure 3 – Access to Grid Hosting Capacity Information

| Step | Description | Information Producer | Information Consumer | Information Object |
|------------|-----------------|------------------|------------------|------------------|
| 3.1 | Compile Hosting Capacity Data | CSO | Internal | Hosting Capacity Dataset |
| 3.2 | Transfer Hosting Capacity Data | CSO | Publication Provider | Hosting Capacity Dataset |
| 3.3 | Publish Hosting Capacity Information | Publication Provider | Eligible Parties | Published Hosting Capacity Data |

---

## Data Exchanged

### eHDV Data Request

Attributes:
- Timestamp
- Geographic Area
- Time Period

---

### eHDV Data

Attributes:
- Dataset Timestamp
- Anonymised Vehicle Usage Data
- Vehicle Event Timestamp

---

### Long-Term Power Forecast Data

Attributes:
- Geographic Dataset
- Time Interval
- Unit (MW)
- Forecast Quantity
- Forecast Accuracy Indicators

---

### Grid Hosting Capacity Information

Attributes:
- Available Production Capacity
- Available Consumption Capacity
- Available Storage Capacity
- Station Identifier
- Voltage Level
- Geographic Location
- Forecast Time Horizon

---

## Interoperability Layers

### Business Layer
Defines roles and responsibilities of participating actors.

### Functional Layer
Defines procedures and workflows for data exchange.

### Information Layer
Defines information objects and attributes.

---

## Compliance and Governance

Implementation of this reference model shall:

- Respect EU data protection requirements
- Ensure interoperability with European data exchange standards
- Support cross-border market integration
- Maintain technology neutrality

---
