<!--- Text entered into this file will appear at the bottom of the profiles page after the Formal Views of the profile content. -->
## Identifiers
Multiple individual healthcare identifiers may be provided in Patient.identifier element.

However, to support particular types of federal patient and person health numbers used by all jurisdictions across Canada following optional types are defined to uniquely identifying patients:
* Canadian Passport Number
* Jurisdictional Person Identification
* Jurisdictional Health Number

### Canadian Passport Number (PPN)
A unique number assigned to the document affirming that a person is a citizen of Canada.

URI to use with this identifier type: https://fhir.infoway-inforoute.ca/NamingSystem/ca-passport-number

**Example:**
```json
{
  "type": {
    "coding": [
      {
        "system": "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code": "PPN"
      }
    ]
  },
  "system": "https://fhir.infoway-inforoute.ca/NamingSystem/ca-passport-number",
  "value": "AB123456",
  "period": {
    "start": "2005-05-11",
    "end": "2015-05-11"
  }
}
```

### Jurisdictional Patient Identifier Number (JPID)
This patient identifier type identifies a number issued in Canada to administer various government programs.

URIs used with this identifier type:
* Canada, Social Insurance Number (SIN) - https://fhir.infoway-inforoute.ca/NamingSystem/ca-social-insurance-number
* Canada Permanent Resident Card Number - https://fhir.infoway-inforoute.ca/NamingSystem/ca-permanent-resident-card-number
* Canada First Nation Indian registry number (band ID) - https://fhir.infoway-inforoute.ca/NamingSystem/ca-federal-firstnation-band-id
* Indigenous and Northern Affairs Canada health card number - https://fhir.infoway-inforoute.ca/NamingSystem/ca-indigenous-northern-affairs-number
* Interim Federal Health Program identifier - https://fhir.infoway-inforoute.ca/NamingSystem/ca-interim-federal-health-id

**Example:**
```json
{
  "type": {
    "coding": [
      {
        "system": "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code": "JPID"
      }
    ]
  },
  "system": "https://fhir.infoway-inforoute.ca/NamingSystem/ca-social-insurance-number",
  "value": "923456789"
  }
}
```

### Jurisdictional Health Number (JHN)
Following URIs are registered to identify health card numbers for provinces and territories:
* Alberta - https://fhir.infoway-inforoute.ca/NamingSystem/ca-ab-patient-healthcare-id
* British Columbia - https://fhir.infoway-inforoute.ca/NamingSystem/ca-bc-patient-healthcare-id
* Manitoba - https://fhir.infoway-inforoute.ca/NamingSystem/ca-mb-patient-healthcare-id
* New Brunswick - https://fhir.infoway-inforoute.ca/NamingSystem/ca-nb-patient-healthcare-id
* Newfoundland and Labrador - https://fhir.infoway-inforoute.ca/NamingSystem/ca-nl-patient-healthcare-id
* Northwest Terrirories - https://fhir.infoway-inforoute.ca/NamingSystem/ca-nt-patient-healthcare-id
* Nova Scotia - https://fhir.infoway-inforoute.ca/NamingSystem/ca-ns-patient-healthcare-id
* Nunavut - https://fhir.infoway-inforoute.ca/NamingSystem/ca-nu-patient-healthcare-id
* Ontario - https://fhir.infoway-inforoute.ca/NamingSystem/ca-on-patient-hcn
* Prince Edward Island - https://fhir.infoway-inforoute.ca/NamingSystem/ca-pe-patient-healthcare-id
* Quebec - https://fhir.infoway-inforoute.ca/NamingSystem/ca-qc-patient-healthcare-id
* Saskatchewan - https://fhir.infoway-inforoute.ca/NamingSystem/ca-sk-patient-healthcare-id
* Yukon - https://fhir.infoway-inforoute.ca/NamingSystem/ca-yt-patient-healthcare-id

Following identifier types identify health card numbers issued in Canada to let a patient to be recognized for services and stay connected to related support programs:
* Canada Veteran's Affairs health card number - https://fhir.infoway-inforoute.ca/NamingSystem/ca-veterans-affairs-health-id
* Canada Correctional Service health card number - https://fhir.infoway-inforoute.ca/NamingSystem/ca-correctional-service-health-id
* Canada Royal Canadian Mounted Police (RCMP) health card number - https://fhir.infoway-inforoute.ca/NamingSystem/ca-royal-mounted-police-health-id
* Canada Armed Forces health card number - https://fhir.infoway-inforoute.ca/NamingSystem/ca-armed-forces-health-id

