---
title: Household Footprint Calculation Reference Model
---

Project INSIEME – Reference Model Template

Task 4.2 – SavingsFootprint – Household footprint calculation

CONTEXT:

* [TODO] If possible, please write explanations like recitals.
  CHAPTER  I

Regarding GENERAL  PROVISIONS

Issue  1

On subject  matter  and scope

* [IGNORE FOR NOW]
  Issue 2

On definitions

For the purpose of this implementing regulation, the definitions in Article 2 of Directive (EU) 2019/944, implementing regulations on metering data and demand response data shall apply. In addition, the following definitions shall apply:

* Footprint
* Household
* Third-party footprint user
* Footprint calculator
* Data provider
* Data Space
  CHAPTER II

Regarding [YOUR USE CASE]

[NOTE] Typically define responsibilities last and in close coordination with T5.5 EU Policy and regulation alignment

Article XX

On responsibilities of ROLE1

* ROLE1 shall …
  ANNEX A

A1. The reference model for [YOUR USE CASE]

Table I contains information needed by [Stakeholder1 AND Stakeholder2] to set up for utilising [YOUR USE CASE] in a Member State.

| Table I - General information on Member State environments | Table I - General information on Member State environments | Table I - General information on Member State environments |
| --- | --- | --- |
| ID | Name | Description |
| I1 | Information about footprint calculator |  |
| I2 | Information about data providers |  |
| I3 | Information about Data Space |  |

[TODO] Please describe all HARMONISED ROLES below.

| Table II - Roles | Table II - Roles | Table II - Roles |
| --- | --- | --- |
| Role name | Role type | Role description |
| Consumer (HEMRM role)

Party connected to the grid (HEMRM role)

Final customer / end-customer / household | Business | A party that consumes energy. (This is a Type of Party Connected to the Grid)

A party that contracts for the right to take out or feed in energy at an Accounting Point.

A party connected to the grid that purchases electricity for its own use.
Please note, that this also includes the case of active customer. |
| Consent administrator (HEMRM role) | Business | A party responsible for administrating a register of consents for a domain. The Consent Administrator makes this information available on request for entitled parties in the sector.
“Consent” is the preferred term instead of “permission” because the demo covers households only, i.e. – natural persons. |
| Authentication service provider | Business |  |
| Data provider (HEMRM role) | Business | A party that has a mandate to provide information to other parties in the energy market. |
| Metered Data Administrator (HEMRM role) | Business | A party responsible for storing and distributing validated measured data.
This is a type of Data provider. |
| Energy service company (HEMRM role) | Business | A party offering energy-related services to the Party Connected to Grid, but not directly active in the energy value chain or the physical infrastructure itself. The Energy Service Company (ESCO) may provide insight services as well as energy management services. |
| Eligible party (implementing regulation role) | Business | An entity offering energy-related services to final customers, such as suppliers, transmission and distribution system operators, delegated operators and other third parties, aggregators, energy service companies, renewable energy communities, citizen energy communities and balancing service providers, as far as they offer energy related services to final customers. |

All roles of type Business are expected to be acting in secure, authenticated manner and through trusted communication channels. For this reason, the authentication steps used for these communication partners are not listed in the scenarios below.

[TODO] First step should be to clearly state the list of procedures.

| Table III - Procedure Conditions | Table III - Procedure Conditions | Table III - Procedure Conditions | Table III - Procedure Conditions |
| --- | --- | --- | --- |
| No. | Procedure name | Primary actor | Pre-condition |
| 1 | Customer onboarding | Final customer | Customer is informed about footprint calculation options. Final customer downloads the application from an app store. |
| 2 | Footprint calculation | Energy service company | Footprint calculator has agreement with final customer. Either direct consenting or indirect consenting or both must be applied in order to get any data. |

All diagrams describing the scenarios are of an illustrative nature and follow Business Process Model and Notation 2.0. Information objects referred in columns Information exchanged (IDs) are defined in Table IV.

### Procedure 1 – Customer onboarding

