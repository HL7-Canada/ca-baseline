This section outlines the process and approach that governed how the profiles in this implementation guide were developed and matured.

### Background

Work began on the CA Baseline in January 2019 as a workstream under the Infocentral FHIR Implementations Working Group. The work was undertaken by a grassroots community of Canadian implementation guide authors, implementors, standards experts and vendors to address the problem of siloed Canadian FHIR-based integration project siloes that were leading to FHIR concepts (resources) being adopted & profiled differently in different projects, contexts, and jurisdictions (i.e. Canadian provinces & territories).

#### Problem Statement

A lack of an available national set of Baseline FHIR Profiles will result in applications and source systems needing to ‘start from scratch’ for each jurisdiction that has implemented a particular use case differently, straining developments costs and willingness for vendors to implement further in the Canadian market. It is understood that implementations such as mHealth applications (e.g., Apple Health), CDS Hooks, and other SMART on FHIR applications require a minimum level of consistency in FHIR Profile structure definitions across implementations in order to have widespread adoption and efficacy.

#### Intent
The CA Baseline exposes the implementation guide and vendor community to what concepts can be expected to be supported across jurisdictions today.

Implementation Guide Authors:
When implementation guide authors leverage the profiles as a starting point, constraints like "Must Support" flag and cardinality are inherited and preferred value sets are more likely to used in the derived implementation guide.

Through derivation of profiles, concepts that were common across existing implementations become ubiquitous in future implementations.

Vendors:
Published baseline profiles offer vendors a stepping stone to begin aligning their systems to Canadian concepts. While vendors will still need to configure their systems to additional constraints to support specific implementations and use cases, conforming to the Baseline will offer vendors a head start across all projects. Consistency across jurisdictions will also mean reduced time, money, and effort spent on implementations by not having to start over with each jurisdictions.

#### Boundaries
- The objective of the Canadian Baseline is not use case driven.
- Implementors are not expected to build an application purely against the Canadian Baseline Profiles. Rather, they should be building their software against jurisdiction or project-specific Implementation Guides that are derived from the CA Baseline)
- The Canadian Baseline Profiles are not about driving what implementers need to do but rather what Canadian Implementation Guide authors need to do.
- The Canadian Baseline Profiles need to be the set of requirements that all Canadian Implementation Guides are capable of incorporating into their guides

### Roadmap to Interoperability
The Baseline is not a silver bullet to Interoperability in Canada, but it is a critical stepping stone in reducing the siloes and improving the consistency across the Canadian Landscape.

There is appetite in Canada's standards and governance community to establish a Canadian Core with stricter conformance that would be enforceable through contractual agreements and jurisdictional procurement practices.
While the Canadian Baseline will likely evolve into or offset a large portion of this work, a larger governance structure is needed to accomplish this goal.

The Canadian Baseline can begin encouraging consistency among various Canadian implementation guides in parallel to the efforts to convene jurisdictional governing bodies and stakeholders to come to a consensus on the set of core use cases and contractual obligations.

#### Comparing a Baseline to a Core Implementation Guide

| Category | Baseline | Core |
|---|---|---|
| What support is needed from jurisdictions? | Public access to jurisdiction’s FHIR Implementation Guides (i.e. so we can see what constraints a jurisdiction’s projects currently have), use of the Canadian Baseline profiles as a starting point for jurisdictional implementation guides | Policy requirements, contract language, or incentives attached to use of the Core profiles, Jurisdictions need to identify and agree on the use cases / workflows supported by the Core profiles |
| Will implementers align to this without financial / jurisdictional / policy incentives? | Yes, minimal constraints with presence in existing implementations is a natural incentive in aligning new implementation guides to the baseline profiles & their minimum expectations | No. Restrictive constraints that require considerable configuration to be compliant can be a stumbling block in adoption to the profiles if incentives/disincentives are not present. |
| Origin | Community, Essentially “here are the constraints that are out there in FHIR implementations right now” | Policy, “These 10 use cases MUST be supported by every digital health product in the province, country” |
| Frequency / strength of constraints (re: both structure definition and business rules / usage notes) | Few strong constraints, only where deemed that any possible use of a concept would do it in the same way | More constraints, Tighter constraints, Each Core profile is designed to support a specific use case, so more constraints can be expected of implementers |

#### Maturing the Baseline
The process to develop and mature the Canadian Baseline Implementation Guide is outlined below.

<br>
<img src="BaselineRoadmap.png" alt="Baseline Maturity Roadmap" width="1200"/>
<br>

#### Profile Development Process
A profiling workstream and a governance workstream were established under the Infocentral FHIR Implementations Working Group.

