---
title: INSIEME T4.5 – Long-Term Power Forecast Reference Model
---

# INSIEME Reference Model
## Long-Term Power Forecast – Connecting System Operators and eHDV Ecosystem

---

## Context / Whereas

(1) This reference model establishes interoperability procedures for exchange of long-term power forecast information between Connecting System Operators (CSOs) and stakeholders of the electric Heavy-Duty Vehicle (eHDV) ecosystem.

(2) Long-term forecasts cover a time horizon of 0-10 years and support network planning, investment planning, and infrastructure deployment.

(3) The reference model supports exchange of information regarding future charging demand, network development planning and flexibility assessment.

(4) The model contributes to implementation of European energy legislation and policy initiatives including:

- Directive (EU) 2019/944
- Regulation (EU) 2024/1747
- Directive (EU) 2024/1711
- Regulation (EU) 2023/1804 (AFIR)
- CO₂ Regulation (EU) 2019/1242
- ENTSO-E Ten-Year Network Development Planning processes

(5) Electrification of heavy-duty transport requires substantial infrastructure planning and grid reinforcement.

(6) CSOs require aggregated forecasts of future charging demand to support hosting capacity planning and investment decision-making.

---

## Definitions

### Long-Term Power Forecast
Forecast describing anticipated electricity demand or generation capacity for future time horizons.

### Connecting System Operator (CSO)
System operator responsible for connecting infrastructure or customers to the grid.

### eHDV Forecast Producer
Entity responsible for producing charging demand forecasts based on fleet behaviour.

### Eligible Party
Entity authorised to access forecast datasets for service provision or planning activities.

### Data Area
Geographical aggregation zone used for forecast modelling.

### Data Set
Power or energy data defined across time and geography.

---

## Responsibilities of Market Roles

### Responsibilities of Connecting System Operator

The CSO shall:

1. Define forecast data requirements.
2. Provide network planning input parameters.
3. Use forecast data for grid expansion planning.
4. Ensure interoperability of forecast data exchange.

---

### Responsibilities of eHDV Forecast Producer

The Forecast Producer shall:

1. Produce aggregated charging demand forecasts.
2. Validate forecast methodologies.
3. Provide forecast datasets to authorised parties.
4. Ensure compliance with confidentiality requirements.

---

### Responsibilities of Forecast Data Access Provider

The Forecast Data Access Provider shall:

1. Manage authorised access to forecast datasets.
2. Validate access requests.
3. Ensure secure and interoperable data exchange.

---

## Annex

---

## Relevant Roles

### Table II – Roles

| Role Name | Role Type | Role Description |
|------------|------------|------------------|
| Connecting System Operator | Business | Responsible for grid planning and connection capacity |
| eHDV Forecast Producer | Business | Responsible for producing charging demand forecasts |
| Forecast Data Access Provider | Business | Responsible for providing access to forecast data |
| Eligible Party | Business | Entity requesting forecast datasets |

---

## Procedures

### Table III – Procedure Overview

| No. | Procedure Name | Primary Actor | Preconditions |
|------|-----------------|----------------|----------------|
| 1 | Access to Long-Term Power Forecast Data | Eligible Party | Authorised access |

---

## Procedure 1 – Access to Long-Term Power Forecast Data

| Step | Description | Producer | Consumer | Information |
|--------|-----------------|------------|-------------|--------------|
| 1.1 | Submit Forecast Request | Eligible Party | Forecast Provider | Forecast Request |
| 1.2 | Validate Request | Forecast Provider | Eligible Party | Validation Result |
| 1.3 | Transfer Forecast Data | Forecast Provider | Eligible Party | Forecast Dataset |

---

## Data Exchanged

### Long-Term Power Forecast Data

Attributes:

- Timestamp
- Geographic dataset (WGS84 polygon or equivalent)
- Time interval
- Unit (MW)
- Forecast quantity
- Forecast accuracy indicators

---

## Interoperability Layers

### Business Layer
Defines stakeholder roles and governance responsibilities.

### Functional Layer
Defines procedures governing forecast data exchange.

### Information Layer
Defines forecast dataset attributes and structure.

---

## Compliance and Governance

Implementation shall:

- Respect EU data protection legislation
- Support cross-border interoperability
- Remain technology neutral  