| Step No. | Step | Step description | Information producer (actor) | Information receiver (actor) | Information exchanged (IDs) |
| --- | --- | --- | --- | --- | --- |
| 1.1 | Request authentication | Final customer logs in to the application with his/her credentials. | Final customer | Authentication service provider | A – Final customer identity |
| 1.2 | Validate authentication request | Internal step. If validation fails then energy service company is provided with a meaningful indication. | Authentication service provider | Authentication service provider | A – Final customer identity |
| 1.3 | Send authentication data | Authentication service provider confirms the credentials of final customer using eIDAS compliant authentication solutions. | Authentication service provider | Energy service company | A – Final customer identity |
| 1.4 | Request contract signing | In case of first usage of the application final customer needs to sign a contract with the energy service company. | Energy service company | Final customer | L – Contract |
| 1.5 | Sign contract | Final customer agrees with terms and conditions of using footprint calculator. | Final customer | Energy service company | L – Contract |
| 1.6 | Notify direct consenting | Final customer gives permission to access his/her personal data from various sources. | Final customer | Energy service company | B – Consent |
| 1.7 | Notify indirect consenting | Where available and required, final customer gives permission to access his/her personal data via consent administrator. In this case the steps of first implementing regulation will be followed. | Final customer | Consent administrator | B – Consent |

### Procedure 2 – Footprint calculation

| Step No. | Step | Step description | Information producer (actor) | Information receiver (actor) | Information exchanged (IDs) |
| --- | --- | --- | --- | --- | --- |
| 2.1 | Request indirect consent | If required, energy service company requests the existence of consent via consent administrator. | Energy service company | Consent administrator | B – Consent |
| 2.2 | Validate indirect consent request | Internal step. If validation fails then energy service company is provided with a meaningful indication. | Consent administrator | Consent administrator | B – Consent |
| 2.3 | Send indirect consent | Consent administrator confirms the existence of consent. | Consent administrator | Energy service company | B – Consent |
| 2.4 | Requesting data | Energy service company requests various personal and public data about the final customer. If data is coming from Metered data administrator, then the steps of implementing regulation (EU) 2023/1162 will be followed. | Energy service company | Data provider, incl. Metered data administrator | C – Data request |
| 2.5 | Send requested data | Data providers make relevant data available to energy service company. | Data provider, incl. Metered data administrator | Energy service company | D – Metered data
E – Energy content data
F – Market data
G – Weather data
H – Additional final customer data |
| 2.6 | Execute data analysis | Energy service company analysis the data received from data providers. | Energy service company | Energy service company | N/A |
| 2.7 | Execute footprint calculation | Energy service company calculates the footprint. | Energy service company | Energy service company | I – Calculated footprint |
| 2.8 | Notify footprint | Final customer sees through application summary overview of the progress of his/her consumption, carbon emissions and monetary footprints as well as comparisons with predefined targets. Energy service provider can make footprint information available to third parties. | Energy service company | Final customer
Eligible party | I – Calculated footprint |
| 2.9 | Notify personalized recommendations | Final customer receives personalized recommendations to decrease the consumption footprint, CO2 footprint and/or monetary footprint, and to participate in demand response programs. | Energy service company | Final customer | J – Recommen-dations |
| 2.10 | Notify impact information | Final customer learns the actual impacts resulting from the recommendation which he/she has implemented, and learns the potential benefits if he/she will apply or would have applied different consumption (and on-site generation) pattern. | Energy service company | Final customer | K – Impact |

| Table IV - Information exchanged | Table IV - Information exchanged | Table IV - Information exchanged |
| --- | --- | --- |
| Information exchanged, ID | Name of information | Description of information exchanged |
| A | Final customer identity | FINAL CUSTOMER IDENTIFIER: Unique identifier for the final customer |
| B | Consent | PRESET CONSENT INFORMATION: Follow ‘Preset permission information’ information object in Commission Implementing Regulation (EU) 2023/1162
BASIC CONSENT INFORMATION: Follow ‘Basic permission information’ information object in Commission Implementing Regulation (EU) 2023/1162
ESTABLISHED CONSENT INFORMATION: Follow ‘Established permission information’ information object in Commission Implementing Regulation (EU) 2023/1162 |
| C | Data request | API: Data provider’s API to connect to
DATA TYPE: Metered (D), energy content (E), market (F), weather (G) or additional final customer data (H)
ELECTRICITY METERING POINT IDENTIFIER: Unique identifier for the metering point within the metered data administrator’s meter identification space (as defined in Commission Implementing Regulation (EU) 2023/1162)
DISTRICT HEATING POINT IDENTIFIER: Unique identifier for the district heating metering point
REQUESTED DATA SPECIFICATION: Specification parameters of information object D, E, F, G or H, respectively |
| D | Metered data | e.g. main meter data, sub-meter data, DMD data – including electricity, gas, heating, cooling
To be addressed in FIRST PHASE: electricity main meter data, electricity sub-meter/DMD data, district heating main meter data

