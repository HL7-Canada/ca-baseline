# CA Baseline MedicationDispense Profile
This profile sets minimum expectations for the MedicationDispense resource.
This profile defines localization concepts for use in the Canadian context.

## Mandatory Data Elements
All elements or attributes within the FHIR specification have cardinality as part of their definition - a minimum number of required appearances and a maximum number of allowable appearances.

Most elements in the FHIR specification have a minimum cardinality of 0, so most elements are not required and subsequently they may be missing from a resource when it is exchanged between systems.

**Required elements in the Observation (General Use) profile:**
* status (required in the base specification)
* medication (required in the base specification)
* subject


## Must Support Data Elements
The following elements are marked as Must Support in this profile:

**Must Support elements:**
* status
* medication
* subject
* quantity
* whenPrepared
* dosageInstruction

## CA Core Considerations
The whenHandedOver element was initially profiled as must support and was later relaxed through the Due Diligence Review Process with the goal of not constraining for certain use cases over others. Given the criticality to many clinical/pharmaceutical use cases, it has been identified as an element to consider for additional constraints in the CA Core Profiles which are to be developed in the future under the guidance of a larger collaborative of pan-Canadian governing bodies.
