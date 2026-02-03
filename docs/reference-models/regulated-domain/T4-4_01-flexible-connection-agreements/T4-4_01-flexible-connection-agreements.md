---
title: T4-4_01 - Flexible Connection Agreements
---

## Procedure 1
## Procedure 2
## Procedure 3
## Procedure 4
## Procedure 5

<!-- Uncomment as soon as all compilation errors are fixed
## Definitions
For the purpose of this implementing regulation, the definitions in Article 2 of Directive (EU) 2019/944 [TODO and state that the definitions in other pieces of European Legislation] shall apply. In addition, the following definitions shall apply: 

* 'Flexible customer' means an individual system user engaged or willing to engage in a flexibility program.  

* 'Controllable Unit' means a single power-generating module and/or a single demand unit pursuant to Article 2(5) of [RfG NC 2.0] and Article 2(4) of [DC NC 2.0], or an ensemble of power-generating modules and/or demand units behind the same accounting point if these power-generating modules and demand units are commonly controlled by a single Power Control System. 

* 'Power Control System' means a system or a device, which can control or limit the power flows of one or several CUs, to ensure compliance with the performances required and certified in line with the applicable national framework. If required, the power control system should be able to receive or send information. 

* 'Flexibility program' means a structured initiative or framework designed to leverage the flexibility from FCs or CUs to achieve specific objectives within the energy system. These programs are typically organized by system operators, service providers, or regulatory bodies to manage and optimize energy consumption and generation as well as avoid congestion. A flexibility program encompasses frameworks such as market-based flexibility monetization activities by an FSP, direct flexibility mechanisms operated by SOs such a Flexible Connection Agreements, or self-consumption, citizen energy sharing communities. 

* 'Controllable unit operator' means an entity in charge of remotely commanding and controlling CUs and sending and receiving all relevant information and command/control signals to do so. 

* 'Flexibility event' means the end-to-end series of operations and information exchanges pursuant to a given Flexibility program in which a Technical Aggregator orchestrates the activation of CUs with the relevant stakeholders. The flexibility event involves the transmission of a flexibility request or a flexibility offer, an activation message, and the real-time observability, and later settlement with system users.  

* 'Digital customer interface' means a communication link that enables data exchange between network operators (DSOs) and customers or their CUs. It plays a central role in the integration of CUs. 

* 'Digital Customer Interface Operator' means …  

Needed ? 

* 'Technical Aggregator' means an entity responsible for orchestrating a flexibility program on behalf of on or several FCs and monitoring their performance over time.  

* 'Flexibility program facilitator' means an entity representing / aggregating several system users (such as citizen energy community, owner of EV charging points in a parking of a housing complex…) or a flexibility service provider

## Abbreviations 

CU: Controllable Unit

CSO: Connecting System Operator     

CUO: Controllable Unit operator 

FC: Flexible Customer  

FCA: Flexibility Connection Agreement 
SPU: ???
SPG: ???

### Responsibilities of ...

[TODO]

## Annex

Table I contains information needed by [Stakeholder 1 and 2...] to set up for utilising flexbile connection agreement and temporary limits set at SPU, SPG or parts of SPG level (Pursuant to Network Code Demand Response or in the context of any Flexibility program) in a memebr state. 

### General Information

