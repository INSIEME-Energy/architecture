### T4-2_04 - Customer switching

## Context / Whereas

(1) Directive (EU) 2019/944 establishes the right of final customers to switch electricity suppliers in a timely, transparent, and non-discriminatory manner.

(2) Efficient supplier switching procedures contribute to consumer empowerment, enhance competition in retail electricity markets, and facilitate market entry for suppliers and service providers.

(3) This Regulation defines interoperability requirements and transparent procedures governing the exchange of data required for supplier switching processes.

(4) The reference model ensures that market participants share a common understanding of roles, responsibilities, and information exchanges required for supplier switching and cancellation of switching processes.

(5) The reference model is technology neutral and establishes business, functional, and information layer interoperability while allowing Member States to define national communication and implementation mechanisms.

(6) The procedures described in this reference model represent successful execution flows and may be adapted or combined at national level.

---

## Definitions

In this section, each term is defined:

* **'customer switching'** means the process by which a final customer changes electricity supplier.

* **'energy supplier'** means a market participant engaged in supplying electricity to final customers.

* **'balance responsible party'** means a market participant responsible for its imbalances in the electricity market.

* **'affected party'** means a party gaining or losing responsibility for an accounting point due to switching supplier.

* **'entitled party'** means a party that must be informed of accounting point changes following supplier switching or cancellation.

* **'accounting point'** means the metering or connection point where electricity consumption or generation is accounted.

---

## Responsibilities of Market Roles

### Responsibilities of Energy Supplier

1. The energy supplier shall:

(a) authenticate final customer information and confirm consent for switching;

(b) request registration as supplier for an accounting point;

(c) notify final customers of switching results;

(d) request cancellation of switching where applicable;

(e) ensure compliance with contractual obligations and regulatory timelines.

---

### Responsibilities of Metering Point Administrator

1. The metering point administrator shall:

(a) validate supplier switching requests;

(b) update the metering point register;

(c) notify affected and entitled parties of switching outcomes;

(d) process cancellation requests for pending supplier switches;

(e) maintain accurate accounting point information.

---

### Responsibilities of Final Customer

1. The final customer shall:

(a) initiate supplier switching;

(b) provide required identification and authorization;

(c) request cancellation of switching within applicable periods;

(d) enter contractual agreements with suppliers.

---

### Responsibilities of Balance Responsible Party

1. The balance responsible party shall:

(a) assume balancing responsibility associated with the accounting point;

(b) coordinate with energy suppliers and system operators where applicable.

---

## Annex

### General Information

| ID | Name | Description |
|-----|---------|-------------|
| I1 | Register of energy suppliers | Entity responsible for publishing information about active suppliers, including identification scheme, website, and contact details. |
| I2 | Register of balance responsible parties | Entity responsible for publishing information about active balance responsible parties, including identification scheme, website, and contact details. |

---

### Relevant Roles

| Role name | Role type | Role description |
|-------------|------------|------------------|
| Final customer | Business | Customer purchasing electricity for own use. |
| Energy supplier | Business | Market participant providing electricity supply. |
| Balance responsible party | Business | Entity responsible for balancing obligations. |
| Metering point administrator | Business | Party responsible for maintaining accounting point registers. |
| Affected party | Business | Party gaining or losing supply or balancing responsibility. |
| Entitled party | Business | Party receiving updated accounting point information following switching. |

All roles of type Business shall operate through secure and authenticated communication channels.

---

### Procedures

| No. | Procedure Name | Primary Actor | Preconditions |
|------|----------------|----------------|----------------|
| 1 | Switching supplier | Final customer | New supplier registered and authorized by final customer |
| 2 | Cancellation of switching supplier (Optional) | Final customer | Supply contract exists and supply has not yet started |

---

## Procedure 1 – Switching Supplier

