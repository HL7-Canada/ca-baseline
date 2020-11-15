# CA Baseline Procedure Profile
This profile sets minimum expectations for the Procedure resource to record, search and fetch current or historical procedures performed on or for a patient. It identifies which elements and value sets SHALL be present in the resource when using this profile.

This profile defines localization concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* status specifying the state of the procedure
* code to classify the procedure that is performed
* reference to a subject
* performer of the procedure

## Must Support Data Elements
Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/HL7-Canada/ca-baseline/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the Procedure profile to aid record matching in databases with many pediatric records.

**Must Support elements:**
* status
* code
* reference to a subject
* performed date
* body site

## Usage Note
This Procedure profile is used to provide summary information about the occurrence of current or historical procedures performed on or for a patient, and is not intended to provide real-time snapshots of a procedure as it unfolds.
Examples include surgical procedures, diagnostic procedures, endoscopic procedures, biopsies, counseling, physiotherapy, personal support services, adult day care services, non-emergency transportation, home modification, exercise and so on.
