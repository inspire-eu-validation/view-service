# GetMap Version Parameter

**Purpose**

Test that the VERSION parameter in GetMap operation is mandatory.

**Prerequisites**

**Test method**

* Send a GetMap request without VERSION parameter and all the other mandatory parameters.

    * Check that the service notifies the missing parameter.

* Send a GetMap request with an invalid VERSION parameter and all the other mandatory parameters.

    * Check that the service notifies the invalid parameter value.

* Send a GetMap request with '1.3.0' value for VERSION parameter and all the other mandatory parameters.

    * Check that the service response is successful.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 50

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
