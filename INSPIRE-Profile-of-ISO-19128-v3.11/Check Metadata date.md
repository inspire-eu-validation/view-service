# Check Metadata date

**Purpose**: As the Metadata Date is not supported by ISO 19128 – WMS 1.3.0, an extension shall be used to map this to an element within an element. The date shall be expressed in conformity with the INS MD.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.
* No metadata URL is given in test case [MetadataURL reference INSPIRE service metadata](MetadataURL reference INSPIRE service metadata.md)

**Test method**

* Check if there is a MetadataDate node in the ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.16

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataDate <a name="MetadataDate"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataDate
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities
