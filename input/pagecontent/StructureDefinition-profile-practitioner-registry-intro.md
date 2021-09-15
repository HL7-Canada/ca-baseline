# CA Baseline Practitioner Profile for Registries
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
	<blockquote class="stu-note">
		<p> While the CA Baseline relies on the existing extensible value set for identifier.type (from the base FHIR Spec) - some Canadian Jurisdictions have published the values that are extensions on that value set. Review of the <a href="https://simplifier.net/provincialproviderregistry-ontario-r4/ppr-organization-identifier-type-duplicate-2">Ontario Provider Registry Identifier.Type ValueSet</a>.identified that the following Ontario specific identifier type codes may be used from the http://ehealthontario.ca/fhir/CodeSystem/ppr-organization-identifier-type code system: LHIN (Local Health Integration Network), MNI (Master Numbering Index), LSS (Lab Services Licensing System, CNUM (Corporate Number), BNUM (Business Number), AC (Accreditation Number).
    <br>
    <br>
    The CA Baseline is asking other jurisdictions or implementers to provide feedback if other values are being used for identifier.type not already discussed in this profile</p>
	</blockquote>
  </div>

This Practitioner profile sets minimum expectations for the Practitioner resource to record, search and fetch demographics and other administrative information about a person who is directly or indirectly involved in the provisioning of healthcare.

This profile further constrains the general purpose Practitioner profile and is intended to be used by Provider or Healthcare Directory systems.

## Differences from US Core
**Note:** This profile was generated from [HL7 StructureDefinition](https://www.hl7.org/fhir/practitioner.profile.json) on 2020-02-19 and constrained during a review of US Core against Canadian sources.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.


Most elements in FHIR specification have a minimum cardinality of 0, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* an identifier
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

## Modifier Extension
This Practitioner profile contains optional [modifier extension](https://www.hl7.org/fhir/extensibility.html#modifierExtension) to indicate if a practitioner is deceased or not.

This extension is labeled as a modifier because once a practitioner is marked as deceased, the clinical processes that the practitioner was involved in may be significantly different.

## Usage Note
This Practitioner profile is intended to provide a foundation for a central or distributed Provider or Healthcare Directory. Additional work flow components and elements may be required for a particular implementation.
