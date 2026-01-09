# CA Baseline PractitionerRole Profile
This PractitionerRole profile sets minimum expectations for the PractitionerRole resource to record, search and fetch the recording of the location and types of services that Practitioner is able to provide for an organization.

This profile defines localization concepts for use in an Canadian context.

## Differences from US Core
**Note:** This profile was generated from [HL7 PractitionerRole StructureDefinition](http://hl7.org/fhir/R4/practitionerrole.html) and constrained during a review of US Core R4 equivalent profile(s) and a review against Canadian sources.

The following differences are noted from the [US Core R4 PractitionerRole Profile](hl7.org/fhir/us/core/STU4/StructureDefinition-us-core-practitionerrole.html):
* MS Differences: US Core R4 PractitionerRole profile includes additional MS constraints on identifier, organization, code, location, telecom.system, telecom.value, and endpoint.
* Cardinality Differences: None
* Terminology Differences: US Core binds PractitionerRole.code to their National Uniform Claim Committet (NUCC) Taxonomy, and binds PractitionerRole.specialty to their Healthcare Provider Taxonomy valueset. Both are expected to be realm specific.
* Invariant Differences: US Core R4 PractitionerRole profile includes an additional invariant necessitating a reference to practitioner, org, healthcareService, or location be present

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

In this Canadian Baseline PractitionerRole Profile all elements are optional, i.e., there is no element with a minimum cardinality of **1**. However, some optional elements (e.g., identifier, telecom) have required components that MUST be present if that optional element is provided.

### Data Absent Reason
In situations where the minimum cardinality of an element or attribute is **1** and information is missing and the Responder knows the precise reason for the absence of data, Responders SHALL send the reason for the missing information using values (such as [NullFlavor](https://www.hl7.org/fhir/extension-iso21090-nullflavor.html)) from the value set where they exist or using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.

## Best Practices/"Should" Support
**identifier**: It is recommended to have an identifier associated with PractitionerRole to assist in searches, however not every implementation (especially legacy implementations that combined both concepts of practitioner & practitionerRole) will include an identifier practitioner role. Given the scope and principles of the CA Baseline, the cardinality on this element was relaxed back to its base cardinality after receiving community feedback from FHIR IGuides that could not support the expectation in their existing implementation(s).

## Invariants
The invariant necessitating either code or specialty be present was removed after review against Canadian FHIR rpracititoner registry implementations identified challenges with some legacy systems (registry and otherwise) that have cpmmon use cases for PractitionerRole that do not include specialty or code.

## Usage Note
This PractitionerRole profile is intended for general use, e.g. to be included into a Bundle along with the Practitioner resource.
