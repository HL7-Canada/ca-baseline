## Verification Status
The _AllergyIntolerance.verificationStatus_ element is optional (i.e., cardinality is 0..1) in this profile since a typical use would involve clinical decision support that produces warnings when potentially dangerous medications/treatments might be prescribed. 

There is potential for confounding/conflicting information if verification status "overrides" a clinical finding of an allergy or intolerance. 

In addition allergies/intolerance are usually reported by the patient and rarely verified probable that this information is not collected and not available, therefore data element is not populated except by default (presumably as "unconfirmed") again leading to problematic data for clinical decision support.

This is also problematic with respect to interoperability considerations.

## Code
If the _AllergyIntolerance.code_ element represents NullFlavor concept (i.e., no known allergy) then the _verificationStatus_ element SHALL be present.

Rational is that recording "no known allergy" without an assessment would a patient safety issue and should not happen. It is not consistent with clinical practice.

## Substance
The identification of the specific substance (or pharmaceutical product) considered to be responsible for the Adverse Reaction event uses Substance Code value set with [Example](https://hl7.org/fhir/R4/terminologies.html#example) binding.
Consider use [Canadian Clinical Drug Data](https://tgateway.infoway-inforoute.ca/package/canadianclinicaldrugdatasetccdd) set in case of medication allergy/intolerance, and SNOMED CT for other substances/agents.

## Manifestation
The _AllergyIntolerance.reaction.manifestation_ element is a required element to provide symptoms and/or signs that are observed or associated with the adverse reaction event. 

```diff
-Consider developing a value set from MEDDRA for drug reactions
```
