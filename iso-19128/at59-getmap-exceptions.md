# GetMap Exceptions

**Purpose**: 

Test that the service accepts the optional parameter EXCEPTIONS.

**Prerequisites**

**Test method**

* Send a GetMap request without EXCEPTIONS parameter and wrong values for some mandatory parameters.

    * Check that the service response an exception in XML format.

* Send a GetMap request with EXCEPTIONS parameter set to XML and wrong values for some mandatory parameters.

    * Check that the service response an exception in XML format.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 59

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
