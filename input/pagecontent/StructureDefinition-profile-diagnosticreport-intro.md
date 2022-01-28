# CA Core DiagnosticReport (Laboratory Results) Profile
This profile sets minimum expectations for the DiagnosticReport resource to record, search, and fetch laboratory results associated with a patient. It identifies which core elements, constraints and value sets SHALL be present in the resource instance when using this profile.

This profile defines core localisation concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* status of the diagnostic report
* code that classifies the author of the report
* code that describes the diagnostic report
* time when report was created

## Must Support Data Elements
Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/HL7-Canada/ca-baseline/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the Canadian DiagnosticReport profile to aid record matching in databases.

**Must Support elements:**
* code that classifies the author of the report
* code that describes the diagnostic report
* subject of the report
* healthcare event this report is about
* time when report was created
* Observations that are part of this report  

## Usage Note

The following are example usage scenarios for the DiagnosticReport profile.

* Query for lab reports belonging to a Patient
* Record or update a lab report for a specific Patient
