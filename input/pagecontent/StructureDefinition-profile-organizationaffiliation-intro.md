<!--- Text entered into this file will appear at the top of the profiles page before the Formal Views of the profile content. -->

This profile was generated from [HL7 StructureDefinition](https://www.hl7.org/fhir/organizationaffiliation.profile.json) on 2019-03-28 and constrained during a review of US Core against Canadian sources.

**Note:** This profile has been added to meet requirements met by [ppr-ext-location-affiliation](https://simplifier.net/ProvincialProviderRe/location-affiliation/~json) extension used in the ON PPR guide.

**Intended use:**
- Resource Use
  - a Location is place
  - an Organization is a group of people
  - an Organization may have one or more location
- ppr-ext-location-affiliation was used to add an element to a ***Location*** used identify an affiliated organization, including:
  - .type ***of affiliation*** [ppr-provider-role-affiliation-type](https://simplifier.net/provincialproviderre/ppr-providerroleaffiliationtype)
  - .period ***of affiliation***
  - .with ***affiliated Organization***
- OrganizationAffiliation associates two Organizations and allows the location of the ParticipatingOrganization to be specified where:
  - OrganizationAffiliation.organization points to ***affiliated organization*** above
  - OrganizationAffiliation.participationOrganization points to the ***Organization*** that performs a role (Location.managingOrganization)
  - OrganizationAffiliation.code specifies the ***role*** the ***participatingOrganization*** plays (similar to Type above)
  - OrganizationAffiliation.location points to the ***Location*** where the role is performed
