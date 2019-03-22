# GetMap CRS Parameter

**Purpose**

Test that the CRS parameter in GetMap operation is mandatory.

**Prerequisites**

**Test method**

* Send a GetMap request without CRS parameter and all the other mandatory parameters.

    * Check that the service notifies the missing parameter.

* Send a GetMap request with an invalid CRS parameter and all the other mandatory parameters.

    * Check that the service notifies the invalid parameter value.

* Send a GetMap request with a value from [INSPIRE](./README.md#ref_INSPIRE) for CRS parameter and all the other mandatory parameters.

    * Check that the service response is successful.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 54
* [INSPIRE](./README.md#ref_INSPIRE), Annex I, theme 1, Coordinate Reference System

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