The Governance stream developed a guiding document and terms of reference that defined the purpose and scope of the grassroots initiative. The Governance stream also developed the Baseline Maturity Roadmap that guided the review process found below.

The Profiling stream developed a process for review and split the 24 initial profiles (from the US Core profiles) into three substreams: Entity, Medication, and Clinical. These streams were led by Shamil Nizamov, Igor Sirkovich, and Scott Prior respectively. The vast majority of the initial 24 profiles are in-scope, however a small sub-section have been tabled until further notice; the decision was made to prioritize the review (both internal to the Community and externally) of the FHIR Profiles whose R4 Resources had reached a higher maturity level.

- The goal of the substreams was to position community leaders and subject matter experts to participate in profiling efforts related to their expertise and to expedite the profiling activities so they could occur in parallel.
- Substreams met weekly and used the Baseline principles developed in the Guiding Document.
- Profiling review periods and the updates from each of the substream were provided to the larger community on a bi-weekly basis during the profiling update calls.
- Participants on the substream calls varied based on the profile being reviewed, but included regional implementation guide authors, local and regional implementors, vendors, clinicians, and standards/terminology experts.
- Additional feedback was collected from the community via email and the projects Github issue log. Feedback issuers were reminded to participate in the calls that their feedback/suggestion was being reviewed and discussed.
- After agreement on the proposed changes on the call, the changes were tracked on spreadsheets and modifications were made to the specification in branched repositories.
- A change control process was put into place whereby substream leaders posted pull requests to the Github repository which were reviewed and accepted by a volunteer change manager (Russ Buchanan).

#### Review Process
The substreams reviewed proposed profiling changes with participants as part of the development process.

After the substreams completed their "first pass" at the profiles they were published to the Github repository and available through the Continuous Integration Build and Simplifier projects.

An initial due diligence review was identified as a critical process in maturing the profiles prior to being exposed to the larger FHIR community and tested in connectathons.
The review was intended to increase the fidelity of the profiles by comparing the initial draft of Canadian Baseline Profiles to a variety of domains and ‘live’ Canadian FHIR implementations. Non-Canadian, international specifications were also suggested by the Community at this stage, in an attempt to cover as many domains and use cases as possible.

The following domains and "live" implementation guides were identified for the due diligence review:
- Lab (ACCESS Gateway - Patient & Provider Access to Lab Results, Ontario Lab Information System FHIR Specification)
- Pharmacy/Medication (Alberta / Saskatchewan v3 Implementation, PrescribeIT specification, Ontario's Digital Health Drug Repository)
- Immunizations
- Registries (Ontario's Provincial Provider Registry, Ontario's Provincial Client Registry, Saskatchewan / British Columbia Jurisdictional Implementations - In Development)
- Patient Summaries (International Patient Summary)
- eReferral (Ontario's eReferral Specification)
- COVID-19 (LOGICA COVID-19 FHIR Specification)

### Implementation Guide Maturity
In the interest of exposing the internally reviewed profiles out to the community for more rapid feedback, we've identified the FHIR maturity level of the profiles and have noted the profiles that have gone through the initial due diligence review on the [artifacts page](artifacts.html).

#### FHIR Maturity Level
All artifacts in this specification are assigned a “Maturity Level”, known as FMM (after the well known CMM grades). The FMM level can be used by implementers to judge how advanced - and therefore stable - an artifact is. The following FMM levels are defined:

FMM 0 = The resource or profile (artifact) has been published on the current build. This level is synonymous with Draft.

FMM 1 = DRAFT 0 PLUS the artifact produces no warnings during the build process and the responsible WG has indicated that they consider the artifact substantially complete and ready for implementation.

FMM 2 = FMM 1 PLUS the artifact has been tested and successfully supports interoperability among at least three independently developed systems leveraging most of the scope (e.g. at least 80% of the core data elements) using semi-realistic data and scenarios based on at least one of the declared scopes of the artifact (e.g. at a connectathon). These interoperability results must have been reported to and accepted by the responsible working group.

FMM 3 = FMM 2 PLUS the artifact has been verified by the work group as meeting the Conformance Resource Quality Guidelines; has been subject to a round of formal balloting; has at least 10 distinct implementer comments recorded in the tracker drawn from at least 3 organizations resulting in at least one substantive change.

FMM 4 = FMM 3 PLUS the artifact is published in a formal publication (e.g. a FHIR Implementation Guide), and implemented in multiple prototype projects. As well, the responsible work group agrees the artifact is sufficiently stable to require implementer consultation for subsequent non-backward compatible changes.

FMM 5 = FMM 5 PLUS the artifact has been published in two formal publication release cycles at FMM1+ (i.e. Trial Use level) and has been implemented in at least 5 independent production systems.

Normative the artifact is now considered stable.
