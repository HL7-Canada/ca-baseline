## Identifiers 
Currently, there is no consensus or requirement for pan-Canadian method to identify a location using a business identifier. Location.identifier will remain unsliced until a requirement or rationale is put forth that supports the need to have unique constraints determined by the business identifier.

## Service Language
The Location MAY have a [Service Language]( http://hl7.org/fhir/ca/baseline/StructureDefinition/ext-servicelanguage) extension. This extension is to identify languages that that services are provided in this particular location.

## Address
The Location profile is provided for use in a Canadian context where some constraint on content is desirable to guarantee the quality of the Canadian address whilst still supporting other type of address (e.g., other countries or UNstructured addresses).

### Canadian postal code
If an address in the Location resource instance represents Canadian address, it SHOULD follow Canadian postal code format.

The Canadian Postal Code SHOULD be a six-character uniformly structured uppercase alphanumeric code in the form of "ANA NAN", where "A" represents an alphabetic character and "N" represents a numeric character, with one space between the first three and the last three characters.

A hyphen SHOULD NOT be used (example of UNacceptable format: T0L-1K0).

