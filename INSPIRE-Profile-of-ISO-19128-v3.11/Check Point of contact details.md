# Check Point of contact details

**Purpose**: INSPIRE is more demanding than ISO 19115 by mandating both the name of the organisation, and a contact e-mail address. The role of the responsible party serving as a metadata point of contact is out of scope of the Metadata Regulation INS MD, but this property is mandated by ISO 19115. Its value shall be defaulted to “pointOfContact”.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.
* No metadata URL is given in test case [MetadataURL reference INSPIRE service metadata](MetadataURL reference INSPIRE service metadata.md)

**Test method**

* Check if there is a MetadataPointOfContact node in the ExtendedCapabilities section.
* If yes, check if there is a OrganisationName node and a EmailAddress node in the MetadataPointOfContact section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.15

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataPointOfContact <a name="MetadataPointOfContact"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities
OrganisationName <a name="OrganisationName"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact/inspire_common:OrganisationName
EmailAddress <a name="EmailAddress"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact/inspire_common:EmailAddress
