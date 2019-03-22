# GetMap Layers Parameter

**Purpose**

Test that the LAYERS parameter in GetMap operation is mandatory.

**Prerequisites**

**Test method**

* Send a GetMap request without LAYERS parameter and all the other mandatory parameters.

    * Check that the service notifies the missing parameter.

* Send a GetMap request with an invalid LAYERS parameter and all the other mandatory parameters.

    * Check that the service notifies the invalid parameter value.

* Send a GetMap request with a valid layer value for LAYERS parameter and all the other mandatory parameters.

    * Check that the service response is successful.

* Send a GetMap request with a valid list of layers separated by commas value for LAYERS parameter and all the other mandatory parameters.

    * Check that the service response is successful.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 52

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
