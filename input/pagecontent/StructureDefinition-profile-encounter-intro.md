# CA Baseline Encounter Profile
This profile sets minimum expectations for the Encounter resource to represent various observations if no other, more specific profile is applicable.

This Encounter profile represents an interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient, or to communicate information on a visit-specific basis.

This profile defines localization concepts for use in the Canadian context.

## Mandatory Data Elements
All elements or attributes within the FHIR specification have cardinality as part of their definition - a minimum number of required appearances and a maximum number of allowable appearances.

Most elements in the FHIR specification have a minimum cardinality of 0, so most elements are not required and subsequently they may be missing from a resource when it is exchanged between systems.

**Required elements in the Encounter profile:**
* state of the encounter (Encounter.status)
* classification of the encounter (Encounter.class)
* subject of the encounter (Encounter.subject)

## Must Support Data Elements
Some elements are marked as Must Support. This means that implementations generating, receiving, or otherwise using resources with Must Support elements SHALL provide support for those elements in some meaningful way (see [Must Support](https://build.fhir.org/ig/HL7-Canada/ca-baseline/general-guidance.html#cardinality-and-mustsupport-definitions) definition).

The following elements are marked as Must Support in the Encounter profile:

**Must Support elements:**
* identifier
* state of the encounter (Encounter.status)
* classification of the encounter (Encounter.class)
* reference to a subject (Encounter.subject)
* responsible providers (Encounter.participant)
* reasons (Encounter.reasonCode)
* diagnosis relevant to the encounter (Encounter.diagnosis)
* diagnosis rank
* admission details (Encounter.hospitalization)

## Usage Note
It is anticipated that many systems only need the current information of the encounter and therefore the Encounter resource represents the most recent information.

Systems that need to track historical information about the encounter should be able to do that by increasing complexity of the Encounter resource instance.
