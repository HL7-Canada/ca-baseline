# CA Baseline Practitioner Profile
This Practitioner profile sets minimum expectations for the Practitioner resource to record, search and fetch demographics and other administrative information about a person who is directly or indirectly involved in the provisioning of healthcare.

This profile defines localization concepts for use in an Canadian context.

## Differences from US Core
**Note:** This profile was generated from [HL7 Practitioner StructureDefinition](http://hl7.org/fhir/R4/practitioner.html) on 2020-02-19 and constrained during a review of US Core and a review against Canadian sources.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

In this Canadian Baseline Practitioner Profile all elements are optional, i.e., there is no element with a minimum cardinality of **1**. However, some optional elements (e.g., identifier) have required components that MUST be present if that optional element is provided.

### Data Absent Reason
In situations where the minimum cardinality of an element or attribute is **1** and information is missing and the Responder knows the precise reason for the absence of data, Responders SHALL send the reason for the missing information using values (such as [NullFlavor](https://www.hl7.org/fhir/extension-iso21090-nullflavor.html)) from the value set where they exist or using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.


## Usage Note
This Practitioner profile is intended for general use, e.g. to be included into a Bundle along with the Patient resource (Patient.generalPractitioner).
