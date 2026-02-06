# CA Baseline Observation (Laboratory Results) Profile
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
	<blockquote class="stu-note">
		While this profile does not currently apply MS constraints on the hasMember, referenceRange, interpretation or component elements, this profile is seeking community and implementer feedback on how these elements are being used to assess whether consistent patterns can be identified for use in the Canadian landscape for certain types of test results (e.g., panel, antibody, blood tests, etc)
		<br>

		Feedback can be provided through the <a href="https://simplifier.net/CanadianFHIRBaselineProfilesCA-Core/ObservationProfileLaboratory/~issues">Simplifier issue log for this profile</a>.</p>
	</blockquote>
  </div>

This Observation (Laboratory Results) profile further constrains the Observation (General Use) profile to represent results of laboratory tests.

This profile may represent a single value from a specific laboratory test (e.g. hematocrit) or it may represent a grouped set of results from a multi- test study or panel (e.g. complete blood count, urinalysis, electrolytes).

The Observation (Laboratory Results) profile reflects localization concepts in the Canadian context. 

## Mandatory Data Elements
All elements or attributes within the FHIR specification have cardinality as part of their definition - a minimum number of required appearances and a maximum number of allowable appearances.

Most elements in the FHIR specification have a minimum cardinality of **0**, so most elements are not required and subsequently they may be missing from a resource when it is exchanged between systems.

**Required elements:**
*	status of the result value
*	category to classify the general type of observation being made
*	category: laboratory (mandatory child element of above)
*	code to classify what was observed
*	reference to a subject

Note: if Observation.component is provided then Observation.component.value is mandatory.

### Data Absent Reason
If the minimum cardinality of an element or attribute is 1 AND information is missing AND the Responder knows the precise reason for the absence of data, then Responders SHOULD send the reason for the missing information using values from the valueset where it exists by using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.

An Observation without a value, SHOULD include a reason why the data is absent unless there are component observations, or references to other Observations that are grouped within it, i.e., unless there are component observations, or references to other Observations that are grouped within it then either ONE of _Observation.value_ OR _Observation.dataAbsentReason_ but NOT both should be present.

Note: The conformance language above was modified from SHALL to SHOULD to reflect the community decision to relax the invariant to account for Canadian implementations that have reason to not meet the rule given circumstances with R4 modeling for value expressions that is corrected in later versions of FHIR. At least one Canadian lab implementation uses an extension to communicate a result value in the form of a PDF (which R4 does not support under its existing value data types).

## Usage Note
Observation (Laboratory Results) is intended to represent results of laboratory tests and studies. This profile constrains the Observation (General Use) resource to represent laboratory results in messages and patient summaries if no other, more specific profile is more appropriate.

The following list of examples is intended to represent some examples of typical use cases and is not exhaustive:
*	complete blood count
*	prothrombin time
*	basic metabolic panel
*	comprehensive metabolic panel
*	lipid panel
*	liver panel
*	thyroid stimulating hormone
*	hemoglobin a1c
*	culture and sensitivity

including the interpretations and reference ranges associated with the result(s).

Observation (Laboratory Results) should not be used if one of the following profiles is applicable: (to be completed later)
