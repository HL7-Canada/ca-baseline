# CA Baseline Device (Implantable) Profile
<div xmlns="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
	<blockquote class="stu-note">
		<p>This profile is seeking broader community and implementer feedback on this profile.
    <br>
    <br>
    The clinical substream review of this profile is paused until a Subject Matter Expert can be found who can speak to the use of implantable device data in Canada. Due to a lack of current Canadian FHIR implementation guides that surface a device profile - this profile has not undergone a Due Diligence Review and should be treated with caution until more community feedback can be acquired. <a href="https://simplifier.net/CanadianFHIRBaselineProfilesCA-Core/deviceprofileimplantable/~issues">Simplifier issue log for this profile</a>.</p>
	</blockquote>
  </div>

This profile sets minimum expectations for the Device resource to record, search, and fetch UDI information associated with a patient's implantable device(s).
It identifies which core elements SHALL be present in the resource when using this profile.

This profile defines core localization concepts for use in the Canadian context.

## Mandatory Data Elements
{% include mandatoryguidance.xml %}


## Usage Note
The following are example usage scenarios for the implantable Device profile:
* Query for a patient's implantable devices
* Record or update a patient implantable device information
