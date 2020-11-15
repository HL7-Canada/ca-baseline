# CA Baseline Observation (General Use) Profile
This profile sets minimum expectations for the Observation resource to represent various observations if no other, more specific profile is applicable. An observation is a measurement or assertion about a subject (person, group, device, location, or another subject).

This profile defines localization concepts for use in the Canadian context.

## Mandatory Data Elements
All elements or attributes within the FHIR specification have cardinality as part of their definition - a minimum number of required appearances and a maximum number of allowable appearances.

Most elements in the FHIR specification have a minimum cardinality of 0, so most elements are not required and subsequently they may be missing from a resource when it is exchanged between systems.

**Required elements in the Observation (General Use) profile:**
* status of the result value (Observation.status)
* type of observation (Observation.code)
* subject of the observation (Observation.subject)

### Data Absent Reason
An Observation without a value, SHALL include a reason why the data is absent unless there are component observations, or references to other Observations that are grouped within it, i.e., unless there are component observations, or references to other Observations that are grouped within it then either ONE of Observation.value OR Observation.dataAbsentReason but NOT both SHALL be present.

## Must Support Data Elements
Some elements are marked as Must Support. This means that implementations generating, receiving, or otherwise using resources with Must Support elements SHALL provide support for those elements in some meaningful way (see Must Support definition).

The following elements are marked as Must Support in the Observation (General Use) profile:

**Must Support elements:**
* category
* code
* reference to a subject (Observation.subject)
* effective data
* value
* dataAbsentReason
* component code
* component value
* component dataAbsentReason

## Usage Note
Observation (General Use) is intended to capture data associated with most observations; it is not intended to capture data in some cases where a more appropriate profile is applicable (see below). Data typically consists of measurements or assertions about a subject. Observation (General Use) can capture data in eclectic use cases as it incorporates multiple categories of observations and datatypes. Observation (General Use) can capture data such as:
* Clinical observations such as clinical finding, diagnosis, disorder
* Demographic information
* Device measurements
* Determinants of health such as housing status, income, family support

Observation (General Use) should not be used if one of the following profiles is applicable:
* Observation (Laboratory Results)
* Observation (Vitals)
