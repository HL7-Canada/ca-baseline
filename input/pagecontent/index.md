### Introduction

This implementation guide is provided to support the use of FHIR®© in a Canadian context.

This document is a working specification that is expected to be tested and referenced by FHIR®© system producers and implementation guide authors to enable feedback to improve the content of this guide.

As the output of a National Baseline Initiative, this implementation guide provides basic interoperability expectations for human-patient systems in the Canadian space. The goal of this specification is to expose the implementation guide author community and vendor community to a set of profiles that identify the data elements, code systems and value sets that are commonly present across Canada for a given FHIR resource (e.g., patient, medication, etc.) regardless of use case, jurisdiction or implementation.

The Canadian Baseline Profiles are not expected to be implemented "out-of-the-box". They are intended to be a starting point that more specific profiles (driven by jurisdictional, use-case, and project-specific needs) can build derived profiles from. By exposing a minimal and consistent set of expectations across local and jurisdictional guides, we intend to create a more transparent and uniform landscape for the vendor marketplace to begin aligning to.

Existing Canadian and International implementation guides (e.g., Canadian eReferral, Ontario PPR, US Core, IPS, etc.) were used as an initial frame of reference that the Canadian Baseline profiles further relaxed / constrained / extended to make sense in the Canadian context.

### Status

This guide is a **living document** that includes notes and profiles that continue to evolve as they undergo a working group review process and a Due Dillegence Review against existing Canadian FHIR Implementation Guides before being exposed to the larger FHIR community for further maturation through feedback and testing.

**The profiles are currently undergoing reconciliation after a period of community review through our Due Dillegence Review (DDR) process.**
- Information about the development and review process can be found [here](http://build.fhir.org/ig/HL7-Canada/ca-baseline/branches/master/developmentprocess.html)
  - You can follow along with our progress as a working group on the [Infocentral FHIR Implementation Working Group page](https://infocentral.infoway-inforoute.ca/en/collaboration/wg/fhir-implementations)
- The list of which profiles have undergone DDRs against existing Canadian FHIR Implementation Guides can be found [here](http://build.fhir.org/ig/HL7-Canada/ca-baseline/branches/master/allartifacts.html)
- Proposed and past changes to profiles are tracked in the [Simplifier issue log](https://simplifier.net/cabaseline/~issues) that can be accessed after logging in to Simplifier and navigating to the issues tab of the project or desired profile. The commnunity is encouraged to review the issues and add issues of their own after reading the [review and development process page](http://build.fhir.org/ig/HL7-Canada/ca-baseline/branches/master/developmentprocess.html).
- The [GitHub repository for this CI build be found here](https://github.com/HL7-Canada/ca-baseline).

### Principles

The following principles were applied when creating the profiles:
- *Start with the profiles outlined in the US Core and avoid arbitrary differences* between Canadian and other international implementation guides to:
  - increase the opportunity for Digital Health / mHealth application reuse across North America
  - reduce developer / vendor effort to adapt to Canadian requirements
- *Only impose additional constraints when strictly necessary* making adjustments as they make sense in the Canadian context. Aligning to the CA Baseline should not **prevent** implementors from participating in specific use cases and/or conforming to existing Canadian implementation guides
- *Provide direction* and set minimal expectations on a few common terminologies (e.g., CCDD, PCLOCD, etc.).
- *Focus on what Canadian implementations currently support* not what they "ought to support". Emerging Canadian concepts can be socialized through extensions, examples, and usage notes but should not be constrained by the Baseline as to be prescriptive.
- *Be consistent* and informed by other pan-Canadian standards where possible.


### Base vs. Baseline vs. Core

The international FHIR community is evolving towards further differentiation between the use of Base, Baseline, and Core terminology to categorize implementation guides - readers should be aware that the definitions below may be refined as formal definitions are provided by HL7 International. At the time that this implementation guide was authored, the following patterns were discerned and proposed by the CA FHIR Baseline Community:

**National Base Implementation Guides** (e.g., Australian Base, Germany Base, Netherlands Base) provide awareness of localized concepts but do not apply cardinality constraints or required binding strengths that enforce conformance to those concepts. In rare cases, cardinality constraints may be applied to elements that have been [sliced](https://www.hl7.org/fhir/profiling.html#slicing) to ensure the presence of sub-elements if a particular slice is used (ex: identified coding system). Must support flags are not utilized in Base National Profiles.

**National Baseline Implementation Guides** (e.g., Canadian Baseline) provide awareness of localized concepts and apply minimal cardinality constraints and preferred binding strengths only where appropriate and when expected given national context. In some scenarios, more restrictive constraints may be found on elements that have been [sliced](https://www.hl7.org/fhir/profiling.html#slicing) to support meaningful conformance when standard heterogenous concepts are expected (ex: fixed values for specific systems the slice applies to). Must Support flags are utilized to identify elements that are expected to be supported broadly regardless of use case.

**National Core Implementation Guides** (e.g., US Core) define a set of conformance requirements that enforce alignment to localized concepts through cardinality constraints, must support flags, and required/extensible binding strengths. Conformance to these profiles is tied to regulatory and/or contractual agreements in order to necessitate adoption to these more prescriptive specifications. To date, National "Cores" may or may not be scoped to specific use cases (e.g., Norway Core vs US Core) however they are a reflection of additional requirements that are expected to be included in implementations in a nation or region.

### CA Baseline Profiles

The list of CA Baseline Profiles can be found [**here**](allartifacts.html).

Each profile defines the minimum mandatory elements, extensions and terminology requirements that MUST be present. For each profile, requirements and guidance are given in a simple narrative summary. A formal hierarchical table that presents a logical view of the content in both a differential and snapshot view is also provided along with references to appropriate terminologies and examples.

Guidance, Capability Statements, and other have not yet been reviewed and added.

-----
Contact: [hl7canada@infoway-inforoute.ca](mailto:hl7canada@infoway-inforoute.ca)
