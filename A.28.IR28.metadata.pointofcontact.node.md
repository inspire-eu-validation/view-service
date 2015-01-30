# A.28.IR28.metadata.pointofcontact.node

**Purpose**: Since only one wms:ContactInformation element is allowed in ISO 19128 – WMS 1.3.0 (to which Responsible Organisation is mapped), an extension shall be used to map this to an element within an element.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is a MetadataPointOfContact node in the ExtendedCapabilities section.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.15

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataPointOfContact <a name="MetadataPointOfContact"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities
