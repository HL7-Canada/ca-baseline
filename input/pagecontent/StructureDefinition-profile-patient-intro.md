<!--- Text entered into this file will appear at the top of the profiles page before the Formal Views of the profile content. -->
# CA Baseline Patient Profile
<blockquote class="stu-note">
  <p>This profile is seeking community and implementer feedback on whether further relaxation of the 1..1 cardinality is needed on the Patient.identifier.type & .system & .value elements.
  <br>
  <br>

  Due Diligence Reviews identified the above elements as 1..1 cardinality but not in the equivalent eReferral Specification profile. This variance is believed to be due to the eReferral Specification profile not necessarily expecting a Patient to always have a health card (or at minimum a health card number). General consensus from Due Diligence Review is that the cardinalities should not be relaxed in the CA Baseline. Feedback can be provided through the Simplifier issue log for this profile.
  <br>

  Feedback can be provided through the <a href="https://simplifier.net/CanadianFHIRBaselineProfilesCA-Core/PatientProfile/~issues">Simplifier issue log for this profile</a>.</p>
</blockquote>
</div>


This Patient profile sets minimum expectations for the Patient resource to record, search and fetch demographics and other administrative information about an individual receiving care or other health-related services.

Since not all concepts are included within the base FHIR Patient resource, this profile defines localization concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of 0, which means that they may be missing from a resource when it is exchanged between systems.

In this Canadian Baseline Patient Profile all elements are optional, i.e., there is no element with a minimum cardinality of 1. However, some optional elements (e.g., identifier) have required components that MUST be present if that optional element is provided.

### Data Absent Reason
In situations where the minimum cardinality of an element or attribute is 1 and information is missing and the Responder knows the precise reason for the absence of data, Responders SHALL send the reason for the missing information using values (such as [NullFlavor](https://www.hl7.org/fhir/extension-iso21090-nullflavor.html)) from the value set where they exist or using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.

## Usage Note
Some of the typical use cases where the Patient profile may be used:

* Enterprise-wide information systems that manage patient registration and services ordering
* Local or cross-jurisdictional systems to query information about patients whose demographics data match data provided in the query parameters
* Synchronization of patient information between multiple ADT systems employed by healthcare enterprises

This profile includes an invariant that enforces that a family.name, given.name, or both be present. This is intended to enforce minimum constraints while allowing for cases where the patient may only have one name.
* Some jurisdictions with more rigid cardinality constraints on both family and given may be handling this today by populating the name of a patient into both fields
* Other jurisdictions may allow the population of either family or given
