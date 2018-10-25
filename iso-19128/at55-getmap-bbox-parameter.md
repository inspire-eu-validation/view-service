# GetMap BBOX Parameter

**Purpose**

Test that the BBOX paramater in GetMap operation is mandatory.

**Prerequisites**

**Test method**

* Send a GetMap request without BBOX parameter and all the other mandatory parameters.

    * Check that the service notify the missing parameter.

* Send a GetMap request with an invalid BBOX parameter and all the other mandatory parameters.

    * Check that the service notify the invalid parameter value.

* Send a GetMap request with valid list of comma-separated real numbers ('minx,miny,maxx,maxy') for BBOX parameter and all the other mandatory parameters.

    * Check that the service response is a correct document.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 55

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
