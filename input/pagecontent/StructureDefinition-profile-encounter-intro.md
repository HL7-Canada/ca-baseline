# CA Baseline Encounter Profile
This profile sets minimum expectations for the Encounter resource to represent various observations if no other, more specific profile is applicable.

This Encounter profile represents an interaction between a patient and healthcare provider(s) for the purpose of providing healthcare service(s) or assessing the health status of a patient, or to communicate information on a visit-specific basis.

This profile defines localization concepts for use in the Canadian context.

## Mandatory Data Elements
{% include mandatoryguidance.xml %}


## Usage Note
It is anticipated that many systems only need the current information of the encounter and therefore the Encounter resource represents the most recent information.

Systems that need to track historical information about the encounter should be able to do that by increasing complexity of the Encounter resource instance.
