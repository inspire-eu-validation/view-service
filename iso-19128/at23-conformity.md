# Conformity

**Purpose**: Test that is provided a Conformity element into the Extended Cpabilities section.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if is provided at least one [Conformity](#Conformity) element within the ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.11, Requirement 23

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Conformity <a name="Conformity"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity