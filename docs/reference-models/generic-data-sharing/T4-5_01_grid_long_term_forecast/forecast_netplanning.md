---
title: INSIEME T4.5.2 – Forecast Netplanning Reference Model
---

# INSIEME Reference Model
## Forecast-Driven Network Planning Interoperability Model

---

## Context / Whereas

(1) This reference model establishes interoperability procedures supporting forecast-driven network planning between Connecting System Operators and forecast data stakeholders.

(2) The reference model supports integration of long-term demand and flexibility forecasts into grid development planning processes.

(3) Forecast-driven network planning enables proactive infrastructure investment and supports efficient utilisation of grid assets.

(4) The reference model contributes to implementation of European policy and regulatory frameworks including:

- Directive (EU) 2019/944
- Regulation (EU) 2024/1747
- ENTSO-E Network Development Planning frameworks
- EU Grid Action Plan

---

## Definitions

### Network Planning Forecast
Forecast datasets supporting long-term network expansion decisions.

### Forecast Data Provider
Entity producing forecast datasets used for network planning.

### Connecting System Operator
Entity responsible for network planning and hosting capacity evaluation.

### Planning Stakeholder
Authorised entity using forecast data to support infrastructure planning.

---

## Responsibilities of Market Roles

### Responsibilities of Connecting System Operator

The CSO shall:

1. Integrate forecast datasets into network planning processes.
2. Validate forecast inputs.
3. Use forecast outputs for infrastructure investment planning.
4. Provide planning requirements and feedback loops.

---

### Responsibilities of Forecast Data Provider

The Forecast Data Provider shall:

1. Produce validated forecast datasets.
2. Provide datasets in interoperable formats.
3. Maintain dataset quality and transparency.

---

### Responsibilities of Forecast Access Provider

The Forecast Access Provider shall:

1. Manage authorised access to planning forecast datasets.
2. Maintain secure exchange interfaces.

---

## Annex

---

## Relevant Roles

### Table II – Roles

| Role Name | Role Type | Role Description |
|------------|------------|------------------|
| Connecting System Operator | Business | Responsible for infrastructure planning |
| Forecast Data Provider | Business | Responsible for producing planning forecasts |
| Forecast Access Provider | Business | Responsible for providing authorised data access |
| Planning Stakeholder | Business | Entity using forecast data for planning decisions |

---

## Procedures

### Table III – Procedure Overview

| No. | Procedure Name | Primary Actor | Preconditions |
|------|-----------------|----------------|----------------|
| 1 | Access to Network Planning Forecast Data | Planning Stakeholder | Authorised access |

---

## Procedure 1 – Access to Network Planning Forecast Data

| Step | Description | Producer | Consumer | Information |
|--------|-----------------|------------|-------------|--------------|
| 1.1 | Submit Forecast Planning Request | Planning Stakeholder | Forecast Provider | Planning Forecast Request |
| 1.2 | Validate Request | Forecast Provider | Planning Stakeholder | Validation Result |
| 1.3 | Transfer Forecast Planning Data | Forecast Provider | Planning Stakeholder | Forecast Planning Dataset |

---

## Data Exchanged

### Network Planning Forecast Dataset

Attributes:

- Geographic planning area
- Time horizon
- Forecasted demand or generation capacity
- Flexibility indicators
- Confidence interval indicators

---

## Interoperability Layers

### Business Layer
Defines governance and planning responsibilities.

### Functional Layer
Defines workflows for forecast integration.

### Information Layer
Defines dataset semantics and data attributes.

---

## Compliance and Governance

Implementation shall:

- Ensure interoperability with European data exchange frameworks
- Support cross-border infrastructure planning
- Maintain transparency and neutrality  
