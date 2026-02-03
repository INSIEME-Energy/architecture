---
title: T4-4_01 - Flexible Connection Agreements
---

## Context / Whereas

(1) Directive (EU) 2019/944 introduced provisions enabling consumers and system users to participate in flexibility services and demand response mechanisms. These provisions require interoperability, transparency, and secure exchange of information between market participants.

(2) This Regulation contributes to implementing flexibility programs including flexible connection agreements, temporary operational limits, and market or rules-based flexibility mechanisms.

(3) Flexibility programs enable system operators and service providers to leverage controllable demand and generation to maintain grid stability, manage congestion, and optimize network planning.

(4) The reference model described in this Regulation defines common roles, responsibilities, and procedures enabling interoperability across Member States while allowing national customisation at communication and component layers.

(5) The reference model is technology neutral and focuses on business, function, and information layers, while Member States may define communication protocols and technical infrastructure according to national practices.

(6) The reference model defines workflows supporting onboarding, operation, revocation, termination, and activation of flexibility services.

(7) Implementation of harmonised procedures supports market access, facilitates innovation, and promotes efficient use of distributed energy resources.

---

## Definitions

In this section, each term is defined:

* **'flexible customer'** means a system user engaged or willing to engage in a flexibility program.

* **'controllable unit (CU)'** means a single or aggregated demand or generation unit under coordinated control.

* **'controllable unit operator (CU operator)'** means an entity responsible for remotely controlling and operating controllable units.

* **'flexibility program'** means a structured framework enabling activation or limitation of energy consumption or generation to support system operation.

* **'flexibility event'** means a coordinated sequence of actions and information exchanges activating or limiting flexibility.

* **'digital customer interface (DCI)'** means a communication interface enabling data exchange between network operators and customers or their controllable units.

* **'technical aggregator'** means an entity responsible for coordinating flexibility services across multiple customers or units.

* **'connecting system operator'** means the system operator responsible for the network connection point.

---

## Responsibilities of Market Roles

### Responsibilities of Connecting System Operator

1. The connecting system operator shall:

(a) define and communicate flexible connection agreement conditions;

(b) provide technical specifications required for operating controllable units;

(c) send activation or limitation instructions for flexibility events;

(d) validate onboarding and commissioning of flexibility services;

(e) ensure secure and non-discriminatory communication with stakeholders.

---

### Responsibilities of Controllable Unit Operator

1. The controllable unit operator shall:

(a) configure controllable units to comply with contractual requirements;

(b) transmit operational data including forecasts and real-time measurements;

(c) execute activation or limitation instructions received from system operators;

(d) notify system operators and eligible parties about operational readiness and performance.

---

### Responsibilities of Flexible Customer

1. The flexible customer shall:

(a) provide consent for data sharing and control of controllable units;

(b) select a controllable unit operator where applicable;

(c) comply with activation or limitation instructions;

(d) maintain contractual arrangements supporting flexibility participation.

---

### Responsibilities of Digital Customer Interface Operator

1. The digital customer interface operator shall:

(a) provide secure communication between customers and system operators;

(b) ensure proper authentication and certification of interfaces;

(c) maintain operational availability of communication systems.

---

## Annex

### General Information

| ID | Name | Description |
|-----|---------|-------------|
| I1 | National competent authority | Name, website and official contact details of authority responsible for flexibility regulation. |
| I2 | Digital customer interfaces employed | Name, documentation link, deployment mode and data exchange standards used for flexibility communication. |
| I3 | Consent administration environment | Organisations responsible for managing customer permissions and data access for flexibility services. |

---

### Relevant Roles

| Role name | Role type | Role description |
|-------------|------------|------------------|
| Flexible customer | Business | A system user participating in flexibility services. |
| Connecting system operator | Business | Network operator responsible for managing grid connection and operational limits. |
| Controllable unit operator | Business | Entity responsible for operation and control of controllable units. |
| Digital customer interface operator | Business | Entity operating communication interfaces between system operators and customers. |

All business roles are expected to operate through secure and authenticated communication channels.

---

### Procedures

| No. | Procedure Name | Primary Actor | Preconditions |
|------|----------------|----------------|----------------|
| 1 | Initialization of Digital Customer Interface | DCI Operator | Physical or virtual access to DCI available |
| 2 | Onboarding of Flexible Customer to FCA | Flexible Customer | Customer willing to participate in flexibility program |
| 3 | Revocation of Flexible Connection Agreement by Customer | Flexible Customer | Active FCA exists |
| 4 | Termination of Flexible Connection Agreement by CSO | Connecting System Operator | Active FCA exists |
| 5 | Activation or Limitation of Flexibility Event | Connecting System Operator | Operational controllable unit available |

---

## Procedure 1 – Initialization of Digital Customer Interface