| ID  | Name | Description |
|-----|------|-------------|
| I1  | National competent authority | <ul><li><b>Name:</b> Name of appointed national competent authority.</li><li><b>Website:</b> Website of appointed national competent authority.</li><li><b>Official contact:</b> Contact details for managing the mappings of national practices.</li></ul> |
| I2  | Digital Customer Interfaces employed | <ul><li><b>Name:</b> Name of the digital customer interface.</li><li><b>Link:</b> URL of a website containing documentation on the DCI.</li><li><b>Mode:</b> In-cloud, on-premise, or other (please describe).</li><li><b>Data exchange standards:</b> Documentation of standards and interfaces used for communication with system operators and other relevant actors.<br/>*Note:</b> For each DCI, Procedure 1 must be mapped.*</li></ul> |
| I3  | Information about permission administrators in a Member State | <ul><li><b>Name:</b> Name of the organisation.</li><li><b>Type of identification:</b> ACER, LEI, BIC, EIC, GLN/GS1, or NIC.</li><li><b>Identification of organisation_</b> Code within the selected identification scheme.</li><li><b>Website:</b> Link to the consent administration web application.</li><li><b>User interface:</b> URL or user portal.</li><li><b>Official contact:</b> Contact details for data sharing.</li><li><b>Consent management responsibility for:</b> Metered data administrators covered.</li><li><b>Documentation of access:</b> Explanation of Member State provisions.</li><li><b>Identity service provider:</b> Used for customer authentication.</li><li><b>Eligible party onboarding:</b> Procedure for production environment.</li><li><b>Eligible party test onboarding:</b> Procedure for test environment.</li><li><b>Price list:</b> Costs for eligible parties.</li></ul> |
### Relevant Roles                                                                                                                        
| Role name                                | Role type | Role description                                                                                                                            |
|------------------------------------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| FC                            | Business  | </li><li> A party connected to the grid that is engaged or willing to engage in a flexibility program. </li><li>From Implementing Act on Demand Response. </li><li>As defined in Article 2(3) of Directive (EU) 2019/944. </li><li>This refers to a party connected to the grid that purchases electricity for its own use. <br/>*Note: this also includes the case of active customer and participants of renewable energy communities or citizen energy communities.* |
| CSO (also listed CSO)                 | Business  | </li><li> A system operator operating the network where a customer is connected. </li><li> From Implementing Act on Demand Response                                                                                                                                         |
| CUO (Also named Technical Aggregator)             | Business  | </li><li> A third party operating the CU delegated by the final customer to command and control the CUs on the final customer premises which enables or orchestrates the participation of the final customer in a flexibility program. <br/>*To be checked: consistency with Implementing Act on Demand Response*                                                                                                                                         |
| Digital Customer Interface Operator                | Business  | </li><li>From Implementing Act on Demand Response. The DCI operator constitutes a critical role in establishing the communication channel via the digital interface. It is expected that the system operator, end customer, technical operator, and CUO will hold this role during the initial phase to ensure proper configuration and communication integrity. |

All roles of type Business are expected to be acting in secure, authenticated manner and through trusted communication channels. For this reason, the authentication steps used for these communication partners are not listed in the scenarios below.  

### Procedures

| No. | Procedure Name                              | Primary Actor  | Preconditions                                         |
|-----|---------------------------------------------|----------------|-------------------------------------------------------|
| 1   | Initialization of digital customer interface  | DCI operator | </li><li> The DCI Operator has physical/virtual access to the DCI hardware or service.  |
| 2   |Onboarding of a FC to FCA in the Digital Customer Interface|CUO |</li><li> System user having (or planning to have) a CU on its premises and willing to engage in a flexibility program. </li><li> List of prequalified CUOs made available by the CSO (see Implementing Act on Demand Response). </li><li> CUO is onboarded (see Implementing Act on Demand Response)|
| 3   | Revocation of a flexible connection agreement by the final customer                                            |Final custome| </li><li> A final customer is onboarded to a flexible connection agreement|
| 4   |  Termination of a flexible connection agreement by the CSO                                            |         CSO        | </li><li> A final customer is onboarded to a flexible connection agreement. |
| 5   | RActivation or limitation of flexibility     |CSO | </li><li> CUO operating the CU of one or several FCs. </li><li> The CUO defines and sends per CU the default value of intake / outtake to its (safe state) (consistent with guaranteed capacity for connection agreement) |


## Procedure 1 - Initialization of digital customer Interface

