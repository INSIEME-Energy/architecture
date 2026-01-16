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

| Reference Model | Procedure | NCA | PA | MDA | DAP |
|---|---|---|---|---|---|
IR Demand Response | 1: General access to Controllable Unit master data by an entitled party | | | 
IR Demand Response |	2: Controllable Unit registration | | | 			
IR Demand Response |	3: Update Controllable Unit information  | | | 							
IR Demand Response |	4: De-registration Controllable Unit									
IR Demand Response |	5: Suspension of Controllable Unit by an entitled party	 | | | 
IR Demand Response |	6: Re-activation of Controllable Unit	 | | | 		
IR Demand Response |	7: Service Provider registration  | | | 									
IR Demand Response |	8: Service Provider application for qualification  | | | 
IR Demand Response |	9: Service contract revocation by Final Customer  | | | 
IR Demand Response |	10: Service contract termination by Service Provider  | | | 				
IR Demand Response |	11: SP Customer switching or new registration on CU  | | | 					
IR Demand Response |	12: Cancellation of SP registration on CU	 | | | 							
IR Demand Response |	15: De-registration of Service Provider		 | | | 							
IR Demand Response |	16: Suspension of Service Provider qualification by System Operator	 | | | 	
IR Demand Response |	17: Revocation of service provider  | | | 
IR Demand Response |	18: Reactivation service provider  | | | 							
IR Demand Response |	19: SPU or SPG grid pre-qualification  | | | 								
IR Demand Response |	20: SPG or SPU product prequalification	 | | | 							
IR Demand Response |	21: SPG or SPU product verification	 | | | 					
IR Demand Response |	22: SPU or SPG registration	 | | | 				
IR Demand Response |	23: SPU or SPG update  | | | 					
IR Demand Response |	24: SPU or SPG de-registration  | | | 							
IR Demand Response |	25: SPU or SPG application  | | | 						
IR Demand Response |	26: SPU or SPG suspension  | | | 							
IR Demand Response |	27: SPU or SPG re-activation | | | 								
IR Demand Response |	28: General access to SPU or SPG master data by an entitled party  | | | 
IR Demand Response |	29: Bidding and activation of a flexibility product	 | | | 
IR Demand Response |	30: Temporary limits  | | | 
IR Demand Response |	31: Baseline data handling	 | | | 
IR Demand Response |	32: Making measurement data available | | | 	
IR Demand Response |	33: Quantification	 | | | 	
IR Demand Response |	34: (Optional) Baseline Validation	 | | | 	
Household Footprint Calculation |	1: Customer onboarding	 | | | 			
Household Footprint Calculation	| 2: Footprint calculation	 | | | 	
Customer Energy Management	| 1: Customer onboarding to energy management service	 | | | 
Customer Energy Management	| 2: Configuration of goals and preferences	 | | | 
Customer Energy Management	| 3: Access to historical metering and consumption data	 | | | 
Customer Energy Management	| 4: Access to real-time or near real-time data	 | | | 
Customer Energy Management	| 5: Provision of recommendations and alerts  | | | 
Customer Energy Management	| 6: Access to data for demand response or third-party services	 | | | 
Customer Energy Management	| 7: Termination, Revocation and offboarding  | | | 
Customer Energy Management	| Implicit Flexibility - Access to grid fee	 | | | 
Customer Energy Management	| Implicit Flexibility - Access to ISP energy price	 | | | 
Customer Energy Management	| ? Implicit Flexibility - Access to ESU grid fee  | | | 
Customer Energy Management	| ? Implicit Flexibility - Access to ESU energy price  | | | 
Collective Energy Sharing (CESU)	| 8: Support to short-term flexibility markets	 | | | 
Flexible Connection Agreements	| 1: Initialization of Digital Customer Interface (DCI)	 | | | 
Flexible Connection Agreements	| 2: Onboarding of flexible customer to FCA in DCI	 | | | 
Flexible Connection Agreements	| 3: Revocation of flexible connection agreement by flexible customer  | | | 
Flexible Connection Agreements	| 4: Termination of FCA by Connecting System Operator  | | | 	
Flexible Connection Agreements	| 5: Activation / limitation of flexibility event  | | | 
eHDV Long-term Power Forecast	| 1: Access to eHDV data  | | | 	
eHDV Long-term Power Forecast	| 2: Access to long-term Power Forecast data  | | | 
eHDV Long-term Power Forecast	| 3: Access to Grid hosting capacity information  | | |
eHDV Short-term Power Forecast	| 1: Access Vehicle (eHDV) data	 | | |		
eHDV Short-term Power Forecast	| 2: Access Road/Traffic data  | | |
eHDV Short-term Power Forecast	| 3: Determine Transport Plan and Charging Plan | | |
Grid-eHDV Short-term Power Forecast	| 1: Access Short-term Power Forecast data | | |
Grid-eHDV Short-term Power Forecast	| 2: Inform Final Customer | | |			
AIGridOpt (SO–AI Vendor)	| 1: Establish legal and contractual framework | | |
AIGridOpt (SO–AI Vendor)	| 2: Set up vendor-hosted secure environment | | |
AIGridOpt (SO–AI Vendor)	| 3: Prepare and transfer training data | | |						
AIGridOpt (SO–AI Vendor)	| 4: Train AI models and validate performance  | | |
AIGridOpt (SO–AI Vendor)	| 5: Deploy AI service for day-ahead grid planning  | | |
AIGridOpt (SO–AI Vendor)	| 6: Use AI outputs in SO planning processes  | | |
AIGridOpt (SO–AI Vendor)	| 7: Monitor service performance and compliance | | |
AIGridOpt (SO–AI Vendor)	| 8: Update and re-train models | | |


#### National competent authority
  
| Attribute | XML data type | Comments |
|------|-----|------|
| ID | Unique ID | Unique ID of master data element within CEEDS. |
| Code | ISO 3166-1 alpha-2 | Standardised two-letter code for MS |
| Name | String | Name of national competent authoriy as of Commission Implementing Regulation (EU) 2023/1162 |
| Remarks | Text | Remarks on the state of the MS, specificities that should be covered etc. |
| Last update | Datetime | Last point in time reference data for the Member State has been updated. |

#### Permission administrator

As of Commission Implementing Regulation (EU) 2023/1162, a Permission Administrator is a party responsible for administering a register of data access permissions for a set of metering points, making this information available to final customers and eligible parties in the sector, on request. The responsiblities of Permission Administrator are defined in Art. 8.

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

