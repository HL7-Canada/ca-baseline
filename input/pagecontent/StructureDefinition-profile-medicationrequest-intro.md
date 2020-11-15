<!--- Text entered into this file will appear at the top of the profiles page before the Formal Views of the profile content. -->

This profile was generated from [HL7 StructureDefinition](https://www.hl7.org/fhir/medicationrequest.profile.json) on 2019-03-28 and constrained during a review of US Core against Canadian sources.

Key differences from [USCoreR4 MedicationRequest](https://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-medicationrequest.html):
- MedicationRequest.medication updated:
  - CodeableConcept binding to ValueSet-prescriptionmedicinalproduct
  - Reference to profile-medication
- MedicationRequest.subject reference updated to profile-patient
- MedicationRequest.requester reference updated to profile-practitioner
