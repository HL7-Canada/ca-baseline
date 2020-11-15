## Code
The _Procedure.code_ element is used to specify a procedure that is performed. 

The _Procedure.code_ element is [CodeableConcept](https://www.hl7.org/fhir/datatypes.html#codeableconcept) data type meaning that more than one [Coding](https://www.hl7.org/fhir/datatypes.html#codesystem) sub-elements can be present.
One of these Coding sub-elements MAY use [InterventionCodeSubsetOperatingRoomProcedure]( https://tgateway.infoway-inforoute.ca/vs/interventioncodesubsetoperatingroomprocedure) value set from Canada Health Infoway.

Use text if the exact nature of the procedure cannot be coded (e.g. "Laparoscopic Appendectomy").
