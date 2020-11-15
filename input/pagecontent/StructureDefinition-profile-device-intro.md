<!--- Text entered into this file will appear at the top of the profiles page before the Formal Views of the profile content. -->

This profile was generated from [HL7 StructureDefinition](https://www.hl7.org/fhir/device.profile.json) on 2019-03-28 and constrained during a review of US Core against Canadian sources.

**Note:**
- USCoreR4 appears to use both
  - a Universal Device Identifier (barcode) provided by one of multiple entities (e.g. [GS1 GDSN](https://www.gs1.org/standards/gdsn))
  - Device Types from SNOMED CT
- Canadian work appears to use both:
  - codes from Canadian regulators (e.g. [Health Canada Device NTP](https://tgateway.infoway-inforoute.ca/hc.html?id=2.16.840.1.113883.2.20.6.1.DeviceNTP) or [OPINIONS](http://www.atlanticpharmaceutical.ca)
  - Device Types from SNOMED CT
- [GS1 Canada is active in the Medical Device space](https://www.gs1ca.org/CHPR2011/) whereas Infoway's Device NTP valueSet shows only a couple sample codes **<< what direction is this headed in?**

Key differences from [USCoreR4 Device](https://build.fhir.org/ig/HL7/US-Core-R4/StructureDefinition-us-core-device.html):
- included more udiCarrier elements for visibility
- changed reference to profile-patient
