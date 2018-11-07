# Resource type is service

**Purpose**: Test that a ResourceType element is given and the value is fixed to 'service'.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if there is a [ResourceType](#ResourceType) node into the inspire_vs:ExtendedCapabilities section. If true,

    * Check that the value is fixed to 'service'.

  * In any other case the test fails.

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.3, Requirement 11
* [INS MD](./README.md#ref_INS_MD), Part D.1

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ResourceType <a name="ResourceType"></a>   |    wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResourceType
