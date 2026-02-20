# CA Baseline Procedure Profile
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
	<blockquote class="stu-note">
		<p>This profile is seeking broader community and implementer feedback.
    <br>
    <br>
    The cardinality on procedure.performed[x] has been constrained to 1..1. While this did not cause any Due Diligence Review Issues with IPS or US Core, we are seeking feedback from additional implementers on whether this cardinality restriction poses problems for their FHIR implementations.
    <br>
    <br>
    Feedback can be provided using the <a href="https://simplifier.net/CanadianFHIRBaselineProfilesCA-Core/procedureprofile/~issues">Simplifier issue log for this profile</a>.
    </p>
	</blockquote>
  </div>

This profile sets minimum expectations for the Procedure resource to record, search and fetch current or historical procedures performed on or for a patient. It identifies which elements and value sets SHALL be present in the resource when using this profile.

This profile defines localization concepts for use in an Canadian context.

## Mandatory Data Elements
All elements or attributes defined in FHIR have cardinality as part of their definition - a minimum number of required appearances and a maximum number.

Most elements in FHIR specification have a minimum cardinality of **0**, which means that they may be missing from a resource when it is exchanged between systems.

**Required elements:**
* status specifying the state of the procedure (required in the base specification)
* code to classify the procedure that is performed
* reference to a subject
* date procedure was performed

## Usage Note
This Procedure profile is used to provide summary information about the occurrence of current or historical procedures performed on or for a patient, and is not intended to provide real-time snapshots of a procedure as it unfolds.
Examples include surgical procedures, diagnostic procedures, endoscopic procedures, biopsies, counseling, physiotherapy, personal support services, adult day care services, non-emergency transportation, home modification, exercise and so on.

A slice for absentOrUnknownProcedure comes from the IPS-UV specification and has been socialized in the profile as a way to represent a standard set of codes for identifying absent or unknown procedures. While the profile expects that a procedure.code be present (cardinality of 1..1) the use of the slice is entirely optional.  
