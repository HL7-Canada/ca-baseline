# CA Baseline Organization Profile

This Organization profile sets minimum expectations for the Organization resource to record, search and fetch a formally or informally recognized grouping of people or organizations formed for the purpose of achieving some form of collective action.

This profile defines localization concepts for use in a Canadian context.

## Mandatory Data Elements

All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of 0, which means that they may be missing from a resource when it is exchanged between systems.

In this Canadian Baseline Organization Profile all elements are optional, i.e., there is no element with a minimum cardinality of 1. However, some optional elements (e.g., identifier) have required components that MUST be present if that optional element is provided.

## Must Support Data Elements

Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/HL7-Canada/ca-baseline/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the Canadian Organization profile to aid record matching in databases with many pediatric records.

**Must Support elements:**

* an identifier
* an organization name
* contact detail (e.g. a telephone number or an email address)