| Step No. | Step | Step description | Information producer (actor) | Information receiver (actor) | Information exchanged (IDs) |
|--------:|------|------------------|------------------------------|------------------------------|-----------------------------|
| 1.1 | Execute Digital Customer Interface (pre-condition) | </li><li> The DCI Operator (final customer or Technical Aggregator) installs and configures the means to communicate directly or indirectly with the CSO. This may be on-premise or cloud-based.  </li><li> Pre-Condition: The DCI Operator has physical/virtual access to the DCI hardware or service. </li><li> Post-Condition: The DCI is operational and can initiate communication with the CSO. | DCI operator | n/a | - |
| 1.2 | Request registration for Digital Customer Interface | </li><li> During setup, the DCI generates or is assigned a unique identification string. This identifier is provided to the DCI Operator and forwarded to the CSO for certification. </li><li> Pre-condition: The DCI is initialized and capable of generating or receiving an identifier. </li><li> Post-condition: The CSO has received the DCI identification information. | DCI operator | (Digital) CSO | 1-A – DCI identification information |
| 1.3 | Validate DCI Registration Request | </li><li> CSO validates that the provided DCI identifier belongs to the final customer and/or to the DCI Operator. This includes checking data consistency and ensuring that contractual and master data are up to date. If applicable, the SO may issue digital credentials and certificates (e.g. PKI/X.509) to secure further interactions. The CSO may employ authentication via eIDAS eID and eIDAS Trust Services (for public/private key creation and timestamp synchronisation). If validation fails, an error flow is triggered providing a meaningful indication to the requester. </li><li> Pre-condition: The CSO has received the DCI identification information. </li><li> Post-condition: The DCI is validated and, if successful, certified credentials are issued; or an error message is sent to the requester. | (Digital) CSO | DCI operator | 2-B – DCI certification information |
| 1.4 | Execute the installation of the certified credential information (post condition) | </li><li> The DCI Operator installs the certified credential information (e.g. CSO-signed authentication certificate) into the DCI. </li><li> Pre-condition: The DCI Operator has received valid certified credential information from the CSO. </li><li> Post-condition: The DCI contains valid, certified credential information, enabling secure communication with the CSO. | DCI operator | DCI operator | - |

| Information exchanged, ID | Name of information | Description of information exchanged |
|--------------------------|---------------------|--------------------------------------|
| 1-A | DCI identification information | </li><li><b> DCI identifier: </b> Identifier used by the DCI in further communication<br> </li><li><b>Certification request:</b> If applicable, a certification request string to be signed by the CSO as a trusted authority<br> </li><li><b>Identifier of the final customer:</b> Final customer identification to be understood by the CSO<br> </li><li><b>Identifier of the CUO:</b> If applicable and if different from the final customer, the identification of the CUO |
| 1-B | DCI certification information | </li><li><b> DCI identification information:</b> 1-A provided for validation<br> </li><li><b>Confirmation result: </b> Result of the step, e.g. to indicate success or invalid data </li><li><b> Signed certificate:</b> If applicable, the signed certificate for the PKI keypair </li><li><b> CSO DCI identification:</b> Identification of the DCI as registered at the CSO (for further communication) |

## Procedure 2 - Onboarding of a FC to FCA in the Digital Customer Interface