| Step No. | Step | Step description | Info producer | Info consumer | Information exchanged |
|------------|----------|-----------------|-----------------|-----------------|-------------------------|
| 1.1 | Execute interface setup | DCI operator installs and configures communication system. | DCI operator | - | - |
| 1.2 | Request interface registration | Unique identifier is generated and forwarded to connecting SO. | DCI operator | Connecting SO | A – DCI identification information |
| 1.3 | Validate registration | Connecting SO validates identifier and issues credentials. | Connecting SO | DCI operator | B – Certification information |
| 1.4 | Install credentials | Credentials are installed into the interface. | DCI operator | - | - |

---

## Procedure 2 – Onboarding of Flexible Customer to FCA

| Step No. | Step | Step description | Info producer | Info consumer | Information exchanged |
|------------|----------|-----------------|-----------------|-----------------|-------------------------|
| 2.1 | Request connection | Customer submits connection application. | Flexible customer | Connecting SO | C – Connection application |
| 2.2 | Connection study | SO evaluates connection and FCA conditions. | Connecting SO | Flexible customer | D – FCA conditions |
| 2.3 | Sign connection agreement | Customer accepts or rejects proposal. | Flexible customer | Connecting SO | E – Connection acceptance |
| 2.4 | Select CU operator | Customer selects qualified CU operator. | Flexible customer | CU operator | D – FCA conditions |
| 2.5 | Configure controllable unit | CU operator prepares CU for participation. | CU operator | Connecting SO | F – Operational readiness |
| 2.6 | Commission FCA | Connecting SO authorizes commissioning. | Connecting SO | Flexible customer | G – FCA commissioning authorization |

---

## Procedure 3 – Revocation of FCA by Flexible Customer

| Step No. | Step | Step description | Info producer | Info consumer | Information exchanged |
|------------|----------|-----------------|-----------------|-----------------|-------------------------|
| 3.1 | Request revocation | Customer submits revocation request. | Flexible customer | Connecting SO | H – Revocation request |
| 3.2 | Validate revocation | SO validates revocation and defines fallback conditions. | Connecting SO | Flexible customer | I – Fallback conditions |
| 3.3 | Notify CU operator | CU operator is informed if control remains necessary. | Connecting SO | CU operator | J – Technical specifications |

---

## Procedure 4 – Termination of FCA by Connecting System Operator

| Step No. | Step | Step description | Info producer | Info consumer | Information exchanged |
|------------|----------|-----------------|-----------------|-----------------|-------------------------|
| 4.1 | Notify termination | SO informs customer of termination. | Connecting SO | Flexible customer | K – Termination notification |
| 4.2 | Provide fallback conditions | New connection conditions are provided. | Connecting SO | Flexible customer | I – Fallback conditions |
| 4.3 | Notify CU operator | CU operator informed of termination. | Connecting SO | CU operator | J – Technical specifications |

---

## Procedure 5 – Activation or Limitation of Flexibility Event

| Step No. | Step | Step description | Info producer | Info consumer | Information exchanged |
|------------|----------|-----------------|-----------------|-----------------|-------------------------|
| 5.1 | Compute baseline | CU operator computes forecast baseline. | CU operator | Connecting SO | L – Baseline forecast |
| 5.2 | Send real-time data | CU operator sends operational measurements. | CU operator | Connecting SO | M – Real-time data |
| 5.3 | Send activation instruction | SO issues activation or limitation order. | Connecting SO | CU operator | N – Activation command |
| 5.4 | Execute CU control | CU operator implements activation on units. | CU operator | CU | O – CU activation |
| 5.5 | Confirm execution | CU confirms receipt and compliance. | CU | CU operator | P – Activation confirmation |

---

### Data Exchanged

| ID | Name of information object | Definition |
|------|--------------------------|---------------|
| A | DCI identification information | Identifier and certification request for DCI |
| B | Certification information | Credential and validation confirmation |
| C | Connection application | Technical and contractual connection parameters |
| D | FCA conditions | Flexible capacity and operational constraints |
| E | Connection acceptance | Customer acceptance or rejection |
| F | Operational readiness notification | Confirmation CU is operational |
| G | FCA commissioning authorization | Authorization to activate FCA |
| H | Revocation request | Customer request to revoke FCA |
| I | Fallback connection conditions | Default firm capacity and operational rules |
| J | Technical specifications | Technical configuration for CU operation |
| K | Termination notification | SO notification terminating FCA |
| L | Forecasted baseline intake/outtake | Baseline forecast data |
| M | Near real-time intake/outtake | Real-time operational data |
| N | Activation or limitation instruction | Flexibility command |
| O | CU activation instruction | Activation instructions per CU |
| P | CU activation confirmation | Confirmation of compliance |


