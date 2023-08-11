# CA Baseline Condition Profile
<blockquote class="stu-note">
  <p>This profile is seeking community and implementer feedback on whether further constraints on use of verificationStatus are needed.
  <br>
  <br>

  VerificationStatus has been identified by members of our community as having clinical significance, though standardization around its use is still evolving in the international community (particularly in implementation guidance and value sets). We are currently seeking feedback from implementers on current utilization practices before further strengthening guidance on its use.

  <br>

  Feedback can be provided through the <a href="https://simplifier.net/CanadianFHIRBaselineProfilesCA-Core/PatientProfile/~issues">Simplifier issue log for this profile.</a>. Proposed language for inclusion under our Best Practice/Should support section is also welcomed.</p>
</blockquote>

This profile constrains the Condition resource to record a list of problems associated with a patient. It identifies which elements, vocabularies and value sets to be present in the resource when using this profile.

This profile defines localization concepts for use in a Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* code identifying the patient's relevant condition
* reference to a subject

## Must Support Data Elements
Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/HL7-Canada/ca-baseline/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the Canadian Condition profile to aid record matching in databases with many pediatric records.

**Must Support elements:**
* clinical status of the condition
* code identifying the patient's relevant condition
* reference to subject
* onset - estimated or actual date of the condition

## Usage Note
Condition is intended for capturing and querying patient's current and historical problems.
