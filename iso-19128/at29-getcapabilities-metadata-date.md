# Metadata Date
**Purpose**: Test that is provided a MetadataDate element within the ExtendedCapabilities section.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if a [MetadataDate](#MetadataDate) element is provided within the ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.16, Requirement 29

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataDate <a name="MetadataDate"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataDate