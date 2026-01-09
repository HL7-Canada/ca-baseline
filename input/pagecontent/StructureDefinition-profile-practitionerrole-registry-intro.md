# CA Baseline PractitionerRole Profile
This PractitionerRole profile sets minimum expectations for the PractitionerRole resource to record, search and fetch the recording of the location and types of services that Practitioner is able to provide for an organization.

This profile defines localization concepts for use in an Canadian context.

## Differences from US Core
This analysis is not applicable as this profile is a specialization of PractitionerRole for registry profiles and there is no equivalent in US Core R4 Implementation Guide, See the general PractitionerRole profile for differences.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* reference to a practitioner

In addition to that, some optional elements (e.g., PractitionerRole.telecom, identifier data type) have required components that MUST be present if that optional element is provided.

### Data Absent Reason
In situations where the minimum cardinality of an element or attribute is **1** and information is missing and the Responder knows the precise reason for the absence of data, Responders SHALL send the reason for the missing information using values (such as [NullFlavor](https://www.hl7.org/fhir/extension-iso21090-nullflavor.html)) from the value set where they exist or using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.


## Best Practices/"Should" Support
**identifier**: It is recommended to have an identifier associated with PractitionerRole to assist in searches, however not every implementation (especially legacy implementations that combined both concepts of practitioner & practitionerRole) will include an identifier practitioner role. Given the scope and principles of the CA Baseline, the cardinality on this element was relaxed back to its base cardinality after receiving community feedback from FHIR Iguides that could not support the expectation in their existing implementation(s).

## Invariants
The invariant necessitating either code or specialty be present was removed after review against Canadian FHIR rpracititoner registry implementations identified challenges with some legacy systems (registry and otherwise) that have cpmmon use cases for PractitionerRole that do not include specialty or code.


## Extensions
**ext-rolestatus**: This PractitionerRole profile contains optional [RoleStatus]( https://build.fhir.org/ig/HL7-Canada/ca-baseline/extension-ext-rolestatus.html) [modifier extension](https://www.hl7.org/fhir/extensibility.html#modifierExtension) to indicate the possible states of the Role as defined by the [HL7v3 Role]( https://www.hl7.org/fhir/v3/RoleStatus/cs.html) class state machine.

This extension is labeled as modifier because the status code may provide additional knowledge about the PractitionerRole resource that modifies its meaning or interpretation.

**ext-statusreason**: In conjunction to the RoleStatus extension, this PractitionerRole profile includes an optional [StatusReason]( https://build.fhir.org/ig/HL7-Canada/ca-baseline/extension-ext-statusreason.html) extension to provides a textual description for the status.

Note: Role status effective from/to dates go to _PractitionerRole.period_ element.

## Usage Note
This PractitionerRole profile is intended to provide a foundation for a central or distributed Provider or Healthcare Directory.
Additional work flow components and elements may be required for a particular implementation.
