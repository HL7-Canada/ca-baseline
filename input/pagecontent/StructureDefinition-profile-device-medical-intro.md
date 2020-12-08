# CA Baseline Device (Medical and Non-medical) Profile
This profile sets minimum expectations for the Device resource to record and search for medical and non-medical devices, wearable devices personal health devices, virtual devices such as computer programs and systems, etc., except patient's implantable device(s). 
It identifies which core elements SHALL be present in the resource when using this profile.

This profile defines core localization concepts for use in the Canadian context.

## Mandatory Data Elements
All elements or attributes within the FHIR specification have cardinality as part of their definition - a minimum number of required appearances and a maximum number of allowable appearances.

Most elements in the FHIR specification have a minimum cardinality of 0, so most elements are not required and subsequently they may be missing from a resource when it is exchanged between systems.

**Required elements in the Device (Implantable) profile:**
* The type of the device (Device.type)

## Must Support Data Elements
Some elements are marked as Must Support. This means that implementations generating, receiving, or otherwise using resources with Must Support elements SHALL provide support for those elements in some meaningful way (see Must Support definition).

The following elements are marked as Must Support in the Device (Medical and Non-medical) profile:

**Must Support elements:**
* Device resource identifier
* Unique Device Identifier (UDI) Barcode string
* distinct identification string
* device manufacturer
* date/time when the device was made
* expiration date/time of the device
* serial number assigned by the manufacturer
* name of the device
* type of the device 
* version of the device
* patient

## Usage Note
The following are example usage scenarios for the Medical and Non-medical Device profile:
* To record and query information about Personal Health Devices (PHDs) to be used in remote patient monitoring programs.
* To record and query information about the Virtual Medical Device installed as software on the computer system.