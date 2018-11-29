# GetMap Transparent Parameter

**Purpose**:

Test that the service accepts the optional parameter TRANSPARENT.

**Prerequisites**

**Test method**

* Send a GetMap request without TRANSPARENT parameter and all the other mandatory parameters.

    * Check if the service response is successful.

* Send a GetMap request with an invalid TRANSPARENT parameter and all the other mandatory parameters.

    * Check if the service notify the invalid parameter value.

* Send a GetMap request with a valid TRANSPARENT parameter and all the other mandatory parameters.

    * Check if the service response is successful.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 58

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