Procedure 2 - Onboarding of a FC to FCA in the Digital Customer Interface 
| Step No. | Step                                                       | Step description                                                                                                                                                                                                                      | Information producer (actor)              | Information receiver (actor)              | Information exchanged (IDs)                                  |
|----------|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|----------------------------|--------------------------------------------------------|
| 2.1      | Request network connection                          | The final customer applies for a connection providing in particular power requirement attributes                                                                                                              | Final customer        | CSO             | 2-A Connection application                                         |
| 2.2 | Execute the connection application study | CSO processes the connection request and defines the proposal to the Final Customer:    </li><li> a connection with firm capacity matching the customer request; </li><li>or 1 or several proposals for flexible connection agreements specifying the FCA conditions (if applicable);</li><li> or refusal of connection (if applicable). | CSO                                                                    |              |              |                                          |
| 2.3      | Request to sign connection proposal                                  | CSO sends the connection proposal to the Final customer <br/>*Note: a « regular » connection proposal is consistent with 2-B FCA condition where flexible capacity is 0, time block is «always», and agreed duration of transitory phase is 0* | CSO             | Final Customer   | 2-B FCA conditions                      |
| 2.4      | Sign the connection proposal |The Final Customer: </li><li> accepts the connection proposal; </li><li> or rejects its connection request (it can then restart the process and apply for a different connection).<br/><br/> If the proposal consists in firm connection agreement, then end of Harmonized Role Model description in this procedure, if no need for CU control or real-time access by CSO <br/><br/>If Flexible Connection Agreement or need for CU control or real-time access, process follows next steps                                                                         | Final customer             | CSO   | 2-C-Acceptance of connection proposal                                         |
| 2.5a      | (optional) Request near real time acces                                          |To enable operation of the network with FCA, CSO may require access to near real time energy data access to the final customer                                                                                                                                           | CSO   | Final Customer  | 2-D Near real time data needed by CSO                                         |
| 2.5b      | [if step above is implemented] Send consent for near real time data request          | The final customer accepts or rejects access to the near real time energy data. <br/><br/> If rejects: termination of the connection proposal or limitation to only firm capacity (no flexible capacity), depending of the applicable connection framework                                                                                                           | Final customer   | CSO             | 2-E Customer consent for near real time data needed by CSO                                         |
| 2.6      | Execute selection of CUO                     | The final customer will delegate FCA operation of his CU to a CUO. He thus selects a CUO in the list of prequalified CUOs provided by CSO. Precondition: CSO defines and maintains a list of Prequalified CUOs, and makes it available to Final Customers                                                                                                                                                                       | Final customer   |              |                       |
| 2.7      | Request CUO to command and control its flexible assets                           | The final customer contacts the CUO of its choice and forward data on its FCA conditions <br/>*Note: A «regular» connection proposal is consistent with 2-B FCA condition where flexible capacity is 0, time block is « always », and agreed duration is 0*  | Final customer             | CUO   | 2-B FCA conditions                       |
| 2.8      | Send the service agreement for CU operation | <div> The CUO sends to the Final Customer a proposal for service provision <br/> <br/> The service agreement for CU operation includes at least:  </li><li> consent for data sharing (data with CUO and data to be forwarded to the eligible parties) and command and control by CUO, </li><li> mandate (representation contract) for CUO to interact with CSO on its behalf, </li><li> Service level agreement, </li><li> Other Terms and Conditions                                                                                     | CUO   | Final customer             | 2-F- service agreement for CU operation                     |
| 2.9     | Sign the service agreement for CU operation | The Final Customer accepts (or rejects) the service agreement for CU operation <br/><br/> If rejects: Customer needs to choose another CUO                                                                                  | Final customer   | CUO | 2-G consent for service agreement for CU operation                       |
| 2.10     | Send CUO choice | The CUO informs the CSO on behalf on the Final Customer that it has been chosen as CUO                                                                                                                                      |CUO  | CSO   | 2-H consent for service agreement for CU operation                     |
| 2.11     | Send the Customer consent              | The CUO forwards the final customer consent to all eligible parties                                                                                                                                                           | CUO   | Eligible parties             | 2-I Customer consent to share and access data                     |
| 2.12     | Send FCA technical properties + specifications for data exchange (if step 2.5.a is implemented)                                           | CSO makes available to the CUO all relevant characteristics of the FCA allowing him to technically enable its operation                                                                                             | CSO   | CUO   | 2-J FCA technical specifications                 |
| 2.13     | Execute CU Operation system configuration                                      | The CUO instruments and configures the CU and performs all technical prerequisites on the CU side and on behalf of the final customer to enable the commissioning of the FCA.<br/><br/><br/> Comment: This step may be already or automatically done, for example when installing equipment (such as “plug and play” interfaces)                                                                                                                                     | CUO   |              |                 |
| 2.14     | Send confirmation of the end of CU configuration – operational readiness                                      | The CUO informs the CSO it is ready to execute command and control of the CU of the Final Customer                                                                                                                                     | CUO   | CSO             |     2-K Operational readiness notification             |
| 2.15     | [optional] Notify Final Customer of successful Command and Control                          | Forward information to Final Customer                                                                                                          | CUO   | Final customer | 2-K operational readiness notification                 |
| 2.16a     | (optional) Send information to prepare for the activation test                            |CSO triggers an activation test of the FCA (procedure 5) and associated CU (operated by CUO) to validate readiness for Business-as-usual FCA operation<br/><br/> CSO would send in step 5.4 of procedure 5 information 5-C Limit notification or activation per FC, or over an ensemble of FCs| CSO             | CUO            | 2-L information to prepare for the activation test<br/><br/> 5-C Limit notification or activation per FC, or over an ensemble of FC                                         |
| 2.16b     | [if previous step is implemented] (optional) Send data required by activation test                            | The CUO sends the data in the required optional steps of Procedure 5 <br/>· 5.1b to 5-A Forecasted baseline intake / outtake<br/> · 5.2b and 5.13.b to 5-B near-real time intake / outtake <br/>· 5.5 to 5-D Limitation / activation receipt notification of flexibility event <br/>· 5.8 to 5-B forecasted / impact (power intake / outtake) due to the activation / limitation | CUO             | CSO             | If required in Procedure 5<br/> 5-A Forecasted baseline intake / outtake<br/><br/> 5-B near-real time intake / outtake<br/><br/> 5-D Limitation / activation receipt notification of flexibility event <br/><br/>5-B forecasted / impact (power intake / outtake) due to the activation / limitation                                         |
| 2.16c     | [if previous step is implemented] Validate the performance of the activation test and of the exchange of data                          | CSO assesses whether the activation test is successful                                                                                                          | CSO   |  | 
| 2.16d     | Send acknowledgement of the proper functioning of the FCA                          | CSO informs the CUO that the FCA performs as expected and authorizes commissioning of FCA.<br/><br/> If it does not function as expected, a new activation test may be performed (go to step 2.13) or the FCA is invalidated.                                                                                                          | CSO   |CUO  | 2-L Activation test result confirmation
| 2.16e     | Notify Final Customer of successful Command and Control         | Forward information to Final Customer | CUO           | Final customer             | 2-M Activation test result confirmation                                         |
| 2.17     | Send Final Customer confirmation of Commissioning Authorization                                             | CSO confirms to the Final Customer that its FCA can be commissioned | CSO | CUO             | 2-N FCA Commissioning authorization |


