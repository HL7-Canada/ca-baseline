## Category
The _ServiceRequest.category_ element conveys a code that classifies the service for searching, sorting and display purposes.

It may use Canada Health Infoway defined [InterventionCodeSubsetCare](https://tgateway.infoway-inforoute.ca/singlesubset.html?id=2.16.840.1.113883.2.20.3.271&versionid=20200930) value set to represent the care procedures performed by a Provider.

## Code
The _ServiceRequest.code_ element identifies a particular service (i.e., procedure, diagnostic investigation, or panel of investigations) that have been requested.

If the service identified by the _ServiceRequest.category_ is _laboratory procedure_ the _pan-Canadian LOINC Observation Code Database_ ([pCLOCD](https://infocentral.infoway-inforoute.ca/en/standards/canadian/pclocd-loinc)) is preferred. pCLOCD is the Canadian version of the LOINC(tm) database. 

## Reason Code
The _ServiceRequest.reasonCode_ element in this profile uses the same [ProcedureReasonCodes](https://www.hl7.org/fhir/valueset-procedure-reason.html) value set as defined by the FHIR standard.

The binding is chagned from [Example](https://www.hl7.org/fhir/terminologies.html#example) to [Preferred](https://www.hl7.org/fhir/terminologies.html#preferred). Implementers are encouraged to draw codes from the specified code system for interoperability purposes. 
