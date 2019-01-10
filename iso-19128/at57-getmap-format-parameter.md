# GetMap Format Parameter

**Purpose**

Test that the FORMAT paramater in GetMap operation is mandatory.

**Prerequisites**

**Test method**

* Send a GetMap request without FORMAT parameter and all the other mandatory parameters.

    * Check if the service notifies the missing parameter.

* Send a GetMap request with an invalid FORMAT parameter and all the other mandatory parameters.

    * Check if the service notifies the invalid parameter value.

* Send a GetMap request with 'image/png' for FORMAT parameter and all the other mandatory parameters.

* Send a GetMap request with 'image/gif' for FORMAT parameter and all the other mandatory parameters.

* Check that at least one of the two previous requests get a successful response.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 57

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
