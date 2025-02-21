# CA Baseline Practitioner Profile for Registries

<div class="stu-note">
<p>While the CA Baseline relies on the existing extensible value set for identifier.type (from the base FHIR Spec) - some Canadian Jurisdictions have published the values that are extensions on that value set. Review of the <a href="https://simplifier.net/provincialproviderregistry-ontario-r4/ppr-organization-identifier-type-duplicate-2">Ontario Provider Registry Identifier.Type ValueSet</a> identified that the following Ontario specific identifier type codes may be used from the <http://ehealthontario.ca/fhir/CodeSystem/ppr-organization-identifier-type> code system: LHIN (Local Health Integration Network), MNI (Master Numbering Index), LSS (Lab Services Licensing System, CNUM (Corporate Number), BNUM (Business Number), AC (Accreditation Number).</p>
<p>The CA Baseline is asking other jurisdictions or implementers to provide feedback if other values are being used for identifier.type not already discussed in this profile.</p>
<p>For Practitioner.qualification, slicing has been maintained to demonstrate that there are some registries supporting hybridized registry/eReferral use cases that utilize a different code system (HealthcareProviderRoleType) from the QualifiedRoleType that was incorporated by many HL7 V3 implementations. This separation based on use case and age of implementation remains a challenge in the Canadian ecosystem, and has persisted in part due to the challenges some registry assets face in consuming the longer character lengths present in the SNOMED CT CA HealthcareProviderRoleType value set. Until practices are more standardized or a resolution is in place regarding the disparate use of these two code systems, implementers are cautioned that the CA Baseline's use of these code systems and value sets still may change.</p>
<p>The CA Baseline is asking implementers to provide feedback on the value sets and code systems they are expecting to utilize as they transition to FHIR.</p>
<p>Feedback can be provided through the <a href="https://simplifier.net/CanadianFHIRBaselineProfilesCA-Core/ObservationProfileLaboratory/~issues">Simplifier issue log for this profile</a>.</p>
</div>

This Practitioner profile sets minimum expectations for the Practitioner resource to record, search and fetch demographics and other administrative information about a person who is directly or indirectly involved in the provisioning of healthcare.

This profile further constrains the general purpose Practitioner profile and is intended to be used by Provider or Healthcare Directory systems.

## Differences from US Core

**Note:** This profile was generated from [HL7 StructureDefinition](https://www.hl7.org/fhir/practitioner.profile.json) on 2020-02-19 and constrained during a review of US Core against Canadian sources.

## Mandatory Data Elements

All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of 0, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* a identifier
* a practitioner name

In addition to that, some optional elements (e.g., _Practitioner.qualification_) have required components that MUST be present if that optional element is provided.

### Data Absent Reason

In situations where the minimum cardinality of an element or attribute is 1 and information is missing and the Responder knows the precise reason for the absence of data, Responders SHALL send the reason for the missing information using values (such as [NullFlavor](https://www.hl7.org/fhir/extension-iso21090-nullflavor.html)) from the value set where they exist or using the [DataAbsentReason](http://hl7.org/fhir/StructureDefinition/data-absent-reason) extension.

## Must Support Data Elements

Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/HL7-Canada/ca-baseline/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the Practitioner profile to aid record matching in databases with many pediatric records.

**Must Support elements:**

* an identifier
* a practitioner name
* contact detail (e.g. a telephone number or an email address)
* a birth date

## Extensions

### Deceased Extension

This Practitioner profile contains optional [[[Extension: Individual is deceased flag or date]]] to indicate if a practitioner is deceased or not.

This extension was previously labeled as a modifier extension (because of its potential impacts on clinical processes if the practitioner is marked deceased), but was removed after further discussion on the nuances of making something a modifierExtension vs regular extension if it was expected to be picked up by registry implementation guides that collect deceased practitioner information but may or may not use it in ways that would align to HL7 FHIR R4 [definition](https://www.hl7.org/fhir/R4/backboneelement-definitions.html#BackboneElement.modifierExtension) and expectations for modifierExtension.

Implementers should recognize that the determination of whether this should be considered a modifierExtension is ongoing. Since Modifier Extensions should have extreme caution in their application and are further nuanced by the use cases in the implementing registry systems, this extension has been shifted back to a regular extension to align to use in existing implementations. Implementers who are considering using this extension in their guidance might consider applying a Must Support flag on the extension, but those treating wanting to re-create it as a modifier extension are required to review the [FHIR Guidance on Modifier Extensions])(https://www.hl7.org/fhir/R4/extensibility.html#modifierExtension) before including this extension in their profile.  Implementers should also be aware of the Practitioner.deceased[x] R5 concept and that the CA Baseline is monitoring changes in the element to determine if the approach to this extension requires a shift.

## Usage Note

This Practitioner profile is intended to provide a foundation for a central or distributed Provider or Healthcare Directory. Additional work flow components and elements may be required for a particular implementation.
