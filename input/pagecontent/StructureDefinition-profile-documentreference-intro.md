# CA Core DocumentReference Profile
This DocumentReference profile sets minimum expectations for mandatory core elements, constraints and value sets required to provide metadata about the document of any kind so that the document can be published, discovered and managed.

This profile defines core localisation concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* status of the refence
* document referenced

## Must Support Data Elements
Some elements are labeled as MustSupport meaning that implementations that produce or consume resources SHALL provide "support" for the element in some meaningful way (see [Must Support](https://build.fhir.org/ig/scratch-fhir-profiles/ca-baseline/general-guidance.html#must-support) definition).

Following elements are marked as Must Support in the Canadian DocumentReference profile to aid record matching in databases.

**Must Support elements:**
* master version identifier
* kind of document
* categorization of document
* subject of the document
* document author
* document authenticator
* organization which maintains the document
* the document itself or URL
* context of the document content
* practice settings
* patient demographics

## Usage Note

The following are example usage scenarios for the DocumentReference profile.

* Publishing a new document. This can be done using the [IHE MHD Provide Document Bundle [ITI-65]](https://wiki.ihe.net/index.php/Mobile_access_to_Health_Documents_(MHD)) transaction that carries both the document and its metadata.
* Querying the document repository for specific document(s) matching various metadata parameters. This is similar to the IHE MHD Find Document References [ITI-67] transaction.
