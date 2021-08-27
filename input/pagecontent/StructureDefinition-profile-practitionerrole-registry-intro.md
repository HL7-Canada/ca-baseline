# CA Baseline PractitionerRole Profile
This PractitionerRole profile sets minimum expectations for the PractitionerRole resource to record, search and fetch the recording of the location and types of services that Practitioner is able to provide for an organization.

This profile defines localization concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* an identifier
* reference to a practitioner

In addition to that, some optional elements (e.g., PractitionerRole.telecom) have required components that MUST be present if that optional element is provided.

### Data Absent Reason
In situations where the minimum cardinality of an element or attribute is **1** and information is missing and the Responder knows the precise reason for the absence of data, Responders SHALL send the reason for the missing information using values (such as [NullFlavor](https://www.hl7.org/fhir/extension-iso21090-nullflavor.html)) from the value set where they exist or using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.

## Must Support Data Elements
Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/HL7-Canada/ca-baseline/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the PractitionerRole profile to aid record matching in databases with many pediatric records.

**Must Support elements:**
* an identifier
* reference to a practitioner
* contact detail (e.g. a telephone number or an email address)
* specialty

## Extensions
This PractitionerRole profile contains optional [RoleStatus]( https://build.fhir.org/ig/HL7-Canada/ca-baseline/extension-ext-rolestatus.html) [modifier extension](https://www.hl7.org/fhir/extensibility.html#modifierExtension) to indicate the possible states of the Role as defined by the [HL7v3 Role]( https://www.hl7.org/fhir/v3/RoleStatus/cs.html) class state machine.

This extension is labeled as modifier because the status code may provide additional knowledge about the PractitionerRole resource that modifies its meaning or interpretation.

In conjunction to the RoleStatus extension, this PractitionerRole profile includes an optional [StatusReason]( https://build.fhir.org/ig/HL7-Canada/ca-baseline/extension-ext-statusreason.html) extension to provides a textual description for the status.

Note: Role status effective from/to dates go to _PractitionerRole.period_ element.

## Usage Note
This PractitionerRole profile is intended to provide a foundation for a central or distributed Provider or Healthcare Directory.
Additional work flow components and elements may be required for a particular implementation.
