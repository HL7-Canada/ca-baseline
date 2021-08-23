# CA Baseline AllergyIntolerance Profile
This profile sets minimum expectations for the AllergyIntolerance resource to record, search and fetch allergies/adverse reactions associated with a patient. It documents the relevant allergies or intolerances (conditions) for a patient, describing the kind of reaction, agent(s) that cause it, criticality and the certainty of the allergy/adverse reaction.

This profile defines localization concepts for use in the Canadian context.

## Mandatory Data Elements
All elements or attributes within the FHIR specification have cardinality as part of their definition - a minimum number of required appearances and a maximum number of allowable appearances.

Most elements in the FHIR specification have a minimum cardinality of 0, so most elements are not required and subsequently they may be missing from a resource when it is exchanged between systems.

**Required elements in the AllergyIntolerance profile:**
* subject who has the allergy or intolerance (AllergyIntolerance.patient)

## Must Support Data Elements
Some elements are marked as Must Support. This means that implementations generating, receiving, or otherwise using resources with Must Support elements SHALL provide support for those elements in some meaningful way (see [Must Support](https://build.fhir.org/ig/HL7-Canada/ca-baseline/general-guidance.html#cardinality-and-mustsupport-definitions) definition).

The following elements are marked as Must Support in the AllergyIntolerance profile:

**Must Support elements:**
* clinical status of the allergy or intolerance (AllergyIntolerance.clinicalStatus)
* verification status (AllergyIntolerance.verificationStatus)
* code of the allergy or intolerance (AllergyIntolerance.code)
* reference to a subject (AllergyIntolerance.patient)
* reaction to the allergy or intolerance (AllergyIntolerance.reaction)
* substance that caused the adverse reaction event (AllergyIntolerance.reaction.substance)
* manifestation of clinical symptoms (AllergyIntolerance.reaction.manifestation)
* severity of the reaction event (AllergyIntolerance.reaction.severity)

## Usage Note
The _AllergyIntolerance_ resource instance use could be clinical decision support applications to generate/display warnings about potentially harmful medications; any intolerance to other agents (e.g. intolerance to soaps, dressings, latex, etc.) more relevant for at the bedside care.

### Profile specific implementation guidance

**History of Allergy or Intolerance**

If the patient has been asked and has indicated a history of allergy or intolerance then this information is represented by:
* _AllergyIntolerance.code_ - an appropriate SNOMED CT code
* _AllergyIntolerance.verificationStatus_ element SHALL be one of the following: confirmed | refuted | entered-in-error 

If a patient asserts a history of allergy or intolerance then the following elements SHOULD be populated:
* _AllergyIntolerance.criticality_
* _AllergyIntolerance.severity_
* _AllergyIntolerance.type_


**No Allergy**

If a patient has been asked and has indicated no history of allergies or intolerance then this is represented by:
* _AllergyIntolerance.code_ = "716186003" No known allergy (situation) SNOMED CT code
* _AllergyIntolerance.verificationStatus_ element SHALL be one of the following: confirmed | refuted | entered-in-error 


**Not Asked**

If the patient has NOT been asked or it is NOT possible to obtain information about any history of allergy or intolerance then this situation is represented with NullFlavor codes: 
* _AllergyIntolerance.code_ - NullFalvor code, e.g., "NASK" (Not asked).

If NullFlavor is used then the following elements SHOULD NOT be populated: 
* _AllergyIntolerance.clinicalStatus_ 
* _AllergyIntolerance.verificationStatus_ 
* _AllergyIntolerance.type_ 
* _AllergyIntolerance.category_ 
* _AllergyIntolerance.criticality_ 

and other allergy related elements.

