## Clinical Status

Rules derived from the FHIR Condition resource description: 
* _Condition.clinicalStatus_ SHALL be present if _Condition.verificationStatus_ is not entered-in-error and category is problem-list-item.
* _Condition.clinicalStatus_ SHALL NOT be present if verification Status is entered-in-error.

Rational: Most systems will expect a clinicalStatus to be valued for problem-list-items that are managed over time, but might not need a clinicalStatus for point in time encounter-diagnosis.

## Verification Status

The verification status supports the clinical status of the condition.

The verification status element is labeled as a modifier because the status contains the code refuted and entered-in-error that mark the Condition as not currently valid.

The _Condition.verificationStatus_ is optional considering the use case of using the Condition to populate a problem list where clinically documented problems range from general descriptions (e.g. "short of breath") to specific diagnoses with no verification step. 

## Code

The identification of the the client's relevant condition, problem or diagnosis or recording of "problem absent" or of "problems unknown", as interpreted by the provider.

The _Condition.code_ element is [CodeableConcept](https://www.hl7.org/fhir/datatypes.html#codeableconcept) data type meaning that more than one [Coding](https://www.hl7.org/fhir/datatypes.html#codesystem) sub-elements can be present.
One of these Coding sub-elements SHALL use [Health Concern Code](https://tgateway.infoway-inforoute.ca/vs/healthconcerncode) value set from Canada Health Infoway. Other Coding component are transaltion of the HealthConcernCode to other code systems.
