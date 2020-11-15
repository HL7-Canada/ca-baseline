### Supported Profiles

CA Baseline adopts the following [Vital Signs profiles from the FHIR Observation resource specification](http://hl7.org/fhir/R4/observation-vitalsigns.html) without modificaton:

* [BMI](http://hl7.org/fhir/R4/bmi.html) - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign body mass index
* [BP](http://hl7.org/fhir/R4/bp.html) - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign blood pressure
* [BodyHeight](http://hl7.org/fhir/R4/bodyheight.html) - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign body height
* [BodyWeight](http://hl7.org/fhir/R4/bodyweight.html) - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign body weight
* [BodyTemp](http://hl7.org/fhir/R4/bodytemp.html) - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign body temperature
* [HeartRate](http://hl7.org/fhir/R4/heartrate.html) - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign heart rate
* [OxygenSat](http://hl7.org/fhir/R4/oxygensat.html) - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign oxygen saturation
* [RespRate](http://hl7.org/fhir/R4/resprate.html) - Defines constraints and extensions on the Observation resource for use in querying and retrieving the vital sign respiratory rate

### Open Issues
**CA Baseline Notes:** It is possible to replace some of Vital Signs profiles with CA Baseline specific. However, what is rational for introducing additional layers of complexity and formality that may be unwelcome, particularly for those systems that do not currently foresee a need to support both FHIR Vital Signs and CA Baseline Vital Signs profiles.

Feedback is welcome.
