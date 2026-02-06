# CA Core DiagnosticReport (Laboratory Results) Profile
This profile sets minimum expectations for the DiagnosticReport resource to record, search, and fetch laboratory results associated with a patient. It identifies which core elements, constraints and value sets SHALL be present in the resource instance when using this profile.

This profile defines core localisation concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* status of the diagnostic report
* code that describes the diagnostic report

## Usage Note

The following are example usage scenarios for the DiagnosticReport profile.

* Query for lab reports belonging to a Patient
* Record or update a lab report for a specific Patient
