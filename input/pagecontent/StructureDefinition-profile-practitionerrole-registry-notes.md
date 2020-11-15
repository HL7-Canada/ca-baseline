## Identifiers
Multiple types of provider identifiers may be used in PractitionerRole.identifier element in the Canadian context:
* Provincial health plan provider/ Billing number
* Licence Number
* Medical Doctor Number

Implementers may use other identifiers to capture in a more specific way such as internal provider number, jurisdictions providing credentials.
The full list of possible identifier types is in [Canadian URI Registry](https://simplifier.net/canadianuriregistry/~resources?category=NamingSystem)

In some cases, the same license number can be used as the provider identifier and provider's qualification identifier.

## Telecom
A provider may have multiple ways to be contacted with different uses or applicable periods. This PractitionerRole profile allows multiple contact points (e.g. a telephone number or an email address) by which the individual may be contacted.

To indicate the preferred way to contact use Practitioner.telecom.rank attribute (i.e., the [ContactPoint.rank](https://www.hl7.org/fhir/datatypes.html#contactpoint) component) that specifies a preferred order in which to use a set of contacts. ContactPoints with lower rank values are more preferred than those with higher rank values.

### Role
Roles which this practitioner is authorized to perform for the organization are defined by Canadian [HealthcareProviderRoleType](https://tgateway.infoway-inforoute.ca/singlesubset.html?id=2.16.840.1.113883.2.20.3.48&versionid=20190813) value set as the coded representation of the provider's credentials.
Credential defines a role type that is used to categorize an entity that delivers health care in an expected and professional manner to an entity in need of health care services. 

The binding strength for the _PractitionerRole.code_ element is [Preferred](https://www.hl7.org/fhir/terminologies.html#preferred) meaning that implementers are encouraged to draw codes from the specified code system for interoperability purposes but are not required to do so to be considered conformant. 

### Specialty
Specific specialty of the practitioner defines the clinical, medical, surgical or other healthcare-related service specialty of a practitioner who interacts, treats or provides such services to or for a patient.
This profile recommends to use Canadian [PractitionerSpecialty](https://tgateway.infoway-inforoute.ca/singlesubset.html?id=2.16.840.1.113883.3.239.12.38) value set for speciality codes.

The binding strength for the _PractitionerRole.speciality_ element is [Preferred](https://www.hl7.org/fhir/terminologies.html#preferred) meaning that implementers are encouraged to draw codes from the specified code system for interoperability purposes but are not required to do so to be considered conformant. 