| Step No. | Step | Step description | Info producer | Info consumer | Information exchanged |
|------------|----------|-----------------|-----------------|-----------------|-------------------------|
| 1.1 | Contact new supplier | Final customer contacts potential new supplier. | Final customer | New supplier | A – Contact new supplier |
| 1.2 | Check contractual restrictions (optional) | New supplier verifies existing contractual constraints. | New supplier | New supplier | - |
| 1.3 | Resolve contractual issues (conditional) | New supplier exchanges required information with present supplier. | New supplier | Present supplier | - |
| 1.4 | Send issue results | Present supplier communicates outcome to new supplier. | Present supplier | New supplier | - |
| 1.5 | Inform final customer | New supplier informs customer of results. | New supplier | Final customer | B – Validation result |
| 1.6 | Validate accounting point requirements | Supplier determines need for accounting point data. | New supplier | New supplier | - |
| 1.7 | Request accounting point characteristics (optional) | New supplier requests characteristics from administrator. | New supplier | Metering point administrator | C – Accounting point request |
| 1.8 | Validate request | Administrator validates request. | Metering point administrator | Metering point administrator | - |
| 1.9 | Send accounting point characteristics | Administrator sends characteristics or rejection notice. | Metering point administrator | New supplier | D – Accounting point characteristics |
| 1.10 | Inform final customer | Supplier informs customer of validation results. | New supplier | Final customer | B |
| 1.11 | Request switch | Supplier requests registration for accounting point. | New supplier | Metering point administrator | E – Switch request |
| 1.12 | Validate switch request | Administrator validates switch request. | Metering point administrator | Metering point administrator | - |
| 1.13 | Send switch validation results | Administrator sends validation results. | Metering point administrator | New supplier | F – Switch results |
| 1.14 | Inform final customer | Supplier informs customer of switching result. | New supplier | Final customer | B |
| 1.15 | Notify affected parties | Administrator notifies parties affected by switching. | Metering point administrator | Affected parties | H – Switch notification |
| 1.16 | Register new supplier | Administrator updates metering point register. | Metering point administrator | Metering point administrator | - |
| 1.17 | Notify entitled parties | Administrator sends updated characteristics. | Metering point administrator | Entitled parties | G – Updated accounting point characteristics |
| 1.18 | Request meter read (optional) | Supplier requests meter reading. | New supplier | Metered data administrator | Regulation 2023/1162 references |
| 1.19 | Validate meter read request | Metered data administrator validates request. | Metered data administrator | Metered data administrator | - |
| 1.20 | Send meter read | Metered data administrator provides requested reading. | Metered data administrator | New supplier | Regulation 2023/1162 references |

---

## Procedure 2 – Cancellation of Switching Supplier (Optional)

| Step No. | Step | Step description | Info producer | Info consumer | Information exchanged |
|------------|----------|-----------------|-----------------|-----------------|-------------------------|
| 2.1 | Request cancellation | Customer requests cancellation of new supply contract. | Final customer | New supplier | J – Cancellation request |
| 2.2 | Validate cancellation request | Supplier validates contract and switching conditions. | New supplier | New supplier | - |
| 2.3 | Notify validation failure | Supplier informs customer if cancellation rejected. | New supplier | Final customer | B |
| 2.4 | Validate registration of new supplier | Supplier confirms switching registration. | New supplier | New supplier | - |
| 2.5 | Request cancellation in register | Supplier requests cancellation of pending switch. | New supplier | Metering point administrator | K – Cancellation request |
| 2.6 | Validate cancellation request | Administrator validates cancellation. | Metering point administrator | Metering point administrator | - |
| 2.7 | Inform supplier of validation result | Administrator communicates outcome. | Metering point administrator | New supplier | M – Cancellation notification |
| 2.8 | Cancel switch | Administrator removes pending switch registration. | Metering point administrator | Metering point administrator | - |
| 2.9 | Notify affected parties | Administrator informs affected parties. | Metering point administrator | Affected parties | L – Cancellation notification |
| 2.10 | Inform final customer | Supplier informs customer of validation failure if applicable. | New supplier | Final customer | B |
| 2.11 | Cancel contract | Supplier cancels contract with customer. | New supplier | New supplier | - |
| 2.12 | Notify final customer | Supplier confirms cancellation. | New supplier | Final customer | N – Contract cancellation notification |

---

### Data Exchanged

| ID | Name of information object | Definition |
|------|--------------------------|---------------|
| A | Contact new supplier | Accounting point ID, final customer identification, requested supply start date |
| B | Validation result | Outcome of validation steps |
| C | Accounting point characteristics request | Accounting point ID, requesting supplier ID, request reason |
| D | Accounting point characteristics | Accounting point information and future supplier details |
| E | Switch of supplier request | Accounting point ID, new supplier ID, balance responsible party ID |
| F | Switch of supplier results | Switch validation result and rejection reasons |
| G | Notification to entitled parties | Updated supplier and balancing information |
| H | Notification to affected parties | Notification of supplier responsibility gain or loss |
| J | Contract cancellation request | Free format cancellation request |
| K | Request cancellation of switch | Accounting point ID, supplier identification, future supply start date |
| L | Notification cancellation to affected parties | Notification that switch is cancelled |
| M | Cancellation notification to supplier | Validation result for cancellation |
| N | Notification of cancellation to final customer | Confirmation of contract cancellation |
