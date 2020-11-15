FHIR transactions often make use of patient-specific information which could be exploited by malicious actors resulting in exposure of patient data. For this reason, all transactions must be secured appropriately with access to limited authorized individuals, data protected in transit, and appropriate audit measures taken.

Implementers should be aware of the [security considerations] associated with FHIR transactions, particularly those related to:

-   [Communications]
-   [Authentication]
-   [Authorization/Access Control]
-   [Audit Logging]
-   [Digital Signatures]
-   [Security Labels]
-   [Narrative]

**Security Conformance Requirements may be added here later.**


  [FHIR Communications]: {{site.data.fhir.path}}security.html#http
  [Smart On FHIR]: http://fhir-docs.smarthealthit.org/argonaut-dev/authorization/backend-services/
  [FHIR Security Labels]: {{site.data.fhir.path}}security-labels.html
  [FHIR Provenance]: {{site.data.fhir.path}}provenance.html
  [FHIR Digital Signatures]: {{site.data.fhir.path}}security.html#digital%20signatures

  [security considerations]: {{site.data.fhir.path}}security.html
  [Communications]: {{site.data.fhir.path}}security.html#http
  [Authentication]: {{site.data.fhir.path}}security.html#authentication
  [Authorization/Access Control]: {{site.data.fhir.path}}security.html#authorization/access%20control
  [Audit Logging]: {{site.data.fhir.path}}security.html#audit%20logging
  [Digital Signatures]: {{site.data.fhir.path}}security.html#digital%20signatures
  [Security Labels]: {{site.data.fhir.path}}security-labels.html
  [Narrative]: {{site.data.fhir.path}}security.html#narrative
  [AuditEvent]: {{site.data.fhir.path}}auditevent.html
  [Audit Logging]: {{site.data.fhir.path}}security.html#audit
  [Consent]: {{site.data.fhir.path}}consent.html
