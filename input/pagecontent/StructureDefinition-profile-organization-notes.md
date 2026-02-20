## Identifiers

Currently, there is no consensus or requirement for pan-Canadian method to identify an organization using a business identifier. Organization.identifier will remain unsliced until a requirement or rationale is put forth that supports the need to have unique constraints determined by the business identifier.

## Service Language

The Organization MAY have an [[[ExtensionServiceLanguage]]] extension. This extension is to identify languages that that services are provided in this particular organization.

## Address

The Organization profile is provided for use in a Canadian context where some constraint on content is desirable to guarantee the quality of the Canadian address whilst still supporting other type of address (e.g., other countries or UNstructured addresses).

### Canadian postal code

If an address in the Organization resource instance represents Canadian address, it SHOULD follow Canadian postal code format.

The Canadian Postal Code SHOULD be a six-character uniformly structured uppercase alphanumeric code in the form of "ANA NAN", where "A" represents an alphabetic character and "N" represents a numeric character, with one space between the first three and the last three characters.

A hyphen SHOULD NOT be used (example of UNacceptable format: T0L-1K0).

### Preferred

The Organization.address MAY have a [Preferred](http://hl7.org/fhir/StructureDefinition/iso21090-preferred) extension. This is the FHIR standard defined extension used as a flag denoting whether parent address item is preferred.
