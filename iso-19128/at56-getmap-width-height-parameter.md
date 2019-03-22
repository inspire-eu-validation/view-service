# GetMap Width and Height Parameter

**Purpose**

Test that the WIDTH and HEIGHT parameters in GetMap operation are mandatory.

**Prerequisites**

**Test method**

* Send a GetMap request without WIDTH and HEIGHT parameters and all the other mandatory parameters.

    * Check that the service notifies the missing parameters.

* Send a GetMap request with an invalid WIDTH and HEIGHT parameters and all the other mandatory parameters.

    * Check that the service notifies the invalid parameters value.

* Send a GetMap request with valid integer values for WIDTH and HEIGHT parameters and all the other mandatory parameters.

    * Check that the service response is successful.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 56

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
