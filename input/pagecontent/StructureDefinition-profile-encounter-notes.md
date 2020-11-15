## Class
The _Encounter.class_ element is to provide the kind of stay that a subject is having. This is different than the _Encounter.type_ that explains what is done to the subject within this encounter.

In other words, the _Encounter.class_ identifies the setting for the encounter (inpatient/outpatient) in which the encounter took place.

Since it is important for interpreting the context of the encounter, for choosing the appropriate business rules to enforce the clinical/management process, this element is required (cardinality 1..1) and marked as Must Support.

The _Encounter.class_ element does NOT identify the priority of the encounter (see _Encounter.priority_). 
Therefore ```Encounter.class = "EMER"``` (Emergency) refers to an encounter happening at a dedicated healthcare service delivery location (e.g., Emergency Department) rather than the priority of the encounter.

## Type
The _Encounter.type_ element is to provide a specific code indicating type of service provided.

This element is bound to [EncounterType]() value set which includes codes from [SNOMED CT](http://www.snomed.org) decending from the 308335008 (Patient encounter procedure (procedure)) concept.

To extract all descendant of the [SNOMED CT](http://www.snomed.org) concept 308335008 use an ECL expression ```<< 308335008```.

```diff
- ISSUE #143: Need to better define the value set for the Encounter.type and explain the difference between Encounter.type and Encounter.serviceType based on use cases. 
- Possible value sets:
- descendant of the SNOMED CT concept 308335008 | Patient encounter procedure (procedure);
- descendant of the SNOMED CT concept 308467007 | Seen in establishment (finding)
- descendant of the SNOMED CT concept 308930007 | Seen by health professional (finding)
```

## Service Type
The _Encounter.serviceType_ element describes the service to be performed during the encounter. 
This element is connected to other resources such as Appointment (Appointment.serviceType), HealthcareService (HealthcareService.type) or Schedule (Schedule.serviceType) 
