# Point of Contact in Extended Capabilities

**Purpose**: Test that a MetadataPointOfContact element is provided within the ExtendedCapabilities section.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check that at least one [MetadataPointOfContact](#MetadataPointOfContact) element is provided into the [ExtendedCapabilities](#ExtendedCapabilities) section.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.15, Requirement 28

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a> | wms:Capability/inspire_vs:ExtendedCapabilities
MetadataPointOfContact <a name="MetadataPointOfContact"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact