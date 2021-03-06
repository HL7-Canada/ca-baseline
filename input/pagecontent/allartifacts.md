This implementation guide defines a number of FHIR Profiles, ValueSets and CodeSets for Canadian Use and uses others from the base FHIR Specification directly without modification.

### <a href="artifacts.html">Canadian Artifacts</a>
### <a href="vitalsigns-profiles.html">Vital Signs Profiles</a>

Each profile defines the minimum mandatory elements, extensions and terminology requirements that MUST be present. For each profile, requirements and guidance are given in a simple narrative summary. A formal hierarchical table that presents a logical view of the content in both a differential and snapshot view is also provided along with references to appropriate terminologies and examples.

### Status

The content of this release has not yet been balloted through HL7 Canada but each of the profiles have gone through [various levels of review](developmentprocess.html#review-process) by the Canadian FHIR community.

All artifacts in this specification are assigned a “Maturity Level”, known as FMM (after the well known CMM grades). The FMM level can be used by implementers to judge how advanced - and therefore stable - an artifact is.

| Profile <br> | Profile Maturity <br> Level <br> | Substream <br>Review Status <br> | Due Diligence<br> Review Status <br> |
|---|---|---|---|
| AllergyIntolerance Profile | 0 | Complete | Ontario eReferral, IPS |
| Condition Profile | 0 | Complete | Ontario eReferral, IPS |
| Device Profile (Implantable) | 0 | Partial - Paused until SME available | Not Complete |
| Device Profile (Medical and Non-medical) | 0 | Partial - Paused until SME available | Attempted against IPS profile, pausing until similarly scoped profile available |
| DiagnosticReport Profile | 0 | Complete, 2nd Review Round review will resume after DDR | PHI Access |
| DiagnosticReport for Report and Note Profile | 0 | Complete | Not Complete |
| Document Reference Profile | 0 | Complete | Not Complete |
| Encounter Profile | 0 | Complete | Not Complete |
| Goal Profile | 0 | Complete | Not Complete |
| Immunization Profile | 0 | Complete | DHIR, IPS, PHI Access |
| ImmunizationRecommendation Profile | 0 | Complete | DHIR |
| Location Profile | 0 | Complete | PPR, Ontario eRefferal |
| Medication Profile | 0 | Complete | PrescribeIT, IPS |
| MedicationAdministration Profile | 0 | Complete | Not Complete |
| MedicationDispense Profile | 0 | Complete | PrescribeIT, PHI Access |
| MedicationRequest Profile | 0 | Complete | PrescribeIT |
| MedicationStatement Profile | 0 | Complete | IPS |
| Observation Profile (General) | 0 | Complete | IPS |
| Observation Profile (Laboratory Results) | 0 | Complete, 2nd Review Round will resume after DDR | PHI Access |
| Observation (Tobacco Smoking Status) Profile | 0 | Inital Review Complete | IPS |
| Organization Profile | 0 | Complete | DHIR, PrescribeIT |
| Patient Profile | 0 | Complete | PCR, DHIR, Ontario eReferral |
| Practitioner Profile (General) | 0 | Complete | PPR, DHIR, Ontario eReferral, PrescribeIT |
| Practitioner Profile (Provider Registry) | 0 | Complete | PPR |
| PractitionerRole Profile (General) | 0 | Complete | PPR |
| PractitionerRole Profile (Provider Registry) | 0 | Complete | PPR |
| Procedure Profile | 0 | Complete | IPS |

<!-- Todo: examples, capabilitystatement, TestScenario? -->
