# Temporal reference

**Purpose**: Test that at least one TemporalReference is given into the ExtendedCapabilities section.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if there is at least one [TemporalReference](#temporalReference) element within the inspire_vs:ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.9, Requirement 21

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
TemporalReference <a name="temporalReference"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference