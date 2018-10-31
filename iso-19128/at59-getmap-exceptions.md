# GetMap Exceptions

**Purpose**: 

Test that the service accepts the optional parameter EXCEPTIONS.

**Prerequisites**

**Test method**

* Send a GetMap request without EXCEPTIONS parameter and all the other mandatory parameters.

    * Check that the service response is successful and the default EXCEPTIONS is XML.

* Send a GetMap request with an invalid EXCEPTIONS parameter and all the other mandatory parameters.

    * Check that the service notify the invalid parameter value.

* Send a GetMap request with a valid EXCEPTIONS parameter (INIMAGE or BLANK) and all the other mandatory parameters.

    * Check that the service response is successful.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 59

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