The full list of identifiers can be found on [Canadian URI Registry](https://simplifier.net/canadianuriregistry/~resources?category=NamingSystem). Canada Health Infoway provides Canadian URI Registry [search tool](https://fhir.infoway-inforoute.ca/nssearch) to simplify search.

**Version Code**

The [Version Code](https://build.fhir.org/ig/scratch-fhir-profiles/ca-baseline/extension-ext-identifierversion.html) extension is added to indicate the currency/validity of an identifier.

The rational is that the version code is current captured separately from the JHN because, in Ontario at least, the JHN is a stable identifier whereas the version code changes over time.
- The working assumption is that it is useful to have this stable identifier but not all of the Ontario specs reviewed stored it as a separate field.  In one case, it appears to be an Patient.identifier.coding.value instead of the identifier ...
- Example JHN and Patient Information from [Ontario Health Care Validation Reference Manual](http://www.health.gov.on.ca/english/providers/pub/ohip/ohipvalid_manual/ohipvalid_manual.pdf)
- Question: would specific examples like this be helpful to illustrate Canadian requirements?

**Example:**
```json
{
  "type": {
    "coding": [
      {
        "system": "http://terminology.hl7.org/CodeSystem/v2-0203",
        "code": "JHN"
      }
    ]
  },
  "system": "https://fhir.infoway-inforoute.ca/NamingSystem/ca-armed-forces-health-id",
  "value": "A98765439"
  }
}
```



## Patient Gender and Sex
Many systems and organizations only provide a single attribute to represent all aspects of a patient's gender and sex with a single value. However, there are many considerations around sex and gender documentation and interoperability.

The FHIR Specification provides [guidance](https://www.hl7.org/fhir/patient.html#gender) and background for representing patient gender.

In addition to that Canadian Patient profile defines following extensions:
* **Gender Identity** - an indication from the patient about what gender they consider themselves to be.
* **Sex assigned at Birth** - the sex assigned at birth, as documented on the birth registration.
* **Preferred Pronoun** - an indication from the patient about what pronoun to use in correspondence.

**!! TO BE COMPLETED !!**

## Telecom
A Patient may have multiple ways to be contacted with different uses or applicable periods. This Patient profile allows multiple contact points (e.g. a telephone number or an email address) by which the individual may be contacted.

To indicate the preferred way to contact use Patient.telecom.rank attribute (i.e., the [ContactPoint.rank](https://www.hl7.org/fhir/datatypes.html#contactpoint) component) that specifies a preferred order in which to use a set of contacts. ContactPoints with lower rank values are more preferred than those with higher rank values.

## Address
The Patient profile is provided for use in a Canadian context where some constraint on content is desirable to guarantee the quality of the Canadian address whilst still supporting other type of address (e.g., other countries or UNstructured addresses).

### Canadian postal code
If an address in the Patient resource instance represents Canadian address, it SHOULD follow Canadian postal code format.

The Canadian Postal Code SHOULD be a six-character uniformly structured uppercase alphanumeric code in the form of "ANA NAN", where "A" represents an alphabetic character and "N" represents a numeric character, with one space between the first three and the last three characters.

A hyphen SHOULD NOT be used (example of UNacceptable format: T0L-1K0).

### Preferred
The Patient.address MAY have a [Preferred](http://hl7.org/fhir/StructureDefinition/iso21090-preferred) extension. This is the FHIR standard defined extension used as a flag denoting whether parent address item is preferred.

### No Fixed Address
The Patient.address MAY have a [No Fixed Address](https://build.fhir.org/ig/scratch-fhir-profiles/ca-baseline/extension-ext-nofixedaddress.html) extension. This extension is to indicate that there is an assertion that there is no fixed address (e.g., homeless).

## Marital Status
The binding for the Patient.maritalStatus element is [extensible](https://www.hl7.org/fhir/terminologies.html#extensible) meaning that to be conformant, codes in this element SHALL be from the specified value set if any of the codes within the value set can apply to the concept being communicated.

Systems can send additional codes (Stats Canada, SNOMED CT, etc.) but can only do that if they also send the relevant HL7-assigned codes.
