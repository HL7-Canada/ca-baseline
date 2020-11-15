## Using codes in Observation
Additional codes that translate or map to the Observation code or category codes are allowed (see [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept) data type). 
For example: providing both a local code and LOINC code providing a more specific category codes, SNOMED CT concept, or system specific codes.

## Category
The _Observation.category_ specifies a code that classifies the general type of observation being made. The _Observation.category_ element is [CodeableConcept](http://hl7.org/fhir/R4/datatypes.html#CodeableConcept) data type and more than one code is allowed.
For interoperability reason one of the codes SHOULD be from the FHIR standard defined [Observation Category Codes](https://www.hl7.org/fhir/valueset-observation-category.html).
Local codes are allowed as well. In case of using local codes to better classify the type both _category.coding.system_ and _category.coding.code_ SHOULD be provided.

## Code
The Observation.code element describes what was observed. Sometimes this is called the observation "name".

The [pan-Canadian LOINC Observation Code Database (pCLOCD)](https://infocentral.infoway-inforoute.ca/en/standards/canadian/pclocd-loinc) is recommended for use in a Canadian context. Code System URI is https://fhir.infoway-inforoute.ca/CodeSystem/pCLOCD

## value[x]
If the result value is a code:
* both _valueCodeableConcept.coding.system_ and _valueCodeableConcept.coding.code_ SHALL be present
* a code from [SNOMED CT](http://www.snomed.org) SHOULD be used
* additional codes that translate or map Observation code or category codes are allowed

If the result value is a numeric quantity:
* _valueQuantity.value_ , _valueQuantity.unit_ and _valueQuantity.sytem_ SHALL be present
* a standard [UCUM](http://unitsofmeasure.org) unit SHALL be used.
          
## dataAbsentReason
An Observation without a value SHALL include a reason why the data is absent unless there are component observations, or references to other Observations that are grouped within it.
I.e., if _Observation.value[x]_ is missed, the _Observation.dataAbsentReason_ SHALL be present and provide a reason why the expected value is missing.
Also, the _Observation.dataAbsentReason_ SHALL only be present if _Observation.value[x]_ is not present
