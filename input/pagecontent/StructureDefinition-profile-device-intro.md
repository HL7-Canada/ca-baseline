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
All elements or attributes within the FHIR specification have cardinality as part of their definition - a minimum number of required appearances and a maximum number of allowable appearances.

Most elements in the FHIR specification have a minimum cardinality of 0, so most elements are not required and subsequently they may be missing from a resource when it is exchanged between systems.

**Required elements in the Device (Implantable) profile:**
* A Unique Device Identifier (UDI) numeric or alphanumeric code (Device.deviceIdentifier):
  * either as the Human Readable Form (HRF) string representation of the barcode (Device.carrierHRF)
  * or the Automatic Identification and Data Capture representation (Device.carrierAIDC)
* The type of the device (Device.type)
* A patient (Device.patient)

## Must Support Data Elements
Some elements are marked as Must Support. This means that implementations generating, receiving, or otherwise using resources with Must Support elements SHALL provide support for those elements in some meaningful way (see Must Support definition).

The following elements are marked as Must Support in the Device (Implantable) profile:

**Must Support elements:**
* Unique Device Identifier (UDI) Barcode string
* distinct identification string
* device manufacturer
* expiration date/time of the device
* lot number of manufacture
* serial number assigned by the manufacturer
* name of the device
* type of the device
* version of the device
* patient

## Usage Note
The following are example usage scenarios for the implantable Device profile:
* Query for a patient's implantable devices
* Record or update a patient implantable device information
