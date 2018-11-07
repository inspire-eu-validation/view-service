# MetadataURL references INSPIRE service metadata

**Purpose**: Test that metadata is referenced through the MetadataURL element within the ExtendedCapabilities section.

**Prerequisites**

**Test method**

This test only applies to [scenario 1](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if the [MetadataURL](#metadataURL) element mapped into the extended capabilities section within the Capability element is used to reference the INSPIRE service metadata available through an INSPIRE Discovery Service.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 6

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataURL <a name="metadataURL"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataURL
