## Identifiers
Multiple types of provider identifiers may be used in Practitioner.identifier element in the Canadian context:
* Provincial health plan provider/ Billing number
* License Number
* Medical Doctor Number

Implementers may use other identifiers to capture in a more specific way such as internal provider number, jurisdictions providing credentials.
The full list of possible identifier types is in [Canadian URI Registry](https://simplifier.net/canadianuriregistry/~resources?category=NamingSystem)

In some cases, the same license number can be used as the provider identifier and provider's qualification identifier.

## Telecom
A provider may have multiple ways to be contacted with different uses or applicable periods. This Practitioner profile allows multiple contact points (e.g. a telephone number or an email address) by which the individual may be contacted.

To indicate the preferred way to contact use Practitioner.telecom.rank attribute (i.e., the [ContactPoint.rank](https://www.hl7.org/fhir/datatypes.html#contactpoint) component) that specifies a preferred order in which to use a set of contacts. ContactPoints with lower rank values are more preferred than those with higher rank values.

## Address
The Practitioner profile is provided for use in a Canadian context where some constraint on content is desirable to guarantee the quality of the Canadian address whilst still supporting other type of address (e.g., other countries or unstructured addresses).

### Canadian postal code
If an address in the Practitioner resource instance represents Canadian address, it SHOULD follow Canadian postal code format.

The Canadian Postal Code SHOULD be a six-character uniformly structured uppercase alphanumeric code in the form of "ANA NAN", where "A" represents an alphabetic character and "N" represents a numeric character, with one space between the first three and the last three characters.

A hyphen SHOULD NOT be used (example of unacceptable format: T0L-1K0).

### Preferred
The Practitioner.address MAY have a [Preferred](http://hl7.org/fhir/StructureDefinition/iso21090-preferred) extension. This is the FHIR standard defined extension used as a flag denoting whether parent address item is preferred.

### Qualifications

This profile recommends to use Canadian [QualifiedRoleType](https://tgateway.infoway-inforoute.ca/singlesubset.html?id=2.16.840.1.113883.2.20.3.48) value set as the coded representation of the provider's qualification.
This value set lists codes for the degree or educational rank that the credential specifies. It may also apply to an Expertise type.

The binding strength for the Practitioner.qualification.code element is [Preferred](https://www.hl7.org/fhir/terminologies.html#preferred) meaning that implementers are encouraged to draw codes from the specified code system for interoperability purposes but are not required to do so to be considered conformant.

Example:
```
"code": {
  "coding": [
    {
      "system": "https://fhir.infoway-inforoute.ca/CodeSystem/scpqual",
      "code": "BSC",
      "display": "Bachelor of Science Degree"
    }
  ],
  "text": "Bachelor of Science Degree"
}
```