Information exchanged – Procedure 2 – Onboarding of a FC to FCA in the Digital Customer Interface

| Information exchanged, ID | Name of information | Description of information exchanged | 
|----|----|----|
| 2-A | Connection application | </li><li> Power </li><li> (Optional) Type of CU</li><li> (Optional) Connection Point identifier </li><li> (Optional) Requested power per time block | 
| 2-B | FCA conditions |</li><li> Maximum capacity (in both directions (guaranteed and flexible) by time block </li><li> Agreed duration (expected date for granting connection to the entire requested firm capacity or permanent FCA)</li><li> Applicable Network charges </li><li> (optional): Minimum intake/outtake when FCA is activated</li><li> (Optional) Additional contractual information </li><li> (Optional) Need for near real-time data </li><li> (Optional) need for forecast of power intake / outtake</li><li> Safe-state setpoint (minimum guaranteed connection capacity) in case of loss of communication <br/>  | 
| 2-C | Acceptance of connection proposal | </li><li>Y / N |
| 2-D | Near real time data needed by CSO | </li><li> Request for technical data (referred to procedure 5 information object 5-B) specifying at least latency and periodicity |
| 2-E | Customer consent for near real time data needed by CSO | </li><li> Y / N |
| 2-F | Service agreement for CU operation | </li><li> Consent for data sharing (data with CUO and data to be forwarded to eligible parties) and consent for command and control by CUO</li><li> Mandate (representation contract) for CUO to interact with CSO on behalf of the Fina Customer. </li><li> Service level agreement </li><li> Other Terms and Condition | 
| 2-G | Consent for service agreement for CU operation |</li><li> Consent (Y/N)
| 2-H | Chosen CUO |</li><li> ID of CUO
| 2-I | Consent for service agreement for CU operation |</li><li> List of data associated with customer consent
| 2-J | FCA technical specifications |</li><li> 2-B + 2-D</li><li>   Technical parameters such as latency, frequency<</li><li>   Connectivity information (such as IP address, )
| 2-K | Operational readiness notification |</li><li>Ready
| 2-L | Information to prepare for the activation test|To be defined
| 2-M | Activation test result confirmation |</li><li>Successful / Failed </li><li>  Authorized /
| 2-N | FCA Commissioning authorization |</li><li> Authorized firm capacity</li><li>  Authorized Flexible capacity
## Procedure 3 - Revocation of a flexible connection agreement by the final customer

Procedure 3 - Revocation by a Final Customer of a FCA in the Digital Customer Interface 
| Step No. | Step                                                       | Step description                                                                                                                                                                                                                      | Information producer (actor)              | Information receiver (actor)              | Information exchanged (IDs)                                  |
|----------|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|----------------------------|--------------------------------------------------------|
| 3.1      | Request for revocation                          | The final customer requests for a revocation of the flexible connection agreement                                                                                                             | Final customer        | CSO             | 3-A Connection application                                         |
| 3.2 | Validation of the revocation | CSO validates the request for final revocation | CSO                                                                    |     Final Customer         |       3-B Revocation valida-tion       |                                          |
| 3.3      |  (optional) Send new connection conditions                                | CSO informs the final customer about the new (fallback) connection agreement<br/>*Note: The fallback conditions may have been defined at the time of the FCA proposal*| CSO             | Final Customer   | 3-C New (fallback) contractual conditions: same as 2-B except no information on agreed duration                     |
| 3.4 | Validation of the new connection condition | The final customer validates the new connection condition | Final Customer                                                                   |    CSO         |       3-D New (fallback) connection validation      |                                          |
| 3.5 a (optional)      | Send the new connection conditions to CUO                         | If there is still a need for a CUO (need to command and control CU to ensure compliance with firm capacity, or need to provide forecast or near-real time data), the CSO informs the CUO about the revocation and the new connection conditions                                                                                                           | CSO        | CUO             | 3-E Information Object (same as 2-J FCA technical specifications)                                        |
| 3.5 b      | Acknowledge revocation                         | The CUO acknowledges the revocation of FCA                                                                                                             | CUO        | CSO             | 3-F Acknowledgment                                        |

Information exchanged – Procedure 3 –Revocation of a flexible connection agreement by the final customer

| Information exchanged, ID | Name of information | Description of information exchanged | 
|----|----|----|
| 3-A |Revocation request | </li><li> Capacity (in both directions) by time block<br/> </li><li> (Optional) Type of CU <br/>Connection Agreement Point identifier | 
| 3-B |Revocation validation | </li><li> Consent (Y/N) | 
| 3-C | New (fallback) contractual conditions |</li><li> Capacity (in both directions) by time block </li><li> Applicable Network charges </li><li> (Optional) Additional contractual information<br/> </li><li> (Optional) need for near real-time data </li><li> (Optional) Need for forecast of power intake / outtake</li><li> Safe state setpoint (minimum guaranteed connection capacity) in case of loss of communication </li><li> (optional) alternatives<br/> Same as 2B excepts no information on agreed duration|
| 3-D | New (fallback) connection validation | Consent (Y/N) or alternative chosen (if implemented) |
| 3-E | Technical specifications of Connection Agreement | Same as 2-J Technical specifications of Connection Agreement|
| 3-F | Acknowledgement| Received |

## Procedure 4 - Termination of a flexible connection agreement by the CSO

Procedure 4 - Termination by a CSO of a Final Customer to FCA in the Digital Customer Interface 
| Step No.                              | Step              | Step description                  | Information producer (actor)      | Information receiver (actor)  |   Information exchanged (IDs) |
|----------------------------------------|------------------------|-----------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 4.1 | Send final customer information about termination of FCA | CSO informs the final customer about termination of FCA | CSO | Final Customer | 4-A Termination information |
| 4.2 | Send new connection conditions | CSO informs the final customer about the new connection conditions | CSO | Final Customer | 4-B New (fallback) contractual conditions (same as 3-C) |
| 4.3 | Acknowledge new connection conditions (including if implemented choice of alternative) | The Final Customer acknowledges the new connection conditions (or chooses a proposed alternative) | Final Customer | CSO | 4-C New (fallback) connection acknowledgement |
| 4.4 | Send information about termination of FCA to CUO | CSO informs the CUO about termination of the FCA | CSO | CUO | 4-C Information Object |
| 4.5 | Send the new connection conditions to CUO | If there is still a need for a CUO (need to command and control CU to ensure compliance with firm capacity, or need to provide forecast or near-real time data), CSO informs the CUO about the termination and the new connection conditions | CSO | CUO | 4-D Technical specifications of Connection Agreement (same as 2-J and 3-E) |
| 4.6 | Acknowledge termination of FCA | The CUO acknowledges termination of FCA (+ if 4.5 is implemented reception of new connection agreement conditions) | CUO | CSO | 4-E Acknowledgment |


Table IV.4 - Information exchanged – Procedure 4 –Termination of a FC to FCA in the Digital Customer Interface

| Information exchanged, ID | Name of information | Description of information exchanged | 
|----|----|----|
| 4-A | Termination information | </li><li> Information object | 
| 4-B | New (fallback) contractual conditions | Same as 3-C </li><li> Capacity (in both directions (guaranteed) by time block  </li><li> Applicable Network charges  </li><li> (Optional) Additional contractual information </li><li> (Optional) Need for near real-time data  </li><li> (Optional) need for forecast of power intake / outtake </li><li> (Optional) alternatives </li><li> (Optional) Type of CU </li><li> Optional) Connection Agreement Point identifier | 
| 4-C | Information object | </li><li> Same as 4-E |
| 4-D | Technical specifications of Connection Agreement | same as 2-J and 3-E: </li><li> Capacity (in both directions (guaranteed) by time block) </li><li> Applicable Network charges </li><li> (Optional) Additional contractual information </li><li> (Optional) Near real-time needed data </li><li> (Optional) Forecast of power intake / outtake </li><li> (Optional) alternatives </li><li> (Optional) Type of CU </li><li> (Optional) Connection Agreement Point identifier |
| 4-E | Acknowledgement | Received |

Missing here a procedure : if final customer revokes (likely to provoke the end of FCA) or switches CUO (likely same as onboarding in FCA at the step of selecting CUO – in the meantime, capacity may be limited to guaranteed capacity only)
  
## Procedure 5 - Activation or limitation of flexibility 

Procedure 5 – Activation / limitation of Flexibility event
| Step No. | Step | Step description | Information producer (actor) | Information receiver (actor) | Information exchanged (IDs) |
|----|----|----|----|----|----|
| 5.1.a | (optional) Execute computation of the forecasted baseline intake / outtake | The CUO computes (or updates) forecasted baseline intake / outtake for each Final Customer or ensemble of Final Customer (FCA, SPU, SPG or part of SPG) (if there is no activation/limitation) | CUO |  |  |
| 5.1.b | [if previous step is implemented] (optional) Send forecasted baseline intake / outtake | The CUO sends the forecasted baseline intake / outtake for each Final Customer or ensemble of Final Customers (FCA, SPU, SPG or part of SPG). | CUO | CSO and eligible parties | 5-A Forecasted baseline intake / outtake |
| 5.2.a | (optional) Execute computation of the near-real time intake / outtake | The CUO computes (or updates) near-real-time intake / outtake for each Final Customer or ensemble of Final Customer (FCA, SPU, SPG or part of SPG) (if there is no activation / limitation) |  |  |  |
| 5.2.b | [if previous step is implemented] (optional) Send near-real time intake / outtake | The CUO sends the near-real-time intake / outtake for each Final Customer or ensemble of Final Customer (FCA, SPU, SPG or parts of SPG) (if there is no activation/limitation) | CUO | CUO | 5-B near-real time intake / outtake |
| 5.3 | Execute computation of activation / limitation of a flexibility event per Final Customer or ensemble of Final Customers | CSO computes (or updates) the activation / limitation of a flexibility event for each Final Customer or ensemble of Final Customers pursuant to a provision in the connection agreement between itself and each Final Customer (or other relevant framework). | CSO | not applicable | not applicable |
| 5.4 | (optional) Send forecast of possible activation / limitation per Final Customer or ensemble of Final Customers | CSO sends forecasts of requested activation / limitation for each Final Customer or ensemble of Final Customers (FCA, SPU, SPG or part of SPG) <br/> <br/>*Note: CSO may be able to inform the CUO in advance of a possible activation / limitation later on.* | CSO | CUO | 5-C Limit notification or activation per FC, or over an ensemble of FCs |
| 5.5 | Send activation / limitation per Final Customer or ensemble of Final Customers | CSO sends the requested activation / limitation for each Final Customer or ensemble of Final Customers (FCA, SPU, SPG or part of SPG). | CSO | CUO | 5-C Limit notification or activation per FC, or over an ensemble of FCs |
| 5.6 | (optional) Acknowledge the activation / limitation of a flexibility event | The CUO acknowledges the activation / limitation back to the CSO | CUO | CSO | 5-D Limitation / activation receipt notification of flexibility event |
| 5.7 | Notify eligible parties (e.g. suppliers, BRPs…) | CSO notifies all affected parties regarding the activation / limitation of the Final Customer (s). | CUO | Eligible parties | Same as 5-C |
| 5.8 | Execute the allocation of activation / limitation per site & CU, and the computation of the forecasted impact (power intake / outtake) per Final Customer or ensemble of Final Customers | The CUO computes (or updates) </li><li> The activation or limitation per site and per CU to comply with the activation / limitation of a flexibility event per Final Customer or ensemble of Final Customers </li><li> The forecasted impact (power intake / outtake for each Final Customer or ensemble of Final Customers (FCA, SPU, SPG or part of SPG)) | CUO |  |  |
| 5.9 | (optional) Send forecast / impact (power intake / outtake) due to the activation / limitation  | The CUO sends forecasted / planned impact (power intake / outtake for each Final Customer or ensemble of Final Customers (FCA, SPU, SPG or part of SPG)) due to the activation / limitation | CUO | CSO + eligible parties | Same as 5-B |
| 5.10 | Send the activation per Final Customer and CU | The CUO activates or limits each CU | CUO | CU | 5-E CU limit / activation notification |
| 5.11 | Acknowledge the activation / limitation at CU leve | The CU acknowledges the activation / limitation back to the CUO | CU | CUO | 5-F Limitation / activation receipt notification at CU level |
| 5.12 | Execute CU limit to default value (safe state mode) in case of communication failure | If the CU limit has not received any communication from the CUO since a given delay (x min or hours), the CU is automatically limited to the default (safe state) value. | CU |  |  |
| 5.13 | (optional) Notify eligible parties (e.g. Final Customer, affected service providers) about CU activation / limitation | The CUO notifies all affected parties that need to be informed that an activation / limitation has been received and split per site & CU. | CUO | Eligible parties | Same as 5-E |
| 5.14.a | (optional) Execute computation of the near-real time intake / outtake | The CUO computes (or updates) near-real-time intake / outtake for each Final Customer or ensemble of Final Customer (FCA, SPU, SPG or part of SPG) (if there is no activation / limitation) |  |  |  |
| 5.14.b | (optional) Send near-real time intake / outtake | The CUO sends the near-real-time intake / outtake for each Final Customer or ensemble of Final Customer (FCA, SPU, SPG or part of SPG) (if there is no activation/limitation) | CUO | CSO and eligible parties | 5-B near-real time intake / outtake |

**Important note:**

This procedure loops: steps 5.13.a and 5.13.b are the same as steps 5.2.a and 5.2.b.


**This procedure considers a single CUO per site, which will be the case for the overwhelming majority of Final Customers.**

The limitations set by CSO must be respected by the Final Customer, regardless the number of CUOs active within its premises.

If there are several CUOs active on premises, the Final Customer shall designate a “Master CUO” which will be responsible for ensuring the respect of any limitation /activation order set by a CSO on the Final Customer i.e. allocating the flexibility activated or limited at the connection / connection agreement point among all CUOs that are active within the Final Customer premises, that is the Master CUO and all subsequent CUOs. In such a case, procedure 5 would need to be adapted where the Master CUO would send orders or limitations directly to its own CU, or per System user to other all subsequent CUOs, which in turn will send orders or limitations to their own CUs.

An allocation rule should be defined by the Final Customer, such as priority to activate assets or priority to not activate assets.

Additional rules should be defined, specifying whether the master CUO is eligible to know the identity of subsequent CUO or whether they should be anonymized, rules if there is incompliance of a subsequent CUO and so forth. Such rules, procedures and data exchange would be complex and difficult to streamline.

This procedure considers a single CUO per site, which will be the case for the overwhelming majority of Final Customers.

Information exchanged: Procedure 5 – Activation or limitation of flexibility event
| Information exchanged, ID | Name of information | Description of information exchanged |
|----|----|----|
| 5-A | Forecasted baseline intake / outtake | </li><li> Time series of active / reactive power in both directions |
| 5-B | Near real time intake / outtake | </li><li>Actual power (active / reactive) |
| 5-C | Limit notification or activation per FC, or over an ensemble of FCs | </li><li> Maximum Active / reactive Power in one or both directions <br/> </li><li> Time frame (start time / end time) </li><li> (Optional) Minimum active / reactive power in one or both directions </li><li> (Optional) Legal or contractual provision pursuant to the limitation or activation </li><li> Identification of the FC, or the ensemble of FCs |
| 5-D | (Optional) Limitation / activation receipt notification of flexibility event | </li><li> (Optional): yes, I have received and can comply </li><li> (Optional): yes, I have received and cannot comply |
| 5-E | CU limit / activation notification at CU level | </li><li> Maximum and/or minimum Active / reactive Power in one or both directions </li><li> Time frame (start time / end time) |
| 5-F | (Optional) Limitation / activation receipt notification at CU level | </li><li> (Optional): yes, I have received and can comply </li><li> (Optional): yes, I have received and cannot comply |

Missing procedures:

· Onboarding of local services: provided by NCDR

· Onboarding of energy communities: provided by Task 4.3

· Procedures for back office and settlement to be reviewed and adapted from the procedures for Network Code Demand Response

-->