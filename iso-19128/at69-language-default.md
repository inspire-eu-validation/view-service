# Language Default

**Purpose**:

Test that Titles and Abstracts are not affected when the LANGUAGE parameter is absent or unsupported.

**Prerequisites**

**Test method**

* Send a GetCapabilities request without LANGUAGE parameter.

* Send a GetCapabilities request with an invalid LANGUAGE parameter.

    * Check that Titles and Abstracts fields are the same as default ones.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 69

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