SPECIFICATION OF ELECTRICITY MAIN METER DATA: Follow ‘Metered data specification’ information object in Commission Implementing Regulation (EU) 2023/1162
ELECTRICITY MAIN METER DATA: Follow ‘Validated historical data’ information object in Commission Implementing Regulation (EU) 2023/1162
SPECIFICATION OF ELECTRICITY SUB-METER/DMD DATA: Start and end times of time series, data granularity, value unit
ELECTRICITY SUB-METER/DMD DATA: Data creation timestamp. energy values within the time series
SPECIFICATION OF DISTRICT HEATING MAIN METER DATA: Start and end times of time series, data granularity, value unit
DISTRICT HEATING MAIN METER DATA: Data creation timestamp. energy values within the time series |
| E | Energy content data | E.g., energy content of transport fuels, various purchased goods and services
NOT TO BE ADDRESSED IN FIRST PHASE |
| F | Market data | E.g. market prices, balancing market volumes, energy mix data
To be addressed in FIRST PHASE: day-ahead electricity price, mFRR price, imbalance price, mFRR market bids, mFRR market activations, mFRR market settlement, electricity grid tariffs, heating prices

SPECIFICATION OF PUBLIC PRICE AND TARIFF DATA: Start and end times of time series, price type (e.g. day-ahead, imbalance, mFRR, district heating), data granularity, price region, currency
PUBLIC PRICE AND TARIFF DATA: Data creation timestamp. price values within the time series
SPECIFICATION OF PUBLIC mFRR MARKET DATA: Start and end times of time series, data type (e.g. activations, bids, settlement), data granularity, value unit
PUBLIC mFRR MARKET DATA: Data creation timestamp. energy values within the time series
SPECIFICATION OF INDIDUAL mFRR DATA: Start and end times of time series, data type (e.g. activations, bids, settlement), data granularity, value unit
INDIVIDUAL mFRR DATA: Data creation timestamp. energy values within the time series |
| G | Weather data | E.g. outdoor temperature
To be addressed in FIRST PHASE: historical outdoor temperature, forecast of outdoor temperature

SPECIFICATION OF TEMPERATURE DATA: Start and end times of time series, temperature type historical, forecasted), data granularity, value unit
TEMPERATURE DATA: Data creation timestamp. temperature values within the time series |
| H | Additional final customer data | E.g., postal address, size of the home, energy tariff schemes, indoor climate data
To be addressed in FIRST PHASE: electricity grid tariff scheme, electricity tariff scheme (dynamic, fixed), heating tariff scheme, available flexible capacity, characteristics of household (number of persons, size of home)

SPECIFICATION OF INDIVIDUAL TARIFF SCHEME: Tariff scheme type (electricity, electricity grid, district heating)
INDIVIDUAL TARIFF SCHEME: Data creation timestamp, name of the tariff scheme
SPECIFICATION OF AVAILABLE FLEXIBLE CAPACITY: Value unit
AVAILABLE FLEXIBLE CAPACITY: Types/names of flexibility providing devices, capacity value per device
SPECIFICATION OF HOUSEHOLD CHARACTERISTICS: Characteristics type (e.g. number of persons in household, size of home), value unit
HOUSEHOLD CHARACTERISTICS: Data creation timestamp. Characteristics values |
| I | Calculated footprint | OBSERVATION PERIOD: Time interval of footprint measurement
REFERENCE PERIOD: Historical time interval for comparing the footprint measurement of observation period
REFERENCE GROUP: Group of households for comparing the footprint measurement with
ENERGY FOOTPRINT: Total energy used (kWh) per observation period and comparison (kWh, %) with reference period and/or reference group
CARBON FOOTPRINT: Total greenhouse gas emissions of energy used (tCO2e) per observation period and comparison (tCO2e, %) with reference period and/or reference group
MONETARY FOOTPRINT: Total net cost of energy (EUR) per observation period and comparison (EUR, %) with reference period and/or reference group |
| J | Recommendations | TARGET VALUE: Recommended values of energy footprint (kWh), carbon footprint (tCO2e) and monetary footprint (EUR) per time period
RECOMMENDED ACTION: Personalized recommendations to final customer to achieve target value – e.g. savings tips, participation in demand response program, consumption shifts to cheaper time period, change of transportation mode |
| K | Impact | CONSUMPTION IMPACT: Reduced energy consumption (kWh) per time period following the recommendations
ENVIRONMENTAL IMPACT: Reduced greenhouse gas emissions (tCO2e) per time period following the recommendations
FINANCIAL IMPACT: Money saved (EUR) per time period following the recommendations |
| L | Contract | SIGNATURE DATE: Date of signing the contract
CONTRACT VALIDITY: Start and end dates of the contract
FINAL CUSTOMER IDENTIFIER: Unique identifier for the final customer |

[TODO] If it helps for understanding, please add EER and/or class Diagrams for Aggregated and Message Information Models
