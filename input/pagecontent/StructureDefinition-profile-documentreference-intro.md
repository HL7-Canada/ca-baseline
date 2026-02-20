# CA Core DocumentReference Profile
This DocumentReference profile sets minimum expectations for mandatory core elements, constraints and value sets required to provide metadata about the document of any kind so that the document can be published, discovered and managed.

This profile defines core localisation concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* status of the refence
* document referenced


## Usage Note

The following are example usage scenarios for the DocumentReference profile.

* Publishing a new document. This can be done using the [IHE MHD Provide Document Bundle [ITI-65]](https://wiki.ihe.net/index.php/Mobile_access_to_Health_Documents_(MHD)) transaction that carries both the document and its metadata.
* Querying the document repository for specific document(s) matching various metadata parameters. This is similar to the IHE MHD Find Document References [ITI-67] transaction.
