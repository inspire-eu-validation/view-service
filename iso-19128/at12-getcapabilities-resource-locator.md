# Resource locator

**Purpose**: Test that a Resource Locator element is provided within the Extended Capabilities section.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check that a [Resource Locator](#ResourceLocator) element is provided within the [ExtendedCapabilities](#ExtendedCapabilities) element.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.4, Requirement 12

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a>      |   wms:Capability/inspire_vs:ExtendedCapabilities
ResourceLocator <a name="ResourceLocator"></a>      |   wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResourceLocator
