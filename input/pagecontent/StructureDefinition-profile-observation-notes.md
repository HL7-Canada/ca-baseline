## Using codes in Observation
Additional codes that translate or map to the Observation code or category codes are allowed (see [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept) data type).

Examples:
* providing both a local code and LOINC code
* providing more specific category codes
* providing a SNOMED CT concept
* providing system specific codes

## Category
The _Observation.category_ specifies a code that classifies the type of observation. The _Observation.category_ element is a [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept) data type, and more than one code is allowed.

For interoperability reasons, one of the codes SHOULD be from the FHIR standard defined [Observation Category Codes](https://www.hl7.org/fhir/valueset-observation-category.html).

Local codes are allowed as well. In the case of using local codes, in order to classify the type of observation both _category.coding.system_ and _category.coding.code_ SHOULD be provided.

## Code
The _Observation.code_ element describes what was observed. Sometimes this is called the observation "name".

The [pan-Canadian LOINC Observation Code Database (pCLOCD)](https://infocentral.infoway-inforoute.ca/en/standards/canadian/pclocd-loinc) is recommended for use in the Canadian context. pCLOCD Code System URI is https://fhir.infoway-inforoute.ca/CodeSystem/pCLOCD

## value[x] and dataAbsentReason
Observation (General Use) uses a name-value pair to code data. When the value for the actual observation is not known, i.e., the value for _Observation.value[x]_ is not available, then _Observation.value[x]_ will not be present and the _Observation.dataAbsentReason_ SHALL be present and will provide a reason why the expected value is missing. 
Also, the _Observation.dataAbsentReason_ SHALL only be present if and only if the value for _Observation.value[x]_ is not present.

The same rule applies when _Observation.component_ is used. I.e., if _Observation.component.value[x]_ is missed, then _Observation.component.dataAbsentReason_ SHALL be present with the reason.
