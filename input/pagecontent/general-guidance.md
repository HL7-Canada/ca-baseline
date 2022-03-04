This section outlines important definitions and interpretations and requirements common to all  actors used in this guide.
The conformance verbs used are defined in [FHIR Conformance Rules].


### Must Support
Base or baseline specifications are specifications that other implementation guides build on top of. When applying constraints, this guide does so with the understanding that any profiling constraints (must support, cardinality, invariants, slicing, etc.) will be inherited into any profiles that derive from them.

Must support constraints are particularly challenging for baseline specifications because the FHIR Standard has enforced that every implementation guide declares the meaning and expectations for a must support flag in their guide. Much like other derived constraints, a must support flag that is inherited into a derived profile can not have a looser definition from the profile the flag originates from. The definition in the derived profile can keep or tighten the definition for must support.

Therefore, the CA Baseline has developed a lightweight must support definition that does not impede or prescribe what a client or server does with the data, so as not to impede each implementation's ability to tighten and define expectations for use under their own business rules, regulations, policies, etc.

**Must Support Definition:**
Vendors in Canada have the base capability to support the elements, with the expectation that business rules, regulations, etc. can determine what of these elements is used and how.

Given the challenge that comes from inheritance of must support flags into implementation guides that have strict definitions for must support (e.g., must be able to display this value to an end user), the CA Baseline has only applied must support flags on the elements that would be expected to be flagged as must support across the majority of Canadian Implementation Guides.

**Should Support Expectations:**
This specification may also identify elements that are "should support" using usage notes. These are elements that may not reasonably meet the rule above of being in the majority of Canadian Implementation Guide, but that the CA Baseline is encouraging further proliferation of.

### Cardinality and MustSupport Definitions

|  | MustSupport | Cardinality | Query Scenario <br> (Server) | Query Scenario <br> (Client)  | Create / Update Scenario <br> (Client)  | Create / Update Scenario <br> (Server)  |
|---|---|---|---|---|---|---|
| A | No | 0..1, 0..* | MAY send/relay data corresponding to this element (not required) <br> <br> SHOULD NOT send element if the data is not available (not collected or null value) | SHOULD NOT assume this element will be received <sup>1, 2</sup> | MAY send/relay data corresponding to this element (not required) <br> <br> SHOULD NOT send element if the data is not available (not collected or null value) | MAY ignore data received in the element <sup>1</sup>
| B | No | 1..1, 1..* | SHALL send/relay the data element populated with a value <br> <br> MAY use a fixed value or rule to populate element with an appropriate value | SHOULD assume this element will be received and may be a fixed value <sup>1, 2</sup> | SHALL send/relay the data element populated with a value <br> <br> MAY use a fixed value or rule to populate element with an appropriate value | MAY ignore data received in the element <sup>1</sup>
| C | Yes | 0..1, 0..* | SHALL send/relay the data element populated with a value (if available and appropriate) <br> <br> SHOULD NOT send element if the value is null |  SHOULD assume this element will be received if data is available <sup>1, 2</sup> <br> <br> SHOULD assume that a missing data element in response means that a value for that data element was not available<sup>1, 2</sup> | SHALL be capable of sending/relaying the data element to the server <br> <br> SHOULD NOT send element if the value is null | SHALL be capable of receiving/relaying/storing the data for this element <sup>1</sup>
| D | Yes | 1..1, 1..* | SHALL send/relay the data element populated with a value | SHOULD assume a value for this data element will be received <sup>1, 2</sup> | SHALL send/relay the data element populated with a value to the server | SHALL be capable of receiving/relaying/storing the data for this element <sup>1</sup>

<sup>1</sup> Business rules, regulations, policies, additional implementation guides should determine what the server will do with the data it receives (i.e., store, persist, etc.)

<sup>2</sup> Scope of the CA Baseline Profiles does not include prescriptive constraints on what a Client or Server has to do with the data it receives (i.e., ignore, display, store, persist, etc.).*

**Client = Requestor, Server = Responder**

#### Conformance Language:

| Verb | Definition |
|---|---|
| **SHALL** | an absolute requirement for all implementations |
| **SHALL NOT** | an absolute prohibition against inclusion for all implementations |
| **SHOULD / SHOULD NOT** | A best practice or recommendation to be considered by implementers within the context of their particular implementation; there may be valid reasons to ignore an item, but the full implications must be understood and carefully weighed before choosing a different course |
| **MAY** | This is truly optional language for an implementation; can be included or omitted as the implementer decides with no implications |

#### Examples

##### Line C: Patient.birthDate - MustSupport = Yes, Cardinality = 0..1

###### Query Scenario

<br>
<img src="C_Query.png" alt="Create / Update Scenario" width="200"/>
<br>

**Requirement:**

The Server SHALL be able to return a BirthDate if it is known.  (i.e., It must be stored on the server or retrievable in some way.)

(The BirthDate MAY be unknown and therefore not available to send.)

**Process:**

1. Client sends GET request to Server for a Patient (their demographics); included in the request is a query parameter (e.g. Patient’s HCN), so the Server knows which Patient’s info to return
1. Server provides a response which includes the requested Patient’s information
  1. IF the Server has a Birth Date for the Patient, it MUST be included in the response
  1. IF the Patient’s Birth Date is not found on the Server, the Server SHOULD NOT send a null-value Birth Date and instead should remove the Birth Date element entirely from the response
1. Client receives the response from the Server which includes the requested Patient’s information, which includes the Patient’s Birth Date (unless 3b is true)
1. More prescriptive instructions on what exactly the Client needs to be able to DO with the Birth Date element it receives from the Server may be provided in additional, project-specific requirements, but these fall outside the scope of the Must Support flag

###### Create / Update Scenario
<br>
<img src="C_CreateUpdate.png" alt="Create / Update Scenario" width="200"/>
<br>

**Requirement:**

The Client SHALL be able to send a BirthDate if it is known.  (i.e., It must be stored on the client or retrievable in some way.)

The Server SHALL be able to store a BirthDate if it is provided.  (i.e., It must be stored on the server or somewhere where it can be retrieved later.)

(The BirthDate MAY be unknown and therefore not available to send.)


**Process:**

1. Client performs SUBMIT function, and sends a Patient’s information to the Server
  1. IF the Client has a Birth Date for the Patient, it MUST be included in the sent information
  1. IF the Client doesn’t know a Birth Date for the Patient, the Client SHOULD NOT send a null-value Birth Date and instead should remove the Birth Date element entirely from the resource that is being pushed to the server
1. Server MUST have the capacity to receive / support the Birth Date element once it is received from the Client
1. More prescriptive instructions on what exactly the Server needs to be able to DO with the Birth Date element it receives from the Client may be provided in additional, project-specific requirement, but these fall outside the scope of the Must Support flag
