# Keyword within ExtendedCapabilities

**Purpose**: Test that keywords are mapped as Keyword and MandatoryKeyword elements into ExtendedCapabilities section.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](#scenario-2). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if keywords are mapped into [Keyword](#keyword) and [MandatoryKeyword](#mandatoryKeyword) elements within the inspire_vs:ExtendedCapabilities section. 

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.7, Requirement 18

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Keyword <a name="keyword"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:Keyword
MandatoryKeyword <a name="mandatoryKeyword"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MandatoryKeyword